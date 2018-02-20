---
title: "Configurer et utiliser des lignes standard pour les ventes et achats récurrents| Microsoft"
description: "Vous pouvez définir des lignes vente et des lignes achat que vous utilisez fréquemment et les insérer dans des documents achat et vente pour remplir rapidement les lignes avec des informations standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7c5820db4d8aa65ddeddfd5ee27f0a7e89100abf
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Créer des lignes ventes et achat récurrentes
Si vous devez souvent créer des lignes ventes et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes.  

La procédure suivante indique comment utiliser des lignes ventes standard. Elle est similaire pour les lignes achat standard.  

## <a name="to-set-up-standard-sales-lines"></a>Configurer des lignes ventes standard  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Codes vente standard**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Lignes vente standard**, cliquez sur l'action **Nouveau**.  
3. Sur le raccourci **Général**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Dans le raccourci **Lignes**, renseignez les champs pour préparer les lignes ventes qui répercutent les lignes standard que vous prévoyez d'utiliser comme lignes récurrentes sur les documents ventes.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Pour insérer des lignes vente standard dans une facture vente
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures**, puis sélectionnez le lien connexe.
2. Ouvrez la facture vente que vous souhaitez pour insérer une ou plusieurs lignes ventes standard.
3. Choisissez l'action **Extraire les lignes vente récurrentes**.
4. Dans la fenêtre **Lignes vente récurrentes**, cliquez sur le bouton de recherche du champ **Code**, puis sélectionnez un ensemble de lignes vente standard.
5. Choisissez le bouton **OK** pour insérer les lignes vente standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Pour créer plusieurs factures vente basées sur des lignes vente standard
Vous pouvez utiliser le traitement par lots **Créer des factures vente récurrentes** pour créer des factures vente en fonction des lignes vente standard qui sont affectées aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans le code vente standard.

Dans la fenêtre **Lignes vente récurrentes**, vous pouvez également spécifier un mode et un mandat de prélèvement. Les factures vente qui sont créées avec le traitement par lots **Créer des factures vente récurrentes** incluront ensuite les informations requises pour collecter le paiement pour les factures vente par prélèvement automatique SEPA. Pour plus d'informations, voir [Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Créer des factures vente récurrentes**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Créer des factures vente récurrentes**, renseignez les champs selon les besoins.
3. Dans le champ **Code**, entrez le code des lignes vente standard associées à un client pour lequel vous souhaitez créer des factures vente.
4. Cliquez sur le bouton **OK**.

Les factures vente sont créées pour les clients ayant le code vente client standard spécifié, et toute information de prélèvement automatique spécifiée, pour la validation à la date spécifiée.

## <a name="see-also"></a>Voir aussi  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

