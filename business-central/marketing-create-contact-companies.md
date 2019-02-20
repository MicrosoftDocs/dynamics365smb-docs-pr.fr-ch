---
title: "Créer des sociétés contact| Microsoft Docs"
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: fr-ch
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Création de sociétés contact
Votre société rencontre régulièrement des sociétés prospects qui deviennent généralement des relations d'affaires. Lorsqu'un nouveau contact est établi, ces informations doivent être enregistrées afin que la communication puisse continuer.

Le fait d'indiquer un maximum de données à propos d'une société spécifique assure une communication efficace. Par exemple, spécifier le secteur d'activité approprié permet de s'assurer que des sociétés spécifiques sont ciblées par une communication donnée.

Vous pouvez également définir la relation d'affaires que vous avez avec un contact. Par exemple, un contact peut être un prospect, une banque ou un contractant.

## <a name="creatinge-contact-companies"></a>Création de sociétés contact
Vous pouvez créer un contact pour chaque nouvelle société avec laquelle vous êtes en contact, par exemple un client, un fournisseur, un prospect, une banque, un cabinet d'avocats, un consultant, et ainsi de suite.

Il existe deux méthodes permettant de créer un contact : à partir de zéro ou à partir d'un client, d'un fournisseur ou d'un compte bancaire existant.

Avant de créer un contact, vous pouvez vérifier les paramètres sur la page **Paramètres Marketing**. Pour plus d'informations, voir [Paramétrage de la Gestion des relations](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Pour créer un contact société à partir de zéro
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **N°**, saisissez le numéro du contact.

    Si vous avez configuré une souche de numéros pour les contacts sur la page **Paramètres Marketing**, appuyez sur la touche Entrée pour sélectionner le numéro de contact suivant.  
4. Définissez **Type** à **Société**.
5. Renseignez les autres champs selon vos besoins.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Pour créer un contact société à partir d'un client, d'un fournisseur ou d'un compte bancaire
Si vous avez configuré plusieurs clients, fournisseurs et comptes bancaires, vous pouvez créer des contacts sur la base des données existantes. Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées avec les informations du client, du fournisseur ou du compte bancaire.

> [!NOTE]  
>   Avant de créer des sociétés contact de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs, ainsi que des comptes bancaires sur la page **Paramètres marketing**. Si vous devez créer des contacts à partir de comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires sur la page **Paramètres comptabilité**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez une des actions suivantes, selon l'emplacement à partir duquel vous souhaitez créer des contacts, puis sélectionnez le lien associé.
   * **Créer contacts à partir des clients**
   * **Créer des contacts à partir des fournisseurs**
   * **Créer des contacts à partir des comptes bancaires**
2. Sur la page de traitement par lots qui s'affiche, dans la section **Client**, **Fournisseur** ou **Compte bancaire**, définissez des filtres si vous souhaitez créer des contacts à partir de clients, de fournisseurs ou de comptes bancaires spécifiques.
3. Pour démarrer la création de contacts, cliquez sur le bouton **OK**.

    Les numéros de contact suivants de la souche de numéros sont affectés aux nouveaux contacts. La relation d'affaires des fournisseurs qui est spécifiée sur la page **Paramètres Marketing** est affectée aux contacts nouvellement créés.

