---
title: Synchroniser les articles et le stock
description: Configurer et exécuter des synchronisations d’articles entre Shopify et Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: c7aea0d0b3d9a8902e704a2d390d6a244e8cbbef
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317315"
---
# <a name="synchronize-items-and-inventory"></a>Synchroniser les articles et le stock

Les **Articles** dans [!INCLUDE[prod_short](../includes/prod_short.md)] correspondent aux *produits* dans Shopify, ce qui comprend les marchandises physiques, les téléchargements numériques, les services et les cartes cadeaux que vous vendez. Il existe deux raisons principales pour synchroniser les articles :

1. Principalement, la gestion des données est effectuée dans [!INCLUDE[prod_short](../includes/prod_short.md)], vous devez exporter tout ou partie des données dans Shopify et les rendre visibles. Vous pouvez exporter le nom, la description, l’image, les prix, la disponibilité, les variantes, les détails du fournisseur et le code à barres de l’article. Une fois ces éléments importés, les articles peuvent devenir immédiatement visibles ou ils peuvent d’abord être examinés et améliorés par une personne responsable.
2. Lorsqu’une commande de Shopify est importée, les informations sur les articles sont essentielles pour le traitement ultérieur du document dans [!INCLUDE[prod_short](../includes/prod_short.md)].

Ces deux scénarios sont toujours activés.

