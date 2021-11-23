---
title: Activation de l’intégration Power BI avec Business Central
description: Découvrez comment configurer la connexion à Power BI. Avec les rapports Power BI, obtenez des informations, des informations décisionnelles et des indicateurs de performance clés à partir de vos données Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 932bf57b8801c758c6bcaff4fbdad69265853487
ms.sourcegitcommit: 428ba6385cb27475e8803c2a8967daa22cfe8879
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/29/2021
ms.locfileid: "7724708"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Activation de l’intégration de Power BI à [!INCLUDE[prod_short](includes/prod_short.md)]

Cet article décrit comment préparer [!INCLUDE[prod_short](includes/prod_short.md)] pour l’intégration avec Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] en ligne est déjà activée pour intégration, bien que vous souhaitiez peut-être lire certaines informations sur les licences. Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous aurez configuré votre environnement pour vous connecter à Power BI avant que les utilisateurs puissent l’utiliser.

## <a name="power-bi-licensing"></a><a name="license"></a>Gestion des licences Power BI

Avec [!INCLUDE[prod_short](includes/prod_short.md)], les utilisateurs bénéficient d’une licence Power BI qui donne accès aux fonctionnalités les plus courantes dans [!INCLUDE[prod_short](includes/prod_short.md)] et Power BI. Vous pouvez également acheter une licence Power BI Pro qui donne accès à des fonctionnalités supplémentaires. Le tableau suivant donne un aperçu des fonctionnalités disponibles avec chaque licence.

