---
title: "Définir les codes des relations d'affaires dans les contacts| Microsoft Docs"
description: "Utilisez les relations d'affaires dans Finance and Operations, Business edition pour vous aider avec le marketing et désigner les rapports établis avec vos prospects, clients, notamment les banques ou les prestataires de services."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a72563f5057a1f9136a2d2b3aced6f028dc24051
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Configuration des relations d'affaires sur des sociétés contact
Les relations d'affaires vous permettent d'indiquer les rapports établis avec vos contacts, tels que les prospects, les banques, les consultants, les prestataires de services, et ainsi de suite.

L'utilisation des relations d'affaires sur les contacts processus en deux étapes. Tout d'abord, vous définissez le code relation d'affaires. Vous ne devez effectuer cette étape qu'une seule fois pour chaque relation d'affaires. Une fois que vous disposez d'un code relation d'affaires, vous pouvez commencer à affecter le code aux sociétés contact.

> [!NOTE]  
>   Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.

## <a name="to-define-a-business-relation-code"></a>Pour définir un code relation d'affaires
Le code relation d'affaires définit une catégorie ou un type de relation d'affaires, telles que BANQUE ou Avocat. Vous pouvez disposer de plusieurs codes relation d'affaires. Pour définir la relation d'affaires, vous utilisez la fenêtre **Relations d'affaires**.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relations d'affaires**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

## <a name="AssignBusRelContact"></a> Pour affecter des relations d'affaires à un contact
Vous ne pouvez pas affecter de relations d'affaires à un individu, mais uniquement à des sociétés.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Relations d'affaires**.

    La fenêtre **Relations d'affaires contact** s'ouvre.
3. Dans le champ **Code relation d'affaires**, sélectionnez la relation d'affaires à affecter.

Répétez ces étapes pour chaque relation d'affaires à affecter. Vous pouvez également affecter des relations d'affaires à partir de la liste des contacts en suivant la même procédure.

Le nombre de relations d'affaires que vous avez affectées au contact s'affiche dans le champ **Nbre relations d'affaires** de la section **Segmentation** de la fenêtre **Contact**.

Une fois que vous avez affecté des relations d'affaires à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

