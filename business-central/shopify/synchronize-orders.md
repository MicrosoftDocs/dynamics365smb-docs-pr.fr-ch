---
title: Synchroniser et exécuter les commandes vente
description: Configurer et exécuter l’importation et le traitement des commandes vente à partir de Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Synchroniser et exécuter les commandes vente

Cet article décrit les paramètres et les étapes à effectuer pour synchroniser et exécuter les commandes vente avec Shopify dans [!INCLUDE[prod_short](../includes/prod_short.md)].

## Définir l’importation des commandes sur la Fiche magasin Shopify

Saisissez un **Code monnaie** si la boutique en ligne utilise une monnaie différente de DS. La devise spécifiée doit avoir des taux de change configurés. Si votre boutique en ligne utilise la même devise que [!INCLUDE[prod_short](../includes/prod_short.md)], laissez le champ vide. 

Vous pouvez voir la devise du magasin dans les paramètres [Détails du magasin](https://www.shopify.com/admin/settings/general) dans votre Admin Shopify. Shopify peut être configuré pour accepter différentes devises, cependant, les commandes importées dans [!INCLUDE[prod_short](../includes/prod_short.md)] utilisent la devise du magasin.

Une commande Shopify classique peut inclure des coûts en plus du sous-total, comme les frais d’expédition ou, s’ils sont activés, les pourboires. Ces montants sont validés directement dans le compte général que vous souhaitez utiliser pour des types de transactions spécifiques :

* **Compte frais d’expédition**
* **Compte carte cadeau vendu** ; en savoir plus dans la rubrique [Carte cadeau](synchronize-orders.md#gift-cards)
* **Compte de pourboires**  

Activez **Créer automatiquement des commandes** pour créer automatiquement des documents vente dans [!INCLUDE[prod_short](../includes/prod_short.md)] après l’importation de la commande Shopify.

Le document vente dans [!INCLUDE[prod_short](../includes/prod_short.md)] contient un lien vers la commande Shopify. Si vous sélectionnez le champ **N° commande sur n° ligne doc. Shopify**, ces informations sont répétées dans les ligne vente de type *Commentaire*.

Dans le champ **Origine zone recouvrement**, vous pouvez définir la priorité en matière de sélection du code zone recouvrement ou du groupe comptabilisation marché TVA en fonction de l’adresse. La commande Shopify importée contient des informations sur les taxes, mais celles-ci sont recalculées lorsque vous créez le document de vente. Il est donc important que les paramètres de TVA/taxe soient corrects dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Pour plus d’informations sur les taxes, voir [Configurer les taxes pour la connexion Shopify](setup-taxes.md).

### Mappage des conditions de livraison

Le **Code condition livraison** pour les documents vente importés de Shopify peut être rempli automatiquement. Vous devez configurer le **Mappage conditions livraison**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez définir le mappage pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Mappage conditions livraison**. Cela crée automatiquement les enregistrements des conditions de livraison définis dans les paramètres [**Expédition**](https://www.shopify.com/admin/settings/payments) dans l’**administration Shopify**.
4. Dans le champ **Nom**, vous affichez le nom de la condition de livraison de Shopify.
5. Saisissez le **Code condition livraison** avec la condition de livraison correspondante dans [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Si plusieurs frais d’expédition sont associés à une commande vente, un seul est sélectionné comme la condition de livraison et est affecté au document vente.

### Cartographie de localisation

Le mappage de l’emplacement est requis à trois fins :

* Pour en savoir plus sur la façon de synchroniser le stock, voir [Synchroniser le stock sur Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Pour remplir le **Code d’emplacement** pour les documents de vente importés de Shopify. C’est important lorsque le bouton à bascule **Magasin Obligatoire** est activé dans la fiche **Paramètres stock**, sinon vous ne pourrez pas créer de documents vente.
* Pour mettre à jour la commande Shopify avec les informations d’exécution basées sur la page **Expédition vente enregistrée**.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez configurer le mappage des emplacements pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Emplacements** pour ouvrir les **Emplacements des magasins Shopify**.
4. Sélectionnez l’action **Obtenir les emplacements Shopify** pour importer tous les emplacements définis dans Shopify. Ils se trouvent dans les paramètres [**Emplacements**](https://www.shopify.com/admin/settings/locations) du volet **Administration Shopify**. Notez que l’emplacement marqué comme *Par défaut* sera utilisé lors de l’importation de commandes Shopify non remplies.
5. Entrez le **Code magasin par défaut** avec l’emplacement correspondant dans [!INCLUDE[prod_short](../includes/prod_short.md)].

## Exécuter la synchronisation des commandes

La procédure suivante décrit comment importer et mettre à jour les commandes vente.

> [!NOTE]  
> Les commandes archivées dans Shopify ne peuvent pas être importées. Désactivez l’option **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres **Validation** dans le volet **Administration Shopify** pour vérifier que toutes les commandes sont importées dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Pour importer des commandes archivées, utilisez l’action **Désarchiver les commandes** dans la page [Commandes](https://www.shopify.com/admin/orders) du volet  **Administration Shopify**.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez importer des commandes pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Commandes**.
4. Sélectionnez l’action **Synchroniser les commandes à partir de Shopify**.
5. Définissez des filtres sur les commandes si nécessaire. Par exemple, vous pouvez importer les commandes entièrement payées ou celles présentant un faible niveau de risque.

> [!NOTE]  
> Lors du filtrage par balise, vous devez utiliser les jetons de filtre `@` et `*`. Par exemple, si vous souhaitez importer des commandes contenant *tag1*, utilisez `@*tag1*`. `@` assurera que le résultat respecte la casse, tandis que `*` recherche des commandes avec plusieurs balises.

7. Cliquez sur le bouton **OK**.

Sinon, vous pouvez rechercher le traitement par lots **Synchroniser les commandes à partir de Shopify**.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. En savoir plus dans la section [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

## Passer en revue les commandes importées

Une fois l’importation terminée, vous pouvez explorer la commande Shopify et trouver toutes les informations associées comme les transactions de paiement, les frais d’expédition, le niveau de risque, les attributs et balises de commande ou les exécutions, si la commande a déjà été exécutée dans Shopify. Vous pouvez également voir les confirmations de commande envoyées au client en sélectionnant l’action **Page de statut Shopify**.

> [!NOTE]  
> Vous pouvez accéder directement à la fenêtre **Commandes Shopify** pour afficher les commandes dont le statut est défini sur *Ouvert* dans tous les magasins. Pour consulter les commandes terminées, vous devez ouvrir la page **Commandes Shopify** à partir de la fenêtre **Fiche magasin Shopify** spécifique.

## Créer des documents vente dans Business Central

Si le bouton à bascule **Créer automatiquement des commandes** est activée sur la **Fiche magasin Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tente de créer un document vente après l’importation de la commande. Si des problèmes tels qu’un client ou un produit manquant surviennent, vous devrez les résoudre, puis créer à nouveau la commande vente.

### Pour créer des documents vente

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les commandes pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Commandes**.
4. Sélectionnez la commande pour laquelle vous voulez créer un document vente et sélectionnez l’action **Créer documents vente**.
5. Choisissez **Oui**.

Si la commande Shopify exige une exécution, une **Commande vente** est créée. Pour les commandes Shopify exécutées, telles que les commandes qui ne contiennent qu’une carte-cadeau ou qui sont déjà traitées dans Shopify, une **Facture vente** est créée.

Un document vente est maintenant créé et peut être géré en utilisant les fonctionnalités standard de [!INCLUDE[prod_short](../includes/prod_short.md)].

### Gérer les clients manquants

Si vos paramètres empêchent la création automatique d’un client et qu’un client existant approprié est introuvable, vous devez attribuer un client à la commande Shopify manuellement. Il explique plusieurs méthodes pour y parvenir :

* Vous pouvez attribuer le **N° donneur d’ordre** et **N° client facturé** directement dans la page **Commandes Shopify** en choisissant un client dans la liste des clients existants.
* Vous pouvez sélectionner un code modèle client, puis créer et affecter le client par l’action **Créer un client** dans la page **Commandes Shopify**. Remarquez que le client Shopify doit avoir au moins une adresse. Les commandes créées via le canal de vente du PDV Shopify manquent souvent de détails d’adresse.
* Vous pouvez mapper un client existant avec le **Client Shopify** existant dans la fenêtre **Clients Shopify**, puis sélectionner l’action **Trouver le mappage** dans la page **Commandes Shopify**.

### Comment le connecteur choisit le client à utiliser

La fonction *Importer la commande à partir de Shopify* tente de sélectionner le client dans l’ordre suivant :

1. Si le champ **N° client par défaut** est défini dans **Modèle client Shopify** pour le pays correspondant, le **N° client par défaut** est utilisé quels que soient les paramètres dans les champs **Importation client à partir de Shopify** et **Type de mappage client**. En savoir plus sur [Modèle client par pays](synchronize-customers.md#customer-template-per-country).
2. Si le champ **Importation client à partir de Shopify** est défini sur *Aucun* et le champ **N° client par défaut** est défini sur la page **Fiche magasin Shopify**, alors le **N° client par défaut** est utilisé.

Les étapes suivantes dépendent du champ **Type de mappage client**.

* **Toujours prendre le client par défaut**, puis le connecteur utilise le client défini dans le champ **N° client par défaut** dans la page **Fiche magasin Shopify**.
* **Par e-mail/téléphone**, le connecteur tente d’abord de trouver le client existant par ID, puis par e-mail, puis par téléphone. Si le client est introuvable, le connecteur crée un client.
* **Par informations de facturation**, le connecteur tente d’abord de trouver le client existant par ID, puis par adresse facturation. Si le client est introuvable, le connecteur crée un client.

> [!NOTE]  
> Le connecteur utilise les informations de l’adresse facturation et crée le client facturé dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Le client vendeur est le même que le client facturé.

### Impact des modifications des commandes

Dans Shopify :

|Modifier|Impact|
|------|-----------|
|Modifier l’emplacement d’exécution | L’emplacement d’origine sera synchronisé avec [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Modifier le lieu d’exécution et enregistrer l’exécution dans Shopify| Si la commande a déjà été importée, les lignes ne seront pas mises à jour. Sinon, la commande importée utilisera l’emplacement d’exécution. |
|Modifier une commande et modifier la quantité| L’en-tête de la commande et les tableaux supplémentaires seront mis à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], les lignes ne le seront pas. |
|Modifier une commande et ajouter un nouvel article | L’en-tête de la commande sera mis à jour, pas les lignes. |

Dans [!INCLUDE[prod_short](../includes/prod_short.md)] :

|Modifier|Impact|
|------|-----------|
|Changez l’emplacement en un autre emplacement, mappé sur les magasins Shopify. Validez l’expédition. | Après la synchronisation de l’exécution, l’emplacement sera mis à jour dans Shopify. |
|Changez l’emplacement en un autre emplacement, non mappé sur les magasins Shopify. Validez l’expédition. | Le traitement ne sera pas synchronisé avec Shopify. |
|Modifiez la diminution de quantité. Validez l’expédition. | La commande Shopify est marquée comme partiellement exécutée. |
|Ajoutez un nouvel article. Validez l’expédition. | La commande Shopify est marquée comme exécutée. Les lignes ne sont pas mises à jour. |

## Synchroniser les livraisons avec Shopify

Lorsqu’une commande vente créée à partir d’une commande Shopify est livrée, vous pouvez synchroniser les livraisons avec Shopify.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Synchroniser livraisons avec Shopify**, puis sélectionnez le lien associé.
2. Définissez les filtres sur les livraisons si nécessaire. Par exemple, vous pouvez mettre à jour une livraison validée à une date donnée.
3. Cliquez sur le bouton **OK**.

La commande dans Shopify est marquée comme exécutée. Le client reçoit automatiquement un message électronique ou un SMS d’avis d’expédition. Si un transporteur et un code de suivi sont spécifiés sur la livraison, les informations de suivi sont indiquées dans le message électronique.

Sinon, utilisez l’action **Synchroniser les expéditions** sur les pages Commandes vente Shopify ou Magasin Shopify.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. En savoir plus dans la section [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

>[Important] L’emplacement, y compris l’emplacement vide, défini dans la ligne d’expédition enregistrée doit avoir un enregistrement correspondant dans l’emplacement Shopify. Sinon, cette ligne ne sera pas renvoyée à Shopify. En savoir plus sur le [Mappage d’emplacement](synchronize-orders.md#location-mapping).

N’oubliez pas d’exécuter **Synchroniser les commandes à partir de Shopify** pour mettre à jour le statut d’exécution d’une commande dans [!INCLUDE[prod_short](../includes/prod_short.md)]. La fonctionnalité du connecteur archive également les commandes entièrement payées et exécutées à la fois dans Shopify et dans [!INCLUDE[prod_short](../includes/prod_short.md)] si les conditions sont remplies.

### Transporteurs et URL de suivi

Si le document **Expédition vente enregistrée** contient le **Code transporteur** et/ou le **N° récépissé**, ces informations sont envoyées à Shopify et au client dans le message électronique de confirmation de livraison.

La société de suivi est renseignée dans l’ordre de priorité suivant (du plus élevé au plus faible), en fonction de l’enregistrement du transporteur :

* **Société de suivi Shopify**
* **Nom**
* **Code**

Si le champ **URL de suivi des colis** est rempli pour l’enregistrement du transporteur, la confirmation de livraison contient aussi une URL de suivi.

## Cartes cadeaux

Dans le magasin Shopify, vous pouvez vendre des cartes cadeaux, qui peuvent être utilisées pour acheter des produits.

En matière de cartes cadeaux, il est important de saisir une valeur dans le champ **Compte carte cadeau vendu** dans la fenêtre **Fiche magasin Shopify**. La carte cadeau vendue est synchronisée avec les commandes en cours. Une carte cadeau lettrée est également importée avec la commande mais en tant que transaction. Notez que la carte cadeau ne diminue pas le montant à facturer.

Pour examiner les cartes cadeaux lettrées et émises, sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Cartes cadeaux**, puis choisissez le lien associé.

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
