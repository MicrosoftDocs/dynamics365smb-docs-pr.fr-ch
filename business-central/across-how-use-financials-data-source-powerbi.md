---
title: "Configuration de la génération d'états pour Business Central dans Power BI | Microsoft Docs"
description: "Vous pouvez rendre vos données disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/03/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: f2b672feed3065791ad5976591c694c6435843f8
ms.contentlocale: fr-ch
ms.lasthandoff: 06/01/2018

---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Utilisation de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] comme source de données Power BI pour générer des états
Vous pouvez rendre vos données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.  

Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Pour ajouter [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] comme source de données dans Power BI Desktop
1. Dans Power BI Desktop, dans le volet gauche de navigation, choisissez **Extraire les données**.
2. Dans la fenêtre **Extraire les données**, choisissez **Services en ligne**, **Microsoft Dynamics 365 Business Central**, puis cliquez sur le bouton **Connexion**.
3. Power BI affiche un assistant qui va vous guider tout au long du [processus de connexion](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Vous serez invité à vous connecter au service. Cliquez sur **Se connecter** et choisissez le compte auquel vous voulez vous connecter. Il doit s'agir du même compte que celui utilisé pour vous connecter à [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Cliquez sur le bouton **Connexion** pour continuer. L'assistant Power BI affiche la liste des sociétés et des sources de données Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces sources de données représentent tous les services Web que vous avez publiés à partir de chaque société dans Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.
6. Spécifiez les données à ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.
7. Répétez les étapes précédentes pour ajouter des informations Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] supplémentaires, ou d'autres données, à votre modèle de données Power BI.

> [!NOTE]  
> Une fois que vous êtes connecté à Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], vous n'êtes plus invité à vous connecter.

Une fois les données chargées, elles apparaissent dans le volet de navigation à droite dans la page. À ce stade, vous êtes connecté à vos données Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] et vous êtes prêt à générer votre état Power BI. 

Avant de générer votre état, il est préférable d'importer le fichier de thème Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Le fichier de thème crée une palette de couleurs afin de pouvoir établir des états avec le même style de couleur que le pack de contenu Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sans avoir à définir des couleurs personnalisées pour chaque visuel.

Pour plus d'informations, voir [Documentation Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finances](finance.md)  
[Connexion de Power BI aux [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

