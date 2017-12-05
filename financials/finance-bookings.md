---
title: "Facturer vos réservations dans Dynamics 365 | Microsoft Docs"
description: "Apprenez comment vous pouvez effectuer des facturations en vrac à partir de Microsoft Bookings dans Dynamics 365 Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 154a4719cdd0e28280c5b0a5de85479beb0b9262
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a>Facturation en vrac pour Microsoft Bookings dans [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si votre société utilise l'application Bookings d'Office 365, vous pouvez effectuer la facturation en vrac des rendez-vous. La page **Réservations non facturées** de [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit une liste des réservations effectuées par la société. Cette page vous permet de rapidement sélectionner les rendez-vous à facturer et de créer des factures provisoires pour les services fournis.  

## <a name="connect-to-bookings"></a>Connexion à Réservations
Pour connecter votre [!INCLUDE[d365fin](includes/d365fin_md.md)] à Réservations, vous devez indiquer votre société Réservations, quoi synchroniser avec Réservations, la fréquence de la synchronisation et les modèles à utiliser. Vous définissez ces informations sur la page **Paramètres synch. réservations**, que vous pouvez lancer depuis la page **Configuration de la synchronisation Exchange**, que vous pouvez rechercher à l'aide de [Rechercher](ui-search.md).  

Par exemple, si vous souhaitez synchroniser des clients entre Réservations et [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez spécifier le modèle par défaut à utiliser pour ajouter de nouveaux clients à [!INCLUDE[d365fin](includes/d365fin_md.md)] selon les clients de votre société de Réservations.  

## <a name="invoice-appointments"></a>Facturer les rendez-vous
Lorsqu'il est temps d'envoyer les factures pour les réservations terminées, vous consultez la page **Réservations non facturées**. Selon le nombre de fois où les informations sont synchronisées, la liste est long ou courte. Vous pouvez créer des factures pour toutes les réservations de la liste ou une réservation à la fois. Vous pouvez sélectionner une ou plusieurs écritures dans la liste et facturer celles-ci uniquement.  

Le prise en charge de la facturation des rendez-vous dans Réservations est plus simple que le flux de travail plus complet consistant à utiliser des devis, des commandes vente, et des factures vente. Pour plus d'informations, reportez-vous à [Procédure : facturer des ventes](sales-how-invoice-sales.md). Vous pouvez choisir de vendre vos services à l'aide de [!INCLUDE[d365fin](includes/d365fin_md.md)] ou d'utiliser Réservations, selon les besoins de votre activité.  

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Procédure : facturer des ventes](sales-how-invoice-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  

