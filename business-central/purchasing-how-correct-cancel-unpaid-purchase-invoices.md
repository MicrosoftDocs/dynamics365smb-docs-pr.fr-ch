---
title: "Corriger ou annuler des factures achat impayées | Microsoft Docs"
description: "Explique comment corriger ou annuler une facture achat validée et créer automatiquement un avoir achat."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2ed3520b3724f9703fca128a2d20c28183795a93
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Corriger ou annuler des factures achat impayées
Vous pouvez corriger ou annuler une facture achat validée. Cela est utile si vous souhaitez corriger une erreur de saisie, ou si vous souhaitez modifier l'achat assez tôt dans le processus de commande.

Si vous avez déjà payé des produits sur la facture achat validée, vous ne pouvez pas la corriger ni l'annuler à partir de la facture achat validée elle-même. Au lieu de cela, vous devez créer manuellement un avoir achat pour contrepasser l'achat, éventuellement géré à l'aide d'un retour achat. Pour plus d'informations, reportez-vous à [Traiter les retours ou annulations d'achats](purchasing-how-process-purchase-returns-cancellations.md).

Dans la fenêtre **Facture achat enregistrée**, vous pouvez cliquer sur le bouton **Corriger** ou **Annuler**. Lorsque vous corrigez ou annulez une facture achat enregistrée, l'avoir achat de correction est appliqué à toutes les écritures comptables de la comptabilité et de l'inventaire créées lors de la validation de la facture achat initiale. Cette action contrepasse la facture achat validée dans vos enregistrements financiers et laisse l'avoir achat validé de correction pour votre piste d'audit. L'utilisation des boutons **Corriger** et **Annuler** est décrite ci-après.

## <a name="to-correct-a-posted-purchase-invoice"></a>Pour corriger une facture achat validée
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture achat validée à corriger.  

    > [!NOTE]  
    >   Si la case à cocher **Annulé** est activée, vous ne pouvez pas corriger la facture achat validée car elle l'a déjà été, ou a été annulée.
3. Dans la fenêtre **Facture achat enregistrée** sélectionnez **Corriger**.

    Une nouvelle facture achat avec les mêmes informations et dans laquelle vous pouvez apporter une correction est créée. Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md). La valeur du champ **Annulé** de la facture achat validée initiale devient **Oui**.

    Un avoir achat est automatiquement créé et validé pour annuler la facture achat validée initiale.
4. Sélectionnez **Afficher un avoir correctif** pour afficher l'avoir achat validé qui annule la facture achat validée initiale.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Pour annuler une facture achat validée
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez la facture achat validée à annuler.

    > [!NOTE]  
    >   Si la case à cocher **Annulé** est activée, vous ne pouvez pas annuler la facture achat validée car elle l'a déjà été, ou a été corrigée.
3. Dans la fenêtre **Facture achat enregistrée** sélectionnez **Annuler**.

    Un avoir achat est automatiquement créé et validé pour annuler la facture achat validée initiale. La valeur du champ **Annulé** de la facture achat validée initiale devient **Oui**.
4. Sélectionnez **Afficher un avoir correctif** pour afficher l'avoir achat validé qui annule la facture achat validée initiale.

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Enregistrer des achats](purchasing-how-record-purchases.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

