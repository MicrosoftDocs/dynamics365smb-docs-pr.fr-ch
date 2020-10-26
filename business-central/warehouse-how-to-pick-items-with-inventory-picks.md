---
title: Comment prélever des articles avec les prélèvements stock | Microsoft Docs
description: Si un magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, vous utilisez les documents prélèvement stock pour enregistrer et valider les informations de prélèvement et d’expédition pour vos documents origine.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7f9887c398833fcf817a6c8707b18b0b77da1ff2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918328"
---
# <a name="pick-items-with-inventory-picks"></a>Prélever des articles avec les prélèvements stock

Lorsque votre magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, vous utilisez la page **Prélèvement stock** pour enregistrer et valider les informations de prélèvement et d’expédition pour vos documents origine. Le document origine sortant peut être une commande vente, un retour achat, un désenlogement transfert ou un ordre de fabrication dont les composants sont prêts à être prélevés.

> [!NOTE]  
> Les composants pour les commandes d’assemblage ne peuvent pas être prélevés ni validés avec des prélèvements stock. À la place, utilisez la page **Mouvement de stock** . Pour plus d’informations, voir [Déplacer les composants vers une zone opérations dans le stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).
>
> En cas de prélèvement et d’expédition de quantités de lignes vente assemblées pour commande, vous devez suivre certaines règles en créant les lignes prélèvement stock. Pour plus d’informations, voir la section [Traitement des articles à assembler pour commande dans les prélèvements stock](#handling-assemble-to-order-items-with-inventory-picks).  

Vous pouvez créer un prélèvement stock de trois manières :  

- Créez le prélèvement en deux étapes en demandant d’abord un prélèvement stock en lançant le document d’origine. Cela permet de signaler à l’entrepôt que le document d’origine est prêt pour le prélèvement. Le prélèvement stock peut ensuite être créé sur la page **Prélèvement stock** sur la base du document origine.  
- Créez le prélèvement stock directement à partir du document origine proprement dit.  
- Vous pouvez créer des prélèvements stock pour plusieurs documents simultanément en utilisant le traitement par lots.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Pour demander un prélèvement stock en lançant le document origine

Pour les commandes vente, de retours achat et de désenlogements transfert, vous créez la demande entrepôt en lançant l’ordre. Ce qui suit décrit comment faire cela pour une commande vente.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente** , puis sélectionnez le lien associé.
2. Sélectionnez la commande vente que vous voulez lancer, puis sélectionnez l’action **Lancer** .

Pour les ordres de fabrication, vous créez automatiquement la demande entrepôt pour le prélèvement de composants, appelé *consommation* lorsque le statut de l’ordre de fabrication passe à **Lancé** ou lorsque l’ordre de fabrication lancé est créé. Pour plus d’informations, voir [Prélever pour la fabrication ou l’assemblage](warehouse-how-to-pick-for-production.md).

Une fois la demande entrepôt créée, le magasinier affecté aux prélèvements des articles peut voir que le document origine est prêt à être prélevé et peut créer un nouveau document prélèvement sur la base de la demande entrepôt.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Pour créer un prélèvement stock en fonction du document origine

Maintenant que la demande est créée, le magasinier peut créer un nouveau prélèvement stock sur la base du document origine lancé.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements stock** , puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau** .  
    Assurez-vous que le champ **N°** du raccourci **Général** est rempli.
3. Dans le champ **Document origine** , sélectionnez le type de document origine relatif au prélèvement.  
4. Dans le champ **N° origine** , sélectionnez le document origine.  
5. Sinon, choisissez l’action **Extraire document origine** pour sélectionner le document à partir de la liste des documents origine sortants prêts pour le prélèvement dans le magasin.  
6. Cliquez sur le bouton **OK** pour renseigner les lignes prélèvement en fonction du document origine sélectionné.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Pour créer un prélèvement stock à partir du document origine

1. Dans le document origine, qui peut être une commande vente, un retour achat, un désenlogement transfert ou un ordre de fabrication, choisissez l’action **Créer prélèv./rangement stock** .
2. Activez la case à cocher **Créer prélèvement stock** .  
3. Cliquez sur le bouton **OK** . Un nouveau prélèvement stock sera créé.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Pour créer plusieurs prélèvements stock avec un traitement par lots

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Créer prélèv./rangement stock** , puis sélectionnez le lien associé.  
2. Sur le raccourci **Demande entrepôt** , utilisez les champs **Document origine** et **N° origine** pour opérer un filtrage sur certains types de documents ou des plages de numéros de document. Par exemple, vous pouvez créer des prélèvements uniquement pour des commandes vente.  
3. Dans le raccourci **Options** , cochez la case **Créer rangement stock. prélèvement** .
4. Cliquez sur le bouton **OK** . Les prélèvements stock spécifiés sont créés.

> [!NOTE]  
> En cas de prélèvement et d’expédition de quantités de lignes vente assemblées pour commande, vous devez suivre certaines règles en créant les lignes prélèvement stock. Pour plus d’informations, voir la section [Traitement des articles à assembler pour commande dans les prélèvements stock](#handling-assemble-to-order-items-with-inventory-picks).  
>
> Dans les configurations de stockage de base, les articles qui sont assemblés aux commandes vente sont prélevés de la commande vente associée, comme expliqué dans cette rubrique. Pour plus d’informations, voir la section [Traitement des articles à assembler pour commande dans les prélèvements stock](#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="to-record-the-inventory-picks"></a>Pour enregistrer les prélèvements stock

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvement stock** , puis sélectionnez le lien associé.  
2. Dans le champ **Code emplacement** sur les lignes prélèvement, l’emplacement à partir duquel les articles doivent être prélevés est proposé sur la base d’un emplacement par défaut de l’article. Vous pouvez modifier l’emplacement sur la page, si nécessaire.  
3. Exécutez le prélèvement et saisissez les informations pour la quantité effectivement rangée dans le champ **Quantité à traiter** .

    S’il s’avère nécessaire de prendre les articles d’une ligne dans plusieurs emplacements, notamment parce qu’ils ne sont pas disponibles dans l’emplacement indiqué, alors utilisez la fonction **Eclater ligne** sur le raccourci **Lignes** . Pour plus d’informations sur l’éclatement des lignes, voir [Répartir des lignes activité entrepôt](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Une fois le prélèvement exécuté, choisissez l’action **Valider** .  

Le processus de validation valide l’expédition des lignes du document origine qui ont été prélevées, ou la consommation dans le cas d’ordres de fabrication. Si le magasin utilise des emplacements, la validation crée également des écritures entrepôt pour valider les modifications apportées aux quantités emplacement.  

## <a name="to-delete-inventory-pick-lines"></a>Pour supprimer des lignes prélèvement stock

Si les articles du prélèvement stock ne sont pas disponibles, vous pouvez supprimer ces lignes prélèvement stock après validation puis supprimer le document prélèvement stock. Le document d’origine, par exemple une commande vente ou un ordre de fabrication, aura d’autres articles à prélever qui peuvent être obtenus via un nouveau prélèvement stock ultérieurement lorsque les articles sont disponibles.  

> [!WARNING]  
> Ce traitement n’est pas possible si des numéros de série/lot sont spécifiés dans le document origine. Par exemple, si une ligne commande vente contient un numéro de série/lot, cette spécification traçabilité sera supprimée si une ligne prélèvement stock du numéro de série/lot est supprimée.  
>
> Si des numéros de série/lot de lignes prélèvement stock ne sont pas disponibles, vous ne devez pas supprimer les lignes concernées. Au lieu de cela, vous devez remettre le champ **Qté à gérer** à zéro, valider les prélèvements réels, puis supprimer le document prélèvement stock. De cette manière, vous pourrez recréer les lignes prélèvement stock de ces numéros de série/lot de la commande vente ultérieurement.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Traitement des articles à assembler pour commande dans les prélèvements stock

La page **Prélvmt invent** est également utilisée pour prélever et livrer les ventes lorsque les articles doivent être assemblés avant de pouvoir être livrés. Pour plus d’informations, reportez-vous à [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).

Les articles à expédier ne sont pas physiquement présents dans un emplacement tant qu’ils ne sont pas assemblés et enregistrés comme production dans un emplacement de la zone d’assemblage. Cela signifie que le prélèvement des articles à assembler pour commande en vue de l’expédition est effectué suivant un flux spécial. Depuis un emplacement, les magasiniers extraient des éléments d’assemblage sur le poste d’accueil de livraison puis valident le prélèvement stock. Le prélèvement stock enregistré valide ensuite les résultats d’assemblage, la consommation de composants et l’expédition vente.

Vous pouvez configurer [!INCLUDE[d365fin](includes/d365fin_md.md)] pour créer automatiquement un mouvement stock lors de la création du prélèvement stock pour l’élément d’assemblage. Pour cela, vous devez sélectionner le champ **Créer des mouvements automatiquement** sur la page **Paramètres d’assemblage** . Pour plus d’informations, voir [Déplacer les composants vers une zone opérations dans le stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Les lignes prélèvement stock pour les articles vente sont créées de différentes manières, selon qu’aucune, certaines ou toutes les quantités des lignes vente sont assemblées pour commande.

Dans les ventes courantes où vous utilisez des prélèvements stocks pour valider l’expédition des quantités en stock, une ligne prélèvement stock, ou plusieurs si l’article se trouve dans différents emplacements, sont créées pour chaque ligne commande vente. Cette ligne prélèvement est basée sur la quantité indiquée dans le champ **Qté à expédier** .

Dans les ventes assembler pour commande où la quantité totale de la ligne commande vente est assemblée pour commande, une ligne prélèvement stock est créée pour cette quantité. Cela signifie que la valeur du champ Quantité à assembler correspond à la valeur du champ **Qté à expédier** . Le champ **Assembler pour commande** est sélectionné sur la ligne.

Si un flux de résultats d’assemblage est paramétré pour le magasin, la valeur du champ **Code empl. exp. ass. pr comm.** ou la valeur du champ **Code empl. depuis assemblage** , de cette commande, est insérée dans le champ **Code emplacement** de la ligne prélèvement stock.

Si aucun code magasin n’est spécifié sur la ligne commande vente et qu’aucun flux résultats d’assemblage n’est paramétré pour le magasin, le champ **Code emplacement** de la ligne prélèvement stock est vide. Le magasinier doit ouvrir la page **Contenu emplacement** et sélectionner l’emplacement où les articles d’assemblage sont assemblés.

Dans les scénarios de combinaison, où une partie de la quantité doit d’abord être assemblée et l’autre doit être prélevée des stocks, un minimum de deux lignes prélèvement stock sont créées. Une ligne prélèvement est calculée pour la quantité à assembler pour commande. L’autre ligne prélèvement dépend des magasins dans lesquels les emplacements peuvent satisfaire la quantité restante du stock. Les codes emplacement sur les deux lignes sont renseignés de différentes manières comme indiqué pour les deux types vente différents respectivement. Pour plus d’informations, voir la section « Scénarios de combinaison » dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Procédure pas à pas : Prélèvement et expédition dans les configurations de stockage de base](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
