---
title: Comment prélever des articles pour l’expédition entrepôt | Microsoft Docs
description: Lorsque le magasin est configuré pour appeler un traitement de prélèvement entrepôt et un traitement d’expédition entrepôt, vous pouvez utiliser les documents prélèvement entrepôt pour créer et traiter les informations préalables à la validation de l’expédition entrepôt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dedd89dfceeb17994ccc18b359d2b02eb086cc60
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756203"
---
# <a name="pick-items-for-warehouse-shipment"></a>Prélever des articles pour l’expédition entrepôt
Lorsque le magasin est configuré pour appeler un traitement de prélèvement entrepôt et un traitement d’expédition entrepôt, vous pouvez utiliser les documents prélèvement entrepôt pour créer et traiter les informations préalables à la validation de l’expédition entrepôt.  

Vous ne pouvez pas créer de toutes pièces un document prélèvement entrepôt car une activité de prélèvement fait toujours partie d’un flux de travail, soit dans un scénario d’extraction, soit dans un scénario de déplacement.  

Vous pouvez créer des documents prélèvement entrepôt en mode extraction en ouvrant un document expédition entrepôt vide, détecter les documents origine qui sont lancés à l’expédition, puis créer des lignes prélèvement entrepôt pour ces expéditions. Vous pouvez utiliser les fonctions **Obtenir documents origine** ou **Utiliser filtre pour obtenir documents origine** pour détecter les documents origine qui sont prêts à l’expédition.

Sinon, vous pouvez utiliser la page **Feuille prélèvement** pour extraire et créer les lignes prélèvement en mode lots. Pour plus d’informations, voir [Planifier des prélèvements dans des feuilles](warehouse-how-to-plan-picks-in-worksheets.md).  

Vous pouvez également créer des documents prélèvement entrepôt en mode pousser à partir de la page **Expédition entrepôt** en sélectionnant **Créer prélèvement**.  

> [!NOTE]  
>  Le prélèvement pour l’expédition entrepôt des articles assemblés à la commande vente en cours d’expédition suit les mêmes étapes que les prélèvements entrepôt ordinaires pour l’expédition, comme décrit dans cette rubrique. Cependant, le nombre de lignes prélèvement par quantité à livrer peut grandement varier car le prélèvement entrepôt concerne les composants et non l’élément d’assemblage.  
>   
>  Les lignes prélèvement entrepôt sont créées suivant la valeur du champ **Quantité restante** sur les lignes de l’ordre d’assemblage associé à la ligne commande vente en cours d’expédition. Ceci garantit le prélèvement de tous les composants en une seule action.  
>   
>  Pour plus d’informations, reportez-vous à la section « Traitement des articles à assembler pour commande dans les expéditions entrepôt ».  
>   
>  Pour plus d’informations sur le prélèvement de composants pour les ordres d’assemblage en général, notamment les situations où l’élément d’assemblage n’est pas dû dans une expédition vente, voir [Prélever pour la fabrication ou l’assemblage](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Pour prélever des articles pour l’expédition entrepôt  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements**, puis sélectionnez le lien associé.  

    Si vous souhaitez travailler à un prélèvement particulier, sélectionnez-le dans la liste ou filtrez cette dernière afin de trouver les prélèvements qui vous ont été spécifiquement affectés. Ouvrez la fiche prélèvement.  
2.  Si le champ **ID utilisateur affecté** est vide, entrez votre ID pour vous identifier si nécessaire.  
3.  Exécutez le prélèvement réel des articles.  

    Si le magasin est configuré pour utiliser des emplacements, les emplacements par défaut des articles sont utilisés pour suggérer où prendre les articles. Les instructions apparaissent sur deux lignes distinctes, une ligne au moins pour chaque type d’action, prélèvement et placement.  

    Si l’entrepôt est configuré pour utiliser un prélèvement et rangement dirigé, le classement d’emplacement est utilisé pour calculer les meilleurs emplacements d’où prélever, et ces emplacements sont ensuite suggérés sur les lignes prélèvement. Les instructions apparaissent sur deux lignes distinctes, une ligne au moins pour chaque type d’action, prélèvement et placement.  

4.  Lorsque vous avez effectué le prélèvement et placé les articles dans la zone ou l’emplacement d’expédition, choisissez l’action **Enregistrer prélèvement**.  

La personne responsable de l’expédition peut alors apporter les articles au quai de chargement et valider l’expédition, dont le document origine lié, sur la page **Expédition entrepôt** . Pour plus d’informations, voir [Expédier des articles](warehouse-how-ship-items.md).   

En plus de prélever les documents origine, comme indiqué dans cette rubrique, vous pouvez prendre et placer les articles entre les emplacements sans faire référence aux documents origine. Pour plus d’informations, voir [Prélever et ranger sans document origine](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Traitement des articles à assembler pour commande dans les expéditions entrepôt
Dans des scénarios d’assemblage pour commande, le champ **Qté à expédier** sur les lignes expédition entrepôt est utilisé pour enregistrer le nombre d’unités assemblées. La quantité spécifiée est ensuite validée comme résultats d’assemblage lorsque l’expédition entrepôt est validée.

Pour d’autres lignes expédition entrepôt, la valeur du champ **Qté à expédier** est zéro dès le début.

Lorsque les travailleurs chargés de l’assemblage finissent d’assembler les pièces ou l’ensemble de la quantité à assembler pour commande, ils l’enregistrent dans le champ **Qté à expédier** de la ligne expédition entrepôt dans les configurations avancées et sélectionnent ensuite l’action **Valider expédition**. Le résultat est que les résultats d’assemblage correspondants sont validés, y compris la consommation de composants. Une expédition vente pour la quantité est validée pour la commande vente.

À partir de l’ordre d’assemblage, vous pouvez choisir **Ligne expédition entrepôt Assembler pour commande** pour accéder à la ligne expédition entrepôt. Ceci peut être utile pour les travailleurs qui n’utilisent pas généralement la page **Expédition entrepôt**.

Une fois l’expédition entrepôt validée, divers champs de la ligne commande vente sont mis à jour pour afficher la progression dans l’entrepôt. Les champs suivants sont également mis à jour pour afficher le nombre de quantités à assembler pour commande qui restent à être assemblées et expédiées :

- **Qté restante entrepôt ATO**
- **Qté restante entrepôt ATO (base)**

> [!NOTE]
> Dans les scénarios de combinaison, où une partie de la quantité doit d’abord être assemblée et l’autre doit être expédiée à partir des stocks, deux lignes expédition entrepôt sont créées. L’une est pour la quantité à assembler pour commande et l’autre est destinée à la quantité en stock.

> Dans ce cas, la quantité à assembler pour commande est traitée comme décrite dans cette rubrique, et la quantité en stock est traitée comme toute autre ligne expédition entrepôt normale. Pour plus d’informations sur les scénarios de combinaison, consultez [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]