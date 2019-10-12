---
title: Détails de conception - Flux d'enlogement sortant | Microsoft Docs
description: Le flux sortant dans l'entrepôt commence par une demande provenant des documents origine lancés pour amener les articles hors de l'entrepôt, pour les expédier soit à un tiers, soit à un autre magasin de la société. Depuis la zone de stockage, des activités entrepôt sont effectuées à différents niveaux de complexité pour sortir les articles pour les amener au quai d'expédition.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c5a3ce2049b1686da04842f7c73abb2255369ffa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307003"
---
# <a name="design-details-outbound-warehouse-flow"></a>Détails de conception : flux de désenlogement
Le flux sortant dans l'entrepôt commence par une demande provenant des documents origine lancés pour amener les articles hors de l'entrepôt, pour les expédier soit à un tiers, soit à un autre magasin de la société. Depuis la zone de stockage, des activités entrepôt sont effectuées à différents niveaux de complexité pour sortir les articles pour les amener au quai d'expédition.  

 Chaque article est identifié et mis en correspondance avec un document origine entrant correspondant. Les documents origine sortants suivants existent :  

- Commande vente  
- Commande désenlogement transfert  
- Retour commande achat  
- Commande service  

En outre, les documents origine internes suivants existent qui fonctionnent comme des sources sortantes :  

