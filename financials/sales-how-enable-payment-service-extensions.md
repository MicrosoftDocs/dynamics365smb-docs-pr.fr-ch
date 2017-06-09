---
title: "Procédure : activer les paiements client via les services de paiement| Microsoft Docs"
description: Activez les services de paiement pour permettre aux clients de payer facilement leurs factures.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 769fd885e5c6070f8a4f6c9082900ea7f5f6ab8d
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-enable-customer-payments-through-payment-services"></a>Procédure : activer les paiements client via les services de paiement
Au lieu de collecter des paiements par l'intermédiaire de transferts bancaires ou de cartes de crédit, vos clients peuvent vous payer via leur compte avec des services de paiement, tels que PayPal ou WorldPay.  

Après avoir activé un service de paiement dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un lien est disponible vers le service sur les documents vente que vous envoyez par e-mail à vos clients. Les clients peuvent utiliser le lien pour accéder au service de paiement et payer la facture, directement à partir du document vente. Si vous ne souhaitez pas inclure le lien, par exemple, si un client paie en liquide, vous pouvez supprimer le service de paiement de la facture avant la validation.  

Les extensions PayPal Payments Standard et WorldPay Payments Standard sont installées dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et sont prêtes à être activées.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Pour activer un service de paiement dans [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Services de paiement**, puis sélectionnez le lien associé.  
2. Dans la fenêtre **Services de paiement**, sélectionnez l'action **Nouveau**.  
3. Sélectionnez le service de paiement, puis fermez la fenêtre.  
4. Dans la fenêtre **Services de paiement**, sélectionnez l'action **Configuration**.  
5. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Fermez la fenêtre.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Pour sélectionner un service de paiement dans une facture vente
1. Sur la page d'accueil, sélectionnez **Factures vente**.  
2. Ouvrez la facture vente que vous souhaitez payer en utilisant le service de paiement.  
3. Dans le champ **Service de paiement**, sélectionnez le service de paiement.  
  
    **Remarque** : le champ **Service de paiement** est uniquement disponible si vous avez activé le service de paiement.  

## <a name="see-also"></a>Voir aussi  
[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

