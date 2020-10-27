---
title: Activation de l’intégration Power BI avec Business Central
description: Découvrez comment configurer la connexion à Power BI afin d’obtenir des informations, des informations décisionnelles et des indicateurs de performance clés à partir de vos données Business Central avec les applications Business Central pour Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ce4b45dbe80ab1972c92cde144b457eeeaff3402
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927087"
---
# <a name="enabling-power-bi-integration-with-prodshort"></a>Activation de l’intégration de Power BI à [!INCLUDE[prodshort](includes/prodshort.md)]

Cet article décrit comment préparer [!INCLUDE[prodshort](includes/prodshort.md)] pour l’intégration avec Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] en ligne est déjà activée pour intégration, bien que vous souhaitiez peut-être lire certaines informations sur les licences. Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site, vous aurez configuré votre environnement pour vous connecter à Power BI avant que les utilisateurs puissent l’utiliser.

## <a name="power-bi-licensing"></a><a name="license"></a>Gestion des licences Power BI

Avec [!INCLUDE[prodshort](includes/prodshort.md)], les utilisateurs bénéficient d’une licence Power BI qui donne accès aux fonctionnalités les plus courantes dans [!INCLUDE[prodshort](includes/prodshort.md)] et Power BI. Vous pouvez également acheter une licence Power BI Pro qui donne accès à des fonctionnalités supplémentaires. Le tableau suivant donne un aperçu des fonctionnalités disponibles avec chaque licence.

|Licence Power|Afficher les états|Créer des états|Partager des états|Actualiser les états| Applications [!INCLUDE[prodshort](includes/prodshort.md)]|
|-------------|--------||
|Power BI, version gratuite|![une coche](media/check.png)|![une autre coche](media/check.png)|(limitée)|(limitée)||
|Power BI Pro|![encore une autre coche](media/check.png)|![c’est une coche](media/check.png)|![encore une coche](media/check.png)|(étendue)|![dernière coche](media/check.png)|

Pour plus d’informations, consultez [Gestion des licences du service Power BI pour les utilisateurs de votre organisation](/power-bi/admin/service-admin-licensing-organization) ou [S’inscrire au service Power BI en tant que particulier](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prodshort-on-premises-for-power-bi-integration"></a><a name="setup"></a>Configurer [!INCLUDE[prodshort](includes/prodshort.md)] sur site pour l’intégration Power BI

Cette section explique les conditions requises pour un déploiement [!INCLUDE[prodshort](includes/prodshort.md)] sur site à intégrer à Power BI.

1. Les services Web OData et le point de terminaison ODataV4 sont activés.

    Le service Web OData doit être activé sur le [!INCLUDE[server](includes/server.md)] et le port OData ouvert dans le pare-feu. Pour plus d’informations, reportez-vous à la rubrique [Configuration de Business Central Server - Services Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Le serveur local doit être accessible depuis Internet.

2. Les comptes d’utilisateur [!INCLUDE[prodshort](includes/prodshort.md)] ont une clé d’accès au service Web.

    Une clé d’accès au service Web est nécessaire pour afficher les données [!INCLUDE[prodshort](includes/prodshort.md)] dans Power BI. Vous pouvez attribuer une clé d’accès au service Web à chaque compte d’utilisateur. Ou plutôt, créez un compte spécifique avec une clé d’accès au service Web à l’usage de tous les utilisateurs. Pour plus d’informations, reportez-vous à la rubrique [Authentification des services Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. L’authentification NavUserPassword ou Azure Active Directory est configurée.

4. Pour voir les états Power BI intégrés dans les pages [!INCLUDE[prodshort](includes/prodshort.md)], une application doit être enregistrée pour [!INCLUDE[prodshort](includes/prodshort.md)] dans Microsoft Azure.

    L’application enregistrée a besoin d’une autorisation pour les services Power BI. Pour plus d’informations, consultez [Enregistrer [!INCLUDE[prodshort](includes/prodshort.md)] sur site dans Azure AD pour l’intégration avec d’autres services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Si votre déploiement utilise l’authentification NavUserPassword, [!INCLUDE[prodshort](includes/prodshort.md)] se connecte au même service Power BI pour tous les utilisateurs. Vous spécifierez ce compte de service dans le cadre de l’enregistrement de l’application. Avec l’authentification Azure AD, [!INCLUDE[prodshort](includes/prodshort.md)] se connecte au service Power BI associé aux comptes utilisateurs individuels.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Publier des données en tant que services Web

Les codeunits, pages et requêtes que vous souhaitez utiliser comme source de données dans les états Power BI doivent être publiés en tant que services Web. Il existe de nombreux services Web publiés par défaut. Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prodshort](includes/prodshort.md)]. Sur la page **Services Web** , assurez-vous que le champ **Publier** est sélectionné pour les services Web répertoriés ci-dessus. Cette tâche est généralement administrative.

Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

> [!TIP]
> Pour savoir ce que vous pouvez faire pour garantir les meilleures performances des services Web, comme observé depuis Business Central Server (point de terminaison) et le consommateur (client), consultez [Écrire des services Web efficaces](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
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