Un troisième scénario consiste à gérer les données dans Shopify, mais à importer ces articles en vrac dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Ce scénario peut être utile pour les événements de migration de données, si vous souhaitez connecter une boutique en ligne existante à un nouvel environnement [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="to-define-item-synchronizations"></a>Pour définir les synchronisations des articles

1. Sélectionnez l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify**. Ouvrez la boutique pour laquelle vous souhaitez configurer la synchronisation des articles.
2. Dans le champ **Synchroniser l’article**, sélectionnez l’option requise. <br>Le tableau suivant présente les différentes options.

|Option|Désignation|
|------|-----------|
|**Vide**| Les produits sont importés avec l’importation des commandes. Les produits sont exportés vers Shopify si un utilisateur exécute l’action **Ajouter un article** dans la page **Produits Shopify**. Il s’agit du processus par défaut. |
|**À Shopify**| Sélectionnez cette option si, après la synchronisation initiale déclenchée par l’action **Ajouter un article**, vous prévoyez de mettre à jour les produits manuellement en utilisant l’action **Synchroniser le produit** ou via la file d’attente des tâches pour les mises à jour récurrentes. N’oubliez pas d’activer le champ **Peut mettre à jour le produit Shopify**. S’il n’est pas activé, cela équivant à l’option **Vide**. Pour plus d’informations, voir [Exporter les articles dans Shopify](synchronize-items.md#export-items-to-shopify)|
|**De Shopify**| Choisissez cette option si vous prévoyez d’importer des produits de Shopify en bloc, soit manuellement en utilisant l’action **Synchroniser le produit**, soit via la file d’attente des tâches pour les mises à jour récurrentes. Si aucune option n’est sélectionnée, cela équivaut à l’option **Vide**. Pour en savoir plus sur l’importation d’articles, voir [Importer des articles à partir de Shopify](synchronize-items.md#import-items-from-shopify)|

## <a name="import-items-from-shopify"></a>Importer des articles de Shopify

Que vous importiez les articles de Shopify en bloc ou en même temps que l’importation des commandes, ces articles sont d’abord ajoutés aux tableaux **Produit Shopify** et **Variante Shopify**. Les paramètres suivants permettent de gérer le processus :

|Champ|Désignation|
|------|-----------|
|**Créer automatiquement des articles inconnus**|Lorsque les produits et variantes Shopify sont importés dans [!INCLUDE[prod_short](../includes/prod_short.md)], la fonction [!INCLUDE[prod_short](../includes/prod_short.md)] tente toujours de trouver d’abord l’enregistrement correspondant dans la liste d’articles. L’option **Mappage point de stock** a un impact sur la correspondance et crée un article et/ou une variante article. Activez cette option pour créer un article ou lorsqu’un enregistrement correspondant n’existe pas. Le nouvel article est créé en utilisant les données importées et le **Code modèle article**. Si cette option n’est pas activée, vous devez créer un élément manuellement et utiliser l’action **Mapper le produit** dans la page **Produits Shopify**.|
|**Code modèle article**|Utilisé avec **Créer automatiquement des articles inconnus**. <br> Choisissez le modèle à utiliser pour les articles créés automatiquement.|
|**Mappage point de stock**|Choisissez comment vous voulez utiliser la valeur **Point de stock** importée de Shopify lors du mappage et de la création de l’article/de la variante. Pour plus d’informations, voir [Comment le point de stock et le code à barres définis dans le produit Shopify affectent le mappage et la création d’articles et de variantes](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**Séparateur de champ de point de stock**|Utilisé avec le paramètre **Mappage point de stock** défini sur **N° article + Code variante**.<br> Définissez un séparateur qui doit servir à diviser le point de stock. <br>Par exemple, si, dans Shopify, vous créez la variante avec le point de stock 1000/001, tapez « / » dans le champ **Séparateur de champ de point de stock** pour obtenir le numéro d’article dans [!INCLUDE[prod_short](../includes/prod_short.md)] comme 1000 et le code variante article comme 001.
|**Préfixe variante**|Utilisé avec le paramètre **Mappage point de stock** défini sur **Code variante** ou **N° article + Code variante** comme stratégie de secours lorsque le point de stock provenant de Shopify est vide.<br>Pour créer la variante article dans [!INCLUDE[prod_short](../includes/prod_short.md)] automatiquement, saisissez une valeur dans **Code**. Par défaut, la valeur définie dans le champ Point de stock importé de Shopify est utilisée. Cependant, si le point de stock est vide, il génère le code commençant par le préfixe de la variante défini et 001.|
|**Shopify peut mettre à jour l’article**| Choisissez cette option pour mettre à jour les articles et/ou les variantes automatiquement.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Comment le point de stock et le code à barres définis dans le produit Shopify affectent le mappage et la création d’articles et de variantes dans Business Central

Lorsque les produits sont importés de Shopify vers les tableaux **Produits Shopify** et **Variantes Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tente de trouver les enregistrements existants. Le tableau suivant présente les différentes options du champ **Mappage point de stock**.

|Option|Effet sur le mappage|Effet sur la création|
|------|-----------------|------------------|
|**Vide**|Le champ Point de stock n’est pas utilisé dans la routine de mappage des articles.|Aucun effet sur la création de l’article. <br>Empêche la création de variantes. Utile lorsque, dans la commande client, seul l’article principal est utilisé. Une variante peut toujours être mappée manuellement à partir de la fenêtre **Produit Shopify**.|
|**N° article**|Choisissez si le champ Point de stock contient le numéro d’article.|Aucun effet sur la création de l’article sans les variantes. Pour un article avec des variantes, chaque variante est créée comme un article séparé.<br> Par exemple, si Shopify a un produit avec deux variantes et que leurs points de stock sont 1000 et 2000, le système [!INCLUDE[prod_short](../includes/prod_short.md)] crée deux articles avec les numéros 1000 et 2000.|
|**Code variante**|Le champ Point de stock n’est pas utilisé dans la routine de mappage des articles.|Aucun effet sur la création de l’article. Si une variante article est créée, la valeur du champ Point de stock est utilisée comme code. Si le point de stock est vide, un code est généré en utilisant le champ **Préfixe variante**.|
|**N° article + Code variante**| Sélectionnez si le champ Point de stock contient un numéro d’article et le code variante article séparés par la valeur définie dans le champ **Séparateur de champ de point de stock**.|Lorsqu’un article est créé, la première partie de la valeur du champ Point de stock est utilisée comme **N°**. Si le point de stock est vide, un numéro d’article est généré en utilisant une série de numéros définie dans **Code modèle article** ou **N° article** dans la fenêtre **Paramètres stock**.<br>Lorsqu’un article est créé, la fonction variante utilise la seconde partie de la valeur du champ Point de stock comme **Code**. Si le point de stock est vide, un code est généré en utilisant le champ **Préfixe variante**.|
|**Référence fournisseur**| Choisissez si le champ Point de stock contient la référence fournisseur. Dans ce cas, le paramètre **Référence fournisseur** n’est pas utilisé dans la fenêtre **Fiche Article**, mais **Référence fournisseur** de **Catalogue fournisseur articles**. Si l’enregistrement *Catalogue fournisseur articles* trouvé contient un code variante, ce dernier est utilisé pour mapper la variante Shopify.|Si un fournisseur correspondant existe dans [!INCLUDE[prod_short](../includes/prod_short.md)], la valeur de point de stock sert de **Référence fournisseur** dans **Fiche Article** et comme **Référence article** de type Fournisseur. <br>Empêche la création de variantes. Utile pour utiliser l’article principal uniquement dans la commande vente. Vous pouvez toujours mapper une variante manuellement à partir de la fenêtre **Produit Shopify**.|
|**Code à barres**| Choisissez si le champ Point de stock contient un code à barres. Une recherche est effectuée sur les **Références articles** de type Fournisseur. Si l’enregistrement Référence article trouvé contient un code variante, ce dernier est utilisé pour mapper la variante Shopify.|Aucun effet sur la création de l’article. <br>Empêche la création de variantes. Peut être utile si seul l’article principal est utilisé dans la commande vente. Une variante peut toujours être mappée manuellement à partir de la fenêtre **Produit Shopify**.|

Le tableau suivant donne l’effet du champ **Code à barres**.

|Effet sur le mappage|Effet sur la création|
|-----------------|------------------|
|Une recherche est effectuée parmi les **Références articles** de type Code à barres sur la valeur définie dans le champ Code à barres dans Shopify. Si l’enregistrement de la référence article trouvé contient un code variante, ce dernier est utilisé pour mapper la variante Shopify.|Le code à barres est enregistré comme **Référence article** pour l’article et la variante article.|

> [!NOTE]  
> Vous pouvez déclencher le mappage pour le produit/les variantes sélectionnés ou tous les produits non mappés importés en choisissant **Essayer de rechercher le mappage du produit** (pour le produit/les variantes sélectionnés) ou **Essayer de rechercher des mappages** (pour tous).

## <a name="export-items-to-shopify"></a>Exporter les articles dans Shopify

Choisissez les articles de la liste d’articles à exporter dans Shopify. Utilisez l’action **Ajouter un article** dans la fenêtre **Produits Shopify** pour ajouter des articles à la liste de produits Shopify.

Les paramètres suivants permettent de gérer l’exportation des articles :

|Champ|Désignation|
|------|-----------|
|**Groupe prix client**|Indique le prix d’un article dans Shopify. Le prix de vente de ce groupe prix client est pris en compte. Si aucun groupe n’est saisi, le prix de la fiche Article est utilisé.|
|**Groupe remises client**|Indique la remise à utiliser pour calculer le prix d’un article dans Shopify. Les prix remisés sont stockés dans le champ **Prix** et le prix total est stocké dans le champ **Comparer au prix**.|
|**Synchroniser texte étendu article**|Sélectionnez pour synchroniser le texte étendu de l’article. Comme il sera ajouté au champ *Description*, il peut contenir du code HTML. |
|**Synchroniser les attributs d’articles**|Sélectionnez pour synchroniser les attributs d’articles. Les attributs sont présentés sous forme de tableau et inclus dans le champ *Description* dans Shopify.|
|**Code langue**|Si ce paramètre est sélectionné, les versions traduites sont utilisées pour le titre, les attributs et le texte étendu.|
|**Mappage point de stock**|Choisissez comment vous voulez remplir le champ Point de stock dans Shopify. Les options possibles sont les suivantes :<br> - **N° article** pour utiliser le numéro d’article pour les produits et les variantes.<br> - **N° article + Code variante** pour créer un point de stock en concaténant les valeurs de deux champs. Pour les articles sans variantes, seul le numéro d’article est utilisé.<br>- **Référence fournisseur** pour utiliser la référence fournisseur définie dans *Fiche Article* pour les produits et les variantes.<br> - **Code à barres** utilise **Référence article** de type Code à barres. Cette option respecte les variantes. |
|**Séparateur de champ de point de stock**|Définissez un séparateur pour l’option **N° article + Code variante**.|
|**Suivi stock**|Choisissez comment le système remplit le champ **Suivi stock** pour les produits exportés dans Shopify. Vous pouvez mettre à jour les informations de disponibilité à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] pour les produits dans Shopify pour lesquels le suivi stock est activé. Pour plus d’informations, voir [Stock](synchronize-items.md#sync-inventory-to-shopify).|
|**Stratégie de stock par défaut**|Choisissez *Refuser* pour éviter tout stock négatif du côté de Shopify. |
|**Possibilité de mettre à jour les produits Shopify**|Définissez si [!INCLUDE[prod_short](../includes/prod_short.md)] peut uniquement créer des articles ou peut également les mettre à jour. Sélectionnez cette option si, après la synchronisation initiale déclenchée par l’action **Ajouter un article**, vous prévoyez de mettre à jour les produits manuellement en utilisant l’action **Synchroniser le produit** ou via la file d’attente des tâches pour les mises à jour récurrentes. N’oubliez pas de sélectionner **À Shopify** dans le champ **Synchronisation article**.|
|**Code modèle client**|Choisissez le modèle par défaut à utiliser lors du calcul du prix. Pour plus d’informations, voir [Configurer les taxes](setup-taxes.md).|


### <a name="fields-mapping-overview"></a>Aperçu du mappage des champs

|Shopify|Source lors de l’exportation à partir de [!INCLUDE[prod_short](../includes/prod_short.md)]|Cible lors de l’importation dans [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Statut|En fonction de **Statut des produits créés** dans la page **Fiche magasin Shopify**. Pour plus d’informations, voir [Mises à jour ponctuelles des produits Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products).|Aucun affichage.|
|Titre|**Description**. Si le code langue est défini et qu’il existe une traduction article correspondante, cette dernière remplace la description.|**Description**|
|Désignation|Combine les textes étendus et les attributs si les bascules correspondantes dans la fiche magasin Shopify sont activées. Respecte le code langue.|Aucun affichage.|
|Titre de la page du SEO|Valeur fixe : vide, voir [Mises à jour ponctuelles des produits Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products). |Aucun affichage.|
|Description méta du SEO|Valeur fixe : vide, voir [Mises à jour ponctuelles des produits Shopify](synchronize-items.md#ad-hock-updates-of-shopify-products). |Aucun affichage.|
|Support|**Image**, pour plus d’informations, voir [Synchroniser les images d’articles](synchronize-items.md#sync-item-images)|**Image**|
|Prix|Le calcul du prix du client final comprend le groupe prix article, le groupe remises article, le code devise et le code modèle client. |**Prix unitaire**|
|Comparer au prix|Le calcul du prix sans remise comprend le groupe prix article, le groupe remises article, le code devise et le code modèle client. |Aucun affichage.|
|Coût par article|**Coût unitaire**|**Coût unitaire**|
|Point de stock|Voir **Mappage point de stock** dans [Exporter les articles dans Shopify](synchronize-items.md#export-items-to-shopify)| Voir [Comment le point de stock et le code à barres définis dans le produit Shopify affectent le mappage et la création d’articles et de variantes](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|Code-barres|**Références articles** de type Code à barres|**Références articles** de type Code à barres|
|Suivi quantité|En fonction de **Suivi stock** dans la page **Fiche magasin Shopify**. Pour plus d’informations, voir [Stock](synchronize-items.md#sync-inventory-to-shopify).|Aucun affichage.|
|Poursuivre la vente même en cas de rupture de stock|En fonction de **Stratégie de stock par défaut** dans la page **Fiche magasin Shopify**. Non importé.|Aucun affichage.|
|Type|**Description** de **Code catégorie article**. Si le type n’est pas spécifié dans Shopify, il est ajouté en tant que type personnalisé.|**Code catégorie article**. Mappage par description.|
|Fournisseur|**Nom** du fournisseur provenant de **N° fournisseur** |Mappage par nom de **N° fournisseur**.|
|Poids|**Poids brut**.|Aucun affichage.|
|Imposable|Valeur fixe : activée.|Aucun affichage.|
|Codes taxe|**Code groupe taxes**. Uniquement pertinent pour les taxes de vente. Pour plus d’informations, voir [Configurer les taxes](setup-taxes.md). |Aucun affichage.|

### <a name="tags"></a>Balises

Examinez les balises importées dans le récapitulatif **Balises** de la page **Produit Shopify**. Pour modifier les balises, choisissez l’action **Balises** dans la page **Produit Shopify**.
Si l’option **À Shopify** est sélectionnée dans le champ **Synchroniser l’article**, les balises attribuées sont exportées vers Shopify à la prochaine synchronisation.

## <a name="run-item-synchronization"></a>Exécuter la synchronisation des articles

La synchronisation complète ou partielle des articles peut être effectuée de différentes manières.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Synchronisation initiale des articles de Business Central vers Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Choisissez l’action **Ajouter des articles**.
3. Dans le champ **Code magasin**, saisissez le code. Si vous ouvrez la fenêtre **Produit Shopify** dans la fenêtre **Fiche magasin**, le code magasin est rempli automatiquement.
4. Définissez des filtres sur les articles selon vos besoins. Par exemple, vous pouvez filtrer par numéro d’article ou code catégorie article.
5. Cliquez sur **OK**.

Les articles résultants sont automatiquement créés dans Shopify avec les prix mais sans inclure les images et les niveaux de stock. L’opération peut prendre un certain temps si un grand nombre d’articles est ajouté.

### <a name="sync-products-from-shopify-to-business-central"></a>Synchroniser les produits de Shopify vers Business Central

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les articles pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les produits**.

Sinon, utilisez l’action **Synchroniser les produits** dans la fenêtre **Produits Shopify** ou recherchez le traitement par lots **Synchroniser les produits**.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. Pour plus d’informations, voir [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

### <a name="ad-hock-updates-of-shopify-products"></a>Mises à jour ponctuelles des produits Shopify

Si les enregistrements sont mis à jour dans le tableau **Produit Shopify**, les modifications suivantes sont synchronisées avec Shopify.

Mise à jour :

* **Statut** (vous avez le choix entre actif, archivé ou brouillon).
* **Titre du SEO**
* **Description du SEO**

Suppression :

En fonction de la valeur indiquée dans **Action pour produits supprimés** dans la page **Fiche magasin Shopify**, le produit est mis à jour dans Shopify lorsque l’enregistrement est supprimé de la page **Produits Shopify**.

* **Vide** : rien ne se passe. Si nécessaire, l’utilisateur doit effectuer l’action requise à partir de l’administration Shopify.
* **Statut sur brouillon** : le statut du produit dans Shopify est défini sur *Brouillon*.
* **Statut sur Archivé** : le produit est archivé dans Shopify.

## <a name="sync-item-images"></a>Synchroniser les images d’articles

La synchronisation des images peut être configurée pour les articles synchronisés. Les options suivantes sont possibles :

* **Vide** : la synchronisation des images est désactivée.
* **À Shopify** : les images des articles sont exportées dans Shopify
* **De Shopify** : les images de Shopify sont importés dans [!INCLUDE[prod_short](../includes/prod_short.md)]

La synchronisation des images peut être initialisée de deux manières.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Synchroniser les images des produits à partir de la fenêtre du magasin Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les images pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les images des produits**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Synchroniser les images des produits à partir de la fenêtre des produits Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Synchroniser les images des produits**.

### <a name="image-synchronization-remarks"></a>Remarques sur la synchronisation des images

* Lors de l’exportation des images de [!INCLUDE[prod_short](../includes/prod_short.md)] dans Shopify, les nouvelles images sont ajoutées à Shopify, les anciennes images sont conservées. Si une image est mise à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], vous devez supprimer les anciennes images dans l’administration Shopify.
* Les images exportées dans Shopify et ne respectant pas les exigences définies par Shopify ne sont pas importées. Pour plus d’informations, voir [Types de support des produits sur help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Synchroniser les prix avec Shopify

Les prix peuvent être exportés pour les articles synchronisés de la manière décrite ci-dessous.

### <a name="sync-prices-from-the-shopify-products-window"></a>Synchroniser les prix à partir de la fenêtre des produits Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Synchroniser les prix avec Shopify**.

### <a name="price-calculation-remarks"></a>Remarques sur le calcul des prix

* Pour le calcul des prix, il est important que le champ **Modèle client par défaut** contienne une valeur. Pour plus d’informations, voir [Configurer les taxes](setup-taxes.md).
* Saisissez un **Code devise** si la boutique en ligne utilise une monnaie différente de DS. La devise spécifiée doit avoir des taux de change configurés. Si votre boutique en ligne utilise la même devise que [!INCLUDE[prod_short](../includes/prod_short.md)], laissez le champ vide.
* Lors de la détermination d’un prix, [!INCLUDE[prod_short](../includes/prod_short.md)] utilise le prix le plus bas. Autrement dit, si le prix unitaire défini dans la fiche article est inférieur à celui défini dans le groupe prix, le prix unitaire de la fiche article est utilisé.

## <a name="sync-inventory-to-shopify"></a>Synchroniser le stock sur Shopify

La synchronisation du stock peut être configurée pour les articles déjà synchronisés. Deux conditions doivent être remplies :

1. Le suivi du stock doit être activé pour un produit dans Shopify. Si les articles sont exportés dans Shopify, pensez à activer **Suivi stock** dans la fiche **Magasin Shopify**. Pour plus d’informations, voir [Exporter les articles dans Shopify](synchronize-items.md#export-items-to-shopify).
2. La synchronisation du stock doit être activée pour **Emplacements Shopify**.

### <a name="to-enable-inventory-sync"></a>Pour activer la synchronisation du stock

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser le stock pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Emplacements** pour ouvrir **Emplacements des magasins Shopify**.
4. Sélectionnez l’action **Obtenir les emplacements Shopify** pour importer tous les emplacements définis dans Shopify. Ils se trouvent dans les paramètres [**Emplacements**](https://www.shopify.com/admin/settings/locations) sous **Administration Shopify**.
5. Dans le champ **Filtre magasin**, ajoutez des emplacements si vous voulez inclure le stock en provenance de certains emplacements uniquement. Par exemple, saisissez *EST|OUEST* pour que seul le stock de ces deux emplacements soit disponible à la vente sur la boutique en ligne.
6. Décochez **Désactivé** pour activer la synchronisation du stock pour les emplacements Shopify sélectionnés.

La synchronisation du stock peut être initialisée de deux manières.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Synchroniser le stock à partir de la fenêtre du magasin Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser le stock pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser le stock**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Synchroniser le stock à partir de la fenêtre des produits Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Synchroniser le stock**.

### <a name="inventory-remarks"></a>Remarques sur le stock

* Le connecteur calcule l’élément **Stock prévisionnel** et l’exporte dans Shopify.
* Vous pouvez consulter les informations de stock en provenance de Shopify dans la page **Récapitulatif du stock Shopify**. Dans ce récapitulatif, un aperçu du stock Shopify et du dernier stock calculé s’affichent dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Il existe un enregistrement par emplacement.
* Si les informations de stock dans Shopify sont différentes de l’élément **Stock prévisionnel** dans [!INCLUDE[prod_short](../includes/prod_short.md)], le stock est mis à jour dans Shopify.

## <a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
