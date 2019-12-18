---
title: 'Procédure : Regroupement de bons de livraison sur une seule facture | Microsoft Docs'
description: Si vous souhaitez facturer plusieurs bons de livraison à la fois, vous pouvez utiliser la fonction de regroupement des bons de livraison.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: febf38da727cb7f41fa6d6c4bacf36877a8df1f3
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882925"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Regroupement de bons de livraison sur une seule facture
Si vous souhaitez facturer plusieurs bons de livraison à la fois, vous pouvez utiliser la fonction de regroupement des bons de livraison.  

 Pour créer un regroupement de bons de livraison, plusieurs bons de livraison vente doivent avoir été validés pour le même client dans la même devise. Autrement dit, vous devez avoir renseigné au moins deux commandes vente et les avoir validées comme étant expédiées, mais pas facturées. Vous devez activer la case à cocher **Regrouper les B.L**. sur le raccourci **Expédition** de la fiche **client** pour utiliser la fonctionnalité.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Regrouper manuellement les expéditions sur une seule facture  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures vente**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**. Pour plus d'informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).
3. Dans le champ **N° donneur d'ordre** entrez le client facturé pour les articles expédiés.  
4. Dans le raccourci **Lignes**, sélectionnez l'action **Extraire lignes expédition**.  
5. Sélectionnez la ligne expédition que vous voulez inclure dans la facture :  

    - Pour insérer toutes les lignes, sélectionnez-les toutes et sélectionnez le bouton **OK**.  
    - Pour insérer des lignes spécifiques, sélectionnez-les et sélectionnez le bouton **OK**. Vous pouvez utiliser la touche Ctrl pour sélectionner plusieurs lignes qui ne sont pas séquentielles.  

    Si une ligne expédition incorrecte a été sélectionnée ou si vous voulez recommencer, supprimez simplement les lignes de la facture, puis exécutez de nouveau la fonction **Extraire lignes expédition**.  
7. Pour valider la facture, sélectionnez l'action **Valider**.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Regrouper automatiquement les expéditions sur une seule facture  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Regrouper les B.L.**, puis sélectionnez le lien associé. La page de sélection du traitement par lots s'ouvre.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Cochez la case **Validation des factures**.  
4.  Cliquez sur le bouton **OK**.  

> [!NOTE]  
>  Vous devez valider manuellement les avoirs si la case à cocher **Valider avoirs** n'a pas été activée pour le traitement par lots.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Pour supprimer des commandes vente ouvertes après la validation des expéditions regroupées 
Lorsque des bons de livraison sont regroupés sur une facture et validés, une Facture vente enregistrée est créée pour les lignes facturées. Le champ **Quantité facturée** de la commande ouverte vente ou de la commande vente d'origine est mis à jour sur la base de la quantité facturée.  

Lorsque vous facturez des livraisons de cette manière, les commandes à partir desquelles les livraisons ont été validées continuent à exister, même si elles ont été entièrement validées et facturées.   

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer cdes vente facturées**, puis sélectionnez le lien.  
2. Dans le champ de filtre **N°**, les commandes vente à supprimer.  
3. Cliquez sur le bouton **OK**.  

Il est également possible de supprimer chacune des commandes vente manuellement.  

Répétez les étapes 1 à 3 pour tous les autres documents affectés, comme des commandes ouvertes vente.

## <a name="see-also"></a>Voir aussi  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
