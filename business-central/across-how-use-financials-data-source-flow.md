---
title: Utiliser les flux Power Automate dans Business Central
description: Configurez et utilisez les flux Power Automate pour créer ou modifier les données Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 10/10/2022
ms.custom: bap-template
---
# Utiliser les flux Power Automate dans [!INCLUDE[prod_short](includes/prod_short.md)]

Avec [!INCLUDE[prod_short](includes/prod_short.md)], vous obtenez une licence de Microsoft Power Automate. Cette licence vous permet d’utiliser vos données [!INCLUDE[prod_short](includes/prod_short.md)] dans le cadre d’un flux de travail dans Microsoft Power Automate. Vous créez des flux personnalisés et vous vous connectez à vos données dans des sources internes et externes à l’aide du connecteur [!INCLUDE [prod_short](includes/prod_short.md)].

Les flux Power Automate sont déclenchés par des événements, comme un enregistrement a été créé, modifié ou supprimé. Ils peuvent également être exécutés selon une planification définie par l’utilisateur ou à la demande.

> [!NOTE]
> Les administrateurs peuvent restreindre l’accès à Power Automate. Si vous vous rendez compte que vous avez du mal à accéder à tout ou partie des fonctionnalités décrites dans cet article, Adressez-vous à un administrateur. Si vous voulez apprendre à contrôler l’accès à Power Automate en tant qu’administrateur, voir [Configuration de l’intégration de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Outre Power Automate, vous pouvez utiliser les modèles de flux de travail approbation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Bien qu’il existe deux systèmes de flux de travail distincts, tous les modèles de flux de travail approbation que vous créez dans Power Automate sont ajoutés à la liste des flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. En savoir plus sur [Flux de travail](across-workflow.md).

## À propos des flux Power Automate

Power Automate est un service qui vous aide à créer des workflows (ou flux) automatisés entre vos applications et services comme [!INCLUDE[prod_short](includes/prod_short.md)]. Les flux Power Automate nécessitent peu ou pas de connaissances en codage. Ils peuvent être associés à une grande variété d’événements et de réponses, notamment :

- Modifications d’enregistrement
- Mises à jour des fichiers externes
- Documents validés
- Différents services Microsoft et tiers, comme Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps, etc.

Trois types distincts de flux de cloud que vous pouvez utiliser :

|Type de flux|Désignation|
|---------|-----------|
|Automatisé|Ce type de flux est exécuté automatiquement par un événement. Dans [!INCLUDE[prod_short](includes/prod_short.md)], un événement peut être la création, la modification ou la suppression d’un enregistrement ou d’un document. Par exemple, une nouvelle facture vente peut déclencher un flux pour un requête d’approbation, qui peut se composer de différents ensembles d’événements selon la réponse de l’approbateur. Une réponse négative envoie une notification et un e-mail au demandeur d’approbation. Une réponse positive met simultanément à jour une feuille de calcul Excel située dans un dossier SharePoint et envoie une mise à jour à une conversation Teams. Les flux automatisés peuvent être démarrés par des événements internes et externes dans [!INCLUDE[prod_short](includes/prod_short.md)].|
|Planifié|Ce type de flux est également exécuté automatiquement mais il s’exécute régulièrement à une date et heure planifiées. |
|Instantané |Ce type de flux est exécuté à la demande. L’utilisateur doit l’exécuter manuellement à l’aide d‘un bouton ou d’une action dans une autre application ou un autre appareil. Dans ce cas, le client [!INCLUDE[prod_short](includes/prod_short.md)]. Les flux instantanés fonctionnent de la même manière que les raccourcis par lots, effectuant plusieurs étapes longues en appuyant sur quelques boutons et sont lancés à partir de pages ou de tableaux spécifiques. Par exemple, un flux peut ajouter un bouton au menu d’action sur la page **Fournisseurs** pour bloquer les paiements à un fournisseur et, en même temps, envoyer des e-mails personnalisables au contact du fournisseur et aux acheteurs de votre entreprise ainsi que mettre à jour le contact dans Outlook. |

## Fonctionnalités Power Automate

Vous pouvez explorer les flux Power Automate disponibles actuellement pour vous en vous connectant à [Power Automate](https://powerautomate.com) et en sélectionnant **Mes flux** sur la barre de navigation à gauche. Vous trouverez des flux que vous avez créés vous-même et les flux partagés avec vous par un administrateur ou un collègue.

- Les flux instantanés sont également disponibles pour s’exécuter directement à partir de la plupart des pages de liste, de fiche et de document dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous trouverez les flux instantanés dans le groupe d’actions **Automatiser** dans la barre d’action des pages. Pour exécuter un flux, sélectionnez-le et suivez les instructions qui vous sont présentées. En savoir plus sur les sections suivantes.
 
- Avec les flux automatisés dans [!INCLUDE[prod_short](includes/prod_short.md)], vous n’avez rien à faire, sauf si vous voulez les changer ou les désactiver. Sinon ils ne fonctionneront qu’une fois déclenchés. 
<!--

## Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## Exécuter des flux instantanés

Les flux instantanés s’ouvrent dans [!INCLUDE [prod_short](includes/prod_short.md)] Online pour pouvoir conserver le contexte du processus métier dans lequel vous travailliez. Vous ne pouvez pas exécuter de flux instantané de la plupart des listes, cartes ou documents.

1. Dans la barre d’actions, sélectionnez **Automatiser**, puis sélectionnez un flux dans les la liste des flux disponibles sous l’action **Power Automate**

    :::image type="content" source="media/power-automate-action-intro.png" alt-text="Affiche l’action Automatiser dans la barre d’actions avec les actions développée.":::

    Sur certaines pages, **Automatiser** est imbriqué sous **Plus d’options (...)**. 
2. Sur le volet **Exécuter le flux**, complétez les champs obligatoires, puis sélectionnez **Continuer** pour exécuter le flux.

> [!NOTE]
> La première fois que vous utilisez l’élément **Automatiser**, vous pouvez ne voir que l’action **Mise en route de Power Automate**. Vous voyez cette action, car vous n’avez pas approuvé la déclaration de confidentialité pour Microsoft Power Automate. Pour continuer, sélectionnez **Déclaration de confidentialité de Power Automate** et suivez les instructions pour approuver ou désapprouver.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Affiche l’élément Automatiser dans la barre d’actions.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## Créez, modifier et gérer les flux

La création de nouveaux flux, la modification et la gestion des flux existants (comme les activer ou les désactiver) peuvent effectués directement dans Power Automate. Mais vous pouvez initier certaines de ces tâches depuis l’intérieur de [!INCLUDE[prod_short](includes/prod_short.md)] :

- Pour créer un flux instantané à partir d’une liste, carte ou une page de document, sélectionnez **Automatiser** > **Créer un flux**.
- Pour ouvrir Power Automate à partir d’une liste, carte ou une page de document, sélectionnez **Automatiser** > **Gérer des flux**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Ces tâches sont généralement effectuées par un administrateur ou un super utilisateur. Les tâches nécessitent des connaissances élargies des processus métier dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour en savoir plus, explorez [Intégration de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview), [Configurer des flux instantanés](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) et [Gérer les flux Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows).
<!-- 

## Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## Voir la [formation Microsoft](/training/modules/use-power-automate/) associée

## Voir aussi

[Dépanner les flux de travail automatisés [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Se préparer aux activités commerciales](ui-get-ready-business.md)  
[Flux de travail](across-workflow.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Configurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finances](finance.md)  
[Gérer les flux Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Activer les flux instantanés](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
m