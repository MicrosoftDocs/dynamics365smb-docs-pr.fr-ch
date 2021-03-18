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
ms.openlocfilehash: 17e41dd44dd4f7f99eabd4904d5ebd7c48d9964d
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493032"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Activation de l’intégration de Power BI à [!INCLUDE[prod_short](includes/prod_short.md)]

Cet article décrit comment préparer [!INCLUDE[prod_short](includes/prod_short.md)] pour l’intégration avec Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] en ligne est déjà activée pour intégration, bien que vous souhaitiez peut-être lire certaines informations sur les licences. Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous aurez configuré votre environnement pour vous connecter à Power BI avant que les utilisateurs puissent l’utiliser.

## <a name="power-bi-licensing"></a><a name="license"></a>Gestion des licences Power BI

Avec [!INCLUDE[prod_short](includes/prod_short.md)], les utilisateurs bénéficient d’une licence Power BI qui donne accès aux fonctionnalités les plus courantes dans [!INCLUDE[prod_short](includes/prod_short.md)] et Power BI. Vous pouvez également acheter une licence Power BI Pro qui donne accès à des fonctionnalités supplémentaires. Le tableau suivant donne un aperçu des fonctionnalités disponibles avec chaque licence.

|Licence Power|Afficher les états|Créer des états|Partager des états|Actualiser les états| Applications [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI, version gratuite|![une coche](media/check.png)|![une autre coche](media/check.png)|(limitée)|(limitée)||
|Power BI Pro|![encore une autre coche](media/check.png)|![c’est une coche](media/check.png)|![encore une coche](media/check.png)|(étendue)|![dernière coche](media/check.png)|

Pour plus d’informations, consultez [Gestion des licences du service Power BI pour les utilisateurs de votre organisation](/power-bi/admin/service-admin-licensing-organization) ou [S’inscrire au service Power BI en tant que particulier](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Configurer [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour l’intégration Power BI

Cette section explique les conditions requises pour un déploiement [!INCLUDE[prod_short](includes/prod_short.md)] sur site à intégrer à Power BI.

1. Configurez l’authentification NavUserPassword ou Azure Active Directory pour le déploiement.

    L’intégration Power BI ne prend pas en charge l’authentification Windows.  

2. Activez les services Web OData et le point de terminaison ODataV4.

    Le service Web OData doit être activé sur le [!INCLUDE[server](includes/server.md)] et le port OData ouvert dans le pare-feu. Pour plus d’informations, reportez-vous à la rubrique [Configuration de Business Central Server - Services Web OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Le serveur local doit être accessible depuis Internet.

3. Accordez aux comptes d’utilisateur [!INCLUDE[prod_short](includes/prod_short.md)] une clé d’accès au service Web.

    Une clé d’accès au service Web est nécessaire uniquement pour afficher les données [!INCLUDE[prod_short](includes/prod_short.md)] dans Power BI. Vous pouvez attribuer une clé d’accès au service Web à chaque compte d’utilisateur. Ou plutôt, créez un compte spécifique avec une clé d’accès au service Web à l’usage de tous les utilisateurs. Pour plus d’informations, reportez-vous à la rubrique [Authentification des services Web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Créez un enregistrement d’application pour [!INCLUDE[prod_short](includes/prod_short.md)] dans Microsoft Azure.

    Pour afficher les rapports Power BI intégrés dans les pages [!INCLUDE[prod_short](includes/prod_short.md)], une application doit être enregistrée pour [!INCLUDE[prod_short](includes/prod_short.md)] dans Microsoft Azure. L’application enregistrée a besoin d’une autorisation pour les services Power BI. Pour plus d’informations, consultez [Enregistrer [!INCLUDE[prod_short](includes/prod_short.md)] sur site dans Azure AD pour l’intégration avec d’autres services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Si votre déploiement utilise l’authentification NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] se connecte au même service Power BI pour tous les utilisateurs. Vous spécifierez ce compte de service dans le cadre de l’enregistrement de l’application. Avec l’authentification Azure AD, [!INCLUDE[prod_short](includes/prod_short.md)] se connecte au service Power BI associé aux comptes utilisateurs individuels.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Établissez la connexion initiale de Business Central vers Power BI.

    Avant que les utilisateurs finaux puissent utiliser Power BI dans [!INCLUDE[prod_short](includes/prod_short.md)], un administrateur de l’application Azure devra donner son accord au service Power BI.

    Pour établir la connexion initiale, ouvrez [!INCLUDE[prod_short](includes/prod_short.md)], et exécutez **Mise en route avec Power BI** à partir du Tableau de bord. Cette action vous guidera tout au long du processus de consentement et vérifiera votre licence Power BI. Lorsque vous y êtes invité, connectez-vous à l’aide d’un compte d’administrateur Azure. Pour en savoir plus, consultez [Se connecter à Power BI – une fois seulement](across-working-with-powerbi.md#connect).

## <a name="publish-data-as-web-services"></a>Publier des données en tant que services Web

Les codeunits, pages et requêtes que vous souhaitez utiliser comme source de données dans les états Power BI doivent être publiés en tant que services Web. Il existe de nombreux services Web publiés par défaut. Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Services Web**, assurez-vous que le champ **Publier** est sélectionné pour les services Web répertoriés ci-dessus. Cette tâche est généralement administrative.

Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

> [!TIP]
> Pour savoir ce que vous pouvez faire pour garantir les meilleures performances des services Web, comme observé depuis Business Central Server (point de terminaison) et le consommateur (client), consultez [Écrire des services Web efficaces](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
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