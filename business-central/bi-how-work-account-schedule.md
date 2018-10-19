---
title: "Générer des états financiers à l'aide de tableaux d'analyse"
description: "Décrit comment utiliser des tableaux d'analyse pour créer différentes vues et différents états pour l'analyse des données de performances financières."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e63e507411f41c67caa94834f4d99861bd1ae77
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Préparer la génération d'états financiers avec des tableaux d'analyse et des catégories de compte
Utilisez les tableaux d'analyse pour obtenir un aperçu des données financières enregistrées dans votre plan comptable. Les tableaux d'analyse analysent les chiffres des comptes généraux et comparent les écritures comptables et les écritures comptables budget. Les résultats s'affichent dans les graphiques de votre tableau de bord, comme le graphique Trésorerie, et dans les états, comme les états Comptes de gestion et Bilan.

Vous accédez à ces deux états, par exemple, avec l'action **Relevés financiers** dans les tableaux de bord Gestionnaire d'activité et Comptable.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des exemples de tableaux d'analyse que vous pouvez utiliser immédiatement, vous pouvez sinon configurer vos propres lignes et colonnes pour spécifier les chiffres à comparer. Par exemple, vous pouvez créer des tableaux d'analyse pour calculer les marges bénéficiaires dans des axes tels que les départements ou les groupes de clients. Vous pouvez créer autant d'états financiers personnalisés que vous le souhaitez.  

La configuration de tableaux d'analyse exige une compréhension des données financières du plan comptable. Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget. Cela suppose que les budgets sont créés. Pour plus d'informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Catégories de compte et tableaux d'analyse
Vous pouvez utiliser les catégories de compte pour modifier la présentation de vos états financiers. Une fois que vous avez configuré vos catégories de compte dans la fenêtre **Catégories de compte général**, et que vous sélectionnez l'action **Générer les tableaux d'analyse**, les tableaux d'analyse sous-jacents pour les états financiers de base sont mis à jour. La prochaine fois que vous exécuterez l'un de ces états, par exemple l'état Relevé de solde, de nouveaux totaux et des sous-entrées seront ajoutés, en fonction de vos modifications. Pour plus d'informations, consultez la section « Catégories de compte » dans [Description des écritures comptables et du plan comptable](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Pour créer de nouveaux tableaux d'analyse  
 Vous pouvez utiliser des tableaux d'analyse pour analyser les chiffres des comptes généraux ou pour comparer les écritures comptables et les écritures comptables budget. Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tableaux d'analyse**, puis sélectionnez le lien associé.  
2. Dans la fenêtre **Noms tableaux d'analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d'analyse.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Choisissez l'action **Modifier tableau d'analyse**.
5. Dans la fenêtre **Tableau d'analyse**, renseignez les champs requis.  

    Une fois que vous avez créé un tableau d'analyse et configuré ses lignes, vous devez configurer ses colonnes. Vous pouvez le faire manuellement ou utiliser une présentation colonne prédéfinie.
6. Choisissez l'action **Modifier paramètres présentation colonne**.
7. Dans la fenêtre **Présentation colonne**, renseignez les champs requis.

> [!NOTE]  
> Si vous n'avez affecté aucune présentation colonne par défaut au tableau d'analyse, vous devez configurer les colonnes manuellement.

### <a name="to-copy-an-existing-account-schedule"></a>Pour copier un tableau d'analyse existant
Les tableaux d'analyse dans la version standard de [!INCLUDE[d365fin](includes/d365fin_md.md)] sont la base des états financiers standard, qui ne sont peut-être pas adaptés aux besoins de votre entreprise. Pour créer rapidement vos propres états financiers, vous pouvez commencer par copier un tableau d'analyse existant.
1. Dans la fenêtre **Tableaux d'analyse**, sélectionnez un tableau d'analyse, puis choisissez l'action **Copier le tableau d'analyse**.
2. Dans la fenêtre **Copier le tableau d'analyse**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.

### <a name="to-create-a-column-that-calculates-percentages"></a>Pour créer une colonne qui calcule des pourcentages  
Il se peut que vous vouliez inclure une colonne dans un tableau d'analyse pour calculer des pourcentages d'un total. Par exemple, si vous avez plusieurs lignes qui ventilent des ventes par dimension, vous pouvez juger utile de disposer d'une colonne indiquant le pourcentage des ventes totales que représente chaque ligne.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tableaux d'analyse**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Noms tableaux d'analyse**, sélectionnez le tableau d'analyse.  
3. Choisissez l'action **Modifier tableau d'analyse** pour configurer une ligne de tableau d'analyse et calculer le total sur lequel le pourcentage sera basé.  
4. Insérez une ligne juste au-dessus de la première ligne pour laquelle vous voulez afficher un pourcentage.  
5. Renseignez les champs de la ligne comme suit : dans le champ **Type totalisation**, entrez **Base de pourcentage**. Dans le champ **Totalisation**, saisissez une formule pour le total sur lequel le pourcentage sera basé. Par exemple, si la ligne 11 contient le total des ventes, saisissez **11**.  
6. Choisissez l'action **Modifier paramètres présentation colonne** pour configurer une colonne.  
7. Renseignez les champs de la ligne comme suit : dans le champ **Type colonne**, sélectionnez **Formule**. Dans le champ **Formule**, saisissez une formule correspondant au montant pour lequel vous voulez calculer un pourcentage, suivie de %. Par exemple, si le numéro de colonne N contient le solde période, saisissez **N%**.  
8. Répétez les étapes 4 à 7 pour chaque groupe de lignes que vous voulez ventiler par pourcentage.

## <a name="to-set-up-account-schedules-with-overviews"></a>Pour configurer des tableaux d'analyse avec des aperçus  
Vous pouvez utiliser un tableau d'analyse pour créer un état comparant les chiffres de la comptabilité et les chiffres budgétés.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tableaux d'analyse**, puis sélectionnez le lien associé.
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

## <a name="comparing-accounting-periods-using-period-formulas"></a>Comparaison de périodes comptables à l'aide de formules de période
Votre tableau d'analyse peut comparer les résultats de différentes périodes comptables, par exemple ce mois et le même mois l'année précédente. Pour ce faire, vous ajoutez une colonne avec le champ **Formule période comparaison**, puis définissez ce champ sur une formule de période.  

Une période comptable ne doit pas correspondre au calendrier, mais chaque exercice doit avoir le même nombre de périodes comptables, même si chaque période peut varier.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] utilise la formule de période pour calculer le montant de la période de comparaison en fonction de la période représentée dans le filtre date du formulaire de sélection de l'état. La période de comparaison est basée sur la période de la date de début du filtre de date. Les abréviations utilisées pour les spécifications de période sont les suivantes :


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Abréviation</th>
<th>Désignation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Période.</p></td>
</tr>
<tr class="even">
<td><p>DP</p></td>
<td><p>Dernière période de l'exercice, du semestre ou du trimestre.</p></td>
</tr>
<tr class="odd">
<td><p>FP</p></td>
<td><p>Fin de période de l'exercice, du semestre ou du trimestre.</p></td>
</tr>
<tr class="even">
<td><p>EC</p></td>
<td><p>Exercice comptable. Par exemple, EC[1..3] désigne le premier trimestre de l'exercice courant.</p></td>
</tr>
</tbody>
</table>

