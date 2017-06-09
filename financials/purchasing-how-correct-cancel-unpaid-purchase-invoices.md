---
title: "Procédure : corriger ou annuler des factures achat impayées| Microsoft Docs"
description: "Procédure : corriger ou annuler des factures achat impayées"
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
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Procédure : corriger ou annuler des factures achat impayées
Vous pouvez corriger ou annuler une facture achat validée Cela est utile si vous souhaitez corriger une erreur de saisie, ou si vous souhaitez modifier l'achat assez tôt dans le processus de commande.

Si vous avez déjà payé des produits sur la facture achat validée, vous ne pouvez pas la corriger ni l'annuler à partir de la facture achat validée elle-même. Au lieu de cela, vous devez créer manuellement un avoir achat pour inverser l'achat. Pour plus d'informations, reportez-vous à [Procédure : traiter les retours ou annulations d'achats](purchasing-how-process-purchase-returns-cancellations.md).

Dans la fenêtre **Facture achat enregistrée**, vous pouvez cliquer sur le bouton **Corriger** ou **Annuler**. Lorsque vous corrigez ou annulez une facture achat enregistrée, l'avoir achat de correction est appliqué à toutes les écritures comptables de la comptabilité et de l'inventaire créées lors de la validation de la facture achat initiale. Cette action contrepasse la facture achat validée dans vos enregistrements financiers et laisse l'avoir achat validé de correction pour votre piste d'audit. L'utilisation des boutons **Corriger** et **Annuler** est décrite ci-après.

## <a name="to-correct-a-posted-purchase-invoice"></a>Pour corriger une facture achat validée
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Factures achat enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture achat validée à corriger.  

    **Remarque** : si la case **Annulé** est cochée, vous ne pouvez pas corriger la facture achat validée car elle l'a déjà été, ou a été annulée.
3. Dans la fenêtre **Facture achat enregistrée** sélectionnez **Corriger**.

    Une nouvelle facture achat avec les mêmes informations et dans laquelle vous pouvez apporter une correction est créée. Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md). La valeur du champ **Annulé** de la facture achat validée initiale devient **Oui**.

    Un avoir achat est automatiquement créé et validé pour annuler la facture achat validée initiale.
4. Sélectionnez **Afficher un avoir correctif** pour afficher l'avoir achat validé qui annule la facture achat validée initiale.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Pour annuler une facture achat validée
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Factures achat enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture achat validée à annuler.

    **Remarque** : si la case **Annulé** est cochée, vous ne pouvez pas annuler la facture achat validée car elle l'a déjà été, ou a été corrigée.
3. Dans la fenêtre **Facture achat enregistrée** sélectionnez **Annuler**.

    Un avoir achat est automatiquement créé et validé pour annuler la facture achat validée initiale. La valeur du champ **Annulé** de la facture achat validée initiale devient **Oui**.
4. Sélectionnez **Afficher un avoir correctif** pour afficher l'avoir achat validé qui annule la facture achat validée initiale.

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Procédure : enregistrer des achats](purchasing-how-record-purchases.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

