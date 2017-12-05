---
title: "Packs de contenu Dynamics 365 Business edition et Power BI | Microsoft Docs"
description: "Il est facile d'obtenir des informations exploitables, de la veille économique et des KPI de vos données Dynamics 365 grâce à Power BI et à Dynamics 365 Content Packs."
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f9a85074f2bc3ed2bff6022b9c248d3568a04e93
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="enabling-your-business-data-for-power-bi"></a>Activation de vos données commerciales pour Power BI
Il est facile d'obtenir des informations exploitables de vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] grâce à Power BI et aux packs de contenu [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI extrait vos données, puis génère un tableau de bord prêt à l'emploi et des états basés sur ces données.  

Microsoft a publié les packs de contenu suivants :

| Application | Désignation |
| --- | --- |
| Microsoft Dynamics 365 for Financials | Fournit un tableau de bord avec des données financières clés dans le temps, telles que les bénéfices et les dépenses, la marge d'exploitation et le cycle de trésorerie.|
| Microsoft Dynamics 365 for Financials - CRM | Fournit un tableau de bord avec des données clés sur les opportunités de vente et les contacts.  |
| Microsoft Dynamics 365 for Financials - Sales | Fournit un tableau de bord avec des données clés sur les ventes et le stock. |

## <a name="using-the-dashboards"></a>Utilisation des tableaux de bord
Chaque pack de contenu contient des états que vous pouvez afficher :

