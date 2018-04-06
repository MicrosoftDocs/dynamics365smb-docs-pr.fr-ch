---
title: "Analyse des montants réalisés et des montants budgétés| Microsoft Docs"
description: "Décrit comment analyser les montants réalisés et les montants budgétés."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 900a14c46a6e5c027b3cf8888bb59765902e50cb
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analyser les montants réalisés et les montants budgétés
Lors de la collecte, l'analyse, et le partage des données de votre société, vous voyez les montants réels comparés aux montants budgétés de tous les comptes et pour plusieurs périodes.

Pour analyser les montants budgétés, vous devez d'abord créer des budgets comptabilité. Pour plus d'informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Pour visualiser un budget comptabilité
Dans un budget doté d'axes, vous pouvez filtrer les écritures et visualiser des budgets spécifiques.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Budgets**, puis choisissez le lien associé.
2. Dans la fenêtre **Budgets**, ouvrez le budget que vous souhaitez visualiser.  
3. En haut de la fenêtre, renseignez les champs nécessaires pour définir ce qui est affiché. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, puis vous devez renseigner le champ **Afficher par**. Si vous n'avez pas sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, entrez la période appropriée dans le champ **Filtre date**.  

> [!NOTE]  
>   Seules les écritures budget en comptabilité contenant les codes filtre entrés sur le raccourci **Filtres** sont incluses dans le calcul. Les écritures budget contenant d'autres codes filtre ou ne contenant aucun code filtre sont exclues. Tant que le filtre est présent dans la fenêtre, le budget n'affiche que les écritures budget contenant ces codes filtre.  

> [!TIP]  
>   Si vous souhaitez modifier le budget, vous pouvez modifier les écritures budget. Choisissez un montant pour afficher les écritures Budget sous-jacentes.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Pour afficher les montants budgétés et réalisés de tous les comptes  
Vous pouvez afficher des budgets et les comparer aux chiffres réels dans différents modules de [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Plan comptable**, choisissez l'action **Réalisé/Budget par compte**.
3. En haut de la fenêtre, renseignez les champs nécessaires pour définir ce qui est affiché.  
4. Pour voir le détail d'un montant affiché, sélectionnez ce champ.  

> [!NOTE]  
>   Les filtres que vous définissez dans l'en-tête de la fenêtre sont appliqués aux écritures comptables et aux écritures budget.

Les colonnes les plus à gauche contiennent le plan comptable. Sur les cinq colonnes les plus à droite, les quatre premières affichent les montants crédit et débit budgétés, et réalisés pour chaque compte. La cinquième colonne indique la relation proportionnelle entre les montants budgétés et réalisés sur le compte général.  

> [!TIP]  
>   Le champ **Afficher par** de la fenêtre **Réalisé/Budget par compte** permet de sélectionner la longueur de la période. Le champ **Afficher en tant que** permet de sélectionner le mode de calcul des montants, à savoir **Solde période** ou **Solde au**. Choisissez **Période précédente** ou **Période suivante** pour changer de période.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Pour afficher les montants budgétés et réalisés de plusieurs périodes  
Au lieu de visualiser les montants budgétés et réalisés de tous les comptes au sein d'une seule période, vous pouvez afficher un certain nombre de périodes pour un seul compte.  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Plan comptable**, sélectionnez le compte général approprié, puis choisissez l'action **Réalisé/Budget compte général**.  
3. En haut de la fenêtre, renseignez les champs nécessaires pour définir ce qui est affiché.   
4. Pour voir le détail d'un montant affiché, sélectionnez ce champ.  

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Utilisation des tableaux d'analyse](bi-how-work-account-schedule.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

