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
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 2a7ab137a9bf8ec3580e718053f8e67320e3af5a
ms.contentlocale: fr-ch
ms.lasthandoff: 08/06/2018

---
# <a name="managing-saved-settings-on-reports"></a>Gestion des paramètres enregistrés dans les états
Lors de l'exécution d'un état, les utilisateurs voient généralement une page qui leur permet de définir certaines options et certains filtres pour modifier les données incluses dans l'état généré. Cette page est appelée la page de demande de l'état. Un état peut inclure un ou plusieurs *paramètres enregistrés* que les utilisateurs peuvent appliquer à l'état à partir de la page de demande. Les *Paramètres enregistrés* sont essentiellement des options et des filtres prédéfinis. Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates. Pour plus d'informations sur l'utilisation des paramètres enregistrés, voir [Utilisation des paramètres enregistrés](ui-work-report.md#SavedSettings).

Si vous avez les bonnes autorisations, vous pouvez visualiser, créer et modifier les paramètres enregistrés pour tous les états pour tous les utilisateurs de la société. Vous pouvez attribuer les paramètres enregistrés d'un état à des utilisateurs en particulier ou à tous les utilisateurs de la société.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Créer et modifier les paramètres enregistrés pour tous les utilisateurs
Vous gérez les paramètres enregistrés à partir de la page **1560 Paramètres des états**. Deux méthodes sont disponibles pour ouvrir cette page :
-   Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Paramètres de l'état**, puis sélectionnez le lien connexe.
-   Ouvrez un état, sélectionnez la fonction de recherche en regard de la zone **Utiliser les valeurs par défaut de :**, puis choisissez **Sélectionner dans la liste complète**.

La page affiche toutes les entrées de paramètres enregistrés existants pour tous les utilisateurs. Si un nom d'utilisateur est indiqué dans la colonne **Affecté à**, seul cet utilisateur peut utiliser les paramètres enregistrés pour l'état associé. Si la colonne **Partager avec tous les utilisateurs** est cochée, tous les utilisateurs peuvent utiliser les paramètres enregistrés pour l'état.

Dans la page **Paramètres de l'état**, vous pouvez :
-   Sélectionner **Nouveau** pour créer une nouvelle entrée de paramètres enregistrés.
-   Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir **Copier** pour créer une copie.
-   Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir **Modifier** pour la modifier.


> [!Important]
> Définir le nom que vous souhaitez affecter à une entrée de paramètres enregistrés. Si vous créez une entrée de paramètres enregistrés pour tous les utilisateurs et vous lui donnez le même nom que l'entrée de paramètres enregistrés existants qui est affectée à un utilisateur spécifique, alors cet utilisateur ne pourra pas utiliser l'entrée de paramètres enregistrés qui est affectée à tous.  Sous **Paramètres enregistrés** dans la page de demande de l'état, l'utilisateur verra deux entrées de paramètres enregistrés avec le même nom. Toutefois, peu importe l'option qu'il choisit, l'entrée de paramètres enregistrés qui lui est spécifique sera utilisée.

> [!NOTE]
> La fonctionnalité Paramètres enregistrés n'est disponible que pour les états où la [propriété SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) de la page de demande de l'état est définie sur `Yes`. La propriété **SaveValues** est définie dans l'environnement de développement.  

## <a name="see-also"></a>Voir aussi
[Utilisation des états](ui-work-report.md)  

