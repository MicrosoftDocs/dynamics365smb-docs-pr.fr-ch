---
title: Créer un client ou un fournisseur à partir d'un contact| Microsoft Docs
description: Vous pouvez enregistrer un contact existant comme client, fournisseur, ou compte bancaire à l'aide des données existantes et spécifier une relation d'affaires.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 5f5e690a8db82c2f95f190d5fac4b6430f900b57
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821520"
---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Créer un client, un fournisseur ou un compte bancaire à partir d'un contact
Vous pouvez enregistrer certains de vos contacts existants en tant que clients, fournisseurs ou comptes bancaires. Créer un client, un fournisseur ou un compte bancaire à partir d'un contact vous permet d'utiliser des données existantes. Lorsque vous créez un client, un fournisseur ou un compte bancaire de cette façon, celui-ci est synchronisé avec le contact. Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.

Avant de pouvoir enregistrer des contacts de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs et les comptes bancaires sur la page **Paramètres marketing**. Si vous devez enregistrer des contacts en tant que comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires sur la page **Paramètres comptabilité**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Pour créer un contact comme client, fournisseur ou compte bancaire
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez le contact que vous souhaitez créer comme client, fournisseur ou compte bancaire.
3. Sélectionnez l'action **Créer comme**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
4. Répondez par l'affirmative au message qui s'affiche.

Les informations du contact sont transférées depuis la fiche **Contact** vers la fiche **Compte bancaire**, **Client** ou **Fournisseur**. Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements.

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Création de personnes contact](marketing-create-contact-persons.md)  
[Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Associer des contacts avec des clients, des fournisseurs ou des comptes bancaires existants](marketing-how-link-contact.md)  
[Affecter des relations d'affaires à un contact](marketing-business-relations.md#AssignBusRelContact)  
[Utilisation de Business Central](ui-work-product.md)
