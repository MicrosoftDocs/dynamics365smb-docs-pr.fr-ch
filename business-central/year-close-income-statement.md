---
title: Clôturer les comptes de gestion
description: 'À la clôture d’exercice, vous devez exécuter le traitement par lots Clôture comptes de gestion afin de clôturer les périodes comptables de l’exercice fiscal.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.date: 06/25/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="closing-income-statement-accounts"></a>Clôturer les comptes de gestion
Lorsqu’un exercice comptable est terminé, vous devez clôturer les périodes qui le composent. Vous exécutez pour cela le traitement par lots **Solder les comptes de gestion**. Ce traitement transfère le résultat de l’exercice dans un compte de bilan et clôture les comptes de gestion. Vous créez des lignes dans une feuille, que vous pouvez valider par la suite.

## <a name="to-run-the-close-income-statement-batch-job"></a>Pour exécutez le traitement par lots Solder les comptes de gestion
1. Clôturez l’exercice comptable. L’exercice comptable doit être clôturé avant le lancement du traitement par lots. Pour plus d’informations, reportez vous à [Clôturer des périodes comptables](year-close-account-periods.md).
2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clôturer exercice comptable**, puis choisissez le lien associé.
3. Pour lancer le traitement par lots, cliquez sur le bouton **OK**.

## <a name="about-the-close-income-statement-batch-job"></a>À propos du traitement par lots Solder les comptes de gestion
Le traitement par lots traite tous les comptes généraux de type Compte de gestion et crée des écritures qui annulent leurs soldes respectifs. C’est-à-dire, chaque écriture représente la somme de toutes les écritures comptables du compte de l’exercice comptable. Ces nouvelles écritures sont placées dans une feuille, dans laquelle vous devez spécifier un compte contrepartie et un compte de bénéfices avant de valider. Lorsque vous validez la feuille, une écriture est validée sur chaque compte de gestion afin que son solde soit égal à zéro et en même temps le résultat de l’exercice est transféré sur le compte de bilan.

Vous devez valider la feuille vous-même. Le traitement par lots ne valide pas les écritures automatiquement, sauf lorsqu’une devise report supplémentaire est utilisée. Lorsque vous utilisez une devise report supplémentaire, le traitement par lots valide les écritures directement dans la comptabilité.

La date sur les lignes insérées par le traitement par lots dans la feuille est toujours une date de clôture pour l’exercice comptable. La date de clôture est une date fictive située entre le dernier jour de l’exercice comptable précédent et le premier jour du nouvel exercice comptable. L’avantage de valider sur une date de clôture est que vous maintenez des soldes corrects pour les dates ordinaires de l’exercice comptable.

Le traitement par lots **Solder les comptes de gestion** peut être utilisé à plusieurs reprises. Vous pouvez valider dans un exercice comptable précédent, même après que les comptes de gestion aient été clôturés, si vous exécutez à nouveau le traitement par lots.

## <a name="see-also"></a>Voir aussi

[Clôture plans](year-close-books.md)  
[Valider l’écriture de clôture d’exercice](year-how-post-year-end-close-entry.md)  
[Utiliser des périodes et exercices comptables](finance-accounting-periods-and-fiscal-years.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
