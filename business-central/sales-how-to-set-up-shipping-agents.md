---
title: Procédure de configuration des transporteurs | Microsoft Docs
description: Vous pouvez définir un code pour chacun de vos transporteurs et saisir les informations qui les concernent.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2ea5d9fce1c10cf3c07c833efbe19b208f0c5a7c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788890"
---
# <a name="set-up-shipping-agents"></a>Configurer des transporteurs
Vous pouvez définir un code pour chacun de vos transporteurs et saisir les informations qui les concernent.  

Si vous saisissez une adresse Internet pour le transporteur, et que le transporteur fournit des prestations de traçabilité des colis sur Internet, vous pouvez utiliser la fonction de récépissé automatique. Pour plus d'informations, voir [Suivre des colis](sales-how-track-packages.md).

Lorsque vous configurez des transporteurs dans vos commandes vente, vous pouvez également spécifier les services proposés par chaque transporteur.  
Pour chaque transporteur, vous pouvez définir un nombre illimité de services et spécifier un délai d'expédition pour chaque service.  

Lorsque vous avez affecté une prestation transporteur à une ligne commande vente, le délai d'expédition de la prestation est inclus dans le calcul de la promesse de livraison, pour cette ligne. Pour plus d'informations, voir [Calculer des dates promesse livraison](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Pour configurer des transporteurs  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Transporteurs**, puis sélectionnez le lien associé.  
2.  Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Sélectionnez l'action **Prestations transporteur**.
4. Dans la fenêtre **Prestations transporteur**, renseignez les champs selon vos besoins.

> [!NOTE]  
>  Si vous supprimez le transporteur de la ligne commande, le code prestation transporteur est également supprimé de la ligne. La valeur des champs basée en partie sur la prestation transporteur est ensuite recalculée.  

## <a name="see-also"></a>Voir aussi
[Configurer des conditions de livraison](sales-how-set-up-shipment-methods.md)  
[Suivre des colis](sales-how-track-packages.md)    
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
