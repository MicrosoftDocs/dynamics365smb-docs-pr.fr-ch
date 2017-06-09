---
title: "Utilisation de Dynamics 365 for Financials comme source de données PowerApps | Microsoft Docs"
description: "Vous pouvez rendre vos données financières disponibles sous forme de source de données dans Power Apps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cedc95b23481b8cb76da85e8459a97b1880a4218
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-powerapps-data-source"></a>Utilisation de Dynamics 365 for Financials comme source de données PowerApps
Vous pouvez rendre vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles sous forme de source de données dans PowerApps.  

**Remarque** : Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans PowerApps
1. Dans votre navigateur, accédez à [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), puis connectez-vous.
2. Dans le volet de navigation de gauche, choisissez **Nouvelle application**.
3. Choisissez votre éditeur, PowerApps Studio for Windows ou PowerApps Studio for Web.

   PowerApps Studio for Windows est une application de bureau utilisée pour créer et publier PowerApps. PowerApps Studio for Web est la solution en ligne utilisée pour créer et publier PowerApps.
4. L'étape suivante pour créer un PowerApp consiste à sélectionner vos données. Cliquez sur l'icône représentant une flèche et choisissez l'option **Nouvelle connexion** dans le coin supérieur gauche de la page.
5. Dans la liste des connexions disponibles, cliquez sur **Dynamics 365 for Financials**.
6. PowerApps affiche une page de connexion qui vous invite à fournir les informations nécessaires pour vous connecter à vos données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour vous connecter, vous devez spécifier une URL OData, un nom d'utilisateur, un mot de passe et le nom de la société.

   Pour l'*URL OData*, vous pouvez copier l'URL OData V4 de n'importe quel service Web répertorié dans la page **Services Web** dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Pour le *Nom de la société*, utilisez le nom qui est affiché dans le champ **Nom** de la fenêtre **Informations société** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si votre [!INCLUDE[d365fin](includes/d365fin_md.md)] contient plusieurs sociétés, sélectionnez le nom de la société approprié dans la liste de la fenêtre **Sociétés**. Dans les deux cas, assurez-vous que le nom que vous spécifiez dans l'assistant PowerApps correspond exactement au texte affiché dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple `My Company`.

   Pour le nom d'utilisateur et le mot de passe, utilisez le nom et la clé d'accès rapide au service Web qui sont spécifiés pour votre compte dans la fenêtre **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, votre nom d'utilisateur est *ADMIN*, et la clé d'accès rapide au service Web qui sert de mot de passe est *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Cliquez sur le bouton **Connexion** pour continuer. PowerApps affiche un ensemble de données par défaut pour [!INCLUDE[d365fin](includes/d365fin_md.md)]. Choisissez l'ensemble de données **Par défaut**.

   PowerApps affiche la liste des tables disponibles à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces tables, ou points de terminaison, représentent tous les services Web que vous avez publiés à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.
8. Choisissez la table à utiliser pour votre PowerApp, puis sélectionnez le bouton **Connexion**.
9. Répétez les étapes précédentes pour ajouter des informations [!INCLUDE[d365fin](includes/d365fin_md.md)] supplémentaires à votre modèle de données Power BI.

   **Remarque** : Une fois que vous êtes connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous ne serez plus invité à fournir l'URL OData, le nom d'utilisateur ou le mot de passe.

À ce stade, vous êtes connecté à vos données Dynamics 365 et vous êtes prêt à générer votre PowerApp. Pour plus d'informations, voir [Documentation PowerApp](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Voir aussi
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importation de données métier à partir d'autres systèmes financiers](upload-data.md)  
[Configuration [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finance](finance.md)  

