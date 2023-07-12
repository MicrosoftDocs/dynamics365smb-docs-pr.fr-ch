---
title: Synchroniser les clients
description: Importer les clients de ou les exporter dans Shopify
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# Synchroniser les clients

Lorsque vous importez une commande à partir de Shopify, les informations sur le client sont essentielles pour le traitement ultérieur du document dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Il existe deux options principales et plusieurs combinaisons :

* Utiliser un client spécial pour toutes les commandes.
* Importez les informations client réelles à partir de Shopify. Cette option est également disponible lorsque vous exportez des clients dans Shopify à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] en premier.

## Paramètres importants lors de l’importation de clients à partir de Shopify

Que vous importiez des clients à partir de Shopify en bloc ou lors de l’importation de commandes, les paramètres suivants permettent de gérer le processus :

|Champ|Description|
|------|-----------|
|**Importation client à partir de Shopify**|Sélectionnez **Tous les clients** si vous prévoyez d’importer des clients à partir de Shopify en bloc, soit manuellement en utilisant l’action **Synchroniser les clients**, soit via la file d’attente des tâches pour les mises à jour récurrentes. Quelle que soit la sélection, les informations client sont toujours importées avec la commande. Cependant, l’utilisation de ces informations dépend du champ **Modèles client Shopify** et des paramètres du champ **Type de mappage client**.|
|**Type de mappage client**|Définissez comment le connecteur effectue le mappage.<br>- **Par e-mail/téléphone**, pour que le connecteur mappe le client Shopify importé sur un client existant dans [!INCLUDE[prod_short](../includes/prod_short.md)] en utilisant l’e-mail et le téléphone.</br>- **Par informations de facturation**, pour que le connecteur utilise l’adresse du destinataire de la facture pour mapper le client Shopify importé sur un client existant dans [!INCLUDE[prod_short](../includes/prod_short.md)] en utilisant les informations d’adresse de la partie qui réceptionne la facture.</br>- Sélectionnez **Toujours prendre le client par défaut** pour que le système utilise un client du champ **N° client par défaut** . |
|**Shopify peut mettre à jour les clients**| Sélectionnez ce champ pour que le connecteur mette à jour les clients trouvés si les options **Par e-mail/téléphone** ou **Par informations de facturation** sont sélectionnées dans le champ **Type de mappage client**.|
|**Créer automatiquement des clients inconnus**| Sélectionnez ce champ pour que le connecteur crée les clients manquants si les options **Par e-mail/téléphone** ou **Par informations de facturation** sont sélectionnées dans le champ **Type de mappage client**. Un client est créé en utilisant les données importées et **Code modèle client** défini dans les pages **Fiche magasin Shopify** ou **Modèle client Shopify**. Remarquez que le client Shopify doit avoir au moins une adresse. Les commandes créées via le canal de vente du PDV Shopify manquent souvent de détails d’adresse. Si cette option n’est pas activée, vous devez créer un client manuellement et le lier au client Shopify.|
|**Code modèle client**|Ce champ est utilisé avec **Créer automatiquement des clients inconnus**.<br>- Choisissez le modèle par défaut à utiliser pour les clients créés automatiquement. Assurez-vous que le modèle sélectionné contient les champs obligatoires, tels que les champs **Groupe compta. marché**, **Groupe compta. client**, de TVA ou relatifs aux taxes.<br>- Vous pouvez définir des modèles par pays/région dans la page **Modèles client Shopify**, ce qui est utile pour calculer correctement les taxes. <br>- En savoir plus sur [Configurer les taxes](setup-taxes.md).|

### Modèle client par pays

