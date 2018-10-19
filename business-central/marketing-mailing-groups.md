---
title: Configurer des groupes de distribution pour des contacts| Microsoft Docs
description: "Vous pouvez utiliser les groupes distribution pour identifier les groupes contacts qui doivent recevoir les mêmes informations, par exemple, pour une campagne marketing ou une promotion."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a7b9c39b1f213bf2b09ee24e3e6172df027e042c
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Configurer des groupes de distribution pour les contacts.
Les groupes distribution vous permettent d'identifier les groupes de contacts qui doivent recevoir les mêmes informations. Par exemple, vous pouvez configurer un groupe de distribution pour les contacts auxquels vous souhaitez envoyer un avis de déménagement, ou un autre groupe auquel envoyer des cadeaux pour les fêtes de fin d'année.

L'utilisation des groupes de distribution sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code groupe de distribution. Vous ne devez effectuer cette étape qu'une seule fois pour chaque groupe de distribution. Une fois que vous disposez d'un code groupe de distribution, vous pouvez commencer à affecter ce code aux sociétés contact.

## <a name="to-define-mailing-group-codes"></a>Pour définir des codes groupe de distribution
Le code groupe de distribution définit le type ou la catégorie du groupe, telles que DÉMÉNAGEMENT pour un déménagement des bureaux, ou CADEAU pour le cadeau de fêtes de fin d'année. Vous pouvez disposer de plusieurs codes secteur d'activité. Pour définir les groupes de distribution, utilisez la fenêtre **Groupes de distribution**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes de distribution**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

## <a name="AssignMailGroupContact"></a> Pour affecter des groupes de distribution à un contact
1. Ouvrez le contact.
2. Sélectionnez l'action **Groupes de distribution**. La fenêtre **Groupes distribution contact** s'affiche.
3. Dans le champ **Code groupes de distribution**, sélectionnez le groupe de distribution à affecter.

Répétez ces étapes pour chaque groupe de distribution à affecter. Vous pouvez également affecter des groupes de distribution à partir de la liste des contacts en suivant la même procédure.

Le nombre de groupes de distribution affectés au contact s'affiche dans le champ **Nbre groupes de distribution** de la section **Segmentation** de la fenêtre **Contact**.

Une fois que vous avez affecté des groupes de distribution à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Création de personnes contact](marketing-create-contact-persons.md)  
[Utilisation de Business Central](ui-work-product.md)

