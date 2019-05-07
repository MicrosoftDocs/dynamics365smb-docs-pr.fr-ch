---
title: Détails de conception - Traçabilité | Microsoft Docs
description: Cette rubrique donne un aperçu des détails de conception pour la traçabilité.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 344c3162ce7f84aa61f9e572f3245d9515cbd81b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "925222"
---
# <a name="design-details-item-tracking"></a>Détails de conception : traçabilité
Étant donné que le flux de biens dans la chaîne d'approvisionnement moderne devient de plus en plus complexe, la capacité à effectuer le suivi des articles est de plus en plus importante pour les sociétés concernées. La surveillance du flux de transaction d'un article est une obligation légale dans le secteur de l'approvisionnement médical et chimique, mais d'autres sociétés peuvent souhaiter contrôler les produits avec des garanties ou des dates d'expiration pour des raisons de service client.  

Un système de traçabilité doit permettre à une société de traiter facilement les numéros de série et les numéros de lot, en considérant chaque marchandise comme étant unique : date et lieu de réception, lieu de stockage, date et lieu de vente. [!INCLUDE[d365fin](includes/d365fin_md.md)] a progressivement étendu sa prise en charge de ce besoin de l'entreprise et fournit actuellement des fonctionnalités à l'échelle de l'application, ainsi qu'une base solide pour le développement d'extensions.  

## <a name="in-this-section"></a>Dans cette section  
[Détails de conception : création de traçabilité](design-details-item-tracking-design.md)  
[Détails de conception : structure de validation de traçabilité](design-details-item-tracking-posting-structure.md)  
[Détails de conception : comparaison entre écritures traçabilité actives et historiques](design-details-active-versus-historic-item-tracking-entries.md)  
[Détails de conception : page Lignes traçabilité](design-details-item-tracking-lines-window.md)  
[Détails de conception : disponibilité traçabilité](design-details-item-tracking-availability.md)  
[Détails de conception : traçabilité et planification d'article](design-details-item-tracking-and-planning.md)  
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Détails de conception : traçabilité dans l'entrepôt](design-details-item-tracking-in-the-warehouse.md)
