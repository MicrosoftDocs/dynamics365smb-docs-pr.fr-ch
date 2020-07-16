---
title: Créer des sociétés en utilisant le guide de configuration assistée | Microsoft Docs
description: Il est facile de créer une nouvelle société vide dans Business Central. Un guide de configuration assistée vous aide à l'aide de procédures, et vous pouvez importer les données métier existantes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/03/2020
ms.author: edupont
ms.openlocfilehash: 4247b6c34fd086d22291408d1058cf8718841888
ms.sourcegitcommit: ca5bf1d934997ef8c0bc9f8ab0e5568f0ed42fa4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/06/2020
ms.locfileid: "3535299"
---
# <a name="creating-new-companies-in-d365fin"></a>Création de sociétés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le conteneur pour les données métier appartenant à une unité commerciale ou une entité juridique sont désignés en tant que *société*. Lorsque vous vous connectez à [!INCLUDE[d365fin](includes/d365fin_md.md)], une société de démonstration et une société vide vous sont attribuées, *Ma société*. Le basculement entre sociétés est facile : accédez simplement à **Mes paramètres** et passez à l'autre société. Vous pouvez également créer de nouvelles sociétés dans [!INCLUDE[d365fin](includes/d365fin_md.md)], selon les besoins de votre activité. Lorsque vous créez une société, un guide de configuration assistée vous permet d'obtenir les fondements de base. Ensuite, vous pouvez importer des données appropriées à partir de votre système hérité ou d'une autre société dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="creating-a-new-company"></a>Création d'une nouvelle société

Si vous décidez d'ajouter une société à votre [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez utiliser le guide de configuration assistée **Créer une nouvelle société** pour démarrer. L'assistant de configuration est disponible à partir de la page **Sociétés** et depuis la zone de recherche dans le champ **Société** de la page **Mes paramètres**.  

L'assistant de configuration propose trois modèles et une option vierge :

- **Évaluation - Exemples de données**  
    Cela crée une société qui est similaire à la société de démonstration avec des exemples de données et des données de configuration.  
- **Production - Données de configuration uniquement**  
    Cela crée une société qui est similaire à **Ma société** avec des données de configuration, mais sans exemples de données.
- **Évaluation avancée - Exemple de données complètes** Cela crée une société avec des données de configuration et des exemples de données complètes pour toutes les fonctions, y compris la production et la gestion des services.
- **Créer nouveau - Aucune donnée**  
    Cela crée une société vide sans données de configuration.  

Si vous souhaitez démarrer facilement avec une nouvelle société, sélectionnez **Production - Données de configuration uniquement**, puis importez vos propres données métier, telles que les clients, les articles et les fournisseurs. Choisissez le modèle **Nouveau** si vous souhaitez tout redéfinir à zéro. Dans ce cas, vous pouvez utiliser le guide de configuration assistée **Configuration de la société** pour vous aider à commencer par des données de configuration essentielles.  

> [!NOTE]  
> Lorsque vous créez une société, cela prend quelques minutes avant de pouvoir y accéder dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. L'état de configuration sur la page **Sociétés** s'affiche lorsque la nouvelle société est prête pour vous. Ensuite, vous pouvez basculer vers la nouvelle société en utilisant **Mes paramètres**.  

Au cours de votre période d'évaluation de 30 jours, vous pouvez créer autant de sociétés que vous voulez, mais elles ne seront disponibles que durant cette période d'évaluation. Pour plus d'informations, contactez votre partenaire [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="copying-a-company"></a>Copier une société

Sur la page **Sociétés**, vous pouvez utiliser l'action **Copier** pour créer une deuxième société sur la base du contenu d’une société existante. Ceci est utile, par exemple, lorsque vous souhaitez tester une société sans perturber les données de production.

> [!Important]
> Cette fonction ne peut pas être utilisée pour sauvegarder une société. La sauvegarde d'une société commence par l'exportation de la base de données sous la forme d'un fichier .bacpac. Pour plus d'informations, voir [Exportation de bases de données](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) dans Aide dédiée au développement et à l'administration.

## <a name="company-setup"></a>Configuration de la société

Lorsque vous vous connectez à une nouvelle société, l'Assistant **Configuration de la société** s'exécute automatiquement et vous permet de démarrer. Il vous sera demandé des informations sur votre activité, telles que l'adresse, les coordonnées bancaires et le mode d'évaluation du stock. Ces informations sont nécessaires parce qu'elles servent de base dans plusieurs zones de [!INCLUDE[d365fin](includes/d365fin_md.md)], ce qui vous évitera de les configurer manuellement plus tard.  

Par exemple, l'adresse de votre société est incluse dans les factures et autres documents, vos coordonnées bancaires sont utilisées pour les paiements, et le mode d'évaluation du stock est utilisé pour calculer les prix, ainsi que pour l'évaluation du stock.  

Une fois les bases en place, vous pouvez configurer les zones de base restantes. Maintenant, vous êtes prêt à ajouter des données métier, telles que les clients et les fournisseurs. Pour plus d'informations, reportez-vous à [Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).  

## <a name="companies-and-environments"></a>Entreprises et environnements

[!INCLUDE [company_environment](includes/company_environment.md)]

Pour plus d'informations, voir [Passer à une autre entreprise ou un autre environnement](ui-organization-switch.md).  

## <a name="see-also"></a>Voir aussi

[Personnalisation de Business Central](ui-customizing-overview.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  
[Mise en route](product-get-started.md)  
