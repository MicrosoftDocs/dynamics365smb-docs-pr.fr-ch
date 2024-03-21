---
title: Configurer et utiliser le connecteur Shopify
description: Divers scénarios d’intégration pour démontrer le workflow entre Shopify et Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Procédure pas à pas : configurer et utiliser le connecteur Shopify

Cette section illustre certains scénarios typiques et vous guide à travers les étapes pour tester ou former les utilisateurs sur le workflow du magasin intégré [!INCLUDE[prod_short](../includes/prod_short.md)] et du magasin Shopify.

## Conditions préalables 

### Shopify

Vous devez disposer :

- D’un compte Shopify
- D’une boutique en ligne Shopify

En savoir plus sur la création de versions d’essai Shopify et les paramètres recommandés dans [Créer et configurer un compte Shopify](shopify-account.md).

### Business Central

Vous devez disposer d’un compte [!INCLUDE[prod_short](../includes/prod_short.md)]. 

Par exemple, vous pouvez créer un compte démo ou démarrer un essai. Pour en savoir plus, rendez-vous sur [Préparer les environnements de démonstrations de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) et [S’inscrire à l’essai](../trial-signup.md). 

## Connexion de Business Central à la boutique Shopify

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Dans le champ **Code**, entrez `DEMO1`.
4. Dans le champ **URL Shopify**, saisissez l’URL de la boutique en ligne à laquelle vous souhaitez vous connecter.
5. Activez le bouton à bascule **Activé**, lisez et acceptez les conditions générales.

Pour configurer le magasin Shopify, procédez comme suit :

1. Désactivez **Autoriser les synchronisations en arrière-plan**.
2. Sélectionnez *Vers Shopify* dans le champ **Synchroniser l’article**.
3. Sélectionnez *Vers Shopify* dans le champ **Synchroniser les images de l’article**.
4. Activez le bouton à bascule **Synchroniser les attributs d’un article**.
5. Activez le bouton bascule **Stock suivi**.
6. Sélectionnez *Refuser* dans le champ **Règle de stock par défaut** .
7. Activez le bouton de basculement **Créer automatiquement des clients inconnus**.
8. Remplissez le champ **Code modèle client/Société** avec le modèle approprié.
9. Remplissez le **Compte de frais d’expédition**, le **Compte de pourboires** avec le compte de revenus. Par exemple, aux É.-U., utilisez `40210`.
10. Activez le bouton de basculement **Créer automatiquement des commandes**.
11. Désactivez le bouton **Lancer automatiquement les commandes clients**.

Configurer le mappage de l’emplacement :

1. Sélectionnez l’action **Emplacements** pour ouvrir **Emplacements des magasins Shopify**.
2. Sélectionnez l’action **Obtenir les emplacements Shopify** pour importer tous les emplacements définis dans Shopify. Sélectionnez l’entrée avec la bascule **Est principal** est sélectionnée.
3. Dans **Filtre magasin**, entrez `''|EAST|MAIN`.
4. Sélectionnez *Solde disponible projeté à aujourd’hui* dans le **Calcul des stocks** pour activer la synchronisation des stocks pour un emplacement Shopify sélectionné.

## Procédure pas à pas : commencer à vendre des produits en ligne

### Scénario

Disons que vous voulez essayer Shopify en tant que boutique en ligne sans passer beaucoup de temps à configurer les choses, surtout parce que vous entretenez déjà vos articles dans [!INCLUDE[prod_short](../includes/prod_short.md)] correctement. Après avoir lancé votre boutique en ligne Shopify, vous obtenez immédiatement de nouveaux clients qui sont satisfaits de votre boutique et de leur expérience d’achat. Alors, ils décident de laisser des pourboires à la caisse.

### Étapes

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
2. Sélectionnez **Ajouter des articles**.
3. Dans le champ **Code magasin**, entrez `DEMO1`.
4. Définissez le filtre `CHAIR` sur le champ **Code de catégorie d’article**.
5. Activez le bouton à bascule **Synchroniser les images de produit**.
6. Activez le bouton bascule **Synchroniser le stock**.
7. Sélectionnez **OK** et attendez que la synchronisation initiale des articles, des prix et le stock soit terminée.

