---
title: "Facturer vos réservations dans Business\_Central"
description: "Cette rubrique explique comment effectuer une facturation groupée à partir de Microsoft Bookings dans Business\_Central."
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: edupont
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-includeprodshortincludesprodshortmd" />Facturation en vrac pour Microsoft Bookings dans [!INCLUDE[prod_short](includes/prod_short.md)]

Si votre société utilise l’application Bookings de Microsoft 365, vous pouvez effectuer la facturation en vrac des rendez-vous. La page **Réservations non facturées** de [!INCLUDE[prod_short](includes/prod_short.md)] fournit une liste des réservations effectuées par la société. Cette page vous permet de rapidement sélectionner les rendez-vous à facturer et de créer des factures provisoires pour les services fournis.  

## <a name="connect-to-bookings" />Connexion à Réservations

Pour connecter votre [!INCLUDE[prod_short](includes/prod_short.md)] à Réservations, vous devez indiquer votre société Réservations, quoi synchroniser avec Réservations, la fréquence de la synchronisation et les modèles à utiliser. Vous définissez ces informations sur la page **Paramètres synch. réservations**, que vous pouvez lancer depuis la page **Configuration de la synchronisation Exchange**, que vous pouvez rechercher à l’aide de [Rechercher](ui-search.md).  

Par exemple, si vous souhaitez synchroniser des clients entre Réservations et [!INCLUDE[prod_short](includes/prod_short.md)], vous devez spécifier le modèle par défaut à utiliser pour ajouter de nouveaux clients à [!INCLUDE[prod_short](includes/prod_short.md)] selon les clients de votre société de Réservations.  

> [!NOTE]
> L’applications Bookings est conçue pour réserver des rendez-vous pour des clients individuels, plutôt que des sociétés. La synchronisation avec [!INCLUDE[prod_short](includes/prod_short.md)], par conséquent, synchronise uniquement les contacts du client de type *Personne*. Un adresse électronique est également nécessaire pour synchroniser le contact.  

De même, si vous souhaitez synchroniser des articles service entre Bookings et [!INCLUDE[prod_short](includes/prod_short.md)], vous devez spécifier le modèle par défaut à utiliser pour ajouter de nouveaux articles service à [!INCLUDE[prod_short](includes/prod_short.md)] selon les services de notre société Bookings.  

> [!NOTE]
> Seuls les articles de type *Service* se synchronisent entre Bookings et [!INCLUDE[prod_short](includes/prod_short.md)]. Le modèle que vous configurez sur la page **Modèles de configuration** pour pouvoir l’utiliser pour la synchronisation d’article doit définir le type comme *Service*.

## <a name="invoice-appointments" />Facturer les rendez-vous

Lorsqu’il est temps d’envoyer les factures pour les réservations terminées, vous consultez la page **Réservations non facturées**. Selon le nombre de fois où les informations sont synchronisées, la liste est long ou courte. Vous pouvez créer des factures pour toutes les réservations de la liste ou une réservation à la fois. Vous pouvez sélectionner une ou plusieurs écritures dans la liste et facturer celles-ci uniquement.  

Le prise en charge de la facturation des rendez-vous dans Réservations est plus simple que le flux de travail plus complet consistant à utiliser des devis, des commandes vente, et des factures vente. Pour plus d’informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md). Vous pouvez choisir de vendre vos services à l’aide de [!INCLUDE[prod_short](includes/prod_short.md)] ou d’utiliser Réservations, selon les besoins de votre activité.  

> [!NOTE]
> En mai 2022, nous avons découvert un problème d’intégration avec Réservations. Actuellement, la synchronisation des réservations vers [!INCLUDE [prod_short](includes/prod_short.md)] vous oblige à associer manuellement les factures aux clients dans [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="see-also" />Voir aussi

[Finances](finance.md)  
[Facturer des ventes](sales-how-invoice-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
