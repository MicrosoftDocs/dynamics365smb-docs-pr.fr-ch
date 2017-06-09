---
title: "Configuration des secteurs d&quot;activité pour des sociétés contact | Microsoft Docs"
description: "Décrit l&quot;utilisation des secteurs d&quot;activité avec les contacts dans Financials"
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
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Configuration des secteurs d'activité pour des sociétés contact
Les secteurs d'activité vous permettent d'indiquer le type de secteur auquel vos contacts appartiennent, par exemple la grande distribution et l'industrie automobile.

L'utilisation secteurs d'activité sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code secteur d'activité. Vous ne devez effectuer cette étape qu'une seule fois pour chaque secteur d'activité. Une fois que vous disposez d'un code secteur d'activité, vous pouvez commencer à affecter le code aux sociétés contact.

**Remarque** : si vous prévoyez de synchroniser vos contacts avec des fournisseurs, des clients ou des comptes bancaires dans d'autres parties de l'application, vous pouvez configurer pour eux une relation d'affaires.

## <a name="to-define-an-industry-group-code"></a>Pour définir un code secteur d'activité
Le code secteur d'activité définit le type ou la catégorie du groupe, par exemple PUB pour la publicité, ou PRESSE pour la télévision et la radio. Vous pouvez disposer de plusieurs codes secteur d'activité. Pour définir les secteurs d'activité, utilisez la fenêtre **Secteurs d'activité**.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Secteurs d'activité**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

## <a name="AssignIndustryGroupContact"></a> Pour affecter des secteurs d'activité à un contact
Vous ne pouvez pas affecter de secteurs d'activité à une personne contact, mais uniquement à des sociétés.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Secteurs d'activité**. La fenêtre **Secteur d'activité contact** s'affiche.
3. Dans le champ **Code secteurs d'activité**, sélectionnez le secteur d'activité à affecter.

Répétez ces étapes pour chaque secteur d'activité à affecter. Vous pouvez également affecter des secteurs d'activité à partir de la liste des contacts en suivant la même procédure.

Le nombre de secteurs d'activité que vous avez affectés au contact s'affiche dans le champ **Nbre secteurs d'activité** de la section **Segmentation** de la fenêtre **Contact**.

Une fois que vous avez affecté des secteurs d'activité à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Procédure : ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

