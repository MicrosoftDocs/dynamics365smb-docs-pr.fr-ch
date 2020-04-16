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
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187523"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Affichage et édition dans Excel depuis Business Central

Avec des pages qui affichent une liste d'enregistrements dans des lignes et des colonnes, comme une liste de clients, de commandes client ou de factures, vous pouvez également afficher les enregistrements à l'aide de Microsoft Excel. Pour cela, vous avez deux possibilités. Vous pouvez sélectionner l'action **Ouvrir dans Excel** ou l'action **Modifier dans Excel** sur la page. Les différences entre les deux actions sont les suivantes :  

## <a name="open-in-excel"></a>Ouvrir dans Excel

- Avec cette action, Excel tient compte de tous les filtres de la page qui limitent les enregistrements affichés. Cela signifie que le classeur Excel contiendra les mêmes lignes et colonnes figurant sur la page dans [!INCLUDE[prodshort](includes/prodshort.md)].

- Vous pouvez apporter des modifications à des enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prodshort](includes/prodshort.md)]. Vous ne pouvez enregistrer les modifications apportées au fichier Excel que sur votre ordinateur.

- Cette action fonctionne sur Windows et macOS.

> [!NOTE]
> Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site, l'action **Ouvrir dans Excel** est disponible par défaut. Cependant, si vous configurez [!INCLUDE [prodshort](includes/prodshort.md)] sur site pour la modification de données dans Excel, l'action **Ouvrir dans Excel** est alors remplacée par l'action **Modifier dans Excel**.

## <a name="edit-in-excel"></a>Modifier dans Excel

- Avec cette action, Excel tient compte de la plupart des filtres de la page qui limitent les enregistrements affichés. Cela signifie que le classeur Excel contiendra presque les mêmes enregistrements et colonnes.

- L'avantage de l'action **Modifier dans Excel** est qu'elle vous permet d'apporter des modifications à des enregistrements dans Excel puis de les publier dans [!INCLUDE[prodshort](includes/prodshort.md)].

- Ceci fonctionne uniquement sur Windows, pas macOS.

- Vous pouvez changer la société que vous utilisez. Pour ce faire, sélectionnez l'icône **Options** ![Options du module complémentaire Excel](media/cogwheel.png "Options du module complémentaire Excel") dans le volet Module complémentaire Excel, puis la société dans le champ **Société**. 

    > [!IMPORTANT]
    > Lors du changement de société, assurez-vous que le champ **Environnement** n'est pas vide. Si tel est le cas, définissez-le sur l'une des options disponibles ; sinon, le module complémentaire ne fonctionnera pas correctement.  

Le module complémentaire Excel a été amélioré lors de la deuxième vague de publication 2019. Pour plus d'informations, voir [Améliorations de l'intégration Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site, l'action **Modifier dans Excel** est disponible seulement si le module complémentaire Excel a été configuré par votre administrateur, et uniquement pour le client web. Pour les administrateurs, si vous souhaitez connaître la manière de configurer le module complémentaire Excel, consultez [Configuration du module complémentaire Excel pour modifier des données Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin). Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site.

### <a name="see-the-differences-between-the-options"></a>Voir les différences entre les options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Utilisation de Business Central](ui-work-product.md)  
