---
title: Créer des contacts professionnels
description: Décrit les tâches impliquées dans la création de contacts et la définition de vos relations commerciales sur la fiche de contact.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.date: 08/30/2022
ms.author: edupont
---
# Créez des contacts

Lorsque vous développez une relation d’affaires avec quelqu’un dans une autre entreprise, ajoutez-la en tant que contact dans [!INCLUDE[prod_short](includes/prod_short.md)]. Ensuite, ajoutez toute information sur eux, ou leur entreprise, qui peut être utile pour de futures communications. Sur la page **Fiche contact**, vous pouvez créer les types de contacts suivants :

* **Personne à contacter** : utiliser lorsque vous avez eu un contact direct avec quelqu’un et que vous avez ses coordonnées.
* **Entreprise** : utiliser si le contact n’est pas une personne physique, mais une entité, telle qu’un contractant ou une banque.

Les informations pertinentes pour chaque type de contact étant différentes, les champs et les actions disponibles sont différents. Par exemple, vous pouvez affecter des responsabilités uniquement à une personne et un secteur d’activité à une société.

Vous pouvez modifier ultérieurement la valeur du champ **Type**. Vous pouvez également utiliser les champs du raccourci **Héritage** sur la page **Configuration marketing** pour spécifier les données à partager entre une personne et son entreprise. En savoir plus sur [Configurer les contacts](marketing-setup-contacts.md).

Lorsqu’une fiche contact est convertie en fiche client, par exemple, la personne à contacter ou l’entreprise de contact devient le nom du client. L’enregistrement du contact est conservé et vous pouvez lier le contact et le client afin que leurs données soient synchronisées à l’avenir.

> [!NOTE]
> Si vous activez la [mise à jour des fonctionnalités pour les modèles de conversion](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees), vous pouvez également créer des fournisseurs ou des employés à partir de contacts professionnels.
>
> Cependant, si vous utilisez déjà la fonctionnalité intégrée pour créer automatiquement des clients ou des articles, cette mise à jour de fonctionnalité ne prend pas en charge les champs personnalisés et les clients ou articles nouvellement créés n’incluront pas ces données.

## Pour créer un contact manuellement

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Dans le champ **N°**, saisissez le numéro du contact.

   Si vous avez configuré une souche de numéros pour les contacts sur la page **Paramètres Marketing**, vous pouvez sélectionner <kbd>Entrée</kbd> pour insérer le numéro de contact suivant.
4. Renseignez les champs restants selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Pour créer un contact à partir d’un client, d’un fournisseur ou d’un compte bancaire