|Licence Power|Afficher les états|Créer des états|Partager des états|Actualiser les états| Applications [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI, version gratuite|![une coche.](media/check.png)|![une autre coche](media/check.png)|(limitée)|(limitée)||
|Power BI Pro|![encore une autre coche.](media/check.png)|![c’est une coche](media/check.png)|![encore une coche](media/check.png)|(étendue)|![dernière coche](media/check.png)|

Pour plus d’informations, consultez [Gestion des licences du service Power BI pour les utilisateurs de votre organisation](/power-bi/admin/service-admin-licensing-organization) ou [S’inscrire au service Power BI en tant que particulier](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-pages-or-odata-web-services"></a><a name="exposedata"></a>Exposer des données via des pages API ou des services Web OData

Business Central propose deux manières d’exposer les données qui peuvent être consommées par les rapports Power BI : pages API et services Web Open Data Protocol (OData).

### <a name="api-pages"></a>Pages API

> **S’APPLIQUE À :** Business Central Online uniquement 

Une page API est un type de page spécifique créé dans le code AL qui permet d’accéder aux tables de la base de données via un service REST pris en charge par les webhooks et OData v4. Ce type de page ne peut pas être affiché dans l’interface utilisateur, mais est destiné à créer des services d’intégration fiables.

Business Central Online est disponible avec un ensemble d’API intégrées, que vous pouvez utiliser pour obtenir des données pour les entités commerciales les plus courantes, telles que les clients, les articles, les commandes client, etc. Aucun travail ou configuration supplémentaire n’est requis pour utiliser ces API comme source de données pour les rapports Power BI. Pour plus d’informations sur ces API, consultez [API Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central Online prend également en charge les API personnalisées. Les développeurs d’applications des solutions Business Central peuvent créer leurs propres pages API et les regrouper dans des extensions. Vous pouvez installer les extensions sur votre locataire. Une fois installé, vous pouvez utiliser les pages API pour vos rapports Power BI, comme vous le feriez avec les API intégrées (v2.0). Pour plus d’informations sur la création de pages d’API, consultez [Développement d’une API personnalisée](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

### <a name="odata-web-services"></a>Services Web OData

Vous pouvez publier des objets d’application Business Central, tels que des unités de code, des pages et des requêtes, comme les [services Web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Avec Business Central Online, de nombreux services Web sont publiés par défaut. Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Services Web**, assurez-vous que le champ **Publier** est sélectionné pour les services Web répertoriés ci-dessus. Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

Pour savoir ce que vous pouvez faire pour garantir les meilleures performances des services Web, comme observé depuis Business Central Server (point de terminaison) et le consommateur (client), consultez [Écrire des services Web efficaces](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Choisir d’utiliser des pages API ou des services Web OData

Dans la mesure du possible, nous vous encourageons à utiliser des pages API au lieu du service Web OData. Les pages API sont généralement plus rapides à charger les données dans les rapports Power BI que les services Web OData. De plus elles sont plus flexibles, car elles vous permettent d’obtenir des données à partir de champs de table qui ne sont pas définis dans un objet de page.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Configurer [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour l’intégration Power BI

Cette section explique les conditions requises pour un déploiement [!INCLUDE[prod_short](includes/prod_short.md)] sur site à intégrer à Power BI.

1. Configurez l’authentification NavUserPassword ou Azure Active Directory pour le déploiement.

    L’intégration Power BI ne prend pas en charge l’authentification Windows.  

2. Activez les services Web OData et le point de terminaison ODataV4.

    Le service Web OData doit être activé sur le [!INCLUDE[server](includes/server.md)] et le port OData ouvert dans le pare-feu. Pour plus d’informations, reportez-vous à la rubrique [Configuration de Business Central Server - Services Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Le serveur local doit être accessible depuis Internet.

3. Accordez aux comptes d’utilisateur [!INCLUDE[prod_short](includes/prod_short.md)] une clé d’accès au service Web.

    Une clé d’accès au service Web est nécessaire uniquement pour afficher les données [!INCLUDE[prod_short](includes/prod_short.md)] dans Power BI. Vous pouvez attribuer une clé d’accès au service Web à chaque compte d’utilisateur. Ou plutôt, créez un compte spécifique avec une clé d’accès au service Web à l’usage de tous les utilisateurs. Pour plus d’informations, reportez-vous à la rubrique [Authentification des services Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Using OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Créez un enregistrement d’application pour [!INCLUDE[prod_short](includes/prod_short.md)] dans Microsoft Azure.

    Pour afficher les rapports Power BI intégrés dans les pages [!INCLUDE[prod_short](includes/prod_short.md)], une application doit être enregistrée pour [!INCLUDE[prod_short](includes/prod_short.md)] dans Microsoft Azure. L’application enregistrée a besoin d’une autorisation pour les services Power BI. Pour plus d’informations, consultez [Enregistrer [!INCLUDE[prod_short](includes/prod_short.md)] sur site dans Azure AD pour l’intégration avec d’autres services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Si votre déploiement utilise l’authentification NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] se connecte au même service Power BI pour tous les utilisateurs. Vous spécifierez ce compte de service dans le cadre de l’enregistrement de l’application. Avec l’authentification Azure AD, [!INCLUDE[prod_short](includes/prod_short.md)] se connecte au service Power BI associé aux comptes utilisateurs individuels.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Établissez la connexion initiale de Business Central vers Power BI.

    Avant que les utilisateurs finaux puissent utiliser Power BI dans [!INCLUDE[prod_short](includes/prod_short.md)], un administrateur de l’application Azure devra donner son accord au service Power BI.

    Pour établir la connexion initiale, ouvrez [!INCLUDE[prod_short](includes/prod_short.md)], et exécutez **Mise en route avec Power BI** à partir du Tableau de bord. Cette action vous guidera tout au long du processus de consentement et vérifiera votre licence Power BI. Lorsque vous y êtes invité, connectez-vous à l’aide d’un compte d’administrateur Azure. Pour en savoir plus, consultez [Se connecter à Power BI – une fois seulement](across-working-with-powerbi.md#connect).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI pour les consommateurs](/power-bi/consumer/end-user-consumer)  
[Le « nouveau look » du service Power BI](/power-bi/service-new-look)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentation Power BI](/power-bi/)  
[Veille économique](bi.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]