---
title: Ventiler les revenus et les coûts sur plusieurs comptes généraux
description: Découvrez comment ventiler les coûts sur un ou plusieurs comptes dans votre comptabilité.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
---

# <a name="allocate-revenue-and-costs-to-multiple-general-ledger-accounts"></a>Ventiler les revenus et les coûts sur plusieurs comptes généraux

Cet article décrit comment utiliser les comptes de ventilation pour répartir les montants des documents vente et achat et des lignes feuille comptabilité entre différents comptes généraux. Vous pouvez ventiler les montants via une répartition fixe ou variable.  

La ventilation divise une ligne feuille comptabilité en lignes définies sur la page **Compte de ventilation**. Par exemple, si vous divisez une dépense de loyer de trois manières à l’aide d’axes analytiques, vous disposez de trois lignes à valider pour la ventilation. Par conséquent, vous disposez de six lignes comptables (ou éventuellement plus si vous utilisez la TVA ou la taxe de vente). Bien que cela valide plus d’écritures comptables que ce dont vous pourriez avoir besoin, cela vous permet de contrepasser des lignes individuelles au lieu de contrepasser toute la ventilation.

Les comptes de ventilation fonctionnent également avec les échelonnements. Pour en savoir plus sur les échelonnements, consultez [Échelonner les revenus et les dépenses](finance-how-defer-revenue-expenses.md).

Le tableau suivant présente les méthodes de ventilation que vous pouvez utiliser.

|Méthode de ventilation  |Description  |
|---------|---------|
|Fixe     | Lorsque vous souhaitez diviser les dépenses de manière répétée sur une période plus longue, vous pouvez utiliser une ventilation fixe. Une ventilation fixe vous permet de définir la division de la ventilation. Cette répartition ne change que lorsque vous modifiez la configuration sur la page **Compte de ventilation**.        |
|Variable     | Pour répartir les revenus ou les dépenses en fonction de valeurs qui changent dans le temps, utilisez la méthode de ventilation variable. Les ventilations variables vous permettent de spécifier les sources à utiliser pour calculer les pourcentages de ventilation. Cette méthode est utile, par exemple, pour répartir les coûts du personnel en fonction des effectifs variables dans un département ou une division. Un autre exemple est la répartition du coût du loyer en fonction de la superficie de l’atelier de production, qui peut varier selon la ligne de production au fil du temps. Les ventilations variables utilisent une combinaison d’axes analytiques et de comptes statistiques pour déterminer la manière dont les montants sont répartis sur une période donnée. Pour en savoir plus sur les comptes statistiques, consultez [Analyser les données avec les comptes statistiques](bi-use-statistical-accounts.md). Pour en savoir plus sur les axes analytiques, consultez [Utiliser les axes analytiques](finance-dimensions.md).        |

## <a name="use-a-fixed-share-or-percentage-method-to-allocate-amounts"></a>Utiliser une méthode de part ou de pourcentage fixe pour ventiler les montants

1. Choisissez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte de ventilation**, puis choisissez le lien associé.  
1. Sur la page **Comptes de ventilation**, choisissez **Nouveau**.
1. Renseignez les champs **N°** et **Nom**.
1. Dans le champ **Type compte**, choisissez **Fixe**.
1. Dans le champ **Type du compte de destination**, choisissez **Compte général** ou **Compte bancaire**.
1. Dans le champ **Numéro du compte de destination**, choisissez le compte sur lequel valider la valeur.
1. Facultatif : choisissez l’action **Axes analytiques**, puis spécifiez les axes analytiques à valider pour la ligne.
1. Dans les champs **Part** et **Pourcentage**, spécifiez comment répartir les montants sur le compte de destination.
  
   > [!TIP]
   > Si vous saisissez le montant réel à ventiler pour une ventilation fixe dans le champ **Part**, le champ **Pourcentage** affiche le pourcentage du montant total.
1. Répétez ce processus pour chaque compte à inclure dans la ventilation.

## <a name="use-a-variable-method-to-allocate-amounts"></a>Utiliser une méthode variable pour ventiler les montants

