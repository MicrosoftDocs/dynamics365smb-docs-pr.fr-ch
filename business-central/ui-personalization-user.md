---
title: Personnalisation des pages | Microsoft Docs
description: Découvrez comment personnaliser l'interface utilisateur pour l'adapter à votre méthode de travail dans Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: de7acb10c76acc05fc6e6a5c708a8d412e4d9b30
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632744"
---
# <a name="personalizing-your-workspace"></a>Personnalisation de votre espace de travail

Vous pouvez *personnaliser* votre espace de travail pour l'adapter à vos habitudes et préférences en modifiant les pages afin qu'elles n'affichent que les informations dont vous avez besoin, où vous avez en besoin. Les modifications de personnalisation que vous apportez n'affectent que ce que vous voyez, pas ce que voient les autres utilisateurs.

Selon le type de page et ce qu'elle inclut, vous pouvez effectuer différentes opérations, comme déplacer ou masquer des champs, colonnes et actions, déplacer et masquer des pièces entières, etc.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Outre ce que les utilisateurs peuvent personnaliser, les administrateurs et les super utilisateurs peuvent remplacer les personnalisations des utilisateurs et définir les fonctionnalités accessibles dans toutes les sociétés ou des sociétés spécifiques. Pour plus d'informations, voir [Personnalisation de Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Pour personnaliser une page

1. Dans l'angle supérieur droit, sélectionnez l'icône ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez **Personnaliser**.

    La bannière **Personnalisation** s'affiche en haut, ce qui indique que vous pouvez commencer à apporter des modifications.

    ![Mode Personnaliser](media/ui_personalize_mode_small.png "Mode Personnaliser")

2. Accédez à une page à personnaliser.

    Si vous voyez une icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation") ou ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée") dans la bannière, vous ne pouvez pas personnaliser la page. Pour en savoir plus, reportez-vous à la rubrique [Pourquoi ne puis-je pas personnaliser une page](ui-personalization-locked.md).

