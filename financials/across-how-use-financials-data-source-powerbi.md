---
title: "Configuration de la génération d'états pour Finance and Operations, Business edition dans Power BI | Microsoft Docs"
description: "Vous pouvez rendre vos données Financials disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 056761b398737bd052b68488756198051f0cdb9a
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI pour générer des états
Vous pouvez rendre vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.  

> [!NOTE]  
> Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Power BI Desktop
1. Dans Power BI Desktop, dans le volet gauche de navigation, choisissez **Extraire les données**.
2. Dans la fenêtre **Extraire les données**, choisissez **Services en ligne**, **Dynamics 365 for Finance and Operations, Business edition**, puis cliquez sur le bouton **Connexion**.
3. Power BI affiche un assistant qui va vous guider tout au long du [processus de connexion](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). La première étape consiste à se connecter au service. Cliquez sur **Se connecter** et choisissez le compte auquel vous voulez vous connecter. Il doit s'agir du même compte que celui utilisé pour vous connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Cliquez sur le bouton **Connexion** pour continuer. L'assistant Power BI affiche la liste des sociétés et des sources de données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces sources de données représentent tous les services Web que vous avez publiés à partir de chaque société dans [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.
6. Spécifiez les données à ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.
7. Répétez les étapes précédentes pour ajouter des informations [!INCLUDE[d365fin](includes/d365fin_md.md)] supplémentaires à votre modèle de données Power BI.

> [!NOTE]  
> Une fois que vous êtes connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous n'êtes plus invité à vous connecter.

Une fois les données chargées, elles apparaissent dans le volet de navigation à droite dans la page. À ce stade, vous êtes connecté à vos données Finance and Operations, Business edition et vous êtes prêt à générer votre état Power BI. Pour plus d'informations, voir [Documentation Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finances](finance.md)  
[Connexion de Power BI aux [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

