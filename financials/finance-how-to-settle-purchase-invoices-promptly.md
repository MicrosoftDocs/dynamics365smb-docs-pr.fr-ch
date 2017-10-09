---
title: "Procédure de règlement rapide de factures achat | Microsoft Docs"
description: "Si vous devez payer le fournisseur en liquide ou par chèque, vous pouvez effectuer toutes les opérations nécessaires lorsque vous validez la facture."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ab72dbc70405323e5dcf7aafb1120f63bd15246c
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-settle-purchase-invoices-promptly"></a>Procédure : établir rapidement des factures achat
Si vous devez payer le fournisseur en liquide ou par chèque, vous pouvez valider le paiement lorsque vous validez la facture.  
  
### <a name="to-settle-purchase-invoices-promptly"></a>Pour établir rapidement des factures achat  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures achat**, puis sélectionnez le lien connexe.  
2. Sous l'onglet **Accueil**, choisissez **Nouveau**.  
3.  Pour payer en liquide ou par virement bancaire, saisissez le numéro du compte général règlement ou du compte bancaire dans le champ **N° compte contrepartie**.  
  
> [!IMPORTANT]  
>  Les champs **Type compte contrepartie** et **N° compte contrepartie** ne font pas partie de la présentation standard de l'en-tête facture. Pour valider le paiement d'une facture, vous devez d'abord les insérer à l'aide des outils du Designer.  
  
> [!NOTE]  
>  Si vous payez fréquemment les factures en liquide, il est conseillé de configurer un mode de règlement spécifique avec un compte contrepartie et de saisir ce mode dans le champ **Mode de règlement** sur la fiche fournisseur. Le programme insère automatiquement le numéro du compte contrepartie sur l'en-tête facture à chaque fois que vous créez une facture.  
  
## <a name="see-also"></a>Voir aussi  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
