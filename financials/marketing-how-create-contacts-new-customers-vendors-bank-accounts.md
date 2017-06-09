---
title: "Créer un client, un fournisseur ou un compte bancaire à partir d&quot;un contact | Microsoft Docs"
description: "Décrit comment créer un client, un fournisseur ou un compte bancaire à partir d&quot;un contact dans Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6ecbc24e447917e6316b0579fa8c3ee046e73915
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Créer un client, un fournisseur ou un compte bancaire à partir d'un contact
Vous pouvez enregistrer certains de vos contacts existants en tant que clients, fournisseurs ou comptes bancaires. Créer un client, un fournisseur ou un compte bancaire à partir d'un contact vous permet d'utiliser des données existantes. Lorsque vous créez un client, un fournisseur ou un compte bancaire de cette façon, celui-ci est synchronisé avec le contact. Avec la synchronisation les informations communes entre les contacts et les clients, les fournisseurs ou les comptes bancaires sont identiques.

Avant de pouvoir enregistrer des contacts de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs et les comptes bancaires dans la fenêtre **Paramètres marketing**. Si vous devez enregistrer des contacts en tant que comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires dans la fenêtre **Paramètres comptabilité**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Pour créer un contact comme client, fournisseur ou compte bancaire
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez le contact que vous souhaitez créer comme client, fournisseur ou compte bancaire.
3. Sélectionnez l'action **Créer comme**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
4. Répondez par l'affirmative au message qui s'affiche.

Les informations du contact sont transférées depuis la fiche **Contact** vers la fiche **Compte bancaire**, **Client** ou **Fournisseur**. Vous pouvez ajouter des informations spécifiques à chacune des fiches, telles que des informations sur les factures ou les paiements.

## <a name="see-also"></a>Voir aussi
[Procédure : créer des sociétés contact](marketing-create-contact-companies.md)  
[Procédure : créer des personnes contact](marketing-create-contact-persons.md)  
[Paramétrage de la Gestion des relations](marketing-setup-marketing.md)  
[Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Procédure : associer des contacts avec des clients, des fournisseurs ou des comptes bancaires existants](marketing-how-link-contact.md)  
[Affecter des relations d'affaires à un contact](marketing-business-relations.md#AssignBusRelContact)  
[Utilisation de Financials](ui-work-product.md)

