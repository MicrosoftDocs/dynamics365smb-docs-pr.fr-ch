---
title: Détails de conception- Structure de l’interface de validation | Microsoft Docs
description: Cette rubrique donne un aperçu des procédures globales dans la structure de l’interface de validation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 529a0e42d814f0754e62fcc4b93b793d44b8daa7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215843"
---
# <a name="design-details-posting-interface-structure"></a>Détails de conception : Structure de l’interface de validation
Dans la structure de l’interface de validation [!INCLUDE[prod_short](includes/prod_short.md)], il y a plusieurs procédures globales utilisant la même structure :  
  
* Code de procédure d’appel RunWithCheck et RunWithoutCheck – interface de validation générique pour Gen. Jnl Line.  
* CustPostApplyCustLedgEntry – l’application du client de la validation, appelé à partir du codeunit 226 CustEntry-Appliquer les écritures validées.  
* VendPostApplyVendLedgEntry – validation de l’application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées.  
* UnapplyCustLedgEntry – validation de la désapplication de l’application du client, appelée à partir du codeunit 226 CustEntry-Appliquer les écritures validées  
* UnapplyVendLedgEntry – validation de la désapplication de l’application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées  
  
## <a name="see-also"></a>Voir aussi  
[Détails de conception : Structure du moteur de validation](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]