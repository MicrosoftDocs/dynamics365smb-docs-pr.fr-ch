---
title: Détails de conception- Structure de l'interface de validation | Microsoft Docs
description: Cette rubrique donne un aperçu des procédures globales dans la structure de l'interface de validation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5905a16341dc487aaf624810d691ac4628ac2e30
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239536"
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