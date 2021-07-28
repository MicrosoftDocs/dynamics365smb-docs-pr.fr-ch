---
title: Appliquer et modifier les paramètres enregistrés dans des états | Microsoft Docs
description: Décrit l’utilisation d’options et filtre prédéfinis pour personnaliser un état, et pour générer les données exactes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6d83597057975757354da06668a7e71e94e5273f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435778"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Gérer les paramètres enregistrés pour les états et les traitements par lots
Lors de l’exécution d’un état, les utilisateurs voient généralement une page qui leur permet de sélectionner des options et de définir des filtres pour modifier les données incluses dans l’état généré. Cette page est appelée la page de demande. Un état peut inclure un ou plusieurs *paramètres enregistrés* que les utilisateurs peuvent appliquer à l’état à partir de la page de demande. Les *Paramètres enregistrés* sont essentiellement des options et des filtres prédéfinis. Le fait d’utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates. Pour plus d’informations, voir [Utilisation des paramètres enregistrés](ui-work-report.md#SavedSettings).

> [!NOTE]
> Cette rubrique fait référence surtout aux « états », mais des informations similaires s’appliquent aux traitements par lots.

Si vous avez les bonnes autorisations, vous pouvez visualiser, créer et modifier les paramètres enregistrés pour tous les états pour tous les utilisateurs de la société. Vous pouvez attribuer les paramètres enregistrés d’un état à des utilisateurs en particulier ou à tous les utilisateurs de la société.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Pour créer et modifier les paramètres enregistrés pour tous les utilisateurs
Vous devez gérer les paramètres enregistrés à partir de la page **Paramètres des états**. Deux méthodes sont disponibles pour ouvrir cette page :
-   Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres de l’état**, puis choisissez le lien associé.
-   Ouvrez un état, sélectionnez la fonction Tell Me dans le champ **Utiliser les valeurs par défaut de**, puis choisissez l’action **Sélectionner dans la liste complète**.

La page affiche toutes les entrées de paramètres enregistrés existants pour tous les utilisateurs. Si un nom d’utilisateur est indiqué dans le champ **Affecté à**, seul cet utilisateur peut utiliser les paramètres enregistrés pour l’état associé. Si le champ **Partager avec tous les utilisateurs** est coché, tous les utilisateurs peuvent utiliser les paramètres enregistrés pour l’état.

Dans la page **Paramètres de l’état**, vous pouvez :
-   Sélectionner l’action **Nouveau** pour créer une nouvelle entrée de paramètres enregistrés.
-   Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir l’action **Copier** pour créer une copie.
-   Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir l’action **Modifier** pour la modifier.

> [!Important]
> Définir le nom que vous souhaitez affecter à une entrée de paramètres enregistrés. Si vous créez une entrée de paramètres enregistrés pour tous les utilisateurs et vous lui donnez le même nom que l’entrée de paramètres enregistrés existants qui est affectée à un utilisateur spécifique, alors cet utilisateur ne pourra pas utiliser l’entrée de paramètres enregistrés qui est affectée à tous.  Dans la section **Paramètres enregistrés** dans la page de demande de l’état, l’utilisateur verra deux entrées de paramètres enregistrés avec le même nom. Toutefois, peu importe l’option qu’il choisit, l’entrée de paramètres enregistrés qui lui est spécifique sera utilisée.

> [!NOTE]
> La fonctionnalité Paramètres enregistrés n’est disponible que pour les états où la propriété [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) de la page de demande de l’état est définie sur **Oui**. La propriété **SaveValues** est définie dans l’environnement de développement.  

## <a name="see-also"></a>Voir aussi
[Utilisation des états, des traitements par lots et des XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]