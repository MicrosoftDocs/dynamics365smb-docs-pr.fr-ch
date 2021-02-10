---
title: Affichage et édition dans Excel depuis Business Central
description: En savoir plus sur la manière dont vous pouvez ouvrir les pages dans Microsoft Excel à partir de Business Central pour une meilleure analyse de données.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/06/2020
ms.author: jswymer
ms.openlocfilehash: cb172cd1d3285128e871fedb44ccd70fb84a669a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754182"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Affichage et édition dans Excel depuis Business Central

Avec des pages qui affichent une liste d’enregistrements dans des lignes et des colonnes, comme une liste de clients, de commandes client ou de factures, vous pouvez également afficher les enregistrements à l’aide de Microsoft Excel. Pour cela, vous avez deux possibilités. Vous pouvez sélectionner l’action **Ouvrir dans Excel** ou l’action **Modifier dans Excel** sur la page. Les différences entre les deux actions sont les suivantes :  

## <a name="open-in-excel"></a>Ouvrir dans Excel

- Avec cette action, Excel tient compte de tous les filtres de la page qui limitent les enregistrements affichés. Le classeur Excel contiendra les mêmes lignes et colonnes figurant sur la page dans [!INCLUDE[prod_short](includes/prod_short.md)].

- Vous pouvez apporter des modifications à des enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous ne pouvez enregistrer les modifications apportées au fichier Excel que sur votre ordinateur.

- Cette action fonctionne sur Windows et macOS.

> [!NOTE]
> Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, l’action **Ouvrir dans Excel** est disponible par défaut. Cependant, si vous configurez [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour la modification de données dans Excel, l’action **Ouvrir dans Excel** est alors remplacée par l’action **Modifier dans Excel**.

## <a name="edit-in-excel"></a>Modifier dans Excel

- Avec cette action, Excel respecte la plupart des filtres de la page qui limitent les enregistrements affichés, de sorte que le classeur Excel contiendra presque les mêmes enregistrements et colonnes.

- L’avantage de l’action **Modifier dans Excel** est qu’elle vous permet d’apporter des modifications à des enregistrements dans Excel puis de les publier dans [!INCLUDE[prod_short](includes/prod_short.md)].

- Ceci fonctionne uniquement sur Windows, pas macOS.

- Vous pouvez changer la société que vous utilisez. Pour ce faire, sélectionnez l’icône **Options** ![Options du module complémentaire Excel](media/cogwheel.png "Options du module complémentaire Excel") dans le volet Module complémentaire Excel, puis la société dans le champ **Société**.  

    > [!IMPORTANT]
    > Lors du changement de société, assurez-vous que le champ **Environnement** n’est pas vide. Si tel est le cas, définissez-le sur l’une des options disponibles ; sinon, le module complémentaire ne fonctionnera pas correctement.  

Si vous apportez des modifications au module complémentaire, vous devez le recharger afin de mettre à jour la connexion. Pour recharger, utilisez le ![menu Module complémentaire Excel](media/excel-addin-menu.png "Menu Module complémentaire Excel") dans le coin supérieur droit du module complémentaire. Si vous ne pouvez pas charger le complément, parlez-en à votre administrateur. Si vous êtes l’administrateur, reportez-vous à la rubrique [Configuration du complément Excel pour la modification des données Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, l’action **Modifier dans Excel** est disponible seulement si le module complémentaire Excel a été configuré par votre administrateur, et uniquement pour le client web. Pour les administrateurs, si vous souhaitez connaître la manière de configurer le module complémentaire Excel, consultez [Configuration du module complémentaire Excel pour modifier des données Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Voir les différences entre les options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md)  
[Utilisation de Business Central](ui-work-product.md)  
[Améliorations de l’intégration d’Excel dans la deuxième vague de publication 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
