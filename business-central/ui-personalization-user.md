---
title: Personnalisation des pages (contient une vidéo)
description: "Découvrez comment personnaliser l’interface utilisateur et votre espace de travail pour l’adapter à votre façon de travailler et aux préférences personnelles dans Business\_Central."
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 01/15/2024
ms.author: jswymer
---
# <a name="personalize-your-workspace"></a>Personnaliser votre espace de travail

Vous pouvez personnaliser votre espace de travail en fonction de vos habitudes et préférences. Modifiez les pages afin qu’elles n’affichent que les informations dont vous avez besoin, où vous en avez besoin. La personnalisation n’affecte que votre espace de travail. Cela ne change pas la façon dont les autres fonctionnent. Vous pouvez personnaliser tous les types de pages, y compris la page [Tableau de bord](ui-change-basic-settings.md#role-center).

> [!NOTE]
> En raison de restrictions sur les capacités de conception du client Web, il n’est actuellement pas possible de personnaliser les contrôles dans la syntaxe `grid` et `fixed`.
Cela s’applique à tous les modes de conception, pas seulement à la personnalisation.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Vous pouvez apporter différentes modifications, comme déplacer ou masquer des champs, des colonnes et des actions, déplacer et masquer des pièces entières, et ajouter de nouveaux champs. La plupart des personnalisations doivent être effectuées en activant d’abord la bannière **Personnalisation**. Des ajustements simples, comme la largeur de colonne, peuvent être effectués immédiatement sur n’importe quelle liste.

> [!NOTE]
> Les administrateurs peuvent effectuer les mêmes modifications de présentation que les utilisateurs en personnalisant le profil (rôle) attribué à plusieurs utilisateurs. Pour en savoir plus sur les pages pour les rôles, accédez à [Personnaliser les pages pour les rôles](ui-personalization-manage.md)<br /><br />
Les administrateurs peuvent aussi remplacer ou désactiver des personnalisations des utilisateurs et définir les fonctionnalités accessibles dans toutes les sociétés ou des sociétés spécifiques. Pour plus d’informations, voir [Personnalisation de Business Central](ui-customizing-overview.md).

## <a name="video"></a>Vidéo

La vidéo suivante montre quelques-unes des façons dont vous pouvez personnaliser votre tableau de bord.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="change-the-width-of-a-column"></a>Modification de la largeur d’une colonne

Vous pouvez facilement redimensionner les colonnes de n’importe quelle liste. Il suffit simplement de faire glisser la limite entre deux colonnes vers la gauche ou la droite.  

1. Dans l’en-tête de la liste, sélectionnez et faites glisser la limite entre deux colonnes.
2. Vous pouvez également double-cliquer sur la limite entre deux colonnes pour ajuster automatiquement la largeur de la colonne. La largeur s’ajuste à la taille optimale pour une meilleure lisibilité.

En ce qui concerne les autres personnalisations, les modifications apportées à la largeur des colonnes sont stockées sur votre compte et vous suivent quel que soit le périphérique auquel vous vous connectez.

## <a name="start-personalizing-by-using-the-personalization-mode"></a>Commencez à personnaliser en utilisant le mode de personnalisation

1. Ouvrez une page quelconque à personnaliser.
1. Dans l’angle supérieur droit, sélectionnez l’icône ![Paramètres.](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord") puis l’action **Personnaliser**.

    La bannière **Personnalisation** s’affiche en haut, ce qui indique que vous pouvez commencer à apporter des modifications.

    > [!NOTE]
    > Pour naviguer pendant la personnalisation, utilisez <kbd>Ctrl</kbd>+<kbd>Clic</kbd> sur une action si elle est mise en surbrillance par la pointe de la flèche.

    Si vous voyez une icône ![Verrouillage de personnalisation](media/personalization-lock-icon.png "Verrouillage de personnalisation") ou ![Personnalisation bloquée](media/personalization-blocked-icon.png "Personnalisation bloquée") sur la bannière, vous ne pouvez pas personnaliser la page. Pour plus d’informations, consultez [Pourquoi la personnalisation d’une page est bloquée](ui-personalization-locked.md).

1. Pour modifier un élément de l’interface utilisateur, pointez sur l’élément, par exemple une action, un champ ou une pièce. L’élément est immédiatement mis en évidence avec une pointe de flèche ou une bordure. Choisissez l’élément, puis choisissez soit **Déplacer**, **Supprimer**, **Masquer**, **Afficher**, **Afficher sous « Afficher plus »**, **Afficher si réduit**, **Afficher toujours**, **Définir/Effacer le volet Figer**, ou **Inclure/Exclure de la saisie rapide**, en fonction du type et de l’état de l’élément d’interface utilisateur.
1. Pour ajouter un champ, choisissez l’action **+ Champ**. À partir du volet **Ajouter un champ à la page**, faites glisser un champ vers la position souhaitée sur la page.
1. Lorsque vous avez fini de modifier la mise en page sur une ou plusieurs pages, choisissez le bouton **Terminé** sur la bannière **Personnalisation**.

Pour plus d’informations, voir [Ce que vous pouvez personnaliser](#What).

## <a name="what-you-can-personalize"></a><a name="What"></a>Ce que vous pouvez personnaliser

|Ce que vous voulez faire|Comment procéder|Remarques|
|----|------------|-------|
|Déplacer quelque chose, comme un champ, une colonne d’une liste, une mosaïque, une action ou une section vers un autre endroit sur la page|Pointez n’importe où sur ce que vous souhaitez déplacer, puis faites glisser vers la nouvelle position. Une ligne verticale ou horizontale épaisse indique la position.<br /><br />![Icône Impossible de déplacer ici](media/personalization-cannot-move-here.png "Mode personnalisation - Icône Impossible de déplacer ici") indique que vous ne pouvez pas déplacer l’élément vers la position sélectionnée.|Les sections sont des subdivisions ou des zones d’une page qui contiennent des éléments comme des champs multiples, une autre page, un graphique, ou des mosaïques.<br /><br />[En savoir plus sur la personnalisation des actions](#Actions)<br>[En savoir plus sur la personnalisation des pièces](#Parts)|
|Masquez un élément actuellement affiché, comme un champ, une colonne dans une liste, une vignette, une action ou une pièce.|Sélectionnez l’élément, sélectionnez la pointe de flèche, puis sélectionnez <b>Masquer</b>.|En mode personnalisation, les actions masquées sont grisées avec du texte en italique et les parties cachées sont ombrées par des lignes diagonales. Les champs et colonnes masqués ne sont pas indiqués sur la page. <!--The element is grayed when you are in personalizing mode.--> Lorsque vous quittez le mode personnalisation, tous les éléments disparaissent de la vue. Si le champ que vous masquez s’affiche également sur l’en-tête Raccourci lorsque ce dernier est réduit, le champ n’y apparaîtra plus.|
|Afficher une action ou une partie actuellement masquée|Pour un élément grisé (masqué), choisissez la pointe de flèche, puis choisissez <b>Afficher</b>.|L’élément masqué est à nouveau visible.|
|Afficher un champ actuellement masqué|Dans la bannière <b>Personnalisation</b>, choisissez l’action <b>+ Champ</b>.<br /></br>Le volet <b>Ajouter un champ à la page</b> s’ouvre à droite de la page. Si vous sélectionnez un champ dans le volet, son emplacement masqué apparaît sur la page.<br /><br />Pour afficher un champ, faites-le glisser du volet ou de son emplacement masqué vers la position que vous souhaitez. La position est indiquée par une ligne verticale ou horizontale épaisse.<br><br> Une autre méthode consiste à sélectionner la pointe de flèche à l’emplacement caché du champ et à sélectionner **Afficher**. |Chaque page comprend un ensemble prédéfini de champs que vous pouvez afficher.<br /><br />[En savoir plus sur les champs de travail](#fields) |
|Affichez un champ dans l’en-tête d’un raccourci lorsqu’il est réduit.|Choisissez la pointe de la flèche, puis cliquez sur <b>Afficher si réduit</b>. <br /> <br />Si vous ne voyez pas cette option, elle est déjà définie. Dans ce cas, pour arrêter d’afficher le champ sur l’en-tête du raccourci, sélectionnez <b>Afficher toujours</b>.|*Raccourci* désigne le terme employé pour un groupe de champs qui s’affichent sous un en-tête commun. Utilisez l’option <b>Afficher si réduit</b> pour afficher les champs les plus importants. Si vous sélectionnez un champ dans l’en-tête, le raccourci s’ouvrira et se concentrera sur le champ sélectionné.<br /><br />Cette option s’applique uniquement si une page a plusieurs raccourcis. S’il n’y a qu’un seul raccourci, il ne peut pas être réduit, aussi l’option <b>Afficher si réduit</b> n’est pas disponible.|
|Affichez un champ uniquement lorsque vous sélectionnez **Afficher plus**.|Choisissez la pointe de flèche, puis cliquez sur <b>Afficher sous « Afficher plus »</b>.|Si vous ne voyez pas l’option <b>Afficher sous « Afficher plus »</b>, elle est déjà définie. Dans ce cas, pour afficher toujours un champ, et non pas uniquement lorsque vous sélectionnez **Afficher plus**, sélectionnez <b>Afficher toujours</b>.|
|Changer si un champ peut être modifié ou non.|Sélectionnez le champ, sélectionnez la pointe de flèche sur le champ, puis sélectionnez <b>Verrouiller la modification</b> pour empêcher la modification de la valeur du champ ou <b>Déverrouiller la modification</b> pour permettre de modifier la valeur du champ.|Vous ne pouvez déverrouiller que les champs que vous avez préalablement verrouillés. Certains champs sont verrouillés par défaut, soit par conception, soit par un administrateur de profil qui a [personnalisé la page](ui-personalization-manage.md). Ces champs ne peuvent pas être déverrouillés.|
|Modifiez le volet Figer d’une liste en d’autres colonnes. |Choisissez la pointe de flèche de la colonne que vous souhaitez être la dernière du volet Figer, puis sélectionnez <b>Définir le volet Figer</b>.<br /><br/>Si vous souhaitez rétablir le volet Figer à sa position d’origine, sélectionnez la pointe de flèche de la colonne actuelle du volet Figer, puis sélectionnez <b>Effacer le volet Figer</b>. Remarque : vous ne pouvez pas supprimer ce volet Figer.|Le volet Figer spécifie les colonnes qui s’affichent toujours à gauche de la liste, même lorsque vous faites défiler horizontalement.|  
|Survolez un champ tout en appuyant sur Entrée.|Choisissez la pointe de la flèche en regard du champ, ou la première colonne d’une liste, et sélectionnez **Exclure de la saisie rapide**.  | Si vous ne voyez pas **Exclure de Saisie rapide**, le champ est déjà défini pour être ignoré. Dans ce cas, pour arrêter d’ignorer le champ, choisissez **Inclure de la saisie rapide**.<br><br>[En savoir plus sur la saisie rapide](ui-enter-data.md#QuickEntry)|
|Réorganisez et supprimez les vues représentant des listes filtrées.|Choisissez la flèche en regard d’une vue, puis choisissez **Déplacer**, **Supprimer** ou **Masquer**.|[En savoir plus sur l’enregistrement et la personnalisation des vues de liste](ui-views.md)|  
|Ajoutez une nouvelle action à une page ou à un état sur votre tableau de bord.|Dans la page cible, la page de demande d’état, ou la fenêtre Tell Me, choisissez l’icône de signet.|[En savoir plus sur la mise en signet des pages et des rapports](ui-bookmarks.md)|
|Toujours démarrer une liste comme développée ou réduite|Choisissez le bouton **Développer tout** ou **Réduire tout** dans le coint supérieur gauche de la liste. Sinon, choisissez l’action **Développer tout** ou **Réduire tout** dans le menu de la première colonne. |S’applique aux listes hiérarchiques réductibles|

## <a name="personalize-action-bar-and-menus"></a><a name="Actions"></a>Personnaliser la barre d’action et les menus

La personnalisation vous permet de choisir les actions à afficher sur les barres de navigation et d’actions et sur les tableaux de bord et où les afficher. Vous pouvez afficher, masquer ou déplacer les actions individuelles ou groupes d’action.

La vidéo suivante montre comment vous pouvez personnaliser les actions sur les pages et les tableaux de bord.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

La personnalisation des barres de navigation et d’actions est exécutée essentiellement de la même façon qu’avec les autres éléments de l’interface utilisateur. Toutefois, ce que vous pouvez faire avec une action ou un groupe dépend de l’emplacement de l’action ou du groupe. La meilleure façon de le savoir consiste à passer en mode de personnalisation et à vous laisser guider par les flèches.

Vous devez vous familiariser avec certains termes pour mieux comprendre la personnalisation de la barre d’actions : *groupe d’actions* et *catégorie promue*.  

Un *groupe d’actions* désigne un élément qui se développe pour afficher d’autres actions ou groupes. Par exemple, sur la page **Commandes vente**, un groupe d’actions est l’action **Fonctions** qui apparaît lorsque vous choisissez l’action **Actions**.

Une *catégorie promue* désigne un groupe d’actions qui s’affiche avant la ligne verticale `|` sur la barre d’actions. Les catégories incluent généralement les actions utilisées le plus fréquemment afin que vous puissiez les trouver rapidement. Par exemple, sur la page **Commande vente**, les actions **Commande**, **Lancer** et **Validation** sont des catégories promues.

> [!NOTE]  
> Pour effacer la personnalisation, sélectionnez la pointe de flèche autour du menu du concepteur de la pièce, puis choisissez **Effacer la personnalisation**.

### <a name="remove-hide-and-show-actions-and-action-groups"></a>Supprimer, masquer et afficher des actions et des groupes d’actions

Lorsque vous souhaitez afficher ou masquer une action, les options situées sous la flèche définissent ce que vous pouvez faire en fonction de l’état de l’action. 

1. Choisissez la flèche d’une action ou d’un groupe d’actions.
2. Choisissez l’une des options suivantes :

|Option|Action|
|------|------------
|**Supprimer**|Cette option s’affiche si l’action sélectionnée est également affichée ailleurs sur les barres de navigation et d’actions. En choisissant cette option, vous supprimez l’action de l’emplacement sélectionné afin qu’elle n’apparaisse plus. L’action ou le groupe d’actions reste dans les autres emplacements. |
|**Masquer**|Cette option s’affiche si l’action ou le groupe d’actions apparaît nulle part ailleurs sur les barres de navigation et d’actions. Comme **Supprimer**, choisissez cette option pour inciter l’action ou le groupe d’actions à disparaître des barres de navigation et d’actions. Toutefois, en mode personnalisation, l’action ou le groupe d’actions est toujours affiché dans la position actuelle, sauf si elle/il apparaît atténué(e).|
|**Afficher**|Cette option s’affiche si l’action ou le groupe d’actions a été précédemment masqué(e) atténué(e). En choisissant cette option, vous permettez à l’action ou au groupe d’actions de figurer dans la barre de navigation ou la barre d’actions.|

### <a name="move-actions-and-action-groups"></a>Déplacer les actions et groupes d’actions

L’emplacement où vous pouvez déplacer des actions ou groupes d’actions est indiqué par une ligne horizontale entre deux actions ou une bordure autour d’un groupe d’actions. Les limitations suivantes s’appliquent :

- Vous pouvez déplacer des actions individuelles dans les catégories promues, mais vous ne pouvez pas réorganiser l’ordre des actions dans la catégorie.
- Vous ne pouvez pas déplacer un groupe d’actions dans une catégorie promue.

1. Pour déplacer une action ou un groupe d’actions, faites-la/le glisser sur la position souhaitée, comme avec les champs et les colonnes.
2. Pour déplacer une action ou un groupe d’actions dans un autre groupe d’actions vide, déplacez l’action ou le groupe d’actions vers le nouveau groupe et placez-la/le dans la zone **Déplacer une action ici**.

### <a name="about-the-automate-menu"></a>À propos du menu Automatiser

- Vous ne pouvez pas masquer ou déplacer le menu **Automatiser** ou le sous-menu **Power Automate** et ses actions.
- Vous pouvez déplacer les flux inclus dans l’élément **Automatiser**, mais vous ne pouvez pas les masquer à l’aide de la personnalisation. Déplacer le flux crée une copie du flux vers la destination qui n’est pas supprimée de l’élément **Automatiser**.

> [!TIP]
> En tant qu’administrateur, vous pouvez masquer l’élément **Automatisation** des utilisateurs. En savoir plus sur [Configuration de l’intégration Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="personalize-parts"></a><a name="Parts"></a>Personnaliser les pièces

Pointez vers ou sélectionnez <kbd>Alt</kbd>+<kbd>Flèche vers le haut</kbd> Les parties sont des zones d’une page généralement composées de plusieurs champs, graphiques ou autres contenus. Une partie peut être identifiée par une bordure colorée lors du réglage du focus sur la partie. Par exemple, un écran d’accueil Tableau de bord comporte plusieurs pièces. En raison de sa limite bien définie, vous pouvez personnaliser l’ensemble de la partie et son contenu.

- Pour déplacer une pièce, faites-la glisser vers la position souhaitée. Une ligne colorée indique les positions valides sur l’écran. Par exemple, les récapitulatifs peuvent être déplacés uniquement à côté d’autres récapitulatifs dans le volet Récapitulatif.
- Vous pouvez masquer une pièce en sélectionnant l’option **Masquer** sous la pointe de flèche.
- Lorsque vous commencez à personnaliser ou accédez à une nouvelle page, toutes les pièces actuellement masquées s’affichent sur la page avec des visuels distinctifs pour indiquer qu’elles sont masquées. Vous pouvez réafficher cette pièce en sélectionnant l’option **Afficher** sous la pointe de flèche.

Vous pouvez effacer toutes les modifications de personnalisation que vous avez apportées dans une seule pièce en sélectionnant l’option **Effacer la personnalisation** sous la pointe de flèche de la pièce. L’effacement de la personnalisation d’une pièce n’affecte que les modifications apportées au contenu de la pièce, et non le placement ou la visibilité de la pièce sur la page.  

## <a name="work-with-fields-and-columns"></a><a name="fields"></a>Utiliser des champs et des colonnes

Lors de la personnalisation d’une page, vous utilisez **Ajouter un champ au volet de la page** pour afficher les champs actuellement masqués sur la page. Vous ouvrez ce volet en sélectionnant l’action **+ Champ** en haut de la page. Contrairement à d’autres éléments, les champs masqués ne sont pas indiqués sur la page elle-même en mode personnalisation. Cependant, vous pouvez identifier les champs masqués en utilisant le volet **Ajouter un champ à la page**.

Pour faciliter l’utilisation des champs, voici quelques directives générales à suivre lors de l’utilisation du volet **Ajouter un champ à la page** :

- Par défaut, le volet répertorie tous les champs masqués, qui sont marqués par l’icône [Affiche l’icône du champ masqué](media/hidden-icon.png "Affiche l’icône du champ caché").
- Vous pouvez filtrer la liste pour afficher d’autres champs, comme ceux actuellement affichés sur la page, en sélectionnant le bouton **Champs recommandés** au-dessus de la liste et en choisissant une option de filtre. Le nom du bouton change en fonction de l’option de filtre que vous choisissez.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Affiche le bouton de filtre dans le volet Ajouter un champ en mode personnalisation.":::
- La sélection d’un champ dans la liste met en évidence son emplacement sur la page. Si le champ est actuellement masqué, son emplacement conçu est affiché dans un état ombré. 
- Pour obtenir plus de détails sur un champ de la liste, pointez dessus ou sélectionnez <kbd>Alt</kbd>+<kbd>Flèche vers le haut</kbd> pour afficher une info-bulle.
- Les champs disponibles dans le volet Ajouter un champ à la page sont déterminés par le développeur de la page et de sa table source, ou par un administrateur de profil qui a [personnalisé la page](ui-personalization-manage.md). Vous ne pouvez pas en créer de nouveaux.
- Certaines pages comportent plusieurs champs de page qui correspondent à la même table source. Le volet affiche les deux/tous ces champs de page indépendamment. Afficher/Masquer/déplacer ces champs est également indépendant sans que l’un n’affecte l’autre.


### <a name="make-a-hidden-field-visible"></a>Rendre visible un champ caché

Il existe deux manières d’afficher un champ actuellement masqué sur la page :

- Faites glisser le champ vers la position souhaitée. L’emplacement cible est indiqué par une ligne verticale ou horizontale épaisse.
- Sélectionnez le champ dans la liste, puis accédez au champ ombré de la page et sélectionnez l’option **Afficher**.

## <a name="clear-personalization"></a>Effacer la personnalisation

Vous pouvez souhaiter annuler toutes les modifications de personnalisation apportées à une page au fil du temps.

1. Sur la bannière **Personnalisation**, choisissez l’action **Effacer la personnalisation**.
2. Choisissez l’une des options suivantes.  

> [!CAUTION]
> Il est impossible d’annuler votre action une fois la personnalisation annulée.

|Option|Action|
|------|------------
|**Menu de navigation uniquement**|Efface toutes les modifications de personnalisation que vous avez apportées au menu de navigation partagé entre le tableau de bord et d’autres pages. Ces modifications incluent toutes les nouvelles actions ajoutées en tant que signets et toutes les modifications apportées aux liens et aux groupes dans le menu.|  
|**Actions seules**|Efface toutes les modifications de personnalisation apportées à la barre de navigation ou d’actions sur la page.|
|**Uniquement les champs et les colonnes**|Efface toutes les modifications de personnalisation apportées à la page, hormis les modifications de la barre de navigation ou d’actions. Ces modifications incluent les modifications apportées aux champs, colonnes, parties et mosaïques. |
|**Tous**|Efface toutes les modifications de personnalisation apportées à cette page afin qu’elle retrouve son aspect d’origine. Ces modifications incluent les modifications apportées aux barres de navigation et d’actions, aux champs, colonnes, parties et mosaïques.|

## <a name="tips-and-other-points-of-interest"></a>Conseils et autres points d’intérêts

Pour vous aider à mieux comprendre la personnalisation, voici quelques points clés.

- Lorsque vous apportez des modifications à une page de fiche ouverte à partir d’une liste, les modifications s’appliquent à tous les enregistrements que vous ouvrez à partir de cette liste. Par exemple, disons que vous ouvrez un client spécifique à partir de la page Liste des clients, puis que vous personnalisez cette page en y ajoutant un champ. Lorsque vous ouvrez d’autres clients à partir de la liste, le champ que vous avez ajouté s’affiche également.
- Les modifications que vous apportez s’appliquent à tous vos tableaux de bord. Par exemple, si vous modifiez la liste Clients lorsque le tableau de bord est défini sur Gestionnaire d’activité, vous verrez également la modification de la page **Clients** lorsque le tableau de bord est défini sur Préparateur de commandes vente.
- Les modifications d’une page dans un volet s’appliquent à la page, où qu’elle s’affiche.  
- Vous ne pouvez pas personnaliser une page en [mode d’analyse](analysis-mode.md). Le commutateur **Analyser** est désactivé. Si vous passez en mode personnalisation alors que la page est en mode analyse, le mode analyse est automatiquement désactivé. 
- Certaines pages comportent plusieurs champs de page qui correspondent à la même table source. Le volet affiche les deux/tous ces champs de page indépendamment. Afficher/Masquer/déplacer ces champs est également indépendant sans que l’un n’affecte l’autre.
- Si une pièce ou un groupe est masqué, les champs fantômes s’afficheront toujours à l’intérieur, mais vous ne pouvez pas faire de glisser-déposer ou ajouter/afficher ce champ tant que vous n’avez pas rendu le groupe/la pièce visible.


## <a name="see-also"></a>Voir aussi
[Personnalisation des pages pour les profils](ui-personalization-manage.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
