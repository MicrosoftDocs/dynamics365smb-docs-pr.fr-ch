---
title: Activer les paiements client via les services de paiement
description: Activez les services de paiement pour permettre aux clients de payer facilement leurs factures.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.search.forms: 1060, 1061, 1062
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 8216c4f34cf63b1dcc9a501747ae8738309ba511
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059871"
---
# <a name="enable-customer-payments-through-payment-services"></a>Activer les paiements client via les services de paiement
Au lieu de collecter des paiements par l’intermédiaire de transferts bancaires ou de cartes de crédit, vos clients peuvent vous payer via leur compte avec des services de paiement, tels que PayPal ou WorldPay.  

Après avoir activé un service de paiement dans [!INCLUDE[prod_short](includes/prod_short.md)], un lien est disponible vers le service sur les documents vente que vous envoyez par e-mail à vos clients. Les clients peuvent utiliser le lien pour accéder au service de paiement et payer la facture, directement à partir du document vente. Si vous ne souhaitez pas inclure le lien, par exemple, si un client paie en liquide, vous pouvez supprimer le service de paiement de la facture avant la validation.  

Les extensions PayPal Payments Standard et WorldPay Payments Standard sont installées dans [!INCLUDE[prod_short](includes/prod_short.md)] et sont prêtes à être activées.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Pour activer un service de paiement dans [!INCLUDE[prod_short](includes/prod_short.md)]
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services de paiement**, puis sélectionnez le lien associé.  
2. Sur la page **Services de paiement**, sélectionnez l’action **Nouveau**.  
3. Sélectionnez le service de paiement, puis fermez la page.  
4. Sur la page **Services de paiement**, sélectionnez l’action **Configuration**.  
5. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Fermez la page.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Pour sélectionner un service de paiement dans une facture vente
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente**, puis sélectionnez le lien associé.  
2. Ouvrez la facture vente que vous souhaitez payer en utilisant le service de paiement.  
3. Dans le champ **Service de paiement**, sélectionnez le service de paiement.  

    > [!NOTE]  
    > Le champ **Service de paiement** est uniquement disponible si vous avez activé le service de paiement.  

## <a name="see-also"></a>Voir aussi  
[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide d’extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]