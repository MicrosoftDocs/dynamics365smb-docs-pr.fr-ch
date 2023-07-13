---
title: Synchroniser les articles et le stock
description: Configurer et exécuter des synchronisations d’articles entre Shopify et Business Central
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: AndreiPanko
ms.author: andreipa
ms.reviewer: bholtorf
---

# Synchroniser les articles et le stock

Les **Articles** dans [!INCLUDE[prod_short](../includes/prod_short.md)] correspondent aux *produits* dans Shopify, ce qui comprend les marchandises physiques, les téléchargements numériques, les services et les cartes cadeaux que vous vendez. Il existe deux raisons principales pour synchroniser les articles :

1. La gestion des données s’effectue principalement dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Vous devez exporter tout ou partie des données de là vers Shopify et le rendre visible. Vous pouvez exporter le nom, la description, l’image, les prix, la disponibilité, les variantes, les détails du fournisseur et le code à barres de l’article. Une fois exportés, vous pouvez revoir les éléments ou les rendre visibles immédiatement.
2. Lorsqu’une commande de Shopify est importée, les informations sur les articles sont essentielles pour le traitement ultérieur du document dans [!INCLUDE[prod_short](../includes/prod_short.md)].

Les deux scénarios précédents sont toujours activés.

Un troisième scénario consiste à gérer les données dans Shopify, mais à importer ces articles en vrac dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Ce scénario peut être utile pour les événements de migration de données, si vous souhaitez connecter une boutique en ligne existante à un nouvel environnement [!INCLUDE[prod_short](../includes/prod_short.md)].

## Définir les synchronisations des articles

1. Sélectionnez l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") et saisissez **Magasin Shopify**. Ouvrez la boutique pour laquelle vous souhaitez configurer la synchronisation des articles.
2. Dans le champ **Synchroniser l’article**, sélectionnez l’option requise.

   Le tableau suivant décrit les options.

