---
title: "Lettrer des écritures dans des devises différentes| Microsoft Docs"
description: "Vous pouvez lettrer des écritures comptables dans différentes devises si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d98fdf358e387be1d53b188cc05c57108e8592b8
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Activer le lettrage d'écritures comptables client en devises différentes
Si vous achetez des produits auprès d'un fournisseur dans une devise et que vous payez ces produits dans une autre devise, vous pouvez lettrer le paiement avec l'achat.

De même, si vous effectuez une vente à un client dans une devise et recevez le règlement dans une autre devise, vous pouvez lettrer le règlement avec la facture vente.

La procédure suivante indique comment configurer cela pour les écritures comptables fournisseur dans la fenêtre **Paramètres achats**. La configuration est semblable à celle des écritures comptables client dans la fenêtre **Paramètres ventes**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Pour activer le lettrage d'écritures comptables fournisseur en devises différentes
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.
2. Dans le champ **Lettrage entre devises**, sélectionnez l'une des options suivantes.

| Option | Description |
| --- | --- |
| Aucun |Le lettrage entre devises n'est pas autorisé. |
| Devises U.M.E. |Le lettrage entre devises UME est autorisé. |
| Tous |Lettrage autorisé entre toutes les devises. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Pour configurer des comptes généraux afin d'autoriser les différences d'arrondi des devises  
Si vous lettrez des écritures dans différentes devises, vous devez configurer les comptes généraux sur lesquels valider les différences d'arrondi.  

> [!NOTE]  
>  Vous devez configurer les comptes généraux avant de terminer la tâche. Pour plus d'informations, voir [Description des écritures comptables et du plan comptable](finance-general-ledger.md).

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Groupes compta. client**, puis choisissez le lien associé.  
2. Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d'arrondi.  
3. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Groupes compta. fournisseur**, puis sélectionnez le lien connexe.  
4. Dans les champs **Cpte arr. lettr. dev. débit** et **Cpte arr. lettr. dev. crédit**, saisissez les comptes généraux correspondants pour valider les différences d'arrondi.  

## <a name="see-also"></a>Voir aussi
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Gestion des comptes client](receivables-manage-receivables.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

