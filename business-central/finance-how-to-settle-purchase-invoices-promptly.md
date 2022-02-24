---
title: Procédure de règlement rapide de factures achat | Microsoft Docs
description: Si vous devez payer le fournisseur en liquide ou par chèque, vous pouvez effectuer toutes les opérations nécessaires lorsque vous validez la facture.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ec5723088553141c1f6df55ba8bac3303ee4e2bd
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183275"
---
# <a name="settle-purchase-invoices-promptly"></a>Établir rapidement des factures achat
Si vous devez payer le fournisseur en liquide ou par chèque, vous pouvez valider le paiement lorsque vous validez la facture.  

### <a name="to-settle-purchase-invoices-promptly"></a>Pour établir rapidement des factures achat  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3.  Pour payer en liquide ou par virement bancaire, saisissez le numéro du compte général règlement ou du compte bancaire dans le champ **N° compte contrepartie**.  

> [!IMPORTANT]  
>  Les champs **Type compte contrepartie** et **N° compte contrepartie** ne font pas partie de la présentation standard de l'en-tête facture. Pour valider le paiement d'une facture, vous devez d'abord les insérer à l'aide des outils du Designer. Pour plus d'informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md). 

> [!NOTE]  
>  Si vous payez fréquemment les factures en liquide, il est conseillé de configurer un mode de règlement spécifique avec un compte contrepartie et de saisir ce mode dans le champ **Mode de règlement** sur la fiche fournisseur. Le programme insère automatiquement le numéro du compte contrepartie sur l'en-tête facture à chaque fois que vous créez une facture.  

## <a name="see-also"></a>Voir aussi  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
