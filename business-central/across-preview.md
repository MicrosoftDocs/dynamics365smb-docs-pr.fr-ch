---
title: "Obtenir la version d'aperçu dans les nouveaux marchés"
description: "Découvrez comment obtenir un accès aux versions d'aperçu de Business Central."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 50d1429a58b878766c76ed97f65936db78191ee0
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>Accéder à la version d'aperçu de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
À compter du printemps 2018, [!INCLUDE[d365fin](includes/d365fin_md.md)] sera disponible dans de nouveaux pays. Pour garantir que [!INCLUDE[d365fin](includes/d365fin_md.md)] est la solution adéquate pour les clients, nous proposons une version d'aperçu du service avant le lancement de la version de printemps. La version d'aperçu pour le Danemark était disponible en janvier 2018, et d'autres marchés suivront bientôt.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Mise en route des versions d'aperçu et des environnements Sandbox
Les versions d'aperçu et les environnements Sandbox sont un excellent moyen de démarrer avec [!INCLUDE[d365fin](includes/d365fin_md.md)]. Une instance d'aperçu contient des fonctionnalités en plus de celles disponibles dans la version actuelle. Les versions d'aperçu donnent aux partenaires et clients la possibilité de tester les fonctionnalités que nous prévoyons de lancer et de fournir des commentaires. Bien que les versions d'aperçu soient principalement destinées aux partenaires, les clients peuvent également les utiliser pour une durée limitée. La version d'aperçu actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] contient la plupart des fonctionnalités disponibles dans Dynamics NAV 2018, qui nécessitent généralement l'aide d'un partenaire pour les configurer.

Pour commencer à utiliser une version d'aperçu, accédez à [cette page](https://go.microsoft.com/fwlink/?linkid=866045) et indiquez votre adresse e-mail professionnelle. Pour en savoir plus sur [!INCLUDE[d365fin](includes/d365fin_md.md)] et les fonctionnalités qu'il propose, reportez-vous à la documentation disponible ici sur ce site.

Un environnement Sandbox est un environnement hors production que vous pouvez utiliser en plus de votre instance de production ou d'aperçu de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un environnement Sandbox permet de créer et tester en toute sécurité des extensions et de développer de nouvelles fonctionnalités pour personnaliser le service sans affecter les données et les paramètres de vos instances de production ou d'aperçu. Pour le moment, tous les clients qui ont une version de production ou d'aperçu peuvent utiliser un environnement Sandbox.

Pour en savoir plus sur l'utilisation d'un environnement Sandbox, reportez-vous aux instructions ci-dessous.

## <a name="creating-a-sandbox-environment"></a>Créeation d'un environnement Sandbox
Pour travailler dans un environnement Sandbox, vous devez disposer d'un abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Il ne peut y avoir qu'un environnement Sandbox par abonnement.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Fonctionnalités avancées disponibles dans un environnement Sandbox
Les environnement Sandbox contiennent une fonction Éditeur interne qui vous permet de créer des pages à l'aide d'une interface « glisser-déplacer » et de créer des extensions dans le client proprement dit en ajoutant et en réordonnant des champs.

Pour plus d'informations, voir [Utilisation de l'éditeur](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Pour créer un environnement Sandbox
1.  Connectez-vous à votre instance de production ou d'aperçu de [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Environnement Sandbox**, puis choisissez le lien associé.
3.  Choisissez **Créer**. Un onglet s'ouvre pour vous permettre de terminer la configuration de votre environnement Sandbox.

    > [!Note]
    > Si le bloqueur de fenêtres publicitaires est activé dans votre navigateur, modifiez-le pour autoriser les URL provenant de l'adresse *.businesscentral.dynamics.com*.  

4.  Lorsque l'environnement Sandbox est prêt, une page d'accueil s'affiche.  
5.  Si vous souhaitez découvrir les scénarios que vous pouvez tester dans un environnement Sandbox, par exemple la procédure de développement d'extensions, choisissez le lien **En savoir plus**. Sinon, sélectionnez **Fermer** pour accéder au tableau de bord de votre instance Sandbox [!INCLUDE[d365fin](includes/d365fin_md.md)].  
6.  En haut du tableau de bord, une notification s'affiche pour vous informer qu'il s'agit d'un environnement Sandbox. Vous pouvez également voir le type de l'environnement dans la barre de titre du client.

    > [!Note]
    > L'environnement Sandbox contient des données de démonstration pour la société fictive CRONUS. Aucune donnée n'est copiée ou autrement transférée à partir de l'environnement de production.  

7.  Vous pouvez revenir à la page Environnements Sandbox à tout moment pour réinitialiser l'environnement Sandbox.

    > [!Note]
    > La réinitialisation d'un environnement Sandbox entraîne sa suppression complète et sa recréation avec les données de démonstration par défaut.  

8.  Pour permuter entre votre environnement de production et Sandbox, utilisez le menu de Dynamics 365 ou la page d'accueil de Dynamics.

    > [!Note]
    > Un administrateur ou un autre utilisateur peut limiter ou même bloquer l'accès à l'environnement Sandbox à l'aide des fonctions de sécurité standard dans [!INCLUDE[d365fin](includes/d365fin_md.md)], comme la fiche utilisateur, les groupes d'utilisateurs et les ensembles d'autorisations.  

### <a name="building-new-solutions-and-intellectual-property"></a>Création de nouvelles solutions et propriété intellectuelle
[!INCLUDE[d365fin](includes/d365fin_md.md)] offre un ensemble d'outils de développement et une plate-forme de génération moderne pour vous permettre de créer vos propres applications complémentaires et solutions intégrées pour connecter ou étendre [!INCLUDE[d365fin](includes/d365fin_md.md)].

[!INCLUDE[d365fin](includes/d365fin_md.md)] fournit des outils permettant d'implémenter vos propres applications complémentaires et fonctionnalités intégrées pour ajouter de nouvelles expériences de bout en bout propres au secteur d'activité ou pour intégrer des solutions tierces. Par exemple, vous pouvez utiliser une API pour créer un application connectée pour échanger des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et votre application de paie. Les applications connectées peuvent également utiliser des extensions pour créer des pages pour le paramétrage, la configuration, ou pour prendre en charge des fonctions spécifiques aux applications. Pour plus d'informations, voir [Développement d'applications pour [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://aka.ms/getstartedwithapps).

## <a name="see-also"></a>Voir aussi
[Mise en route](product-get-started.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

