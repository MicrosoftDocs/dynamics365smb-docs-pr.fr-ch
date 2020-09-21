---
title: Introduction à Business Central et Power BI| Microsoft Docs
description: Il est facile d'obtenir des informations exploitables, de la veille économique et des KPI de vos applications Business Central pour Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: a1e2e8ceee41c2c6ed517d000fc7c3a4a6aa274c
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697687"
---
# <a name="prodshort-and-power-bi"></a>[!INCLUDE[prodshort](includes/prodshort.md)] et Power BI

Obtenir des informations sur vos données [!INCLUDE[prodshort](includes/prodshort.md)] est facile avec [Power BI](https://powerbi.microsoft.com), système de visualisation de données de Microsoft. Power BI récupère les données [!INCLUDE[prodshort](includes/prodshort.md)] vous permettant de créer des tableaux de bord et des états basés sur ces données. Power BI fournit une alternative flexible aux états intégrés dans [!INCLUDE[prodshort](includes/prodshort.md)], vous permettant d’explorer et de personnaliser la visualisation, et même de fusionner les données de différentes entreprises dans [!INCLUDE[prodshort](includes/prodshort.md)]. Certains états Power BI peuvent également être intégrés à Business Central et affichés sans quitter le système. Les tableaux de bord plus complexes sont mieux expérimentés depuis le site Web Power BI.

![Power BI et Business Central](media/power-bi-intro.png)


## <a name="what-you-can-do-with-power-bi-and-prodshort"></a>Ce que vous pouvez faire avec Power BI et [!INCLUDE[prodshort](includes/prodshort.md)]

Il existe différentes fonctionnalités pour utiliser [!INCLUDE[prodshort](includes/prodshort.md)] et Power BI. Vous pouvez faire certaines choses depuis Power BI, tandis que vous pouvez en faire d’autres depuis [!INCLUDE[prodshort](includes/prodshort.md)]. De plus, certaines fonctionnalités ne sont disponibles qu’avec [!INCLUDE[prodshort](includes/prodshort.md)] en ligne, pas sur site. Le tableau suivant vous donne une vue d’ensemble.

|Fonctionnalité|Description|En ligne|Sur site|Plus d'informations|
|-------|-----------|--------------|-----------|----------------|
|Afficher les données [!INCLUDE[prodshort](includes/prodshort.md)] dans Power BI|Vous pouvez consulter vos données depuis [!INCLUDE[prodshort](includes/prodshort.md)] dans les états dans Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] en ligne comprend des états Power BI prédéfinis. Ou votre organisation a peut-être mis à votre disposition certains états personnalisés.|![coche](media/check.png)|![coche](media/check.png)|[Voir…](across-working-with-powerbi.md)|
|Afficher les états Power BI dans le client [!INCLUDE[prodshort](includes/prodshort.md)].| Les états Power BI qui affichent les données [!INCLUDE[prodshort](includes/prodshort.md)] peuvent être intégrés directement dans les pages [!INCLUDE[prodshort](includes/prodshort.md)] des composants. Vous pouvez changer de partie pour afficher tout état mis à votre disposition. |![coche](media/check.png)|![coche](media/check.png)<sup>[*](#onprem)</sup>|[Voir…](across-working-with-business-central-in-powerbi.md).|
|Créez des états et des tableaux de bord dans Power BI qui affichent les données [!INCLUDE[prodshort](includes/prodshort.md)].|Utilisez Power BI Desktop pour créer vos propres états et tableaux de bord. Vous pouvez publier les états vers votre propre service Power BI ou les partager avec tous les utilisateurs de votre organisation.|![coche](media/check.png)|![coche](media/check.png)|[Voir…](across-how-use-financials-data-source-powerbi.md)
|Applications [!INCLUDE[prodshort](includes/prodshort.md)] dans Power BI| [!INCLUDE[prodshort](includes/prodshort.md)] publie trois applications pour Power BI sur Microsoft AppSource. Ces applications créent des états et des tableaux de bord détaillés dans votre service Power BI pour visualiser les données [!INCLUDE[prodshort](includes/prodshort.md)]. Les applications disponibles incluent : <ul><li>[!INCLUDE [prodlong](includes/prodlong.md)] - CRM </li><li>[!INCLUDE [prodlong](includes/prodlong.md)] - Finance </li><li>[!INCLUDE [prodlong](includes/prodlong.md)] - Sales </li></ul>  |![coche](media/check.png)||[Voir…](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a>Cette fonctionnalité nécessite une application enregistrée pour Business Central dans Microsoft Azure. Pour plus d’informations, consultez [Enregistrer Business Central sur site dans Azure AD pour l’intégration avec d’autres services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Prise en main de Power BI

Il y a quelques tâches à effectuer avant de pouvoir commencer à utiliser Power BI avec [!INCLUDE[prodshort](includes/prodshort.md)]. Certaines des tâches ne sont généralement effectuées que par des administrateurs ou des super utilisateurs.

1. Si vous utilisez [!INCLUDE[prodshort](includes/prodshort.md)] sur site, assurez-vous que votre déploiement réponde aux exigences décrites dans [Configurer [!INCLUDE[prodshort](includes/prodshort.md)] sur site pour l’intégration Power BI](admin-powerbi-setup.md#setup). Cette tâche est généralement administrative.

2. Publiez des données en tant que services Web.

    Les codeunits, pages et requêtes que vous souhaitez utiliser comme source de données dans les états Power BI doivent être publiés en tant que services Web. Il existe de nombreux services Web publiés par défaut. Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prodshort](includes/prodshort.md)].
    
    Pour plus d’informations sur la publication des services Web, voir [Publier un service Web](across-how-publish-web-service.md).

3. Obtenez un compte Power BI.

    Pour faire quoi que ce soit avec Power BI et [!INCLUDE[prodshort](includes/prodshort.md)], que vous soyez administrateur ou simple consommateur, vous aurez besoin d’un compte de service Power BI. Pour créer un compte, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Pour vous inscrire à un compte, utilisez votre adresse e-mail professionnelle et votre mot de passe. L’inscription nécessite que vous ayez une licence, mais dans la plupart des cas, vous devriez déjà avoir une licence gratuite. Pour plus d’informations, reportez-vous à la rubrique [Gestion des licences Power BI](admin-powerbi-setup.md#license).

4. Si vous souhaitez créer vos propres états Power BI, obtenez Power BI Desktop.

    Vous pouvez télécharger [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Pour plus d’informations, reportez-vous à la rubrique [Obtenir Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Power BI pour les consommateurs](/power-bi/consumer/end-user-consumer)  
[Le « nouveau look » du service Power BI](/power-bi/service-new-look)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentation Power BI](/power-bi/)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
