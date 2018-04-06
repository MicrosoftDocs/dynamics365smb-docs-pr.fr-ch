---
title: "Configurer des recherches Web pour des sociétés contact| Microsoft Docs"
description: "Vous pouvez définir des sources Internet ou Web et les affecter à une société contact pour identifier la manière dont vous souhaitez rechercher des informations sur vos contacts."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b80edfbbad575cfcaa15b2c1b79a4feacb077371
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a>Configuration de recherches Web pour des sociétés contact
Vous pouvez utiliser les recherches Web avec vos sociétés contact afin d'identifier, par exemple, des moteurs de recherche et des sites Web que vous souhaitez utiliser pour rechercher des informations relatives aux contacts. Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.

L'utilisation des recherches Web au niveau des contacts est un processus en deux étapes. Tout d'abord, vous définissez le code recherche Web. Vous ne devez effectuer cette étape qu'une seule fois pour chaque recherche Web. Une fois que vous disposez d'un code recherche Web, vous pouvez commencer à affecter ce code aux personnes contact.

## <a name="to-define-a-web-source-code"></a>Pour définir un code recherche Web
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Recherche Web**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs **Code**, **Désignation** et **URL**.

    Tapez %1 dans le champ **URL** pour insérer un espace réservé correspondant au mot recherché dans l'URL. Lorsque vous lancez la recherche Web à partir d'un contact, le %1 est automatiquement remplacé par le mot recherché (par exemple le nom de la société) que vous avez saisi dans la fenêtre **Recherche contacts Web**.

Répétez ces étapes pour chaque recherche Web à configurer.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Pour affecter une recherche Web à une société contact
Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Recherche Web**. La fenêtre **Recherche contact Web** s'affiche.
3. Dans le champ **Code recherche web**, sélectionnez la recherche Web à affecter.
4. Dans le champ **Mot recherché**, saisissez le mot recherché à utiliser pour trouver les données.

Répétez ces étapes pour chaque recherche Web à affecter.

Vous pouvez également affecter des recherches Web à partir de la fenêtre **Liste des contacts** en suivant la même procédure.

## <a name="see-also"></a>Voir aussi
[Création de sociétés contact](marketing-create-contact-companies.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