* Sélectionnez un visuel du tableau de bord pour afficher l'un des états sous-jacents.  
* Filtrez l'état ou ajoutez les champs que vous souhaitez contrôler.  
* Épinglez cette vue personnalisée au tableau de bord pour continuer à effectuer le suivi.  
  Vous pouvez actualiser les données manuellement, et vous pouvez configurer un programme d'actualisation. Pour plus d'informations, voir [Configuration d'une actualisation planifiée](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Les packs de contenu sont pré-configurés pour fonctionner avec les données provenant de la société de démonstration que vous obtenez lorsque vous vous connectez à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lorsque vous installez les applications dans Power BI et que vous vous connectez à vos propres données, certains états peuvent ne pas fonctionner, car ils reposent sur des données dont votre société ne dispose pas. Dans ces cas, vous pouvez simplement supprimer ces états de votre tableau de bord.  

> [!NOTE]  
>   Vous pouvez également générer vos propres états et tableaux de bord dans Power BI selon vos données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Connexion de vos données métier à Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Accéder à [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI
Pour afficher vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI, vous devez disposer des éléments suivants :  

* Accès à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Communauté Dynamics 365 Business edition](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Accès à Power BI. Pour plus d'informations, reportez-vous à [Power BI](https://powerbi.microsoft.com).

Sur le site Power BI, vous trouverez des informations supplémentaires relatives à la [connexion aux services avec les packs de contenu pour Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Pour accéder à vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI, dans la page de connexion, vous devez spécifier les informations suivantes :

| Champ | Désignation |
| --- | --- |
| **URL de flux OData** |L'URL OData permet à Power BI d'accéder aux données de votre société, par exemple https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Méthode d'authentification** |Sélectionnez **Basique**. |
| **Nom utilisateur** |Votre nom tel qu'il s'affiche pour votre compte dans [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple *Jean Dupont*. |
| **Mot de passe** |Il s'agit de la clé d'accès rapide au service Web pour votre compte d'utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Cela signifie que vous devez extraire 2 informations de [!INCLUDE[d365fin](includes/d365fin_md.md)] : l'*URL OData* et la *clé d'accès au service Web* pour votre compte utilisateur.  

### <a name="getting-the-url"></a>Obtention de l'URL
Lorsque vous ajoutez [!INCLUDE[d365fin](includes/d365fin_md.md)] à Power BI, vous devez spécifier une URL pour que Power BI puisse accéder aux données de votre société. Dans la page de connexion, l'URL est appelée **URL de flux OData** et doit avoir le format suivant :

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
Dans cet exemple, *monentreprise* est le nom de votre service [!INCLUDE[d365fin](includes/d365fin_md.md)], *CRONUS US* est le nom de la société de démonstration et *%20* représente l'espace dans le nom.   
Pour obtenir l'URL, dans [!INCLUDE[d365fin](includes/d365fin_md.md)], recherchez et ouvrez la fenêtre **Services Web**. Cette fenêtre répertorie les services Web actuellement disponibles, et vous pouvez copier le lien du champ **URL OData** pour l'un des services Web OData par défaut.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Affichage du nom d'utilisateur et de la clé d'accès rapide au service Web
Pour utiliser des données à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI, dans la fenêtre **Se connecter à Financials**, vous devez spécifier un nom d'utilisateur et un mot de passe. Le nom d'utilisateur est votre nom tel qu'il s'affiche pour votre compte dans [!INCLUDE[d365fin](includes/d365fin_md.md)] afin que Power BI puisse se connecter à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le mot de passe correspond à la clé d'accès rapide au service Web définie pour votre compte utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Pour trouver ces informations, dans [!INCLUDE[d365fin](includes/d365fin_md.md)], recherchez la fenêtre **Utilisateurs**, puis ouvrez la fiche de votre compte d'utilisateur. Sur le raccourci **Général**, copiez la valeur du champ **Nom d'utilisateur** et sur le raccourci **Accès service web**, copiez la valeur du champ **Clé d'accès service web**. Si le champ **Clé d'accès service web** est vide, sélectionnez dans le ruban **Modifier la clé d'accès service web**, sélectionnez le champ **La clé n'expire jamais**, puis cliquez sur le bouton OK. Vous pouvez alors copier la clé.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Obtention de données de [!INCLUDE[d365fin](includes/d365fin_md.md)]
Le tableau de bord [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche les états les plus courants que vous utiliserez pour effectuer le suivi de votre activité. Les données sont extraites de votre société [!INCLUDE[d365fin](includes/d365fin_md.md)] en utilisant les services Web pour lire les données en temps réel. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], la fenêtre **Services web** répertorie les services Web qui ont été créés pour vous.

> [!NOTE]  
>   Si vous modifiez le nom de l'un de ces services Web, les données ne s'affichent pas dans Power BI.  
Si vous souhaitez ajouter et utiliser d'autres données dans Power BI, vous devez trouver les tables dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les exposer comme services Web, puis les ajouter au pack de contenu. Il s'agit d'un scénario avancé, et nous vous recommandons de commencer avec les données déjà disponibles dans Power BI.  

## <a name="troubleshooting"></a>Incident
Le tableau de bord Power BI s'appuie sur les services Web publiés qui sont répertoriés ci-dessus. Il affichera les données de la société de démonstration ou de votre propre société si vous importez les données de votre solution financière actuelle. Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.  

**« Échec de la validation des paramètres, assurez-vous que tous les paramètres sont valides »**  
Si ce message d'erreur s'affiche une fois que vous avez saisi votre URL [!INCLUDE[d365fin](includes/d365fin_md.md)], assurez-vous que les conditions suivantes sont remplies :  

* L'URL suit exactement ce motif :

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Supprimez tout texte qui suit le nom de la société entre parenthèse  
* Assurez-vous qu'il n'y a pas de barre oblique à la fin de l'URL.  
* Assurez-vous que la connexion est sécurisée, ce qui est indiqué par l'URL qui commence par *https*.  

**« Échec de la connexion »**  
Si vous obtenez un message d'erreur de type échec de la connexion lorsque vous vous connectez au tableau de bord à l'aide de vos informations d'identification [!INCLUDE[d365fin](includes/d365fin_md.md)], cela peut être causé par l'un des problèmes suivants :

* Le compte que vous utilisez n'est pas doté des autorisations nécessaires pour lire les données [!INCLUDE[d365fin](includes/d365fin_md.md)] de votre compte.

    Vérifiez votre compte utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vérifiez que vous avez utilisé la bonne clé d'accès rapide au service Web comme mot de passe, puis essayez de nouveau.  
* L'instance de [!INCLUDE[d365fin](includes/d365fin_md.md)] à laquelle vous essayez de vous connecter n'est pas dotée d'un certificat SSL valide. Dans ce cas, vous obtiendrez un message d'erreur plus détaillé (« impossible d'établir une relation SSL fiable »).

    > [!NOTE]  
>   Les certificats auto-signés ne sont pas pris en charge.  

**« Oups »**  
Si une boîte de dialogue d'erreur « Oups » s'affiche une fois que vous avez passé la boîte de dialogue d'authentification, cela est généralement causé par un problème qui survient lors de la connexion aux données du pack de contenu.

* Vérifiez que l'URL suit le motif qui a été spécifié plus tôt :

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* Une erreur courante est de spécifier l'intégralité de l'URL pour un service Web spécifique :

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Vous avez peut-être aussi oublié de spécifier le nom de la société :

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Migrer des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] comme source de données PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] dans Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

