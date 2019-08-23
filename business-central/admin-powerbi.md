---
title: Activation de vos données commerciales pour Power BI| Microsoft Docs
description: Il est facile d'obtenir des informations exploitables, de la veille économique et des KPI de vos applications Business Central pour Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 07/08/2019
ms.author: bmeier
ms.openlocfilehash: 4223d3eba6253f87aee3f86b3a9dfe4107d48947
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755279"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Activation de vos données commerciales pour Power BI

Il est facile d'obtenir des informations exploitables de vos données [!INCLUDE[prodshort](includes/prodshort.md)] grâce à [!INCLUDE[prodshort](includes/prodshort.md)] et aux applications pour Power BI. Power BI extrait vos données, puis génère un tableau de bord prêt à l'emploi et des états basés sur ces données.  

Vous devez disposer d'un compte valide avec [!INCLUDE[prodshort](includes/prodshort.md)] et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) si vous souhaitez créer vos propres états Power BI. Les applications Power BI nécessitent des autorisations vers les tables d'où sont extraites les données. Vous trouverez plus d'informations sur les besoins ci-dessous.  

> [!IMPORTANT]
> Les applications Power BI décrites dans cet article sont conçues pour utiliser Azure Active Directory comme mécanisme d'authentification sauf indication contraire. Pour installer une application Power BI, vous devez également avoir une licence Power BI Pro.  Une fois que l'application Power BI est installée, elle peut être partagée avec les utilisateurs avec n'importe quel type de licence.

Microsoft a publié les applications suivantes pour Power BI :

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)] (sur site) - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] (sur site) - Finances  
- [!INCLUDE [prodlong](includes/prodlong.md)] (sur site) - Ventes  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Utilisation des tableaux de bord [!INCLUDE [prodshort](includes/prodshort.md)] dans Power BI

Chaque application contient des états que vous pouvez afficher :

