---
title: Détails de conception - Demande et approvisionnement | Microsoft Docs
description: Le mot demande désigne tout sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication. En outre, l'application permet davantage de types techniques de demande, tels que le stock négatif et les retours achat.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8ef7211aa812b1faf784ecf36f1873a6e2dcc6fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303654"
---
# <a name="design-details-demand-and-supply"></a>Détails de conception : demande et approvisionnement
Le mot demande désigne tout sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication. En outre, l'application permet davantage de types techniques de demande, tels que le stock négatif et les retours achat.  

 Approvisionnement est le terme courant utilisé pour désigner toute sorte de quantité positive ou d'entrée, telle qu'un stock, des achats, un assemblage, une production ou des transferts d'enlogement. De plus, un retour vente peut également représenter un approvisionnement.  

 Pour trier les nombreuses sources de demande et d'approvisionnement, le système de planification les organise sur deux chronologies appelées profils de stock. Un profil contient des événements de demande, ainsi l'autre contient les événements d'approvisionnement correspondants. Chaque événement représente une entité réseau de commande, par exemple une ligne commande vente, une écriture comptable article ou une ligne O.F.  

 Lorsque les profils de stock sont chargés, les différents ensembles demande-approvisionnement sont équilibrés pour produire un plan d'approvisionnement répondant aux objectifs répertoriés.  

 Les paramètres de planification et les niveaux de stock sont d'autres types de demande et d'approvisionnement respectivement, qui subissent un équilibrage intégré pour réapprovisionner les articles en stock. Pour plus d'informations, voir [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md).  

## <a name="see-also"></a>Voir aussi  
 [Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
 [Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)   
 [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
