---
title: Gérer les paramètres enregistrés pour les états et les traitements par lots
description: Décrit comment l’administrateur peut configurer des options et des filtres prédéfinis pour un rapport et partager ces paramètres avec un ou tous les utilisateurs.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: edupont
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><a name="manage-saved-settings-for-reports-and-batch-jobs"></a><a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Gérer les paramètres enregistrés pour les états et les traitements par lots

Lors de l’exécution d’un état, les utilisateurs voient généralement une page qui leur permet de sélectionner des options et de définir des filtres pour modifier les données incluses dans l’état généré. Cette page est appelée la *page de demande*. Un état peut inclure un ou plusieurs *paramètres enregistrés* que les utilisateurs peuvent appliquer à l’état à partir de la page de demande. Les *Paramètres enregistrés* sont essentiellement des options et des filtres prédéfinis. Le fait d’utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates. Pour plus d’informations, voir [Utiliser les paramètres enregistrés](ui-work-report.md#SavedSettings).

> [!NOTE]
> Cette rubrique fait référence aux *états*, mais des informations similaires s’appliquent aux *traitements par lots*.

Si vous avez les bonnes autorisations, vous pouvez visualiser, créer et modifier les paramètres enregistrés pour tous les états pour tous les utilisateurs de la société. Vous pouvez attribuer les paramètres enregistrés d’un état à des utilisateurs en particulier ou à tous les utilisateurs de la société.

## <a name="manage-saved-settings"></a><a name="manage-saved-settings"></a><a name="manage-saved-settings"></a>Gérer les paramètres enregistrés

Vous devez gérer les paramètres enregistrés à partir de la page **Paramètres des états**. Deux méthodes sont disponibles pour ouvrir cette page :

- Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres de l’état**, puis choisissez le lien associé.
- Sur la page de demande d’un état, sélectionnez la fonction de recherche dans le champ **Utiliser les valeurs par défaut de**, puis choisissez l’action **Sélectionner dans la liste complète**.

    Ce champ n’est visible que si vous avez exécuté le rapport au moins une fois auparavant. La liste n’affichera que les paramètres qui sont disponibles pour vous, soit parce qu’il s’agit de vos propres paramètres, soit parce que les paramètres sont partagés avec vous.

La page **Paramètres de l’état** affiche toutes les entrées de paramètres enregistrés existants pour tous les utilisateurs. Si un nom d’utilisateur est indiqué dans le champ **Affecté à**, seul cet utilisateur peut utiliser les paramètres enregistrés pour l’état associé. Si le champ **Partager avec tous les utilisateurs** est coché, tous les utilisateurs peuvent utiliser les paramètres enregistrés pour l’état.  

> [!TIP]
> Lorsqu’un utilisateur a exécuté un rapport qui prend en charge les paramètres partagés, ses paramètres sont enregistrés et ajoutés à cette liste. Dans la plupart des cas, l’administrateur peut ensuite modifier ces paramètres et choisir de partager les paramètres avec tous les utilisateurs.
>
> Cependant, dans certains cas, les paramètres ne peuvent pas être partagés et l’administrateur ne peut pas non plus les modifier. La plupart des traitements par lots ne prennent pas en charge les paramètres partagés.  

## <a name="create-or-modify-saved-settings-for-all-users"></a><a name="create-or-modify-saved-settings-for-all-users"></a><a name="create-or-modify-saved-settings-for-all-users"></a>Créer ou modifier les paramètres enregistrés pour tous les utilisateurs

Dans la page **Paramètres de l’état**, vous pouvez :

- Sélectionner l’action **Nouveau** pour créer une nouvelle entrée de paramètres enregistrés.
- Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir l’action **Copier** pour créer une copie.
- Sélectionner une entrée de paramètres enregistrés dans la liste, puis choisir l’action **Modifier** pour la modifier.

> [!Important]
> Définir le nom que vous souhaitez affecter à une entrée de paramètres enregistrés. Si vous créez une entrée de paramètres enregistrés pour tous les utilisateurs et vous lui donnez le même nom que l’entrée de paramètres enregistrés existants qui est affectée à un utilisateur spécifique, alors cet utilisateur ne pourra pas utiliser l’entrée de paramètres enregistrés qui est affectée à tous.  Dans la section **Paramètres enregistrés** dans la page de demande de l’état, l’utilisateur verra deux entrées de paramètres enregistrés avec le même nom. Toutefois, peu importe l’option qu’il choisit, l’entrée de paramètres enregistrés qui lui est spécifique sera utilisée.

> [!NOTE]
> La possibilité d’enregistrer les paramètres n’est disponible que pour les états où la [propriété SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) de la page de demande de l’état est définie sur **Oui**. La propriété **SaveValues** est définie par le développeur.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
