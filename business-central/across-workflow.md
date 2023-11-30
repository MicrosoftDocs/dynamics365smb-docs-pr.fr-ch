---
title: Flux de travail dans Dynamics 365 Business Central
description: Utilisez les fonctionnalités de flux de travail intégrées pour configurer des flux de travail approbation afin de compléter les flux de travail automatisés basés sur Power Automate. Vous pouvez configurer des étapes pour affecter des tâches à différentes personnes dans le cadre des différentes tâches de processus métier.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flux de travail dans Dynamics 365 Business Central

Vous pouvez configurer et utiliser des flux de travail qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches système, telles que la validation automatique, peuvent être incluses en tant qu’étapes dans les workflows. Les tâches système peuvent être précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.

La version par défaut de [!INCLUDE [prod_short](includes/prod_short.md)] prend en charge ces types de flux de travail :
  
* Flux Power Automate

  * Les flux automatisés qui sont déclenchés par des événements (tels que la création, la modification ou la suppression d’enregistrements ou de documents) dans [!INCLUDE[prod_short](includes/prod_short.md)]. Sont également inclus les flux d’approbation créés dans Power Automate qui se déclenchent quand une approbation est demandée dans [!INCLUDE[prod_short](includes/prod_short.md)].
  * Les flux instantanés déclenchés manuellement à partir du menu d’action **Automatiser** dans les listes, fiches et pages de document.

    Créez et déclenchez manuellement un flux Power Automate sur un enregistrement [!INCLUDE[prod_short](includes/prod_short.md)], tel qu’un client, un article ou une commande client, avec des options pour manipuler les informations à la fois en interne et en externe (à l’aide d’outils intégrés).

* Les flux de travail approbation basés sur des modèles de flux de travail intégrés

  Dans la page **Modèles flux de travail**, vous affichez tous les flux de travail disponibles. La version d’essai de [!INCLUDE[prod_short](includes/prod_short.md)] inclut plusieurs flux de travail préconfigurés, représentés par des modèles de flux de travail que vous pouvez copier pour créer des flux de travail. Lorsque vous ouvrez un modèle de flux de travail depuis la page **Modèles flux de travail** et que le nom du flux de travail commence par *MS-*, le modèle de flux de travail est ajouté par Microsoft.

## <a name="power-automate-flows"></a>Flux Power Automate

Avec [!INCLUDE [prod_short](includes/prod_short.md)] Online, vous pouvez vous inscrire à Power Automate pour créer de puissants workflows automatisés. Vous exécutez ces workflows depuis l’intérieur de [!INCLUDE [prod_short](includes/prod_short.md)]. Les flux peuvent se connecter aux sources de données internes et externes et les outils, sans connaissances en matière de codage.

|**Pour** |**Voir**|
|-------|-------|
|Mise en route avec Power Automate, création de flux et exécution de flux instantanés|[Utiliser les flux Power Automate dans [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Découvrez comment créer, modifier et gérer des flux|[Configuration de flux automatisés et de flux instantanés](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) et [Configuration de flux instantanés](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Configuration de l’intégration de Power Automate avec [!INCLUDE[prod_short](includes/prod_short.md)] pour les utilisateurs en tant qu’administrateurs|[Configuration de l’intégration de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## <a name="approval-workflows"></a>Flux de travail d’approbation

Créez un flux de travail approbation en définissant ce qui démarre le flux de travail et ce qui se passe ensuite, comme suit :

* Un événement de flux de travail, qui est modéré par les conditions de l’événement.
* Une réponse de flux de travail, qui est modérée par les options de réponse.

Pour définir les étapes de flux de travail, renseignez les champs des lignes de flux de travail à partir des valeurs d’événement et de réponse qui représentent les scénarios pris en charge.

Les exemples d’événements de flux de travail approbation incluent la création de bons de commande/devis/factures, les modifications de prix, les modifications de fournisseur ou de client, et plus encore.

[!INCLUDE[workflow](includes/workflow.md)]

| **Pour** | **Voir** |
|--|--|
| Configurer des utilisateurs du flux de travail approbation, spécifier comment les utilisateurs sont notifiés et créer des flux de travail. (Pour de nouveaux flux de travail pour des scénarios non pris en charge, implémentez les éléments requis du flux de travail en personnalisant le code d’application.) | [Configurer les flux de travail approbation](across-set-up-workflows.md) |
| Activer des flux de travail approbation, agir sur les notifications du flux de travail, notamment la demande et l’approbation d’une étape de flux de travail. Archiver et supprimer des workflows. | [Utilisation des flux de travail approbation](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Dépanner les flux de travail automatisés [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