> [!TIP]  
>   Vous pouvez également créer un client, un fournisseur ou un compte bancaire à partir d'un contact. Pour plus d'informations, reportez-vous à [Créer un client, un fournisseur ou un compte bancaire à partir d'un contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires
Si certains de vos contacts sont également des clients, des fournisseurs ou des comptes bancaires, vous pouvez synchroniser les informations de contact avec le client, le fournisseur ou le compte bancaire correspondant. Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.  

Pour pouvoir synchroniser vos contacts avec des clients, des fournisseurs ou des comptes bancaires, vous devez spécifier un code relation d'affaires pour ces derniers sur la page **Paramètres marketing**. Pour plus d'informations, voir [Paramétrage de la Gestion des relations](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Différentes manières de synchroniser les contacts avec les clients, les fournisseurs et les comptes bancaires
Pour synchroniser vos contacts avec des clients, des fournisseurs ou des comptes bancaires, choisissez l'une des trois méthodes suivantes :

* Liaison de contacts avec des clients, des fournisseurs ou des comptes bancaires existants à partir de la fiche contact. Pour plus d'informations, voir [Liaison de contacts avec des clients, des fournisseurs et des comptes bancaires](marketing-how-link-contact.md).
* Créez des clients, des fournisseurs ou des comptes bancaires à partir du contact. Pour plus d'informations, reportez-vous à [Créer un client, un fournisseur ou un compte bancaire à partir d'un contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Créez des contacts à partir de clients, fournisseurs ou comptes bancaires. Pour plus d'informations, voir [Créer un contact société à partir d'un client, d'un fournisseur ou d'un compte bancaire](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Conséquences de la synchronisation
Lorsque le contact est synchronisé avec le client, le fournisseur ou le compte bancaire :

* Vous n'avez besoin de mettre à jour les données que dans une seule fiche. Par exemple, si vous modifiez le numéro de téléphone au niveau du contact, le numéro de téléphone est automatiquement mis à jour avec la même modification au niveau du client, du fournisseur ou du compte bancaire.
* Si vous avez spécifié une souche de numéros pour les contacts, une fiche contact est automatiquement créée pour le client, le fournisseur ou le compte bancaire lorsque vous créez une fiche client, fournisseur ou compte bancaire.
* Vous pouvez créer des devis, des commandes de vente, des demandes de prix et des commandes d'achat à partir du contact.
* Vous pouvez enregistrer vos interactions lorsque vous effectuez des opérations telles que l'impression de commandes et de commandes ouvertes, la création de commandes pour le service des ventes, l'envoi d'e-mails, etc.
* Si vous supprimez un contact lié à un client, un fournisseur ou un compte bancaire, seule le contact est effacé. Le client, le fournisseur ou le bancaire est conservé.
* Si vous supprimez un client, un fournisseur ou un compte bancaire lié à un contact, le contact est conservé.

> [!NOTE]  
>   Certaines informations, par exemple concernant la facturation et la validation, n'apparaissent pas sur la fiche contact. Par conséquent, vous pouvez les ajouter manuellement sur la fiche client, la fiche fournisseur ou la fiche compte bancaire lorsque vous créez des contacts en tant que clients, fournisseurs ou comptes bancaires.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Liaison de contacts avec des clients, des fournisseurs et des comptes bancaires
Si vous disposez d'un contact et d'un client, d'un fournisseur ou d'un compte bancaire pour la même société, vous pouvez lier les deux entités. Lier les deux entités vous permet de synchroniser les données communes afin qu'elles soient identiques aux deux emplacements.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Pour lier un contact à un client, un fournisseur ou un compte bancaire existant
1. Ouvrez le contact que vous souhaitez lier.
2. Sélectionnez l'action **Lier avec existant**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
3. Sélectionnez le client, le fournisseur ou le compte bancaire à lier.

   Dans le champ **Champs prioritaires**, spécifiez les champs à considérer comme prioritaires en cas de conflit d'informations entre les champs communs au contact et au client, au fournisseur ou au compte. Par exemple, si le code vendeur est différent entre le contact et le client, vous pouvez décider d'utiliser les données du contact en sélectionnant **Contact**.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Création d'un client, d'un fournisseur ou d'un compte bancaire à partir d'un contact
   Vous pouvez enregistrer certains de vos contacts existants en tant que clients, fournisseurs ou comptes bancaires. Créer un client, un fournisseur ou un compte bancaire à partir d'un contact vous permet d'utiliser des données existantes. Lorsque vous créez un client, un fournisseur ou un compte bancaire de cette façon, celui-ci est synchronisé avec le contact. Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.

   Avant de pouvoir enregistrer des contacts de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs et les comptes bancaires sur la page **Paramètres marketing**. Si vous devez enregistrer des contacts en tant que comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires sur la page **Paramètres comptabilité**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Pour créer un contact comme client, fournisseur ou compte bancaire
   1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
   2. Sélectionnez le contact que vous souhaitez créer comme client, fournisseur ou compte bancaire.
   3. Sélectionnez l'action **Créer comme**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
   4. Répondez par l'affirmative au message qui s'affiche.

   Les informations du contact sont transférées depuis la fiche **Contact** vers la fiche **Compte bancaire**, **Client** ou **Fournisseur**. Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements.

## <a name="setting-up-business-relations-on-contact-companies"></a>Configuration des relations d'affaires sur des sociétés contact
Les relations d'affaires vous permettent d'indiquer les rapports établis avec vos contacts, tels que les prospects, les banques, les consultants, les prestataires de services, et ainsi de suite.

L'utilisation des relations d'affaires sur les contacts processus en deux étapes. Tout d'abord, vous définissez le code relation d'affaires. Vous ne devez effectuer cette étape qu'une seule fois pour chaque relation d'affaires. Une fois que vous disposez d'un code relation d'affaires, vous pouvez commencer à affecter le code aux sociétés contact.

> [!NOTE]  
>   Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.

### <a name="to-define-a-business-relation-code"></a>Pour définir un code relation d'affaires
Le code relation d'affaires définit une catégorie ou un type de relation d'affaires, telles que BANQUE ou Avocat. Vous pouvez disposer de plusieurs codes relation d'affaires. Pour définir la relation d'affaires, vous utilisez la page **Relations d'affaires**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Relations d'affaires**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

### <a name="AssignBusRelContact"></a> Pour affecter des relations d'affaires à un contact
Vous ne pouvez pas affecter de relations d'affaires à un individu, mais uniquement à des sociétés.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Relations d'affaires**.

    La page **Relations d'affaires contact** s'ouvre.
3. Dans le champ **Code relation d'affaires**, sélectionnez la relation d'affaires à affecter.

Répétez ces étapes pour chaque relation d'affaires à affecter. Vous pouvez également affecter des relations d'affaires à partir de la liste des contacts en suivant la même procédure.

Le nombre de relations d'affaires que vous avez affectées au contact s'affiche dans le champ **Nbre relations d'affaires** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des relations d'affaires à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="see-also"></a>Voir aussi
[Création de personnes contact](marketing-create-contact-persons.md)   
[Utilisation de Business Central](ui-work-product.md)

