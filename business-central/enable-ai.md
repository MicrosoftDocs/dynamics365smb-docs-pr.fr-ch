---
title: Configurer les capacités Copilot et IA
description: Cet article explique comment activer Copilot sur un environnement.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
---

# Configuration des fonctionnalités de Copilot et d’IA 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Cet article explique comment contrôler Copilot et d’autres fonctionnalités de l’IA dans Business Central. Cette tâche est effectuée par un administrateur. Copilot est une fonctionnalité système et fait partie intégrante de Business Central. Comme pour la plupart des fonctionnalités du système, vous n’accordez pas l’accès à des utilisateurs individuels et vous ne pouvez pas non plus activer ou désactiver Copilot. Cependant, Copilot offre des contrôles de gouvernance des données et la possibilité de désactiver les capacités individuelles de Copilot et d’IA pour chaque environnement. Il existe différents niveaux de contrôle d’accès aux fonctionnalités d’IA, en fonction de la fonctionnalité :

- Autoriser le mouvement des données entre les régions géographiques

  Cette tâche n’est requise que si votre environnement Business Central se trouve dans une zone géographique autre que celle qu’Azure OpenAI Service utilise. [en savoir plus](#allow-data-movement-across-geographies)

- Activez la fonctionnalité sur la page **Fonctionnalités de Copilot et de l’IA**. [en savoir plus](#activate-features)

- Activez la fonctionnalité spécifique, si elle est toujours régie par la **Gestion des fonctionnalités**.

  Dans la 2e vague de lancement 2023, les suggestions de textes marketing et les fonctionnalités d’aide au rapprochement des comptes bancaires sont incluses dans la **Gestion des fonctionnalités**. [en savoir plus](#enable-feature-in-feature-management)

Si l’une de ces conditions n’est pas remplie, la fonctionnalité ne peut pas être utilisée.

## Conditions préalables

- Vous utilisez Business Central Online, version 23.1 ou ultérieure. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Vous disposez des autorisations d’administrateur ou de super autorisations dans Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Autoriser le déplacement des données entre les zones géographiques

Cette tâche s’applique uniquement si le commutateur **Autoriser le mouvement des données** s’affiche en haut de l’écran **Fonctionnalités de Copilot et de l’IA**. Le commutateur **Autoriser le déplacement des données** indique que l’emplacement de votre environnement Business Central&mdash;c’est-à-dire la région où les données sont traitées et stockées&mdash;n’est pas la même que la région d’Azure OpenAI Service utilisée par Copilot. Si vous souhaitez activer Copilot, vous devez autoriser le déplacement des données entre les régions. Pour en savoir plus sur le déplacement des données, consultez [Déplacement des données Copilot entre régions](ai-copilot-data-movement.md). 

Pour autoriser le déplacement des données en dehors de votre région géographique, procédez comme suit :

1. Dans Business Central, recherchez et ouvrez la page **Fonctionnalités Copilot et de l’IA**.
1. Activez le commutateur **Autoriser le déplacement des données**.

   ![![Texte de remplacement](allow-data-movement.png)](allow-data-movement.png)

Vous pouvez désactiver l’option en désactivant le commutateur **Autoriser le déplacement des données**. Une fois qu’un Azure OpenAI Service est disponible dans la région de votre environnement Business Central, votre environnement y est automatiquement connecté et le commutateur n’est plus disponible. 


<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## Activer les fonctionnalités

Toutes les fonctionnalités de Copilot et d’IA sont actives par défaut lorsqu’elles sont mises à disposition en avant-première ou lorsqu’elles deviennent généralement disponibles. Via la page **Fonctionnalités de Copilot et de l’IA**, vous pouvez désactiver ou réactiver des fonctionnalités individuelles pour tous les utilisateurs.

1. Dans Business Central, recherchez et ouvrez la page **Fonctionnalités Copilot et de l’IA**.

1. La page répertorie toutes les fonctionnalités disponibles liées à Copilot et à l’IA et leur état actuel, qui peut être actif ou inactif. Les fonctionnalités sont divisées en deux sections&mdash;une section pour les fonctionnalités en version préliminaire et une autre pour les fonctionnalités généralement disponibles. 

   [![Affiche le tableau de bord Business Central et la liste de contrôle pour Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Pour activer une fonctionnalité, sélectionnez-la dans la liste, puis sélectionnez l’action **Activer**.
   - Pour désactiver une fonctionnalité, sélectionnez-la, puis sélectionnez l’action **Désactiver**. 


## Activer la fonctionnalité dans la gestion des fonctionnalités

Lorsque des fonctionnalités Copilot individuelles sont publiées dans les mises à jour mineures de Business Central, ces fonctionnalités sont facultatives jusqu’à la prochaine mise à jour majeure. **Gestion des fonctionnalités** permet d’activer ou de désactiver les fonctionnalités en avant-première, telles que le rapprochement bancaire, ainsi que certaines fonctionnalités généralement disponibles, telles que les suggestions de texte marketing. [En savoir plus sur la gestion des fonctionnalités](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Dans Business Central, recherchez et ouvrez la page **Gestion des fonctionnalités**.
2. Pour activer une fonctionnalité, définissez la colonne **Activé pour** sur **Tous les utilisateurs**. Pour désactiver une fonctionnalité, définissez la colonne **Activé pour** sur **Aucun**. Utilisez le tableau suivant pour vous aider à déterminer le commutateur qui s’applique à la fonctionnalité Copilot et AO que vous souhaitez activer :

   - **Fonctionnalité en version préliminaire : rapprochement de compte bancaire avec Copilot** concerne la fonctionnalité d’aide au rapprochement des comptes bancaires.
   - **Version préliminaire de la fonctionnalité : Créer des descriptions de produits basées sur l’IA avec Copilot** concerne la fonctionnalité de suggestions de textes marketing.

   Pour plus d’informations sur la gestion des fonctionnalités en général, accédez à [Gestion des fonctionnalités](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Accorder l’accès utilisateur 

Les capacités Copilot et IA peuvent offrir des fonctionnalités destinées à tous les utilisateurs de votre organisation ou à des rôles d’utilisateur spécifiques. La plupart des fonctionnalités de Copilot et d’IA offrent un contrôle d’accès à l’aide d’autorisations et d’ensembles d’autorisations dans le système de gestion des autorisations de Business Central. [En savoir plus sur les autorisations et les ensembles d’autorisations](ui-define-granular-permissions.md).

Pour accorder ou refuser l’accès à des fonctionnalités Copilot et IA spécifiques, consultez la documentation ou l’éditeur de cette fonctionnalité pour identifier les autorisations requises. 

## Étapes suivantes

Après avoir activé et accepté les fonctionnalités, vous êtes prêt à les essayer. Accédez à :

- [Ajouter du texte marketing aux articles](item-marketing-text.md) 
- [Rapprocher à l’aide de l’assistant de rapprochement de compte bancaire](bank-reconciliation-with-copilot.md) 

## Voir aussi

[Résoudre les problèmes des fonctionnalités de Copilot et d’IA](ai-copilot-troubleshooting.md)  
[Vue d’ensemble des suggestions de texte marketing](ai-overview.md)   
[FAQ pour les suggestions de texte marketing](faqs-marketing-text.md)  