|Option|Désignation|
|------|-----------|
|**Vide**| Les produits sont importés avec l’importation des commandes. Les produits sont exportés vers Shopify si un utilisateur exécute l’action **Ajouter un article** dans la page **Produits Shopify**. Cette option est le processus par défaut.|
|**À Shopify**| Sélectionnez cette option si, après la synchronisation initiale déclenchée par l’action **Ajouter un article**, vous prévoyez de mettre à jour les produits manuellement en utilisant l’action **Synchroniser le produit** ou via la file d’attente des tâches pour les mises à jour récurrentes. N’oubliez pas d’activer le champ **Peut mettre à jour le produit Shopify**. S’il n’est pas activé, il est égal à l’option **Vide** (processus par défaut). Pour plus d’informations, voir la section [Exporter les articles dans Shopify](synchronize-items.md#export-items-to-shopify)|
|**De Shopify**| Choisissez cette option si vous prévoyez d’importer des produits de Shopify en bloc, soit manuellement en utilisant l’action **Synchroniser le produit**, soit via la file d’attente des tâches pour les mises à jour récurrentes. Pour plus d’informations, voir la section [Importer les articles dans Shopify](synchronize-items.md#import-items-from-shopify).|

> [!NOTE]
> Changer **Synchroniser l’élément** de **Depuis Shopify** vers **À Shopify** n’aura d’effet que si vous activez **Peut mettre à jour les produits Shopify**.

## Importer des articles de Shopify

Tout d’abord, importiez les articles de Shopify en bloc ou en même temps que l’importation des commandes, ces articles sont d’abord ajoutés aux tableaux **Produit Shopify** et **Variante Shopify**. Mappez ensuite les produits et variantes importés aux articles et variantes dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Gérez le processus avec les paramètres suivants :

|Champ|Description|
|------|-----------|
|**Créer automatiquement des articles inconnus**|Lorsque les produits et variantes Shopify sont importés dans [!INCLUDE[prod_short](../includes/prod_short.md)], la fonction [!INCLUDE[prod_short](../includes/prod_short.md)] tente toujours de trouver d’abord l’enregistrement correspondant dans la liste d’articles. L’option **Mappage point de stock** a un impact sur la correspondance et crée un article et/ou une variante article. Activez cette option pour créer un article ou lorsqu’un enregistrement correspondant n’existe pas. Le nouvel article est créé en utilisant les données importées et le **Code modèle article**. Si cette option n’est pas activée, vous devez créer un élément manuellement et utiliser l’action **Mapper le produit** dans la page **Produits Shopify**.|
|**Code modèle article**|Utilisez cette option avec le bouton à bascule **Créer automatiquement des articles inconnus**.<br>Choisissez le modèle à utiliser pour les articles créés automatiquement.|
|**Mappage point de stock**|Choisissez comment vous voulez utiliser la valeur **Point de stock** importée de Shopify lors du mappage et de la création de l’article/de la variante. En savoir plus dans la section [Effet des points de stock et codes barres de produit Shopify sur le mappage et la création d’articles et de variants dans Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Séparateur de champ de point de stock**|Utilisez-le avec **Mappage point de stock** défini sur **[N° article + Code variante](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Définissez un séparateur qui doit servir à diviser le point de stock.<br>Par exemple, si, dans Shopify, vous créez la variante avec le point de stock 1000/001, tapez « / » dans le champ **Séparateur de champ de point de stock** pour obtenir le numéro d’article dans [!INCLUDE[prod_short](../includes/prod_short.md)] comme 1000 et le code variante article comme 001.|
|**Préfixe variante**|Utilisez avec le paramètre **Mappage point de stock** défini sur **Code variante** ou **N° article + Code variante** comme stratégie de secours lorsque le point de stock provenant de Shopify est vide.<br>Pour créer la variante article dans [!INCLUDE[prod_short](../includes/prod_short.md)] automatiquement, saisissez une valeur dans **Code**. Par défaut, la valeur définie dans le champ Point de stock importé de Shopify est utilisée. Cependant, si le point de stock est vide, il génère le code commençant par le préfixe de la variante défini et 001.|
|**Shopify peut mettre à jour l’article**|Choisissez cette option pour mettre à jour les articles et/ou les variantes automatiquement.|

### Effet des points de stock et codes à barres dans le produit Shopify sur le mappage et la création d’articles et de variantes dans Business Central

Lorsque les produits sont importés de Shopify vers les tableaux **Produits Shopify** et **Variantes Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] tente de trouver les enregistrements existants.

Le tableau suivant présente les différentes options du champ **Mappage point de stock**.

|Option|Effet sur le mappage|Effet sur la création|
|------|-----------------|------------------|
|**Vide**|Le champ Point de stock n’est pas utilisé dans la routine de mappage des articles.|Aucun effet sur la création de l’article.<br>Cette option empêche la création de variantes. Lorsque, dans la commande client, seul l’article principal est utilisé. Une variante peut toujours être mappée manuellement à partir de la page **Produit Shopify**.|
|**N° article**|Choisissez si le champ Point de stock contient le numéro d’article|Aucun effet sur la création de l’article sans les variantes. Pour un article avec des variantes, chaque variante est créée comme un article séparé.<br>Si Shopify a un produit avec deux variantes et que leurs points de stock sont 1000 et 2000, le système [!INCLUDE[prod_short](../includes/prod_short.md)] crée deux articles avec les numéros 1000 et 2000.|
|**Code variante**|Le champ Point de stock n’est pas utilisé dans la routine de mappage des articles.|Aucun effet sur la création de l’article. Si une variante article est créée, la valeur du champ Point de stock est utilisée comme code. Si le point de stock est vide, un code est généré en utilisant le champ **Préfixe variante**.|
|**N° article + Code variante**|Sélectionnez si le champ Point de stock contient un numéro d’article et le code variante article séparés par la valeur définie dans le champ **Séparateur de champ de point de stock**.|Lorsqu’un article est créé, la première partie de la valeur du champ Point de stock est utilisée comme **N°**. Si le point de stock est vide, un numéro d’article est généré en utilisant une série de numéros définie dans le champ **Code modèle article** ou **N° article** de la page **Paramètres stock**.<br>Lorsqu’un article est créé, la fonction variante utilise la seconde partie de la valeur du champ Point de stock comme **Code**. Si le champ du point de stock est vide, un code est généré en utilisant le champ **Préfixe variante**.|
|**Référence fournisseur**|Choisissez si le champ Point de stock contient le numéro d’article du fournisseur. Dans ce cas, le **Numéro du fournisseur de l’article** n’est pas utilisé sur la page **Fiche article** ; le **Numéro d’article du fournisseur** du **Catalogue des fournisseurs d’articles** est plutôt utilisé. Si l’enregistrement *Catalogue fournisseur articles* trouvé contient un code variante, ce dernier est utilisé pour mapper la variante Shopify.|Si un fournisseur correspondant existe dans [!INCLUDE[prod_short](../includes/prod_short.md)], la valeur de point de stock sert de **Référence fournisseur** dans **Fiche Article** et comme **Référence article** de type *Fournisseur*. <br>Empêche la création de variantes. Utile pour utiliser l’article principal uniquement dans la commande vente. Vous pouvez toujours mapper une variante manuellement à partir de la page **Produit Shopify**.|
|**Code à barres**|Choisissez si le champ Point de stock contient un code à barres. Une recherche est effectuée sur les **Références articles** de type *code-barres*. Si l’enregistrement Référence article trouvé contient un code variante, ce dernier est utilisé pour mapper la variante Shopify.|Aucun effet sur la création de l’article. <br>Empêche la création de variantes. Utile pour utiliser l’article principal uniquement dans la commande vente. Vous pouvez toujours mapper une variante manuellement à partir de la page **Produit Shopify**.|

Le tableau suivant donne les effets du champ **Code à barres**.

|Effet sur le mappage|Effet sur la création|
|-----------------|------------------|
|Une recherche est effectuée parmi les **Références articles** de type Code à barres sur la valeur définie dans le champ **Code à barres** dans Shopify. Si l’enregistrement Référence article trouvé contient un code variante, ce dernier est utilisé pour mapper la variante Shopify.|Le code à barres est enregistré comme **Référence article** pour l’article et la variante article.|

> [!NOTE]  
> Vous pouvez déclencher le mappage pour le produit/les variantes sélectionnés ou tous les produits non mappés importés en choisissant **Essayer de rechercher le mappage du produit** (pour le produit/les variantes sélectionnés) ou **Essayer de rechercher des mappages**.

## Exporter les articles dans Shopify

Choisissez les articles de la liste d’articles à exporter dans Shopify. Utilisez l’action **Ajouter un article** dans la page **Produits Shopify** pour ajouter des articles à la liste de produits Shopify. 

>[!IMPORTANT]
>Le produit est ajouté uniquement au canal de vente de la **boutique en ligne**. Vous devez publier des produits sur d’autres canaux de vente, tels que PDV Shopify, à partir de Shopify.

Les paramètres suivants permettent de gérer l’exportation des articles :

|Champ|Description|
|------|-----------|
|**Synchroniser texte étendu article**|Sélectionnez ce champ pour synchroniser le texte étendu de l’article. Comme il sera ajouté au champ **Description**, il peut contenir du code HTML. |
|**Synchroniser les attributs d’articles**|Sélectionnez ce champ pour synchroniser les attributs d’articles. Les attributs sont présentés sous forme de tableau et inclus dans le champ **Description** dans Shopify.|
|**Synchroniser texte marketing article**|Sélectionnez ce champ pour synchroniser le texte marketing de l’article. Bien que le texte marketing soit une sorte de description, il est différent du champ **Description** de l’article. Le champ **Description** est généralement utilisé comme nom d’affichage concis pour identifier rapidement le produit. Le texte marketing, quant à lui, est un texte plus riche et descriptif. Son objectif est d’ajouter du contenu marketing et promotionnel. Ce texte peut ensuite être publié avec l’article dans Shopify. Il existe deux manières de créer du texte marketing. Utilisez Copilot, qui suggère le texte généré par l’IA pour vous, ou commencez à partir de zéro.|
|**Code langue**|Sélectionnez ce champ si vous souhaitez que les versions traduites soient utilisées pour le titre, les attributs et le texte étendu.|
|**Mappage point de stock**|Choisissez comment vous voulez remplir le champ Point de stock dans Shopify. Les options possibles sont les suivantes :<br> - **N° article** pour utiliser le numéro d’article pour les produits et les variantes.<br> - **N° article + Code variante** pour créer un point de stock en concaténant les valeurs de deux champs. Pour les articles sans variantes, seul le numéro d’article est utilisé.<br>- **Référence fournisseur** pour utiliser la référence fournisseur définie dans **Fiche Article** pour les produits et les variantes.<br> - **Code à barres** pour utiliser le type de code à barres de **Référence article**. Cette option respecte les variantes.|
|**Séparateur de champ de point de stock**|Définissez un séparateur pour l’option **N° article + Code variante**.|
|**Suivi stock**| Choisissez comment le système remplit le champ **Suivi stock** pour les produits exportés dans Shopify. Vous pouvez mettre à jour les informations de disponibilité à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] pour les produits dans Shopify pour lesquels le suivi stock est activé. Consultez la section [Stock](synchronize-items.md#sync-inventory-to-shopify).|
|**Stratégie de stock par défaut**|Choisissez *Refuser* pour éviter tout stock négatif du côté de Shopify.|
|**Possibilité de mettre à jour les produits Shopify**|Définissez ce champ si [!INCLUDE[prod_short](../includes/prod_short.md)] peut uniquement créer des articles ou peut également les mettre à jour. Sélectionnez cette option si, après la synchronisation initiale déclenchée par l’action **Ajouter un article**, vous prévoyez de mettre à jour les produits manuellement en utilisant l’action **Synchroniser le produit** ou via la file d’attente des tâches pour les mises à jour récurrentes. N’oubliez pas de sélectionner **À Shopify** dans le champ **Synchronisation article**.<br>**Peut mettre à jour les produits Shopify** n’a pas d’impact sur la synchronisation des prix, des images ou des niveaux d’inventaire, qui sont configurés par des contrôles indépendants.<br>Si **Peut mettre à jour les produits Shopify** est activée, les champs suivants du côté Shopify seront mis à jour au niveau du produit et si nécessaire au niveau de la variante : **SKU**, **Code-barres**, **Poids**. Les champs **Titre**, **Type de produit**, **Fournisseur**, **Description** du produit seront également mis à jour si les valeurs exportées ne sont pas vides. Pour la description, cela signifie que vous devez activer l’un des boutons à bascule **Synchroniser texte étendu article**, **Synchroniser texte marketing article**, **Synchroniser les attributs d’articles** et les attributs, le texte étendu ou marketing doivent avoir des valeurs. Si le produit utilise des variantes, une variante sera ajoutée ou supprimée si nécessaire.|

### Aperçu du mappage des champs

|Shopify|Source lors de l’exportation à partir de [!INCLUDE[prod_short](../includes/prod_short.md)]|Cible lors de l’importation dans [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Statut|En fonction du champ **Statut des produits créés** dans la page **Fiche magasin Shopify**. Pour plus d’informations, voir [Mises à jour ponctuelles des produits Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Aucun affichage.|
|Titre | **Description**. Si le code langue est défini et qu’il existe une traduction article correspondante, cette dernière remplace la description.|**Description**|
|Désignation|Combine les textes étendus, le texte marketing et les attributs si vous activez les bascules correspondantes dans la fiche magasin Shopify. Respecte le code langue.|Aucun affichage.|
|Titre de la page du SEO|Valeur fixe : vide. Pour plus d’informations, voir [Mises à jour ponctuelles des produits Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Aucun affichage.|
|Description méta du SEO|Valeur fixe : vide. Pour plus d’informations, voir [Mises à jour ponctuelles des produits Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Aucun affichage.|
|Support|**Image**. En savoir plus dans la section [Synchroniser les images des articles](synchronize-items.md#sync-item-images)|**Image**|
|Prix|Le calcul du prix du client final comprend le prix unitaire de l’article, le groupe de prix client, le groupe de remises client et le code devise. En savoir plus dans la section [Synchroniser les prix](synchronize-items.md#sync-prices-with-shopify)|**Prix unitaire**. Le prix est uniquement importé dans les articles récemment créés, mais il ne sera pas mis à jour lors des synchronisations ultérieures.|
|Comparer au prix|Le calcul du prix sans remise.|Aucun affichage.|
|Coût par article|**Coût unitaire**|**Coût unitaire**. Le coût unitaire est uniquement importé dans les articles récemment créés et il ne sera pas mis à jour lors des synchronisations ultérieures.|
|SKU|En savoir plus sous **Mappage point de stock** dans la section [Exporter des articles vers Shopify](synchronize-items.md#export-items-to-shopify).|En savoir plus dans la section [Effet des points de stock et codes barres de produit Shopify sur le mappage et la création d’articles et de variants dans Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Code-barres|**Références articles** de type Code à barres.|**Références articles** de type Code à barres.|
|Suivi quantité|En fonction du champ **Suivi stock** dans la page **Fiche magasin Shopify**. Consultez la section [Stock](synchronize-items.md#sync-inventory-to-shopify). Utilisé uniquement lorsque vous exportez un produit pour la première fois.|Aucun affichage.|
|Poursuivre la vente même en cas de rupture de stock|En fonction de **Stratégie de stock par défaut** dans la page **Fiche magasin Shopify**. Utilisé uniquement lorsque vous exportez un produit pour la première fois.|Aucun affichage.|
|Type|**Description** de **Code catégorie article**. Si le type n’est pas spécifié dans Shopify, il est ajouté en tant que type personnalisé.|**Code catégorie article**. Mappage par description.|
|Fournisseur|**Nom** du fournisseur provenant de **N° fournisseur**|Mappage par nom de **N° fournisseur**.|
|Poids|**Poids brut**.|Aucun affichage.|
|Imposable|Valeur fixe : activée.|Aucun affichage.|
|Codes taxe|**Code groupe taxes**. Uniquement pertinent pour les taxes de vente. En savoir plus sur [Configurer les taxes](setup-taxes.md).|Aucun affichage.|

### Balises

Examinez les balises importées dans le récapitulatif **Balises** de la page **Produit Shopify**. Sur la même page, pour modifier les balises, choisissez l’action **Balises**.
Si l’option **À Shopify** est sélectionnée dans le champ **Synchroniser l’article**, les balises attribuées sont exportées vers Shopify à la prochaine synchronisation.

## Exécuter la synchronisation des articles

La synchronisation complète ou partielle des articles peut être effectuée de différentes manières.

### Synchronisation initiale des articles de Business Central vers Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Choisissez l’action **Ajouter des articles**.
3. Dans le champ **Code magasin**, saisissez le code. Si vous ouvrez la fenêtre **Produit Shopify** dans la page **Fiche magasin**, le code magasin est rempli automatiquement.
4. Si vous avez configuré la synchronisation des images et du stock, vous pouvez les inclure dans le même processus. Les inclure dans le même processus est pratique pour les scénarios de démonstration ou lorsqu’il s’agit de traiter une plus petite quantité de données. 
5. Définissez des filtres sur les articles selon vos besoins. Par exemple, vous pouvez filtrer par numéro d’article ou code catégorie article.
6. Cliquez sur **OK**.

Les articles résultants sont automatiquement créés dans Shopify avec les prix. Selon les choix que vous avez faits, des images et des niveaux de stock peuvent être inclus. L’opération peut prendre un certain temps si un grand nombre d’articles est ajouté.

### Synchroniser les produits de Shopify vers Business Central

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify**, puis choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les articles pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les produits**.

Sinon, utilisez l’action **Synchroniser les produits** dans la page **Produits Shopify** ou recherchez le traitement par lots **Synchroniser les produits**.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. En savoir plus dans la section [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

### Mises à jour ponctuelles des produits Shopify

Si les enregistrements sont mis à jour dans le tableau **Produit Shopify**, les modifications suivantes sont synchronisées avec Shopify.

Mise à jour :

* **Statut** (vous avez le choix entre actif, archivé ou brouillon).
* **Titre du SEO**
* **Description du SEO**

Suppression :

En fonction de la valeur indiquée dans **Action pour produits supprimés** dans la page **Fiche magasin Shopify**, le produit est mis à jour dans Shopify lorsque l’enregistrement est supprimé de la page **Produits Shopify**.

* **Vide** : rien ne se passe. Si nécessaire, l’utilisateur doit effectuer l’action requise à partir de l’**administration Shopify**.
* **Statut sur brouillon** : le statut du produit dans Shopify est défini sur *Brouillon*.
* **Statut sur Archivé** : le produit est archivé dans Shopify.

## Synchroniser les images d’articles

La synchronisation des images peut être configurée pour les articles synchronisés. Choisissez parmi les options suivantes :

* **Désactivé** : la synchronisation des images est désactivée.
* **À Shopify** : les images des articles sont exportées dans Shopify.
* **De Shopify** : les images de Shopify sont importés dans [!INCLUDE[prod_short](../includes/prod_short.md)].

La synchronisation des images peut être initialisée de deux manières décrites ci-dessous.

### Synchroniser les images des produits à partir de la page du magasin Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les images pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les images des produits**.

### Synchroniser les images des produits à partir de la page des produits Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Synchroniser les images des produits**.

### Remarques sur la synchronisation des images

* Lors de l’exportation des images de [!INCLUDE[prod_short](../includes/prod_short.md)] dans Shopify, les nouvelles images sont ajoutées à Shopify, les anciennes images sont conservées. Si une image est mise à jour dans [!INCLUDE[prod_short](../includes/prod_short.md)], vous devez supprimer les anciennes images dans l’**administration Shopify**.
* Les images exportées dans Shopify et ne respectant pas les exigences définies par Shopify ne sont pas importées. Pour plus d’informations, voir [Types de support des produits sur help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## Synchroniser les prix avec Shopify

Les paramètres suivants permettent d’exporter les prix avec ces paramètres :

|Champ|Description|
|------|-----------|
|**Groupe prix client**|Indique le prix d’un article dans Shopify. Le prix de vente de ce groupe prix client est pris en compte. Si aucun groupe n’est spécifié, le prix de la fiche Article est utilisé.|
|**Groupe remises client**|Indique la remise à utiliser pour calculer le prix d’un article dans Shopify. Les prix remisés sont stockés dans le champ **Prix** et le prix total est stocké dans le champ **Comparer au prix**.|
|**Autoriser remise ligne**|Indique si la remise ligne est autorisée lors du calcul des prix pour Shopify. Ce paramètre s’applique uniquement aux prix de l’article. Les prix pour le groupe de prix client ont leur propre bouton à bascule sur les lignes.|
|**Prix TTC**|Indique si les calculs de prix pour Shopify comprennent la TVA. En savoir plus sur [Configurer les taxes](setup-taxes.md).|
|**Groupe compta. marché TVA**|Indique le groupe compta. marché TVA utilisé pour calculer les prix dans Shopify. Cela devrait être le groupe que vous utilisez pour les clients nationaux. En savoir plus sur [Configurer les taxes](setup-taxes.md).|
|**Code devise**|Saisissez un Code monnaie si la boutique en ligne utilise une monnaie différente de DS. La devise spécifiée doit avoir des taux de change configurés. Si votre boutique en ligne utilise la même devise que [!INCLUDEprod_short], laissez le champ vide.|

Vous pouvez exporter les prix pour les articles synchronisés de la manière décrite ci-dessous.

### Synchroniser les prix à partir de la page des produits Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Synchroniser les prix avec Shopify**.

### Remarques sur le calcul des prix

* Lors de la détermination d’un prix, [!INCLUDE[prod_short](../includes/prod_short.md)] utilise le prix le plus bas. Cependant, la logique du prix le plus bas ignore le prix unitaire défini sur la fiche article si un prix est défini dans le groupe de prix. Cela est vrai même si le prix unitaire du prix de la fiche article est inférieur.
* Pour calculer les prix, le connecteur crée un devis temporaire pour l’article avec une quantité de 1 et utilise une logique de calcul de prix standard. Seuls les prix et remises applicables pour la quantité 1 sont utilisés. Vous ne pouvez pas exporter différents prix ou remises en fonction de la quantité.

## Synchroniser le stock sur Shopify

La synchronisation du stock peut être configurée pour les articles déjà synchronisés. Deux conditions doivent être remplies :

1. Le suivi du stock doit être activé pour un produit dans Shopify. Si les articles sont exportés dans Shopify, pensez à activer **Suivi stock** dans la page **Magasin Shopify**. Pour plus d’informations, voir la section [Exporter les articles dans Shopify](synchronize-items.md#export-items-to-shopify)
2. La synchronisation du stock doit être activée pour **Emplacements Shopify**.

### Pour activer la synchronisation du stock

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify**, puis choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser le stock pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Emplacements** pour ouvrir **Emplacements des magasins Shopify**.
4. Sélectionnez l’action **Obtenir les emplacements Shopify** pour importer tous les emplacements définis dans Shopify. Ils se trouvent dans les paramètres [**Emplacements**](https://www.shopify.com/admin/settings/locations) sous **Administration Shopify**.
5. Dans le champ **Filtre magasin**, ajoutez des emplacements si vous voulez inclure le stock en provenance de certains emplacements uniquement. Par exemple, saisissez *EST|OUEST* pour que seul le stock de ces deux emplacements soit disponible à la vente sur la boutique en ligne.
6. Sélectionnez la méthode de calcul des stocks à utiliser pour les emplacements Shopify sélectionnés.

La synchronisation du stock peut être initialisée de deux manières décrites ci-dessous.

### Synchroniser le stock à partir de la page du magasin Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser le stock pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser le stock**.

### Synchroniser le stock à partir de la page des produits Shopify

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez l’action **Synchroniser le stock**.

### Remarques sur le stock

* La méthode standard de calcul des stocks est **Solde disponible projeté à la date**. Avec l’extensibilité, vous pouvez ajouter plus d’options. Pour en savoir plus sur l’extensibilité, rendez-vous sur [ exemples](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md). 
* Vous pouvez consulter les informations de stock en provenance de Shopify dans la page **Récapitulatif du stock Shopify**. Dans ce récapitulatif, un aperçu du stock Shopify et du dernier stock calculé s’affichent dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Il existe un enregistrement par emplacement.
* Si les informations de stock dans Shopify sont différentes de l’élément **Stock prévisionnel** dans [!INCLUDE[prod_short](../includes/prod_short.md)], le stock est mis à jour dans Shopify.
* Lorsque vous ajoutez un nouveau magasin dans Shopify, vous devez également ajouter des enregistrements d’inventaire pour celui-ci. Shopify ne le fait pas automatiquement pour les produits et variantes existants et le connecteur ne synchronisera pas les niveaux de stock pour ces articles dans le nouveau magasin. Pour en savoir plus, consultez [Affecter un stock à des magasins](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* L’inventaire et l’expédition sur **Services d’exécution Business Central** ne sont pas pris en charge, utilisez plutôt des emplacements normaux.

#### Exemple de calcul du solde disponible prévisionnel

Il y a 10 pièces de l’article A disponibles en stock et deux commandes vente en attente. Une pour lundi avec la quantité de *Un* et une pour jeudi avec une quantité de *Deux*. Selon le moment où vous synchronisez le stock, le système mettra à jour le niveau de stock dans Shopify avec différentes quantités :

|Quand la synchronisation du stock est exécutée|Valeur utilisée pour mettre à jour le niveau de stock|Commentaire|
|------|-----------------|-----------------|
|Mardi|9|Stock 10 moins commande vente définis sur une expédition lundi|
|Vendredi|7|Stock 10 moins les deux commandes vente|

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