Certains paramètres peuvent être définis au niveau du pays/de la région ou au niveau de l’état/de la province. Les paramètres peuvent être configurés dans [Expédition et livraison](https://www.shopify.com/admin/settings/shipping) sur Shopify.

Vous pouvez procéder comme suit pour chaque client avec le **Modèle client Shopify** :

1. Indiquer le **N° client par défaut**, qui a priorité sur la sélection présente dans les champs **Importation client à partir de Shopify** et **Type de mappage client**. Il est utilisé dans la commande vente importée.
2. Définir le **Code modèle client**, qui est utilisé pour créer des clients manquants, si l’option **Créer automatiquement des clients inconnus** est activée. Si le **Code modèle client** est vide, la fonction utilise le **Code modèle client** défini dans la page **Fiche magasin Shopify**. Le système essaie d’abord de trouver un modèle pour le **Code pays/région** pour l’adresse par défaut. S’il ne trouve pas de modèle, il utilise la première adresse.
3. Dans certains cas, le **Code modèle client** défini pour un pays n’est pas suffisant pour assurer le calcul correct des taxes (par exemple, pour les pays avec taxe de vente). Dans ce cas, la **Zone de recouvrement** peut constituer un complément utile.
4. Le champ **Zone recouvrement** contient également une paire **Code pays** et **Nom de la région**. Cette paire est utile lorsque le connecteur doit convertir un code en un nom, ou vice versa.

> [!NOTE]  
> Les codes pays sont les codes pays ISO 3166-1 alpha-2. En savoir plus sur le [Code postal](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Exporter les clients dans Shopify

Vous pouvez exporter les clients existants dans Shopify en bloc. Dans chaque cas, un client et une adresse par défaut sont créés. Vous pouvez gérer le processus avec les paramètres suivants :

|Champ|Description|
|------|-----------|
|**Exporter les clients dans Shopify**|Sélectionnez cette option si vous prévoyez d’exporter tous les clients de [!INCLUDE[prod_short](../includes/prod_short.md)] vers Shopify en bloc. Vous pouvez le faire soit manuellement, en utilisant l’action **Synchroniser les clients**, ou automatiquement, en utilisant une file d’attente de travaux pour les mises à jour récurrentes.<br> Lorsque vous exportez des clients avec des provinces/états, assurez-vous que **Code ISO** est rempli pour les pays/régions.|
|**Peut mettre à jour les clients Shopify**|Utilisé avec le paramètre **Exporter le client dans Shopify**. Activez cette option pour générer des mises à jour ultérieurement à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] pour les clients qui existent déjà dans Shopify.|

Voici les conditions requises pour exporter un client :

* Le client doit avoir une adresse e-mail valide.
* Un pays/région est sélectionné sur la fiche client, pour les clients locaux, avec pays/région vide, le pays/région spécifié sur la page **Informations sur la société** doit avoir un code ISO défini.
* Si le client a un numéro de téléphone, ce numéro doit être unique, car Shopify n’acceptera pas un deuxième client avec le même numéro de téléphone.
* Si le client a un numéro de téléphone, celui-ci doit être au format E.164. Différents formats sont pris en charge s’ils représentent un numéro qui peut être composé de n’importe où dans le monde. Les formats suivants sont valides :

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Une fois que vous avez créé les clients dans Shopify, vous pouvez leur envoyer des invitations directes les incitant à activer leurs comptes.

### Remplir les informations client dans Shopify

Un client dans Shopify a un prénom, un nom de famille, une adresse e-mail et/ou un numéro de téléphone. Vous pouvez renseigner le prénom et le nom de famille à partir de la fiche client dans [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorité|Champ de la fiche client|Désignation|
|------|------|-----------|
|0|**Nom du contact**|Priorité la plus élevée, si le champ **Nom du contact** est rempli et si le champ **Source du contact** dans la page **Fiche magasin Shopify** contient les options *Prénom et nom* ou *Nom et prénom*, ce qui définit comment diviser les valeurs.|
|2|**Nom 2**|Si le champ **Nom 2** est rempli et si le champ **Source nom 2** dans la page **Fiche magasin Shopify** contient les options *Prénom et nom* ou *Nom et prénom*, ce qui définit comment diviser les valeurs.|
|3|**Nom**|Priorité la moins élevée, si le champ **Nom** est rempli et si le champ **Origine nom** dans la page **Fiche magasin Shopify** contient les options *Prénom et nom* ou *Nom et prénom*, ce qui définit comment diviser les valeurs.|

Un client dans Shopify a également une adresse par défaut. L’adresse pourrait contenir, en plus du prénom, du nom, de l’e-mail et/ou du téléphone, la société et l’adresse. Vous pouvez remplir le champ **Société** en fonction des données présentes dans la fiche client dans [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorité|Champ de la fiche client|Désignation|
|------|------|-----------|
|0|**Nom**|Priorité la plus élevée, si le champ **Origine nom** dans la page **Fiche magasin Shopify** contient *Nom de la société*.|
|2|**Nom 2**|Priorité la moins élevée, si le champ **Source nom 2** dans la page **Fiche magasin Shopify** contient *Nom de la société*.|

Pour les adresses où la région/la province est utilisé(e), sélectionnez **Code** ou **Nom** dans le champ **Source région** sur la page **Fiche magasin Shopify**. Ceci spécifie le type de données stockées dans [!INCLUDE[prod_short](../includes/prod_short.md)] dans le champ **Région**. N’oubliez pas d’initialiser les modèles de clients par pays afin que le mappage code/nom de la région soit prêt. 


## Synchroniser les clients

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche 1.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Magasin Shopify**, puis sélectionnez le lien associé.
2. Sélectionnez le magasin spécifique pour lequel vous voulez synchroniser les clients.
3. Sélectionnez l’action **Synchroniser les clients**.

Sinon, vous pouvez utiliser l’action **Lancer la synchronisation des clients** dans la fenêtre **Clients Shopify** ou rechercher le traitement par lots **Synchroniser les clients**.

Vous pouvez programmer la tâche pour qu’elle soit exécutée de manière automatisée. En savoir plus dans la section [Programmer des tâches récurrentes](background.md#to-schedule-recurring-tasks).

## Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
