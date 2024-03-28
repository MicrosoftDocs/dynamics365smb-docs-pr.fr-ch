---
title: "Introduction à Microsoft\_Fabric et Business\_Central"
description: "Obtenez une vue d’ensemble de l’utilisation de Microsoft\_Fabric pour obtenir des informations, des informations décisionnelles et des indicateurs de performance clés à partir de vos données Business\_Central."
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 10/10/2023
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Introduction à Microsoft Fabric et Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] est une solution d’analyse de bout en bout dotée de fonctionnalités complètes incluant le mouvement des données, les lacs de données, l’ingénierie des données, l’intégration des données, la science des données, l’analyse en temps réel et la business intelligence&mdash;le tout soutenu par un plate-forme offrant une sécurité, une gouvernance et une conformité des données robustes. Votre organisation n’a plus besoin de regrouper les services d’analyse individuels de plusieurs fournisseurs. Utilisez plutôt une solution rationalisée, facile à connecter, à intégrer et à utiliser.

> [!NOTE]
> [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] est actuellement en version préliminaire. Pour plus d’informations sur le plan de versions Microsoft Fabric, voir [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> La publication régulière de cette feuille de route vous aidera à rester informé de la façon dont [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] répondra à vos besoins.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Où [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] s’intègre aux analyses [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_short](includes/prod_short.md)] est livré avec de nombreux rapports et fonctionnalités d’analyse de données prêts à l’emploi tels que les rapports financiers, ouverts dans Excel et le mode d’analyse sur les listes et les requêtes. En plus de cela, il est facile de définir des rapports Power BI qui lisent les données des API standard et personnalisées, définissent les tableaux de bord de mesures Power BI, et intègrent tous ces éléments directement dans le client [!INCLUDE[prod_short](includes/prod_short.md)]. Mais pour les clients ayant des scénarios de science des données ou de business intelligence plus avancés qui nécessitent une ingénierie ou une intégration de données plus riche, [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] pourrait être une bonne option. 

## <a name="onelake"></a>OneLake

Un élément clé de l’offre [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] est OneLake. OneLake est un lac de données unique, unifié et logique pour l’ensemble de l’organisation. Vous pouvez considérer OneLake comme le OneDrive pour les données. Il vous fournit un lac de données en tant que service sans avoir à le créer vous-même. OneLake est livré automatiquement avec chaque client [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] sans infrastructure à gérer. Toutes les données, qui atterrissent dans OneLake, participent automatiquement à une gouvernance des données prête à l’emploi, telle que le traçage des données, la protection des données, la certification et l’intégration du catalogue. Il répartit les silos de données en permettant aux différentes parties de l’organisation de travailler de manière indépendante tout en contribuant au même lac de données.

Les éléments [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] stockent vos données dans OneLake dans un format de fichier ouvert. Pour les données tabulaires structurées, ce format est *delta parquet*. Le format Delta Parquet permet à chaque moteur d’analyse de [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] d’accéder aux données d’autres moteurs d’analyse. De cette façon, cela permet aux praticiens des données d’utiliser les outils de votre choix.

> [!NOTE]
> Nous nous attendons à ce qu’avec l’une de nos futures versions, [!INCLUDE[prod_short](includes/prod_short.md)] les données seront également mises à disposition dans OneLake pour les clients qui utilisent à la fois [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] et [!INCLUDE[prod_short](includes/prod_short.md)] et ont des exigences uniques dans les domaines que [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] prend en charge. Le calendrier dépend du calendrier de disponibilité générale de [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] et ses composants requis pour permettre cette expérience. Nous allons mettre à jour cet article avec une chronologie plus précise, une fois que nous en saurons plus.

## <a name="see-also"></a>Voir aussi
[Utilisation de Power BI avec Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