Dans la **boutique en ligne Shopify** :
> [!Tip]  
> Ouvrez **Admin Shopify** en accédant à l’URL spécifiée dans le champ **URL** de la page **Carte de la boutique Shopify**. Sélectionnez l’icône en forme d’œil à côté du canal de vente de la **boutique en ligne**, située dans la barre latérale **Admin Shopify**. 

Ouvrez le catalogue de produits. Avis :

* Titres, images et prix des produits.
* Indicateur de disponibilité (épuisé pour les produits en rupture de stock).

Choisissez n’importe quel produit qui peut être vendu, par exemple, `BERLIN Swivel Chair, yellow`. Notez que la description contient des attributs d’élément.

Sélectionnez **Acheter maintenant** et passez à la caisse.

1. Dans le champ **Adresse e-mail ou numéro de téléphone portable**, saisissez `cl@contoso.com` (ou l’adresse e-mail à laquelle vous souhaitez recevoir les confirmations de commande et d’expédition).
2. Dans les champs **Prénom** et **Nom**, saisissez `Claudia Lawson`.
3. Entrez l’adresse locale.
4. Cochez la case **Enregistrer ces informations pour la prochaine fois** .
6. Conservez *Standard* comme mode d’expédition.
8. Dans le champ **N° de carte de crédit**, saisissez `1` si vous utilisez *(pour tester) Bogus Gateway*, ou saisissez `5555 5555 5555 4444` si vous utilisez *Shopify Payments* en mode test.
9. Renseignez le champ **Nom sur la fiche**.
10. Dans le champ **Date d’expiration**, saisissez le mois/l’année en cours.
11. Dans le champ **Code de sécurité**, entrez `111`.
7. Facultatif : Sélectionnez un pourboire de `10%`.
8. 12. Sélectionnez **Payer maintenant**.

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], exécutez l’une des prochaines étapes :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Commandes Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Synchroniser les commandes à partir de Shopify**.
3. Sélectionnez **OK**.

La commande importée est prête à être traitée.

1. Sélectionnez la commande importée pour ouvrir la fenêtre **Commande Shopify**.
2. Notez que le client et la commande client sont créés.
3. Explorez les actions **Risque** et **Coût d’expédition**.
4. Sélectionnez **Commande vente** pour ouvrir la fenêtre **Commande vente**. La commande vente est une demande qui, si nécessaire, peut être couverte par l’assembly, la production ou l’achat à l’aide du moteur de planification. Il prend également en charge divers processus de manutention en entrepôt avec une séparation complète des tâches.
6. Dans le champ **Agent**, saisissez `DHL`. Rouvrez la commande si nécessaire en choisissant l’action **Réouvrir** .
7. Dans **N° de suivi du colis**, entrez `123456789`.
8. Sélectionnez **Valider**, conservez l’option **Expédier et facturer** , puis sélectionnez **OK**.

Désormais, les données physiques et financières sont enregistrées dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Il est temps d’informer Shopify des changements.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Synchroniser les livraisons avec Shopify** et sélectionnez le lien associé.
2. Sélectionnez **OK**.

Dans **Admin Shopify** notez que la commande est maintenant marquée comme *Exécuté*. Vous pouvez également consulter les détails de l’envoi et y voir l’URL de suivi. Si vous exécutez à nouveau **Synchroniser les commandes à partir de Shopify**, la commande sera archivée dans les deux systèmes.

## Procédure pas à pas : ajouter vos clients dans votre nouvelle boutique en ligne

### Scénario

Après un lancement rapide et réussi de votre nouvelle boutique en ligne, vous souhaitez que vos clients actuels la visitent et commencent à passer des commandes. En fonction de votre Shopify plan et processus, vous pouvez essayer les flux B2B et D2C.

### Étapes D2C

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Clients Shopify** et sélectionnez le lien associé.
2. Sélectionnez **Ajouter des clients**.
3. Dans le champ **Code magasin**, entrez `DEMO1`.
4. Définir le filtre `20000` sur **N°** .
5. Sélectionnez **OK** et attendez que la synchronisation initiale des clients soit terminée.

