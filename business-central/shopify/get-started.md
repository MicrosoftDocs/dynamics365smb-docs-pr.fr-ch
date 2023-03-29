---
title: Mise en route du connecteur pour Shopify
description: Premières étapes lors de la configuration de la connexion entre Business Central et Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Mise en route du connecteur Shopify

Connectez votre magasin Shopify (ou vos magasins) avec [!INCLUDE [prod_short](../includes/prod_short.md)] et optimisez la productivité de votre entreprise. Gérez et affichez les informations de votre entreprise et de votre magasin Shopify comme une seule unité.

Pour utiliser Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)], vous devez d’abord effectuer quelques actions. Cet article sert de guide pour terminer l’intégration de votre magasin Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)].

## Conditions préalables pour Shopify

Vous devez disposer :

- D’un compte Shopify
- D’une boutique en ligne Shopify

Pour en savoir plus sur la création de versions d’essai Shopify et les paramètres recommandés en accédant à [Création et configuration d’un compte Shopify](shopify-account.md).

## Conditions préalables pour Business Central

- Assurez-vous que l’application **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)** est installée.

  L’application est préinstallée pour toutes les nouvelles inscriptions et tous les essais. En savoir plus sur l’installation d’applications à partir d’AppSource dans [Installation et désinstallation des extensions](../ui-extensions-install-uninstall.md#install). Suivez les étapes ci-dessous si vous n’avez pas [!INCLUDE[prod_short](../includes/prod_short.md)].

- Assurez-vous que l’utilisateur dispose de suffisamment d’autorisations. Le connecteur Shopify est couvert par l’ensemble d’autorisations *Shopify – Admin (SHPFY – ADMIN)*. En savoir plus à [Créer des utilisateurs en fonction des licences](../ui-how-users-permissions.md) et [Affectation des autorisations aux utilisateurs et aux groupes](../ui-define-granular-permissions.md)


## Installation de l’application Dynamics 365 Business Central pour votre boutique en ligne Shopify

Pour le [!INCLUDE[prod_short](../includes/prod_short.md)] existant, cette étape est facultative et peut être ignorée.

1. Localisez l’application [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) sur l’[AppStore Shopify](https://apps.shopify.com/)
2. Cliquez sur le bouton **Ajouter des applications**. Si vous y êtes invité, connectez-vous à votre compte Shopify. Sélectionnez la boutique en ligne souhaitée si vous en avez plusieurs.
3. Après avoir passé en revue la confidentialité et les autorisations, choisissez le bouton **Installer l’application**.

   Vous pouvez trouver et ouvrir l’application **Dynamics 365 Business Central** installée dans la section **Applications** dans la barre latérale de la page **Adinistrateur Shopify**.
4. Choisissez **S’inscrire maintenant** pour commencer l’essai [!INCLUDE[prod_short](../includes/prod_short.md)] ou **Se connecter** si vous avez déjà [!INCLUDE[prod_short](../includes/prod_short.md)]. Vous serez redirigé vers votre page [Business Central](https://businesscentral.dynamics.com).
5. Les étapes suivantes doivent avoir lieu dans [!INCLUDE[prod_short](../includes/prod_short.md)].

## Connexion de Business Central à la boutique en ligne Shopify

1. Sélectionnez ![l’icône Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Code**, entrez le code qui vous permettra de le retrouver facilement dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Par exemple, un nom peut refléter ce qu’un magasin vend, comme « Meubles » ou « Café », ou le pays ou la région qu’il dessert.
4. Dans le champ **URL Shopify**, saisissez l’URL de votre boutique en ligne, qui doit être connectée. Utilisez le format suivant : `https://{shop}.myshopify.com/`.
5. Activez la bascule **Activé**, lisez et acceptez les conditions générales.
6. Si vous y êtes invité, connectez-vous à votre compte Shopify, passez en revue la confidentialité et les autorisations, puis cliquez sur le bouton **Installer l’application**.

Répétez les étapes 2 à 6 pour toutes les boutiques en ligne que vous voulez connecter.

### Problèmes connus

- Le navigateur bloque la fenêtre contextuelle. Quand vous activez le bouton à bascule **Activé**, le système ouvre la page **En attente d’une réponse – ne pas fermer cette page**, en attente d’un jeton d’accès de Shopify, si cette page est fermée ou bloquée, vous ne pouvez pas vous connecter à Shopify. En savoir plus sur [Demander le jeton d’accès](troubleshoot.md#request-the-access-token)
- [error invalid_request Oauth : impossible de trouver l’application de l’API Shopify avec api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Impossible de se connecter depuis le bac à sable](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Étapes suivantes

Votre boutique en ligne est désormais connectée à [!INCLUDE[prod_short](../includes/prod_short.md)]. Dans les étapes suivantes, vous allez définir comment et quoi synchroniser.

- [Synchroniser les articles](synchronize-items.md)
- [Synchroniser les clients](synchronize-customers.md)
- [Synchroniser les commandes](synchronize-orders.md)

## Voir aussi

[Procédure pas à pas : configurer et utiliser le connecteur Shopify](walkthrough-setting-up-and-using-shopify.md)  

