---
title: "Appliquer et modifier les paramètres enregistrés dans des états | Microsoft Docs"
description: "Décrit l'utilisation d'options et filtre prédéfinis pour personnaliser un état, et pour générer les données exactes."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 42deec3d94209a7963e596e7deb5584fccd6db7f
ms.openlocfilehash: adc15d5f80f4d7ab2a1ca5a8247588ec0aa9779a
ms.contentlocale: fr-ch
ms.lasthandoff: 07/19/2018

---
# <a name="managing-saved-settings-on-reports"></a>Gestion des paramètres enregistrés dans les états
En fonction de l'état exécuté, vous pouvez bénéficier d'une page qui vous laisse définir certaines options et certains filtres pour modifier les données incluses dans l'état généré. Cette page est connue comme la page de demande de l'état. Un état peut inclure un ou plusieurs *paramètres enregistrés* que vous pouvez appliquer à l'état à partir de la page de demande. Les *Paramètres enregistrés* sont essentiellement des options et des filtres prédéfinis. Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates.

Vous pouvez voir les paramètres enregistrés qui sont à votre disposition pour un état dans la section **Paramètres enregistrés** de la page de demande de l'état.  

## <a name="apply-saved-settings-to-a-report"></a>Appliquer des paramètres enregistrés à un état
1. Ouvrez l'état.

   La page de demande de l'état s'affiche.    
2. Dans la section **Paramètres enregistrés** de la page, définissez le champ **Nom** dans les paramètres enregistrés que vous souhaitez utiliser.

   La section **Paramètres enregistrés** apparaît uniquement si l'état a été exécuté avant ou s'il y a des écritures de paramètres enregistrées. L'écriture de paramètres enregistrés appelée **Options et filtres récemment utilisés** est toujours disponible. Ces paramètres sont les valeurs d'option et de filtre qui ont été utilisées la dernière fois que vous avez exécuté l'état.

## <a name="create-and-modify-saved-settings-for-all-users"></a>Créer et modifier les paramètres enregistrés pour tous les utilisateurs
Si vous avez les bonnes autorisations, vous pouvez visualiser, créer et modifier les paramètres enregistrés pour tous les états pour tous les utilisateurs de la société. Vous pouvez attribuer les paramètres enregistrés d'un état à des utilisateurs en particulier ou à tous les utilisateurs de la société.

Vous gérez les paramètres enregistrés à partir de la page 1560 **Paramètres des états**. Pour ouvrir cette page, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres de l'état**, puis sélectionnez le lien connexe.

Sur la page **Paramètres d'état**, vous pouvez créer de nouveaux paramètres à partir de zéro ou vous pouvez effectuer une copier et modifier des paramètres existants. Pour modifier les options et les filtres pour un paramètre, sélectionnez l'action **Modifier**.

> [!NOTE]
> la fonctionnalité des paramètres enregistrés des états n'est appropriée que lorsque la propriété SaveValues de la page de demande est définie sur Oui. La propriété SaveValues est définie dans l'environnement de développement.  

> [!Important]
> Si vous créez un article de paramètres enregistrés pour tous les utilisateurs, et qu'il porte le même nom que les paramètres enregistrés existants pour un utilisateur spécifique, alors cet utilisateur ne pourra pas utiliser les paramètres enregistrés affectés à tous.  Dans le champ Paramètres enregistrés de la page de demande d'état, l'utilisateur verra deux options de paramètres enregistrées avec le même nom. Toutefois, peu importe l'option qu'il choisit, les paramètres enregistrés qui lui sont spécifiques seront utilisés.

## <a name="see-also"></a>Voir aussi
[Utilisation des états](ui-work-report.md)  

