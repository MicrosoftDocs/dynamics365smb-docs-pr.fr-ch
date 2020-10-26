---
title: Créer un environnement Sandbox | Microsoft Docs
description: Créez un environnement à des fins d’exploration, d’apprentissage, de démonstration, de développement et de test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 5482460acb6ce0e92b1d6dbe876b1b64267974ae
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919703"
---
# <a name="creating-a-sandbox-environment-in-prodshort"></a>Créeation d’un environnement Sandbox dans [!INCLUDE[prodshort](includes/prodshort.md)]

Avec [!INCLUDE[prodshort](includes/prodshort.md)], vous pouvez facilement créer un environnement sûr dans lequel vous pouvez tester, former ou résoudre les problèmes sans perturber les processus de travail ou les données métier de votre société. Cet environnement hors production est appelé *sandbox* . Isolé de la production, un environnement Sandbox est l’emplacement où vous pouvez explorer, apprendre, démontrer, développer et tester en toute sécurité le service sans que les données et les paramètres de votre environnement de production en soient affectés.  

Votre administrateur peut créer des environnements sandbox dans le [centre d’administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mais si vous voulez effectuer un test rapide, vous pouvez créer un environnement sandbox depuis [!INCLUDE[prodshort](includes/prodshort.md)].  

> [!NOTE]
> Techniquement, les environnements sandbox sont très différents des environnements de production, même si votre administrateur crée un sandbox incluant des données de production. Vous ne pouvez pas utiliser un sandbox à des fins d’évaluation, et vous ne pouvez pas demander une exportation de base de données, par exemple. Si vous souhaitez créer un sandbox à des fins d’évaluation, votre administrateur peut créer un environnement de production dédié dans le centre d’administration. Pour plus d’informations, voir [Types d’environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-prodshort"></a>Pour créer un environnement sandbox dans votre [!INCLUDE[prodshort](includes/prodshort.md)]

1. Connectez-vous à votre instance de production de [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Environnement sandbox** , puis sélectionnez le lien associé.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Cliquez sur le bouton **Créer** .  

    Un autre onglet avec [!INCLUDE[d365fin](includes/d365fin_md.md)] s’ouvre à l’endroit où vous pouvez terminer la configuration de votre environnement Sandbox.

    > [!NOTE]  
    >  Si le bloqueur de fenêtres publicitaires est activé dans votre navigateur, modifiez-le pour autoriser les URL provenant de l’adresse *.businesscentral.dynamics.com.

Lorsque l’environnement Sandbox est prêt, vous êtes redirigé vers l’assistant Bienvenue de l’environnement Sandbox.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Vous pouvez choisir le bouton **En savoir plus** pour en savoir plus sur les scénarios de développeur que vous pouvez essayer dans un environnement sandbox, ou choisir le bouton **Fermer** pour passer au Tableau de bord de votre instance sandbox [!INCLUDE[d365fin](includes/d365fin_md.md)].

En haut du tableau de bord, une notification s’affiche pour vous informer qu’il s’agit d’un environnement Sandbox. Vous pouvez également voir le type de l’environnement dans la barre de titre du client.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Un environnement Sandbox créé de cette manière ne contient que les données de démonstration par défaut pour l’entreprise CRONUS. Aucune donnée n’est copiée ou autrement transférée à partir de l’environnement de production.<br /><br />
> Vous pouvez également créer un environnement Sandbox contenant les données de production. Vous devez le faire via le Centre d’administration. Pour plus d’informations, voir [Gestion des environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) dans l’aide sur Developer and IT Pro.

À tout moment, vous pouvez revenir à la page **Environnement Sandbox** et réinitialiser l’environnement Sandbox.

> [!NOTE]  
> La réinitialisation de l’environnement Sandbox entraîne sa suppression complète et sa recréation avec les données de démonstration par défaut.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Un administrateur peut limiter ou même bloquer l’accès de certains utilisateurs à l’environnement sandbox. Ceci peut être effectué à l’aide des fonctions de sécurité standard du produit, telles que la fiche utilisateur, les groupes d’utilisateurs et les ensembles d’autorisations. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Fonctionnalités avancées de l’environnement Sandbox

L’environnement sandbox n’est pas moins utile, car il comprend quelques fonctionnalités pratiques.

### <a name="to-enable-the-advanced-user-experience"></a>Pour activer l’expérience utilisateur avancée

Il est possible d’activer et de tester la fonctionnalité complète de la version standard de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un abonné Sandbox en définissant le champ **Expérience** sur la page **Informations société** sur *Premium* . Trouvez la page **Informations société** dans le menu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Icône Paramètres":::.  

Après avoir activé l’expérience utilisateur *Premium* , vous avez accès à tous les profils (rôles) et tableaux de bord standard dans la version standard. Vous pouvez également créer une société d’évaluation qui est entièrement configurée, notamment les données de démonstration et l’accès aux zones avancées du produit. Vous pouvez également contacter un partenaire revendeur pour une démonstration des fonctionnalités. Pour plus d’informations, voir [Comment trouver un partenaire revendeur ?](across-faq.md#findpartner).  

### <a name="to-enable-complete-sample-data"></a>Pour activer des exemples de données complètes

Dans l’environnement sandbox, vous pouvez également créer une nouvelle société avec l’option **Évaluation avancée - Exemples de données complètes** pour que vous puissiez suivre une formation ou parcourir des procédures qui nécessitent des exemples de données supplémentaires, telles que [Procédure pas à pas : réception et stockage dans des configurations d’entrepôt de base](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).  

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Pour créer une société avec des exemples de données complètes dans un sandbox

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sociétés** , puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau** , puis sélectionnez **Créer une nouvelle société** .  
3. Sur la page **Configuration assistée pour la création d’une société** , choisissez **Suivant** .  
4. Spécifiez un nom pour la nouvelle société, puis, dans le champ **Sélectionnez les données et les paramètres de mise en route** , choisissez **Évaluation avancée - exemples de données complètes** .  
5. Exécutez le reste du guide de configuration assistée.  

Une fois le guide de configuration assistée terminé, vous pouvez commencer à explorer la nouvelle société avec les exemples de données complètes. Pour plus d’informations, voir [Création de sociétés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).  

### <a name="designer"></a>Concepteur

Dans un environnement sandbox, la fonctionnalité **Concepteur** est activée. Vous pouvez activer la fonctionnalité Éditeur en sélectionnant l’icône de conception ![Concepteur](./media/across-sandbox/sandbox-inclient-design-icon.png) sur une page, ou en choisissant l’option de menu **Conception** dans le menu Paramètres ![Paramètres](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Voir aussi

[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Versions d’évaluation et abonnements [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-preview.md)  
[Gestion des environnements dans le centre d’administration de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
