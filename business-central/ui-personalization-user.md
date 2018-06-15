---
title: Personnalisation de pages dans Financials | Microsoft Docs
description: "Découvrez comment personnaliser l'interface utilisateur pour l'adapter à votre méthode de travail."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 246e6fa65de1d638715d16ee76c0c60a88c44cec
ms.contentlocale: fr-ch
ms.lasthandoff: 04/18/2018

---
# <a name="personalizing-your-workspace"></a>Personnalisation de votre espace de travail
<!--NAV in the Web client-->
Vous pouvez *personnaliser* votre espace de travail pour l'adapter à vos habitudes et préférences en modifiant les pages afin qu'elles n'affichent que les informations dont vous avez besoin, où vous avez en besoin. Les modifications de personnalisation que vous apportez n'affectent que ce que vous voyez, pas ce que voient les autres utilisateurs.

Selon le type de page et ce qu'elles comportent, vous pouvez :

-   Ajouter, déplacer et supprimer des champs.
-   Ajouter, déplacer et supprimer des colonnes dans une liste.
-   Modifier le volet Figer des colonnes dans une liste. Le volet Figer verrouille une ou plusieurs colonnes du côté gauche de la liste, de sorte qu'elles soient toujours visibles, même lorsque vous faites défiler la liste horizontalement.
-   Ajuster la largeur des colonnes d'une liste.
-   Déplacer et supprimer des piles (mosaïques).
-   Déplacer et supprimer des sections. Les sections sont des subdivisions ou des zones d'une page qui contiennent des éléments comme des champs multiples, une autre page, un graphique, ou des mosaïques.  

## <a name="to-personalize-a-page"></a>Pour personnaliser une page

1. Dans le coin supérieur droit, sélectionnez l'icône ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez **Personnaliser**.

    La bannière **Personnalisation** s'affiche en haut, ce qui indique que vous pouvez commencer à apporter des modifications.

    ![Mode Personnaliser](media/ui_personalize_mode_small.png "Mode Personnaliser")

2.  Accédez à une page à personnaliser.

    Si vous voyez une icône de verrouillage dans la bannière, voir [Pourquoi la page est verrouillée](ui-personalization-locked.md) pour plus de détails.

3.  Pointez sur une zone à personnaliser, comme un champ ou un en-tête de colonne dans la liste. Tout ce que vous pouvez personnaliser est immédiatement mis en évidence avec une flèche ou un contour.
<!--
    -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
    -   If the component is a part, the extent of the part is indicated by a border.
    -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
    -->

4.  Utilisez cette table pour faciliter vos modifications :     <table>
        <tr><th>Ce que vous voulez faire</td><th>Comment procéder</th></tr>
        <tr><td>Déplacer quelque chose, comme un champ, une colonne d'une liste, une mosaïque ou une section</td><td> Pointez n'importe où sur ce que vous souhaitez déplacer, puis faites-le glisser vers son nouvel emplacement. L'emplacement est indiqué par une ligne verticale ou horizontale épaisse.</td></tr>
        <tr><td>Supprimer quelque chose</td><td>Sélectionnez la pointe de flèche, puis sélectionnez <b>Supprimer</b>. </td></tr>
        <tr><td>Ajouter un champ ou une colonne</td><td>Dans la bannière <b>Personnalisation</b>, choisissez <b>Plus</b>, puis sélectionnez <b>Champ</b>.<br /></br>Le volet <b>Ajouter un champ à la page</b> s'ouvre à droite. Il répertorie les champs que vous pouvez ajouter à la page. Les champs marqués comme <b>Placé</b> sont déjà dans la page. Les champs marqués comme <b>Prêt</b> ne sont pas actuellement dans la page.<br /></br>Pour ajouter un champ, faites-le glisser du volet vers l'emplacement que vous souhaitez. L'emplacement est indiqué par une ligne verticale ou horizontale épaisse.</td></tr>
        <tr><td>Modifier le volet Figer d'une liste en d'autres colonnes</td><td>Sélectionnez la pointe de flèche de la colonne que vous souhaitez être la dernière du volet Figer, puis sélectionnez <b>Définir le volet Figer</b>.<br /><br/>Si vous souhaitez rétablir le volet Figer à son emplacement d'origine, sélectionnez la pointe de flèche de la colonne actuelle du volet Figer, puis sélectionnez <b>Effacer le volet Figer</b>. Remarque : vous ne pouvez pas supprimer ce volet Figer d'origine.</td></tr>
        <tr><td>Modification de la largeur d'une colonne</td><td>Dans la ligne d'en-tête de la table, faites glisser la bordure droite de la colonne. <br /><br />Pour optimiser la largeur de colonne en fonction de la plus longue ligne de texte de la colonne, double-cliquez sur la bordure de droite.</td></tr>
      </table>

    > [!IMPORTANT]  
    >   Vous ne pouvez pas modifier une liste celle-ci est affichée en tant que mosaïques. Vous devez d'abord basculer la vue de page en vue de liste en sélectionnant l'icône ![Afficher sous forme de liste](media/ui_show_as_list_icon.png "Afficher sous forme de liste").

5.  Vous pouvez continuer à apporter des modifications sur la même page, ou passer à une autre page. Vos modifications sont automatiquement enregistrées au fur et à mesure. Lorsque vous avez terminé, dans la bannière **Personnalisation**, sélectionnez **Terminée**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Effacer la personnalisation pour rétablir une page à sa disposition initiale
Vous pouvez souhaiter annuler toutes les modifications de personnalisation apportées à une page au fil du temps, afin que cette page reprenne son aspect d'origine. Pour ce faire, dans la bannière **Personnalisation**, sélectionnez **Plus**, puis **Effacer la personnalisation**.

## <a name="personalization-in-detail"></a>Personnalisation en détail
Pour vous aider à mieux comprendre la personnalisation, voici quelques points clés.  
-   Lorsque vous apportez des modifications à une page de fiche ouverte à partir d'une liste, les modifications s'appliquent à tous les enregistrements que vous ouvrez à partir de cette liste. Par exemple, disons que vous ouvrez un client spécifique à partir de la page Liste des clients, puis que vous personnalisez cette page en y ajoutant un champ. Lorsque vous ouvrez d'autres clients à partir de la liste, le champ que vous avez ajouté s'affiche également.
-   Les modifications que vous apportez s'appliquent à tous vos tableaux de bord. Par exemple, si vous modifiez la liste Clients lorsque le tableau de bord est défini sur Gestionnaire d'activité, vous verrez également la modification de la liste Client lorsque le tableau de bord est défini sur Préparateur de commandes vente.
-   Les modifications d'une page dans un volet s'appliquent à la page, où qu'elle s'affiche.  
-   Vous ne pouvez ajouter de champs et de colonnes qu'à partir d'une liste prédéfinie, laquelle est basée sur la page. Vous ne pouvez pas en créer de nouveaux.

## <a name="see-also"></a>Voir aussi
[Gérer la personnalisation](ui-personalization-manage.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des paramètres de base](ui-change-basic-settings.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  

