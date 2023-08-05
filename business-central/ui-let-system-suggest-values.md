---
title: Permettre à Business Central de suggérer des valeurs
description: "Pour éviter des calculs manuels et effectuer les tâches rapidement et précisément, vous pouvez configurer la saisie automatisée de données afin que Business\_Central renseigne les champs sélectionnés."
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '39, 251, 981'
ms.date: 04/01/2021
ms.author: edupont
---
# Laisser [!INCLUDE[prod_short](includes/prod_short.md)] suggérer des valeurs
[!INCLUDE[prod_short](includes/prod_short.md)] peut vous aider à effectuer ces tâches plus rapidement et précisément en préremplissant les champs ou en complétant les lignes avec des données que vous devriez sinon calculer et saisir vous-même. Bien qu’une telle saisie de données automatisée soit toujours correcte, vous pouvez la modifier par la suite si vous le souhaitez.

La fonctionnalité qui saisit les valeurs de champ pour vous est en général proposée pour les tâches qui demandent la saisie de volumes importants de données transactionnelles et pour lesquelles vous souhaitez éviter les erreurs et gagner du temps. Cette rubrique contient une sélection de ces fonctionnalités. Davantage de sections seront ajoutées dans les prochaines mises à jour de [!INCLUDE[prod_short](includes/prod_short.md)].

## La case à cocher **Suggérer le montant contrepartie** sur la page **Noms feuille comptabilité**
Lorsque, par exemple, vous saisissez des lignes feuille comptabilité pour plusieurs frais qui doivent tous être validés dans le même compte bancaire, chaque fois que vous saisissez une nouvelle ligne feuille pour les frais, vous pouvez faire en sorte que le champ **Montant** de la ligne compte bancaire soit automatiquement mis à jour avec le montant qui équilibre les frais. Pour plus d’informations sur l’utilisation des feuilles comptabilité, reportez-vous à [Utiliser des feuilles comptabilité](ui-work-general-journals.md).

### Pour que le champ **Montant** sur les lignes feuille comptabilité contrepartie soit renseigné automatiquement
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles comptabilité**, puis choisissez le lien associé.
2. Sur la ligne du nom de votre feuille comptabilité favorite, cochez la case **Suggérer le montant contrepartie**.
3. Ouvrez la feuille comptabilité commencez à enregistrer et valider des transactions en utilisant la fonctionnalité décrite pour la saisie automatique d’une valeur de champ.       

Pour plus d’informations sur la procédure permettant de configurer un nom de feuille comptabilité personnel, par exemple pour la gestion des frais, reportez-vous à [Utiliser des feuilles comptabilité](ui-work-general-journals.md).

## Le champ **Renseigner automatiquement la date de réception** sur la page **Enregistrement de paiement**
La page **Enregistrement de paiement** affiche les arriérés de paiement entrants sous la forme de lignes représentant les documents vente pour lesquels un montant doit être payé. Pour plus d’informations sur le lettrage des paiements client, reportez-vous à [Rapprocher les paiements client à partir d’une liste des documents vente échus](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Vos tâches principales sur la page consistent à cocher la case **Paiement effectué** et à renseigner le champ **Date de réception**. Vous pouvez définir [!INCLUDE[prod_short](includes/prod_short.md)] de sorte à saisir automatiquement la date de travail dans le champ **Date de réception** lorsque vous cochez la case **Paiement effectué**.

### Pour que le champ **Date de réception** de la page **Enregistrement de paiement** soit automatiquement renseigné
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramétrage de l’enregistrement de paiement**, puis choisissez le lien associé.
2. Cochez la case **Renseigner automatiquement la date de réception**.
3. Ouvrez la page **Enregistrement de paiement** et commencer à traiter les paiements client entrants à l’aide de la fonctionnalité décrite pour la saisie automatique d’une valeur de champ.

## Voir aussi
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finances](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]