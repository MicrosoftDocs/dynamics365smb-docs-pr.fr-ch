---
title: Configurer une société avec RapidStart Services
description: Vous pouvez configurer une nouvelle société dans Business Central avec RapidStart Services pour améliorer la productivité en automatisant et en simplifiant les tâches récurrentes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518326"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Configurer une société avec RapidStart Services

Vous pouvez configurer une nouvelle société dans [!INCLUDE[prod_short](includes/prod_short.md)] avec RapidStart Services, qui est un outil conçu pour réduire les temps de déploiement, améliorer la qualité de l’implémentation, présenter une approche reproductible des implémentations et augmenter la productivité en automatisant et en simplifiant des tâches récurrentes.  

Utilisez ces fonctionnalités pour faire évoluer votre entreprise en tant que revendeur. La plupart des pages pertinentes s’appliquent à [!INCLUDE [prod_short](includes/prod_short.md)] Online et sur site. Cependant, certains processus reposent sur l’accès à des fichiers sur disque et sont trop complexes à utiliser pour [!INCLUDE [prod_short](includes/prod_short.md)] Online. Pour [!INCLUDE [prod_short](includes/prod_short.md)] sur site, vous souhaiterez probablement utiliser Windows PowerShell pour vous aider à déployer. Pour plus d’informations, voir [Administration de Business Central sur site](/dynamics365/business-central/dev-itpro/administration/administration) et [Administration de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration), respectivement.  

RapidStart Services permet d’obtenir une vue d’ensemble du processus de configuration de votre nouvelle société grâce à une feuille dans laquelle vous pouvez configurer les tables souvent impliquées dans le processus de configuration de nouvelles sociétés. Comme vous effectuez cela, vous pouvez créer un questionnaire pour guider vos clients par le biais de la collecte des informations de configuration. Les clients peuvent choisir d’utiliser le questionnaire pour configurer des modules ou d’ouvrir la page de configuration directement et d’y effectuer la configuration. Chose plus importante, RapidStart Services vous aide, en tant que client, à mettre en place la société à l’aide de données de configuration par défaut que vous pouvez ajuster et personnaliser. Pour terminer, lorsque vous utilisez RapidStart Services, vous pouvez configurer et migrer les données des clients existants, par exemple la liste des clients ou des articles, vers la nouvelle société.

Vous pouvez utiliser les composants suivants pour accélérer la configuration de votre société :  

- Assistant Configuration  
- Feuille configuration  
- Packages configuration  
- Modèles de configuration  
- Questionnaire de configuration  

> [!Note]  
> Vous devez configurer manuellement d’autres zones de [!INCLUDE[prod_short](includes/prod_short.md)]. Celles-ci incluent l’ajout d’utilisateurs, la configuration de périodes comptables et la configuration d’axes analytiques pour la veille économique. Pour plus d’informations, reportez-vous à [Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|**Pour**|**Voir**|  
|------------|-------------|  
|Créer une société et importer les données de configuration et les modèles de base.|[Configurer une société](admin-set-up-company-configuration.md)|  
|Déployer le package configuré vers votre client pour l’implémentation.|[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)|
|Définir et valider les valeurs de configuration de votre client pour toutes les zones de base, telles que les informations sur la société, la comptabilité, le stock, les ventes ou la fabrication.|[Collecter les valeurs de configuration client](admin-gather-customer-setup-values.md)|  
|Configurer les enregistrements de données de base à l’aide de modèles pour préparer la migration des données client existantes.|[Préparer la migration des données client](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Définir les tables et les champs, valider les données client existantes et migrer les données vers la base de données [!INCLUDE[prod_short](includes/prod_short.md)].|[Migrer des données client](admin-migrate-customer-data.md)|
|Se préparer à réutiliser les configurations de la société dans d’autres sociétés (dans le contenu pour développeurs et administrateurs).|[Créer des packages configuration de société personnalisés](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Rechercher des solutions aux problèmes connus dans le kit d’outils RapidStart Services.|[Conseils : RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Voir aussi

[Administration](admin-setup-and-administration.md)  
[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Configurer des domaines d’application complexes à l’aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]