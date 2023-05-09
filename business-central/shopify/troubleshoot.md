---
title: Dépannage de la synchronisation entre Shopify et Business Central
description: Découvrez ce qu’il faut faire si une erreur se produit lors de la synchronisation des données entre Shopify et Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# Dépannage de la synchronisation entre Shopify et Business Central

Vous pouvez vous trouver face à des situations où vous devez résoudre des problèmes lors de la synchronisation de données entre Shopify et [!INCLUDE[prod_short](../includes/prod_short.md)]. Cette page définit les étapes permettant de dépanner certains scénarios courants.

## Exécuter des tâches au premier plan

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasin Shopify**, puis choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez résoudre les problèmes pour ouvrir la page **Fiche magasin Shopify**.
3. Désactivez **Autoriser les synchronisations en arrière-plan**.

Désormais, lorsque l’action de synchronisation est déclenchée, la tâche s’exécute au premier plan. Si une erreur se produit, une boîte de dialogue d’erreur s’affiche, avec un lien **Copier les détails**. Utilisez le lien pour copier les informations dans un éditeur de texte pour une analyse plus approfondie.

## Journaux

Si une tâche de synchronisation échoue, vous pouvez activer le bouton à bascule **Journal activé** dans la page **Fiche magasin Shopify** pour activer la journalisation. Puis déclenchez manuellement la tâche de synchronisation et consultez les journaux.

### Pour activer la journalisation

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasin Shopify**, puis choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez résoudre les problèmes pour ouvrir la page **Fiche magasin Shopify**.
3. Activez le bouton bascule **Journal activé**.

### Pour vérifier les journaux

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Écritures journal Shopify**, puis choisissez le lien associé.
2. Sélectionnez l’écriture journal associée, puis ouvrez la page **Écriture journal Shopify**.
3. Examinez les valeurs de demande, de code statut et de description, et de réponse. Vous pouvez télécharger les valeurs de demande et de réponse sous forme de fichiers au format texte.

Ultérieurement, n’oubliez pas de désactiver la journalisation pour éviter un effet négatif sur les performances et une augmentation de la taille de la base de données.

Dans la page **Écritures journal Shopify**, vous pouvez déclencher la suppression de toutes les écritures journal ou des écritures antérieures à 7 jours.

## Capture de données

Que le paramètre **Journal activé** soit activé ou pas, certaines réponses de Shopify sont toujours journalisées. Vous pouvez inspecter ou télécharger les journaux à partir de la page **Liste de capture de données**.

Sélectionnez l’action **Données Shopify récupérées** dans l’une des pages suivantes :

- **Commande Shopify**
- **Exécution des commandes Shopify**
- **Frais de livraison de la commande Shopify**
- **Transactions commande Shopify**
- **Règlements Shopify**
- **Transactions de paiement Shopify**
- **Transactions Shopify**

## Réinitialiser la synchronisation

Pour des performances optimales, le connecteur importe uniquement les clients, les produits et les commandes créés ou modifiés après la dernière synchronisation. Dans la page **Fiche magasin Shopify**, des fonctions sont disponibles pour modifier la date/l’heure de la dernière synchronisation ou la réinitialiser complètement. Cette fonction garantit que toutes les données sont synchronisées et pas uniquement les modifications apportées depuis la dernière synchronisation.

Cette fonction ne s’applique qu’aux synchronisations de Shopify à [!INCLUDE[prod_short](../includes/prod_short.md)]. Cette fonction peut être utile si vous voulez restaurer des données supprimées, comme les produits, les clients ou les commandes supprimées.

## Demander le jeton d’accès

Si [!INCLUDE[prod_short](../includes/prod_short.md)] ne parvient pas à se connecter à votre compte Shopify, tentez de réinitialiser le jeton d’accès auprès de Shopify. Le jeton peut être nécessaire en cas de modifications des clés de sécurité ou des autorisations requises (étendues).

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez obtenir le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify.

Le bouton à bascule **A une clé d’accès** sera activé.

### Vérifier et activer les autorisations pour effectuer des requêtes HTTP dans un environnement hors production

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

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez faire tourner le jeton d’accès pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Demander l’accès**.
4. Si vous y êtes invité, connectez-vous à votre compte Shopify, passez en revue la confidentialité et les autorisations, puis cliquez sur le bouton **Installer l’application**.

## Problèmes connus

### Erreur : L’en-tête des ventes n’existe pas. Champs et valeurs d’identification : Document Type=’Quote’,No.=’YOUR SHOPIFY STORE’

Pour calculer les prix, le connecteur Shopify crée un document de vente temporaire (devis) pour un client temporaire (code de magasin) et utilise la logique de calcul du prix standard. Si une extension tierce s’abonne à des événements dans un document de vente temporaire, l’en-tête peut ne pas être disponible. Nous vous recommandons de contacter le fournisseur de l’extension. Demandez-lui de modifier son code pour rechercher des enregistrements temporaires. Dans certains cas, il lui suffit d’ajouter la méthode `IsTemporary` au bon endroit. Pour en savoir plus sur `IsTemporary`, consultez [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Pour vérifier que le problème est causé par une extension tierce, utilisez le lien **Copier les informations dans le presse-papiers** dans le message d’erreur et copiez le contenu dans un éditeur de texte. Les informations contiennent une **pile d’appels AL**, où la ligne supérieure est la ligne où l’erreur s’est produite. L’exemple suivant illustre une pile d’appels AL.

Pile d’appels AL :

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

N’oubliez pas de partager les informations de la pile d’appels AL avec le fournisseur de l’extension.

### Erreur : Gén. Groupe compta. marché doit comporter une valeur dans Client: ’YOUR SHOPIFY STORE’. La valeur ne peut pas être zéro et le champ ne peut pas être vide

Sur la page **Fiche magasin Shopify**, remplissez le champ **Code modèle client** dans la fenêtre Fiche magasin  avec le modèle pour lequel **Groupe compta. marché** est renseigné. Le modèle client est utilisé pour créer des clients et pour calculer les prix de vente pour les documents de vente.

### Erreur : L’importation de données dans votre boutique Shopify n’est pas activée. Accédez à la fiche magasin pour l’activer

Sur la page **Fiche magasin Shopify**, activez le bouton bascule **Autoriser la synchronisation des données vers Shopify**. Ce paramètre aide à empêcher la boutique en ligne d’obtenir des données de démonstration de [!INCLUDE[prod_short](../includes/prod_short.md)].

### Erreur : Oauth error invalid_request: Could not find Shopify API application with api_key

Selon toute vraisemblance, vous utilisez l’[application intégrée](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), où l’URL du client a le format : `https://[application name].bc.dynamics.com`. Le connecteur Shopify ne fonctionne pas pour les applications intégrées. Pour en savoir plus, consultez [Quels sont les produits Microsoft pour lesquels le connecteur Shopify est disponible ?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)
