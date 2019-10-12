---
title: Utilisez les états Business Central dans Power BI | Microsoft Docs
description: Vous pouvez rendre vos données disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: b57b87dd8cdc9390ed5b1b7136107639f689c192
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305012"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>Utilisation de [!INCLUDE [prodlong](includes/prodlong.md)] comme source de données Power BI pour générer des états

Vous pouvez rendre vos données [!INCLUDE[prodlong](includes/prodlong.md)] disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.  

Vous devez disposer d'un compte valide avec [!INCLUDE[prodshort](includes/prodshort.md)] et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Pour plus d'informations, voir [Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>Pour ajouter [!INCLUDE[prodshort](includes/prodshort.md)] comme source de données dans Power BI Desktop

1. Dans Power BI Desktop, dans le volet de navigation de gauche, choisissez **Extraire les données**.
2. Sur la page **Extraire les données**, choisissez **Services en ligne**, **Microsoft Dynamics 365 Business Central**, puis cliquez sur le bouton **Connexion**.
3. Power BI affiche un assistant qui va vous guider tout au long du processus de connexion. Vous serez invité(e) à vous connecter à [!INCLUDE [prodshort](includes/prodshort.md)]. Cliquez sur **Se connecter** et choisissez le compte auquel vous voulez vous connecter. Il doit s'agir du même compte que celui utilisé pour vous connecter à [!INCLUDE [prodshort](includes/prodshort.md)].
4. Cliquez sur le bouton **Connexion** pour continuer. L'assistant Power BI affiche la liste des sociétés, des environnements et des sources de données Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces sources de données représentent tous les services Web que vous avez publiés à partir de chaque abonné/société dans Microsoft [!INCLUDE [prodshort](includes/prodshort.md)].
5. Sinon, créer une nouvelle URL de service Web dans [!INCLUDE [prodshort](includes/prodshort.md)] à l'aide de l'option **Créer un ensemble de données** sur la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.
6. Spécifiez les données à ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.
7. Répétez les étapes précédentes pour ajouter des informations [!INCLUDE [prodshort](includes/prodshort.md)] supplémentaires, ou d'autres données, à votre modèle de données Power BI.

> [!NOTE]  
> Une fois que vous êtes connecté(e) à [!INCLUDE [prodshort](includes/prodshort.md)], vous n'êtes plus invité(e) à vous connecter.

Une fois les données chargées, elles apparaissent dans le volet de navigation à droite dans la page. À ce stade, vous êtes connecté(e) à vos données [!INCLUDE [prodshort](includes/prodshort.md)] et vous êtes prêt(e) à générer votre état Power BI.  

Avant de générer votre état, il est préférable d'importer le fichier de thème [!INCLUDE [prodshort](includes/prodshort.md)].  Le fichier de thème crée une palette de couleurs afin de pouvoir établir des états avec le même style de couleur que les applications [!INCLUDE [prodshort](includes/prodshort.md)] sans avoir à définir des couleurs personnalisées pour chaque visuel.

Pour plus d'informations, reportez-vous à la [documentation Power BI](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-also"></a>Voir aussi

[Activation de vos données commerciales pour Power BI](admin-powerbi.md)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
