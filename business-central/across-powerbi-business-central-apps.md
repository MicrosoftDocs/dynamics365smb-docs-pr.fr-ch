---
title: Utilisation des applications Business Central dans Power BI| Microsoft Docs
description: Il est facile d’obtenir des informations exploitables, de la veille économique et des KPI de vos applications Business Central pour Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 292f78f16b77940fa16a6ffc25bd79dbca0684e3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915875"
---
# <a name="using-the-prodshort-apps-in-power-bi"></a>Utilisation des applications [!INCLUDE [prodshort](includes/prodshort.md)] dans Power BI

> **S’APPLIQUE À :** [!INCLUDE [prodlong](includes/prodlong.md)] en ligne 

[!INCLUDE [prodlong](includes/prodlong.md)] publie les applications Power BI suivantes, qui fournissent des tableaux de bord détaillés pour afficher les données :

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales

## <a name="overview"></a>Aperçu

Chaque application comprend plusieurs états dans lesquels vous pouvez explorer les données, y compris les fonctionnalités suivantes :

- Sélectionnez un visuel du tableau de bord pour afficher l’un des états sous-jacents.  
- Filtrez l’état ou ajoutez les champs que vous souhaitez contrôler.  
- Épinglez une vue personnalisée au tableau de bord pour continuer à effectuer le suivi.  
  Vous pouvez actualiser les données manuellement, et vous pouvez configurer un programme d’actualisation. Pour plus d’informations, voir [Configuration d’une actualisation planifiée](/power-bi/refresh-scheduled-refresh).  

Les applications sont conçues pour fonctionner avec les données de toute société dans [!INCLUDE[prodshort](includes/prodshort.md)]. Lorsque vous installez l’application Power BI, spécifiez un ou plusieurs paramètres à connecter à votre [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Vous pouvez également générer vos propres états et tableaux de bord dans Power BI selon vos données [!INCLUDE[prodshort](includes/prodshort.md)]. Pour plus d’informations, voir [Connexion de vos données métier à Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Conditions préalables

Les applications Power BI nécessitent des autorisations sur les tables à partir desquelles les données sont extraites et les services Web utilisés pour récupérer les données. La table suivante répertorie les services Web requis pour chaque application Power BI :
    
|Application | Services Web|
|----|-------------|
|[!INCLUDE[prodshort](includes/prodshort.md)] - CRM| <ul><li>Opportunités ventes</li><li>Informations sur le modèle Excel Afficher Société</li><li>Étiquettes d’état Power BI</li></ul>|
|[!INCLUDE[prodshort](includes/prodshort.md)] - Finance| <ul><li>PowerBIFinance</li><li>Informations sur le modèle Excel Afficher Société</li><li>Étiquettes d’état Power BI</li></ul>|
|[!INCLUDE[prodshort](includes/prodshort.md)] - Sales| <ul><li>Ventes d’articles par client</li><li>Tableau de bord ventes</li><li>Informations sur le modèle Excel Afficher Société</li><li>Étiquettes d’état Power BI</li></ul>|

> [!TIP]
> Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prodshort](includes/prodshort.md)]. Sur la page **Services Web** , assurez-vous que le champ **Publier** est sélectionné pour les services Web répertoriés ci-dessus. Pour plus d’informations, voir [Publication d’un service Web](across-how-publish-web-service.md).

## <a name="get-ready"></a>Mise en route

Inscrivez-vous au service Power BI. Si vous ne vous êtes pas encore inscrit, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Au moment de votre inscription, utilisez votre adresse e-mail professionnelle et votre mot de passe.

## <a name="install-a-prodshort-app-in-power-bi"></a>Installer une application [!INCLUDE[prodshort](includes/prodshort.md)] dans Power BI

