---
title: "Comment prélever pour la fabrication dans les configurations de stockage de base | Microsoft Docs"
description: "Lorsque l'entrepôt appelle un traitement de prélèvement sans appeler de traitement d'expédition, vous pouvez utiliser la fenêtre **Prélèvement stock** pour organiser et enregistrer le prélèvement des composants."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 68702e384ea750535a8d7e5b83ee619856b6a34b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-production-or-assembly"></a>Prélever pour la fabrication et l'assemblage
Le mode de rangement de vos composants de prélèvement pour les ordres de fabrication ou d'assemblage dépend de la configuration du stockage en tant qu'emplacement. Pour plus d'informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans les configurations de stockage de base où l'emplacement requiert un traitement de prélèvement sans appeler de traitement d'expédition, vous pouvez utiliser la fenêtre **Prélèvement stock** pour organiser et enregistrer le prélèvement des composants.  

Dans les configurations de stockage de base, vous devez prélever les ordres d'assemblage à l'aide de la fenêtre **Mouvement de stock**. Pour plus d'informations, reportez-vous à la section « Traitement d'un article à assembler pour commande dans les prélèvements stock » dans [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).  

Dans les configurations d'entrepôt avancées où les magasins requièrent des prélèvements et des expéditions, vous utilisez la fenêtre **Prélèvement entrepôt** pour ajouter des composants aux ordres de fabrication.

> [!NOTE]  
>  Les différences importantes suivantes existent entre les prélèvements de stock et les mouvements de stock :  
>   
>  -   Lorsque vous enregistrez un prélèvement stock pour une opération interne, telles que la production, la consommation des composants sélectionnés est validée en même temps. Lorsque vous enregistrez un mouvement stock pour une opération interne, vous enregistrez seulement le mouvement physique des articles requis dans un emplacement de la zone Opérations sans valider la consommation.  
> -   Lorsque vous utilisez des prélèvements stock, le champ **Code emplacement** sur une ligne composant d'ordre de fabrication. définit l'emplacement de *prélèvement* où les composants sont déduits lors de la validation de la consommation. Lorsque vous utilisez des mouvements de stock, le **Code emplacement** sur des lignes composant d'ordre cde fabrication définit l'emplacement *placement* dans la zone Opérations où l'employé du magasin doit placer les composants.  

Si une condition préalable du système pour le prélèvement ou le déplacement de composants pour les documents d'origine est qu'une demande de désenlogement existe pour informer la zone d'entrepôt du besoin de composant. La demande désenlogement est créée lorsque le statut de l'ordre de fabrication devient Lancé ou lorsqu'un ordre de fabrication lancé est créé.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Pour prélever les composants pour les configurations de stockage de base
Dans les configurations de stockage de base, dans lesquelles le magasin est configuré pour utiliser uniquement le prélèvement ainsi que l'expédition, vous pouvez prélever des composants pour les activités de fabrication et d'assemblage à l'aide de la fenêtre **Prélèvement entrepôt**. Pour plus d'informations, voir [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Prélèvements stock**, puis sélectionnez le lien connexe.  
2.  Pour accéder aux composants de l'ordre de fabrication, choisissez l'action **Extraire documents origine**, puis sélectionnez l'ordre de fabrication lancé.  
3.  Procédez au prélèvement, puis enregistrez les informations sur le prélèvement réel dans le champ **Qté prélevée**.  
4.  Lorsque les lignes sont prêtes à être validées, choisissez l'action **Valider**. Les écritures entrepôt nécessaires sont alors créées et la consommation des articles est validée.  

Vous pouvez également créer un **Prélèvement de stock** directement à partir de la commande de fabrication lancée. Choisissez l'action **Créer prélèv./rangement stock**, cochez la case **Créer prélèvement stock**, puis choisissez le bouton **OK**.

Vous pouvez également utiliser la fenêtre **Mouvement de stock** pour déplacer des articles entre emplacements ad hoc, c'est-à-dire sans référence à un document origine.
Pour plus d'informations, voir [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Traitement des articles à assembler pour commande dans les prélèvements stock
La fenêtre **Prélvmt invent** est également utilisée pour prélever et livrer les ventes lorsque les articles doivent être assemblés avant de pouvoir être livrés. Pour plus d'informations, reportez-vous à [Vente d'articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).

Les articles à expédier ne sont pas physiquement présents dans un emplacement tant qu'ils ne sont pas assemblés et enregistrés comme production dans un emplacement de la zone d'assemblage. Cela signifie que le prélèvement des articles à assembler pour commande en vue de l'expédition est effectué suivant un flux spécial. Depuis un emplacement, les magasiniers extraient des éléments d'assemblage sur le poste d'accueil de livraison puis valident le prélèvement stock. Le prélèvement stock enregistré valide ensuite les résultats d'assemblage, la consommation de composants et l'expédition vente.

Vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour créer automatiquement un mouvement stock lors de la création du prélèvement stock pour l'élément d'assemblage. Pour cela, vous devez sélectionner le champ **Créer des mouvements automatiquement** dans la fenêtre **Paramètres d'assemblage**. Pour plus d'informations, voir [Déplacer les composants vers une zone opérations dans le stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Les lignes prélèvement stock pour les articles vente sont créées de différentes manières, selon qu'aucune, certaines ou toutes les quantités des lignes vente sont assemblées pour commande.

Dans les ventes courantes où vous utilisez des prélèvements stocks pour valider l'expédition des quantités en stock, une ligne prélèvement stock, ou plusieurs si l'article se trouve dans différents emplacements, sont créées pour chaque ligne commande vente. Cette ligne prélèvement est basée sur la quantité indiquée dans le champ **Qté à expédier**.

Dans les ventes assembler pour commande où la quantité totale de la ligne commande vente est assemblée pour commande, une ligne prélèvement stock est créée pour cette quantité. Cela signifie que la valeur du champ Quantité à assembler correspond à la valeur du champ **Qté à expédier**. Le champ **Assembler pour commande** est sélectionné sur la ligne.

Si un flux de résultats d'assemblage est paramétré pour le magasin, la valeur du champ **Code empl. exp. ass. pr comm.** ou la valeur du champ **Code empl. depuis assemblage**, de cette commande, est insérée dans le champ **Code emplacement** de la ligne prélèvement stock.

Si aucun code magasin n'est spécifié sur la ligne commande vente et qu'aucun flux résultats d'assemblage n'est paramétré pour le magasin, le champ **Code emplacement** de la ligne prélèvement stock est vide. Le magasinier doit ouvrir la fenêtre **Contenu emplacement** et sélectionner l'emplacement où les articles d'assemblage sont assemblés.

Dans les scénarios de combinaison, où une partie de la quantité doit d'abord être assemblée et l'autre doit être prélevée des stocks, un minimum de deux lignes prélèvement stock sont créées. Une ligne prélèvement est calculée pour la quantité à assembler pour commande. L'autre ligne prélèvement dépend des magasins dans lesquels les emplacements peuvent satisfaire la quantité restante du stock. Les codes emplacement sur les deux lignes sont renseignés de différentes manières comme indiqué pour les deux types vente différents respectivement. Pour plus d'informations, voir la section « Scénarios de combinaison » dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Pour prélever les composants pour les configurations de stockage avancées
Dans les configurations de stockage avancées, dans lequel le magasin est configuré pour utiliser le prélèvement ainsi que l'expédition, vous pouvez prélever des composants pour les activités de fabrication et d'assemblage à l'aide de la fenêtre **Prélèvement entrepôt**. Pour plus d'informations, voir [Prélever des articles avec les prélèvements entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Vous pouvez également utiliser la fenêtre **Feuille mouvement** pour déplacer des articles entre emplacements ad hoc, c'est-à-dire sans référence à un document origine. Pour plus d'informations, voir [Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Vous ne pouvez pas créer de toutes pièces un document prélèvement entrepôt car une activité de prélèvement fait toujours partie d'un flux de travail, soit dans un scénario d'extraction, soit dans un scénario de déplacement.  

Vous pouvez créer le document prélèvement entrepôt par déplacement en sélectionnant l'action **Créer prélèvement ent.** dans le document origine, par exemple, un ordre d'assemblage ou une expédition entrepôt lancé. Pour plus d'informations, voir [Prélever des articles avec les prélèvements entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Sinon, vous pouvez créer le document prélèvement entrepôt par extraction à l'aide de la fenêtre **Feuille prélèvement** pour détecter les demandes de prélèvement, à la fois pour l'expédition et les opérations internes, puis créer les documents prélèvement entrepôt requis.  

La procédure suivante explique un scénario d'extraction dans lequel vous prélevez des composants d'un ordre de fabrication lancé via la fenêtre **Feuille prélèvement**. Cette procédure s'applique également aux ordres d'assemblage.  

Pour créer des demandes de prélèvement dans le cadre de scénarios d'extraction et de déplacement, il faut que les documents origine en question soient lancés. Lancez les documents origine des opérations internes en procédant comme suit.  

 |Document origine|Méthode de lancement|  
 |---------------------|--------------------|  
 |Ordre de fabrication|Remplacez le type commande par un ordre de fabrication lancé.|  
 |Ordre d'assemblage|Remplacez le statut actuel par le statut Lancé.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Pour prélever des composants à partir des feuilles prélèvement  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille prélèvement**, puis sélectionnez le lien connexe.  
2.  Choisissez l'action **Extraire documents entrepôt**, puis sélectionnez les lignes composant de l'ordre de fabrication lancé.  
3.  Vérifiez les lignes, triez-les pour assurer un prélèvement optimisé et, si nécessaire, combinez les avec d'autres lignes de la feuille pour utiliser au mieux la disponibilité de l'employé.  
4.  Choisissez l'action **Créer prélèvement**.  
5.  Définissez le mode de création des documents prélèvement entrepôt et la manière de trier les lignes prélèvement en renseignant les champs de la fenêtre **Créer prélèvement** .  
6.  Cliquez sur le bouton **OK**.

Les documents prélèvement entrepôt sont maintenant créés avec des lignes prélèvement pour chaque composant requis dans l'opération interne.

Si la zone Opérations internes (par exemple, un atelier de production) est configurée avec un emplacement par défaut pour les composants à utiliser dans l'opération, ce code emplacement est inséré dans les lignes Emplacement qui figurent sur le document prélèvement entrepôt pour indiquer aux magasiniers où placer les articles. Pour plus d'informations, voir [Configurer des entrepôts de base avec les zones d'opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

## <a name="filling-the-consumption-bin"></a>Renseigner l'emplacement consommation
Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d'emplacement](media/binflow.png "BinFlow")

## <a name="see-also"></a>Voir aussi
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

