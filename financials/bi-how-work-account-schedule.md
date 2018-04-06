---
title: Utiliser des tableaux d'analyse| Microsoft Docs
description: "Décrit comment utiliser des tableaux d'analyse pour créer différentes vues et différents états pour l'analyse des données de performances financières."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7b28d3ec6f4a52c5229d2e121ff1fe8ed847eeb7
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-account-schedules"></a>Utilisation des tableaux d'analyse
Utilisez les tableaux d'analyse pour obtenir un aperçu des données financières enregistrées dans votre plan comptable. Les tableaux d'analyse analysent les chiffres des comptes généraux et comparent les écritures comptables et les écritures comptables budget. Les résultats s'affichent dans les graphiques du tableau de bord, dans le plan de trésorerie, par exemple.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des exemples de tableaux d'analyse que vous pouvez utiliser immédiatement, vous pouvez sinon configurer vos propres lignes et colonnes pour spécifier les chiffres à comparer. Par exemple, vous pouvez créer des tableaux d'analyse pour calculer les marges bénéficiaires dans des axes tels que les départements ou les groupes de clients. Vous pouvez créer autant d'états financiers personnalisés que vous le souhaitez.  

La configuration de tableaux d'analyse exige une compréhension des données financières du plan comptable. Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget. Cela suppose que les budgets sont créés. Pour plus d'informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Catégories de compte et tableaux d'analyse
Vous pouvez utiliser les catégories de compte pour modifier la présentation de vos états financiers. Une fois que vous avez configuré vos catégories de compte dans la fenêtre **Catégories de compte général**, et que vous sélectionnez l'action **Générer les tableaux d'analyse**, les tableaux d'analyse sous-jacents pour les états financiers de base sont mis à jour. La prochaine fois que vous exécutez l'un de ces états, par exemple le solde relevé, de nouveaux totaux et des sous-entrées sont ajoutés, en fonction de vos modifications. Pour plus d'informations, reportez-vous à [Les écritures comptables et le plan comptable](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Pour créer de nouveaux tableaux d'analyse  
 Vous pouvez utiliser des tableaux d'analyse pour analyser les chiffres des comptes généraux ou pour comparer les écritures comptables et les écritures comptables budget. Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.  
2. Dans la fenêtre **Noms tableaux d'analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d'analyse.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Choisissez l'action **Modifier tableau d'analyse**.
5. Dans la fenêtre **Tableau d'analyse**, renseignez les champs requis.  

    Une fois que vous avez créé un tableau d'analyse et configuré ses lignes, vous devez configurer ses colonnes. Vous pouvez le faire manuellement ou utiliser une présentation colonne prédéfinie.
6. Choisissez l'action **Modifier paramètres présentation colonne**.
7. Dans la fenêtre **Présentation colonne**, renseignez les champs requis.

> [!NOTE]  
>   Si vous n'avez affecté aucune présentation colonne par défaut au tableau d'analyse, vous devez configurer les colonnes manuellement.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Pour créer une colonne qui calcule des pourcentages  
Il se peut que vous vouliez inclure une colonne dans un tableau d'analyse pour calculer des pourcentages d'un total. Par exemple, si vous avez plusieurs lignes qui ventilent des ventes par dimension, vous pouvez juger utile de disposer d'une colonne indiquant le pourcentage des ventes totales que représente chaque ligne.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.
2. Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez le tableau d'analyse.  
3. Choisissez l'action **Modifier tableau d'analyse** pour configurer une ligne de tableau d'analyse et calculer le total sur lequel le pourcentage sera basé.  
4. Insérez une ligne juste au-dessus de la première ligne pour laquelle vous voulez afficher un pourcentage.  
5. Renseignez les champs de la ligne comme suit : dans le champ **Type totalisation**, entrez **Base de pourcentage**. Dans le champ **Totalisation**, saisissez une formule pour le total sur lequel le pourcentage sera basé. Par exemple, si la ligne 11 contient le total des ventes, saisissez **11**.  
6. Choisissez l'action **Modifier paramètres présentation colonne** pour configurer une colonne.  
7. Renseignez les champs de la ligne comme suit : dans le champ **Type colonne**, sélectionnez **Formule**. Dans le champ **Formule**, saisissez une formule correspondant au montant pour lequel vous voulez calculer un pourcentage, suivie de %. Par exemple, si le numéro de colonne N contient le solde période, saisissez **N%**.  
8. Répétez les étapes 4 à 7 pour chaque groupe de lignes que vous voulez ventiler par pourcentage.

## <a name="to-set-up-account-schedules-with-overviews"></a>Pour configurer des tableaux d'analyse avec des aperçus  
Vous pouvez utiliser un tableau d'analyse pour créer un état comparant les chiffres de la comptabilité et les chiffres budgétés.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Tableaux d'analyse**, puis choisissez le lien connexe.
2. Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez le tableau d'analyse.  
3. Choisissez l'action **Modifier tableau d'analyse**  
4. Dans la fenêtre **Tableau d'analyse**, sélectionnez le nom du tableau d'analyse souhaité dans le champ **Nom**.
5. Choisissez l'option **Insérer comptes**.  
6. Sélectionnez les comptes à inclure dans votre relevé, puis cliquez sur le bouton **OK**.

    Ces comptes sont à présent insérés dans le tableau d'analyse. Si vous le souhaitez, vous pouvez aussi modifier la présentation colonne.  
7. Sélectionnez l'action **Présentation**.  
8. Sur le raccourci **Filtres axe**, définissez le filtre budget sur le nom du filtre désiré.  
9. Cliquez sur le bouton **OK**.  

Vous pouvez maintenant copier et coller votre budget dans un classeur.

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

