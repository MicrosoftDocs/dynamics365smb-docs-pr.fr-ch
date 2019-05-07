---
title: Créer un environnement Sandbox | Microsoft Docs
description: Créez un environnement à des fins d'exploration, d'apprentissage, de démonstration, de développement et de test.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 113c081e60b825c48cfb85ae3475a713a1a1e215
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "937961"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Créeation d'un environnement Sandbox
Un environnement Sandbox (aperçu) est une instance hors production de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isolé de la production, un environnement Sandbox est l'emplacement où vous pouvez explorer, apprendre, démontrer, développer et tester en toute sécurité le service sans que les données et les paramètres de votre environnement de production en soient affectés.

## <a name="to-create-a-sandbox-environment"></a>Pour créer un environnement Sandbox
Vous devez disposer d'un abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)] pour pouvoir créer un environnement Sandbox. Il ne peut y avoir qu'un environnement Sandbox par abonnement.

1. Connectez-vous à votre instance de production du service [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Environnement Sandbox**, puis choisissez le lien associé.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Sélectionnez **Créer**.  
  Un autre onglet de votre navigateur s'ouvre pour vous permettre de terminer la configuration de votre environnement Sandbox.
> [!NOTE]  
>  Si le bloqueur de fenêtres publicitaires est activé dans votre navigateur, modifiez-le pour autoriser les URL provenant de l'adresse *.businesscentral.dynamics.com.   

4. Lorsque l'environnement Sandbox est prêt, vous êtes redirigé vers l'assistant Bienvenue de l'environnement Sandbox.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Sélectionnez **En savoir plus** pour découvrir les scénarios que vous pouvez tester dans un environnement Sandbox. Sinon, sélectionnez **Fermer** pour accéder au tableau de bord de votre instance Sandbox [!INCLUDE[d365fin](includes/d365fin_md.md)].
6. En haut du tableau de bord, une notification s'affiche pour vous informer qu'il s'agit d'un environnement Sandbox. Vous pouvez également voir le type de l'environnement dans la barre de titre du client.
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) --> Dans l'environnement Sandbox, un nouvel abonné a été créé. Cet abonné est chargé avec les données de démonstration par défaut de la société CRONUS. Aucune donnée n'est copiée ou transférée à partir de l'environnement de production lors de la création de l'environnement Sandbox.

7. À tout moment, vous pouvez revenir à la page **Environnement Sandbox** et réinitialiser l'environnement Sandbox.
> [!NOTE]  
>  La réinitialisation de l'environnement Sandbox entraîne sa suppression complète et sa recréation avec les données de démonstration par défaut.  

8. Pour permuter entre vos environnements de production et Sandbox, vous pouvez utiliser le lanceur d'applications Business Central.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

9. Un administrateur ou un autre utilisateur peut limiter ou même bloquer l'accès de certains utilisateurs à l'environnement Sandbox. Ceci peut être effectué à l'aide des fonctions de sécurité standard du produit, telles que la fiche utilisateur, les groupes d'utilisateurs et les ensembles d'autorisations.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Fonctionnalités avancées de l'environnement Sandbox
### <a name="designer"></a>Concepteur
Dans un environnement Sandbox, la fonctionnalité **Éditeur** peut être activée en sélectionnant l'icône de conception ![Éditeur](./media/across-sandbox/sandbox-inclient-design-icon.png) sur la page.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="enable-the-advanced-user-experience"></a>Activer l'expérience utilisateur avancée
Il est possible d'activer et de tester la fonctionnalité (complète) avancée de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un abonné Sandbox en définissant le champ **Expérience** sur la page **Informations société**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Une fois que vous avez activé la fonctionnalité avancée dans un abonné Sandbox, vous avez accès à tous les profils et tableaux de bord standard. Vous pouvez également créer une société d'évaluation qui est entièrement configurée, notamment les données de démonstration et l'accès aux zones avancées du produit.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
