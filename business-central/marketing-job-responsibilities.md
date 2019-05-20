---
title: Configuration des responsabilités pour des contacts| Microsoft Docs
description: Vous pouvez définir un code de responsabilité et l'affecter à un contact pour indiquer les tâches dont votre contact est en charge dans sa société, par exemple, l'informatique ou la production.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: d9c6b19d49ea9423762b0b4b5cf61eae0e325034
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242253"
---
# <a name="set-up-job-responsibilities-for-contact-persons"></a>Configurer les responsabilités pour les personnes contact
Vous pouvez ajouter des informations relatives aux responsabilités des personnes contact afin d'indiquer les tâches dont une personne contact est responsable au sein de sa société, par exemple, l'informatique, la gestion ou la production. Vous pouvez utiliser ces informations lors de la saisie de données sur vos contacts.

L'utilisation des responsabilités sur les contacts est un processus en deux étapes. Tout d'abord, vous définissez le code responsabilité. Vous ne devez effectuer cette étape qu'une seule fois pour chaque responsabilité. Une fois que vous disposez d'un code responsabilité, vous pouvez commencer à affecter ce code aux personnes contact.

## <a name="to-define-a-job-responsibility-code"></a>Pour définir un code de responsabilité
Le code responsabilité définit le type ou la catégorie du projet, par exemple MARKETING ou ACHAT. Vous pouvez disposer de plusieurs codes responsabilité. La page **Responsabilités** vous permet de définir la responsabilité.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Responsabilités**, puis choisissez le lien associé.
2. Sélectionnez l'action **Nouveau**, et entrez un code et une désignation. Vous pouvez saisir pour le code un maximum de 11 caractères, et toute combinaison de chiffres et des lettres.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Pour affecter des responsabilités à vos contacts
Vous ne pouvez pas affecter de responsabilités aux sociétés contact.

1. Ouvrez la fiche de la personne contact.
2. Sélectionnez l'action **Personne**, puis sélectionnez l'action **Responsabilités**. La page **Responsabilités contact** s'affiche.
3. Dans le champ **Code responsabilité**, sélectionnez la responsabilité que vous souhaitez affecter.

Répétez ces étapes pour chaque responsabilité à affecter. Vous pouvez également affecter des responsabilités à partir de la liste des contacts en suivant la même procédure.

Le nombre de responsabilités affectées au contact s'affiche dans le champ **Nbre responsabilités** de la section **Segmentation** de la page **Contact**.

Une fois que vous avez affecté des responsabilités à vos contacts, vous pouvez utiliser ces informations pour sélectionner des contacts pour vos segments. Pour plus d'informations, reportez-vous à [Ajouter des contacts à des segments](marketing-add-contact-segment.md).

## <a name="see-also"></a>Voir aussi
[Création de contacts](marketing-create-contact-companies.md)  
[Utilisation de Business Central](ui-work-product.md)
