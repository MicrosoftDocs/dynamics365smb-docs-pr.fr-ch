---
title: "Créer une demande de prix pour demander une offre à votre fournisseur | Microsoft Docs"
description: "Décrit comment créer une offre vente offrent ou un document de demande de proposition pour enregistrer votre offre à un client pour vendre des produits dans certaines conditions."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: df1793d811dea11c01ff5e7d90a9f52b9e987c13
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-request-quotes"></a>Procédure : Demander des devis
Vous pouvez utiliser une demande de prix en tant que phase préliminaire d'une commande achat, et convertir cette commande en facture achat ou en commande.


## <a name="to-create-a-purchase-quote"></a>Pour créer une demande de prix
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Demandes de prix**, puis sélectionnez le lien connexe.
2. Créez un document, de la même manière que vous passez une commande achat. Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Pour convertir une demande de prix en commande achat
Lorsque vous avez accepté le devis du fournisseur, vous pouvez le convertir en facture achat ou en commande pour procéder à l'achat.

1. Ouvrez une demande de prix est prête à être convertie, puis sélectionnez l'action **Créer commande**.

La demande de prix est supprimée de la base de données. Une facture achat ou une commande achat basée sur les informations de la demande de prix et dans laquelle vous pouvez traiter l'achat est créée. Dans le champ **N° devis** de la facture achat ou de la commande achat, vous pouvez visualiser le numéro de la demande de prix à partir de laquelle elle a été réalisée.

## <a name="see-also"></a>Voir aussi
[Achats](purchasing-manage-purchasing.md)  
[Définition des achats](purchasing-setup-purchasing.md)  
[Procédure : envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