- Ordre de fabrication avec besoin de composant  
- Ordre d'assemblage avec besoin de composant  

 Les deux derniers documents représentent les flux sortants de l'entrepôt vers les zones d'opération internes. Pour plus d'informations sur l'activité entrepôt pour les processus enlogement et désenlogement internes, reportez\-vous à [Détails de conception : flux d'entrepôt internes](design-details-internal-warehouse-flows.md).  

 Les processus et les documents de l'interface utilisateur dans les flux de désenlogement sont différents pour les configurations d'entrepôt de base et avancées. La principale différence est que les activités sont effectuées par commande dans les configurations d'entrepôt de base, et qu'elles sont regroupées pour plusieurs commandes dans les configurations d'entrepôt avancées. Pour plus d'informations sur les différents niveaux de complexité entrepôt, consultez [Détails de conception : vue d'ensemble d'entrepôt](design-details-warehouse-setup.md).  

 Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les processus sortants de prélèvement et d'expédition peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt.  

|Méthode|Processus entrant|Emplacements|Prélèvements|Livraisons|Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l'expédition à partir de la ligne commande|X|||2|  
|B|Validation du prélèvement et de l'expédition à partir d'un document prélèvement stock||X||3|  
|C|Validation du prélèvement et de l'expédition à partir d'un document expédition entrepôt|||X|5/4/6|  
|J|Validation du prélèvement à partir d'un document prélèvement entrepôt et validation de l'expédition à partir d'un document expédition entrepôt||X|X|5/4/6|  

 Sélectionner une méthode dépend des pratiques recommandées de la société et de la complexité de son organisation. Dans un environnement par commande avec des processus et une structure d'emplacement simples, la méthode A, de prélèvement et d'expédition à partir de la ligne commande, est appropriée. Dans d'autres sociétés par commande où les articles d'une ligne commande peuvent provenir de plusieurs emplacements et où les magasiniers ne peuvent pas utiliser des documents commande, l'utilisation des différents documents prélèvement est appropriée, la méthode B. Lorsque les processus de prélèvement et d'expédition d'une société impliquent plusieurs traitements de commande et donc requièrent davantage de contrôle et de supervision, la société peut choisir d'utiliser un document expédition entrepôt et un document prélèvement entrepôt afin de séparer les tâches de prélèvement et d'expédition, les méthodes C et D.  

 Dans les méthodes A, B et C, les actions de prélèvement et d'expédition sont combinées en une étape lors de la validation du document correspondant comme étant expédié. Dans la méthode D, le prélèvement est d'abord validé, puis l'expédition est validée à une date ultérieure à partir d'un document différent.  

## <a name="basic-warehouse-configurations"></a>Configurations d'entrepôt de base  
 Le schéma suivant présente les flux de désenlogement par type de document dans les configurations d'entrepôt de base. Les numéros dans le schéma correspondent aux étapes dans les sections suivant le schéma.  

 ![Flux sortant dans les configurations d'entrepôt de base](media/design_details_warehouse_management_outbound_basic_flow.png "Flux sortant dans les configurations d'entrepôt de base")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1 : Lancer le document origine / Créer un prélèvement stock ou un mouvement de stock  
 Lorsqu'un utilisateur responsable des documents d'origine, comme un préparateur de commandes ou un gestionnaire de production, est prêt pour l'activité d'entrepôt sortant, il émet le document d'origine pour signaler aux magasiniers que les articles ou les composants vendus peuvent être prélevés et placés dans les emplacements spécifiés. Sinon, l'utilisateur crée des documents de prélèvement ou de mouvement de stock pour les lignes de commande individuelles, en mode de poussée, basés sur les emplacements spécifiés et quantités à gérer.  

> [!NOTE]  
>  Des mouvements de stock sont utilisés pour déplacer des articles vers des zones d'opération interne dans les configurations d'entrepôt de base, sur la base des documents origine ou sur une base ad-hoc.  

### <a name="2-create-outbound-request"></a>2 : Créer demande désenlogement  
 Lorsque le document d'origine sortant est émis, une demande d'entrepôt sortant est automatiquement créée. Elle contient des références au type et au numéro du document origine et n'est pas visible à l'utilisateur.  

### <a name="3-create-inventory-pick-or-movement"></a>3 : Créer un prélèvement stock ou un mouvement de stock  
 Sur la page **Prélèvement stock** ou **Mouvement de stock**, le magasinier extrait, en mode extraction, les lignes document origine en attente en fonction des demandes désenlogement. Sinon, les lignes prélèvement stock sont déjà créées, par déplacement, par l'utilisateur responsable du document origine.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Valider un prélèvement stock ou enregistrer un mouvement de stock  
 Sur chaque ligne pour les articles qui ont été prélevées ou déplacés, entièrement ou partiellement, le magasinier renseigne le champ **Quantité**, puis valide le prélèvement stock ou enregistre le mouvement de stock. Les documents origine associé au prélèvement stock sont validés comme étant expédiés ou consommés. Les documents origine liés aux mouvements de stock ne sont pas validés.  

 Pour les prélèvements stock, les écritures comptables article négatives sont créées, les écritures entrepôt sont créées, et la demande de prélèvement est supprimée, si entièrement enregistrée. Par exemple, le champ **Qté expédiée** sur la ligne document origine sortant est mis à jour. Un document expédition validé est créé et indique la commande vente, par exemple, ainsi que les articles expédiés.  

## <a name="advanced-warehouse-configurations"></a>Configurations d'entrepôt avancées  
 Le schéma suivant présente le flux de désenlogement par type de document dans les configurations d'entrepôt avancées. Les numéros dans le schéma correspondent aux étapes dans les sections suivant le schéma.  

 ![Flux sortant dans les configurations d'entrepôt avancées](media/design_details_warehouse_management_outbound_advanced_flow.png "Flux sortant dans les configurations d'entrepôt avancées")  

### <a name="1-release-source-document"></a>1 : Lancer le document origine  
 Lorsqu'un utilisateur responsable des documents d'origine, comme un préparateur de commandes ou un gestionnaire de production, est prêt pour l'activité d'entrepôt sortant, il émet le document d'origine pour signaler aux magasiniers que les articles ou les composants vendus peuvent être prélevés et placés dans les emplacements spécifiés.  

### <a name="2-create-outbound-request"></a>2 : Créer demande désenlogement  
 Lorsque le document d'origine entrant est émis, une demande d'entrepôt sortant est automatiquement créée. Elle contient des références au type et au numéro du document origine et n'est pas visible à l'utilisateur.  

### <a name="3-create-warehouse-shipment"></a>3 : Créer expédition entrepôt  
 Sur la page **Expédition entrepôt**, le responsable de l'expédition extrait les lignes document origine en attente en fonction de la demande désenlogement. Plusieurs lignes document origine peuvent être combinées dans un document expédition entrepôt.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4 : Lancer l'expédition / Créer un prélèvement entrepôt  
 Le responsable de l'expédition lance l'expédition entrepôt, afin que les magasiniers puissent créer ou coordonner des prélèvements entrepôt pour l'expédition en question.  

 Sinon, l'utilisateur crée des documents prélèvement entrepôt pour des lignes expédition individuelles, par déplacement, selon les emplacements spécifiés et les quantités à traiter.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5 : Lancer une opération interne / Créer un prélèvement entrepôt  
 L'utilisateur qui est responsable des opérations internes émet un document origine interne, tel qu'un ordre de fabrication et d'assemblage, afin que les magasiniers puissent créer ou coordonner des prélèvements entrepôt pour l'opération interne en question.  

 Sinon, l'utilisateur crée des documents prélèvement entrepôt pour l'ordre de fabrication ou l'ordre d'assemblage individuel, par déplacement, selon les emplacements spécifiés et les quantités à traiter.  

### <a name="6-create-pick-request"></a>6 : Créer une demande de prélèvement  
 Lorsque le document d'origine sortant est émis, une demande de prélèvement d'entrepôt est automatiquement créée. Elle contient des références au type et au numéro du document origine et n'est pas visible à l'utilisateur. En fonction de la configuration, la consommation d'un ordre de fabrication et d'un ordre d'assemblage génère également une demande de prélèvement pour prélever les composants nécessaires dans le stock.  

### <a name="7-generate-pick-worksheet-lines"></a>7 : Générer des lignes feuille prélèvement  
 L'utilisateur qui est responsable de coordonner les prélèvements copie des lignes de prélèvement entrepôt dans la **Feuille prélèvement** en fonction des demandes de prélèvement des expéditions entrepôt ou des opérations internes pour la consommation des composants. L'utilisateur sélectionne les lignes à prélever et prépare les prélèvements en spécifiant à partir de quels emplacements les prendre, à quels emplacements les placer, et le nombre d'unités à traiter. Les emplacements peuvent être prédéfinis par la configuration d'un entrepôt ou d'une ressource d'opération.  

 L'utilisateur spécifie des méthodes de prélèvement pour la gestion d'entrepôt optimisée puis utilise une fonction pour créer les documents de prélèvement entrepôt correspondants, qui sont affectés aux différents magasiniers exécutant les prélèvements entrepôt. Lorsque les prélèvements entrepôt sont entièrement affectés, les lignes dans la **Feuille prélèvement** sont supprimées.  

### <a name="8-create-warehouse-pick-documents"></a>8 : Créer des documents prélèvement entrepôt  
 Le magasinier qui effectue des prélèvements crée un document de prélèvement entrepôt, sur le mode de l'extraction, basé sur le document origine émis. Sinon, le document prélèvement entrepôt est créé et affecté au magasinier par déplacement.  

### <a name="9-register-warehouse-pick"></a>9 : Enregistrer un prélèvement entrepôt  
 Sur chaque ligne pour les articles qui ont été prélevés, entièrement ou partiellement, le magasinier renseigne le champ **Quantité** sur la page **Prélèvement entrepôt**, puis enregistre le prélèvement entrepôt.  

 Les écritures d'entrepôt sont créées, et les lignes de prélèvement entrepôt sont supprimées, si entièrement traitées. Le document de prélèvement entrepôt reste ouvert jusqu'à ce que la quantité totale de l'expédition entrepôt associée soit validée. Le champ **Qté prélevée** sur les lignes expédition entrepôt est mis à jour en conséquence.  

### <a name="10-post-warehouse-shipment"></a>10 : Valider expédition entrepôt  
 Lorsque tous les articles dans le document d'expédition entrepôt sont enregistrés comme prélevés dans les emplacements d'expédition spécifiés, le magasinier responsable valide l'expédition entrepôt. Des écritures comptables article négatives sont créées. Par exemple, le champ **Qté expédiée** sur la ligne document origine sortant est mis à jour.  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)
