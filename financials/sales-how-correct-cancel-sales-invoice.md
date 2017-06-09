---
title: "Procédure : corriger ou annuler des factures vente impayées| Microsoft Docs"
description: "Procédure : corriger ou annuler des factures vente impayées"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9289aeb9b44ec300646fbe6e6fdbf77e72cd7b08
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a>Procédure : corriger ou annuler des factures vente impayées
Vous pouvez corriger ou annuler une facture vente validée Cela est utile si vous faites une erreur ou si le client demande une modification.

**Remarque** : une fois la facture vente validée entièrement ou partiellement payée, vous ne pouvez pas la corriger ni l'annuler à partir de la facture vente elle-même. Au lieu de cela, vous devez créer manuellement un avoir vente pour annuler la vente et rembourser le client. Pour plus d'informations, reportez-vous à [Procédure : traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).

Dans la fenêtre **Facture vente enregistrée**, vous pouvez sélectionnez l'action **Corriger** ou **Annuler** pour exécuter les actions décrites dans le tableau suivant.

| Action | Description |
| --- | --- |
| **Corriger** |La facture vente validée est annulée. Une nouvelle facture vente avec les mêmes informations est créée. Vous pouvez créer une correction, puis continuer le processus de vente. La nouvelle facture vente a un numéro différent de celui de la facture vente initiale. Un avoir vente de correction est automatiquement créé et validé pour annuler la facture vente validée initiale. Sur la facture vente validée initiale, les cases Annulée et Payée sont cochées. |
| **Annuler** |La facture vente validée est annulée. Un avoir vente de correction est automatiquement créé et validé pour annuler la facture vente validée initiale. Sur la facture vente validée initiale, les cases Annulée et Payée sont cochées. |

Lorsque vous corrigez ou annulez une facture vente enregistrée, l'avoir vente de correction est appliqué à toutes les écritures comptables de la comptabilité et de l'inventaire créées lors de la validation de la facture vente initiale. Cette action contrepasse la facture vente validée dans vos enregistrements financiers et laisse l'avoir vente validé de correction pour votre piste d'audit.

## <a name="to-correct-a-posted-sales-invoice"></a>Pour corriger une facture vente validée
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Factures vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture vente validée à corriger.

    **Remarque** : si la case **Annulé** est cochée, vous ne pouvez pas corriger la facture vente validée car elle l'a déjà été, ou a été annulée.
3. Dans la fenêtre **Facture vente enregistrée** sélectionnez l'action **Corriger**.  
4. Une nouvelle facture vente avec les mêmes informations et dans laquelle vous pouvez apporter une correction est créée. La valeur du champ **Annulé** de la facture vente validée initiale devient **Oui**.

    Un avoir vente est automatiquement créé et validé pour annuler la facture vente validée initiale.
5. Sélectionnez l'action **Afficher un avoir correctif** pour afficher l'avoir vente validé qui annule la facture vente validée initiale.

## <a name="to-cancel-a-posted-sales-invoice"></a>Pour annuler une facture vente validée
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Factures vente enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture vente validée à annuler.

    **Remarque** : si la case **Annulé** est cochée, vous ne pouvez pas annuler la facture vente validée car elle l'a déjà été, ou a été corrigée.
3. Dans la fenêtre **Facture vente enregistrée** sélectionnez l'action **Annuler**.

    Un avoir vente est automatiquement créé et validé pour annuler la facture vente validée initiale. La valeur du champ **Annulé** de la facture vente validée initiale devient **Oui**.
4. Sélectionnez l'action **Afficher un avoir correctif** pour afficher l'avoir vente validé qui annule la facture vente validée initiale.

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Procédure : envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

