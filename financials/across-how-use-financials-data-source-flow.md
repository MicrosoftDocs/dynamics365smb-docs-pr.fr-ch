---
title: "Connecter vos données avec Flow| Microsoft Docs"
description: "Vous pouvez rendre vos données Financials disponibles sous forme de données sources et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé
Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.  

> [!NOTE]  
>   Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Flow
1. Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com/en-us/), puis connectez-vous.
2. Choisissez **Mes flux** dans le ruban en haut de la page.
3. Dans la fenêtre **Mes flux**, cliquez sur l'option **Créer à partir de rien**.
4. Dans la liste des déclencheurs disponibles, sélectionnez l'un des déclencheurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles :  
    *Lorsqu'un enregistrement est créé*,  
    *Lors de la suppression d'un enregistrement*,  
    *Lorsqu'un enregistrement est modifié*,  
    *Lorsque l'approbation d'un client est exigée*,  
    *Lorsque l'approbation d'un nom feuille comptabilité est exigée*,  
    *Lorsque l'approbation d'une ligne feuille comptabilité est exigée*,  
    *Lorsque l'approbation d'un article est exigée*,  
    *Lorsque l'approbation d'un document achat est exigée*,  
    *Lorsque l'approbation d'un document vente est exigée*, ou  
    *Lorsque l'approbation d'un fournisseur est exigée*.
5. Le flux affiche vous invite à fournir les informations nécessaires pour vous connecter à vos données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si vous avez sélectionné l'un des déclencheurs suivants : *Lorsqu'un enregistrement est créé*, *Lorsqu'un enregistrement est modifié* ou *Lors de la suppression d'un enregistrement*, vous devez sélectionner un nom de société et un nom de table. Avec un autre déclencheur, seul le nom de la société est nécessaire pour se connecter.

   Flow affiche la liste des sociétés et des tables disponibles à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ces tables, ou points de terminaison, représentent tous les services Web que vous avez publiés à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Sinon, créer une nouvelle URL de service Web dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide de l'option **Créer un ensemble de données** de la page **Services Web**, à l'aide du guide de configuration assistée **Configurer la création d'états** ou en choisissant l'option **Modifier dans Excel** dans n'importe quelle liste.

À ce stade, vous êtes connecté à vos données Finance and Operations, Business edition et vous êtes prêt à générer votre flux. Pour plus d'informations, voir [Documentation Flow](https://flow.microsoft.com/documentation/getting-started/).

Pour résoudre les problèmes avec Microsoft Flow, voir [Résolution des problèmes : Intégration à Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Voir aussi
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)    
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  