- Sélectionnez un visuel du tableau de bord pour afficher l'un des états sous-jacents.  
- Filtrez l'état ou ajoutez les champs que vous souhaitez contrôler.  
- Épinglez cette vue personnalisée au tableau de bord pour continuer à effectuer le suivi.  
  Vous pouvez actualiser les données manuellement, et vous pouvez configurer un programme d'actualisation. Pour plus d'informations, voir [Configuration d'une actualisation planifiée](/power-bi/refresh-scheduled-refresh).  

Les applications sont conçues pour fonctionner avec les données de toute société de votre [!INCLUDE[prodshort](includes/prodshort.md)]. Lorsque vous installez l'application Power BI, spécifiez un ou plusieurs paramètres à connecter à votre [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Vous pouvez également générer vos propres états et tableaux de bord dans Power BI selon vos données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Connexion de vos données métier à Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Pour connecter vos données dans Power BI

1. Ouvrez votre navigateur, accédez à https://powerbi.microsoft.com et connectez-vous à votre compte.
2. Sélectionnez **Extraire les données** en bas du volet de navigation gauche.  

    ![Naviguer pour obtenir des données](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Vous pouvez également démarrer depuis [!INCLUDE [prodshort](includes/prodshort.md)]. Depuis votre page d'accueil, accédez à **Sélection des états** dans la section Power BI. Sélectionnez **Service** ou **Mon organisation** dans le ruban. Lorsque l'une de ces actions est sélectionnée, vous arrivez dans la galerie Organisation de Power BI ou dans Microsoft AppSource, qui sera également filtrée pour afficher uniquement les applications associées à [!INCLUDE[prodshort](includes/prodshort.md)].

3. Dans la zone **Services**, sélectionnez **Extraire**. Une page s'ouvre et affiche **AppSource** et **Applications pour Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Sélectionnez **Applications** dans l'onglet **Applications pour Power BI** et choisissez l'application **Microsoft Dynamics 365 Business Central** à utiliser, puis cliquez sur **Obtenir maintenant**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Lorsque vous y êtes invité(e), entrez le nom de la société dans votre [!INCLUDE[prodshort](includes/prodshort.md)] auquel vous souhaitez vous connecter. Il ne s'agit pas du nom complet. Vous pourrez trouver le nom de la société dans la page **Sociétés** de votre instance [!INCLUDE[prodshort](includes/prodshort.md)].  

    > [!NOTE]
    > Si vous vous connectez à [!INCLUDE [prodshort](includes/prodshort.md)] sur site, vous devez spécifier le paramètre *URL du service Web*. Trouvez ceci sur la page **Services Web** dans [!INCLUDE [prodshort](includes/prodshort.md)]. Votre instance [!INCLUDE [server](includes/server.md)] doit être configurée pour l'authentification de base et vous devez spécifier un utilisateur et la clé d'accès Web de cet utilisateur comme mot de passe. Dans l'exemple suivant, remplacez *myserver :7048* par votre nom [!INCLUDE [server](includes/server.md)] et *CRONUS%20US* par le nom de votre société.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Une fois connecté(e), un tableau de bord et des états sont ajoutés à votre espace de travail Power BI. Une fois terminé, les mosaïques affichent les données de votre société [!INCLUDE[prodshort](includes/prodshort.md)].

    ![Sélectionnez Dynamics 365 Business Central, puis Obtenir maintenant.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Et ensuite ?

- Cliquez sur [poser une question dans la zone Q&R](/power-bi/service-q-and-a-tips) en haut du tableau de bord.
- [Modifiez les mosaïques](/power-bi/service-dashboard-edit-tile) du tableau de bord.  
- [Sélectionnez une mosaïque](/power-bi/service-dashboard-tiles) pour ouvrir l'état sous-jacent.  
- Par défaut, votre ensemble de données n'est pas planifié pour être actualisé. Vous pouvez modifier le calendrier d'actualisation ou essayer de l'actualiser à la demande à l'aide de **Actualiser maintenant**. Pour plus d'informations, voir [Configuration d'une actualisation planifiée](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI dans [!INCLUDE [prodshort](includes/prodshort.md)]

Votre page d'accueil dans [!INCLUDE [prodshort](includes/prodshort.md)] peut inclure un élément de contrôle Power BI pouvant être configuré pour afficher les états Power BI sur votre page d'accueil.

> [!IMPORTANT]
> Vous devez disposer d'un compte valide avec [!INCLUDE [prodshort](includes/prodshort.md)] et avec Power BI. De plus, si vous souhaitez modifier des états, vous devez télécharger Power BI Desktop. Pour plus d'informations, voir [Utilisation de Business Central en tant que source de données Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>À la première connexion

Quand vous vous connectez pour la première fois à [!INCLUDE [prodshort](includes/prodshort.md)], vous remarquerez une partie Power BI vide sur votre page d'accueil. Pour voir les états, vous devez d’abord vous connecter à Power BI en sélectionnant le lien *Mise en route avec Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)], puis communique avec le service Power BI pour déterminer si vous avez un compte Power BI valide. Une fois votre licence vérifiée, les états Power BI par défaut s'affichent sur votre page d'accueil.

### <a name="selecting-power-bi-reports"></a>Sélection des états Power BI

Le contrôle Power BI sur votre page d'accueil peut afficher tout état Power BI. Pour afficher un état existant, choisissez l'action **Sélectionner un état** dans la liste déroulante des commandes Power BI.  

La page de sélection des états affiche une liste de tous les états Power BI auxquels vous avez accès. Cette liste est extraite de votre espace de travail Power BI. Activez chaque état que vous souhaitez afficher sur la page d'accueil, puis choisissez OK. Vous serez redirigé(e) vers votre page d'accueil et le dernier état que vous avez activé apparaîtra. A l'aide de la liste déroulante des commandes, utilisez les commandes Précédent et Suivant pour naviguer entre les états.  

### <a name="get-reports"></a>Obtenir des états

Si vous ne voyez aucun état sur la page Sélectionner des états, ou vous ne voyez pas l'état souhaité. Vous pouvez choisir d’obtenir des états à partir de *Mon organisation* ou de *Services*.
Choisissez *Mon organisation* pour accéder aux services Power BI où vous pouvez afficher les états au sein de votre organisation pour lesquels vous avez le droit de les visualiser et de les ajouter à votre espace de travail. Choisissez *Services* pour accéder à Microsoft AppSource où vous pouvez installer les applications Power BI.  

Vous pouvez également choisir de créer de nouveaux états Power BI. Une fois ces états publiés dans votre espace de travail Power BI, ils apparaîtront sur cette page.  

### <a name="managing-reports"></a>Gestion des états

Dans la section Power BI de votre page d’accueil, vous pouvez choisir l'action **Gérer l'état** dans la liste déroulante des commandes afin que vous puissiez modifier l'état sélectionné dans le tableau de bord.  

Des modifications peuvent être apportées à l'état, puis sauvegardées.  Toute modification apportée à l'état sera modifiée pour tout utilisateur avec lequel cet état est partagé puisque vous modifiez l'état stocké dans le service Power BI.  

Une fois vos modifications terminées, sélectionnez Enregistrer. S'il s'agit d'un état partagé, vous pouvez sélectionner Enregistrer sous pour éviter d'apporter cette modification à tous les utilisateurs.
Revenez au tableau de bord et l'état mis à jour apparaîtra. Si vous avez effectué une commande Enregistrer sous, vous devez ouvrir la page de sélection des états et activer le nouvel état.

### <a name="uploading-reports"></a>Téléchargement d'états

Vous pouvez télécharger de nouveaux états Power BI et les partager avec tous les utilisateurs de votre [!INCLUDE [prodshort](includes/prodshort.md)]. Les états sont partagés au sein de chaque société dans [!INCLUDE [prodshort](includes/prodshort.md)].  

Pour télécharger un état, sélectionnez l'action **Télécharger l’état** dans la liste déroulante des commandes. Vous pouvez ensuite télécharger un fichier .pbix qui définit les états que vous souhaitez partager. Vous pouvez modifier le nom par défaut du fichier.  

Une fois l'état téléchargé dans votre espace de travail Power BI, il est automatiquement chargé dans les espaces de travail Power BI de tous les autres utilisateurs de cette société lors de leur prochaine connexion à [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Configuration système requise

Pour importer les données [!INCLUDE[prodshort](includes/prodshort.md)] dans Power BI, vous devez disposer des autorisations sur les services Web utilisés pour récupérer les données. Les services Web obligatoires pour chaque application Power BI incluent :

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Opportunités ventes
- Informations sur le modèle Excel Afficher Société
- Étiquettes d'état Power BI

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Informations sur le modèle Excel Afficher Société
- Étiquettes d'état Power BI

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Ventes d'articles par client
- Tableau de bord ventes
- Modèle Excel Afficher Société
- Étiquettes d'état Power BI

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] sur site utilise les mêmes points de terminaison de service Web que [!INCLUDE [prodshort](includes/prodshort.md)] en ligne.

## <a name="web-services"></a>Services web

Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prodshort](includes/prodshort.md)]. Sur la page **Services Web**, assurez-vous que le champ **Publier** est sélectionné pour les services Web répertoriés ci-dessus.

## <a name="troubleshooting"></a>Incident

Le tableau de bord Power BI s'appuie sur les services Web publiés qui sont répertoriés ci-dessus. Il affichera les données de la société de démonstration ou de votre propre société si vous importez les données de votre solution financière actuelle. Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.  

### <a name="you-do-not-have-a-power-bi-account"></a>Vous n'avez pas de compte Power BI

Aucun compte Power BI n'a été créé. Afin d'avoir un compte Power BI valide, vous devez avoir une licence et vous devez avoir déjà ouvert une session dans Power BI, pour pouvoir créer votre espace de travail Power BI.  

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Vous devez disposer d'une licence Power BI Pro pour installer l'application [!INCLUDE [prodshort](includes/prodshort.md)] dans Power BI

Les applications Power BI ne peuvent être installées que par les utilisateurs disposant d'une licence Power BI Pro. Une fois que l'application Power BI est installée, vous pouvez la partager avec des utilisateurs ne disposant pas d'une licence Power BI Pro.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>« Échec de la validation des paramètres, assurez-vous que tous les paramètres sont valides »

Cette erreur indique qu'un ou plusieurs paramètres ne sont pas valides.

- Le paramètre de société spécifié ne correspond à aucune société [!INCLUDE [prodshort](includes/prodshort.md)] existante. Vérifiez le nom de la société dans la page **Sociétés** dans [!INCLUDE [prodshort](includes/prodshort.md)].
- Si vous vous connectez à [!INCLUDE [prodshort](includes/prodshort.md)] sur site. vous avez entré une URL non valide. Vous pouvez vérifier l’URL sur la page **Services Web** dans [!INCLUDE [prodshort](includes/prodshort.md)]  
- Un port n'est pas ouvert pour permettre à la demande de passer par votre pare-feu.

### <a name="login-failed"></a>Échec de la connexion

Si vous obtenez un message d'erreur de type échec après avoir utilisé vos informations d'identification utilisateur [!INCLUDE [prodshort](includes/prodshort.md)] pour vous connecter, vous rencontrez peut-être l'un des problèmes suivants :

- Le compte que vous utilisez n'est pas doté des autorisations nécessaires pour récupérer les données [!INCLUDE [prodshort](includes/prodshort.md)] de votre compte. Vérifiez que vous disposez des autorisations pour les données requises dans [!INCLUDE [prodshort](includes/prodshort.md)]et essayez à nouveau.
- Vous avez sélectionné un type d'authentification autre que Basique si vous vous connectez à [!INCLUDE [prodshort](includes/prodshort.md)] sur site.
- Vous n'avez pas entré de nom d'utilisateur ni de mot de passe valide.

### <a name="incorrect-company-name"></a>Nom de société incorrect

Une erreur commune consiste à entrer le nom complet de la société au lieu du nom de la société. Pour trouver le nom de la société, cherchez dans **Sociétés**. Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre société.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>La clé ne correspond à aucune ligne de la table

Si vous entrez un nom de société non valide pendant le processus de connexion, le message d'erreur suivant « La clé ne correspond à aucune ligne de la table » peut s'afficher. Indiquez le nom de société correct, puis reconnectez-vous.

### <a name="historical-data-appears-to-be-missing"></a>Les données historiques semblent manquer

Une fois que l'application Power BI est installée et que vos données apparaissent dans Power BI, vous remarquerez peut-être que toutes vos données ne s'affichent pas. Les ensembles de données sont filtrés pour ne renvoyer que les 365 derniers jours de données. Ce paramètre par défaut est en place pour accélérer les états.  

### <a name="i-only-see-data-for-a-single-company"></a>Je ne vois que des données pour une seule société

L'application Power BI affichera uniquement les données de la société [!INCLUDE [prodshort](includes/prodshort.md)] qui a été définie lorsque l'application Power BI a été installée. Les données provenant d'autres sociétés peuvent être ajoutées aux états en ajoutant de nouvelles requêtes utilisant différentes sociétés en tant que source de données.  

## <a name="see-also"></a>Voir aussi

[Mise en route avec Power BI](/power-bi/service-get-started)  
[Power BI - Concepts de base](/power-bi/service-basic-concepts)  
[Applications dans Power BI](/power-bi/consumer/end-user-app)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Microsoft Flow](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
