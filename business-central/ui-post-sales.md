---
title: Validation de documents vente
description: Découvrez les différentes fonctions de validation pour valider les documents vente et comment mettre à jour les documents validés.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Validation des ventes

Dans le menu **Validation** sur un document vente, vous pouvez faire votre choix parmi les fonctions de validation suivantes :

* **Valider**
* **Valider et créer**
* **Valider et envoyer**
* **Aperçu compta.**
* **Valider par lot**
* **Impression test**

> [!NOTE]
> Pour les commandes vente, vous pouvez également voir les options liées à la fonctionnalité de prépaiement. Pour plus d’informations, voir [Facturer les acomptes](finance-invoice-prepayments.md).

Lorsque vous avez renseigné toutes les lignes et entré toutes les informations de la commande de vente, vous pouvez la valider. Cela crée une expédition et une facture.

Lorsqu’une commande vente est validée, le compte du client, les écritures comptables et les écritures comptables article sont mis à jour.

Pour chaque commande vente, une écriture vente est créée dans la table **Écriture comptable**. Une écriture est également créée dans le compte client de la table **Écriture comptable client** et une écriture comptable est créée dans le compte client approprié. De plus, la validation de la commande peut avoir pour résultat la création d’une écriture TVA et d’une écriture comptable pour le montant de la remise. La validation d’une écriture pour la remise dépend de la valeur du champ **Comptabilisation remises** de la page **Paramètres ventes**.

Pour chaque ligne commande vente, une écriture comptable article est créée dans la table **Écriture comptable article** (si les lignes vente contiennent des numéros des articles) ou une écriture comptable est créée dans la table **Écriture comptable** (si les lignes vente contiennent un compte général). En outre, les commandes vente sont toujours enregistrées dans les tables **En-tête expédition vente** et **En-tête facture vente**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Vous pouvez valider ou valider et envoyer. Si vous choisissez de valider et d’envoyer, un fichier PDF est généré que vous pouvez ensuite envoyer. Vous pouvez aussi choisir la fonction **Valider par lot**, qui vous permet de valider plusieurs commandes en même temps. Pour plus d’informations, voir [Valider plusieurs documents en même temps](ui-batch-posting.md).

## Affichage des écritures comptables

Lorsque la validation est terminée, les lignes vente validées sont supprimées de la commande. Un message vous indique lorsque la validation est terminée. Vous pouvez ensuite afficher les écritures validées dans les diverses pages qui contiennent les écritures validées, telles que **Écritures comptables client**, **Écritures comptables**, **Écritures comptables article**, **Expéditions vente enregistrées** et **Factures vente enregistrées**.  

Dans la plupart des cas, vous pouvez ouvrir des écritures comptables à partir de la fiche ou du document concerné. Par exemple, sur la page **Fiche client**, sélectionnez l’action **Écritures comptables**.

## Modification des écritures comptables

Vous pouvez modifier certains champs dans les documents d’achat validés, tels que le champ **N° de suivi du colis**. . Pour plus d’informations, voir [Modifier les documents validés](across-edit-posted-document.md). Pour les champs plus critiques qui concernent la piste d’audit, vous devez inverser ou annuler la validation. Pour plus d’informations, voir [Inversion d’une validation feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md).

## Voir aussi

[Ventes](sales-manage-sales.md)  
[Validation de plusieurs documents en même temps](ui-batch-posting.md)  
[Valider les documents validés](across-edit-posted-document.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md)  
[Recherche de pages et d’informations avec Tell Me](ui-search.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
