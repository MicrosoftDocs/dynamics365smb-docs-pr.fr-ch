---
title: Utiliser les flux Power Automate dans Business Central
description: Configurez et utilisez les flux Power Automate pour créer ou modifier les données Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 369ee2b4aded272a8a3a21fe810b4b6c62dd1de0
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585506"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Utiliser les flux Power Automate dans [!INCLUDE[prod_short](includes/prod_short.md)]

Vous pouvez utiliser vos données [!INCLUDE[prod_short](includes/prod_short.md)] en tant que partie du flux de travail dans Microsoft Power Automate. Créez vos propres flux et connectez-vous à vos données depuis des sources internes et externes avec le connecteur [!INCLUDE [prod_short](includes/prod_short.md)].

> [!NOTE]
> Vous devez disposer d’un compte valide avec [!INCLUDE[prod_short](includes/prod_short.md)] et Power Automate.  

> [!TIP]
> Outre Power Automate, vous pouvez utiliser les modèles de flux de travail approbation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Bien qu’il existe deux systèmes de flux de travail distincts, tous les modèles de flux de travail approbation que vous créez dans Power Automate sont ajoutés à la liste des flux de travail dans [!INCLUDE[prod_short](includes/prod_short.md)]. En savoir plus sur [Flux de travail](across-workflow.md).

Les flux Power Automate sont déclenchés par des événements tels que la création, la modification ou la suppression d’enregistrements et de documents (flux automatisés). Les flux peuvent également s’exécuter selon une planification définie par l’utilisateur (flux planifiés) ou à la demande (flux instantanés).

## <a name="power-automate-features-in-prod_short"></a>Fonctionnalités Power Automate dans [!INCLUDE[prod_short](includes/prod_short.md)]

Les flux étendent les fonctionnalités d’approbation intégrées disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)] sans connaissances en codage particulières, et peuvent être associés à une vaste plage d’événements et de réponses, tels que des modifications d’enregistrement, des mises à jour de fichiers externes, des documents validés, ainsi que différents services Microsoft et tiers tels que Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps, etc.

Ainsi, par exemple, une nouvelle facture de vente peut déclencher un flux de travail pour une demande d’approbation, qui peut avoir différents événements définis en fonction de la réponse de l’approbateur. Une réponse négative envoie une notification et un e-mail au demandeur d’approbation. Une réponse positive met simultanément à jour une feuille de calcul Excel située dans un dossier SharePoint et envoie une mise à jour à une conversation Teams.

Les flux instantanés fonctionnent de la même manière que les raccourcis par lots, effectuant plusieurs étapes longues en appuyant sur quelques boutons et sont lancés à partir de pages ou de tableaux spécifiques. Par exemple, un flux peut ajouter un bouton au menu d’action sur la page **Fournisseurs** pour bloquer les paiements à un fournisseur et, en même temps, envoyer des e-mails personnalisables au contact du fournisseur et aux acheteurs de votre entreprise ainsi que mettre à jour le contact dans Outlook.

## <a name="automated-workflows"></a>Flux de travail automatisés

Avec Power Automate, vous pouvez créer des flux métiers directement en interne et vous appuyer sur des développeurs citoyens. Les flux de travail automatisés peuvent être lancés par des événements internes et externes dans [!INCLUDE[prod_short](includes/prod_short.md)], et également être configurés pour s’exécuter périodiquement. En savoir plus et obtenir des instructions sur la façon de créer des flux de travail dans l’article [Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) dans le contenu de l’administration.

## <a name="instant-flows"></a>Flux instantanés

À compter de la 1ère vague de lancement 2022 (mai 2022), les administrateurs de [!INCLUDE [prod_short](includes/prod_short.md)] en ligne peuvent [activer une fonctionnalité](admin-feature-management.md) pour permettre d’exécuter un flux Power Automate de la plupart des pages de liste, fiche et document. Pour plus d’informations, voir [Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) dans le contenu d’administration.

Une fois l’administrateur connecté à [!INCLUDE [prod_short](includes/prod_short.md)] avec Power Automate, vous affichez tous les flux ajoutés par votre organisation lorsque vous sélectionnez l’action **Automatiser** dans les pages concernées. Les flux instantanés sont exécutés sans quitter [!INCLUDE [prod_short](includes/prod_short.md)].

Ces flux de travail instantanés s’ouvrent sur une page dans [!INCLUDE [prod_short](includes/prod_short.md)] en ligne afin que vous restiez dans le contexte du processus métier dans lequel vous vous trouviez. Sélectionnez l’action **Automatiser** sur certaines pages imbriquées sous le menu **Plus d’options**, trouvez-la, sélectionnez l’élément de menu **Power Automate**, puis sélectionnez le lien approprié pour déclencher le flux de travail. La connexion à Power Automate est déjà configurée pour vous.

La plupart des flux vous demandent de remplir un champ ou deux avant de sélectionner l’action **Exécuter le flux**.

> [!TIP]
> Si vous n’affichez pas l’action **Automatiser**, il est possible que [!INCLUDE [prod_short](includes/prod_short.md)] ne soit pas encore configuré pour utiliser Power Automate. En savoir plus auprès de votre administrateur.

## <a name="add-more-automated-flows-and-instant-flows"></a>Ajouter plus de flux automatisés et de flux instantanés

Vous pouvez créer des flux sur le site Web [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Toutefois, si votre administrateur a activé la possibilité d’exécuter les flux Power Automate depuis [!INCLUDE [prod_short](includes/prod_short.md)] en ligne, vous pouvez démarrer le processus de création d’un flux à partir de l’action **Automatiser** sur les pages correspondantes, qui se trouvent sous le menu **Autres options** selon la page. Puis sélectionnez l’élément du menu **Power Automate**, puis sélectionnez l’action **Créer un flux**. Power Automate s’ouvre alors dans un nouvel onglet du navigateur et vous êtes automatiquement connecté.

Vous pouvez trouver des exemples de modèles à adapter à votre entreprise et à tous les événements déclencheurs disponibles, en utilisant à la fois [!INCLUDE [prod_short](includes/prod_short.md)] et des outils externes, en choisissant le menu **Connecteurs** sur le site web Power Automate. Pour plus d’informations sur les modèles et déclencheurs disponibles, voir [Configurer des flux de travail automatisés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) dans le contenu d’administration.

## <a name="manage-automated-workflows"></a>Gérer les flux de travail automatisés

Vous pouvez créer des flux ou gérer des flux Power Automate existants dans [!INCLUDE [prod_short](includes/prod_short.md)] sur la page **Gérer les flux Power Automate**. Pour plus d’informations, voir [Gérer les flux Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows.md) dans le contenu d’administration.

Vous pouvez également gérer les flux de travail Power Automate disponibles sur la page **Flux de travail** dans [!INCLUDE[prod_short](includes/prod_short.md)]. La page répertorie à la fois l’approbation intégrée et les flux de travail Power Automate, avec des options permettant à ces derniers d’activer/désactiver, de supprimer et d’afficher le flux de travail sur le site web Power Automate.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/use-power-automate/) associée

## <a name="see-also"></a>Voir aussi

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
