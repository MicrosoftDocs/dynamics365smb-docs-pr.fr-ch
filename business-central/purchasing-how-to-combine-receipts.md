---
title: Procédure de regroupement des réceptions | Microsoft Docs
description: Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction Regroupement des réceptions.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 991c244d9e9233067903cfe21fbabcb732293490
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387714"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Regroupement de bons de réception sur une seule facture

Si vous voulez facturer plusieurs réceptions achat en une fois, vous pouvez utiliser la fonction **Regroupement des réceptions**.  

Avant de pouvoir regrouper des réceptions achat, plusieurs réceptions achat du même fournisseur doivent être validées dans la même devise. En d’autres termes, vous devez avoir renseigné au moins deux commandes achat et les avoir validées comme reçues, mais non facturées.  

Lorsque des réceptions achat sont regroupées sur une facture et validées, une facture achat enregistrée est créée pour les lignes facturées. Le champ **Quantité facturée** de la commande achat d’origine, ou de la commande ouverte achat, est mis à jour en fonction de la quantité facturée. Comme ce document d’achat d’origine n’est toutefois pas supprimé, même s’il a été entièrement reçu et facturé, vous devez supprimer le document d’achat.  

> [!NOTE]
> La facture achat qui en résulte ne peut pas être corrigée ou annulée ultérieurement. Si vous souhaitez modifier une facture achat ainsi créée, vous devez utiliser des avoirs achat. Pour plus d’informations, voir [Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Pour regrouper des réceptions

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).  
3. Dans le raccourci **Lignes**, sélectionnez l’action **Extraire lignes réception**.  
4. Sélectionnez plusieurs lignes réception à inclure dans la facture.  

    Si une ligne réception incorrecte a été sélectionnée ou que vous souhaitez recommencer, il vous suffit de supprimer les lignes de la facture achat et d’utiliser à nouveau la fonction **Extraire lignes réception**.  
5. Pour valider la facture, sélectionnez l’action **Valider**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Pour supprimer des commandes achat ouvertes après la validation de reçus regroupés

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les commandes achat facturées**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Cliquez sur le bouton **OK**.  

Vous pouvez également supprimer chacune des commandes manuellement.

Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes achat.

## <a name="see-also"></a>Voir aussi

[Achats](purchasing-manage-purchasing.md)  
[Corriger ou annuler des factures achat impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]