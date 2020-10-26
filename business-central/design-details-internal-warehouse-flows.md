---
title: Détails de conception - Flux d’entrepôt internes | Microsoft Docs
description: Circulation des articles entre les emplacements dans les centres d’une société lors du prélèvement des composants, du rangement des articles finis pour les ordres d’assemblage ou de fabrication et les mouvements ad-hoc, tels que les réapprovisionnements emplacement, sans relation avec les documents origine.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dd07d7d25bea1e49ffa4927a717088663c5d48da
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911045"
---
# <a name="design-details-internal-warehouse-flows"></a>Détails de conception : flux d’entrepôt internes
Circulation des articles entre les emplacements dans les centres d’une société lors du prélèvement des composants, du rangement des articles finis pour les ordres d’assemblage ou de fabrication et les mouvements ad-hoc, tels que les réapprovisionnements emplacement, sans relation avec les documents origine. La portée et la nature des activités impliquées varient entre l’entreposage de base et l’entreposage avancé.  

 Certains flux internes chevauchent des flux entrants ou sortants. Une partie de cette superposition est illustrée aux étapes 4 et 5 dans les schémas graphiques des flux enlogement et désenlogement avancés respectivement. Pour plus d’informations, reportez\-vous à [Détails de conception : flux d’enlogement](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Flux internes dans l’entreposage de base  
 Dans une configuration entrepôt de base, la circulation des articles entre les emplacements dans les centres de la société lors du prélèvement des composants, du rangement des articles finis pour les ordres de fabrication ou les ordres d’assemblage et les mouvements ad-hoc, tels que les réapprovisionnements emplacement, sans relation avec les documents origine.  

### <a name="flows-to-and-from-production"></a>Flux entrants et sortants de la production  
 La principale intégration entre les ordres de fabrication et les activités d’entrepôt de base est représentée par la capacité de prélever des composants de production à l’aide de la page **Prélèvement stock** ou **Mouvement de stock** .  

> [!NOTE]  
>  Sur la page **Prélèvement stock** , la consommation de composants est validée lors de la validation du prélèvement. À l’aide de la page **Mouvement de stock** , seuls les ajustements d’emplacement sont enregistrés, aucune validation dans la comptabilité article n’a lieu.  

 En plus de la gestion de composants, l’intégration est représentée par la capacité de ranger les articles fabriqués à l’aide de la page **Rangement stock** .  

 Les champs **To-Production Bin Code** , **From-Production Bin Code** , et **Open Shop Floor Bin Code** de la fiche magasin ou des fiches poste/centre de charge définissent les flux par défaut depuis ou vers les zones de production.  

 Pour plus d’informations sur la manière dont la consommation de composants est vidée des emplacements des consommations ou des emplacements atelier ouverts, reportez-vous à la section « Consommation des composants de production dans l’entrepôt » de cette rubrique.  

### <a name="flows-to-and-from-assembly"></a>Flux entrants et sortants de l’assemblage  
 La principale intégration entre les ordres d’assemblage et les activités d’entrepôt de base est représentée par la capacité de déplacer les composants d’assemblage vers la zone d’assemblage.  

 Lorsqu’aucune fonctionnalité entrepôt spécifique n’existe pour le stockage des éléments d’assemblage, le code d’emplacement sur l’ordre d’assemblage peut être défini sur un emplacement de stockage par défaut. La validation de l’ordre d’assemblage fonctionne alors comme la validation d’un rangement. L’activité entrepôt pour déplacer des éléments d’assemblage dans l’entrepôt peut être gérée sur la page **Mouvement interne** , sans rapport avec l’ordre d’assemblage.  

 Les flux d’assemblage suivants existent.  

|Flux de travail|Désignation|  
|----------|---------------------------------------|  
|Assembler pour stock|Les composants sont nécessaires sur un ordre d’assemblage dans lequel la production est stockée dans l’entrepôt.<br /><br /> Ce flux d’entrepôt est géré sur la page **Mouvement de stock** . Une ligne prélèvement spécifie où prélever les composants. Une ligne d’emplacement spécifie où placer les composants.|  
|Assembler pour commande|Les composants sont nécessaires sur un ordre d’assemblage qui est lié à une commande vente expédiée lors de l’assemblage de l’article vendu.|  

> [!NOTE]  
>  Si les articles sont assemblés pour commande, le prélèvement stock de la commande vente liée déclenche un mouvement de stock pour tous les composants d’assemblage impliqués, et non seulement pour l’article vendu, comme lors de l’expédition d’articles en stock.  

 Les champs **Code empl. vers assemblage** , **Code empl. depuis assemblage** et **Code empl. exp. ass. pr comm.** de la fiche magasin définissent les flux par défaut depuis et vers les champs d’assemblage.  

> [!NOTE]  
>  Le champ **Code empl. exp. ass. pr comm.** fonctionne comme emplacement après assemblage dans les scénarios assembler pour commande.  

### <a name="ad-hoc-movements"></a>Mouvements ad hoc  
 Dans l’entreposage de base, un mouvement d’articles d’un emplacement à un autre sans relation avec les documents origine est effectué sur la page **Mouvement interne** qui fonctionne conjointement avec la page **Mouvement de stock** .  

 Il existe un autre moyen de déplacer des articles ad hoc entre les emplacements : il suffit de valider les écritures positives dans le champ **Nouveau code emplacement** de la page **Feuille reclassement article** .  

## <a name="internal-flows-in-advanced-warehousing"></a>Flux internes dans l’entreposage avancé  
 Dans les configurations d’entrepôt avancées, la circulation des articles entre les emplacements dans les centres de la société lors du prélèvement des composants, du rangement des articles finis pour les ordres de fabrication et du prélèvement des composants pour les ordres d’assemblage. En outre, les flux internes se produisent en tant que mouvements ad-hoc, tels que les réapprovisionnements emplacement, sans relation avec les documents origine.  

### <a name="flows-to-and-from-production"></a>Flux entrants et sortants de la production  
 La principale intégration entre les ordres de fabrication et les activités d’entrepôt avancées est représentée par la capacité de prélever des composants de production, sur la page **Prélèvement entrepôt** et sur la page, **Feuille prélèvement** , et par la capacité de ranger des articles fabriqués à l’aide de la page **Rangement interne entrepôt** .  

 Un autre point d’intégration dans la production est fourni via la page **Mouvement entrepôt** , ainsi que la page Feuille mouvement, ce qui vous permet de placer des composants et de prendre des articles fabriqués pour des ordres de fabrication lancés.  

 Les champs **To-Production Bin Code** , **From-Production Bin Code** , et **Open Shop Floor Bin Code** de la fiche magasin ou des fiches poste/centre de charge définissent les flux par défaut depuis ou vers les zones de production.  

 Pour plus d’informations sur la manière dont la consommation de composants est vidée des emplacements des consommations ou des emplacements atelier ouverts, reportez-vous à la section « Consommation des composants de production dans l’entrepôt » de cette rubrique.  

### <a name="flows-to-and-from-assembly"></a>Flux entrants et sortants de l’assemblage  
 La principale intégration entre les ordres d’assemblage et les activités d’entrepôt avancées est représentée par la capacité de prélever des composants d’assemblage, aussi bien à l’aide de la page **Prélèvement entrepôt** que de la page **Feuille prélèvement** . Cette fonctionnalité est identique au prélèvement des composants pour les ordres de fabrication.  

 Lorsqu’aucune fonctionnalité entrepôt spécifique n’existe pour le stockage des éléments d’assemblage, le code d’emplacement sur l’ordre d’assemblage peut être défini sur un emplacement de stockage par défaut. La validation de l’ordre d’assemblage fonctionne alors comme la validation d’un rangement. L’activité entrepôt pour déplacer des éléments d’assemblage dans l’entrepôt peut être gérée sur la page **Feuille mouvement** ou la page **Rangement interne entrepôt** , sans rapport avec l’ordre d’assemblage.  

> [!NOTE]  
>  Si les articles sont assemblés pour commande, l’expédition entrepôt de la commande vente liée déclenche un prélèvement entrepôt de tous les composants d’assemblage impliqués, et non seulement de l’article vendu, comme lors de l’expédition d’articles en stock.  

 Les champs **To-Assembly Bin Code** **From-Assembly Bin Code** de la fiche magasin définissent les flux par défaut depuis et vers les champs d’assemblage.  

### <a name="ad-hoc-movements"></a>Mouvements ad hoc  
 Dans l’entreposage avancé, un mouvement d’articles d’un emplacement à un autre sans relation avec les documents origine est géré sur la page **Feuille mouvement** et enregistré sur la page Mouvement entrepôt.  

## <a name="flushing-production-components-in-the-warehouse"></a>Consommation des composants de production dans l’entrepôt  
 Si cela est paramétré dans la fiche article, les composants prélevés avec des prélèvements entrepôt sont validés comme étant consommés par l’ordre de fabrication lorsque le prélèvement entrepôt est enregistré. En utilisant la méthode **Prélèvement + Aval** et la méthode de consommation **Prélèvement + Amont** , l’enregistrement de prélèvement déclenche la validation des consommations associées lorsque la première opération commence ou lorsque la dernière opération finit, respectivement.  

 Considérez le scénario suivant basé sur la base de données de démonstration [!INCLUDE[d365fin](includes/d365fin_md.md)], magasin BLANC.  

 Il existe un ordre de fabrication pour 15 pièces de l’article LS-100. Certains articles sur la liste des composants doivent être consommés manuellement dans une feuille consommation et d’autres articles de la liste peuvent être prélevés et consommés automatiquement à l’aide de la méthode de consommation **Prélèvement + Amont** .  

> [!NOTE]  
>  **Prélèvement + Aval** ne fonctionne que si la deuxième opération ligne gamme de production utilise le code lien gamme. Le lancement d’un ordre de fabrication planifié lance la consommation en aval des composants paramétrés sur **Prélèvement + Aval** . Toutefois, la consommation ne peut pas avoir lieu tant que le prélèvement des composants n’est pas enregistré, ce qui à nouveau ne peut avoir lieu que lorsque la commande est lancée.  

 Les étapes suivantes décrivent les actions impliquées par divers utilisateurs et la réponse associée :  

1.  Le chef atelier lance l’ordre de fabrication. Les articles utilisant la méthode de consommation **Aval** et aucun code lien gamme sont déduits de l’emplacement atelier ouvert.  
2.  Le chef atelier choisit le bouton **Créer prélèvement entrepôt** sur l’ordre de fabrication. Un document prélèvement entrepôt est créé pour les articles avec les méthodes de consommation **Manuelle** , **Prélèvement + Amont** et **Prélèvement + Aval** . Ces articles sont placés dans l’emplacement des consommations.  
3.  Le gestionnaire d’entrepôt affecte les prélèvements à un magasinier.  
4.  Le magasinier prélève les articles des emplacements appropriés et les place dans l’emplacement des consommations ou dans l’emplacement spécifié sur le prélèvement entrepôt, qui peut être un emplacement de centre de charge ou du poste de charge.  
5.  Le magasinier enregistre le prélèvement. La quantité est soustraite des emplacements prélèvement et ajoutée à l’emplacement de consommation. Le champ **Qté prélevée** sur la liste des composants de tous les articles prélevés est mis à jour.  

    > [!NOTE]  
    >  Seule la quantité qui est prélevée peut être consommée.  

6.  L’opérateur indique au gestionnaire de production que les articles finis sont terminés.  
7.  Le chef atelier utilise la feuille consommation ou la feuille production pour valider la consommation de composants qui utilisent la méthode de consommation **Manuel** ou les méthodes de consommation **Aval** ou **Prélèvement + Aval** avec des codes lien gamme.  
8.  Le gestionnaire de production valide la production de l’ordre de fabrication et modifie le statut en **Terminé** . La quantité de composants qui utilisent la méthode de consommation **En amont** est déduite de l’emplacement atelier ouvert, et la quantité de composants qui utilisent la méthode de consommation **Prélèvement + Amont** est déduite de l’emplacement des consommations.  

 La figure ci-après indique la date à laquelle le champ **Code emplacement** de la liste des composants est renseigné en fonction du paramétrage de votre magasin ou poste/centre de charge.  

 ![Aperçu de quand/comment le champ Code emplacement est renseigné](media/binflow.png "Aperçu de quand/comment le champ Code emplacement est renseigné")  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)
