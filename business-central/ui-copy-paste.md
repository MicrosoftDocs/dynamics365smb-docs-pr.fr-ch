---
title: "Copier et coller des données"
description: "Copier des champs et des lignes depuis des pages Business Central et les coller à d'autres emplacements."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e924eeb10e98b81035837ca498ec4f1a7b28bf60
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---

# <a name="copying-and-pasting-in-included365finincludesd365finmdmd"></a>Copier et coller dans [!INCLUDE[d365fin](includes/d365fin_md.md)]
Vous pouvez copier une ou plusieurs lignes dans une liste ou un champ unique sur une page, puis collez ce que vous avez copié dans la même page, une autre page, ou un document externe (comme Microsoft Excel et un e-mail Outlook). En raccourci, pour copier, appuyez sur CTRL+C (cmd+C dans macOS) sur votre clavier. Pour coller, appuyez sur CTRL+V (cmd+V dans macOS).

Plusieurs autres raccourcis clavier permettent de copier et coller afin de faire gagner du temps pendant la saisie des données. Pour plus d'informations sur ceux-ci, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#CopyRows).

Cet article répond à des questions courantes que vous pouvez avoir à propos de copier et coller.  

## <a name="what-can-i-copy-and-paste"></a>Que puis-je copier et coller ?
-   Copier une ou plusieurs lignes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] vers la même liste, ou dans n'importe quelle liste avec des colonnes identiques.
-   Copier une ou plusieurs lignes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et les collez dans Excel ou d'autres applications.
-   Copier une ou plusieurs lignes dans Excel et les coller dans une liste [!INCLUDE[d365fin](includes/d365fin_md.md)].
-   Copier la valeur d'un champ individuel dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et la collez n'importe où ailleurs.

## <a name="how-do-i-copy-rows"></a>Comment copier des lignes ?
Pour copier une ligne unique, sélectionnez-la, et appuyez sur Ctrl+C.

Pour copier plusieurs lignes, vous pouvez :
-   Appuyer sur Ctrl+clic sur une autre ligne ou appuyer sur Maj+clic pour sélectionner la ligne et toutes les lignes entre les deux. Voir [Raccourcis clavier](keyboard-shortcuts.md#CopyRows) pour plusieurs combinaisons souris et clavier pour sélectionner des lignes.
-   Sélectionnez ![Afficher plus d'options](media/show-more-options-icon.png "icônes Afficher plus d'options") de la première colonne d'une ligne, sélectionnez **Sélectionner davantage**, activez la case à cocher à côté de chaque ligne à copier, puis appuyez sur Ctrl+C.

## <a name="how-do-i-paste-rows"></a>Comment coller des lignes ?
Sélectionnez une ligne vide, puis appuyez sur Ctrl+V. Pour remplacer des lignes existantes, sélectionnez-les et appuyez sur Ctrl+V. Dans ce cas, vous pouvez uniquement coller le même nombre de lignes que vous avez sélectionnées.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email-or-onenote"></a>Puis-je coller des lignes dans un e-mail Outlook ou OneNote ?
Oui. Le collage s'effectue dans un tableau convivial qui conserve l'indentation, l'alignement numérique et les couleurs, tout comme vous le verriez dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="does-copy-and-paste-work-with-tiles"></a>La fonction Copier/Coller fonctionne-t-elle avec des vignettes ?
Non. La liste doit être affichée en tant que lignes (Vue Liste) pour vous effectuer le copier/coller.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>Dans quelles listes puis-je copier et coller des lignes ?
Vous pouvez copier des lignes dans tout type de liste, y compris les feuilles de calcul, les récapitulatifs, ou les listes qui sont incorporées sur une page (telles que les lignes d'une commande vente). Toutefois, pour coller des lignes, la liste doit être modifiable.

Dans certaines pages, la conception de l'application peut vous empêcher de coller des lignes. Contactez votre administrateur ou développeur d'application pour modifier la [propriété modifiable](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) dans la page ou la [propriété PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) du tableau source.

## <a name="on-which-clients-is-copy-and-paste-available"></a>Sur quels clients la fonction Copier/Coller est-elle disponible ?
La fonction Copier/Coller est disponible dans le navigateur ou l'application [!INCLUDE[d365fin](includes/d365fin_md.md)] Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Quel est le nombre maximal de lignes pouvant être copié ?
Vous pouvez copier autant de lignes que vous pouvez faire défiler dans la vue. Par exemple, pour copier 1 000 lignes dans une page, vous devez d'abord faire défiler jusqu'au bas de la page et attendre que les lignes s'affichent avant de les copier. Le nombre maximal de lignes que vous pouvez copier est uniquement limité par la mémoire de votre périphérique.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Dois-je avoir exactement le même nombre de colonnes en collant des lignes ?
Oui. Que vous copiiez depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], d'Excel, ou d'un autre tableau d'origine, les lignes que vous collez doivent avoir les mêmes colonnes correspondantes - ni plus ni moins.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Pourquoi est-ce que j'obtiens des erreurs en collant des lignes ?
Lorsque vous collez dans [!INCLUDE[d365fin](includes/d365fin_md.md)], chaque ligne est vérifiée pour s'assurer que les valeurs de chaque colonne sont valides. Si une colonne contient une valeur qui n'est pas valide, le collage arrêté, et un message d'erreur s'affiche. Pour éviter cela, assurez-vous que les colonnes ont des valeurs valides avant de les coller.


## <a name="see-also"></a>Voir aussi .
[Fonctionnalités d'assistance](ui-accessibility.md)  
[Mise en route](product-get-started.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Forum Aux Questions](across-faq.md)  