3. Pointez sur une zone à personnaliser, comme un champ ou un en-tête de colonne dans la liste. Tout ce que vous pouvez personnaliser est immédiatement mis en évidence avec une flèche ou un contour. Reportez-vous à la [section suivante](#What) pour connaître les détails des possibilités qui vous sont offertes.

4. Vous pouvez continuer à apporter des modifications sur la même page, ou ouvrir une autre page. Vos modifications sont automatiquement enregistrées au fur et à mesure. Lorsque vous avez terminé, dans la bannière **Personnalisation**, sélectionnez **Terminée**.

## <a name="What"></a>Ce que vous pouvez personnaliser

|Ce que vous voulez faire|Comment procéder|Remarques|
|----|------------|-------|
|Déplacer quelque chose, comme un champ, une colonne d'une liste, une mosaïque, une action ou une section|Pointez n'importe où sur ce que vous souhaitez déplacer, puis faites-le glisser vers son nouvel emplacement. L'emplacement est indiqué par une ligne verticale ou horizontale épaisse.<br /><br />![Impossible de déplacer une icône ici](media/personalization-cannot-move-here.png "Mode Personnaliser - Impossible de déplacer une icône ici") indique que vous ne pouvez pas déplacer l'élément vers l'emplacement sélectionné.|Les sections sont des subdivisions ou des zones d'une page qui contiennent des éléments comme des champs multiples, une autre page, un graphique, ou des mosaïques.<br /><br />Pour en savoir plus sur la personnalisation des actions, reportez-vous à la [section suivante](ui-personalization-user.md#Actions). |
|Masquez quelque chose, comme un champ, une colonne d'une liste, une mosaïque ou une section.|Sélectionnez la pointe de flèche, puis sélectionnez <b>Masquer</b>.|Si le champ que vous masquez s'affiche également dans l'en-tête Raccourci lorsque ce dernier est réduit, le champ n'y apparaîtra plus.|
|Ajoutez un champ ou une colonne.|Dans la bannière <b>Personnalisation</b>, choisissez <b>Plus</b>, puis sélectionnez <b>Champ</b>.<br /></br>Le volet <b>Ajouter un champ à la page</b> s'ouvre à droite. Il répertorie les champs que vous pouvez ajouter à la page.<br /><br />Pour ajouter un champ, faites-le glisser du volet vers l'emplacement que vous souhaitez. L'emplacement est indiqué par une ligne verticale ou horizontale épaisse.|Chaque page comprend un ensemble prédéfini de champs que vous pouvez afficher. Utilisez cette procédure pour afficher des champs ou des colonnes qui n'ont pas été précédemment affichés ou pour afficher des champs que vous avez masqués.|
|Affichez un champ dans l'en-tête d'un raccourci lorsque le raccourci est réduit.|Sélectionnez la pointe de la flèche, puis cliquez sur <b>Afficher si réduit</b>. <br /> <br />Si vous ne voyez pas cette option, elle est déjà définie. Dans ce cas, pour arrêter d'afficher le champ dans l'en-tête du raccourci, sélectionnez <b>Afficher toujours</b>.|*Raccourci* désigne le terme employé pour un groupe de champs qui s'affichent sous une en-tête commune. Utilisez l'option <b>Afficher si réduit</b> pour afficher les champs les plus importants. Si vous sélectionnez un champ dans l'en-tête, le raccourci s'ouvrira et se concentrera sur le champ sélectionné.<br /><br />Cette option s'applique uniquement si une page a plusieurs raccourcis. S'il s'agit de l'unique raccourci, il ne peut pas être réduit, aussi l'option <b>Afficher si réduit</b> n'est pas disponible.|
|Affichez un champ uniquement lorsque vous sélectionnez **Afficher plus**.|Sélectionnez la pointe de flèche, puis cliquez sur <b>Afficher sous « Afficher plus »</b>. <br /> <br />Si vous ne voyez pas l'option <b>Afficher sous « Afficher plus »</b>, elle est déjà définie. Dans ce cas, pour afficher toujours un champ, et non pas uniquement lorsque vous sélectionnez **Afficher plus**, sélectionnez <b>Afficher toujours</b>.||
|Modifiez le volet Figer d'une liste en d'autres colonnes. |Sélectionnez la pointe de flèche de la colonne que vous souhaitez être la dernière du volet Figer, puis sélectionnez <b>Définir le volet Figer</b>.<br /><br/>Si vous souhaitez rétablir le volet Figer à son emplacement d'origine, sélectionnez la pointe de flèche de la colonne actuelle du volet Figer, puis sélectionnez <b>Effacer le volet Figer</b>. Remarque : vous ne pouvez pas supprimer ce volet Figer d'origine.|Le volet Figer spécifie les colonnes qui s'affichent toujours à gauche, même lorsque vous faites défiler horizontalement.|  
|Modifiez la largeur d'une colonne.|Dans l'en-tête de la liste, faites glisser la limite entre les colonnes. <br /><br />Vous pouvez double-cliquer sur la limite entre les en-têtes de colonne pour l'ajuster automatiquement, ce qui permet de définir une largeur confortable pour la lisibilité.||
|Survolez un champ tout en appuyant sur Entrée.|Sélectionnez la pointe de la flèche en regard du champ, ou la première colonne d'une liste, et sélectionnez **Exclure de la saisie rapide**. <br /><br /> Si vous ne voyez pas cette option, le champ est déjà défini pour être ignoré. Dans ce cas, pour arrêter d'ignorer le champ, choisissez **Inclure de la saisie rapide**. |Reportez-vous à la rubrique [Accélérer la saisie de données à l'aide de la fonction Saisie rapide](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Personnalisation des actions

Vous pouvez personnaliser la barre d'actions qui se trouve en haut de la page, comme indiqué par la zone sélectionnée dans l'illustration suivante.

![Personnaliser la barre d'actions](media/personalize-action-bar.png "Personnaliser la barre d'actions")

La personnalisation vous permet de choisir quelles actions afficher sur la barre d'actions et où les afficher. Vous pouvez afficher, masquer ou déplacer les actions individuelles ou groupes d'action. La personnalisation de la barre d'actions est exécutée essentiellement de la même façon qu'avec les autres éléments de l'espace de travail. Toutefois, ce que vous pouvez faire exactement avec une action ou un groupe dépend de l'emplacement de l'action ou du groupe dans la barre d'actions. La meilleure façon de le savoir consiste à essayer et à vous laisser guider sur l'écran. Les sections suivantes expliquent certaines des nuances de la personnalisation de la barre d'actions.

### <a name="action-bar-overview"></a>Aperçu de la barre d'actions

Vous devez vous familiariser avec certains termes pour mieux comprendre la personnalisation de la barre d'actions : *groupe d'actions* et *catégorie promue*.  

Un *groupe d'actions* désigne l'article qui se développe pour afficher d'autres actions ou groupes. Par exemple, dans l'illustration suivante, **Validation** désigne un groupe d'actions.

Une *catégorie promue* désigne un groupe d'actions qui s'affiche entre les deux lignes verticales `|` de la barre d'actions. Les catégories incluent généralement les actions utilisées le plus fréquemment afin que vous puissiez les trouver rapidement. Par exemple, dans l'illustration suivante, **Lancer**, **Validation**, **Facture** et **Naviguer** sont des catégories promues.

![Personnaliser le groupe de la barre d'actions](media/personalize-action-bar-group-clip.png "Personnaliser le groupe de la barre d'actions")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Pour supprimer, masquer et afficher des actions et des groupes

Pour afficher ou masquer des actions ou des groupes, sélectionnez-les, puis sélectionnez une des options suivantes :

|Option|Action|
|------|------------
|**Supprimer**|Cette option s'affiche si l'action sélectionnée est également affichée ailleurs dans la barre d'actions. En choisissant cette option, vous supprimez l'action de l'emplacement sélectionné afin qu'elle n'apparaisse plus. L'action ou le groupe d'actions reste dans les autres emplacements. |
|**Masquer**|Cette option s'affiche si l'action ou le groupe d'actions apparaît nulle part ailleurs dans la barre d'actions. Comme **Supprimer**, choisissez cette option pour inciter l'action ou le groupe d'actions à disparaître de la barre d'actions. Toutefois, en mode personnalisation, l'action ou le groupe d'actions est toujours affiché dans l'emplacement actuel, sauf si elle/il apparaît atténué(e).|
|**Afficher**|Cette option s'affiche si l'action ou le groupe d'actions a été précédemment masqué(e) atténué(e). En choisissant cette option, vous permettez à l'action ou au groupe d'actions de figurer dans la barre d'actions.|

### <a name="to-move-actions-and-action-groups"></a>Pour déplacer les actions et groupes d'actions

Pour déplacer une action ou un groupe d'actions, faites-la/le glisser à l'emplacement souhaité, comme avec les champs et les colonnes.

Là où vous pouvez déplacer des actions ou groupes d'actions est indiqué par une ligne horizontale entre les actions ou une bordure autour d'un groupe d'actions.

- Vous pouvez déplacer les actions individuelles dans les catégories promues, mais vous ne pouvez pas réorganiser l'ordre des actions dans la catégorie.
- Vous ne pouvez pas déplacer un groupe d'actions dans une catégorie promue.
- Pour déplacer une action ou un groupe d'actions dans un autre groupe d'actions vide, déplacez l'action ou le groupe d'actions vers le nouveau groupe et placez-la/le dans la zone **Déplacer une action ici**.

## <a name="additional-points-of-interest"></a>Points d'intérêts supplémentaires

Pour vous aider à mieux comprendre la personnalisation, voici quelques points clés.

- Lorsque vous apportez des modifications à une page de fiche ouverte à partir d'une liste, les modifications s'appliquent à tous les enregistrements que vous ouvrez à partir de cette liste. Par exemple, disons que vous ouvrez un client spécifique à partir de la page Liste des clients, puis que vous personnalisez cette page en y ajoutant un champ. Lorsque vous ouvrez d'autres clients à partir de la liste, le champ que vous avez ajouté s'affiche également.
- Les modifications que vous apportez s'appliquent à tous vos tableaux de bord. Par exemple, si vous modifiez la liste Clients lorsque le tableau de bord est défini sur Gestionnaire d'activité, vous verrez également la modification de la liste Client lorsque le tableau de bord est défini sur Préparateur de commandes vente.
- Les modifications d'une page dans un volet s'appliquent à la page, où qu'elle s'affiche.  
- Vous ne pouvez ajouter de champs et de colonnes qu'à partir d'une liste prédéfinie, laquelle est basée sur la page. Vous ne pouvez pas en créer de nouveaux.

## <a name="to-clear-personalization"></a>Pour annuler la personnalisation

Vous pouvez souhaiter annuler toutes les modifications de personnalisation apportées à une page au fil du temps. Pour ce faire, dans la bannière **Personnalisation**, sélectionnez **Plus**, puis **Effacer la personnalisation** et sélectionnez une des options suivantes. Sachez qu'il est impossible d'annuler votre action une fois la personnalisation annulée.

|Option|Action|
|------|------------
|Actions seules|Efface toutes les modifications de personnalisation apportées à la barre d'actions sur la page.|
|Tous sauf les actions|Annule toutes les modifications de personnalisation apportées à la page, hormis celles de la barre d'actions. Cela inclut les modifications apportées aux champs, colonnes, pièces et mosaïques. |
|Tous|Efface toutes les modifications de personnalisation apportées à cette page afin que cette page retrouve son aspect d'origine. Cela inclut les modifications apportées à la barre d'actions, aux champs, colonnes, pièces et mosaïques.|

## <a name="see-also"></a>Voir aussi

[Gérer la personnalisation](ui-personalization-manage.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
