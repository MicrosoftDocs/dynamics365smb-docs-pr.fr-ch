---
title: Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires | Microsoft Docs
description: "Décrit la synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires dans Financials"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b28cd00659b077403e3174ac69c32ad5d9a8bf83
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires
Si certains de vos contacts sont également des clients, des fournisseurs ou des comptes bancaires, vous pouvez synchroniser les informations de contact avec le client, le fournisseur ou le compte bancaire correspondant. Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.  

Pour pouvoir synchroniser vos contacts avec des clients, des fournisseurs ou des comptes bancaires, vous devez spécifier un code relation d'affaires pour ces derniers dans la fenêtre **Paramètres marketing**. Pour plus d'informations, voir [Paramétrage de la Gestion des relations](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Différentes manières de synchroniser les contacts avec les clients, les fournisseurs et les comptes bancaires
Pour synchroniser vos contacts avec des clients, des fournisseurs ou des comptes bancaires, choisissez l'une des trois méthodes suivantes :

* Liaison de contacts avec des clients, des fournisseurs ou des comptes bancaires existants à partir de la fiche contact. Pour plus d'informations, reportez-vous à [Procédure : liaison de contacts avec des clients, des fournisseurs et des comptes bancaires](marketing-how-link-contact.md).
* Créez des clients, des fournisseurs ou des comptes bancaires à partir du contact. Pour plus d'informations, reportez-vous à [Créer un client, un fournisseur ou un compte bancaire à partir d'un contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Créez des contacts à partir de clients, fournisseurs ou comptes bancaires. Pour plus d'informations, voir [Créer un contact société à partir d'un client, d'un fournisseur ou d'un compte bancaire](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Conséquences de la synchronisation
Lorsque le contact est synchronisé avec le client, le fournisseur ou le compte bancaire :

* Vous n'avez besoin de mettre à jour les données que dans une seule fiche. Par exemple, si vous modifiez le numéro de téléphone au niveau du contact, le numéro de téléphone est automatiquement mis à jour avec la même modification au niveau du client, du fournisseur ou du compte bancaire.
* Si vous avez spécifié une souche de numéros pour les contacts, une fiche contact est automatiquement créée pour le client, le fournisseur ou le compte bancaire lorsque vous créez une fiche client, fournisseur ou compte bancaire.
* Vous pouvez créer des devis, des commandes de vente, des demandes de prix et des commandes d'achat à partir du contact.
* Vous pouvez enregistrer vos interactions lorsque vous effectuez des opérations telles que l'impression de commandes et de commandes ouvertes, la création de commandes pour le service des ventes, l'envoi d'e-mails, etc.
* Si vous supprimez un contact lié à un client, un fournisseur ou un compte bancaire, seule le contact est effacé. Le client, le fournisseur ou le bancaire est conservé.
* Si vous supprimez un client, un fournisseur ou un compte bancaire lié à un contact, le contact est conservé.

**Remarque** : certaines informations, par exemple concernant la facturation et la validation, n'apparaissent pas sur la fiche contact. Par conséquent, vous pouvez les ajouter manuellement sur la fiche client, la fiche fournisseur ou la fiche compte bancaire lorsque vous créez des contacts en tant que clients, fournisseurs ou comptes bancaires.

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

