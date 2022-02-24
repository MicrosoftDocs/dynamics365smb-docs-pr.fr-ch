---
title: Procédure de saisie de données dans Business Central | Microsoft Docs
description: En savoir plus sur les fonctions générales qui vous permettent de saisir les données dans les champs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/03/2020
ms.author: sgroespe
ms.openlocfilehash: f3af601f0de00445a42c88bb47053084b05fc14b
ms.sourcegitcommit: 8a4e66f7fc8f9ef8bdf34595e0d3983df4749376
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262157"
---
# <a name="entering-data"></a>Saisie de données

Plusieurs fonctions générales vous permettent de saisir vos données de manière plus facile, rapide et précise. Les principes de base et les fonctionnalités avancées de saisie de données sont décrites dans cet article.  

Les exemples contenus dans cet article utilisent les données de démonstration.

## <a name="working-with-editable-fields"></a>Utilisation des champs modifiables
Les champs dans [!INCLUDE[d365fin](includes/d365fin_md.md)] peuvent contenir différentes données modifiables, telles que des montants de texte ou de devise. Les champs modifiables affichent généralement une zone de saisie dans laquelle vous pouvez taper ou choisir une valeur. Les champs non modifiables sont généralement affichés sur fond gris.   

Certains champs modifiables fournissent un sélecteur pour vous aider à spécifier une valeur.  

<!-- TODO: Add illustrations or images of each picker -->
|**Employé en charge du prélèvement**        |**Comment cela vous aide à spécifier une valeur**|
|------------------|------------------------------------|
|Sélecteur de date       |Ce sélecteur affiche un calendrier basé sur vos paramètres régionaux actuels. Il vous aide à choisir une date unique.|
|Menu déroulant          |Les listes déroulantes offrent un choix de valeurs fixes ou d'enregistrements de référence d'une autre table|
|Commutateur ou case à cocher|Certains champs offrent un choix simple : valeurs *Oui* ou *Non*. Le commutateur est utilisé pour spécifier cette valeur et est toujours affiché sous forme de case à cocher dans les listes|
|Modification assistée       |Certains champs fournissent des sélecteurs personnalisés adaptés à la recherche et au choix de la meilleure valeur pour ce champ, comme une fenêtre contextuelle|


### <a name="modifying-a-field-value"></a>Modification d'une valeur de champ

Pour modifier la valeur d'un champ, vous devez d'abord définir le focus sur ce champ. Vous définissez le focus en effectuant les actions suivantes :

- Utilisez la touche de **tabulation**. L'action sélectionne la valeur entière.
- Effectuez un clic gauche sur votre souris ou un périphérique d'entrée similaire. Cette action ne sélectionnera la valeur entière du champ que si le champ est dans une liste.  

Lorsque vous interagissez avec des champs de l'interface utilisateur, [!INCLUDE[d365fin](includes/d365fin_md.md)] favorise généralement la sélection de la valeur entière du champ pour faciliter le remplacement de cette valeur.

Lorsque toute la valeur du champ est sélectionnée :
- Remplacez la valeur en tapant simplement pour spécifier une nouvelle valeur. Si le champ propose un sélecteur, vous pouvez l'activer à l'aide du raccourci clavier **Alt + flèche vers le bas**.
- Utilisez la touche **Supprimer** ou **Retour arrière** pour effacer la valeur.

Appuyez sur la touche **F2** entre la sélection de la valeur entière du champ ou le placement du curseur après la valeur du champ. Le fait de placer le curseur à la fin de la valeur facilite l'ajout à la valeur existante.

Lorsque le curseur apparaît à la fin de la valeur du champ :
- Ajout à la valeur par simple saisie.
- Utilisez les touches **Accueil**, **Fin**, **Flèche gauche** et **Flèche droite** pour déplacer le curseur dans la valeur. Si vous modifiez un champ dans une liste, appuyez à nouveau sur la touche **Flèche gauche** lorsque le curseur est au début de la valeur, le focus sera mis sur le champ précédent. De même, en appuyant à nouveau sur la touche **Flèche droite** lorsque le curseur est à la fin de la valeur, le focus sera placé sur le champ suivant.

> [!NOTE]
> Après avoir spécifié une valeur, Business Central vérifie uniquement sa validité après avoir cliqué en dehors du champ ou défini le focus sur un autre article, tel que le champ suivant.  


## <a name="keyboard-shortcuts"></a>Raccourcis clavier

