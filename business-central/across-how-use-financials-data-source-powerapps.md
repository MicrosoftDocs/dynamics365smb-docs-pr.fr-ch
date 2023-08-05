---
title: Utilisez vos données pour créer une application | Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer une application métier à l’aide de Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# Connexion à vos données Business Central pour générer un application professionnelle à l’aide de Power Apps

Vous pouvez rendre vos données [!INCLUDE[prod_short](includes/prod_short.md)] disponibles sous forme de source de données dans Power Apps.  

> [!TIP]  
> Business Central propose désormais une assistance au développement et aux opérations pour Power Platform dans AL-Go et des exemples pour vous aider à créer vos propres applications Power Apps. Ces fonctionnalités sont actuellement en version préliminaire. Pour en savoir plus, accédez à [Business Central et Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) dans l’aide aux développeurs et aux professionnels de l’informatique.

## Conditions préalables

Vous devez disposer d’un compte valide avec [!INCLUDE[prod_short](includes/prod_short.md)] et avec Power Apps.  

## Ajouter [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power Apps

Ces étapes ajoutent une table Business Central, comme des clients ou des articles, comme source de données d’une Power Apps application.

1. Dans votre navigateur, accédez à [powerapps.microsoft.com](https://powerapps.microsoft.com/), puis connectez-vous.
2. Dans le volet de navigation sur le côté gauche, sélectionnez **+ Créer**, puis sélectionnez **Plus de sources de données** sur le **Créer une application** .
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. Les **Connexions** la liste affiche toutes les connexions de données existantes dont vous disposez.

   - S’il existe déjà une connexion **Business Central**, sélectionnez-la, puis sélectionnez **Créer**.

   - Si vous ne voyez pas de connexion Business Central, sélectionnez **+ Nouvelle connexion**, recherchez et sélectionnez **Business Central**, puis sélectionnez **Créer**.

   > [!NOTE]
   > Si vous souhaitez vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous devez choisir le connecteur **Business Central (sur site)**.  
  
4. Power Apps se connecte à votre [!INCLUDE[prod_short](includes/prod_short.md)]. Connectez-vous avec le nom du compte et le mot de passe Business Central. Si vous n’êtes pas un administrateur de votre [!INCLUDE[prod_short](includes/prod_short.md)], vous devrez peut-être vous connecter avec un autre compte.  
5. Après avoir signé, Power Apps affiche une liste *Environnements et des sociétés* disponibles à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Choisissez l’environnement et la société contenant les données auxquelles vous souhaitez vous connecter, comme *PRODUCTION - Ma société*.  
6. Ensuite, une liste de tables qui sont exposées dans le cadre de l’API pour votre environnement vous sera présentée. Sélectionnez la table à laquelle vous souhaitez vous connecter, puis choisissez **Connecter**.

Ces tables sont exposées en tant que points de terminaison par le connecteur [!INCLUDE[prod_short](includes/prod_short.md)] pour Power Apps.  

> [!NOTE]
> Si vous souhaitez inclure des données d’autres tables dans [!INCLUDE[prod_short](includes/prod_short.md)] dans votre application, vous devez travailler avec un développeur pour définir une API personnalisée dans [!INCLUDE[prod_short](includes/prod_short.md)].  

À ce stade, vous êtes connecté à vos données [!INCLUDE[prod_short](includes/prod_short.md)] et vous êtes prêt à générer votre application Power App. Vous pouvez toujours ajouter des écrans supplémentaires et vous connecter à des données supplémentaires. Pour en savoir plus, voir [Créer une application de canevas à partir d’un exemple dans Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Lorsque vous avez conçu et créé votre application, vous pouvez la partager avec vos collègues. Pour plus d’informations, voir [Enregistrer et publier une application de canevas dans Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## Voir la [formation Microsoft](/training/paths/power-apps-power-automate-business-central/) associée

## Voir aussi

[Créer une application de canevas à partir d’un modèle dans Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Familiarisation avec le développement d’applications connectées pour Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
