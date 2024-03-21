---
title: Mise en route du connecteur pour Shopify
description: Premières étapes lors de la configuration de la connexion entre Business Central et Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# Mise en route du connecteur Shopify

Connectez vos magasins Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)] et optimisez la productivité de votre entreprise. Gérez et affichez les informations de votre entreprise et de votre magasin Shopify comme une seule unité.

Pour utiliser Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)], vous devez d’abord effectuer quelques actions. Cet article sert de guide pour terminer l’intégration de votre magasin Shopify avec [!INCLUDE [prod_short](../includes/prod_short.md)].

## Conditions préalables pour Shopify

Vous devez disposer :

- D’un compte Shopify
- D’une boutique en ligne Shopify

Pour en savoir plus sur la création de versions d’essai Shopify et sur les paramètres recommandés, accédez à [Créer et configurer un compte Shopify](shopify-account.md).

## Conditions préalables pour Business Central

- Assurez-vous que l’application **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)** est installée.

  L’application est préinstallée pour toutes les nouvelles inscriptions et tous les essais. En savoir plus sur l’installation d’applications à partir d’AppSource dans [Installation et désinstallation des extensions](../ui-extensions-install-uninstall.md#install). Suivez les étapes ci-dessous si vous n’avez pas [!INCLUDE[prod_short](../includes/prod_short.md)].

- Assurez-vous que l’utilisateur dispose des bonnes autorisations. Le connecteur Shopify est couvert par l’ensemble d’autorisations **Shopify – Admin (SHPFY – ADMIN)**. En savoir plus à [Créer des utilisateurs en fonction des licences](../ui-how-users-permissions.md) et [Affectation des autorisations aux utilisateurs et aux groupes](../ui-define-granular-permissions.md).

## Installation de l’application Dynamics 365 Business Central pour votre boutique en ligne Shopify

Pour les instances existantes de [!INCLUDE[prod_short](../includes/prod_short.md)], cette étape est facultative et peut être ignorée.

1. Localisez l’application [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) sur l’[AppStore Shopify](https://apps.shopify.com/)
2. Cliquez sur le bouton **Ajouter des applications**. Si vous y êtes invité, connectez-vous à votre compte Shopify. Sélectionnez la boutique en ligne si vous en avez plusieurs.
3. Après avoir passé en revue la confidentialité et les autorisations, choisissez le bouton **Installer l’application**.

   Vous pouvez trouver et ouvrir l’application **Dynamics 365 Business Central** installée dans la section **Applications** dans la barre latérale de la page **Adinistrateur Shopify**.
4. Choisissez **S’inscrire maintenant** pour commencer l’essai [!INCLUDE[prod_short](../includes/prod_short.md)] ou **Se connecter** si vous avez déjà [!INCLUDE[prod_short](../includes/prod_short.md)]. Vous serez redirigé vers votre page [Business Central](https://businesscentral.dynamics.com).
5. Procédez comme suit dans [!INCLUDE[prod_short](../includes/prod_short.md)].

## Connexion de Business Central à la boutique en ligne Shopify

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasin Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Code**, entrez un code qui sera facile à trouver dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Par exemple, le nom peut refléter ce que vend un magasin, comme « Meubles » ou « Café », ou le pays ou la région qu’il dessert.
4. Dans le champ **URL Shopify**, saisissez l’URL de la boutique en ligne à laquelle vous souhaitez vous connecter. Utilisez le format suivant : `https://{shop}.myshopify.com/`.
5. Activez le bouton à bascule **Activé**, lisez et acceptez les conditions générales.
6. Si vous y êtes invité, connectez-vous à votre compte Shopify. Examinez les conditions de confidentialité et les autorisations, puis choisissez le bouton **Installer l’application**.

Répétez les étapes 2 à 6 pour toutes les boutiques en ligne que vous voulez connecter.

### Problèmes connus

- Le navigateur bloque la fenêtre contextuelle. Lorsque vous activez le bouton **Activé**, [!INCLUDE [prod_short](../includes/prod_short.md)] ouvre la page **En attente d’une réponse - ne fermez pas cette page** en attendant un jeton d’accès de Shopify. Si cette page est fermée ou bloquée, vous ne pouvez pas vous connecter à Shopify. Pour en savoir plus, consultez [Demander le jeton d’accès](troubleshoot.md#request-the-access-token).
- Il pourrait être judicieux d’ouvrir l’administrateur Shopify dans le même navigateur que [!INCLUDE [prod_short](../includes/prod_short.md)].
- [Erreur : erreur Oauth invalid_request : impossible de trouver l’application API Shopify avec api_key.](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Erreur : Oauth erreur invalid_request : votre compte n’est pas autorisé à accorder l’accès demandé pour cette application.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Impossible de se connecter depuis le bac à sable](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)
- Assurez-vous de saisir la bonne URL dans le champ **Shopify URL** . Vous pouvez créer l’URL en combinant l’ID de magasin à partir de l’URL d’administrateur. Par exemple, `admin.shopify.com/store/{shop}` et `.myshopify.com` pour obtenir `https://{shop}.myshopify.com/`.

## Étapes suivantes

Votre boutique en ligne est désormais connectée à [!INCLUDE[prod_short](../includes/prod_short.md)]. Dans les étapes suivantes, vous allez définir comment et quoi synchroniser.

- [Synchroniser les articles](synchronize-items.md)
- [Synchroniser les clients](synchronize-customers.md)
- [Synchroniser les commandes](synchronize-orders.md)

## Stratégies de test

Il existe différentes approches pour tester une intégration, et chaque approche a ses avantages et ses inconvénients.

Vous pouvez connecter [!INCLUDE[prod_short](../includes/prod_short.md)] et les comptes Shopify aussi souvent que vous le souhaitez. Le connecteur Shopify n’affecte que l’environnement, ou pour être plus précis, l’entreprise dans laquelle il est activé. Vous pouvez vous connecter à la même boutique en ligne Shopify à partir de plusieurs environnements ou entreprises. Vous pouvez désactiver et réactiver le connecteur.

Il est facile de relancer les tests de synchronisation. Le connecteur vous permet de supprimer les données importées, telles que les produits, les clients et les commandes, puis de les réimporter. Il vous suffit de [réinitialiser la synchronisation](troubleshoot.md#reset-sync).

### Bac à sable Shopify et bac à sable Business Central

C’est probablement le moyen le plus sûr de tester l’intégration. Au lieu d’utiliser un bac à sable Shopify, vous pouvez également utiliser un abonnement d’essai ou une boutique de développement. Dans [!INCLUDE[prod_short](../includes/prod_short.md)], vous pouvez également utiliser une société de test dans un environnement de production.

Pour en savoir plus sur les bacs à sable [!INCLUDE[prod_short](../includes/prod_short.md)], accédez à [Créer un environnement](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### Bac à sable Shopify et production Business Central

Ce n’est *pas* une configuration recommandée pour les tests, car le connecteur Shopify peut créer ou modifier des articles et des clients. Il peut également créer des documents de vente tels que des commandes et des factures. Ces documents peuvent être difficiles à annuler.
 
Si vous devez utiliser cette configuration, nous vous recommandons de vérifier et probablement de désactiver les paramètres suivants :

* **Créer automatiquement un article inconnu** pour ne pas créer d’articles.
* **Shopify peut mettre à jour les articles** pour ne pas mettre à jour les articles mappés.
* **Créer automatiquement un client inconnu** pour ne pas créer de clients et de contacts.
* **Shopify peut mettre à jour les clients** pour ne pas mettre à jour les clients existants.
* **Créer automatiquement des commandes vente** pour ne pas créer de commandes ni de factures vente.

Pour plus d’informations, voir [Restauration d’un environnement](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### Production Shopify et bac à sable Business Central

Il peut être judicieux de sauvegarder vos données. Par exemple, exportez vos produits et vos clients. Pour plus d’informations, voir [Utiliser des fichiers CSV pour sauvegarder les informations du magasin](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Désactivez l’option **Autoriser la synchronisation des données vers Shopify** pour que [!INCLUDE[prod_short](../includes/prod_short.md)] n’écrive pas dans Shopify. Dans ce cas, vous pourrez importer des produits, des images, des clients et des commandes depuis Shopify. Mais vous ne pourrez pas envoyer d’articles, de prix, de niveaux de stock, de clients ni d’informations d’exécution à Shopify.

Si vous laissez le bouton à bascule **Autoriser la synchronisation des données vers Shopify** activé, les mesures de protection supplémentaires sont :

*   Sélectionnez **Brouillon** dans le champ **Statut pour créer un produit** pour vous assurer que les produits exportés ne sont pas disponibles pour les acheteurs. Vous pouvez vérifier l’apparence des produits dans la boutique en ligne et synchroniser les prix, les options et les niveaux de stock. Assurez-vous simplement d’utiliser des filtres sur la page  **Ajouter un élément à Shopify** pour limiter le nombre d’éléments exportés.
* Désactivez le bouton à bascule **Exporter le client vers Shopify** afin de ne pas envoyer de clients vers Shopify.

## Voir aussi

[Procédure pas à pas : configurer et utiliser le connecteur Shopify](walkthrough-setting-up-and-using-shopify.md)  

