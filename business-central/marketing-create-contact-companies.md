---
title: Créer des sociétés contact| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 09/06/2019
ms.author: sgroespe
ms.openlocfilehash: 5ec6a7580cd4211b33d276f5523bfcf34b91ad59
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985853"
---
# <a name="create-contacts"></a>Créez des contacts
Vous rencontrez régulièrement des personnes d'autres sociétés, ce qui peut générer de nouvelles relations commerciales, comme une relation client. À la création d'un tel contact, il convient d'enregistrer le plus d'informations possible sur une fiche contact afin que la communication puisse se poursuivre.

Vous pouvez créer le contact de type **Entreprise**, par exemple, si la relation n’est pas une personne physique, mais une entité, telle qu’un contractant ou une banque. Vous pouvez aussi créer le contact de type **Personne**. La fonctionnalité est plus ou moins la même pour les deux types et les deux peuvent être modifiés à mesure que la relation évolue.

Lorsqu'une carte de contact est convertie en fiche client, par exemple, la personne de contact ou l'entreprise de contact devient le nom du client. La fiche contact reste en mémoire et les données sur les deux cartes seront synchronisées à l'avenir si vous les liez.

## <a name="person-or-company"></a>Personne ou société
Vous pouvez décider de configurer un contact comme une personne ou société, généralement si vous connaissez le nom du contact au moment de la création. Vous y parvenez en complétant le champ **Type** sur la page **Fiche contact**. Vous pouvez également conserver les fiches contact pour une société et une ou plusieurs personnes travaillant au sein de la société. Cela se produit automatiquement lorsque vous complétez le champ **Nom de la société** sur une fiche contact de type **Personne**.

