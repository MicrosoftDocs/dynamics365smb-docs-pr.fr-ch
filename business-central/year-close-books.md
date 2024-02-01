---
title: Aperçu des tâches pour clôturer les livres
description: 'En savoir plus sur le processus de clôture des livres d’un exercice ou d’une période fiscale, et ce qui a lieu après la clôture à la fin d’un exercice.'
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Clôture des livres
Après vous être assuré que tous vos comptes sont à jour et avoir ventilé les coûts et les bénéfices, vous pouvez clôturer les livres d’un exercice ou d’une période comptable.

Vous n’êtes pas obligé de clôturer un exercice mais cela vous aidera à travailler plus facilement dans le système parce que vous serez en mesure de bénéficier des options de filtrage commodes à votre disposition. Vous ne devrez pas vous préoccuper de la perte de détails de transactions lors de la clôture parce que tous les détails sont conservés, même après la clôture de l’année.

## Processus de clôture des livres
Le processus de clôture d’un livre inclut les tâches principales suivantes :

1. Clôture de la période comptable.

    Un exercice comptable est défini comme une ou plusieurs périodes, telles qu’elles sont définies sur la page **Périodes comptables**. Un exercice fiscal type contient 12 périodes d’un mois chacune, mais vous pouvez également choisir un autre mode de définition des exercices.

    Pour plus d’informations, reportez vous à [Clôturer des périodes comptables](year-close-account-periods.md).
2. Enregistrement des écritures de l’exercice précédent.

    Lorsque vous clôturez un exercice fiscal, vous devez saisir un certain nombre de transactions administratives (telles que les articles prépayés ou à payer). Ces transactions sont appelées écritures d’ajustement. Il n’existe pas de règles spécifiques pour la validation de ces écritures et, comme pour les autres écritures, le champ **Écr. exercice précédent** de ces écritures est activé si elles sont validées dans une date d’un exercice comptable clôturé. Même si un exercice comptable a été clôturé, vous pouvez toujours y valider des écritures.
3. Transfert des soldes des comptes de gestion au compte de bilan.

    Une fois qu’un exercice comptable a été clôturé et que toutes les écritures de l’exercice précédent ont été validées, les comptes de gestion doivent être soldés et le revenu net de l’exercice doit être transféré dans un compte en capitaux propres dans le bilan. Pour cela, utilisez le traitement par lots Solder les comptes de gestion. Le traitement par lots traite tous les comptes généraux de type Compte de gestion et crée des écritures qui inversent leurs soldes. Ces écritures sont placées dans une feuille à partir de laquelle elles peuvent être validées. Le traitement par lots ne les valide pas automatiquement, sauf lorsqu’une devise report supplémentaire est utilisée. Lorsque vous utilisez une devise report supplémentaire, le traitement par lots valide directement dans la comptabilité.

    Pour plus d’informations, reportez-vous à [Solder les comptes de gestion](year-close-income-statement.md).
4. Validation de l’écriture de clôture d’exercice en même temps que les écritures comptables de fonds propres de décalage.

    Lorsque le traitement par lots Solder les comptes de gestion est terminé, vous validez les écritures générées par le traitement. Si vous n’avez pas spécifié de compte de bénéfices non répartis dans le traitement par lots, saisissez une ligne avec une écriture contrepartie qui valide le revenu net dans le compte général en capitaux propres adéquat dans le bilan. Pour terminer, validez la feuille.

    Pour plus d’informations, reportez-vous à [Valider une écriture de clôture d’exercice](year-how-post-year-end-close-entry.md).

## Ce qui se produit lorsque vous clôturez
Lorsque vous clôturez en fin d’exercice, le système déplace votre bénéfice des bénéfices calculés vers le compte Réserve. Le système marque également l’exercice comptable comme « clôturé » et toutes les écritures suivantes pour l’exercice clôturé comme « écritures de l’exercice précédent ».

Le système génère ensuite une écriture de clôture mais ne la valide pas automatiquement. Vous avez la possibilité de créer les écritures comptables de fonds propres de décalage qui vous permettent de choisir la manière dont vous voulez affecter votre écriture de clôture. Par exemple, si votre société comprend plusieurs départements, vous pouvez laisser le système générer une écriture de clôture unique pour tous les départements et créer une écriture de décalage pour le compte de fonds propres de chaque département.

Vous pouvez valider dans un exercice comptable précédent, même après la clôture des comptes résultats, si vous exécutez de nouveau le traitement par lots Solder les comptes de gestion par la suite.

## Voir aussi

[Utiliser des périodes et exercices comptables](finance-accounting-periods-and-fiscal-years.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]