1. Ouvrez votre navigateur, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com) et connectez-vous à votre compte.
2. Sélectionnez **Extraire les données** en bas du volet de navigation gauche.  

    ![Naviguer pour obtenir des données](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Vous pouvez également démarrer depuis [!INCLUDE [prodshort](includes/prodshort.md)]. Depuis votre page d’accueil, accédez à **Sélection des états** dans la section Power BI. Sélectionnez **Service** ou **Mon organisation** dans le ruban. Soit la galerie Organisation dans Power BI, soit Microsoft AppSource s’ouvre, filtré pour n’afficher que les applications liées à [!INCLUDE[prodshort](includes/prodshort.md)].

3. Dans la zone **Services** , sélectionnez **Extraire** .

    Cette étape ouvre la page **Applications Power BI** , qui vous permet de rechercher l’application Power BI disponible dans **AppSource** .  

4. Dans la boîte de dialogue **Rechercher** , entrez **Dynamics 365 Business Central** .
5. Sélectionnez l’application que vous souhaitez utiliser, sélectionnez **Obtenir maintenant** , puis **Installer** .  

    Ensuite l’application sera disponible à partir d’ **Applications** dans le menu de navigation dans Power BI.

## <a name="connect-the-prodshort-app-to-your-data"></a>Connecter l’application [!INCLUDE[prodshort](includes/prodshort.md)] à vos données

1. Sous **Applications** , sélectionnez l’application Business Central, puis **Connecter** .
2. À l’invite, renseignez les champs **Nom de la société** et **Environnement** avec les informations concernant l’instance [!INCLUDE[prodshort](includes/prodshort.md)] à laquelle vous souhaitez vous connecter.

    - Pour **Nom de la société** , assurez-vous d’utiliser le nom complet et non le nom d’affichage. Vous pourrez trouver le nom de la société dans la page **Sociétés** dans [!INCLUDE[prodshort](includes/prodshort.md)]. 
    - Pour **Environnement** , si vous n’avez pas créé plusieurs environnements, entrez **Production** .

3. Sélectionnez **Suivant** .
4. Sélectionnez **Se connecter** .
5. À l’invite, entrez le nom d’utilisateur et le mot de passe pour vous connecter à [!INCLUDE[prodshort](includes/prodshort.md)].
6. Une fois connecté(e), un tableau de bord et des états sont ajoutés à votre espace de travail Power BI. Une fois terminé, les mosaïques affichent les données de votre société [!INCLUDE[prodshort](includes/prodshort.md)].

    ![Sélectionnez Dynamics 365 Business Central, puis Obtenir maintenant.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Résolution des problèmes

Le tableau de bord Power BI repose sur les services Web publiés répertoriés ci-dessus. Il affiche les données de la société de démonstration ou de votre propre entreprise si vous importez des données de votre solution financière actuelle. Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.  

### <a name="you-dont-have-a-power-bi-account"></a>Vous n’avez pas de compte Power BI

Aucun compte Power BI n’a été créé. Vous devez avoir une licence pour obtenir un compte Power BI valide. De plus, vous devez vous être déjà connecté à Power BI pour créer votre espace de travail Power BI.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Message : Aucun état n’est activé. Choisissez Sélectionner un état pour afficher la liste des états disponibles.

Ce message apparaît si l’état par défaut n’a pas pu être déployé sur votre espace de travail Power BI. Ou l’état a été déployé, mais n’a pas été actualisé avec succès. Si ce problème se produit, accédez à l’état dans votre espace de travail Power BI, sélectionnez **Ensemble de données** , **Paramètres** , puis mettez à jour les informations d’identification manuellement. Une fois le jeu de données actualisé, revenez dans [!INCLUDE[prodshort](includes/prodshort.md)] et sélectionnez manuellement l’état dans la page **Sélectionner des états** .

### <a name="you-need-a-power-bi-pro-license-to-install-the-prodshort-app-in-power-bi"></a>Vous devez disposer d’une licence Power BI Pro pour installer l’application [!INCLUDE[prodshort](includes/prodshort.md)] dans Power BI

Vous avez besoin d’une [licence Power BI Pro](/power-bi/service-features-license-type) pour partager votre contenu, ainsi que les personnes avec lesquelles vous le partagez. Le contenu doit se trouver dans un espace de travail dans une [Capacité Premium](/power-bi/service-premium-what-is). Pour en savoir plus, consultez [Moyens de partager votre travail dans Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>« Échec de la validation des paramètres, assurez-vous que tous les paramètres sont valides »

Cette erreur indique qu’un ou plusieurs paramètres ne sont pas valides.

- Le paramètre d’environnement spécifié ne correspond à aucun environnement de production ou sandbox [!INCLUDE[prodshort](includes/prodshort.md)] existant.
- Le paramètre de société spécifié ne correspond à aucune société [!INCLUDE[prodshort](includes/prodshort.md)] existante. Vérifiez le nom de la société dans la page **Sociétés** dans [!INCLUDE[prodshort](includes/prodshort.md)].
- Si vous vous connectez à [!INCLUDE[prodshort](includes/prodshort.md)] sur site, vous avez entré une URL qui n’est pas valide. Vous pouvez vérifier l’URL sur la page **Services Web** dans [!INCLUDE[prodshort](includes/prodshort.md)]  
- Un port n’est pas ouvert pour permettre à la demande de passer par votre pare-feu.

### <a name="cant-sign-in"></a>Connexion impossible

Si vous obtenez un message d’erreur de type échec après avoir utilisé vos informations d’identification utilisateur [!INCLUDE[prodshort](includes/prodshort.md)] pour vous connecter, vous rencontrez peut-être l’un des problèmes suivants :

- Le compte que vous utilisez n’est pas doté des autorisations nécessaires pour récupérer les données [!INCLUDE[prodshort](includes/prodshort.md)] de votre compte. Vérifiez que vous disposez des autorisations pour les données requises dans [!INCLUDE[prodshort](includes/prodshort.md)] et réessayez.
- Vous avez sélectionné un type d’authentification autre que Basique si vous vous connectez à [!INCLUDE[prodshort](includes/prodshort.md)] sur site.
- Vous n’avez pas entré de nom d’utilisateur ni de mot de passe valide.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Message : Votre source de données ne peut pas être actualisée, car les informations d’identification ne sont pas valides. Veuillez mettre à jour vos informations d’identification et réessayer.

Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site, le problème peut être que l’URL OData n’est exposée qu’au réseau local.

### <a name="incorrect-company-name"></a>Nom de société incorrect

Une erreur commune consiste à entrer le nom complet de la société au lieu du nom de la société. Pour trouver le nom de la société, cherchez dans **Sociétés** . Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre société.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>La clé ne correspond à aucune ligne de la table

Si vous entrez un nom de société non valide pendant le processus de connexion, le message d’erreur suivant « La clé ne correspond à aucune ligne de la table » peut s’afficher. Indiquez le nom de société correct, puis reconnectez-vous.

### <a name="historical-data-appears-to-be-missing"></a>Les données historiques semblent manquer

Une fois que l’application Power BI est installée et que vos données apparaissent dans Power BI, vous remarquerez peut-être que toutes vos données ne s’affichent pas. Les ensembles de données sont filtrés pour ne renvoyer que les 365 derniers jours de données. Ce paramètre par défaut est en place pour accélérer les états.  

### <a name="i-only-see-data-for-a-single-company"></a>Je ne vois que des données pour une seule société

L’application Power BI affichera uniquement les données de la société [!INCLUDE[prodshort](includes/prodshort.md)] qui a été définie lorsque l’application Power BI a été installée. Les données provenant d’autres sociétés peuvent être ajoutées aux états en ajoutant de nouvelles requêtes utilisant différentes sociétés en tant que source de données.  

### <a name="what-now"></a>Et ensuite ?

- Cliquez sur [poser une question dans la zone Q&R](/power-bi/service-q-and-a-tips) en haut du tableau de bord.
- [Modifiez les mosaïques](/power-bi/service-dashboard-edit-tile) du tableau de bord.  
- [Sélectionnez une mosaïque](/power-bi/service-dashboard-tiles) pour ouvrir l’état sous-jacent.  
- Par défaut, votre ensemble de données n’est pas planifié pour être actualisé. Vous pouvez modifier le calendrier d’actualisation ou essayer de l’actualiser à la demande à l’aide de **Actualiser maintenant** . Pour plus d’informations, voir [Configuration d’une actualisation planifiée](/power-bi/refresh-scheduled-refresh).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Utilisation avec les données [!INCLUDE [prodshort](includes/prodshort.md)] dans Power BI](across-working-with-business-central-in-powerbi.md)  
[Création d’états Power BI pour afficher les données [!INCLUDE [prodlong](includes/prodlong.md)]](across-how-use-financials-data-source-powerbi.md)  
[Power BI pour les consommateurs](/power-bi/consumer/end-user-consumer)  
[Le « nouveau look » du service Power BI](/power-bi/service-new-look)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentation Power BI](/power-bi/)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
