---
title: Utilisation de Dynamics 365 for Financials dans Microsoft Flow | Microsoft Docs
description: "Vous pouvez rendre vos données financières disponibles sous forme de source de données dans Power Apps."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 76d24ed80adb08083c6167040be8cc6a4bcc3167
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-in-microsoft-flow"></a>Utilisation de Dynamics 365 for Financials dans Microsoft Flow
Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.  

**Remarque** : Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Flow
1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com/en-us/), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Dans la fenêtre **Mes flux**, cliquez sur l'option **Créer à partir de rien**.
4. Dans la liste des déclencheurs disponibles, sélectionnez l'un des deux déclencheurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles : *Lorsqu'un enregistrement est créé*, ou *Lorsqu'un enregistrement est modifié*.
5. Le flux affiche une page de connexion qui vous invite à fournir les informations nécessaires pour vous connecter à vos données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour vous connecter, vous devez spécifier un nom pour la connexion, une URL OData, un nom d'utilisateur, un mot de passe et le nom de la société.

   Pour l'*URL OData*, vous pouvez copier l'URL OData V4 de n'importe quel service Web répertorié dans la page **Services Web** dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Pour le *Nom de la société*, utilisez le nom qui est affiché dans le champ **Nom** de la fenêtre **Informations société** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si votre [!INCLUDE[d365fin](includes/d365fin_md.md)] contient plusieurs sociétés, sélectionnez le nom de la société approprié dans la liste de la fenêtre **Sociétés**. Dans les deux cas, assurez-vous que le nom que vous spécifiez dans l'assistant PowerApps correspond exactement au texte affiché dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple `My Company`.

   Pour le nom d'utilisateur et le mot de passe, utilisez le nom et la clé d'accès rapide au service Web qui sont spécifiés pour votre compte dans la fenêtre **Utilisateurs** dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, votre nom d'utilisateur est *ADMIN*, et la clé d'accès rapide au service Web qui sert de mot de passe est *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Pour en savoir plus, reportez-vous à [Procédure : gérer les utilisateurs et les autorisations](ui-how-users-permissions.md).
6. Choisissez le bouton **Créer** au bas de la page pour continuer.

   Flow affiche une liste des tables disponibles à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces tables, ou points de terminaison, représentent tous les services Web que vous avez publiés à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.
7. Choisissez les données à utiliser dans Flow.

À ce stade, vous êtes connecté à vos données Dynamics 365 et vous êtes prêt à générer votre flux. Pour plus d'informations, voir [Documentation Flow](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Voir aussi
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importation de données métier à partir d'autres systèmes financiers](upload-data.md)  
[Procédure : gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)    
[Configuration [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finance](finance.md)  