Dans **Admin Shopify** notez que le client a été importés. Ouvrez les clients et remarquez que le prénom et le nom du client proviennent du champ **Nom du contact** de la **Fiche client**. Le nom de l’entreprise se trouve dans l’adresse par défaut, liée au client. Si vous utilisez *Comptes clients classiques*, vous pouvez sélectionner **Envoyer une invitation au compte** pour inviter le client. Avec *Nouveaux comptes clients* aucun mot de passe n’est requis pour que les clients se connectent. Shopify permet à vos clients de se connecter à l’aide d’un 6- code de vérification à chiffres envoyé par e-mail. 

### Étapes B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Sociétés Shopify** et sélectionnez le lien associé.
2. Sélectionner **Ajouter une société**.
3. Dans le champ **Code magasin**, entrez `DEMO1`.
4. Définir le filtre `30000` sur **N°** .
5. Sélectionnez **OK** et attendez que la synchronisation initiale des clients soit terminée.

Dans **Shopify Admin**, notez que la société et le client ont été importés. Ouvrez les clients et remarquez la zone d’informations sur l’entreprise avec un lien vers l’entreprise, l’emplacement et les autorisations attribuées. Sélectionnez **[...]** dans la **récap société, puis sélectionnez **Envoyer un e-mail d’accès B2B** pour inviter le client.

## Procédure pas à pas : ajustement de la gestion des articles

### Scénario 

Vous aimerez ajouter plus de flexibilité et de contrôle à vos processus de gestion des articles. Vous souhaitez améliorer les descriptions de produits et souhaitez ajouter plus d’étapes de révision avant que les produits ne soient disponibles pour tous les clients.

### Étapes

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], procédez comme suit :

Préparez les données.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Groupe prix client** et sélectionnez le lien associé.
2. Ajoutez un nouveau groupe de tarifs. Dans le champ **Code**, entrez `SHOPIFY`.
3. Fermez fenêtre **Groupe prix client**.
4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Articles** et sélectionnez le lien associé.
5. Sélectionnez l’élément *1896-S, Bureau d’Athènes*, puis procédez comme suit :

6. Sélectionnez l’action **Variantes**, puis ajoutez deux variantes : `PREMIUM, Athens Desk, Premium edition` et `ESSENTIAL, Athens Desk, Essential edition`.
7. Sélectionnez l’action **Texte marketing** et utilisez le **Brouillon avec Copilot** pour obtenir un texte créatif et engageant. Si la suggestion de texte marketing n’est pas activée, saisissez simplement : **Un design simple et élégant** se marie à n’importe quel ensemble. *Disponible en deux éditions.*. 
8. Sélectionnez l’action **Prix de vente** et ajoutez de nouveaux prix comme indiqué dans le tableau suivant :

   |Ligne|Type vente|Code vente|Type|Code|Code variante<br>(ajoutez le champ via la personnalisation)|Prix unit|
   |------|------------|------------|------------|----------------|------------|------------|
   |0|Groupe prix client|SHOPIFY|Article|1896-S|ESSENTIAL|700|
   |2|Groupe prix client|SHOPIFY|Article|1896-S|PREMIUM|1 000|

9. Sélectionnez l’action **Remises sur les ventes** et ajoutez une nouvelle remise :

   * **Type de vente** *Groupe rem. client*
   * **Code vente** *VENTE AU DÉTAIL*
   * **Type** *Article*
   * **Code** *1896-S*
   * **Code unité** *PCS*
   * **% Remise ligne** *10*

10. Sélectionnez l’action **Références article** et ajoutez les lignes suivantes :

   |Ligne|Type référence|N° référence|Code variante|
   |------|------------|------------|------------|
   |0|Code-barres|77777777|ESSENTIAL|
   |2|Code-barres|11111111|PREMIUM|

11. Sélectionnez l’élément *1920-S, Table de conférence ANVERS*, puis procédez comme suit :
12. Sélectionnez **Ajuster le stock** et dans le champ **Nouveau stock**, saisissez `100` pour les emplacements *EST* et *OUEST*. 
13. Sélectionnez **OK**.

Ajustez les paramètres de synchronisation.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et sélectionnez le lien associé.
2. Sélectionnez le magasin `DEMO1`1 pour lequel vous voulez synchroniser les articles pour ouvrir la page **Shopify Fiche magasin**.
3. Activez le champ **Synchronisation du texte Marketing**.
4. Sélectionnez *N° d’article + code de variante* dans le champ **Mappage SKU**.
5. Sélectionnez *Continuer* dans le champ **Règle de stock par défaut** .
6. Sélectionnez *Brouillon* dans le champ **Statut des produits créés**.
7. Sélectionnez *Statut à archiver* dans le champ **Action pour le produit supprimé**.
8. Sélectionnez *SHOPIFY* dans le champ **Groupe de prix client**.
9. Sélectionnez *VENTE AU DÉTAIL* dans le champ **Groupe rem. client**.
 
