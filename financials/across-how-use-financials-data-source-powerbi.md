---
title: "Créer une source de données Power BI avec votre Financials | Microsoft Docs"
description: "Vous pouvez rendre vos données Financials disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 53fb2ae7bbbaf3215ca2549e207512f7c06838b4
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="using-included365finincludesd365finmdmd-as-a-power-bi-data-source"></a>Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI
Vous pouvez rendre vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles sous forme de source de données dans Power BI et créer des rapports puissants sur l'état de votre activité.  

> [!NOTE]  
>   Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Power BI Desktop
1. Dans Power BI Desktop, dans le volet gauche de navigation, choisissez **Extraire les données**.
2. Dans la fenêtre **Extraire les données**, choisissez **Services en ligne**, **Dynamics 365 for Financials**, puis cliquez sur le bouton **Connexion**.

   Power BI affiche un assistant qui va vous guider tout au long du processus de connexion. La première étape consiste à entrer une URL OData et le nom de la société qui est associé à votre compte [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Pour l'*URL OData*, vous pouvez copier l'URL OData V4 de n'importe quel service Web répertorié dans la page **Services Web** dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Pour le *Nom de la société*, utilisez le nom qui est affiché dans le champ **Nom** de la fenêtre **Informations société** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si votre [!INCLUDE[d365fin](includes/d365fin_md.md)] contient plusieurs sociétés, sélectionnez le nom de la société approprié dans la liste de la fenêtre **Sociétés**. Dans les deux cas, assurez-vous que le nom que vous spécifiez dans l'assistant Power BI correspond exactement au texte affiché dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple `My Company`.
3. Après avoir entré les informations, cliquez sur le bouton OK. L'étape suivante de l'assistant consiste à entrer votre nom d'utilisateur et votre mot de passe.

   > [!NOTE]  
>    S'il existe d'autres options d'authentification disponibles dans le volet gauche de navigation, choisissez *Basique*.
4. Entrez votre nom d'utilisateur et votre mot de passe. Vous pouvez trouver ces informations dans la fenêtre **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilisez la **Clé d'accès Web** comme mot de passe.

   Par exemple, votre nom d'utilisateur est *ADMIN*, et la clé d'accès rapide au service Web qui sert de mot de passe est *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Cliquez sur le bouton **Connexion** pour continuer. L'assistant Power BI affiche la liste des sources de données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces sources de données représentent tous les services Web que vous avez publiés à partir de votre [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.
6. Spécifiez les données à ajouter à votre modèle de données, puis sélectionnez le bouton **Charge**.
7. Répétez les étapes précédentes pour ajouter des informations [!INCLUDE[d365fin](includes/d365fin_md.md)] supplémentaires à votre modèle de données Power BI.

   > [!NOTE]  
>    Une fois que vous êtes connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous ne serez plus invité à fournir l'URL OData, le nom d'utilisateur ou le mot de passe.

Une fois les données chargées, elles apparaissent dans le volet de navigation à droite dans la page. À ce stade, vous êtes connecté à vos données Dynamics 365 et vous êtes prêt à générer votre état Power BI. Pour plus d'informations, voir [Documentation Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Voir aussi
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  

