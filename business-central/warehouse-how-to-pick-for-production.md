---
title: Comment prélever pour la fabrication dans les configurations de stockage de base | Microsoft Docs
description: Lorsque l'entrepôt appelle un traitement de prélèvement sans appeler de traitement d'expédition, vous pouvez utiliser la page **Prélèvement stock** pour organiser et enregistrer le prélèvement des composants.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2c9d19d8406fe49df7449a9b5ecfe231cc3024c9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779551"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Prélever pour la fabrication ou l'assemblage dans les configurations de stockage de base.
Le mode de rangement de vos composants de prélèvement pour les ordres de fabrication ou d'assemblage dépend de la configuration du stockage en tant qu'emplacement. Pour plus d'informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans les configurations de stockage de base où l'emplacement requiert un traitement de prélèvement sans appeler de traitement d'expédition, vous pouvez utiliser la page **Prélèvement stock** pour organiser et enregistrer le prélèvement des composants.  

Dans les configurations de stockage de base, vous devez prélever les ordres d'assemblage à l'aide de la page **Mouvement de stock**. Pour plus d’informations, voir [Traitement des articles à assembler pour commande dans les prélèvements stock](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Dans les configurations d'entrepôt avancées où les magasins requièrent des prélèvements et des expéditions, vous utilisez la page **Prélèvement entrepôt** pour ajouter des composants aux ordres de fabrication. Pour plus d'informations, consultez [Prélever pour la fabrication ou l'assemblage dans les configurations de stockage avancées](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

> [!NOTE]  
>  Les différences importantes suivantes existent entre les prélèvements de stock et les mouvements de stock :  
>   
>  -   Lorsque vous enregistrez un prélèvement stock pour une opération interne, telles que la production, la consommation des composants sélectionnés est validée en même temps. Lorsque vous enregistrez un mouvement stock pour une opération interne, vous enregistrez seulement le mouvement physique des articles requis dans un emplacement de la zone Opérations sans valider la consommation.  
> -   Lorsque vous utilisez des prélèvements stock, le champ **Code emplacement** sur une ligne composant d'ordre de fabrication. définit l'emplacement de *prélèvement* où les composants sont déduits lors de la validation de la consommation. Lorsque vous utilisez des mouvements de stock, le **Code emplacement** sur des lignes composant d'ordre cde fabrication définit l'emplacement *placement* dans la zone Opérations où l'employé du magasin doit placer les composants.  

Si une condition préalable du système pour le prélèvement ou le déplacement de composants pour les documents d'origine est qu'une demande de désenlogement existe pour informer la zone d'entrepôt du besoin de composant. La demande désenlogement est créée lorsque le statut de l'ordre de fabrication devient Lancé ou lorsqu'un ordre de fabrication lancé est créé.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Pour prélever les composants pour les configurations de stockage de base
Dans les configurations de stockage de base, dans lesquelles le magasin est configuré pour utiliser uniquement le prélèvement ainsi que l'expédition, vous pouvez prélever des composants pour les activités de fabrication et d'assemblage à l'aide de la page **Prélèvement entrepôt**. Pour plus d'informations, voir [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements stock**, puis sélectionnez le lien associé.  
2.  Pour accéder aux composants de l'ordre de fabrication, choisissez l'action **Extraire documents origine**, puis sélectionnez l'ordre de fabrication lancé.  
3.  Procédez au prélèvement, puis enregistrez les informations sur le prélèvement réel dans le champ **Qté prélevée**.  
4.  Lorsque les lignes sont prêtes à être validées, choisissez l'action **Valider**. Les écritures entrepôt nécessaires sont alors créées et la consommation des articles est validée.  

Vous pouvez également créer un **Prélèvement de stock** directement à partir de la commande de fabrication lancée. Choisissez l'action **Créer prélèv./rangement stock**, cochez la case **Créer prélèvement stock**, puis choisissez le bouton **OK**.

Vous pouvez également utiliser la page **Mouvement de stock** pour déplacer des articles entre emplacements ad hoc, c'est-à-dire sans référence à un document origine.
Pour plus d'informations, voir [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Traitement des articles à assembler pour commande dans les prélèvements stock
La page **Prélvmt invent** est également utilisée pour prélever et livrer les ventes lorsque les articles doivent être assemblés avant de pouvoir être livrés. Pour plus d'informations, reportez-vous à [Vente d'articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).

Les articles à expédier ne sont pas physiquement présents dans un emplacement tant qu'ils ne sont pas assemblés et enregistrés comme production dans un emplacement de la zone d'assemblage. Cela signifie que le prélèvement des articles à assembler pour commande en vue de l'expédition est effectué suivant un flux spécial. Depuis un emplacement, les magasiniers extraient des éléments d'assemblage sur le poste d'accueil de livraison puis valident le prélèvement stock. Le prélèvement stock enregistré valide ensuite les résultats d'assemblage, la consommation de composants et l'expédition vente.

Vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour créer automatiquement un mouvement stock lors de la création du prélèvement stock pour l'élément d'assemblage. Pour cela, vous devez sélectionner le champ **Créer des mouvements automatiquement** sur la page **Paramètres d'assemblage**. Pour plus d'informations, voir [Déplacer les composants vers une zone opérations dans le stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Les lignes prélèvement stock pour les articles vente sont créées de différentes manières, selon qu'aucune, certaines ou toutes les quantités des lignes vente sont assemblées pour commande.

Dans les ventes courantes où vous utilisez des prélèvements stocks pour valider l'expédition des quantités en stock, une ligne prélèvement stock, ou plusieurs si l'article se trouve dans différents emplacements, sont créées pour chaque ligne commande vente. Cette ligne prélèvement est basée sur la quantité indiquée dans le champ **Qté à expédier**.

Dans les ventes assembler pour commande où la quantité totale de la ligne commande vente est assemblée pour commande, une ligne prélèvement stock est créée pour cette quantité. Cela signifie que la valeur du champ Quantité à assembler correspond à la valeur du champ **Qté à expédier**. Le champ **Assembler pour commande** est sélectionné sur la ligne.

Si un flux de résultats d'assemblage est paramétré pour le magasin, la valeur du champ **Code empl. exp. ass. pr comm.** ou la valeur du champ **Code empl. depuis assemblage**, de cette commande, est insérée dans le champ **Code emplacement** de la ligne prélèvement stock.

Si aucun code magasin n'est spécifié sur la ligne commande vente et qu'aucun flux résultats d'assemblage n'est paramétré pour le magasin, le champ **Code emplacement** de la ligne prélèvement stock est vide. Le magasinier doit ouvrir la page **Contenu emplacement** et sélectionner l'emplacement où les articles d'assemblage sont assemblés.

Dans les scénarios de combinaison, où une partie de la quantité doit d'abord être assemblée et l'autre doit être prélevée des stocks, un minimum de deux lignes prélèvement stock sont créées. Une ligne prélèvement est calculée pour la quantité à assembler pour commande. L'autre ligne prélèvement dépend des magasins dans lesquels les emplacements peuvent satisfaire la quantité restante du stock. Les codes emplacement sur les deux lignes sont renseignés de différentes manières comme indiqué pour les deux types vente différents respectivement. Pour plus d'informations, voir la section « Scénarios de combinaison » dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Renseigner l'emplacement consommation
Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d'emplacement](media/binflow.png "BinFlow")

## <a name="see-also"></a>Voir aussi
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