Si vous avez des clients, des fournisseurs, et des comptes bancaires pour lesquels vous souhaitez créer des fiches contact, vous pouvez utiliser les traitements par lots **Créer des contacts à partir** pour créer des contacts sur la base des données existantes. Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées ensuite avec les informations du client, du fournisseur ou du compte bancaire associé. En savoir plus, [Synchronisation des contacts avec les clients, les fournisseurs, les employés et les comptes bancaires](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Avant de créer des contacts basés sur des données existantes, vous devez spécifier un code relation d’affaires pour les clients, les fournisseurs ou les comptes bancaires sur l’organisateur **Interactions** de la page **Paramètres marketing**. En savoir plus sur [Configurer les contacts](marketing-setup-contacts.md).

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez l’un des choix suivants, selon l’élément à partir duquel vous souhaitez créer des contacts, puis sélectionnez le lien associé.
   * **Créer contacts à partir des clients**
   * **Créer des contacts à partir des fournisseurs**
   * **Créer des contacts à partir des comptes bancaires**
2. Sur la page de demande qui s’affiche, dans la section **Client**, **Fournisseur** ou **Compte bancaire**, définissez des filtres si vous souhaitez créer des contacts à partir de clients, de fournisseurs ou de comptes bancaires spécifiques.
3. Cliquez sur **OK** pour commencer à créer des contacts.

Les numéros de contact suivants de la souche de numéros sont affectés aux nouveaux contacts. La relation d’affaires spécifiée sur la page **Paramètres Marketing** est affectée aux contacts nouvellement créés.

> [!TIP]  
> Vous pouvez également effectuer cette opération inversement, à savoir en créant un client, un fournisseur, un employé ou un compte bancaire à partir d’un contact. Pour plus d’informations, reportez-vous à la section [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## Pour créer un client, un fournisseur, un employé ou un compte bancaire depuis un contact

Si vous avez un client, un fournisseur, un employé ou un compte bancaire pour la société pour laquelle vous souhaitez créer un contact, vous pouvez utiliser l’action **Créer en tant que**. Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées ensuite avec les informations du client, de l’employé du fournisseur ou du compte bancaire associé. En savoir plus, [Synchronisation des contacts avec les clients, les fournisseurs, les employés et les comptes bancaires](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Avant de créer des clients, fournisseurs, employés ou comptes bancaires à partir des contacts, vous devez spécifier un code relation d’affaires sur l’organisateur **Interactions** de la page **Paramètres marketing**. En savoir plus sur [Configurer les contacts](marketing-setup-contacts.md).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez le contact que vous souhaitez créer comme client, fournisseur, employé ou compte bancaire.
3. Sélectionnez l’action **Créer en tant que**, puis sélectionnez **Client**, **Fournisseur**, **Banque** ou **Employé**.
4. Cliquez sur **OK**.

Les informations du contact sont transférées depuis la fiche contact vers une nouvelle fiche compte bancaire, client, fournisseur ou employé. Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).

## Pour lier un contact à un client, un fournisseur, un employé un compte bancaire existant

Si vous disposez d’un contact et d’un client, d’un fournisseur, d’un employé ou d’un compte bancaire pour la même société, vous pouvez lier les deux entités afin de synchroniser les données.

1. Ouvrez le contact que vous souhaitez lier.
2. Sélectionnez l’action **Lier avec existant**, puis sélectionnez l’action **Client**, **Fournisseur**, **Banque** ou **Employé**.
3. Sur a page qui s’affiche, sélectionnez le client, le fournisseur, l’employé ou le compte bancaire à lier.
4. Dans le champ **Champs prioritaires**, spécifiez les champs à considérer comme prioritaires en cas de conflit d’informations entre les champs communs au contact et au client, au fournisseur à l’employé ou au compte bancaire. Par exemple, si le code vendeur est différent sur le contact et le client, vous pouvez décider de conserver celui de la fiche contact en sélectionnant **Contact**.
5. Cliquez sur **OK**.

## Pour supprimer un lien entre un contact et un client, un fournisseur, un employé un compte bancaire existant

Si vous avez lié par erreur un contact et un client, fournisseur, employé ou compte bancaire, supprimez le lien entre les entités afin que les données ne se synchronisent plus.

1. Ouvrez le contact qui a le mauvais lien.  
2. Choisissez l’action **Relations d’affaires**.  
3. Sur a page qui s’affiche, sélectionnez le client, le fournisseur, l’employé ou le compte bancaire à partir duquel supprimer le lien.  
4. Cliquez sur l’action **Supprimer**.  

> [!NOTE]  
> N’utilisez pas la fenêtre **Relations d’affaires** pour modifier les relations existantes. À la place, supprimez la relation et utilisez l’action **Lien avec existant**. Pour plus d’informations, consultez la section [Lier un contact à un client, fournisseur, employé ou compte bancaire existant](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Synchronisation des contacts avec les clients, les fournisseurs, les employés et les comptes bancaires

Si certains de vos contacts sont également des clients, des fournisseurs, des employés ou des comptes bancaires, vous pouvez synchroniser ensuite les données du contact et profiter des avantages suivants :

* Vous n’avez besoin de mettre à jour les données que dans une seule fiche. Par exemple, si vous modifiez le numéro de téléphone au niveau du contact, le numéro de téléphone est automatiquement mis à jour pour le client, le fournisseur, l’employé ou le compte bancaire.
* Si vous avez spécifié une souche de numéros pour les contacts, un contact est automatiquement créé pour le client, le fournisseur, l’employé ou le compte bancaire.
* Vous pouvez créer des devis, des commandes de vente, des demandes de prix et des commandes d’achat à partir du contact.
* Vous pouvez enregistrer vos interactions, telles que l’impression de commandes et de commandes cadres, la création de commandes pour le service des ventes, l’envoi d’e-mails, etc.
* Si vous supprimez un contact lié à un client, un fournisseur, un employé ou un compte bancaire, seule le contact est effacé. Le client, le fournisseur, l’employé ou le compte bancaire est conservé.
* Si vous supprimez un client, un fournisseur, un employé ou un compte bancaire lié à un contact, le contact est conservé.

> [!NOTE]  
> Certaines informations, par exemple concernant la facturation et la validation, ne sont pas disponibles pour les contacts. Lorsque vous créez des contacts en tant que clients, fournisseurs, employés ou comptes bancaires, vous souhaitez peut-être les ajouter manuellement.

La synchronisation des données entre les contacts et les clients, les fournisseurs, les employés ou les comptes bancaires est activée de trois manières :

* Lorsque vous créez des contacts à partir des clients, fournisseurs ou comptes bancaires. Pour plus d’informations, reportez-vous à la section [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Lorsque vous créez des clients, fournisseurs, employés ou comptes bancaires à partir des contacts. Pour plus d’informations, reportez-vous à la section [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Lorsque vous liez les contacts avec des clients, des fournisseurs, des employés ou des comptes bancaires existants à partir de la fiche contact. Pour plus d’informations, consultez la section [Lier un contact à un client, fournisseur, employé ou compte bancaire existant](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Pour voir à quel client, fournisseur, employé ou compte bancaire un contact est associé

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne pour un contact, choisissez l’action **Informations connexes**, puis choisissez l’action **Client/Fournisseur/Employé/Compte bancaire**.

## Voir aussi

[Gestion de contacts](marketing-contacts.md)  
[Paramétrage des contacts](marketing-setup-contacts.md)  
[Utilisez des cartes en ligne pour trouver des emplacements et des directions](across-online-maps.md)  
[Utiliser Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
