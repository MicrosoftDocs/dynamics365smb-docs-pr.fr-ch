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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528477"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Utilisation de [!INCLUDE[prodlong](includes/prodlong.md)] comme source de données Power BI pour générer des états

Vous pouvez rendre vos données [!INCLUDE[prodlong](includes/prodlong.md)] disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.  

Vous devez disposer d'un compte valide avec [!INCLUDE[prodshort](includes/prodshort.md)] et avec Power BI. Vous devez également télécharger [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Pour plus d'informations, voir [Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Pour ajouter [!INCLUDE[prodshort](includes/prodshort.md)] comme source de données dans Power BI Desktop

1. Dans Power BI Desktop, dans le volet de navigation de gauche, choisissez **Extraire les données**.
2. Sur la page **Extraire les données**, choisissez **Services en ligne**, **Microsoft Dynamics 365 Business Central**, puis cliquez sur le bouton **Connexion**.
3. Power BI affiche un assistant qui va vous guider tout au long du processus de connexion, notamment à [!INCLUDE[prodshort](includes/prodshort.md)]. Choisissez **Se connecter**, puis le compte approprié. Utilisez le même compte que celui avec lequel vous vous êtes connecté(e) à [!INCLUDE[prodshort](includes/prodshort.md)].
4. Cliquez sur le bouton **Connexion** pour continuer. L'assistant Power BI affiche la liste des sociétés, des environnements et des sources de données Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces sources de données représentent tous les services web que vous avez publiés à partir de [!INCLUDE[prodshort](includes/prodshort.md)].

    Vous pouvez également créer une nouvelle URL de service web dans [!INCLUDE[prodshort](includes/prodshort.md)]. Choisissez l'une des méthodes suivantes :

      - Utiliser l'action **Créer un ensemble de données** sur la page **Services web**
      - Utiliser le guide de configuration assistée **Configurer la création d'états**
      - Choisir l'action **Modifier dans Excel** dans toutes les listes

5. Spécifiez les données à ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.
6. Répétez les étapes précédentes pour ajouter des informations [!INCLUDE[prodshort](includes/prodshort.md)] supplémentaires, ou d'autres données, à votre modèle de données Power BI.

> [!NOTE]  
> Une fois que vous êtes connecté(e) à [!INCLUDE[prodshort](includes/prodshort.md)], vous n'êtes plus invité(e) à vous connecter.

Une fois les données chargées, elles s'affichent dans le volet de navigation à droite dans la page. Vous êtes connecté(e) à vos données [!INCLUDE[prodshort](includes/prodshort.md)] et vous pouvez commencer à générer votre état Power BI.  

Avant de générer votre état, il est préférable d'importer le fichier de thème [!INCLUDE[prodshort](includes/prodshort.md)].  Le fichier de thème crée une palette de couleurs afin de pouvoir établir des états avec le même style de couleur que les applications [!INCLUDE[prodshort](includes/prodshort.md)] sans avoir à définir des couleurs personnalisées pour chaque visuel.

Pour plus d'informations, reportez-vous à la [documentation Power BI](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Activation de vos données commerciales pour Power BI](admin-powerbi.md)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
