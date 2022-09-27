---
title: 'Procédure : planifier des prélèvements dans la feuille'
description: Découvrez comment les lignes des documents expédition peuvent être mises à disposition sur les feuilles de travail de prélèvement pour les magasiniers.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 667aa2702d064e44b9b52dc167e2372f98d7944f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530422"
---
# <a name="plan-picks-in-worksheets"></a>Planifier des prélèvements dans la feuille

Si votre entrepôt est configuré pour exiger à la fois le traitement des prélèvements et des expéditions, vous pouvez choisir de rendre les lignes des documents d’expédition disponibles sur les feuilles de travail de prélèvement au lieu des instructions de prélèvement.  

> [!NOTE]  
> Si des instructions de prélèvement entrepôt ont déjà été créées et que vous souhaitez les combiner pour former une instruction de prélèvement, supprimez les prélèvements entrepôt individuels. Les lignes à prélever sont alors listées dans une feuille de travail de prélèvement.  

Sur la page **Feuilles de travail de prélèvement**, vous pouvez configurer des listes de sélection qui aident les employés à rassembler des articles dans l’entrepôt. La page affiche les quantités disponibles dans les bacs de transbordement, ce qui est utile pour planifier les affectations de travail dans les situations de transbordement. [!INCLUDE[prod_short](includes/prod_short.md)] proposera toujours en premier un prélèvement dans un bac de transbordement. Les lignes de la feuille de calcul peuvent provenir de plusieurs documents sources. Par exemple, ils peuvent provenir de plusieurs commandes vente. 

> [!NOTE]  
> Le prélèvement d’articles assemblés pour une commande vente en cours d’expédition suit les mêmes étapes que les prélèvements entrepôt ordinaires pour l’expédition. Cependant, le nombre de lignes prélèvement par quantité à livrer peut grandement varier, car le prélèvement entrepôt concerne les composants et non l’élément d’assemblage.  
>
> Les lignes prélèvement entrepôt sont créées suivant la valeur du champ **Quantité restante** sur les lignes de l’ordre d’assemblage associé à la ligne commande vente en cours d’expédition. Ceci garantit le prélèvement de tous les composants en une seule action. Pour plus d’informations, voir [Vente d’articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Pour plus d’informations sur le prélèvement de composants pour les ordres d’assemblage en général, notamment les situations où l’élément d’assemblage n’est pas dû dans une expédition vente, voir [Prélever pour l’assemblage ou la production dans les configurations de stockage avancées.](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Tri des lignes sur une feuille de travail de prélèvement

Vous pouvez trier les lignes par article, numéro de rayon, document source, date d’échéance ou destination. Voici quelques exemples de tri :

* Si vous triez par date d’échéance, vous pouvez choisir d’effacer toutes les lignes à l’exception de celles nécessitant un traitement immédiat. Les lignes moins urgentes ne sont pas effacées mais renvoyées à la feuille **sélection prélèvement**. Lorsque vous créez le prélèvement, les lignes sont déjà triées par date d’échéance et vous pouvez choisir d’affecter le prélèvement à un employé.
* Si vos bacs sont numérotés pour correspondre à la disposition physique de votre entrepôt, le tri des lignes par numéro de bac peut faciliter le prélèvement pour plusieurs expéditions en même temps. 
* Si vous utilisez le classement par catégorie, le tri par classement peut vous faire gagner du temps. 
* Vous pouvez trier par destination, ce qui vous permet d’assembler et d’expédier les commandes par client.

## <a name="to-plan-picks-in-the-worksheet"></a>Pour planifier des prélèvements dans la feuille

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille prélèvement**, puis choisissez le lien associé.  
2. Choisissez l’action **Extraire documents entrepôt**.  
3. Sélectionnez les expéditions pour lesquelles vous souhaitez préparer un prélèvement. Vous pouvez trier les lignes, mais le tri ne sera pas appliqué à l’instruction de sélection. Vous pouvez aussi supprimer certaines lignes pour rendre le prélèvement plus efficace. Par exemple, si plusieurs lignes comportent des articles situés dans des bacs de transbordement, vous pouvez créer un prélèvement pour toutes les lignes. Les articles transbordés seront expédiés, avec les autres articles des expéditions, et les emplacements de transbordement pourront à nouveau recevoir d’autres articles entrants.  
4. Choisissez l’action **Créer prélèvement**, puis remplissez la page **Créer prélèvement**. Le tri que vous demandez ici organisera les lignes prélèvement que vous créez. Par exemple, vous pouvez créer un prélèvement pour chaque zone et trier les lignes selon l’ordre des emplacements au sein de chaque prélèvement.  
5. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements entrepôt**, puis choisissez le lien associé. La page **Prélèvements entrepôt** s’ouvre.  
6. Vous pouvez à présent trouver le prélèvement affecté en sélectionnant le prélèvement doté du numéro le plus élevé.  
7. Si nécessaire, vous pouvez affecter un autre utilisateur ou trier les lignes différemment.  
8. Choisissez l’action **Imprimer** pour imprimer les instructions relatives au prélèvement.  
9. Une fois le prélèvement terminé, choisissez l’action **Enregistrer**.  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/pick-ship-items-warehouse/) associée

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
