---
title: Générer des états financiers à l’aide de tableaux d’analyse
description: Décrit comment utiliser des tableaux d’analyse pour créer différentes vues et différents états pour l’analyse des données de performances financières.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 91a97ab506f7536b9c468862709d1d39ed767d53
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335490"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Préparer la génération d’états financiers avec des tableaux d’analyse et des catégories de compte

Utilisez les tableaux d’analyse pour obtenir un aperçu des données financières enregistrées dans votre plan comptable. Les tableaux d’analyse analysent les chiffres des comptes généraux et comparent les écritures comptables et les écritures comptables budget. Les résultats s’affichent dans les graphiques de votre tableau de bord, comme le graphique Trésorerie, et dans les états, comme les états Comptes de gestion et Bilan.

Vous accédez à ces deux états, par exemple, avec l’action **Relevés financiers** dans les tableaux de bord Gestionnaire d’activité et Comptable.  

[!INCLUDE[prod_short](includes/prod_short.md)] fournit des exemples de tableaux d’analyse que vous pouvez utiliser immédiatement, vous pouvez sinon configurer vos propres lignes et colonnes pour spécifier les chiffres à comparer. Par exemple, vous pouvez créer des tableaux d’analyse pour calculer les marges bénéficiaires dans des axes tels que les départements ou les groupes de clients. Vous pouvez créer autant d’états financiers personnalisés que vous le souhaitez.  

