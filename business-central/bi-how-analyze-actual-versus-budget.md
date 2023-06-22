---
title: Analyser les montants réalisés et les montants budgétés
description: 'Cet article explique comment analyser les montants réels par rapport aux montants budgétés afin de collecter, d’analyser et de partager les données de votre entreprise.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts" />Analyser les montants réalisés et les montants budgétés

Lors de la collecte, l’analyse, et le partage des données de votre société, vous voyez les montants réels comparés aux montants budgétés de tous les comptes et pour plusieurs périodes.

Pour analyser les montants budgétés, vous devez d’abord créer des budgets comptabilité. Pour plus d’informations, consultez [Créer des budgets](finance-how-create-budgets.md).

## <a name="view-a-gl-budget" />Afficher un budget comptabilité

Dans un budget doté d’axes, vous pouvez filtrer les écritures et visualiser des budgets spécifiques.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Budgets comptabilité**, puis choisissez le lien associé.
2. Sur la page **Budgets comptabilité**, ouvrez le budget que vous souhaitez visualiser.  
3. En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, alors vous devez renseigner le champ **Afficher par**. Si vous n’avez pas sélectionné **Période** dans l’un de ces champs, entrez la période appropriée dans le champ **Filtre date**.  

> [!NOTE]  
> Seules les écritures budget en comptabilité contenant les codes filtre entrés sur le raccourci **Filtres** sont incluses dans le calcul. Les écritures budget contenant d’autres codes filtre ou ne contenant aucun code filtre sont exclues. Tant que le filtre est présent sur la page, le budget n’affiche que les écritures budget contenant ces codes filtre.  

> [!TIP]  
> Utilisez l’action **Modifier le budget** pour modifier le budget. Sur la page des budgets, choisissez un montant pour afficher les écritures Budget sous-jacentes.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts" />Afficher les montants budgétés et réalisés de tous les comptes

Vous pouvez afficher des budgets et les comparer aux chiffres réels dans différents modules de [!INCLUDE[prod_short](includes/prod_short.md)].

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, choisissez l’action **Réalisé/Budget par compte**.
3. Dans le raccourci **Options**, renseignez les champs nécessaires pour définir ce qui est affiché dans la table.  
4. Survolez un champ de la table pour lire une brève description du montant affiché.

> [!NOTE]  
> Les filtres que vous définissez dans l’en-tête de la page sont appliqués à la fois aux écritures comptables et aux écritures budget.

Les colonnes les plus à gauche contiennent le plan comptable. Sur les cinq colonnes les plus à droite, les quatre premières affichent les montants crédit et débit budgétés, et réalisés pour chaque compte. La cinquième colonne indique la relation proportionnelle entre les montants budgétés et réalisés sur le compte général.  

> [!TIP]  
> Le champ **Afficher par** de la page **Réalisé/Budget par compte** permet de sélectionner la longueur de la période. Le champ **Afficher en tant que** permet de sélectionner le mode de calcul des montants, à savoir **Solde période** ou **Solde au**. Choisissez **Période précédente** ou **Période suivante** pour changer de période.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods" />Pour afficher les montants budgétés et réalisés de plusieurs périodes

Au lieu de visualiser les montants budgétés et réalisés de tous les comptes au sein d’une seule période, vous pouvez afficher un certain nombre de périodes pour un seul compte.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, sélectionnez le compte général approprié, puis choisissez l’action **Réalisé/Budget compte général**.  
3. Dans le raccourci **Options**, renseignez les champs nécessaires pour définir ce qui est affiché dans la table.  
4. Dans le raccourci **Lignes**, survolez un champ de la table pour lire une brève description du montant affiché.  

## <a name="see-related-training-at-microsoft-learnlearnmodulesbudgets-exchange-rates-dynamics--business-centralindex" />Voir la formation associée sur [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index).

## <a name="see-also" />Voir aussi

[Décisionnel pour le secteur de la finance](bi.md)  
[Utiliser les états financiers](bi-how-work-account-schedule.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