Il existe plusieurs raccourcis clavier qui vous permettent de travailler "sans souris" et d'accélérer la saisie de vos données. Ces raccourcis clavier sont particulièrement utiles avec les entrées à grande échelle et les tâches de frappe répétitives.

Pour plus d'informations sur les raccourcis, reportez-vous à la rubrique [Raccourcis clavier](keyboard-shortcuts.md). Certains raccourcis clavier font l'objet de cet article.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Accélérer la saisie de données à l'aide de la fonction Saisie rapide

La saisie rapide est une fonction conçue pour saisir les données avec le clavier. La fonction Saisie rapide fonctionne sur les champs (comme les pages Fiche) et dans les listes (lignes et colonnes). Cela est avantageux lorsque vous effectuez des tâches de frappe répétitives qui nécessitent de créer plusieurs enregistrements en séquence. Les exemples incluent un lot de commandes vente ou l'enregistrement de nouveaux articles.

Vous pouvez utiliser la touche Tab afin de naviguer d'un champ sur une page au champ suivant modifiable. L'inconvénient de l'utilisation de la touche Tab ? Elle passe toujours de façon séquentielle au champ suivant. <!-- even if the field is non-editable or seldom filled it in.-->La fonction Saisie rapide vous permet de modifier ce chemin d'accès. Avec la fonction Saisie rapide, utilisez la touche Entrée pour naviguer uniquement dans les champs qui vous intéressent. La fonction Saisie rapide ignore les champs non modifiables et les champs que vous ne remplissez généralement pas. Vous avez peut-être déjà remarqué ce comportement sur certaines pages. Ce comportement est dû au fait que les champs à inclure lorsque vous appuyez sur Entrée et ceux à ignorer ont été prédéfinis. Vous pouvez personnaliser la fonction Saisie rapide en personnalisant votre espace de travail et en optimisant la manière dont vous saisissez les données sur chaque page.

### <a name="how-quick-entry-works"></a>Fonction Saisie rapide : fonctionnement

Chaque champ peut être marqué comme *inclus dans la fonction Saisie rapide* ou *exclus de la Saisie rapide*. Les champs inclus dans la fonction Saisie rapide seront inclus dans le chemin lorsque vous appuyez sur Entrée. Les champs exclus de la fonction Saisie rapide ne le seront pas.

