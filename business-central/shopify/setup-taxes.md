---
title: Configurer les taxes pour la connexion Shopify
description: Comment configurer les taxes dans Shopify et dans Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Configurer les taxes pour la connexion Shopify

Dans cet article, nous allons étudier de quelle manière divers paramètres de Shopify ont un impact sur les taxes et les prix en magasin qui sont affichés au client. Nous verrons également comment configurer [!INCLUDE[prod_short](../includes/prod_short.md)] pour prendre en charge les paramètres dans Shopify. Cet article n’est pas conçu comme un guide complet sur les taxes. Pour en savoir plus, contactez votre administration fiscale locale ou un expert en fiscalité.  

L’article suppose que vous êtes assujettis à des taxes lorsque vous vendez des biens au niveau local ou international.

## Si vous vendez sur le marché intérieur

Une fois que vous avez configuré votre Shopify pour recouvrer les taxes dans votre pays ou région, vous pouvez décider de la manière dont vous souhaitez afficher les prix en magasin.
Vous contrôlez cela en activant ou en désactivant le bouton bascule **Tous les prix sont taxes comprises** dans les paramètres [**Taxes et droits de douanes**](https://www.shopify.com/admin/settings/taxes) de votre administrateur **Shopify**.

Il est courant que ce bouton bascule soit activé pour des pays tels que l’Australie, l’Autriche, la Belgique, la République tchèque, le Danemark, la Finlande, la France, l’Allemagne, l’Islande, l’Italie, les Pays-Bas, la Nouvelle-Zélande, la Norvège, l’Espagne, la Suède, la Suisse et le Royaume-Uni. Sur des marchés comme ceux-ci, le prix *100 euros* défini dans la fiche produit contient déjà la taxe sur la valeur ajoutée (TVA) et c’est ce prix qui est affiché au client en magasin et à la caisse.  

Aux États-Unis et au Canada, les clients s’attendent à voir les prix des produits hors taxes, et les taxes sont ajoutées à la caisse. Dans ces deux pays, le champ **Tous les prix sont taxes comprises** n’est généralement pas sélectionné. Dans ce cas, le prix *100 $* défini dans la fiche produit représente le prix HT. Au moment du paiement, les taxes seront ajoutées au prix pour correspondre au montant total.

Pour prendre en charge le scénario où **Tous les prix sont taxes comprises** est sélectionné sur le côté [!INCLUDE[prod_short](../includes/prod_short.md)], renseignez le champ **Code modèle client** sur la page **Fiche magasin Shopify** pour accéder au modèle avec les champs suivants définis :  

1. **Groupe comptabilisation marché**, utilisé pour les clients nationaux.  
2. **Groupe compta. marché TVA**, utilisé pour les clients nationaux.  
3. **Prix TTC** défini sur *Oui*.  

Définissez maintenant les prix article dans le champ **Fiche article** ou dans le champ **Liste prix vente**, avec ou sans taxe. Lors de l’exportation des prix vers Shopify, le système calcule le prix afin d’inclure les taxes nationales, puis affiche ce prix dans la fiche produit dans Shopify.

> [!NOTE]
> Si vous avez configuré le connecteur Shopify pour créer automatiquement des clients, vous aurez peut-être besoin de plus de champs dans votre modèle, par exemple **Groupe compta. client**. Si vous utilisez le client par défaut pour les commandes importées, assurez-vous les mêmes champs sont renseignés pour le client. Vous devez encore renseigner le champ **Code modèle client** comme indiqué ci-dessus, car le champ **Prix TTC**/**Prix TTC** dans le document vente créé ne dépend pas du client, mais du **Modèle client** de la page Fiche magasin Shopify ou du modèle client par pays.

## Si vous vendez à l’international

Dans cette section, nous allons explorer les paramètres des scénarios dans lesquels vous devez recouvrer des taxes lors de la vente dans un autre pays, par exemple d’autres pays de l’UE.

Actuellement, l’extension **connecteur Shopify** prend en charge l’exportation d’un seul prix. Shopify applique automatiquement les taxes locales, les devises et les arrondis. Le bouton bascule **Tous les prix sont taxes comprises** entraîne les actions décrites dans les sous-sections suivantes.

### *Tous les prix sont taxes comprises* est sélectionné

|-|Ventes nationales|Pays étranger où vous recouvrez des taxes|Pays étranger où vous ne recouvrez pas de taxes|
|------------------------|--------|--------|--------|
|Prix affiché en magasin|1200|1200|1200|
|Pourcentage de taux de taxe|20|25|0|
|Prix à la caisse|1200|1200|1200|

Le prix pour le client reste inchangé, quel que soit sa localisation, mais cela affecte votre marge, car les taux de taxe sont différents selon les pays.

### *Tous les prix sont taxes comprises* n’est pas sélectionné

|-|Ventes nationales|Pays étranger où vous recouvrez des taxes|Pays étranger où vous ne recouvrez pas de taxes|
|------------------------|--------|--------|--------|
|Prix affiché en magasin|1 000|1 000|1 000|
|Pourcentage de taux de taxe|20|25|0|
|Prix à la caisse|1200|1250|1 000|

Shopify ajoute les taxes locales en plus du prix défini sur la fiche produit en fonction de l’endroit où les marchandises sont expédiées.

## Tarification TTC dynamique

Étant donné que différents pays ont des exigences différentes, selon que vous incluez ou non la taxe dans le prix affiché, vous pouvez activer [Tarification TTC dynamique](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) dans Shopify. La fonction d’inclusion de la taxe est ainsi automatisée.

Sélectionner **Inclure ou exclure les taxes en fonction du pays de votre client** dans la section **Autres marchés – Préférences** des paramètres [**Marchés**](https://www.shopify.com/admin/settings/markets) dans votre **Administrateur Shopify**.  

> [!NOTE]
> Ce paramètre n’affecte pas la représentation des prix sur les marchés nationaux, qui est contrôlée par le bouton bascule **Tous les prix sont taxes comprises**.

### *Tous les prix sont taxes comprises* est sélectionné

|-|Ventes nationales|Pays étranger où la taxe est incluse dans le prix|Pays étranger où la taxe n’est pas incluse|
|------------------------|--------|--------|--------|
|Prix affiché en magasin|1200|1250|1 000|
|Pourcentage de taux de taxe|20|25|10|
|Prix à la caisse|1200|1250|1100|

Le prix pour chaque client varie en fonction de la localisation du client.

### *Tous les prix sont taxes comprises* n’est pas sélectionné

|-|Ventes nationales|Pays étranger où la taxe est incluse dans le prix|Pays étranger, où la taxe n’est pas incluse|
|------------------------|--------|--------|--------|
|Prix affiché en magasin|1 000|1250|1 000|
|Pourcentage de taux de taxe|20|25|10|
|Prix à la caisse|1200|1250|1100|

> [!NOTE]
> Le bouton bascule **Tous les prix sont taxes comprises** ne modifie pas la façon dont les prix sont affichés pour les clients internationaux.

## Si vous vendez à des clients de l’UE

Différents pays de l’UE ont des taux de taxes locales différents. Toutefois, si vous êtes situé dans l’UE et que vous vendez dans d’autres pays de l’UE, vous pouvez, dans certains cas, utiliser votre taux de taxe local.  

Cochez la case **Recouvrer la TVA** dans la section **Union européenne** des paramètres [**Taxes et droits de douanes**](https://www.shopify.com/admin/settings/taxes) dans votre **Administrateur Shopify**.

|Recouvrer la TVA|Taux de TVA|
|-|-|
|Exonération des micro-entreprises|Utiliser votre taux de taxe national pour toutes les ventes à l’intérieur de l’UE|
|Guichet unique ou identification spécifique au pays|Utiliser le taux de TVA du pays de votre client|


### Recouvrer la TVA définie sur l’identification à guichet unique

Dans l’exemple suivant, le bouton bascule **Tous les prix sont taxes comprises** est activé. Le prix sur la fiche produit est fixé à *1 200*.
        
|-|Ventes nationales|Pays étranger|
|------------------------|--------|--------|
|Prix affiché en magasin|1200|1250|
|Pourcentage de taux de taxe|20|25|
|Prix à la caisse|1200|1250|       
        
### Recouvrer la TVA fixée définie sur l’exonération des micro-entreprises

Dans l’exemple suivant, le bouton bascule **Tous les prix sont taxes comprises** est activé. Le prix sur la fiche produit est fixé à *1 200*.
        
|-|Ventes nationales|Pays étranger avec un taux de taxe local de 25 %.|
|------------------------|--------|--------|
|Prix affiché en magasin|1200|1200|
|Pourcentage de taux de taxe|20|20|
|Prix à la caisse|1200|1200|           
    
Shopify ignore le taux de taxe dans le pays étranger lors du calcul des prix finaux et utilise le taux de taxe national.

## Importation des commandes Shopify vendues à des clients internationaux

Si vous recouvrez des taxes dans plusieurs pays, vous devrez probablement définir un paramètre spécifique au pays dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Cela est nécessaire car lorsqu’un document de vente est créé dans [!INCLUDE[prod_short](../includes/prod_short.md)], le système calcule les taxes au lieu de réutiliser celles importées de Shopify.

Les paramètres spécifiques au pays/région sont choisis dans la fenêtre **Modèle client Shopify**. C’est là que vous pouvez définir **N° client par défaut** ou **N° modèle client**. Dans les deux cas, assurez-vous que les champs suivants sont définis pour le client ou le modèle sélectionné :

1. **Groupe comptabilisation marché** (utilisé pour les clients étrangers).
2. **Groupe compta. marché TVA** (utilisé pour les clients étrangers).
3. **Prix TTC** (aligné avec le réglage sur le côté Shopify) :
* Choisissez *Oui* si **Tous les prix sont taxes comprises** est activé et **Inclure ou exclure les taxes en fonction du pays de votre client** est désactivé.
* Choisissez *Non* si **Tous les prix sont taxes comprises** est désactivé et **Inclure ou exclure les taxes en fonction du pays de votre client** est désactivé.
* Choisissez *Oui* si **Inclure ou exclure les taxes en fonction du pays de votre client** est activé, et le pays ou la région est répertorié dans [Pays TTC](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Choisissez *Non* si **Inclure ou exclure les taxes en fonction du pays de votre client** est activé, et le pays ou la région n’est pas répertorié dans [Pays TTC](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> Le paramètre du champ **Prix TTC** provient du modèle, pas du client spécifique. C’est pourquoi il est important que le modèle client soit défini.

## Autres remarques sur les taxes

Même si la commande Shopify importée contient des informations sur les taxes, les taxes sont recalculées lorsque vous créez le document vente. Ce nouveau calcul indique qu’il est important que les paramètres TVA/Taxe soient corrects dans [!INCLUDE[prod_short](../includes/prod_short.md)].

- Plusieurs taux de taxe ou de TVA sur les produits. Par exemple, certaines catégories de produits peuvent bénéficier de taux de taxe réduits. Vous pouvez utiliser la fonctionnalité de [remplacement des taxes](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) dans Shopify. Lorsque des articles sont importés et créés dans [!INCLUDE[prod_short](../includes/prod_short.md)], ils utilisent le paramètre de taxe tel qu’il est renseigné sur le code modèle article dans le magasin Shopify. Avant d’importer des commandes avec ces articles, vous devez mettre à jour le groupe comptabilisation des produits TVA.  

- Taux de taxe dépendant de l’adresse. Utilisez le champ **Priorité zone recouvrement** avec le tableau **Modèles client** pour remplacer la logique standard qui remplit le **Code zone recouvrement** dans le document vente. Le champ **Priorité zone recouvrement** spécifie la priorité qui indique à la fonction où prendre des informations sur le pays ou la région, et sur l’état ou la province. L’enregistrement correspondant dans les modèles client Shopify est ensuite identifié, et les champs **Code zone recouvrement**, **Soumis à recouvrement** et **Groupe compta. marché TVA** sont utilisés lors de la création d’un document vente.  

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
