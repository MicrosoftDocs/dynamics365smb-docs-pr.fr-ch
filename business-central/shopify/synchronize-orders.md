---
title: Synchroniser et exécuter les commandes vente
description: Configurer et exécuter l’importation et le traitement des commandes vente à partir de Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ce11aa8766550e72cab2f811ef6602dba4271211
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076320"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Synchroniser et exécuter les commandes vente

Cet article décrit les paramètres et les étapes à effectuer pour synchroniser et exécuter les commandes vente à partir de Shopify dans [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Définir l’importation des commandes sur la Fiche magasin Shopify

Une commande Shopify régulière peut contenir des montants supplémentaires, comme des frais d’expédition, ou, si activés, des pourboires. Ces montants sont directements imputés sur les comptes généraux. Choisissez le compte général qui doit être utilisé pour certaines transactions :

- **Compte frais d’expédition**
- **Compte carte cadeau vendu**, pour plus d’informations, voir [Carte cadeau](synchronize-orders.md#gift-cards).
- **Compte de pourboires**  

Activez **Créer automatiquement des commandes** pour créer automatiquement des documents vente dans [!INCLUDE[prod_short](../includes/prod_short.md)] après l’importation de la commande Shopify.
Le document vente dans [!INCLUDE[prod_short](../includes/prod_short.md)] contient un lien vers la commande Shopify. Si vous sélectionnez le champ **N° commande sur n° ligne doc. Shopify**, ces informations sont répétées dans les ligne vente de type *Commentaire*.

Dans le champ **Origine zone recouvrement**, vous pouvez définir la priorité en matière de sélection du code zone recouvrement ou du groupe comptabilisation marché TVA en fonction de l’adresse. Cette étape est pertinente pour les pays avec taxe de vente, mais peut être utilisée pour les pays avec TVA. Pour plus d’informations, voir [Remarques sur les taxes](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Mappage des conditions de livraison

Le **Code condition livraison** pour les documents vente importés de Shopify peut être rempli automatiquement. Vous devez configurer le **Mappage conditions livraison**.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez définir le mappage pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Mappage conditions livraison**. Les enregistrements des conditions de livraison définis dans les paramètres [**Expédition**](https://www.shopify.com/admin/settings/payments) dans l’**administration Shopify** sont créés automatiquement.
4. Dans le champ **Nom**, vous affichez le nom de la condition de livraison de Shopify.
5. Saisissez le **Code condition livraison** avec la condition de livraison correspondante dans [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Si plusieurs frais d’expédition sont associés à une commande vente, un seul est sélectionné comme la condition de livraison et est affecté au document vente.

### <a name="payment-method-mapping"></a>Mappage du mode de paiement

Pour remplir le **Code mode de règlement** pour les documents vente importés de Shopify automatiquement, vous devez configurer le **Mappage du mode de paiement**.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez définir le mappage pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Mappage du mode de paiement**.
4. Dans les champs **Passerelle** et **Société de carte de crédit**, saisissez le nom du mode de paiement Shopify. L’enregistrement est créé automatiquement lorsque vous importez des commandes Shopify.
5. Saisissez le **Code mode de règlement** avec le mode de règlement correspondant dans [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Définissez la **Priorité** pour les cas où le client utilise plusieurs moyens de paiement. Le mode de paiement avec la priorité la plus élevée est sélectionné dans le document vente. Si les deux modes de paiement ont la même priorité, le mode de paiement avec le montant le plus élevé est utilisé.

### <a name="location-mapping"></a>Cartographie de localisation

Pour remplir le **Code magasin** pour les documents vente importés de Shopify automatiquement, vous devez configurer les **Emplacements des magasins Shopify**.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez configurer le mappage des emplacements pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Emplacements** pour ouvrir les **Emplacements des magasins Shopify**.
4. Sélectionnez l’action **Obtenir les emplacements Shopify** pour importer tous les emplacements définis dans Shopify. Ils se trouvent dans les paramètres [**Emplacements**](https://www.shopify.com/admin/settings/locations) du volet **Administration Shopify**. Notez que l’emplacement marqué comme *Par défaut* sera utilisé lors de l’importation de commandes Shopify non remplies.
5. Entrez le **Code magasin par défaut** avec l’emplacement correspondant dans [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Vous devez configurer le mappage d’emplacement si le bouton à bascule **Magasin Obligatoire** est activé dans la fiche **Paramètres stock**, sinon vous ne pourrez pas créer de documents vente.

## <a name="run-the-order-synchronization"></a>Exécuter la synchronisation des commandes

La procédure suivante décrit comment importer et mettre à jour les commandes vente.

> [!NOTE]  
> Les commandes archivées dans Shopify ne peuvent pas être importées. Désactivez l’option **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres **Validation** dans le volet **Administration Shopify** pour vérifier que toutes les commandes sont importées dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Pour importer des commandes archivées, utilisez l’action **Désarchiver les commandes** dans la page [Commandes](https://www.shopify.com/admin/orders) du volet Administration Shopify.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez importer des commandes pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Commandes**.
4. Sélectionnez l’action **Synchroniser les commandes à partir de Shopify**.
5. Définissez des filtres sur les commandes si nécessaire. Par exemple, vous pouvez importer les commandes entièrement payées ou celles présentant un faible niveau de risque.
6. Cliquez sur le bouton **OK**.

Sinon, vous pouvez rechercher le traitement par lots **Synchroniser les commandes à partir de Shopify**.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. Pour plus d’informations, voir [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Passer en revue les commandes importées

Une fois l’importation terminée, vous pouvez explorer la commande Shopify et rechercher toutes les informations connexes. Vous pouvez par exemple rechercher les transactions de paiement, les frais d’expédition, le niveau de risque ou les exécutions si la commande a déjà été exécutée dans Shopify. Vous pouvez également voir les confirmations de commande envoyées au client en sélectionnant l’action **Page de statut Shopify**.

> [!NOTE]  
> Vous pouvez accéder directement à la fenêtre **Commandes Shopify** pour afficher les commandes dont le statut est défini sur *Ouvert* dans tous les magasins. Pour consulter les commandes terminées, vous devez ouvrir la page **Commandes Shopify** à partir de la fenêtre **Fiche magasin Shopify** spécifique.

## <a name="create-sales-documents-in-business-central"></a>Créer des documents vente dans Business Central

Si le bouton à bascule **Créer automatiquement des commandes** est activée sur la **Fiche magasin Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tente de créer un document vente après l’importation de la commande. Si le processus rencontre des problèmes, par exemple si un client ou un produit est manquant, vous devrez résoudre le problème. Ensuite, vous pouvez essayer de créer à nouveau la commande vente.

### <a name="to-create-sales-documents"></a>Pour créer des documents vente

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les commandes pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Commandes**.
4. Sélectionnez la commande pour laquelle vous voulez créer un document vente et sélectionnez l’action **Créer documents vente**.
5. Choisissez **Oui**.

Si la commande Shopify exige une exécution, une **Commande vente** est créée. Pour les commandes Shopify exécutées, telles que les commandes qui ne contiennent qu’une carte-cadeau ou qui sont déjà traitées dans Shopify, une **Facture vente** est créée.

Un document vente est maintenant créé et peut être géré en utilisant les fonctionnalités standard [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="manage-missing-customers"></a>Gérer les clients manquants

Si vos paramètres empêchent la création automatique d’un client et qu’un client existant approprié est introuvable, attribuez un client à la commande Shopify manuellement. Plusieurs options sont disponibles :

- Vous pouvez attribuer le **N° donneur d’ordre** directement dans la **Commande Shopify** en choisissant un client dans la liste des clients existants.
- Vous pouvez sélectionner un code modèle client, créer et affecter le client par l’action **Créer un client** dans la page **Commandes Shopify**.
- Vous pouvez mapper un client existant avec le **Client Shopify** existant dans la fenêtre **Clients Shopify**, puis sélectionner l’action **Trouver le mappage** dans la page **Commandes Shopify**.

### <a name="tax-remarks"></a>Remarques sur les taxes

Même si la commande Shopify importée contient des informations sur les taxes, les taxes sont recalculées lorsque vous créez le document vente. Pour ce nouveau calcul, il est important que les paramètres TVA/Taxe soient corrects dans [!INCLUDE[prod_short](../includes/prod_short.md)].

- Plusieurs taux de TVA/Taxe sur les produits. Par exemple, certaines catégories de produits sont soumises à des taux de taxe réduits. Ces articles doivent exister dans [!INCLUDE[prod_short](../includes/prod_short.md)] et être mappés avec les produits Shopify. Sinon, avec la création automatique des articles manquants, le groupe comptabilisation produit TVA est utilisé.

- Taux de taxe dépendant de l’adresse. Utilisez le champ **Priorité zone recouvrement** avec le tableau **Modèles client** pour remplacer la logique standard qui remplit le **Code zone recouvrement** dans le document vente. Le champ **Priorité zone recouvrement** indique la priorité à partir de laquelle la fonction doit prendre des informations sur le pays/la région et l’état/la province. L’enregistrement correspondant dans les modèles client Shopify est ensuite trouvé et les champs **Code zone recouvrement**, **Soumis à recouvrement** et **Groupe compta. marché TVA** sont utilisés lors de la création d’un document vente.

- Prix TTC. Le champ **Prix incluant les taxes**/**Prix TTC** dans le document vente créé ne dépend pas du client, mais du **Modèle client** due la fiche magasin Shopify ou du modèle client par pays.

### <a name="impact-of-edits-of-orders"></a>Impact des modifications des commandes

|Modifier|Impact|
|------|-----------|
|Dans Shopify, modifier l’emplacement d’exécution | L’emplacement d’origine sera synchronisé avec [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Dans Shopify, modifier une commande et modifier la quantité| L’en-tête de la commande et les tableaux supplémentaires seront mis à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], les lignes ne le seront pas. |
|Dans Shopify, modifier une commande et ajouter un nouvel article | L’en-tête de la commande sera mis à jour, pas les lignes. |
|Dans [!INCLUDE[prod_short](../includes/prod_short.md)], changez l’emplacement en un autre emplacement, mappé sur les Magasins Shopify. Validez l’expédition. | Après la synchronisation de l’exécution, l’emplacement sera mis à jour dans Shopify. |
|Dans [!INCLUDE[prod_short](../includes/prod_short.md)], changez l’emplacement en un autre emplacement, non mappé sur les Magasins Shopify. Validez l’expédition. | Le traitement ne sera pas synchronisé avec Shopify. |
|Dans [!INCLUDE[prod_short](../includes/prod_short.md)], changez la diminution de quantité. Validez l’expédition. | La commande Shopify est marquée comme partiellement exécutée. |
|Dans [!INCLUDE[prod_short](../includes/prod_short.md)], ajoutez un nouvel article. Validez l’expédition. | La commande Shopify est marquée comme exécutée. Les lignes ne sont pas mises à jour. |

## <a name="synchronize-shipments-to-shopify"></a>Synchroniser les livraisons avec Shopify

Lorsqu’une commande vente créée à partir d’une commande Shopify est livrée, vous pouvez synchroniser les livraisons avec Shopify.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Synchroniser livraisons avec Shopify**, puis sélectionnez le lien associé.
2. Définissez les filtres sur les livraisons si nécessaire. Par exemple, vous pouvez mettre à jour une livraison validée à une date donnée.
3. Cliquez sur le bouton **OK**.

La commande dans Shopify est marquée comme exécutée. Le client reçoit automatiquement un message électronique ou un SMS d’avis d’expédition. Si un transporteur et un code de suivi sont spécifiés sur la livraison, les informations de suivi sont indiquées dans le message électronique.

> [!NOTE]  
> N’oubliez pas d’exécuter **Synchroniser les commandes à partir de Shopify** pour mettre à jour le statut d’exécution de la commande dans [!INCLUDE[prod_short](../includes/prod_short.md)]. La fonctionnalité du connecteur archive également les commandes entièrement payées et exécutées à la fois dans Shopify et dans [!INCLUDE[prod_short](../includes/prod_short.md)] si les conditions sont remplies.

### <a name="shipping-agents-and-tracking-url"></a>Transporteurs et URL de suivi

Si le document **Expédition vente enregistrée** contient le **Code transporteur** et/ou le **N° récépissé**, ces informations sont envoyées à Shopify et au client final dans le message électronique de confirmation de livraison.

La société de suivi est renseignée en fonction de l’enregistrement du transporteur avec les priorités suivantes (de la plus élevée à la plus faible) :

- **Société de suivi Shopify**
- **Nom**
- **Code**

Si le champ **URL de suivi des colis** est rempli pour l’enregistrement du transporteur, la confirmation de livraison contient aussi une URL de suivi.

## <a name="gift-cards"></a>Cartes cadeaux

Dans le magasin Shopify, vous pouvez vendre des cartes cadeaux, qui peuvent ensuite être utilisées pour acheter des produits.

En matière de cartes cadeaux, il est important de saisir une valeur dans le champ **Compte carte cadeau vendu** dans la fenêtre **Fiche magasin Shopify**. La carte cadeau vendue est synchronisée avec les commandes en cours. Une carte cadeau lettrée est également importée avec la commande mais en tant que transaction. Notez que la carte cadeau ne diminue pas le montant à facturer.

Pour examiner les cartes cadeaux lettrées et émises, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Cartes cadeaux**, puis choisissez le lien associé.

## <a name="transactions"></a>Transactions

Les transactions réalisées sur Shopify sont synchronisées avec les commandes et s’affichent dans la page *Commandes Shopify*.

Pour examiner toutes les transactions, sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Transactions**, puis choisissez le lien associé.

## <a name="payouts"></a>Règlements

Si votre magasin a activé Shopify Payments, vous recevez les paiements via *Règlements Shopify* lorsqu’un client paie en utilisant le service Shopify Payments et les règlements accélérés.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les règlements pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les règlements**.

Pour examiner tous les règlements, sélectionnez l’icône en forme ![d’ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Règlements**, puis choisissez le lien associé.

## <a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