Exécuter la synchronisation.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et sélectionnez le lien associé.
2. Sélectionnez le magasin `DEMO1`1 pour lequel vous voulez synchroniser les articles pour ouvrir la page **Shopify Fiche magasin**.
3. Sélectionnez **Produits** pour ouvrir la fenêtre **Produits Shopify**.
4. Sélectionnez l’action **Ajouter des articles**.
5. Définissez le filtre *TABLE|BUREAU* sur le champ **Code de catégorie d’article**.
6. Activez le bouton à bascule **Synchroniser les images de produit**.
7. Activez le bouton bascule **Synchroniser le stock**.
8. Sélectionnez **OK** et attendez que la synchronisation initiale des articles, des prix et le stock soit terminée.

Les produits sont ajoutés. Notez que le statut est défini sur *Brouillon*, par conséquent les articles ne sont pas visibles dans la boutique en ligne Shopify.

1. Sélectionnez la ligne avec l’article *1920-S, Table de conférence ANTWERP*. Dans le champ **Titre du SEO**, entrez le `Rectangular meeting table Antwerp, 10 seats, black`.
2. Dans le champ **Statut**, sélectionnez *Actif*.
3. Sélectionnez la ligne avec l’article *1906-S, ATHENS, Piédestal mobile*, puis sélectionnez **Supprimer**.

Dans **Admin Shopify**, notez que tous les produits ont des statuts différents.

* *ANTWERP Table de conférence* est *Active*, car nous avons modifié son statut dans la fenêtre **Produit Shopify**.
* *Bureau ATHENS* est un *Brouillon*, car nous avons configuré le statut par défaut pour tous les produits ajoutés sur *Brouillon*.
* Le *piédestal mobile ATHENS* est *Archivé* parce que nous avons configuré la boutique pour attribuer automatiquement le statut *Archivé* pour les produits supprimés.

Notez que le stock de la table de conférence ANTWERP est de 100, car nous avons configuré le système pour utiliser l’inventaire uniquement à partir de deux emplacements MAIN et EAST. Le stock à un autre emplacement (OUEST) est ignoré.

* Ouvrez *Table de conférence ANTWERP*, notez les champs **Type personnalisé**, **Fournisseur**, **Poids** et **Coût par article**, puis la section **Aperçu de la liste du moteur de recherche**.
* Ouvrez *Bureau Athens*, faites défiler jusqu’à la section **Variantes** et notez comment **SKU** est rempli.
* Sélectionnez **Modifier** pour revoir le code-barres et les prix.
* Modifiez le statut de *Bureau Athens* sur *Actif* et sélectionnez **Aperçu**.

Dans la **boutique en ligne Shopify**, ouvrez le catalogue de produits et recherchez le produit *Bureau ATHENS*. Notez que différentes options sont disponibles. Pour différentes options, les prix sont différents. Faites attention aux informations de réduction.

### Étapes supplémentaires pour le B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Vous pouvez configurer le connecteur pour créer et attribuer automatiquement un catalogue aux sociétés exportées. Les étapes ci-dessous sont utiles si vous souhaitez un contrôle plus précis de ce qui est disponible pour les clients B2B.

Dans **Shopify Admin**cCréez et attribuez un catalogue.

1. Sélectionnez **Produits** puis **Catalogues** dans la barre latérale de **Shopify admin**.
2. Créer un catalogue pour des produits spécifiques. Donnez le titre ’B2B’. 
3. Choisissez **Gérer** puis **Gérer les produits et les prix**.
4. Sélectionnez le filtre *Exclus* , recherchez *ATHERN Desk* et choisissez **Inclure dans le catalogue**.
5. Sélectionnez **Clients** puis **Sociétés** dans la barre latérale de **Shopify admin**.
6. Sélectionnez *École des Beaux-Arts* et choisissez **[...]** puis **Ajouter catalogues** et ajouter *B2B* catalogue créé précédemment.

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], procédez comme suit :

