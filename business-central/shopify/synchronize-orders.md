---
title: Synchroniser et exécuter les commandes vente
description: Configurer et exécuter l’importation et le traitement des commandes vente à partir de Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-and-fulfill-sales-orders"></a>Synchroniser et exécuter les commandes vente

Cet article décrit les paramètres et les étapes à effectuer pour synchroniser et exécuter les commandes vente avec Shopify dans [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Définir l’importation des commandes sur la Fiche magasin Shopify

Saisissez un **Code monnaie** si la boutique en ligne utilise une monnaie différente de DS. La devise spécifiée doit avoir des taux de change configurés. Si votre boutique en ligne utilise la même devise que [!INCLUDE[prod_short](../includes/prod_short.md)], laissez le champ vide. 

Vous pouvez vérifier à la devise du magasin dans les paramètres [Détails du magasin](https://www.shopify.com/admin/settings/general) dans votre administrateur Shopify. Shopify peut être configuré pour accepter différentes devises, cependant, les commandes importées dans [!INCLUDE[prod_short](../includes/prod_short.md)] utilisent la devise du magasin.

Une commande Shopify classique peut inclure des coûts en plus du sous-total, comme les frais d’expédition ou, s’ils sont activés, les pourboires. Ces montants sont validés directement dans le compte général que vous souhaitez utiliser pour des types de transactions spécifiques :

* **Compte frais d’expédition**
* **Compte carte cadeau vendu** ; en savoir plus dans la rubrique [Carte cadeau](synchronize-orders.md#gift-cards)
* **Compte de pourboires**  

Activez **Créer automatiquement des commandes** pour créer automatiquement des documents vente dans [!INCLUDE[prod_short](../includes/prod_short.md)] après l’importation de la commande Shopify.

Si vous souhaitez lancer automatiquement un document de vente, activez le bouton bascule **Lancer automatiquement les commandes vente**.

Si vous sélectionnez le champ **N° commande Shopify sur n° ligne doc.**, [!INCLUDE [prod_short](../includes/prod_short.md)] insère les ligne vente de type **Commentaire** avec le numéro de commande Shopify.

>[!NOTE]
>Le document de vente dans [!INCLUDE[prod_short](../includes/prod_short.md)] est lié à la commande Shopify, et vous pouvez ajouter le **N° de commande Shopify** aux pages de liste ou de carte pour les bons de commande, les factures et l’expédition. Pour en savoir plus sur l’ajout d’un champ, accédez à [Commencer à personnaliser une page via la bannière **Personnalisation**](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

Dans le champ **Priorité zone recouvrement**, vous pouvez définir la priorité en matière de sélection du code zone recouvrement sur les adresses dans la commande. La commande Shopify importée contient des informations sur les taxes. Les taxes sont recalculées lorsque vous créez les documents de vente, il est donc important que les paramètres de TVA/taxe soient corrects dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Pour plus d’informations sur les taxes, accédez à [Configurer les taxes pour la connexion Shopify](setup-taxes.md).

Précisez comment vous traiterez les retours et les remboursements :

* **Vide** spécifie que vous n’importez pas et ne traitez pas les retours et les remboursements.
* **Importer uniquement** indique que vous importez des informations, mais vous créerez manuellement l’avoir correspondant.
* **Créer automatiquement une note de crédit** spécifie que vous importez des informations et [!INCLUDE[prod_short](../includes/prod_short.md)] crée automatiquement les notes de crédit. Cette option nécessite que vous activiez le bouton à bascule **Créer automatiquement une commande client**.

Spécifiez un emplacement pour les retours et des comptes généraux pour les remboursements de marchandises et autres remboursements.

* **Articles non réapprovisionnés du compte de remboursement** : indique un n° compte général pour les articles pour lesquels vous ne souhaitez pas avoir de correction de stock.
* **Compte de remboursement** : indique un compte général pour la différence entre le montant total remboursé et le montant total des articles.

En savoir plus sur [Retours et remboursements](synchronize-orders.md#returns-and-refunds)

### <a name="shipment-method-mapping"></a>Mappage des conditions de livraison

Le **Code condition livraison** pour les documents vente importés de Shopify peut être rempli automatiquement. Vous devez configurer le **Mappage conditions livraison**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez définir le mappage pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Mappage conditions livraison**. Cela crée automatiquement les enregistrements des conditions de livraison définis dans les paramètres [**Expédition**](https://www.shopify.com/admin/settings/payments) dans l’**administration Shopify**.
4. Dans le champ **Nom**, vous affichez le nom de la condition de livraison de Shopify.
5. Saisissez le **Code condition livraison** avec la condition de livraison correspondante dans [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Si plusieurs frais d’expédition sont associés à une commande vente, un seul est sélectionné comme la condition de livraison et est affecté au document vente.

### <a name="location-mapping"></a>Cartographie de localisation

Le mappage de l’emplacement est nécessaire pour compléter le **Code magasin** pour les lignes de documents vente importées depuis Shopify. C’est important lorsque le bouton à bascule **Magasin Obligatoire** est activé dans la fiche **Paramètres stock**, sinon vous ne pourrez pas créer de documents vente.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez configurer le mappage des emplacements pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Emplacements** pour ouvrir les **Emplacements des magasins Shopify**.
4. Sélectionnez l’action **Obtenir les emplacements Shopify** pour importer tous les emplacements définis dans Shopify. Ils se trouvent dans les paramètres [**Emplacements**](https://www.shopify.com/admin/settings/locations) du volet **Administration Shopify**. 
5. Entrez le **Code magasin par défaut** avec l’emplacement correspondant dans [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Le mappage de l’emplacement est également utilisé pour synchroniser l’inventaire. Pour plus d’informations, consultez [Synchroniser l’inventaire sur Shopify](synchronize-items.md#sync-inventory-to-shopify).
  
## <a name="run-the-order-synchronization"></a>Exécuter la synchronisation des commandes

La procédure suivante décrit comment importer et mettre à jour les commandes vente.

> [!NOTE]  
> Les commandes archivées dans Shopify ne peuvent pas être importées. Si vous devez vérifier l’état de la commande, ouvrez la commande à partir de la page [commandes](https://www.shopify.com/admin/orders) du panneau **Shopify d’administration** et examinez-la. détails de la commande.
> 
> Désactivez l’option **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres **Validation** dans le volet **Administration Shopify** pour vérifier que toutes les commandes sont importées dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Pour importer des commandes archivées, utilisez l’action **Désarchiver les commandes** dans la page [Commandes](https://www.shopify.com/admin/orders) du volet  **Administration Shopify**. 

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez importer des commandes pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Commandes**.
4. Sélectionnez l’action **Synchroniser les commandes à partir de Shopify**.
5. Définissez des filtres sur les commandes si nécessaire. Par exemple, vous pouvez importer les commandes entièrement payées ou celles présentant un faible niveau de risque.

> [!NOTE]  
> Lors du filtrage par balise, vous devez utiliser les jetons de filtre `@` et `*`. Par exemple, si vous souhaitez importer des commandes contenant *tag1*, utilisez `@*tag1*`. `@` assurera que le résultat ne respecte pas la casse, tandis que `*` recherche des commandes avec plusieurs balises.

6. Cliquez sur le bouton **OK**.

Sinon, vous pouvez rechercher le traitement par lots **Synchroniser les commandes à partir de Shopify**.

Vous pouvez programmer la tâche pour qu’elle soit exécutée automatiquement. En savoir plus dans la section [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

### <a name="under-the-hood"></a>Informations détaillées

Le connecteur Shopify importe les commandes en deux étapes :

1.  Il importe les en-têtes de commande dans la table **Commandes Shopify à importer** lorsqu’ils remplissent certaines conditions :
    
* Ils ne sont pas archivés. Cela signifie que vous pouvez inclure ou exclure des commandes de la synchronisation en les archivant ou en les désarchivant dans l’administrateur Shopify.
* Ils ont été créés ou modifiés après la dernière synchronisation. Cela signifie que vous pouvez forcer la réimportation d’une commande spécifique si vous la modifiez, par exemple en ajoutant les **Notes** ou **Balise**.

2.  Il importe les commandes Shopify et des informations supplémentaires.
* Le connecteur Shopify traite tous les enregistrements de la table **Commandes Shopify à importer** qui correspondent aux critères de filtre que vous avez définis dans la page de demande **Synchroniser les commandes à partir de Shopify**. Par exemple, les balises, le canal ou le statut d’exécution. Si vous n’avez spécifié aucun filtre, il traite tous les enregistrements.
* Lors de l’importation d’une commande Shopify, le connecteur Shopify demande des informations supplémentaires à Shopify :

    * En-tête de commande
    * Lignes de commande
    * Informations d’expédition et d’exécution
    * Transactions
    * Retours et remboursements, s’ils sont configurés

La page **Commande Shopify à importer** est utile pour résoudre les problèmes d’importation de commandes. Vous pouvez évaluer les commandes disponibles et effectuer les étapes suivantes :

* Vérifiez si une erreur a bloqué l’importation d’une commande spécifique et explorez les détails de l’erreur. Vérifiez le champ **Contient une erreur**.
* Traitez uniquement des commandes spécifiques. Vous devrez remplir le champ **Code magasin**, sélectionner une ou plusieurs commandes, puis choisir l’action **Importer les commandes sélectionnées**.
* Supprimez des commandes de la page **Commande Shopify à importer** pour les exclure de la synchronisation.

## <a name="review-imported-orders"></a>Passer en revue les commandes importées

Une fois l’importation terminée, vous pouvez explorer la commande Shopify et trouver toutes les informations associées comme les transactions de paiement, les frais d’expédition, le niveau de risque, les attributs et balises de commande ou les exécutions, si la commande a déjà été exécutée dans Shopify. Vous pouvez également voir les confirmations de commande envoyées au client en sélectionnant l’action **Page de statut Shopify**.

> [!NOTE]  
> Vous pouvez accéder directement à la fenêtre **Commandes Shopify** pour afficher les commandes dont le statut est défini sur *Ouvert* dans tous les magasins. Pour consulter les commandes terminées, vous devez ouvrir la page **Commandes Shopify** à partir de la fenêtre **Fiche magasin Shopify** spécifique.

## <a name="create-sales-documents-in-business-central"></a>Créer des documents vente dans Business Central

Si le bouton à bascule **Créer automatiquement des commandes** est activée sur la **Fiche magasin Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tente de créer un document vente après l’importation de la commande. Si des problèmes tels qu’un client ou un produit manquant surviennent, vous devrez les résoudre, puis créer à nouveau la commande vente.

### <a name="to-create-sales-documents"></a>Pour créer des documents vente

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les commandes pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Commandes**.
4. Sélectionnez la commande pour laquelle vous voulez créer un document vente et sélectionnez l’action **Créer documents vente**.
5. Choisissez **Oui**.

Si la commande Shopify exige une exécution, une **Commande vente** est créée. Pour les commandes Shopify exécutées, telles que les commandes qui ne contiennent qu’une carte-cadeau ou qui sont déjà traitées dans Shopify, une **Facture vente** est créée.

Un document vente est maintenant créé et peut être géré en utilisant les fonctionnalités standard de [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="manage-missing-customers"></a>Gérer les clients manquants

Si vos paramètres empêchent la création automatique d’un client et qu’un client existant approprié est introuvable, vous devez attribuer un client à la commande Shopify manuellement. Il explique plusieurs méthodes pour y parvenir :

* Vous pouvez attribuer le **N° donneur d’ordre** et **N° client facturé** directement dans la page **Commandes Shopify** en choisissant un client dans la liste des clients existants.
* Vous pouvez sélectionner un code modèle client, puis créer et affecter le client par l’action **Créer un client** dans la page **Commandes Shopify**. Remarquez que le client Shopify doit avoir au moins une adresse. Les commandes créées via le canal de vente du PDV Shopify manquent souvent de détails d’adresse.
* Vous pouvez mapper un client existant avec le **Client Shopify** existant dans la fenêtre **Clients Shopify**, puis sélectionner l’action **Trouver le mappage** dans la page **Commandes Shopify**.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Comment le connecteur choisit le client à utiliser

La fonction *Importer la commande à partir de Shopify* tente de sélectionner le client dans l’ordre suivant :

1. Si le champ **N° client par défaut** est défini dans **Modèle client Shopify** pour le **Code pays/région destinataire**, puis le **N° client par défaut** est utilisé quels que soient les paramètres dans les champs **Importation client à partir de Shopify** et **Type de mappage client**. En savoir plus sur [Modèle client par pays](synchronize-customers.md#customer-template-per-countryregion).
2. Si le champ **Importation client à partir de Shopify** est défini sur *Aucun* et le champ **N° client par défaut** est défini sur la page **Fiche magasin Shopify**, alors le **N° client par défaut** est utilisé.

Les étapes suivantes dépendent du champ **Type de mappage client**.

* **Toujours prendre le client par défaut**, puis le connecteur utilise le client défini dans le champ **N° client par défaut** dans la page **Fiche magasin Shopify**.
* **Par e-mail/téléphone**, le connecteur tente d’abord de trouver le client existant par ID, puis par e-mail, puis par téléphone. Si le client est introuvable, le connecteur crée un client.
* **Par informations de facturation**, le connecteur tente d’abord de trouver le client existant par ID, puis par adresse facturation. Si le client est introuvable, le connecteur crée un client.

> [!NOTE]  
> Le connecteur utilise les informations de l’adresse facturation et crée le client facturé dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Le client vendeur est le même que le client facturé.

### <a name="different-processing-rules-for-orders"></a>Différentes règles de traitement des commandes

Vous souhaiterez peut-être traiter les commandes différemment en fonction d’une règle. Par exemple, les commandes provenant d’un canal de vente spécifique, comme le point de vente, doivent utiliser le client par défaut, mais vous souhaitez que votre boutique en ligne ait de vraies informations sur le client.

Une façon de répondre à cette exigence consiste à créer une fiche Shopify Shop supplémentaire et à utiliser des filtres dans la page de demande **Synchroniser des commandes à partir de Shopify** .

Exemple : vous avez une boutique en ligne ainsi qu’un PDV Shopify. Pour votre PDV, vous souhaitez utiliser un client fixe, mais pour votre boutique en ligne, vous souhaitez créer des clients dans [!INCLUDE[prod_short](../includes/prod_short.md)]. La procédure suivante répertorie les étapes de haut niveau. Pour en savoir plus, consultez les articles d’aide correspondants.

1. Créez une boutique Shopify appelée *MAGASIN* et associez-la à votre compte Shopify.
2. Configurez la synchronisation article/produit pour que ce magasin gère les informations produit.
3. Spécifiez que les clients sont importés avec les commandes. Le connecteur doit trouver des clients en recherchant leur adresse électronique. S’il ne trouve pas d’adresse, il utilise le modèle de client pour créer un client.
4. Créez une boutique Shopify appelée *PDV* et associez-la au même compte Shopify.
6. Assurez-vous que la synchronisation article/produit est désactivée.
7. Sélectionnez le connecteur qui utilise le client par défaut.
8. Créez une entrée de file d’attente de tâches récurrentes pour l’état 30104 **Synchroniser les commandes à partir de Shopify**. Sélectionnez **MAGASIN** dans le champ **Code magasin Shopify** et utilisez des filtres pour saisir toutes les commandes sauf celles qui passent par le canal de vente PDV crée. Par exemple, **<>Point de vente**
9. Créez une entrée de file d’attente de tâches récurrentes pour l’état 30104 **Synchroniser les commandes à partir de Shopify**. Sélectionnez **PDV** dans le champ **Code magasin Shopify** et utilisez des filtres pour saisir les commandes générées par le canal de vente PDV. Par exemple, **Point de vente**.

Chaque file d’attente importe et traite les commandes dans les filtres définis et utilise les règles de la fiche magasin Shopify correspondante. Par exemple, elles créent des commandes de point de vente pour le client par défaut.

>[!Important]
> Pour éviter les conflits lors du traitement des commandes, n’oubliez pas d’utiliser la même catégorie de file d’attente pour les deux entrées de file d’attente.

### <a name="impact-of-order-editing"></a>Impact des modifications des commandes

Dans Shopify :

|Modifier|Impact pour la commande déjà importée|Impact pour la commande importée pour la première fois|
|------|-----------|-----------|
|Modifier l’emplacement d’exécution | L’emplacement d’origine est dans les lignes | L’emplacement d’exécution est synchronisé avec [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Modifier une commande et accroître sa quantité| L’en-tête de la commande et les tableaux supplémentaires seront mis à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], les lignes ne le seront pas.| La commande importée utilise la nouvelle quantité|
|Modifier une commande et réduire sa quantité| L’en-tête de la commande et les tableaux supplémentaires seront mis à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], les lignes ne le seront pas.| La commande importée utilise la quantité d’origine, le champ Quantité réalisable contient une nouvelle valeur.|
|Modifier une commande et supprimer un article existant | L’en-tête de la commande et les tableaux supplémentaires seront mis à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], les lignes ne le seront pas.| L’article supprimé est toujours importé, le champ Quantité réalisable contient la valeur zéro. |
|Modifier une commande et ajouter un nouvel article | L’en-tête de la commande sera mis à jour, pas les lignes. | Les articles originaux et ajoutés sont importés. |
|Traiter la commande : remplir, mettre à jour les informations de paiement | L’en-tête de la commande est mis à jour, pas les lignes. |Le changement n’a aucun impact sur la façon dont la commande est importée.|
|Annuler une commande | L’en-tête de la commande est mis à jour, pas les lignes. |La commande annulée n’est pas importée |

Comme vous pouvez le constater, dans certains cas, il peut être raisonnable de supprimer la commande modifiée dans [!INCLUDE[prod_short](../includes/prod_short.md)] et de l’importer comme nouvelle.

Dans [!INCLUDE[prod_short](../includes/prod_short.md)] :

|Modifier|Impact|
|------|-----------|
|Changez l’emplacement en un autre emplacement, mappé sur les magasins Shopify. Validez l’expédition. | La commande est marquée comme exécutée. L’emplacement d’origine est utilisé. |
|Changez l’emplacement en un autre emplacement, non mappé sur les magasins Shopify. Validez l’expédition. | Le traitement ne sera pas synchronisé avec Shopify. |
|Réduisez la quantité. Validez l’expédition. | La commande Shopify est marquée comme partiellement exécutée. |
|Augmentez la quantité. Validez l’expédition. | Le traitement ne sera pas synchronisé avec Shopify. |
|Ajoutez un nouvel article. Validez l’expédition. | La commande Shopify est marquée comme exécutée. Les lignes ne sont pas mises à jour. |

## <a name="synchronize-shipments-to-shopify"></a>Synchroniser les livraisons avec Shopify

Lorsqu’une commande vente créée à partir d’une commande Shopify est livrée, vous pouvez synchroniser les livraisons avec Shopify.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Synchroniser livraisons avec Shopify**, puis sélectionnez le lien associé.
2. Définissez les filtres sur les livraisons si nécessaire. Par exemple, vous pouvez mettre à jour une livraison validée à une date donnée.
3. Cliquez sur le bouton **OK**.

La commande dans Shopify est marquée comme exécutée. Le client reçoit automatiquement un message électronique ou un SMS d’avis d’expédition. Si un transporteur et un code de suivi sont spécifiés sur la livraison, les informations de suivi sont indiquées dans le message électronique.

Sinon, utilisez l’action **Synchroniser les expéditions** sur les pages Commandes vente Shopify ou Magasin Shopify.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. En savoir plus dans la section [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

>[!Important]
>L’emplacement, y compris l’emplacement vide, défini dans la ligne d’expédition enregistrée doit avoir un enregistrement correspondant dans l’emplacement Shopify. Sinon, cette ligne ne sera pas renvoyée à Shopify. En savoir plus sur le [Mappage d’emplacement](synchronize-orders.md#location-mapping).

N’oubliez pas d’exécuter **Synchroniser les commandes à partir de Shopify** pour mettre à jour le statut d’exécution d’une commande dans [!INCLUDE[prod_short](../includes/prod_short.md)]. La fonctionnalité du connecteur archive également les commandes entièrement payées et exécutées à la fois dans Shopify et dans [!INCLUDE[prod_short](../includes/prod_short.md)] si les conditions sont remplies. 

### <a name="shipping-agents-and-tracking-url"></a>Transporteurs et URL de suivi

Si le document **Expédition vente enregistrée** contient le **Code transporteur** et/ou le **N° récépissé**, ces informations sont envoyées à Shopify et au client dans le message électronique de confirmation de livraison.

La société de suivi est renseignée dans l’ordre de priorité suivant (du plus élevé au plus faible), en fonction de l’enregistrement du transporteur :

* **Société de suivi Shopify**
* **Nom**
* **Code**

Si le champ **URL de suivi des colis** est rempli pour l’enregistrement du transporteur, la confirmation de livraison contient aussi une URL de suivi.

## <a name="returns-and-refunds"></a>Retours et remboursements

Dans une intégration entre Shopify et [!INCLUDE[prod_short](../includes/prod_short.md)], il est important de pouvoir synchroniser autant de données métier que possible. Cela facilite la mise à jour de vos niveaux de financement et de stock dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Les données que vous pouvez synchroniser incluent les retours et les remboursements qui ont été enregistrés dans Administrateur Shopify ou PDV Shopify.

Les retours et les remboursements sont importés avec leurs commandes associées si vous avez activé le type de traitement sur la fiche magasin Shopify.

Les retours sont importés à des fins d’information uniquement. Aucune logique de traitement ne leur est associée.

Les transactions financières et, si nécessaire, les transactions de stock sont traitées via des remboursements. Les remboursements peuvent inclure des produits ou simplement des montants, par exemple, si un marchand a décidé de compenser les frais d’expédition ou un autre montant.
Vous pouvez créer des avoirs de vente pour les remboursements. Les avoirs peuvent avoir les types de lignes suivants :

|Type|N°|Commentaire|
|-|-|-|
|Compte général|Compte carte cadeau vendu| À utiliser pour les remboursements liés aux cartes-cadeaux.|
|Compte général|Articles non-stockés du compte de remboursement | Utilisez pour les remboursements associés à des produits qui n’ont pas été réapprovisionnés. |
|Article |Nombre d’articles| Utilisez pour les remboursements associés à des produits qui ont été réapprovisionnés. Valable pour les remboursements directs ou les remboursements liés aux remboursements. Le code d’emplacement sur la ligne de crédit plus est défini en fonction de la valeur sélectionnée pour l’emplacement de retour.|
|Compte général| Compte de remboursement | Utilisez pour d’autres montants remboursés qui ne sont pas associés à des produits ou à des cartes-cadeaux. Par exemple, des pourboires, ou si vous avez indiqué manuellement un montant à rembourser dans Shopify. |

>[!Note]
>L’emplacement de retour, y compris les emplacements vides, définis dans la **Fiche magasin Shopify** sont utilisés sur la note de crédit créée. Le système ignore les emplacements d’origine des commandes ou des expéditions.

## <a name="gift-cards"></a>Cartes cadeaux

Dans le magasin Shopify, vous pouvez vendre des cartes cadeaux, qui peuvent être utilisées pour acheter des produits.

En matière de cartes cadeaux, il est important de saisir une valeur dans le champ **Compte carte cadeau vendu** dans la fenêtre **Fiche magasin Shopify**. La carte cadeau vendue est synchronisée avec les commandes en cours. Une carte cadeau lettrée est également importée avec la commande mais en tant que transaction. Notez que la carte cadeau ne diminue pas le montant à facturer.

Pour examiner les cartes cadeaux lettrées et émises, sélectionnez l’icône ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Cartes cadeaux**, puis choisissez le lien associé.

## <a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
