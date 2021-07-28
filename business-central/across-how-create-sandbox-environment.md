---
title: Créer un environnement sandbox
description: Créez un environnement « test » de type sandbox à des fins sécurisées d’exploration, d’apprentissage, de démonstration, de développement, de résolution des problèmes et de test depuis Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: 2f4ca6a98aac49fa5fea7d8658ef51a9510c97d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437692"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Créeation d’un environnement Sandbox dans [!INCLUDE[prod_short](includes/prod_short.md)]

Avec [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez facilement créer un environnement sûr dans lequel vous pouvez tester, former ou résoudre les problèmes sans perturber les processus de travail ou les données métier de votre société. Cet environnement hors production est appelé *sandbox*. Isolé de la production, un environnement Sandbox est l’emplacement où vous pouvez explorer, apprendre, démontrer, développer et tester en toute sécurité le service sans que les données et les paramètres de votre environnement de production en soient affectés.  

Votre administrateur gère des environnements sandbox dans le [centre d’administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mais si vous voulez effectuer un test rapide, vous pouvez créer un environnement sandbox depuis [!INCLUDE[prod_short](includes/prod_short.md)]. Une fois que vous avez terminé, vous pouvez supprimer l’environnement sandbox, en utilisant le centre d’administration.  

> [!NOTE]
> Techniquement, les environnements sandbox sont très différents des environnements de production, même si votre administrateur crée un sandbox incluant des données de production. Vous ne pouvez pas utiliser un sandbox à des fins d’évaluation, et vous ne pouvez pas demander une exportation de base de données, par exemple. Si vous souhaitez créer un environnement sandbox à des fins d’évaluation, votre administrateur peut créer un environnement de production dédié dans le centre d’administration. Pour plus d’informations, consultez [Environnements de production et sandbox](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Pour créer un environnement sandbox dans votre [!INCLUDE[prod_short](includes/prod_short.md)]

1. Connectez-vous à votre instance de production de [!INCLUDE[prod_short](includes/prod_short.md)].

2. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Environnement Sandbox**, puis choisissez le lien associé.
    <!-- ![Sandbox Environment Setup.](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Cliquez sur le bouton **Créer**.  

    Un autre onglet avec [!INCLUDE[prod_short](includes/prod_short.md)] s’ouvre à l’endroit où vous pouvez terminer la configuration de votre environnement Sandbox.

    > [!NOTE]  
    >  Si le bloqueur de fenêtres publicitaires est activé dans votre navigateur, modifiez-le pour autoriser les URL provenant de l’adresse *.businesscentral.dynamics.com.

Lorsque l’environnement Sandbox est prêt, vous êtes redirigé vers l’assistant Bienvenue de l’environnement Sandbox.
<!-- ![Sandbox Welcome Wizard.](./media/across-sandbox/sandbox-wizard.png) -->

Vous pouvez choisir le bouton **En savoir plus** pour en savoir plus sur les scénarios de développeur que vous pouvez essayer dans un environnement sandbox, ou choisir le bouton **Fermer** pour passer au Tableau de bord de votre instance sandbox [!INCLUDE[prod_short](includes/prod_short.md)].

En haut du tableau de bord, une notification s’affiche pour vous informer qu’il s’agit d’un environnement Sandbox. Vous pouvez également voir le type de l’environnement dans la barre de titre du client.
    <!-- ![Sandbox RoleCenter Notification.](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Un environnement Sandbox créé de cette manière ne contient que les données de démonstration par défaut pour l’entreprise CRONUS. Aucune donnée n’est copiée ou autrement transférée à partir de l’environnement de production.
>
> Vous pouvez également créer un environnement sandbox basé sur les données de production. Vous devez le faire via le Centre d’administration. Pour plus d’informations, voir [Gestion des environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) dans le contenu dédié à l’équipe Administration et aux développeurs.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu.](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Un administrateur peut limiter ou même bloquer l’accès de certains utilisateurs à l’environnement sandbox. Ceci peut être effectué à l’aide des fonctions de sécurité standard du produit, telles que la fiche utilisateur, les groupes d’utilisateurs et les ensembles d’autorisations. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets.](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Fonctionnalités avancées de l’environnement Sandbox

L’environnement sandbox n’est pas moins utile, car il comprend quelques fonctionnalités pratiques :

* [Expérience utilisateur avancée](#advanced-user-experience)  
* [Exemples de données complets](#complete-sample-data)  
* [Concepteur](#designer)  

### <a name="advanced-user-experience"></a>Expérience utilisateur avancée

Il est possible d’activer et de tester la fonctionnalité complète de la version standard de [!INCLUDE[prod_short](includes/prod_short.md)] dans un abonné Sandbox en définissant le champ **Expérience** sur la page **Informations société** sur *Premium*. Trouvez la page **Informations société** dans le menu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Icône Paramètres":::. .  

Après avoir activé l’expérience utilisateur *Premium*, vous avez accès à tous les profils (rôles) et tableaux de bord standard dans la version standard. Vous pouvez également créer une société d’évaluation qui est entièrement configurée, notamment les données de démonstration et l’accès aux zones avancées du produit. Vous pouvez également contacter un partenaire revendeur pour une démonstration des fonctionnalités. Pour plus d’informations, voir [Comment trouver un partenaire revendeur ?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Exemples de données complets

Pour les situations où vous avez besoin d’exemples de données supplémentaires, veuillez vous adresser à votre partenaire revendeur.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Pour créer une société avec des exemples de données complètes dans un sandbox

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Sociétés**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**, puis sélectionnez **Créer une nouvelle société**.  
3. Sur la page **Configuration assistée pour la création d’une société**, choisissez **Suivant**.  
4. Spécifiez un nom pour la nouvelle société, puis, dans le champ **Sélectionnez les données et les paramètres de mise en route**, choisissez **Évaluation avancée - exemples de données complètes**.  
5. Exécutez le reste du guide de configuration assistée.  

Une fois le guide de configuration assistée terminé, vous pouvez commencer à explorer la nouvelle société avec les exemples de données complètes. Pour plus d’informations, voir [Création de sociétés dans [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Concepteur

Dans un environnement sandbox, la fonctionnalité **Concepteur** est activée. Vous pouvez activer Concepteur en sélectionnant l’icône de conception ![Concepteur.](./media/across-sandbox/sandbox-inclient-design-icon.png) sur une page, ou en choisissant l’élément de menu **Conception** dans le menu ![Paramètres](media/ui-experience/settings_icon_small.png).  

Pour plus d’informations, consultez [Utilisation du concepteur](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) dans le contenu dédié à l’équipe Administration et aux développeurs (en anglais uniquement).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Voir aussi

[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
Versions d’évaluation et abonnements [[!INCLUDE[prod_long](includes/prod_long.md)]](across-preview.md)  
[Gestion des environnements dans le centre d’administration de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
