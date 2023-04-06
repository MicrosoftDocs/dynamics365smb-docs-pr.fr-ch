---
title: Dépannage de la synchronisation entre Shopify et Business Central
description: Découvrez ce qu’il faut faire si une erreur se produit lors de la synchronisation des données entre Shopify et Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Dépannage de la synchronisation entre Shopify et Business Central

Vous pouvez vous trouver face à des situations où vous devez résoudre des problèmes lors de la synchronisation de données entre Shopify et [!INCLUDE[prod_short](../includes/prod_short.md)]. Cette page définit les étapes permettant de dépanner certains scénarios courants.

## Journaux

Si une tâche de synchronisation échoue, vous pouvez activer la journalisation en activant le bouton à bascule **Activation du journal** dans la page **Fiche magasin Shopify**. Puis déclenchez manuellement la tâche de synchronisation et consultez les journaux.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Écritures journal Shopify**, puis choisissez le lien associé.
2. Sélectionnez l’écriture journal associée et ouvrez la page **Écriture journal Shopify**.
3. Examinez les valeurs de demande, de code statut et de description, et de réponse.

Ultérieurement, n’oubliez pas de désactiver la journalisation ultérieurement pour éviter un impact négatif sur les performances et une augmentation de la taille de la base de données.

Dans la page **Écritures journal Shopify**, vous pouvez déclencher la suppression de toutes les écritures journal ou des écritures antérieures à 7 jours.

## Capture de données

Indépendamment des paramètres **Journal activé**, certaines réponses de Shopify sont toujours journalisées et vous pouvez les inspecter ou les télécharger en utilisant la fenêtre **Liste de capture de données**.

Sélectionnez l’action **Données Shopify récupérées** dans l’une des pages suivantes :

- **Commande Shopify**
- **Exécution des commandes Shopify**
- **Frais de livraison de la commande Shopify**
- **Transactions commande Shopify**
- **Règlements Shopify**
- **Transactions de paiement Shopify**
- **Transactions Shopify**

## Réinitialiser la synchronisation

Pour des performances optimales, le connecteur importe uniquement les clients, les produits et les commandes créés ou modifiés depuis la dernière synchronisation. Dans la page **Fiche magasin Shopify**, ces fonctions sont disponibles pour modifier la date/l’heure de la dernière synchronisation ou la réinitialiser complètement. Cette fonction garantit que, lors de l’exécution de la synchronisation, toutes les données sont synchronisées et pas uniquement les modifications apportées depuis la dernière synchronisation.

Cette fonction ne s’applique qu’aux synchronisations de Shopify à [!INCLUDE[prod_short](../includes/prod_short.md)]. Cette fonction peut être utile si vous voulez restaurer des données supprimées, comme les produits, les clients ou les commandes supprimées.

## Demander le jeton d’accès

Si [!INCLUDE[prod_short](../includes/prod_short.md)] ne parvient pas à se connecter à votre compte Shopify, tentez de réinitialiser le jeton d’accès auprès de Shopify. Cette demande peut être nécessaire en cas de rotation des clés de sécurité ou de modification des autorisations requises (étendues).

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez obtenir le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify.

Le bouton à bascule **A une clé d’accès** sera activé.

### Vérifier et activer les autorisations pour effectuer des requêtes HTTP lors de l’exécution dans un environnement hors production

Pour fonctionner correctement, l’extension de connecteur Shopify nécessite une autorisation pour effectuer des requêtes HTTP. Lors des tests en sandbox, les requêtes HTTP sont interdites pour toutes les extensions.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Gestion des extensions**, puis sélectionnez le lien associé.
2. Sélectionnez l’extension **Connecteur Shopify**.
3. Choisissez l’action **Configurer** pour ouvrir la page **Paramètres de l’extension**.
4. Assurez-vous que le bouton à bascule **Autoriser les requêtes HTTPClient** est activé.

## Faire tourner le jeton d’accès Shopify

Les procédures suivantes décrivent comment faire tourner le jeton d’accès utilisé par le connecteur Shopify pour accéder à votre magasin en ligne Shopify.

### Dans Shopify

1. Depuis votre **Administration Shopify**, accédez à [Applications](https://www.shopify.com/admin/apps).
2. Sélectionnez **Supprimer** dans la ligne avec l’application **Dynamics 365 Business Central**.
3. Sélectionnez **Supprimer** dans le message qui s’affiche.

### Dans [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez faire tourner le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify, passez en revue la confidentialité et les autorisations, puis cliquez sur le bouton **Installer l’application**.

## Problèmes connus

### Le champ *Groupe compta. marché* ne peut pas être nul ou vide ; il doit y avoir une valeur dans le champ client

Sur la page **Fiche magasin Shopify**, remplissez le champ **Code modèle client** dans la fenêtre Fiche magasin  avec le modèle pour lequel **Groupe compta. marché** est renseigné. Le modèle client est utilisé non seulement pour la création de clients, mais également pour le calcul du prix de vente et lors de la création de documents vente.

### L’importation de données dans votre boutique Shopify n’est pas activée. Accédez à la fiche magasin pour l’activer

Dans la fenêtre **Fiche magasin Shopify**, activez le bouton bascule **Autoriser la synchronisation des données vers Shopify**. Ce bouton bascule est destiné à empêcher la boutique en ligne d’obtenir des données de démonstration de [!INCLUDE[prod_short](../includes/prod_short.md)].

### Oauth error invalid_request : Impossible de trouver l’application de l’API Shopify avec api_key

Selon toute vraisemblance, vous utilisez l’[application intégrée](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), où l’URL du client a le format : `https://[application name].bc.dynamics.com`. Le connecteur Shopify ne fonctionne pas pour les applications intégrées. Pour en savoir plus, voir [Quels sont les produits Microsoft pour lesquels le connecteur Shopify est disponible ?](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)
