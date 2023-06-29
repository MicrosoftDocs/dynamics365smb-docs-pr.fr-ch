---
title: Valider l’écriture de clôture d’exercice
description: 'Décrit comment ouvrir la feuille spécifiée dans le traitement par lots Clôturer exercice comptable, puis examiner et valider l’écriture de clôture de fin d’exercice.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="posting-the-year-end-closing-entry"></a><a name="posting-the-year-end-closing-entry"></a>Validation de l’écriture de clôture d’exercice

Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d’exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.  

> [!TIP]
> En fonction des processus de travail de votre organisation, vous pouvez choisir de clôturer ou non les périodes comptables et les exercices dans [!INCLUDE [prod_short](includes/prod_short.md)]. La procédure suivante suppose que vous avez clôturé l’exercice en utilisant l’option *Périodes comptables*, généré une écriture de clôture d’exercice à l’aide du traitement par lots **Clôturer exercice comptable** et que vous êtes maintenant prêt à valider l’écriture de clôture d’exercice avec la compensation des écritures de compte de fonds propres. Votre organisation peut choisir de travailler différemment, par exemple valider l’écriture de clôture d’exercice dans le cadre de la clôture de l’exercice comptable.

## <a name="to-post-the-year-end-closing-entry"></a><a name="to-post-the-year-end-closing-entry"></a>Pour valider l’écriture de clôture d’exercice

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille comptabilité**, puis choisissez le lien associé.
2. Sur la page **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.
3. Examinez les écritures.
4. Pour valider la feuille, sélectionnez l’action **Valider**.

> [!NOTE]  
> En cas de détection d’une erreur, un message d’erreur s’affiche. Si la validation réussit, les entrées validées sont supprimées de la feuille. Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l’exercice soient transférés vers le bilan.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Clôturer des périodes comptables](year-close-account-periods.md)  
[Clôture plans](year-close-books.md)  
[Clôturer exercice comptable](year-close-income-statement.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
