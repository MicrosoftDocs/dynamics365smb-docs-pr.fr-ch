---
title: Utiliser les états Power BI dans Business Central| Microsoft Docs
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
ms.openlocfilehash: a747a0bdb67187597cc33185b418844247b2e2b2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752990"
---
# <a name="working-with-power-bi-reports-in-prod_short"></a>Utilisation d’états Power BI dans [!INCLUDE [prod_short](includes/prod_short.md)]

Dans cet article, vous découvrirez quelques notions de base sur l’affichage des états Power BI dans [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="overview"></a>Aperçu

Les états Power BI vous donnent un aperçu de votre [!INCLUDE[prod_short](includes/prod_short.md)]. Diverses pages dans [!INCLUDE [prod_short](includes/prod_short.md)] incluent une partie d’états Power BI qui peut afficher des états Power BI. Le tableau de bord est une page type où vous verrez une partie d’éléments Power BI. Certaines pages de liste, comme **Articles**, comprennent également une partie Power BI.

[!INCLUDE [prod_short](includes/prod_short.md)] utilise le service Power BI. Les états à afficher dans [!INCLUDE [prod_short](includes/prod_short.md)] sont stockés dans un service Power BI. Dans [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez changer l’état affiché dans la partie Power BI vers tout état Power BI disponible dans votre service Power BI. La première fois que vous vous connectez à [!INCLUDE [prod_short](includes/prod_short.md)], et jusqu’à ce que vous vous connectiez à un service Power BI, les pièces restent vides, comme indiqué ici :

![Partie Power BI dans Business Central](./media/power-bi-part.png)

## <a name="prerequisites"></a>Conditions préalables

Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] sur site, il doit être activé pour l’intégration de Power BI. Cette tâche est généralement effectuée par un administrateur. Pour plus d’informations, consultez [Configurer [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour l’intégration Power BI](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] en ligne est déjà configuré pour s’intégrer à Power BI.

## <a name="get-ready"></a>Mise en route

Inscrivez-vous au service Power BI. Si vous ne vous êtes pas encore inscrit, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Au moment de votre inscription, utilisez votre adresse e-mail professionnelle et votre mot de passe.

## <a name="connect-to-power-bi---one-time-only"></a>Se connecter à Power BI - une fois seulement

Lorsque vous vous connectez pour la première fois [!INCLUDE [prod_short](includes/prod_short.md)], vous pourriez voir une partie Power BI vide sur une page, comme indiqué dans la figure précédente. La première chose à faire est de vous connecter à votre compte Power BI. Une fois connecté, vous pouvez voir les états. Vous ne devez effectuer cette étape qu’une seule fois.

Pour vous connecter à Power BI, sélectionnez le lien **Prise en main de Power BI** dans la partie **États Power BI**.

Pendant le processus de connexion, [!INCLUDE [prod_short](includes/prod_short.md)] communique avec le service Power BI pour déterminer si vous avez un compte et une licence Power BI valides. Une fois votre licence vérifiée, l’état Power BI par défaut s’affiche sur la page. Si aucun état n’est affiché, vous pouvez sélectionner un état dans la partie.

> [!TIP]
> Avec [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, cette étape téléchargera automatiquement les états Power BI par défaut utilisés dans [!INCLUDE [prod_short](includes/prod_short.md)] vers votre espace de travail Power BI.

##### <a name="from-prod_short-on-premises"></a>Depuis [!INCLUDE [prod_short](includes/prod_short.md)] sur site

Se connecter à Power BI depuis [!INCLUDE [prod_short](includes/prod_short.md)] est identique à la version en ligne. Cependant, vous serez invité sur la page **AUTORISATIONS DE SERVICE AZURE ACTIVE DIRECTORY** pour accorder l’accès aux services Power BI. Pour accorder l’accès, sélectionnez **Autoriser les services Azure**, puis **Accepter**.

Une fois connecté, vous pouvez sélectionner un état dans la partie Power BI sur les pages.

## <a name="show-power-bi-reports-on-list-pages"></a>Afficher les états Power BI sur les pages de liste

[!INCLUDE[prod_long](includes/prod_long.md)] comprend un Récapitulatif Power BI sur plusieurs pages de liste clé. Ce Récapitulatif fournit des informations supplémentaires sur les données de la liste. Lorsque vous vous déplacez entre les lignes de la liste, l’état est mis à jour et filtré pour l’écriture sélectionnée. Si vous ne voyez pas cette partie, dans la barre d’action, sélectionnez **Actions** > **Afficher** > **Afficher/Masquer les états Power BI**. Pour plus d’informations, consultez [Création d’états Power BI pour afficher les données de la liste dans [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="select-power-bi-reports"></a>Sélectionner les états Power BI

Une partie Power BI sur une page peut afficher n’importe quel état Power BI à votre disposition. Pour basculer vers un autre état, choisissez l’action **Sélectionner un état** depuis la liste déroulante des commandes en haut de la partie.  

La page **Sélection des états Power BI** affiche une liste de tous les états Power BI auxquels vous avez accès. Cette liste est extraite de votre espace de travail Power BI. Sélectionnez la zone **Activer** pour chaque état que vous souhaitez afficher sur la page d’accueil, puis choisissez **OK**. Vous serez redirigé(e) vers la page et le dernier état que vous avez activé apparaîtra. A l’aide de la liste déroulante des commandes, utilisez les commandes **Précédent** et **Suivant** pour naviguer entre les états.  

## <a name="get-reports"></a>Obtenir des états

Si vous ne voyez aucun état sur la page **Sélectionner des états Power BI**, ou si vous ne voyez pas l’état souhaité, choisissez **Obtenir des états**. Cette action vous permet de rechercher des états à partir de deux emplacements : *Mon organisation* ou *Prestations de service*.

- Choisissez **Mon organisation** pour accéder aux services Power BI. À partir de là, vous pouvez afficher les rapports au sein de votre organisation que vous avez le droit de consulter. Vous pouvez ensuite les ajouter à votre espace de travail.
- Choisissez **Services** pour accéder à Microsoft AppSource où vous pouvez installer les applications Power BI.  

> [!TIP]
> Si vous avez Power BI Desktop, vous pouvez également créer des états Power BI. Puis, une fois ces états publiés dans votre espace de travail Power BI, ils apparaîtront sur cette page **Sélectionner des états Power BI**.  

## <a name="manage-and-modify-reports"></a>Gérer et modifier les états

Vous pouvez apporter des modifications à un état dans la partie Power BI. Les modifications que vous apportez seront ensuite publiées dans le service Power BI. Si l’état est partagé avec d’autres utilisateurs, ils verront également les modifications, sauf si vous enregistrez les modifications dans un nouvel état.

Pour modifier un état, choisissez l’action **Gérer un état** dans la liste déroulante des commandes dans la partie Power BI. Ensuite, commencez à apporter des modifications. Une fois les modifications terminées, sélectionnez **Fichier** > **Enregistrer**. S’il s’agit d’un état partagé et si vous ne souhaitez pas effectuer la modification pour tous les utilisateurs, sélectionnez **Enregistrer sous** pour éviter de faire ce changement pour tous les utilisateurs.

Lorsque vous revenez au tableau de bord, l’état mis à jour apparaîtra. Si vous avez utilisé **Enregistrer sous**, vous devrez choisir **Sélectionner un état**, puis activez le nouvel état pour l’afficher.

> [!NOTE]
> Cette fonctionnalité n’est pas disponible avec [!INCLUDE [prod_short](includes/prod_short.md)] sur site.

## <a name="upload-reports"></a><a name="upload"></a>Télécharger des états

Les états Power BI peuvent être distribués entre les utilisateurs sous forme de fichiers .pbix. Si vous avez des fichiers .pbix, vous pouvez les télécharger et les partager avec tous les utilisateurs de [!INCLUDE [prod_short](includes/prod_short.md)]. Les états sont partagés au sein de chaque société dans [!INCLUDE [prod_short](includes/prod_short.md)].  

Pour télécharger un état, sélectionnez l’action **Télécharger l’état** dans la liste déroulante des commandes sur la partie **États Power BI**. Puis localisez le fichier .pbix qui définit les états que vous souhaitez partager. Vous pouvez modifier le nom par défaut du fichier.  

Une fois l’état téléchargé sur votre espace de travail Power BI, il se télécharge automatiquement sur les espaces de travail Power BI des autres utilisateurs.

> [!NOTE]
> Le téléchargement d’un état nécessite que vous disposiez d’autorisations de SUPER utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)]. De plus, vous ne pouvez pas télécharger d’états avec [!INCLUDE [prod_short](includes/prod_short.md)] sur site. Avec la version sur site, vous téléchargez des états directement sur votre espace de travail Power BI. Pour plus d’informations, reportez-vous à [Utilisation des données[!INCLUDE [prod_short](includes/prod_short.md)] dans Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Résolution des problèmes

Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.  

### <a name="you-dont-have-a-power-bi-account"></a>Vous n’avez pas de compte Power BI

Aucun compte Power BI n’a été créé. Pour obtenir un compte Power BI valide, vous devez avoir une licence et vous devez avoir déjà ouvert une session dans Power BI, pour créer votre espace de travail Power BI.   

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Message : Aucun état n’est activé. Choisissez Sélectionner un état pour afficher la liste des états disponibles.

Ce message apparaît si l’état par défaut n’a pas pu être déployé sur votre espace de travail Power BI. Ou l’état a été déployé, mais n’a pas été actualisé avec succès. Accédez à l’état dans votre espace de travail Power BI, sélectionnez **Ensemble de données**, **Paramètres**, puis mettez à jour les informations d’identification manuellement. Une fois le jeu de données actualisé, revenez dans [!INCLUDE[prod_short](includes/prod_short.md)] et sélectionnez manuellement l’état dans la page **Sélectionner des états**.


## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Création d’états Power BI pour afficher les données [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Utilisation avec les données [!INCLUDE [prod_short](includes/prod_short.md)] dans Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI pour les consommateurs](/power-bi/consumer/end-user-consumer)  
[Le « nouveau look » du service Power BI](/power-bi/service-new-look)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentation Power BI](/power-bi/)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]