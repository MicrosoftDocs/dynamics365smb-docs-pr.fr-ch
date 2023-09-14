---
title: Corriger ou annuler une facture vente validée
description: 'Cette rubrique décrit comment corriger, annuler, ou annuler une facture vente enregistrée et lettrer un avoir vente.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.date: 06/23/2021
ms.author: bholtorf
---
# Corriger ou annuler des factures vente impayées

Vous pouvez corriger ou annuler une facture de vente impayée, à condition qu’elle n’ait pas été entièrement expédiée. Cela est utile si vous faites une erreur ou si le client demande une modification avant l’exécution de l’expédition. Dans tous les autres scénarios, nous vous recommandons de créer directement un avoir vente correctif. Pour plus d’informations, consultez [Créer un avoir vente à partir d’une facture vente enregistrée](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Une fois la facture vente validée entièrement ou partiellement payée, vous ne pouvez pas la corriger ou l’annuler depuis elle-même. Au lieu de cela, vous devez créer manuellement un avoir vente pour annuler la vente et rembourser le client, géré de manière facultative avec un retour vente. Pour plus d’informations, reportez-vous à [Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).

La différence entre l’annulation ou la correction d’une facture vente enregistrée qui n’a pas été payée ou expédiée est décrite dans le tableau suivant.

| Action | Description |
| --- | --- |
| **Annuler** |La facture vente validée est annulée. Un avoir vente de correction est automatiquement créé et validé pour annuler la facture vente validée initiale. Sur la facture vente validée enregistrée, les cases **Annulée** et **Payée** sont cochées. |
| **Corriger** |La facture vente validée est annulée. Une nouvelle facture vente avec les mêmes informations est créée, sauf si la commande client enregistrée a été validée à partir d’une commande client. Dans ce cas, nous vous suggérons d’annuler la facture vente enregistrée à la place, puis d’effectuer la correction et de poursuivre le processus de vente à partir de la commande client d’origine. <br/><br/>La nouvelle facture vente a un numéro différent de celui de la facture vente initiale. Un avoir vente de correction est automatiquement créé et validé pour annuler la facture vente validée initiale. Sur la facture vente validée enregistrée, les cases **Annulée** et **Payée** sont cochées. |

Lorsque vous corrigez ou annulez une facture vente enregistrée, l’avoir vente de correction est appliqué à toutes les écritures comptables de la comptabilité et de l’inventaire créées lors de la validation de la facture vente initiale. Cette action contrepasse la facture vente validée dans vos enregistrements financiers et laisse l’avoir vente validé de correction pour votre piste d’audit.  

> [!TIP]
> Si vous avez enregistré une facture de prépaiement pour une facture vente que vous corrigez ou annulez ensuite, vous devez également corriger ou annuler le prépaiement. Pour plus d’informations, voir [Corriger des acomptes](finance-how-to-correct-prepayments.md).

## Pour annuler une facture vente validée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture vente validée à annuler.

    > [!NOTE]  
    >   Si la case à cocher **Annulé** est activée, vous ne pouvez pas annuler la facture vente validée car elle a déjà été annulée ou corrigée.
3. Sur la page **Facture vente enregistrée** sélectionnez l’action **Annuler**.

    Un avoir vente est automatiquement créé et validé pour annuler la facture vente validée initiale. La valeur du champ **Annulé** de la facture vente validée initiale devient **Oui**.
4. Sélectionnez l’action **Afficher un avoir correctif** pour afficher l’avoir vente validé qui annule la facture vente validée initiale.

### Validation partielle de facture également prise en charge

Si l’annulation est liée à une validation de facture partielle, la ligne de commande vente d’origine est mise à jour pour refléter la quantité facturée annulée. Les champs **Qté à facturer** et **Qté facturée** de la ligne de commande vente associée sont réinitialisés aux valeurs avant l’enregistrement partiel.

## Pour corriger une facture vente validée

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture vente validée à corriger.

    > [!NOTE]  
    >   Si la case à cocher **Annulé** est activée, vous ne pouvez pas corriger la facture vente validée car elle l’a déjà été, ou a été annulée.
3. Sur la page **Facture vente enregistrée** sélectionnez l’action **Corriger**.  

    > [!NOTE]
    > Si la facture vente a été enregistrée à partir d’une commande vente, nous vous recommandons d’*annuler* cette facture vente, puis de traiter la correction à partir de la commande client d’origine. Si la commande client d’origine a été supprimée, par exemple si elle a été entièrement expédiée, vous pouvez créer une nouvelle commande client en utilisant l’action **Copier le document**. Pour plus d’informations, consultez [Créer un avoir vente en copiant une facture vente enregistrée](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Une nouvelle facture vente avec les mêmes informations et dans laquelle vous pouvez apporter une correction est créée. La valeur du champ **Annulé** de la facture vente validée initiale devient **Oui**.

    Un avoir vente est automatiquement créé et validé pour annuler la facture vente validée initiale.
5. Sélectionnez l’action **Afficher un avoir correctif** pour afficher l’avoir vente validé qui annule la facture vente validée initiale.

## Voir la [formation Microsoft](/training/modules/ship-invoice-items-dynamics-365-business-central/) associée

## Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
