---
title: Affichage et édition dans Excel depuis Business Central | Microsoft Docs
description: En savoir plus sur la manière dont vous pouvez ouvrir les pages dans Microsoft Excel à partir de Business Central pour une meilleure analyse de données.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 68139f258595bcca2658e394a4251e30dfbe6510
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "925055"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Affichage et édition dans Excel depuis Business Central 

Avec des pages qui affichent une liste d'enregistrements dans des lignes et des colonnes, comme une liste de clients, de commandes client ou de factures, vous pouvez également afficher les enregistrements à l'aide de Microsoft Excel. Pour cela, vous avez deux possibilités. Vous pouvez sélectionner l'action **Ouvrir dans Excel** ou l'action **Modifier dans Excel** sur la page. Les différences entre les deux actions sont les suivantes :  

## <a name="open-in-excel"></a>Ouvrir dans Excel

-    Avec cette action, Excel tient compte de tous les filtres de la page qui limitent les enregistrements affichés. Cela signifie que le classeur Excel contiendra les mêmes lignes et colonnes figurant sur la page dans [!INCLUDE[prodshort](includes/prodshort.md)].

-    Vous pouvez apporter des modifications à des enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prodshort](includes/prodshort.md)]. Vous ne pouvez enregistrer les modifications apportées au fichier Excel que sur votre ordinateur. 

-    Cette action fonctionne sur Windows et macOS. 

>[!NOTE]
>Pour [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, l'action **Ouvrir dans Excel** n'est pas disponible si l'action **Modifier dans Excel** l'est.

## <a name="edit-in-excel"></a>Modifier dans Excel

-    Avec cette action, le classeur Excel ne tient pas compte des filtres de la page qui limitent les enregistrements affichés. Cela signifie que le classeur Excel contiendra tous les enregistrements et colonnes disponibles, indépendamment de ce qui est affiché sur la page. 

-    L'avantage de l'action **Modifier dans Excel** est qu'elle vous permet d'apporter des modifications à des enregistrements dans Excel puis de les publier dans [!INCLUDE[prodshort](includes/prodshort.md)].

-    Ceci fonctionne uniquement sur Windows, pas macOS.

>[!NOTE]
>Pour [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, l'action **Modifier dans Excel** est disponible uniquement si le module complémentaire Excel a été installé par votre administrateur. Pour les administrateurs, si vous souhaitez connaître la manière de configurer le module complémentaire Excel, consultez [Configuration du module complémentaire Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Voir les différences entre les options 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Voir aussi
[Utilisation de Business Central](ui-work-product.md)  