La fonctionnalité est la même pour les deux types, hormis le fait que les options pour des informations supplémentaires changent selon le type. Par exemple, vous pouvez affecter des responsabilités uniquement à une personne et un groupe d'activité à une société. Cela est indiqué dans l'interface utilisateur en faisant apparaître en gris les champs et les actions qui ne s'appliquent pas. Vous pouvez modifier la valeur du champ **Type** ultérieurement, ou vous pouvez utiliser les champs du raccourci **Héritage** sur la page **Paramètres marketing** pour contrôler les données partagées entre une personne et la société associée. Pour plus d'informations, reportez-vous à la rubrique [Paramétrage des contacts](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Pour créer un contact manuellement
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **N°**, saisissez le numéro du contact.

    Si vous avez configuré une souche de numéros pour les contacts sur la page **Paramètres Marketing**, appuyez sur la touche Entrée pour insérer le numéro de contact suivant.  
5. Renseignez les champs restants selon vos besoins. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Pour créer un contact à partir d'un client, d'un fournisseur ou d'un compte bancaire
Si vous avez des clients, des fournisseurs, et des comptes bancaires pour lesquels vous souhaitez créer des fiches contact, vous pouvez utiliser les traitements par lots **Créer des contacts à partir** pour créer des contacts sur la base des données existantes. Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées ensuite avec les informations du client, du fournisseur ou du compte bancaire associé. Pour plus d'informations, reportez-vous à [Procédure de synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Avant de créer des contacts basés sur des données existantes, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs ou les comptes bancaires sur l'organisateur **Interactions** de la page **Paramètres marketing**. Pour plus d'informations, voir [Configuration de contacts](marketing-setup-contacts.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez une des actions suivantes, selon l'élément à partir duquel vous souhaitez créer des contacts, puis sélectionnez le lien associé.
   * **Créer des contacts à partir des clients**
   * **Créer des contacts à partir des fournisseurs**
   * **Créer des contacts à partir des comptes bancaires**
2. Sur la page de demande qui s'affiche, dans la section **Client**, **Fournisseur** ou **Compte bancaire**, définissez des filtres si vous souhaitez créer des contacts à partir de clients, de fournisseurs ou de comptes bancaires spécifiques.
3. Pour démarrer la création de contacts, cliquez sur le bouton **OK**.

Les numéros de contact suivants de la souche de numéros sont affectés aux nouveaux contacts. La relation d'affaires spécifiée sur la page **Paramètres Marketing** est affectée aux contacts nouvellement créés.

> [!TIP]  
> Vous pouvez également effectuer cette opération inversement, à savoir en créant un client, un fournisseur, ou un compte bancaire à partir d'un contact. Pour plus d'informations, reportez-vous à [Pour créer un contact comme client, fournisseur ou compte bancaire](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Pour créer un client, un fournisseur ou un compte bancaire depuis un contact
Si vous avez un client, un fournisseur, ou un compte bancaire pour la société pour laquelle vous souhaitez créer un contact, vous pouvez utiliser la fonction **Créer comme**. Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées ensuite avec les informations du client, du fournisseur ou du compte bancaire associé. Pour plus d'informations, reportez-vous à [Procédure de synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Avant de créer des contacts basés sur des clients, des fournisseurs ou des comptes bancaires à partir de contacts, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs ou les comptes bancaires sur l'organisateur **Interactions** de la page **Paramètres marketing**. Pour plus d'informations, reportez-vous à [Paramétrage des contacts](marketing-setup-contacts.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez le contact que vous souhaitez créer comme client, fournisseur ou compte bancaire.
3. Sélectionnez l'action **Créer comme**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
4. Choisissez le bouton **OK**.

Les informations du contact sont transférées depuis la fiche contact vers une nouvelle fiche compte bancaire, client ou fournisseur. Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements. Pour plus d'informations, reportez vous, par exemple, à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Pour lier un contact à un client, un fournisseur ou un compte bancaire existant
Si vous disposez d'un contact et d'un client, d'un fournisseur ou d'un compte bancaire pour la même société, vous pouvez lier les deux entités afin que les données communes soient synchronisées.

1. Ouvrez le contact que vous souhaitez lier.
2. Sélectionnez l'action **Lier avec existant**, puis sélectionnez l'action **Client**, **Fournisseur** ou **Banque**.
3. Sur a page qui s'affiche, sélectionnez le client, le fournisseur ou le compte bancaire à lier.
4. Dans le champ **Champs prioritaires**, spécifiez les champs à considérer comme prioritaires en cas de conflit d'informations entre les champs communs au contact et au client, au fournisseur ou au compte. Par exemple, si le code vendeur est différent sur la fiche contact et la fiche client, vous pouvez décider de conserver celui de la fiche contact en sélectionnant **Contact**.
5. Cliquez sur le bouton **OK**.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires
Si certains de vos contacts sont également des clients, des fournisseurs ou des comptes bancaires, vous pouvez synchroniser les informations de contact avec le client, le fournisseur ou le compte bancaire correspondant.

Lorsqu'un contact est synchronisé sur un client, un fournisseur ou un compte bancaire de cette façon, les avantages suivants s'offrent à vous :

* Vous n'avez besoin de mettre à jour les données que dans une seule fiche. Par exemple, si vous modifiez le numéro de téléphone au niveau du contact, le numéro de téléphone est automatiquement mis à jour avec la même modification au niveau du client, du fournisseur ou du compte bancaire.
* Si vous avez spécifié une souche de numéros pour les contacts, une fiche contact est automatiquement créée pour le client, le fournisseur ou le compte bancaire lorsque vous créez une fiche client, fournisseur ou compte bancaire.
* Vous pouvez créer des devis, des commandes de vente, des demandes de prix et des commandes d'achat à partir du contact.
* Vous pouvez enregistrer vos interactions lorsque vous effectuez des opérations telles que l'impression de commandes et de commandes ouvertes, la création de commandes pour le service des ventes, l'envoi d'e-mails, etc.
* Si vous supprimez un contact lié à un client, un fournisseur ou un compte bancaire, seule le contact est effacé. Le client, le fournisseur ou le bancaire est conservé.
* Si vous supprimez un client, un fournisseur ou un compte bancaire lié à un contact, le contact est conservé.

> [!NOTE]  
> Certaines informations, par exemple concernant la facturation et la validation, n'apparaissent pas sur la fiche contact. Par conséquent, vous pouvez les ajouter manuellement sur la fiche client, la fiche fournisseur ou la fiche compte bancaire lorsque vous créez des contacts en tant que clients, fournisseurs ou comptes bancaires.

La synchronisation des données communes entre les contacts et clients, les fournisseurs, ou les comptes bancaires associés est activée de trois manières :

* Lorsque vous créez des contacts à partir des clients, fournisseurs ou comptes bancaires. Voir [Pour créer un contact à partir d'un client, d'un fournisseur ou d'un compte bancaire](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Lorsque vous créez des clients, fournisseurs ou comptes bancaires à partir de contacts. Voir [Pour créer un client, un fournisseur ou un compte bancaire depuis un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Lorsque vous liez les contacts avec des clients, des fournisseurs ou des comptes bancaires existants à partir de la fiche contact. Voir [Pour lier un contact à un client, un fournisseur ou un compte bancaire existant](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Pour voir à quel client, fournisseur ou compte bancaire un contact est associé
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez la ligne pour un contact, choisissez l'action **Informations connexes**, puis choisissez l'action **Client/Fournisseur/Compte bancaire**.

La page de la fiche associée s'ouvre.

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Paramétrage des contacts](marketing-setup-contacts.md)  
[Utilisation de Business Central](ui-work-product.md)
