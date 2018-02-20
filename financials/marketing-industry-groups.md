---
title: "Paramétrer des secteurs d'activité pour des sociétés contact| Microsoft Docs"
description: "Décrit comment définir un secteur d'activité et l'affecter à une société contact, par exemple, le marché de détail ou l'industrie automobile."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c7a8549a5c6528cafb5e2959a3391fb323fe92ca
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a>Configurer des secteurs d'activité pour des sociétés contact
Les secteurs d'activité vous permettent d'indiquer le type de secteur auquel vos contacts appartiennent, par exemple la grande distribution et l'industrie automobile.

L'utilisation secteurs d'activité sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code secteur d'activité. Vous ne devez effectuer cette étape qu'une seule fois pour chaque secteur d'activité. Une fois que vous disposez d'un code secteur d'activité, vous pouvez commencer à affecter le code aux sociétés contact.

> [!NOTE]  
>   Si vous souhaitez synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer une relation d'affaires.

## <a name="to-define-an-industry-group-code"></a>Pour définir un code secteur d'activité
Le code secteur d'activité définit le type ou la catégorie du groupe, par exemple PUB pour la publicité, ou PRESSE pour la télévision et la radio. Vous pouvez disposer de plusieurs codes secteur d'activité. Pour définir les secteurs d'activité, utilisez la fenêtre **Secteurs d'activité**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Secteurs d'activité**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

## <a name="AssignIndustryGroupContact"></a> Pour affecter des secteurs d'activité à un contact
Vous ne pouvez pas affecter de secteurs d'activité à une personne contact, mais uniquement à des sociétés.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Secteurs d'activité**. La fenêtre **Secteur d'activité contact** s'affiche.
3. Dans le champ **Code secteurs d'activité**, sélectionnez le secteur d'activité à affecter.

Répétez ces étapes pour chaque secteur d'activité à affecter. Vous pouvez également affecter des secteurs d'activité à partir de la liste des contacts en suivant la même procédure.

Le nombre de secteurs d'activité que vous avez affectés au contact s'affiche dans le champ **Nbre secteurs d'activité** de la section **Segmentation** de la fenêtre **Contact**.

Une fois que vous avez affecté des secteurs d'activité à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

