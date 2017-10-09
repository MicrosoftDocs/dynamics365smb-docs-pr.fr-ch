---
title: "Paramétrer l'amortissement| Microsoft Docs"
description: "Vous spécifiez dans une loi d'amortissement comment vous souhaitez amortir ou déprécier les immobilisations."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fbdfc4431056c4851208aa063daf8761b4e70bf1
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-depreciation"></a>Procédure : configurer un amortissement immobilisation
 Vous pouvez utiliser plusieurs méthodes d'amortissement pour préparer les états financiers et les déclarations de revenus. De nombreuses sociétés de grande taille utilisent la méthode de l'amortissement linéaire dans leurs états financiers car elle permet généralement la déclaration des bénéfices supérieurs. Toutefois, dans le cadre de l'impôt sur le revenu, la plupart des entreprises utilise une méthode d'amortissement accélérée. Pour en savoir plus, voir [Méthodes d'amortissement](fa-depreciation-methods.md).

 Lorsque vous avez créé les lois d'amortissement nécessaires, vous devez en attribuer au moins une à chaque immobilisation. La loi d'amortissement attribuée à une immobilisation est désignée comme loi d'amortissement immobilisation. Par conséquent, la fenêtre pour les lois d'amortissement attribuées est intitulée **Lois d'amortissement immo.**.

## <a name="to-create-a-depreciation-book"></a>Pour créer une loi d'amortissement
Dans une loi d'amortissement immobilisation, vous spécifiez comment les immobilisations sont amorties. Pour prendre en charge plusieurs méthodes d'amortissement, vous pouvez paramétrer plusieurs lois d'amortissement.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Lois d'amortissement**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Liste des lois d'amortissement**, sélectionnez l'action **Nouveau**.
3. Dans la fenêtre **Fiche loi d'amortissement**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Vous pouvez enregistrer les transactions immobilisation dans la fenêtre **Feuille compta. immo.** ou dans la fenêtre **Feuille immo.**, selon que les transactions sont destinées pour des rapports financiers ou pour la gestion interne. Procédez comme suit pour définir quel type de feuille est utilisé pour les différentes activités immobilisation par défaut.
4. Sur le raccourci **Intégration**, cochez la case pour chaque activité immobilisation dont vous souhaitez valider les transactions via la fenêtre **Feuille compta. immo.**.
5. Répétez les étapes 2 à 4 pour chaque méthode d'amortissement ou méthode de validation que vous souhaitez attribuer à des immobilisations en tant que loi d'amortissement.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Pour attribuer une loi d'amortissement à une immobilisation
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Immobilisations**, puis sélectionnez le lien connexe.
2. Sélectionnez l'immobilisation pour laquelle vous souhaitez configurer une loi d'amortissement.
3. Sur le raccourci **Loi d'amortissement**, renseignez les champs, le cas échéant.
4. Si vous devez assigner plus d'une loi d'amortissement à l'immobilisation, sélectionnez l'action **Ajouter davantage de lois d'amortissement**.
5. Sinon, sélectionnez l'action **Lois d'amortissement** pour spécifier une, voire plusieurs lois d'amortissement immobilisation.

    > [!NOTE]  
>   Lorsque vous utilisez la méthode manuelle d'amortissement, vous devez saisir l'amortissement manuellement dans la feuille comptabilisation immobilisation. La fonction **Calculer amortissement** ignore les immobilisations qui utilisent la méthode d'amortissement manuelle. Vous pouvez recourir à cette méthode pour les immobilisations qui ne font pas l'objet d'un amortissement, par exemple les terrains.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Pour attribuer une loi d'amortissement à plusieurs immobilisations avec un traitement par lots
Si vous voulez associer une loi d'amortissement à plusieurs immobilisations, vous pouvez utiliser le traitement par lots **Créer plans amortissement** pour créer des lois d'amortissement d'immobilisation.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Immobilisations**, puis sélectionnez le lien connexe.
2. Sélectionnez l'immobilisation à laquelle vous souhaitez attribuer une loi d'amortissement, puis sélectionnez l'action **Modifier**.
3. Dans la fenêtre **Fiche livre d'amortissement**, sélectionnez l'action **Créer plans amortissement**.
4. Dans la fenêtre **Créer plans amortissement immo.**, renseignez le champ **Loi d'amortissement**.
5. Choisissez le champ **Copier immo. n°**, puis sélectionnez le numéro de l'immobilisation à utiliser comme base pour créer de nouvelles lois d'amortissement d'immobilisation.

    Si vous renseignez ce champ, les champs d'amortissement des nouvelles lois d'amortissement d'immobilisation contiennent les mêmes informations que ceux de la loi d'amortissement d'immobilisation que vous copiez. N'entrez rien dans ce champ si vous souhaitez créer de nouvelles lois d'amortissement d'immobilisation avec des champs d'amortissement vides.  
6. Sur le raccourci **Immo.**, vous pouvez positionner un filtre afin de sélectionner les immobilisations pour lesquelles vous souhaitez créer des lois d'amortissement immobilisation.
7. Cliquez sur le bouton **OK**.

## <a name="to-set-up-depreciation-posting-types"></a>Pour configurer les types de validation amortissement
Pour chaque loi d'amortissement, vous devez définir la manière dont vous souhaitez que [!INCLUDE[d365fin](includes/d365fin_md.md)] gère les différents types de validation. Par exemple, vous devez indiquer s'il s'agit d'un débit ou d'un crédit et si le type de validation doit être inclus dans la base d'amortissement.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Lois d'amortissement**, puis sélectionnez le lien connexe.  
2. Sélectionnez la loi d'amortissement que vous souhaitez configurer, puis sélectionnez l'action **Type paramètre compta. immo.**.
3. Dans la fenêtre **Type paramètre compta. immo.**, renseignez les champs, le cas échéant.

    > [!NOTE]  
>   Vous ne pouvez pas insérer ni supprimer de lignes dans la fenêtre **Type paramètre compta. immo**. Vous ne pouvez modifier que les lignes existantes.

    Il est recommandé de ne pas modifier les paramètres des lois d'amortissement pour lesquelles des écritures ont déjà été validées. Les modifications apportées n'ont pas d'incidence sur les écritures déjà validées, ce qui rendrait les statistiques des lois d'amortissement inexactes.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Pour configurer les modèles par défaut et les lots pour l'amortissement immobilisation
Pour chaque loi d'amortissement, vous définissez une configuration par défaut de modèles et de feuilles. Vous devez utiliser ces valeurs par défaut pour dupliquer les lignes d'une feuille vers une autre, créer des lignes feuille à l'aide du traitement par lots **Calculer amortissement** ou **Actualiser immobilisations**, dupliquer des coûts d'acquisition dans la feuille assurance.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Lois d'amortissement**, puis sélectionnez le lien connexe.  
2. Sélectionnez la loi d'amortissement pour laquelle vous souhaitez définir les feuilles par défaut, puis sélectionnez l'action **Configuration feuille immo.**.  
3. Pour avoir une configuration par défaut pour chaque utilisateur, choisissez le champ **Code utilisateur** à sélectionner à partir de la fenêtre **Utilisateurs**.  
4. Dans les autres champs, sélectionnez le modèle feuille ou la feuille qui doit être utilisé(e) par défaut.  

## <a name="see-also"></a>Voir aussi
[Paramétrage d'immobilisations](fa-setup.md)  
[Immobilisations](fa-manage.md)  
[Finances](finance.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

