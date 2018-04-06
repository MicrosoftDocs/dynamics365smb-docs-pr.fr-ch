---
title: "Créer un client ou un fournisseur à partir d'un contact| Microsoft Docs"
description: "Vous pouvez enregistrer un contact existant comme client, fournisseur, ou compte bancaire à l'aide des données existantes et spécifier une relation d'affaires."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e1f1d9e89d4164f36fb90c027cd636da67bc40d9
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Créer un client, un fournisseur ou un compte bancaire à partir d'un contact
Vous pouvez enregistrer certains de vos contacts existants en tant que clients, fournisseurs ou comptes bancaires. Créer un client, un fournisseur ou un compte bancaire à partir d'un contact vous permet d'utiliser des données existantes. Lorsque vous créez un client, un fournisseur ou un compte bancaire de cette façon, celui-ci est synchronisé avec le contact. Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.

Avant de pouvoir enregistrer des contacts de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs et les comptes bancaires dans la fenêtre **Paramètres marketing**. Si vous devez enregistrer des contacts en tant que comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires dans la fenêtre **Paramètres comptabilité**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Pour créer un contact comme client, fournisseur ou compte bancaire
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Contacts**, puis sélectionnez le lien connexe.
2. Sélectionnez le contact que vous souhaitez créer comme client, fournisseur ou compte bancaire.
3. Sélectionnez l'action **Créer comme**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
4. Répondez par l'affirmative au message qui s'affiche.

Les informations du contact sont transférées depuis la fiche **Contact** vers la fiche **Compte bancaire**, **Client** ou **Fournisseur**. Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements.

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Création de personnes contact](marketing-create-contact-persons.md)  
[Paramétrage de la Gestion des relations](marketing-setup-marketing.md)  
[Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Associer des contacts avec des clients, des fournisseurs ou des comptes bancaires existants](marketing-how-link-contact.md)  
[Affecter des relations d'affaires à un contact](marketing-business-relations.md#AssignBusRelContact)  
[Utilisation de Business Central](ui-work-product.md)