La configuration de tableaux d’analyse exige une compréhension des données financières du plan comptable. Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget. Cela suppose que les budgets sont créés. Pour plus d’informations, voir [Créer des budgets comptabilité](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Tableaux d’analyse

Les tableaux d’analyse permettent de réorganiser des comptes répertoriés dans le plan comptable de manière à présenter des informations sur ces comptes. Vous pouvez configurer différentes présentations pour définir les informations que vous souhaitez extraire du plan comptable. L’une des fonctions principales des tableaux d’analyse est de fournir un emplacement pour les calculs ne pouvant être effectués directement dans le plan comptable, tels que la création de sous-totaux pour les groupes de comptes, qui peuvent être inclus dans de nouveaux totaux, puis utilisé dans d’autres totaux. Par exemple, les utilisateurs peuvent créer des tableaux d’analyse pour calculer les marges bénéficiaires dans des axes tels que les départements ou les groupes client. De plus, les écritures comptables et les écritures comptables budget peuvent être filtrées, par exemple, par solde période ou par montant débit.

Vous pouvez également comparer deux ou plusieurs tableaux d’analyse et présentations colonne à l’aide de formules. Ce type de comparaison permet de :

* créer des états financiers personnalisé ;
* créer autant de tableaux d’analyse que nécessaire, chacun étant doté d’un nom unique ;
* configurer différentes présentations d’états et imprimer les états avec les chiffre actuels.

## <a name="gl-account-categories"></a>Catégories de compte général

Vous pouvez utiliser les catégories de compte général pour modifier la présentation de vos états financiers. Une fois que vous avez configuré vos catégories de compte sur la page **Catégories de compte général**, et que vous sélectionnez l’action **Générer les tableaux d’analyse**, les tableaux d’analyse sous-jacents pour les états financiers de base sont mis à jour. La prochaine fois que vous exécuterez l’un de ces états, par exemple l’état **Relevé de solde**, de nouveaux totaux et des sous-entrées seront ajoutés, en fonction de vos modifications.

> [!NOTE]
> Les catégories de compte de niveau supérieur, telles que le nœud **Passif**, sont fixes et vous ne pouvez pas ajouter les vôtres. Cependant, vous pouvez supprimer et ajouter des catégories de compte à des niveaux inférieurs et modifier leur structure pour définir la façon dont le tableau d’analyse associé apparaît dans les états.
>
> Il est recommandé de créer et de structurer vos propres catégories de compte général de niveau inférieur à partir de zéro, dans une hiérarchie si nécessaire, plutôt que d’essayer de réorganiser les catégories existantes. Par exemple, vous pouvez restructurer le nœud **Passif** pour contenir un nouveau nœud **Équité** suivi des nœuds **Passif à court terme** et **Passif à long terme**.

## <a name="to-create-a-new-account-schedule"></a>Pour créer un tableau d’analyse

Vous pouvez utiliser des tableaux d’analyse pour analyser les chiffres des comptes généraux ou pour comparer les écritures comptables et les écritures comptables budget. Par exemple, vous pouvez afficher les écritures comptables en tant que pourcentages des écritures budget.

Les tableaux d’analyse dans la version standard de [!INCLUDE[prod_short](includes/prod_short.md)] sont la base des états financiers standard, qui ne sont peut-être pas adaptés aux besoins de votre entreprise. Pour créer rapidement vos propres états financiers, vous pouvez commencer par copier un tableau d’analyse existant. Reportez-vous à l’étape 3 ci-dessous.

La page **Aperçu tableau d’analyse** vous permet de consulter l’état financier défini par le tableau d’analyse. Dans l’exemple suivant, il est important de comprendre que ce que vous créez en tant que lignes et colonnes de tableau d’analyse peut uniquement être vu et validé sur la page **Aperçu tableau d’analyse**, que vous ouvrez à partir d’un tableau d’analyse en choisissant l’action **Aperçu**. La page **Tableau d’analyse** elle-même est uniquement une zone de configuration.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableaux d’analyse**, puis sélectionnez le lien associé.  
2. Sur la page **Tableaux d’analyse**, choisissez **Nouveau** pour créer un nom pour le tableau d’analyse.
3. Sinon, choisissez l’action **Copier le tableau d’analyse**, renseignez les deux champs, puis cliquez sur le bouton **OK**.
4. Renseignez les champs selon vos besoins. Dans le champ **Présentation colonne par déf.** sélectionnez une présentation existante. Vous pouvez la modifier ultérieurement au besoin.

    Vous utilisez les présentations de colonne pour définir des colonnes pour divers paramètres par lesquels les données financières dans les lignes sont affichées. Par exemple, vous pouvez créer une présentation de colonne de manière à comparer le solde période et le solde pour une même période de l’exercice actuel et du précédent, avec quatre colonnes. Pour plus d’informations, voir [Pour modifier une présentation de colonne](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Choisissez l’action **Modifier tableau d’analyse**.
6. Créez une ligne pour chaque élément financier que vous souhaitez voir apparaître dans l’état, par exemple une ligne pour des actifs à court terme et une autre pour les immobilisations. Pour obtenir de l’inspiration, visualisez les tableaux d’analyse existants de la société de démonstration CRONUS.
7. Choisissez l’action **Aperçu** pour visualiser l’état financier qui en résulte.
8. Sur la page **Aperçu tableau d’analyse**, dans le champ **Nom présentation colonne**, sélectionnez une autre présentation de colonne pour afficher les données financières selon d’autres paramètres.
9. Choisissez le bouton **OK**.

Vous avez désormais défini la base du tableau d’analyse, les lignes de données financières à afficher, et une présentation existante de colonnes pour afficher les données sur les lignes selon divers paramètres. Si la présentation de colonne par défaut que vous avez sélectionnée dans l’étape 4 ne convient pas à votre objectif, suivez la procédure suivante.

### <a name="to-edit-a-column-layout"></a>Pour modifier une présentation de colonne

Les présentations de colonne vous permettent de définir les colonnes devant être incluses dans l’état résultant. Par exemple, vous pouvez créer une présentation de manière à comparer le solde période et le solde pour une même période de l’exercice actuel et du précédent.

> [!NOTE]
> Une version imprimée/aperçu/enregistrée du tableau d’analyse peut afficher un maximum de cinq colonnes. Si le tableau d’analyse est uniquement destiné pour l’analyse de la page **Aperçu tableau d’analyse**, vous pouvez créer autant de colonnes que vous le souhaitez.

1. Sur la page **Tableaux d’analyse**, sélectionnez le tableau d’analyse approprié, puis cliquez sur l’action **Modifier paramètres présentation colonne**.
2. Sur la page **Présentations colonne**, créez une ligne pour chaque colonne en fonction de laquelle les données financières sont affichées dans l’état financier. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Choisissez le bouton **OK**.
4. Ouvrez la page **Aperçu tableau d’analyse** de temps en temps pour vérifier que la nouvelle présentation de colonne fonctionne comme prévu.

> [!NOTE]
> Les colonnes que vous définissez sur chaque ligne représentent les colonnes 3 et supérieures de la page **Aperçu tableau d’analyse**. Les deux premières colonnes, **N° ligne** et **Description**, sont fixes.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Pour créer une colonne qui calcule des pourcentages

Il se peut que vous vouliez inclure une colonne dans un tableau d’analyse pour calculer des pourcentages d’un total. Par exemple, si vous avez plusieurs lignes qui ventilent des ventes par dimension, vous pouvez juger utile de disposer d’une colonne indiquant le pourcentage des ventes totales que représente chaque ligne.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableaux d’analyse**, puis sélectionnez le lien associé.
2. Sur la page **Noms tableaux d’analyse**, sélectionnez le tableau d’analyse.  
3. Choisissez l’action **Modifier tableau d’analyse** pour configurer une ligne de tableau d’analyse et calculer le total sur lequel le pourcentage sera basé.  
4. Insérez une ligne juste au-dessus de la première ligne pour laquelle vous voulez afficher un pourcentage.  
5. Renseignez les champs de la ligne comme suit : dans le champ **Type totalisation**, entrez **Base de pourcentage**. Dans le champ **Totalisation**, saisissez une formule pour le total sur lequel le pourcentage sera basé. Par exemple, si la ligne 11 contient le total des ventes, saisissez **11**.  
6. Choisissez l’action **Modifier paramètres présentation colonne** pour configurer une colonne.  
7. Renseignez les champs de la ligne comme suit : dans le champ **Type colonne**, sélectionnez **Formule**. Dans le champ **Formule**, saisissez une formule correspondant au montant pour lequel vous voulez calculer un pourcentage, suivie de %. Par exemple, si le numéro de colonne N contient le solde période, saisissez **N%**.  
8. Répétez les étapes 4 à 7 pour chaque groupe de lignes que vous voulez ventiler par pourcentage.

## <a name="to-set-up-account-schedules-with-overviews"></a>Pour configurer des tableaux d’analyse avec des aperçus

Vous pouvez utiliser un tableau d’analyse pour créer un état comparant les chiffres de la comptabilité et les chiffres budgétés.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Tableaux d’analyse**, puis sélectionnez le lien associé.
2. Sur la page **Noms tableaux d’analyse**, sélectionnez le tableau d’analyse.  
3. Choisissez l’action **Modifier tableau d’analyse**  
4. Sur la page **Tableau d’analyse**, sélectionnez le nom du tableau d’analyse souhaité dans le champ **Nom**.
5. Choisissez l’option **Insérer comptes**.  
6. Sélectionnez les comptes à inclure dans votre relevé, puis cliquez sur le bouton **OK**.

    Ces comptes sont à présent insérés dans le tableau d’analyse. Si vous le souhaitez, vous pouvez aussi modifier la présentation colonne.  
7. Sélectionnez l’action **Présentation**.  
8. Sur la page **Aperçu tableau d’analyse**, sur le raccourci **Filtres axe**, définissez le filtre budget sur le nom du filtre désiré.  
9. Cliquez sur le bouton **OK**.  

Vous pouvez maintenant copier et coller votre budget dans un classeur.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Comparaison de périodes comptables à l’aide de formules de période

Votre tableau d’analyse peut comparer les résultats de différentes périodes comptables, par exemple ce mois et le même mois l’année précédente. Pour ce faire, ouvrez la page **Présentation colonne** et personnalisez-la en ajoutant le champ **Formule période comparaison** sous forme de colonne. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md). Vous pouvez ensuite définir ce champ sur une formule de période.  

Une période comptable ne doit pas correspondre au calendrier, mais chaque exercice doit avoir le même nombre de périodes comptables, même si chaque période peut varier.  

[!INCLUDE[prod_short](includes/prod_short.md)] utilise la formule de période pour calculer le montant de la période de comparaison en fonction de la période représentée dans le filtre date du formulaire de sélection de l’état. La période de comparaison est basée sur la période de la date de début du filtre de date. Les abréviations utilisées pour les spécifications de période sont les suivantes :

| Abréviation | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Période                                                                                |
| DP           | Dernière période de l’exercice, du semestre ou du trimestre.                                   |
| FP           | Fin de période de l’exercice, du semestre ou du trimestre. Utilisez FP dans les formules pour définir la période qui commence ou termine la formule. Par exemple, EC\[1..FP\] désigne la durée entre le début de l’exercice comptable en cours et la fin de la période.|
| EC           | Exercice comptable. Par exemple, EC\[1..3\] désigne le premier trimestre de l’exercice courant |

Exemples de formule :

| Formule         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Période en cours                                                                                  |
| \-1P            | Période précédente                                                                                 |
| \-1EC\[1..DP\]  | Ensemble de l’exercice comptable précédent                                                                     |
| \-1EC           | Période de l’exercice comptable précédent équivalente à la période en cours                                                          |
| \-1EC\[1..3\]   | Premier trimestre de l’exercice comptable précédent                                                           |
| \-1EC\[1..FP\]  | Du début de l’exercice comptable précédent à la fin de la période de l’exercice comptable précédent, les deux périodes incluses |
| \-1EC\[FP..DP\] | De la fin de la période de l’exercice comptable précédent à la dernière période de l’exercice comptable précédent, les deux périodes incluses   |

Pour effectuer des calculs basés par périodes, vous devez entrer une formule dans le champ **Formule date comparaison** à la place. Par exemple, si le champ est défini sur -1A, [!INCLUDE [prod_short](includes/prod_short.md)] procède à une comparaison à la même période 1 an avant.

> [!NOTE]
> Il n’est pas toujours transparent de déterminer les périodes à comparer, car vous pouvez définir un filtre date sur un état qui couvre des dates différentes des périodes comptables représentées dans les données du plan comptable. Par exemple, vous créez un tableau d’analyse dans lequel vous souhaitez comparer cette période avec la même période l’année précédente. Vous définissez le champ **Formule date comparaison** sur *-1EC*. Ensuite, vous exécutez l’état le 28 février et définissez le filtre date sur Janvier et février. Par conséquent, le tableau d’analyse compare les mois de janvier et février de cette année au mois de janvier de l’année précédente, qui est la seule période comptable terminée des deux pour l’année précédente.  

Pour plus d’informations sur les formules de date, voir [Utilisation de dates civiles et des heures](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Veille économique](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]