---
title: Fonctionnalités d’assistance
description: "Cet article fournit des informations sur les raccourcis clavier et d’autres fonctionnalités d’assistance dans Business\_Central pour les personnes à mobilité réduite."
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accessibility, shortcuts, charts, tooltips, screen reader'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: jswymer
---
# <a name="accessibility-and-keyboard-shortcuts" />Accessibilité et raccourcis clavier

Cet article fournit des informations sur les fonctionnalités qui rendent [!INCLUDE[prod_short](includes/prod_short.md)] accessible aux personnes handicapées. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les fonctionnalités d’accessibilité suivantes :  

- Raccourcis clavier. Voir [Raccourcis clavier](keyboard-shortcuts.md).
- Gestes tactiles et au stylet sur tablettes et téléphones. Voir [Gestes tactiles et au stylet](touch-gestures.md).
- Navigation  
- En-têtes  
- Texte secondaire pour les images et les liens  
- Prise en charge des technologies d’assistance courantes 
- Zoom avant ou zoom arrière sur n′importe quelle page
- Info-bulles sur les éléments de l′interface utilisateur

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="navigation" /><a name="Navigation"></a> Navigation
  
Vous pouvez utiliser différentes combinaisons des touches Tab, Maj et fléchées du clavier pour vous déplacer entre les éléments d′une page. Les éléments comprennent des actions, des champs et des colonnes, des parties et d′autres commandes. En général, appuyez sur <kbd>Tab</kbd> ou <kbd>Maj</kbd>+<kbd>Tab</kbd> pour passer à l′élément suivant ou précédent.

Si vous vous concentrez sur une zone contenant des actions, comme la barre de navigation en haut du tableau de bord ou la barre d′actions sur les autres pages, utilisez les touches fléchées pour accéder aux différents groupes et actions. Appuyez sur <kbd>Entrée</kbd> sur un groupe pour ouvrir ses actions sous-jacentes, puis continuez à utiliser les touches fléchées. Appuyez sur <kbd>Tab</kbd> ou <kbd>Maj</kbd>+<kbd>Tab</kbd> pour sortir de la zone d′action.

À l’aide de l’ordre de tabulation, vous pouvez également basculer entre la page de navigateur principale et les boîtes de dialogue de demande de confirmation, par exemple, ou la page de première connexion.  

## <a name="headings-in-content" /><a name="Headings"></a> En-têtes dans le contenu

La source HTML du contenu [!INCLUDE[prod_short](includes/prod_short.md)] utilise des balises pour aider les utilisateurs de la technologie d’assistance à comprendre la structure et le contenu de la page. Par exemple, sur les pages de liste, les colonnes sont définies dans les balises TH et les en-têtes de colonne sont définies avec l’attribut TITLE au sein de la balise. Les légendes des éléments, tels que les raccourcis, récapitulatifs et champs sont incluses dans les balises d’en-tête (H1, H2, H3 et H4).  

## <a name="image-and-links" /><a name="Images"></a> Image et liens

Un texte descriptif pour les images est défini avec l’attribut ALT au sein de la balise IMG. Un texte descriptif pour les liens hypertexte est défini avec l’attribut title au sein de la balise A.  

## <a name="assistive-technologies" /><a name="AssistiveTech"></a> Technologies d’assistance

[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge différentes technologies d’assistance, telles que le contraste élevé, les lecteurs d’écran et les logiciels de reconnaissance vocale. Certaines technologies d’assistance ne fonctionnent pas correctement avec certains éléments des pages [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="zoom" /><a name="zoom"></a> Zoom

La plupart des navigateurs utilisent des raccourcis clavier standard pour effectuer un zoom avant et arrière sur la page en cours. Ces raccourcis clavier ne sont pas spécifiques à [!INCLUDE [prod_short](includes/prod_short.md)] mais ils fonctionnent lorsque vous utilisez [!INCLUDE [prod_short](includes/prod_short.md)] dans un navigateur. Pour obtenir la liste des raccourcis clavier pris en charge, voir [Raccourcis clavier pour le zoom avant et arrière](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips" />Info-bulles

Les info-bulles sont disponibles sur la plupart des éléments de l′interface utilisateur, tels que les champs et les colonnes de page, les actions, les mosaïques de piles et les graphiques. Une info-bulle fournit un texte supplémentaire qui explique un élément pour vous aider à mieux comprendre son objectif. 

Les info-bulles sont accessibles de différentes manières, en fonction du client (Web ou mobile) et de l′appareil que vous utilisez. Utilisez le tableau suivant comme référence. Certaines info-bulles peuvent être lues par les lecteurs d′écran. Dans ce cas, vous accédez aux info-bulles comme décrit dans le tableau, puis utilisez le lecteur d′écran pour accéder à l′info-bulle comme vous le feriez avec tout autre élément.

#### <a name="accessing-tooltips" />Accès aux info-bulles

|Élément|Action de la souris pour le client Web|Raccourci clavier pour le client Web|Geste tactile sur tablette/téléphone pour application mobile|Prise en charge du lecteur d′écran|
|-------|-----------------|------------|--------------------------|---------------------|
|Champs de page et en-têtes de colonne|Survoler ou cliquer sur la légende du champ ou l′en-tête de colonne|Déplacer le focus sur l′en-tête du champ ou de la colonne, puis appuyer sur les touches <kbd>Alt</kbd>+<kbd>Flèche vers le haut</kbd>|Appuyer sur la légende du champ |oui|
|Éléments des graphiques, comme une barre, une ligne, un secteur|Survoler l′élément|Déplacer le focus sur l′élément, par exemple, à l′aide des touches fléchées|Appuyer longuement sur l′élément|oui|
|Actions|Survoler l′action|aucun|aucun |non|
|Mosaïques de piles|Survoler la vignette |aucun|aucun|non|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information" />Informations supplémentaires sur l’accessibilité

Vous trouverez des informations supplémentaires sur l’accessibilité des produits Microsoft et les technologies d’assistance sur le site [Accessibilité Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).

## <a name="see-also" />Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Forum Aux Questions](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