Lorsque vous avez fini de saisir les données dans un champ, appuyez simplement sur Entrée pour confirmer les changements et accéder au champ suivant. Si vous souhaitez inverser le sens, et accéder au champ précédent, appuyez sur Maj+Entrée. Pour plus d'informations sur les raccourcis, voir [Raccourcis rapides d'écriture pour les champs](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Conseils

Vous trouverez ci-après les informations utiles concernant la fonction Saisie rapide.

- Elle est disponible pour tout champ modifiable.
- Elle fonctionne également à travers les colonnes et les lignes.
- Elle n'empêche pas d'accéder à d'autres articles d'une page, comme des actions. Ces articles restent accessibles en utilisant la touche Tab et la combinaison des touches Maj+Tab.  
- Il n'est pas nécessaire que les raccourcis soient étendus pour que l'entrée rapide fonctionne. Si le champ suivant Saisie rapide se situe dans un raccourci réduit, ce raccourci développe automatiquement et se concentre sur le champ choisi. [!INCLUDE[d365fin](includes/d365fin_md.md)] se souviendra que le raccourci devrait être développé la prochaine fois que vous visiterez la page.  
- La fonction Saisie rapide fonctionne peu importe si les champs sont obligatoires ou non. Ainsi, il est recommandé de veiller à ce que les champs obligatoires soient inclus dans la fonction Saisie rapide.
- Par défaut, la plupart des champs sont automatiquement inclus dans la fonction Saisie rapide. Ainsi, à la base, il est fort probable que votre tâche exclura les champs de la fonction Saisie rapide.

### <a name="to-change-quick-entry-fields"></a>Pour modifier les champs de saisie rapide

Pour configurer la fonction Saisie rapide sur les champs, vous utilisez la personnalisation.

1. Commencez la personnalisation en sélectionnant l'icône ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez l'action **Personnaliser**.
2. Sélectionnez un champ que vous souhaitez modifier. Dans les listes, sélectionnez l'en-tête de colonne correspondant. Ensuite, choisissez **Inclure dans la saisie rapide** ou **Exclure de la saisie rapide**.

Pour plus d'informations sur la personnalisation, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Champs obligatoires

Lorsque vous entrez des données sur les pages, certains champs sont marqués par un astérisque rouge. L'astérisque rouge signifie que le champ doit être rempli pour effectuer un certain processus. Par exemple, lorsque vous validez une transaction qui utilise la valeur dans le champ.  

Même si un champ est obligatoire, vous n'êtes pas forcé de remplir le champ avant de poursuivre avec les autres champs ou fermer la page. L'astérisque rouge sert uniquement à rappeler que la fin d'un certain processus restera bloquée.  

## <a name="finding-data-as-you-type"></a>Recherche immédiate

 Lorsque vous commencez à taper des caractères dans un champ, une liste déroulante affiche les valeurs de champ possibles. La liste change à mesure que vous tapez des caractères, et vous pouvez sélectionner la valeur correcte lorsqu'elle s'affiche.  

 De nombreux champs ont un bouton de Flèche vers le bas que vous pouvez choisir. sélectionnez la flèche pour obtenir la liste des données disponibles pour le champ. Selon le type de champ, le bouton peut être associé à l'une deux fonctions suivantes :  

-   Liste - Affiche les informations d'une autre table que vous pouvez entrer dans le champ. Vous pouvez sélectionner un élément à la fois.  

-   Consulter - Affiche les options qui existent pour le champ. Vous ne pouvez sélectionner qu'une des options.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>FAQ Copier et coller des champs et des lignes

Vous pouvez copier une ou plusieurs lignes d'une liste ou d'un seul champ sur une page. Collez ensuite ce que vous avez copié dans la même page, une autre page ou un document externe. Vous pouvez, par exemple, collez dans Microsoft Excel ou un e-mail Outlook. En raccourci, pour copier, appuyez sur CTRL+C (cmd+C dans macOS) sur votre clavier. Pour coller, appuyez sur CTRL+V ou cmd+V dans macOS.

Dans une liste, pour copier le champ dans la même colonne de la ligne précédente, et le coller dans la ligne actuelle, il vous suffit d'appuyer sur F8.

Pour plus d'informations, voir [FAQ sur l'opération Copier et coller](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Filtrage des articles de ligne

Pour commencer à filtrer, sélectionnez ![icône de volet Filtre](media/open-filter-pane-icon.png "Icône de volet Filtre") en haut de la liste ou appuyez sur Maj+F3 pour ouvrir le volet Filtre. Vous travaillez avec le volet Filtrer comme vous le faites sur toute autre liste. Pour plus d'informations, reportez-vous à la rubrique [Filtrage](ui-enter-criteria-filters.md#filtering).

La fonction Filtrage est utile notamment pour afficher et analyser de longs documents. Imaginez que vous ouvrez une facture de vente enregistrée. Ensuite, vous filtrez les articles de ligne pour afficher tous les articles de ligne dont la remise individuelle est supérieure à 5 %. Ou, vous filtrez pour afficher uniquement les accessoires de vélo avec "pro" dans le nom.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Se concentrer sur les articles de ligne

Lorsque vous travaillez sur des documents qui comprennent une pièce des articles de ligne, vous pouvez basculer votre vue pour vous concentrer uniquement sur les articles de ligne. Les exemples de documents sont la page de commande client ou de facture. La partie des articles de ligne se développe pour occuper presque tout l'espace de travail. Elle masque les autres parties de la page à l'exception de la zone d'actions en haut. Cette disposition vous donne un meilleur aperçu des articles de ligne et offre un plus grand espace pour les exploiter.

Vous bénéficierez particulièrement lorsque vous travaillez avec de grandes listes d'articles et que vous souhaitez saisir des données rapidement. Cette fonction offre également une capacité de filtrage avancée. Comme sur d'autres listes, la navigation et la recherche dans les articles de ligne deviennent encore plus faciles.

### <a name="switching-the-focus-on-and-off"></a>Activation/Désactivation du focus

Pour vous concentrer sur les articles de ligne, faites votre sélection n'importe où dans la partie des articles de ligne, puis sélectionnez ![icône mode Focalisation](media/focus-mode.png "Icône du mode Focalisation") dans l'angle supérieur droit ou appuyez sur Ctrl+Maj+F12.

Pour revenir à la vue normale, sélectionnez ![icône mode Focalisation](media/focus-mode.png "Icône du mode Focalisation") ou appuyez à nouveau sur Ctrl+Maj+F12.

## <a name="multitasking-across-multiple-pages"></a>Multitâche sur plusieurs pages

Vous pouvez ouvrir une page de carte ou de document dans une nouvelle fenêtre. L'ouverture d'une nouvelle fenêtre vous permet :

- Utiliser plusieurs tâches en même temps
- Gérez les interruptions de la tâche en cours, comme prendre un appel entrant.
- Gardez une fenêtre ouverte pour une tâche en cours pendant que vous démarrez ou terminez une autre tâche dans les fenêtres.

Pour ouvrir la fiche ou le document en cours dans une nouvelle fenêtre, choisissez ![Ouvrir dans une nouvelle fenêtre](media/open-new-window-icon.png "Icône Ouvrir dans une nouvelle fenêtre") dans le coin supérieur droit, ou appuyez sur Alt+Maj+W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Pour ouvrir la fiche ou le document en cours dans une nouvelle fenêtre, choisissez ![Ouvrir dans une nouvelle fenêtre](media/open-new-window-icon.png "Icône Ouvrir dans une nouvelle fenêtre") dans le coin supérieur droit, ou appuyez sur Alt+Maj+W.

> [!NOTE]
> Lorsque vous ouvrez d'autres pages d'une fiche ou d'un document ouvert dans une nouvelle fenêtre, ces pages s'ouvrent dans une nouvelle fenêtre même si vous ne choisissez pas ![Ouvrir dans une nouvelle fenêtre](media/open-new-window-icon.png "Icône Ouvrir dans une nouvelle fenêtre").

> [!NOTE]
> Si vous travaillez dans le navigateur Safari, un bloqueur de fenêtres publicitaires intempestives peut empêcher la nouvelle fenêtre de s'ouvrir. Si tel est le cas, spécifiez l'URL du produit en tant que site Web autorisé. Pour plus d'informations, voir [Modifier les préférences dans Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> La même chose peut se produire dans d'autres navigateurs, tels que Firefox. Pour plus d'informations, voir [Paramètres du bloqueur de fenêtres publicitaires intempestives dans Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Une autre façon d'effectuer plusieurs tâches simultanément consiste à ouvrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sur deux ou plusieurs onglets du navigateur. Pour ce faire, vous devez créer un onglet, puis copier/coller l'URL de l'onglet initial dans le nouvel onglet. Cela crée une session.   

> [!NOTE]
> N'utilisez pas la fonction **Dupliquer** du navigateur pour créer l'onglet : cela peut entraîner des actions sur un onglet pour bloquer des actions sur d'autres onglets, car elles font partie de la même session.

## <a name="entering-quantities-by-calculation"></a>Saisie de quantités par calcul

Lors de la saisie de nombres dans les champs de quantité, tels que le champ **Quantité** d'une ligne feuille article, vous pouvez entrer la formule plutôt que la somme des quantités.  

### <a name="examples"></a>Exemples  

-   Si vous entrez 19+19, le champ est renseigné à l'aide du nombre 38.  

-   Si vous entrez 41-9, le champ est renseigné à l'aide du nombre 32.  

-   Si vous entrez 12*4, le champ est renseigné à l'aide du nombre 48.  

-   Si vous entrez 12/4, le champ est renseigné à l'aide du nombre 3.  

## <a name="entering-negative-numbers"></a>Saisie de chiffres négatifs

Vous pouvez saisir des chiffres négatifs de deux manières. Le numéro -20,5 peut être saisi de la manière suivante :  

-   -20,5  

    Ou
-   20,5-  

 Dans les deux cas, le montant est enregistré comme -20,5.  

 Si le dernier caractère de l'expression est **+** ou **-**, l'expression entière est enregistrée avec ce caractère. Par exemple, **10-20+** aboutira à 10 et non -10.  

## <a name="entering-dates-and-times"></a>Saisie de dates et d'heures

Vous pouvez entrer des dates et des heures dans tous les champs affectés à des dates (champs Date). Vous pouvez saisir les dates avec ou sans séparateurs.

> [!NOTE]  
> Le mode de saisie des dates et heures dépend des paramètres **Région**. Pour plus d'informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Saisie de dates

Vous pouvez utiliser le sélecteur de date pour choisir une date depuis un calendrier, ou vous pouvez saisir les dates manuellement. Cette section offre un bref aperçu de la manière de saisir les dates. Pour plus d'informations, reportez-vous à la rubrique [Utilisation de dates civiles et les heures](ui-enter-date-ranges.md).

Pour la saisie manuelle de la date, saisissez deux, quatre, six ou huit chiffres :  

-   Deux chiffres sont interprétés comme le jour. Il ajoutera le mois et l'année de la date de travail.  

-   Quatre chiffres sont interprétés comme le jour et le mois. Il ajoutera l'année de la date de travail.  

-   Si la date souhaitée se situe entre le 01/01/1930 et le 31/12/2029, entrez l'année à deux chiffres. Sinon, entrez l'année à quatre chiffres.  

Vous pouvez également saisir une date comme un jour de la semaine suivi d'un numéro de semaine. Ou, vous pouvez entrer une année. Par exemple, Lun25 ou lun25 signifie le lundi de la semaine 25.  

Plutôt que de saisir une date spécifique, vous pouvez saisir l'un de ces codes.  

|Code|Résultat|  
|--------------|----------------|  
|a|Spécifie la date du jour (la date système de l'ordinateur).|  
|p|Spécifie une période comptable où p signifie la première période comptable, p2 indique la seconde période comptable, etc. |
|t|Spécifie la date de travail configurée dans l'application. Pour modifier la date de travail, voir [Modification des paramètres de base](ui-change-basic-settings.md). Vous souhaiterez peut-être utiliser une date de travail si vous avez beaucoup de transactions avec une date différente de la date d'aujourd'hui.|
|c|Spécifie que la date après c'est une date de clôture, par exemple C123101.|  

## <a name="entering-times"></a>Saisie des heures

Lorsque vous saisissez des heures, vous pouvez insérer n'importe quel type de séparateur entre les unités, mais cette opération est facultative. Vous n'avez pas besoin d'ajouter la mention « minutes », « secondes » ou « AM/PM ».  

Le tableau suivant répertorie les différents formats de saisie possibles pour les heures, ainsi que leur interprétation.  

|Écriture|Interprétation|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05.5|  
|053005050|05:30:05.05|  

 Saisissez deux chiffres par unité temporelle si vous n'utilisez pas de séparateur.  

## <a name="entering-datetimes"></a>Saisie des dates/heures

Lors de la saisie des dates/heures, vous devez saisir un espace entre la date et l'heure.  

Le tableau suivant répertorie les différents formats de saisie possibles pour les dates/heures, ainsi que leur interprétation.  

|Écriture|Interprétation|  
|---------------|------------------------|  
|`131202` 132455|13/12/02 13:24:55|  
|1-12-02 10|01/12/02 10:00:00|  
|1.12.02 5|01/12/02 05:00:00|  
|1.12.02|01/12/02 00:00:00|  
|11 12|11/mois en cours/année en cours 12:00:00|  
|1112 12|11/12/année en cours 12:00:00|  
|a ou date du jour|date du jour 00:00:00|  
|heure h|date du jour heure réelle|  
|a 10:30|date du jour 10:30:00|  
|a 3:3:3|date du jour 03:03:03|  
|t ou date de travail|date de travail 00:00:00|  
|lu ou lundi|Lundi de la semaine en cours 00:00:00|  
|ma ou mardi|Mardi de la semaine en cours 00:00:00|  
|me ou mercredi|Mercredi de la semaine en cours 00:00:00|  
|je ou jeudi|Jeudi de la semaine en cours 00:00:00|  
|ve ou vendredi|Vendredi de la semaine en cours 00:00:00|  
|sa ou samedi|Samedi de la semaine en cours 00:00:00|  
|di ou dimanche|Dimanche de la semaine en cours 00:00:00|  
|ma 10:30|Mardi de la semaine en cours 10:30:00|  
|ma 3:3:3|Mardi de la semaine en cours 03:03:03|  

## <a name="entering-duration"></a>Saisie des durées

Vous devez saisir les durées sous la forme d'un chiffre suivi d'une unité de mesure.  

Voilà quelques exemples.  

|Durée|Unité**|  
|------------------|-------------------------|  
|2h|2 heures|  
|6h 30m|6 heures 30 minutes|  
|6,5h|6 heures 30 minutes|  
|90m|1 heure 30 minutes|  
|2j 6h 30m|2 jours 6 heures 30 minutes|  
|2j 6h 30m 56s 600ms|2 jours 6 h 30 m 56 s 600 ms|  

 Vous pouvez également saisir un nombre automatiquement converti en durée. Le nombre saisi est converti en fonction de l'unité de mesure par défaut spécifiée pour le champ de durée.  

 Pour connaître l'unité de mesure utilisée pour un champ de durée, saisissez un nombre et observez l'unité de mesure dans laquelle il est converti.  

 Si l'unité est « heures », 5 est converti en 5h.  

## <a name="see-also"></a>Voir aussi  
 [Tri, recherche et filtrage de listes](ui-enter-criteria-filters.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
