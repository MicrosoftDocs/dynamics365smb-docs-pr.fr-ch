---
title: Détails de conception- Structure de l'interface de validation | Microsoft Docs
description: Cette rubrique donne un aperçu des procédures globales dans la structure de l'interface de validation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1e80b905d96fc2204b61b03c0970257755b9e105
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787361"
---
# <a name="design-details-posting-interface-structure"></a>Détails de conception : Structure de l'interface de validation
Dans la structure de l'interface de validation [!INCLUDE[d365fin](includes/d365fin_md.md)], il y a plusieurs procédures globales utilisant la même structure :  
  
* Code de procédure d'appel RunWithCheck et RunWithoutCheck – interface de validation générique pour Gen. Jnl Line.  
* CustPostApplyCustLedgEntry – l'application du client de la validation, appelé à partir du codeunit 226 CustEntry-Appliquer les écritures validées.  
* VendPostApplyVendLedgEntry – validation de l'application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées.  
* UnapplyCustLedgEntry – validation de la désapplication de l'application du client, appelée à partir du codeunit 226 CustEntry-Appliquer les écritures validées  
* UnapplyVendLedgEntry – validation de la désapplication de l'application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées  
  
## <a name="see-also"></a>Voir aussi  
[Détails de conception : Structure du moteur de validation](design-details-posting-engine-structure.md)