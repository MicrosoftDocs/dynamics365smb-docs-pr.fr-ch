---
title: Configurer des recherches Web pour des sociétés contact| Microsoft Docs
description: Vous pouvez définir des sources Internet ou Web et les affecter à une société contact pour identifier la manière dont vous souhaitez rechercher des informations sur vos contacts.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: aa5998b989d8a3d37f3d7bfcdb348a2c09381168
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "934411"
---
# <a name="set-up-web-sources-for-contact-companies"></a>Configuration de recherches Web pour des sociétés contact
Vous pouvez utiliser les recherches Web avec vos sociétés contact afin d'identifier, par exemple, des moteurs de recherche et des sites Web que vous souhaitez utiliser pour rechercher des informations relatives aux contacts. Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.

L'utilisation des recherches Web au niveau des contacts est un processus en deux étapes. Tout d'abord, vous définissez le code recherche Web. Vous ne devez effectuer cette étape qu'une seule fois pour chaque recherche Web. Une fois que vous disposez d'un code recherche Web, vous pouvez commencer à affecter ce code aux personnes contact.

## <a name="to-define-a-web-source-code"></a>Pour définir un code recherche Web
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Recherche Web**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs **Code**, **Désignation** et **URL**.

    Tapez %1 dans le champ **URL** pour insérer un espace réservé correspondant au mot recherché dans l'URL. Lorsque vous lancez la recherche Web à partir d'un contact, le %1 est automatiquement remplacé par le mot recherché (par exemple le nom de la société) que vous avez saisi sur la page **Recherche contacts Web**.

Répétez ces étapes pour chaque recherche Web à configurer.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Pour affecter une recherche Web à une société contact
Lorsque vous affectez des recherches Web, vous spécifiez le moteur de recherche et les mots recherchés que l'application doit utiliser pour trouver les données demandées.

1. Ouvrez le contact.
2. Sélectionnez l'action **Société**, puis l'action **Recherche Web**. La page **Recherche contact Web** s'affiche.
3. Dans le champ **Code recherche web**, sélectionnez la recherche Web à affecter.
4. Dans le champ **Mot recherché**, saisissez le mot recherché à utiliser pour trouver les données.

Répétez ces étapes pour chaque recherche Web à affecter.

Vous pouvez également affecter des recherches web à partir de la page **Liste des contacts** en suivant la même procédure.

## <a name="see-also"></a>Voir aussi
[Création de contacts](marketing-create-contact-companies.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
