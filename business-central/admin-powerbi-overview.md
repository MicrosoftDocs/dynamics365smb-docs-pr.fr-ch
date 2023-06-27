---
title: "Vue d’ensemble Architecture et composant d’intégration Power BI pour Business\_Central| Microsoft Docs"
description: "En savoir plus sur les différents aspects de l′intégration Power BI avec Business\_Central."
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="power-bi-integration-component-and-architecture-overview-for-" />Vue d’ensemble Architecture et composant d’intégration Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)]

Dans cet article, vous découvrirez les différents aspects de l’intégration de Power BI à [!INCLUDE[prod_short](includes/prod_short.md)] pour vous aider à comprendre sa mise en œuvre et son utilisation.

## <a name="components" />Composants

Le tableau suivant décrit les principaux composants impliqués dans l’intégration Power BI.

|Composant|Description|
|---------|-----------|
|Power BI|Un service d’hébergement et de gestion des états basé sur le cloud.|
|Power BI Desktop|Un outil de création pour créer des états et des tableaux de bord, et vous permet d’exécuter des états. Il est disponible en téléchargement gratuit sur Microsoft Store et est installé localement.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Solution en ligne ou sur site avec des connecteurs exposés à Power BI et possibilité d’intégrer une partie de Power BI.|

## <a name="whats-available-from-the-start" />Ce qui est disponible dès le départ

Le tableau suivant décrit les fonctionnalités disponibles.

|Fonctionnalité|Support [!INCLUDE[prod_short](includes/prod_short.md)] en ligne ou sur site|
|-------|---------------------|
|Connecteurs Power BI|Les deux. Différents connecteurs pour la solution ligne et la solution sur site. Connecteur identique utilisé pour le service Power BI Desktop et Power BI |
|Expérience intégrée pour afficher un état donné dans un Récapitulatif dans [!INCLUDE[prod_short](includes/prod_short.md)]|Les deux. Nécessite une configuration pour afficher les états sur site.|
|Gestion des états Power BI depuis [!INCLUDE[prod_short](includes/prod_short.md)]|En ligne|
|États Power BI par défaut sur les tableaux de bord déployés vers Power BI|En ligne|
|Applications Power BI sur Microsoft AppSource|En ligne|

## <a name="architecture" />Architecture

[!INCLUDE[prod_short](includes/prod_short.md)] s’intègre à Power BI via un connecteur utilisant OData. La source de données pour les états Power BI est exposée comme les pages API et les services Web OData.

:::image type="content" source="./media/power-bi-architecture.png" alt-text="Texte de remplacement de l’image." lightbox="./media/power-bi-architecture.png":::

À partir de février 2022, les états Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)] Online proviennent d’une réplique de base de données secondaire en lecture seule. La réplique de la base de données fait partie de la capacité [échelle horizontale en lecture](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) dans [!INCLUDE[prod_short](includes/prod_short.md)] Online. Cette configuration libère la base de données principale pour les transactions, ce qui améliore les performances du système. La connexion à la réplique de la base de données en lecture seule fait partie intégrante du connecteur Business Central Online et ne nécessite aucune configuration supplémentaire de votre part. Tous les nouveaux rapports se connecteront par défaut au réplica de base de données en lecture seule. Les anciens rapports utiliseront toujours la base de données principale. Pour plus d’informations, voir [Plan de la 2e vague de lancement 2021 pour Business Central](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## <a name="general-flow" />Flux général

Le diagramme suivant illustre le flux de travail de base pour les utilisateurs lors de la connexion de [!INCLUDE[prod_short](includes/prod_short.md)] à Power BI.

![Flux de travai Power BI pour l’intégration avec Business Central.](./media/power-bi-flow.png)

1. L’utilisateur s’inscrit à un compte Power BI.
2. L’utilisateur se connecte à Power BI depuis [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie la licence.
4. [!INCLUDE[prod_short](includes/prod_short.md)] déploie les états par défaut sur le service Power BI. Cette étape ne se produit que pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne.
5. [!INCLUDE[prod_short](includes/prod_short.md)] rend les états dans Power BI disponibles pour la sélection dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les états par défaut sont automatiquement affichés dans des parties de Power BI.
6. L’utilisateur crée un état dans Power BI Desktop.
7. L’utilisateur publie l’état vers le service Power BI. Les états sont ensuite disponibles pour la sélection dans [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Power BI pour les consommateurs](/power-bi/consumer/end-user-consumer)  
[Le « nouveau look » du service Power BI](/power-bi/service-new-look)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentation Power BI](/power-bi/)  
[Veille économique](bi.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
