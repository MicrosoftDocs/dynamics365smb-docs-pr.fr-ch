---
title: 'Procédure : Regroupement de bons de livraison sur une seule facture | Microsoft Docs'
description: Si vous souhaitez facturer plusieurs bons de livraison à la fois, vous pouvez utiliser la fonction de regroupement des bons de livraison.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2936e819ba50adde6df021cc0dc2694367c29fc9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778512"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Regroupement de bons de livraison sur une seule facture
Si vous souhaitez facturer plusieurs bons de livraison à la fois, vous pouvez utiliser la fonction de regroupement des bons de livraison.  

Pour créer un regroupement de bons de livraison, plusieurs bons de livraison vente doivent avoir été validés pour le même client dans la même devise. Autrement dit, vous devez avoir créé au moins deux commandes vente et les avoir validées comme étant expédiées, mais pas facturées. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Regrouper manuellement les expéditions sur une seule facture  
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**. Pour plus d’informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).
3. Dans le champ **N° donneur d’ordre** entrez le client facturé pour les articles expédiés.  
4. Dans le raccourci **Lignes**, sélectionnez l’action **Extraire lignes expédition**.  
5. Sélectionnez la ligne expédition que vous voulez inclure dans la facture :  

    - Pour insérer toutes les lignes, sélectionnez-les toutes et sélectionnez le bouton **OK**.  
    - Pour insérer des lignes spécifiques, sélectionnez-les et sélectionnez le bouton **OK**. Vous pouvez utiliser la touche Ctrl pour sélectionner plusieurs lignes qui ne sont pas séquentielles.  

    Si une ligne expédition incorrecte a été sélectionnée ou si vous voulez recommencer, supprimez simplement les lignes de la facture, puis exécutez de nouveau la fonction **Extraire lignes expédition**.  
7. Pour valider la facture, sélectionnez l’action **Valider**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Regrouper automatiquement les expéditions sur une seule facture  
[!INCLUDE[prod_short](includes/prod_short.md)] ne sélectionne que les commandes vente où **Regrouper les B.L.** est coché. 

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Regrouper les B.L.**, puis sélectionnez le lien associé. La page de sélection du traitement par lots s’ouvre.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Cochez la case **Validation des factures**.  
4. Cliquez sur le bouton **OK**.  

> [!NOTE]  
>  Vous devez valider manuellement les avoirs si la case à cocher **Valider avoirs** n’a pas été activée pour le traitement par lots.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Pour supprimer des commandes vente ouvertes après la validation des expéditions regroupées 
Lorsque des bons de livraison sont regroupés sur une facture et validés, une Facture vente enregistrée est créée pour les lignes facturées. Le champ **Quantité facturée** de la commande ouverte vente ou de la commande vente d’origine est mis à jour sur la base de la quantité facturée.  

Lorsque vous facturez des livraisons de cette manière, les commandes à partir desquelles les livraisons ont été validées continuent à exister, même si elles ont été entièrement validées et facturées.   

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer cdes vente facturées**, puis sélectionnez le lien.  
2. Dans le champ de filtre **N°**, les commandes vente à supprimer.  
3. Cliquez sur le bouton **OK**.  

Il est également possible de supprimer chacune des commandes vente manuellement.  

Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes vente.

## <a name="see-also"></a>Voir aussi  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]