Préparez les données.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Articles** et sélectionnez le lien associé.

2. Sélectionnez l’élément **1896-S, Bureau d’Athènes**, puis procédez comme suit :

3. Sélectionnez l’action **Remises sur les ventes** et ajoutez une nouvelle remise :

   * **Type de vente** *Groupe rem. client*
   * **Code vente** *GRAND CPTE*
   * **Type** *Article*
   * **Code** *1896-S*
   * **Code unité** *PCS*
   * **% Remise ligne** *25*

4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Catalogues Shopify** et choisissez le lien associé.
5. Sélectionner **Obtenir les catalogues**.
6. Dans le champ **Code magasin**, entrez `DEMO1`.
7. Sélectionnez l’entrée portant le nom *B2B* catalogue pour laquelle vous souhaitez synchroniser les prix.
8. Activez le bouton **Synchroniser les prix** .
9. Sélectionnez *SHOPIFY* dans le champ **Groupe de prix client**.
10. Sélectionnez *GRAND CPTE* dans le champ **Groupe rem. client**.
11. Sélectionnez **Sync prix** et attendez que la synchronisation des prix soit terminée.

Dans **Shopify Admin**, explorez les prix du *B2B* catalogue.

Dans la **boutique en ligne Shopify**, ouvrez le catalogue de produits et recherchez le produit *Bureau ATHENS*. Notez que les prix sont des informations sur les réductions.

