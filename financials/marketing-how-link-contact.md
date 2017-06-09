---
title: Liaison de contacts avec des clients, des fournisseurs et des comptes bancaires | Microsoft Docs
description: "Décrit comment lier des contacts avec des clients, des fournisseurs et des comptes bancaires dans Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 44dff830f293f4a33e6358d816635aa67e8a8de6
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-link-contacts-with-customers-vendors-and-bank-accounts"></a>Procédure : liaison de contacts avec des clients, des fournisseurs et des comptes bancaires
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

