---
title: Liaison de contacts avec des clients et des fournisseurs| Microsoft Docs
description: "Décrit comment lier un contact avec un client, un fournisseur, ou un compte bancaire de la même société, afin de pouvoir synchroniser les données communes."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2613e32873c91fe24c4734456338bb1f7e18849d
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="link-contacts-with-customers-vendors-and-bank-accounts"></a>Liaison de contacts avec des clients, des fournisseurs et des comptes bancaires
Si vous disposez d'un contact et d'un client, d'un fournisseur ou d'un compte bancaire pour la même société, vous pouvez lier les deux entités. Lier les deux entités vous permet de synchroniser les données communes afin qu'elles soient identiques aux deux emplacements.

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Lier un contact à un client, un fournisseur ou un compte bancaire existant
1. Ouvrez le contact que vous souhaitez lier.
2. Sélectionnez l'action **Lier avec existant**, puis sélectionnez **Client**, **Fournisseur** ou **Banque**.
3. Sélectionnez le client, le fournisseur ou le compte bancaire à lier.

   Dans le champ **Champs prioritaires**, spécifiez les champs à considérer comme prioritaires en cas de conflit d'informations entre les champs communs au contact et au client, au fournisseur ou au compte. Par exemple, si le code vendeur est différent entre le contact et le client, vous pouvez décider d'utiliser les données du contact en sélectionnant **Contact**.

## <a name="see-also"></a>Voir aussi
[Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Création et gestion des contacts](marketing-contacts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

