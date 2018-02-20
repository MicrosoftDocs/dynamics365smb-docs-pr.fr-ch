---
title: "Créer un environnement Sandbox | Microsoft Docs"
description: "Créez un environnement à des fins d'exploration, d'apprentissage, de démonstration, de développement et de test."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3ee160e2c38107aea1342b51d729aa172bbbc3e
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a>Créer un environnement Sandbox
Un environnement Sandbox (aperçu) est une instance hors production de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isolé de la production, un environnement Sandbox est l'emplacement où vous pouvez explorer, apprendre, démontrer, développer et tester en toute sécurité le service sans que les données et les paramètres de votre environnement de production en soient affectés.

## <a name="to-create-a-sandbox-environment"></a>Pour créer un environnement Sandbox
Vous devez disposer d'un abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)] pour pouvoir créer un environnement Sandbox. Il ne peut y avoir qu'un environnement Sandbox par abonnement.

1. Connectez-vous à votre instance de production du service [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Environnement Sandbox**, puis sélectionnez le lien connexe.
![Configuration de l'environnement Sandbox](./media/across-sandbox/sandbox-environment-setup.png)
3. Sélectionnez **Créer**.  
  Un autre onglet de votre navigateur s'ouvre pour vous permettre de terminer la configuration de votre environnement Sandbox.
> [!NOTE]  
>  Si le bloqueur de fenêtres publicitaires est activé dans votre navigateur, modifiez-le pour autoriser les URL provenant de l'adresse *.financials.dynamics.com.   

4. Lorsque l'environnement Sandbox est prêt, vous êtes redirigé vers l'assistant Bienvenue de l'environnement Sandbox.
![Assistant Bienvenue de l'environnement Sandbox](./media/across-sandbox/sandbox-wizard.png)

5. Sélectionnez **En savoir plus** pour découvrir les scénarios que vous pouvez tester dans un environnement Sandbox. Sinon, sélectionnez **Fermer** pour accéder au tableau de bord de votre instance Sandbox [!INCLUDE[d365fin](includes/d365fin_md.md)].
6. En haut du tableau de bord, une notification s'affiche pour vous informer qu'il s'agit d'un environnement Sandbox. Vous pouvez également voir le type de l'environnement dans la barre de titre du client.
![Notification du tableau de bord Sandbox](./media/across-sandbox/sandbox-rolecenter-notification.png)  
Dans l'environnement Sandbox, un nouvel abonné a été créé. Cet abonné est chargé avec les données de démonstration par défaut de la société CRONUS. Aucune donnée n'est copiée ou transférée à partir de l'environnement de production lors de la création de l'environnement Sandbox.
7.  À tout moment, vous pouvez revenir à la page **Environnement Sandbox** et réinitialiser l'environnement Sandbox.
> [!NOTE]  
>  La réinitialisation de l'environnement Sandbox entraîne sa suppression complète et sa recréation avec les données de démonstration par défaut.  

8.  Pour permuter entre vos environnements de production et Sandbox, vous pouvez utiliser le lanceur d'applications Finance and Operations, Business edition.
![Menu Dynamics 365 de l'environnement Sandbox](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Un administrateur ou un autre utilisateur peut limiter ou même bloquer l'accès de certains utilisateurs à l'environnement Sandbox. Ceci peut être effectué à l'aide des fonctions de sécurité standard du produit, telles que la fiche utilisateur, les groupes d'utilisateurs et les ensembles d'autorisations.

![Ensembles d'autorisations Sandbox](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Fonctionnalités avancées de l'environnement Sandbox
### <a name="the-in-client-designer"></a>Éditeur interne du client
Dans un environnement Sandbox, la fonctionnalité Éditeur interne du client peut être activée en sélectionnant l'icône de conception ![Éditeur](./media/across-sandbox/sandbox-inclient-design-icon.png) sur une page.

![Éditeur interne du client](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Activer l'expérience utilisateur avancée
Il est possible d'activer et de tester la fonctionnalité (complète) avancée de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un abonné Sandbox en définissant le champ **Expérience** sur la page **Informations société**.

![Expérience avancée dans l'environnement Sandbox](./media/across-sandbox/sandbox-advanced.png)

![Sandbox/Production](./media/across-sandbox/sandbox-production.png)

Une fois que vous avez activé la fonctionnalité avancée dans un abonné Sandbox, vous avez accès à tous les profils et tableaux de bord standard. Vous pouvez également créer une société d'évaluation qui est entièrement configurée, notamment les données de démonstration et l'accès aux zones avancées du produit.

![Nouvelle société Sandbox](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

