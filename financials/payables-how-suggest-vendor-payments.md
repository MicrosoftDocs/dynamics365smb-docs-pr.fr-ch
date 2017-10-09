---
title: Utilisez le traitement par lots Proposer paiements fournisseur| Microsoft Docs
description: "Vous pouvez spécifier les paramètres du paiement fournisseur pour obtenir des suggestions ou des propositions pour les paiements échus sous peu ou donnant lieu à une remise."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: 2085cc744c2ff3761937920cd893faab5a84dada
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-suggest-vendor-payments"></a>Procédure : proposer des paiements fournisseur
Dans la fenêtre **Feuille paiement**, vous pouvez utiliser le traitement par lots **Proposer paiements fournisseur** pour proposer des lignes paiement. Des lignes pour des éléments tels que les paiements échus à courte échéance ou les paiements pour lesquels un escompte est disponible, sont proposées en fonction de vos paramètres.

Pour bénéficier pleinement des lignes proposées, vous devez d'abord attribuer une priorité à vos fournisseurs. Pour plus d'informations, reportez-vous à [Procédure : octroyer une priorité à des fournisseurs](purchasing-how-prioritize-vendors.md).  

Les écritures fournisseur qui ne sont pas **En attente** ne sont pas incluses.  

> [!IMPORTANT]  
>   Si vous souhaitez profiter d'escomptes et que vous avez saisi un montant disponible, ce montant est d'abord utilisé pour :  

* Les écritures fournisseur échues et prioritaires, par ordre de priorité.  
* Les écritures fournisseur échues et non prioritaires.  
* Les écritures fournisseur ouvertes donnant lieu à un escompte, dans l'ordre des numéros des fournisseurs.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Pour utiliser la fonction Proposer paiements fournisseur
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.  
2. Ouvrez la feuille appropriée, puis sélectionnez l'action **Proposer paiements fournisseur**.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Cliquez sur le bouton **OK**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Pour insérer la date d'échéance comme date comptabilisation sur les lignes feuille paiement
Lorsque vous utilisez le traitement par lots **Proposer paiements fournisseur** pour créer des lignes de paiement pour vos fournisseurs, vous pouvez remplir deux champs spéciaux pour vous assurer que les lignes générées utilisent la date d'échéance pour calculer la date comptabilisation. Ces champs sont **Calculer la date comptabilisation à partir de la date d'échéance doc. lettrage** et **Décalage date d'échéance doc. lettrage**.  

> [!IMPORTANT]  
>   Vous ne pouvez pas utiliser le champ **Calculate Posting Date from Applies-to-Doc Due Date** avec le champ **Find Payment Discounts** ou le champ **Summarize per Vendor**. Si la date comptabilisation est basée sur la date d'échéance, des escomptes fournisseur risquent de ne pas être calculés correctement, parce que la date comptabilisation peut se trouver après la date d'escompte.  

De plus, si la date comptabilisation calculée se trouve dans le passé, la date de comptabilisation est déplacée à la date de travail, et un message d'avertissement s'affiche.  

Vous pouvez aussi créer manuellement des lignes de paiement à l'aide de la date d'échéance pour calculer la date comptabilisation. Une fois que vous avez appliqué les écritures comptables fournisseur, vous pouvez utiliser l'option **Calculer date comptabilisation** pour mettre à jour la date comptabilisation de la ligne feuille à la date d'échéance de la facture achat associée. Pour plus d'informations, reportez-vous à [Procédure : Lettrer les achats manuellement](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Si la facture achat est en retard, la date comptabilisation est définie sur la date de travail et la police de la ligne devient rouge.  

## <a name="see-also"></a>Voir aussi
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Effectuer des paiements](payables-make-payments.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