Exemples de formule :


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formule</th>
<th>Désignation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Vide&gt;</p></td>
<td><p>Période en cours</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Période précédente</p></td>
</tr>
<tr class="odd">
<td><p>-1EC[1..DP]</p></td>
<td><p>Ensemble de l'exercice comptable précédent</p></td>
</tr>
<tr class="even">
<td><p>-1EC</p></td>
<td><p>Période de l'exercice comptable précédent équivalente à la période en cours</p></td>
</tr>
<tr class="odd">
<td><p>-1EC[1..3]</p></td>
<td><p>Premier trimestre de l'exercice comptable précédent</p></td>
</tr>
<tr class="even">
<td><p>-1EC[1..FP]</p></td>
<td><p>Du début de l'exercice comptable précédent à la fin de la période de l'exercice comptable précédent incluse</p></td>
</tr>
<tr class="odd">
<td><p>-1EC[FP..DP]</p></td>
<td><p>De la fin de période de l'exercice précédent à la dernière période de l'exercice comptable précédent incluse</p></td>
</tr>
</tbody>
</table>

Pour effectuer des calculs basés par périodes, vous devez entrer une formule dans le champ **Formule date comparaison** à la place.

> [!NOTE]
> Il n'est pas toujours transparent de déterminer les périodes à comparer, car vous pouvez définir un filtre date sur un état qui couvre des dates différentes des périodes comptables représentées dans les données du plan comptable. Par exemple, vous créez un tableau d'analyse dans lequel vous souhaitez comparer cette période avec la même période l'année précédente. Vous définissez le champ **Filtre période date comparaison** sur *-1EC*. Ensuite, vous exécutez l'état le 28 février et définissez le filtre date sur Janvier et février. Par conséquent, le tableau d'analyse compare les mois de janvier et février de cette année au mois de janvier de l'année précédente, qui est la seule période comptable terminée des deux pour l'année précédente.  


## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

