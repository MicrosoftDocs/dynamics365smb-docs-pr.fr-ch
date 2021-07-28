---
title: Analyse comparative Réel/Budget
description: Cette rubrique explique comment analyser les montants réels par rapport aux montants budgétés afin de collecter, d’analyser et de partager les données de votre entreprise.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 9011f3d488c659b7b2b44f8801c4af055f51bc54
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437116"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analyser les montants réalisés et les montants budgétés
Lors de la collecte, l’analyse, et le partage des données de votre société, vous voyez les montants réels comparés aux montants budgétés de tous les comptes et pour plusieurs périodes.

Pour analyser les montants budgétés, vous devez d’abord créer des budgets comptabilité. Pour plus d’informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Pour visualiser un budget comptabilité
Dans un budget doté d’axes, vous pouvez filtrer les écritures et visualiser des budgets spécifiques.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Budgets comptables**, puis choisissez le lien associé.
2. Sur la page **Budgets**, ouvrez le budget que vous souhaitez visualiser.  
3. En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Si vous avez sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, puis vous devez renseigner le champ **Afficher par**. Si vous n’avez pas sélectionné **Période** dans le champ **Afficher lignes** ou **Afficher colonnes**, entrez la période appropriée dans le champ **Filtre date**.  

> [!NOTE]  
>   Seules les écritures budget en comptabilité contenant les codes filtre entrés sur le raccourci **Filtres** sont incluses dans le calcul. Les écritures budget contenant d’autres codes filtre ou ne contenant aucun code filtre sont exclues. Tant que le filtre est présent sur la page, le budget n’affiche que les écritures budget contenant ces codes filtre.  

> [!TIP]  
>   Si vous souhaitez modifier le budget, vous pouvez modifier les écritures budget. Choisissez un montant pour afficher les écritures Budget sous-jacentes.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Pour afficher les montants budgétés et réalisés de tous les comptes  
Vous pouvez afficher des budgets et les comparer aux chiffres réels dans différents modules de [!INCLUDE[prod_short](includes/prod_short.md)].

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, choisissez l’action **Réalisé/Budget par compte**.
3. En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché.  
4. Pour voir le détail d’un montant affiché, sélectionnez ce champ.  

> [!NOTE]  
>   Les filtres que vous définissez dans l’en-tête de la page sont appliqués aux écritures comptables et aux écritures budget.

Les colonnes les plus à gauche contiennent le plan comptable. Sur les cinq colonnes les plus à droite, les quatre premières affichent les montants crédit et débit budgétés, et réalisés pour chaque compte. La cinquième colonne indique la relation proportionnelle entre les montants budgétés et réalisés sur le compte général.  

> [!TIP]  
>   Le champ **Afficher par** de la page **Réalisé/Budget par compte** permet de sélectionner la longueur de la période. Le champ **Afficher en tant que** permet de sélectionner le mode de calcul des montants, à savoir **Solde période** ou **Solde au**. Choisissez **Période précédente** ou **Période suivante** pour changer de période.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Pour afficher les montants budgétés et réalisés de plusieurs périodes  
Au lieu de visualiser les montants budgétés et réalisés de tous les comptes au sein d’une seule période, vous pouvez afficher un certain nombre de périodes pour un seul compte.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, sélectionnez le compte général approprié, puis choisissez l’action **Réalisé/Budget compte général**.  
3. En haut de la page, renseignez les champs nécessaires pour définir ce qui est affiché.   
4. Pour voir le détail d’un montant affiché, sélectionnez ce champ.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Utilisation des tableaux d’analyse](bi-how-work-account-schedule.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]