1. Choisissez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte de ventilation**, puis choisissez le lien associé.  
1. Sur la page **Comptes de ventilation**, choisissez **Nouveau**.
1. Renseignez le champ **N°** et **Nom**.
1. Dans le champ **Type compte**, choisissez **Variable**.
1. Dans le champ **Type du compte de destination**, choisissez **Compte général**.
1. Dans le champ **Numéro du compte de destination**, choisissez le compte sur lequel valider la valeur.
1. Dans le champ **Type du compte de ventilation**, choisissez **Compte statistique**.
1. Dans le champ **Période de calcul**, choisissez la période pour laquelle répartir les montants.
1. Facultatif : pour filtrer des sections analytiques globales spécifiques, choisissez l’action **Filtres du solde du compte de ventilation**, puis spécifiez les valeurs de filtre.
1. Facultatif : choisissez l’action **Axes analytiques**, puis spécifiez les axes analytiques à valider pour la ligne.

## <a name="allocate-amounts-on-the-fly"></a>Ventiler les montants à la volée

Vous créez des comptes de ventilation pour répartir les produits et les coûts pour les comptes généraux et les comptes bancaires. L’automatisation de la ventilation peut vous faire gagner beaucoup de temps. Toutefois, si vous souhaitez utiliser des comptes de ventilation, mais vous ne souhaitez pas les créer pour chaque compte général, vous pouvez gagner encore plus de temps.

L’option Copier à partir du parent vous permet d’utiliser le compte de ventilation pour répartir les montants de tout compte général sur une ligne d’un document ou d’une feuille. Dans le champ **Type de compte** d’une ligne document ou feuille, vous choisissez un compte général, puis choisissez le compte de ventilation dans le champ **N° du compte de ventilation**. Le montant de la ligne est réparti pour le compte général selon la configuration dans votre compte de ventilation. Il s’agit d’une méthode de ventilation moins transparente, mais il n’est pas nécessaire de créer un compte de ventilation spécifiquement pour le compte général.

Les ventilations ad hoc sont faciles à configurer. Au lieu de spécifier un compte bancaire ou général dans le champ **Type du compte de destination** de la page **Compte de ventilation**, choisissez l’option **Copier à partir du parent**. Laissez le champ **Numéro du compte de destination** vide. Lorsque vous choisissez le compte général sur la ligne document ou feuille, ce compte est utilisé pour ventiler les montants.

## <a name="verify-that-amounts-distribute-correctly-before-you-post-them"></a>Vérifier que les montants sont correctement répartis avant de les valider

Il existe plusieurs façons de vérifier que les montants sont correctement répartis :

* Sur la page **Compte de ventilation**, choisissez l’action **Tester la ventilation**. Utilisez le champ **Montant à ventiler** pour tester différents montants.
* Sur la page **Feuilles comptabilité**, choisissez la feuille et utilisez l’action **Aperçu validation**.

## <a name="adjust-the-distribution"></a>Ajuster la répartition

Si vous trouvez quelque chose dans une ventilation que vous souhaitez modifier, vous pouvez ajuster la ventilation avant de la valider.  

1. Ouvrez le document ou le journal contenant la ventilation que vous souhaitez modifier.
1. Choisissez la ligne, puis choisissez l’action **Répartir à nouveau les ventilations du compte**.
1. Sur la page **Modifier les ventilations**, effectuez votre ajustement.

## <a name="post-an-allocation-transaction"></a>Valider une transaction de ventilation

Les étapes suivantes décrivent comment valider une transaction de ventilation à partir d’un journal général. Les étapes sont les mêmes pour les documents vente et achat.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité**, puis sélectionnez le lien associé.  
1. Créez une ligne. Remplissez les champs de la même manière que vous le feriez pour tout autre type de journal général.
1. Si vous utilisez une ventilation fixe ou variable, remplissez les champs suivants :
    1. Dans le champ **Type compte**, choisissez **Compte de ventilation**.
    1. Dans le champ **N° compte**, choisissez le compte de ventilation.
1. Si vous utilisez une ventilation qui utilise l’option Copier à partir du parent, procédez comme suit :
    1. Dans le champ **Type compte**, choisissez **Compte général**.
    1. Dans le champ **N° compte**, choisissez le compte général.
    1. Dans le champ **N° du compte de ventilation**, choisissez le compte de ventilation configuré pour utiliser l’option Copier à partir du parent. 
1. Choisissez **Valider**.
1. 

## <a name="see-also"></a>Voir aussi

[Utilisation des feuilles comptabilité](ui-work-general-journals.md)  
