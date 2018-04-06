---
title: "Corriger ou annuler une facture vente validée| Microsoft Docs"
description: "Décrit comment corriger, annuler, ou annuler une facture vente enregistrée et lettrer un avoir vente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e8e5a4762564d036ac8c0e7bdaf9e13b448d37f4
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Corriger ou annuler des factures vente impayées
Vous pouvez corriger ou annuler une facture vente validée. Cela est utile si vous faites une erreur ou si le client demande une modification.

> [!NOTE]  
>   Une fois la facture vente validée entièrement ou partiellement payée, vous ne pouvez pas la corriger ou l'annuler depuis elle-même. Au lieu de cela, vous devez créer manuellement un avoir vente pour annuler la vente et rembourser le client, géré de manière facultative avec un retour vente. Pour plus d'informations, reportez-vous à [Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).

Dans la fenêtre **Facture vente enregistrée**, vous pouvez sélectionnez l'action **Corriger** ou **Annuler** pour exécuter les actions décrites dans le tableau suivant.

| Action | Description |
| --- | --- |
| **Corriger** |La facture vente validée est annulée. Une nouvelle facture vente avec les mêmes informations est créée. Vous pouvez créer une correction, puis continuer le processus de vente. La nouvelle facture vente a un numéro différent de celui de la facture vente initiale. Un avoir vente de correction est automatiquement créé et validé pour annuler la facture vente validée initiale. Sur la facture vente validée initiale, les cases Annulée et Payée sont cochées. |
| **Annuler** |La facture vente validée est annulée. Un avoir vente de correction est automatiquement créé et validé pour annuler la facture vente validée initiale. Sur la facture vente validée initiale, les cases Annulée et Payée sont cochées. |

Lorsque vous corrigez ou annulez une facture vente enregistrée, l'avoir vente de correction est appliqué à toutes les écritures comptables de la comptabilité et de l'inventaire créées lors de la validation de la facture vente initiale. Cette action contrepasse la facture vente validée dans vos enregistrements financiers et laisse l'avoir vente validé de correction pour votre piste d'audit.

## <a name="to-correct-a-posted-sales-invoice"></a>Pour corriger une facture vente validée
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures vente enregistrées**, puis sélectionnez le lien connexe.  
2. Sélectionnez la facture vente validée à corriger.

    > [!NOTE]  
>   Si la case à cocher **Annulé** est activée, vous ne pouvez pas corriger la facture vente validée car elle l'a déjà été, ou a été annulée.
3. Dans la fenêtre **Facture vente enregistrée** sélectionnez l'action **Corriger**.  
4. Une nouvelle facture vente avec les mêmes informations et dans laquelle vous pouvez apporter une correction est créée. La valeur du champ **Annulé** de la facture vente validée initiale devient **Oui**.

    Un avoir vente est automatiquement créé et validé pour annuler la facture vente validée initiale.
5. Sélectionnez l'action **Afficher un avoir correctif** pour afficher l'avoir vente validé qui annule la facture vente validée initiale.

## <a name="to-cancel-a-posted-sales-invoice"></a>Pour annuler une facture vente validée
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures vente enregistrées**, puis sélectionnez le lien connexe.  
2. Sélectionnez la facture vente validée à annuler.

    > [!NOTE]  
>   Si la case à cocher **Annulé** est activée, vous ne pouvez pas annuler la facture vente validée car elle a déjà été annulée ou corrigée.
3. Dans la fenêtre **Facture vente enregistrée** sélectionnez l'action **Annuler**.

    Un avoir vente est automatiquement créé et validé pour annuler la facture vente validée initiale. La valeur du champ **Annulé** de la facture vente validée initiale devient **Oui**.
4. Sélectionnez l'action **Afficher un avoir correctif** pour afficher l'avoir vente validé qui annule la facture vente validée initiale.

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

