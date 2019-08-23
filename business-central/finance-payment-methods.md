---
title: Paramétrer des modes de règlement| Microsoft Docs
description: Vous utilisez des modes de règlement, par exemple, les chèques, le transfert bancaire, les espèces, ou Paypal, pour définir la façon dont les factures vente et achat sont payées.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 07/22/2019
ms.author: bholtorf
ms.openlocfilehash: 3f4741485a032dfef8b724ff4a18ed58c640778e
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796887"
---
# <a name="defining-payment-methods"></a>Définition des modes de règlement
Les modes de règlement définissent le mode de paiement que vous souhaitez voir vos clients utiliser, et comment vous souhaitez payer les fournisseurs. Le mode peut varier pour chaque client ou fournisseur. Les exemples de modes de règlement courants sont **virement**, **espèces**, **chèque** ou **dépôt**.

Vous pouvez affecter un mode de règlement aux clients et aux fournisseurs pour que le même mode soit toujours utilisé dans les documents achat et vente que vous créez pour eux. Si nécessaire, vous pouvez modifier le mode du document vente ou achat. Par exemple, si vous souhaitez payer une facture achat donnée en espèces plutôt que par le chèque. Cela ne modifie pas le mode de règlement par défaut affecté au fournisseur.

Les mêmes modes de règlement sont utilisés pour les documents vente et achat. Par exemple, un mode de règlement _espèces_ est utilisé lorsque vous effectuez des paiements et lorsque vous recevez les. [!INCLUDE[d365fin](includes/d365fin_md.md)] sait que lorsque vous créez une facture vente vous pensez recevoir le paiement, et inversement pour les factures achat.

Les avoirs pour les retours, cependant, sont des exceptions parce que le règlement s'effectue dans le sens inverse, de vous à votre client et de votre fournisseur à vous. Par conséquent, un mode de règlement par défaut n'est pas affecté aux avoirs. Il existe, cependant, une solution si vous avez spécifié des conditions de paiement pour le client ou le fournisseur. Bien que le champ **Calculer escompte sur les avoirs** ne soit pas prévu pour cela, si vous activez la case à cocher sur la page **Conditions de paiement**, un mode de règlement par défaut est ajouté lorsque vous créez un avoir.

## <a name="to-set-up-a-payment-method"></a>Pour configurer un mode de règlement
[!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des modes de règlement que les entreprises utilisent souvent. Vous pouvez cependant en ajouter autant que nécessaire.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modes de règlement**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Pour affecter un mode de règlement à un client ou fournisseur
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Client** ou **Fournisseur**, puis sélectionnez le lien associé.
2. Dans le champ **Code mode de règlement**, choisissez le mode à utiliser par défaut pour le client ou le fournisseur.

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