## Procédure pas à pas : vérification et synchronisation des commandes pour l’acheteur individuel et le représentant de l’entreprise
Ceci est la suite de la [Procédure pas à pas : Commencez à vendre des produits en ligne](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Vous pouvez également essayer avec vos propres données, par exemple, votre boutique ou bac à sable Shopify.

Acheteur individuel

1. Dans la **boutique en ligne Shopify**. Choisissez icône **compte**. Entrer e-mail accès à.
2. Connectez-vous à l’aide d’un code de vérification unique à 6 chiffres envoyé par e-mail que vous avez saisi.
3. Explorez le catalogue de produits, vous devriez pouvoir voir tous les produits avec leurs prix de détail.
4. Sélectionnez la variante Essential, puis sélectionnez **Acheter maintenant** et procédez au paiement.
5. Remplir **Prénom** et **Nom**.
6. Entrez l’adresse locale.
7. Conservez *Standard* comme mode d’expédition.
8. Dans le champ **N° de carte de crédit**, saisissez `1` si vous utilisez *(pour tester) Bogus Gateway*, ou saisissez `5555 5555 5555 4444` si vous utilisez *Shopify Payments* en mode test.
9. Dans le champ **Date d’expiration**, saisissez le mois/l’année en cours.
10. Dans le champ **Code de sécurité**, entrez `111`.
11. Renseignez le champ **Nom sur la fiche**.
12. Sélectionnez **Payer maintenant**.
 
Représentante société

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. Dans **Shopify Admin**.
2. Sélectionnez **Clients** puis **Sociétés** dans la barre latérale de **Shopify admin**.
3. Ouvrir *l’entrée à l’École des Beaux-Arts* .
4. Choisir **[...]** dans le récap **Ecole des Beaux-Arts**, puis **Modifier les conditions de paiement** et sélectionnez *Due à l’exécution*.
5. Choisir **[...]** dans le récap **Clients**, puis **Ajouter un client** et ajoutez-en un avec l’e-mail que vous avez utilisé pour vous connecter au magasin plus tôt.
6. Dans la **boutique en ligne Shopify**. Choisissez icône **compte**. Entrer e-mail accès à.
7. Connectez-vous à l’aide d’un code de vérification unique à 6 chiffres envoyé par e-mail que vous avez saisi.
8. Explorez le catalogue de produits, vous devriez pouvoir voir uniquement les produits ajoutés au *B2B* catalogue avec prix spéciaux de détail.
9. Sélectionnez la variante Essential, puis sélectionnez **Acheter maintenant** et procédez au paiement.
10. Notez que le compte, l’adresse d’expédition et le mode de paiement sont renseignés.
11. Remplissez le champ **Numéro de bon de commande** avec `PO-12345`.
12. Sélectionner **Soumettre la commande**.
 
Dans [!INCLUDE[prod_short](../includes/prod_short.md)], exécutez l’une des prochaines étapes :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Commandes Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Synchroniser les commandes à partir de Shopify**.
3. Sélectionnez **OK**.

La commande importée est prête à être traitée.

1. Sélectionnez la commande importée pour ouvrir la fenêtre **Commande Shopify**.
2. Notez que même si les deux commandes ont été soumises par la même personne, elles sont liées à deux clients différents. 
3. Dans la commande soumise au nom de l’entreprise, vous pouvez voir la valeur de **Numéro de bon de commande** champ, qui est également transféré au **Numéro de document externe** champ du document de vente créé.
4. Parce que nous avons configuré l’entreprise B2B pour gérer les paiements en dehors de Shopify le **Statut financier** est réglé sur *En attente*. Une fois le paiement reçu, sélectionnez le **Marquer comme payé** action. La situation financière sera mise à jour dans Shopify. 

## Procédure pas à pas : importer des articles, clients sociétés de Shopify

### Scénario 

Vous avez déjà une boutique en ligne performante et souhaitez commencer à l’utiliser [!INCLUDE[prod_short](../includes/prod_short.md)] comme logiciel de gestion d’entreprise. Vous souhaitez importer autant de données de Shopify que possible. 

### Étapes

Ceci est la suite de [Procédure pas à pas : Commencez à vendre des produits en ligne](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) et [Procédure pas à pas : Ajoutez vos clients à votre nouvelle boutique en ligne](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Vous pouvez également essayer avec vos propres données, par exemple, votre boutique ou bac à sable Shopify.

Dans [!INCLUDE[prod_short](../includes/prod_short.md)], suivez les étapes indiquées ci-dessous.

#### Préparer les données

1. Passez à un essai gratuit de 30 jours sans exemples de données. Pour plus d’informations, voir [Ajouter vos propres données à une société test vide](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify**, puis sélectionnez le lien associé.
3. Sélectionnez **Nouveau**.
4. Dans le champ **Code**, entrez `DEMO2`.
5. Dans le champ **URL Shopify**, saisissez l’URL de la boutique en ligne à laquelle vous souhaitez vous connecter.
6. Activez le bouton à bascule **Activé**, lisez et acceptez les conditions générales.

Configurez le magasin Shopify comme décrit ici :

1. Désactivez **Autoriser les synchronisations en arrière-plan**.
2. Sélectionnez *De Shopify* dans le champ **Synchroniser l’article**.
3. Activez le bouton à bascule **Créer automatiquement des articles inconnus**.
4. Remplissez le champ **Code modèle article** avec le modèle approprié.
5. Sélectionnez *De Shopify* dans le champ **Synchroniser les images de l’article**.
6. Sélectionnez *N° d’article + code de variante* dans le champ **Mappage SKU**.
7. Sélectionnez *Tous les clients* dans **Importation de clients depuis Shopify**.
8. Activez le bouton à bascule **Créer automatiquement un client inconnus**.
9. Remplissez le champ **Code modèle client/Société** avec le modèle approprié.
10. Sélectionnez *Tous les clients* dans **Importation de société depuis Shopify**.
11. Activez le bouton à bascule **Créer automatiquement des sociétés inconnus**.

#### Exécuter la synchronisation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasins Shopify** et sélectionnez le lien associé.
2. Sélectionnez le magasin *DÉMO2* pour lequel vous voulez synchroniser les données pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez **Synchroniser les produits**.
4. Sélectionnez **Synchroniser les images produit**.
5. Sélectionnez **Synchroniser les clients**.
6. Sélectionnez **Synchroniser les sociétés**

### Résultats

* Les produits Shopify sont importés. Pour vérifier, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Produits Shopify** et choisissez le lien associé.
* Des articles avec des images sont créés. Pour vérifier, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Article** et sélectionnez le lien associé.
* Les clients Shopify sont importés. Pour vérifier, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Clients Shopify** et sélectionnez le lien associé.
* Les sociétés Shopify sont importés. Pour vérifier, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Sociétés Shopify** et sélectionnez le lien associé.
* Les clients sont créés. Pour vérifier, sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Clients** et sélectionnez le lien associé.


## Voir aussi

[Mise en route avec le connecteur Shopify](get-started.md)  
