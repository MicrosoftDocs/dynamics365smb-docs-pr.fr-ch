---
title: Gérez les paramètres et préférences utilisateur en tant qu’administrateur
description: Gérez les paramètres et les préférences de l’utilisateur dans Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
---
# Gérer les paramètres et les préférences de l’utilisateur

En tant qu’administrateur, vous pouvez configurer les paramètres utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)], semblable à la façon dont les utilisateurs individuels peuvent gérer leurs propres préférences sur la page **Mes paramètres**.  

Obtenez un aperçu de tous les utilisateurs de la liste **Utilisateurs**, et modifiez les paramètres individuels en choisissant l’action **Paramètres utilisateur** pour l’utilisateur concerné.

> [!TIP]
> La liste **Paramètres utilisateur** affiche les paramètres actuels de chaque utilisateur. Pour afficher ou modifier des utilisateurs individuels, choisissez l’action **Afficher** ou **Modifier**.

La page **Carte des paramètres utilisateur** est similaire à la page **Mes paramètres** à laquelle chaque utilisateur a accès, et c’est un outil puissant pour vous en tant qu’administrateur pour définir les paramètres par défaut et effacer les pages personnalisées, par exemple.  

## Types de paramètres utilisateur

*Paramètres utilisateur* n’est pas la même chose que *configuration utilisateur*, qui concerne l’utilisateur en tant qu’entité et l’accès de l’utilisateur dans le système. En outre, les paramètres utilisateur n’ont rien à voir avec la personnalisation d’un utilisateur, comme les modifications légères de l’interface utilisateur. Les paramètres utilisateur déterminent les paramètres prédéfinis de chaque utilisateur dans divers aspects de la façon dont l’application se présente à l’utilisateur. Le paragraphe suivant répertorie les cinq types de paramètres et préférences de l’utilisateur qui peuvent être définis par l’individu ou de manière centralisée par l’administrateur :

* **Société**  

  Ce paramètre détermine la société à laquelle se connecter lors de la prochaine connexion. Un utilisateur peut avoir accès à plusieurs sociétés et peut être actif dans plusieurs sociétés.

* **Rôle**  

  Le rôle ou le profil décrit la fonction de l’utilisateur dans la société, comme *Directeur commercial*, *Comptable*, ou *Agent d’achat*. Le profil détermine ensuite le tableau de bord de l’utilisateur, la page d’accueil que les utilisateurs verront lorsqu’ils se connecteront. Le profil n’a pas d’impact sur les droits d’accès aux fonctionnalités de [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Langue**  

  Définit la langue d’application dans laquelle [!INCLUDE[prod_short](includes/prod_short.md)] présente du texte, des légendes et des messages d’erreur. Si les utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] sont synchronisés à partir de Microsoft 365, les paramètres de langue de Microsoft 365 sont utilisés, en supposant que l’utilisateur souhaite utiliser les mêmes paramètres dans les produits Office et [!INCLUDE[prod_short](includes/prod_short.md)]. L’administrateur peut modifier le paramètre par défaut et chaque utilisateur peut choisir parmi les langues disponibles sur la page Mes paramètres. Mais ils seront réinitialisés sur la valeur de Microsoft 365 une fois la synchronisation suivante effectuée.

  Si le paramètre de langue de Microsoft 365 correspond à une langue prise en charge dans [!INCLUDE[prod_short](includes/prod_short.md)], cette langue sera choisie pour l’utilisateur.  

  > [!NOTE]
  > Vous devrez peut-être installer une application de langue pour que [!INCLUDE[prod_short](includes/prod_short.md)] affiche correctement la langue. Par conséquent, il est recommandé d’installer les applications de langue nécessaires avant qu’un utilisateur ne se connecte pour la première fois afin qu’il ait une bonne expérience dès le premier jour. Pour plus d’informations, consultez la liste des [langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Région**  

  Définit la façon dont les dates et les nombres sont présentés dans le client [!INCLUDE[prod_short](includes/prod_short.md)], par exemple s’il faut utiliser des formats de date européen ou américain, ou comment afficher le signe décimal et le séparateur des milliers dans les montants. Si les utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] sont synchronisés à partir de Microsoft 365, les paramètres régionaux de Microsoft 365 sont utilisés, en supposant que l’utilisateur souhaite utiliser les mêmes paramètres dans les produits Office et [!INCLUDE[prod_short](includes/prod_short.md)]. Un administrateur ou un utilisateur peut modifier ces paramètres manuellement dans [!INCLUDE[prod_short](includes/prod_short.md)], mais ils seront réinitialisés à la valeur de Microsoft 365 une fois la synchronisation suivante effectuée.

* **Fuseau horaire**  

  Définit le fuseau horaire dans lequel se trouve l’utilisateur. Actuellement, ce n’est pas synchronisé à partir de Microsoft 365 et doit être réglé manuellement.  

* **Conseils d’apprentissage**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] En tant qu’administrateur, vous pouvez désactiver les conseils pédagogiques pour tous les utilisateurs, par exemple si vous êtes en train d’intégrer des utilisateurs déjà familiarisés avec [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Si une synchronisation des utilisateurs Microsoft 365 est effectuée pendant que les utilisateurs sont connectés à [!INCLUDE[prod_short](includes/prod_short.md)], ces utilisateurs doivent actualiser le navigateur, ou se déconnecter et se reconnecter à [!INCLUDE[prod_short](includes/prod_short.md)] pour voir une langue potentiellement différente définie par l’action de synchronisation.

## Vue d’ensemble de toutes les modifications spécifiques à l’utilisateur

En tant qu’administrateur, vous pouvez obtenir un aperçu des modifications individuelles apportées à [!INCLUDE [prod_short](includes/prod_short.md)] que chaque utilisateur peut avoir fait sur différentes pages dans [!INCLUDE [prod_short](includes/prod_short.md)]. Lorsque les utilisateurs modifient leur expérience dans [!INCLUDE [prod_short](includes/prod_short.md)], ces changements seront reflétés dans la liste **Personnalisations utilisateur**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## Pour consulter ou supprimer les personnalisations des utilisateurs

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Pages personnalisées**, puis sélectionnez le lien associé.
2. Cela montre la liste des utilisateurs et leurs pages personnalisées. Pour effacer la personnalisation d’un utilisateur, cliquez sur la ligne appropriée ou choisissez **Gérer**, puis **Supprimer**.

Cela supprime la personnalisation et l’expérience de l’utilisateur de la page concernée revient à l’état par défaut.

## Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Disponibilité par pays/région et langues prises en charge](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Modification de la langue et des paramètres régionaux](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
