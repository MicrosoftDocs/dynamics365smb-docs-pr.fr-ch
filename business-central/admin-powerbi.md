---
title: Introduction à Business Central et Power BI| Microsoft Docs
description: Obtenez une vue d’ensemble de l’utilisation de Power BI pour obtenir des informations, des informations décisionnelles et des indicateurs de performance clés à partir de vos données Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 38d7cc9bf45c3bef239a68cd0e4865ef2833776e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935151"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] et Power BI

Obtenir des informations sur vos données [!INCLUDE[prod_short](includes/prod_short.md)] est facile avec [Power BI](https://powerbi.microsoft.com), système de visualisation de données de Microsoft. Power BI récupère les données [!INCLUDE[prod_short](includes/prod_short.md)] vous permettant de créer des tableaux de bord et des états basés sur ces données. Power BI fournit une alternative flexible aux états intégrés dans [!INCLUDE[prod_short](includes/prod_short.md)], vous permettant d’explorer et de personnaliser la visualisation, et même de fusionner les données de différentes entreprises dans [!INCLUDE[prod_short](includes/prod_short.md)]. Certains états Power BI peuvent également être intégrés à Business Central et affichés sans quitter le système. Les tableaux de bord plus complexes sont mieux expérimentés depuis le site Web Power BI.

![Power BI et Business Central](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Ce que vous pouvez faire avec Power BI et [!INCLUDE[prod_short](includes/prod_short.md)]

Il existe différentes fonctionnalités pour utiliser [!INCLUDE[prod_short](includes/prod_short.md)] et Power BI. Vous pouvez faire certaines choses depuis Power BI, tandis que vous pouvez en faire d’autres depuis [!INCLUDE[prod_short](includes/prod_short.md)]. De plus, certaines fonctionnalités ne sont disponibles qu’avec [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, pas sur site. Le tableau suivant vous donne une vue d’ensemble.

|Fonctionnalité|Description|En ligne|Sur site|Plus d’informations|
|-------|-----------|--------------|-----------|----------------|
|Afficher les données [!INCLUDE[prod_short](includes/prod_short.md)] dans Power BI|Vous pouvez consulter vos données depuis [!INCLUDE[prod_short](includes/prod_short.md)] dans les états dans Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] en ligne comprend des états Power BI prédéfinis. Ou votre organisation a peut-être mis à votre disposition certains états personnalisés.|![Fonctionne en ligne](media/check.png)|![Fonctionne en local](media/check.png)|[Voir…](across-working-with-business-central-in-powerbi.md)|
|Afficher les états Power BI dans le client [!INCLUDE[prod_short](includes/prod_short.md)].| Les états Power BI qui affichent les données [!INCLUDE[prod_short](includes/prod_short.md)] peuvent être intégrés directement dans les pages [!INCLUDE[prod_short](includes/prod_short.md)] des composants. Vous pouvez changer de partie pour afficher tout état mis à votre disposition. |![fonctionne en ligne](media/check.png)|![Fonctionne en local](media/check.png)<sup>[*](#onprem)</sup>|[Voir…](across-working-with-powerbi.md).|
|Créez des états et des tableaux de bord dans Power BI qui affichent les données [!INCLUDE[prod_short](includes/prod_short.md)].|Utilisez Power BI Desktop pour créer vos propres états et tableaux de bord. Vous pouvez publier les états vers votre propre service Power BI ou les partager avec tous les utilisateurs de votre organisation.|![Fonctionne en ligne](media/check.png)|![fonctionne en local](media/check.png)|[Voir…](across-how-use-financials-data-source-powerbi.md)
|Applications [!INCLUDE[prod_short](includes/prod_short.md)] dans Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publie trois applications pour Power BI sur Microsoft AppSource. Ces applications créent des états et des tableaux de bord détaillés dans votre service Power BI pour visualiser les données [!INCLUDE[prod_short](includes/prod_short.md)]. Les applications disponibles incluent : <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Fonctionne en ligne](media/check.png)||[Voir…](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a>Cette fonctionnalité nécessite une application enregistrée pour Business Central dans Microsoft Azure. Pour plus d’informations, consultez [Enregistrer Business Central sur site dans Azure AD pour l’intégration avec d’autres services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Prise en main de Power BI

Il y a quelques tâches à effectuer avant de pouvoir commencer à utiliser Power BI avec [!INCLUDE[prod_short](includes/prod_short.md)]. Certaines des tâches ne sont généralement effectuées que par des administrateurs ou des super utilisateurs.

1. Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] sur site, assurez-vous que votre déploiement réponde aux exigences décrites dans [Configurer [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour l’intégration Power BI](admin-powerbi-setup.md#setup). Cette tâche est généralement administrative.

2. Publiez des données en tant que services Web.

    Les codeunits, pages et requêtes que vous souhaitez utiliser comme source de données dans les états Power BI doivent être publiés en tant que services Web. Il existe de nombreux services Web publiés par défaut. Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prod_short](includes/prod_short.md)].

    Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

3. Obtenez un compte Power BI.

    Pour faire quoi que ce soit avec Power BI et [!INCLUDE[prod_short](includes/prod_short.md)], que vous soyez administrateur ou simple consommateur, vous aurez besoin d’un compte de service Power BI. Pour créer un compte, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Pour vous inscrire à un compte, utilisez votre adresse e-mail professionnelle et votre mot de passe. L’inscription nécessite que vous ayez une licence, mais dans la plupart des cas, vous devriez déjà avoir une licence gratuite. Pour plus d’informations, reportez-vous à la rubrique [Gestion des licences Power BI](admin-powerbi-setup.md#license).

4. Si vous souhaitez créer vos propres états Power BI, obtenez Power BI Desktop.

    Vous pouvez télécharger [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Pour plus d’informations, reportez-vous à la rubrique [Obtenir Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

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