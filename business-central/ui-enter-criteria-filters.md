---
title: Tri, recherche et filtrage de listes | Microsoft Docs
description: "Travaillez efficacement dans les listes en parcourant toutes vos données, en triant les colonnes, et en affinant les résultats en utilisant des symboles de filtre et des raccourcis clavier puissants."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: c6eb9465d07b702e545347cad5acf0a42f01d1de
ms.contentlocale: fr-ch
ms.lasthandoff: 01/22/2019

---
# <a name="sorting-searching-and-filtering-lists"></a>Tri, recherche et filtrage de listes
Il existe quelques fonctions que vous pouvez utiliser pour vous aider à analyser, rechercher et limiter des enregistrements d'une liste. Ce sont notamment le tri, la recherche et le filtrage. Vous pouvez en appliquer certaines ou toutes simultanément pour trouver rapidement ou analyser vos données.

> [!TIP]
> En affichant vos données en tant que vignettes, vous pouvez rechercher et utiliser le filtrage de base. Pour utiliser l'ensemble complet de puissantes fonctions de tri, de recherche et de filtrage, choisissez l'icône ![Afficher comme liste](media/ui_show_as_list_icon.png "Flèche vers la gauche Afficher comme liste") pour afficher sous forme de liste.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Tri
Le tri vous permet d'avoir facilement un aperçu de vos données. Si vous avez de nombreux clients, par exemple, vous pouvez choisir de les trier par **N° client**, **Groupe compta. client**, **Code devise**, **Code pays/région** ou **N° d'enregistrement Sales Tax** pour obtenir l'aperçu que vous souhaitez.

Pour trier une liste, vous pouvez choisir un texte d'en-tête de colonne pour permuter entre l'ordre croissant et décroissant, ou cliquer sur la petite flèche vers le bas dans l'en-tête de colonne et choisir **Croissant** ou **Décroissant**.  

> [!NOTE]  
>   Le tri n'est pas pris en charge sur les images, les champs de type BLOB, les FlowFilters, et les champs n'appartenant pas à une table.  

## <a name="searching"></a>Recherche
<!--## Searching by using the Quick Filter --> En haut de chaque page de liste, il existe une icône ![Rechercher une liste](media/ui-search/search-list.png "icône Rechercher une liste") **Rechercher** qui fournit une manière rapide et facile de réduire les enregistrements en une liste et d'afficher uniquement les enregistrements qui contiennent les données que vous souhaitez afficher.

Pour rechercher, sélectionnez simplement l'icône de recherche, puis dans la case, entrez le texte souhaité. Vous pouvez saisir des lettres, des chiffres et d'autres symboles.

### <a name="fine-tune-the-search"></a>Affiner la recherche
Généralement, la recherche tente de mettre en correspondance le texte entre tous les champs ; elle ne distingue pas les minuscules et les majuscules (en d'autres termes, ne respecte pas la casse), puis met en correspondance le texte placé n'importe où dans le champ (au début, à la fin, ou au milieu).

Cependant, vous pouvez faire une recherche plus précise en utilisant les caractères spéciaux suivants :

- Pour rechercher uniquement des valeurs de champ correspondant à tout le texte et à la casse, positionnez le texte de recherche entre apostrophes `''` (par exemple, `'man'`).

- Pour rechercher des valeurs de champ qui commencent par un certain texte et correspondant à la casse, placez `*` après le texte de recherche (par exemple, `man*`).

- Pour rechercher des valeurs de champ qui finissent par un certain texte et correspondant à la casse, placez `*` avant le texte de recherche (par exemple, `*man`).

- Lorsque vous utilisez `''` ou `*` la recherche respecte la casse. Si vous souhaitez que la recherche ne respecte pas la casse, placez `@` avant le texte de recherche (par exemple `@man*`).

Le tableau suivant fournit des exemples expliquant comment vous pouvez utiliser la recherche.


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|Critères de recherche|Résultat…|
|---------------|----------|
|`man`<br />ou <br />`Man`|Tous les enregistrements avec des champs contenant le texte **man**, quelle que soit la casse. Par exemple, **Manchester**, **manuel** ou **Sportsman**. |
|`'Man'`|Tous les enregistrements avec des champs contenant uniquement **man**, avec la casse correspondante.|
|`Man*`|Tous les enregistrements commençant par le texte <b>Man</b>, avec la casse correspondante. Par exemple, **Manchester**, mais pas **manuel** ni **Sportsman**.|
|`@Man*`|Tous les enregistrements commençant par **man**, quelle que soit la casse. Par exemple, **Manchester** et **manuel** mais pas **Sportsman**.|
|`@*man`|Tous les enregistrements finissant par **man**, quelle que soit la casse. Par exemple, **Sportsman**, mais pas **Manchester** ni **manuel**.|

> [!TIP]
> Vous pouvez appuyer sur F3 pour activer et désactiver la zone de recherche. Pour plus d'informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#KeyboardFilter).

## <a name="filtering"></a>Filtrage
Le filtrage fournit une manière plus avancée et plus souple de contrôler les enregistrements affichés dans une liste. Il existe deux différences majeures entre rechercher et filtrer, comme décrit dans le tableau ci-dessous.

|| **Recherche** | **Filtrage** |
|--|----------|------------|
| **Champs applicables** | Les recherches entre tous les champs visibles sur la page. | Filtre un ou plusieurs champs individuellement, en sélectionnant parmi tous les champs de la table, y compris les champs qui ne sont pas visibles dans la page. |
| **Correspondance** | Affiche les enregistrements avec des champs correspondants au texte de recherche, indépendamment de la casse ou de l'emplacement de ce texte. | Affiche les enregistrement dont le champ correspond exactement au filtre et respecte la casse, sauf si des symboles de filtre spéciaux sont renseignés.

Le filtrage vous permet de visualiser des enregistrements pour des comptes ou les clients, des dates, des montants, ainsi que d'autres informations spécifiques en spécifiant des critères du filtre. Seuls les enregistrements correspondant aux critères sont affichés. Si vous spécifiez des critères pour plusieurs champs, seuls les enregistrements correspondant à tous les critères sont affichés.

### <a name="working-in-the-filter-pane"></a>Utilisation du volet Filtre
Le volet Filtre affiche les filtres actuels de la liste, et permet de définir vos propres filtres personnalisés sur un ou plusieurs champs. La figure ci-après indique un exemple de volet Filtre d'une liste des devis.

![Aperçu du volet Filtre](media/filter-pane-overview.png "Icône de filtre")

Pour afficher le volet Filtre, utilisez le raccourci clavier **Shift+F3**. Pour les listes dans le tableau de bord, vous pouvez également choisir la flèche vers le bas en regard du titre de la page dans la barre de navigation au-dessus de la liste, puis choisir **Afficher le volet Filtre**.

![Afficher le volet filtre](media/open-filter-pane.png "Afficher le volet filtre")

Un volet filtre est divisé en trois sections : **Vues**, **Filtrer la liste par** et **Filtrer les totaux** :

- **Vues**

  Certaines listes incluent la section **Vues**. Les vues sont des variations de la liste qui ont été préconfigurées avec les filtres. Pour passer à une autre vue de votre liste, sélectionnez simplement un autre lien. Vous pouvez modifier temporairement les filtres d'une vue, mais les modifications ne seront pas enregistrés de manière permanente.

- **Filtrer la liste par**

  La section **Filtrer la liste par** vous permet d'ajouter des filtres sur des champs spécifiques pour réduire le nombre d'enregistrements affichés. Pour ajouter un filtre, sélectionnez **+ Filtre**, sélectionnez le champ que vous souhaitez filtrer de n'importe quel champ dans la table, puis entrez les critères du filtre dans la zone.

- **Filtrer les totaux par**

  Certaines listes qui affichent des champs calculés, comme des montants et des quantités, incluent la section **Filtrer les totaux par** où vous pouvez ajuster les différents axes qui ont une incidence sur les calculs. Par exemple, vous pouvez analyser rapidement votre plan comptable en filtrant les montants selon une période spécifique, ou vous pouvez afficher les totaux des commandes vente uniquement pour un entrepôt spécifique.

  Pour ajouter un filtre, sélectionnez **+ Filtre**, sélectionnez l'un des axes prédéfinis, puis ajoutez les critères de filtre dans la zone.

  > [!NOTE]
  > Les filtres de la section **Filtrer les totaux par** sont contrôlés par les FlowFilters sur la conception de page. Pour des informations techniques, voir [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Saisie de critères de filtre dans le volet Filtre
Pour sélectionner un champ à filtrer, procédez comme suit :
  - Dans le volet Filtre, choisissez **+ Champ**. Saisissez le nom du champ à filtrer, ou choisissez un champ dans le menu qui affiche tous les champs de la table.

  - Dans l'en-tête de colonne, choisissez la flèche vers le bas, choisissez **Filtrer...**. Le volet Filtre s'affiche et ajoute la colonne au volet Filtre.

Vous pouvez maintenant saisir ou sélectionner vos critères de filtre dans la zone. Le type de champ à filtrer détermine les critères que vous pouvez entrer. Par exemple, filtrer un champ avec des valeurs fixes vous permet uniquement de choisir parmi ces valeurs. Pour plus d'informations sur les symboles de filtre spéciaux, consultez [Critères de filtre](#FilterCriteria) et [Jetons de filtre](#FilterTokens).

Les colonnes qui ont déjà des filtres sont indiquées par l'![Icône de filtre](media/ui-search/filter-icon.png "Icône de filtre") dans l'en-tête de colonne. Pour supprimer un filtre, sélectionnez l'en-tête de colonne, puis choisissez **Effacer le filtre**.


### <a name="entering-filter-criteria-without-the-filter-pane"></a>Saisie de critères de filtre sans le volet Filtre
Vous pouvez spécifier des filtres simples directement dans la liste sans utiliser le volet Filtre.
Avec un champ sélectionné sur une ligne, utilisez le raccourci clavier **Alt+F3** pour afficher uniquement les enregistrements ayant la même valeur. Vous pouvez ensuite sélectionner un autre champ et utiliser le même raccourci pour continuer d'affiner vos filtres. Si le champ sélectionné est déjà filtré, utiliser **Alt+F3** effacera ce filtre.

> [!TIP]
> Accélérez la recherche et l'analyse de vos données en utilisant des combinaisons des raccourcis clavier. Par exemple, sélectionnez un champ, utilisez **Maj+Alt+F3** pour ajouter ce champ au volet Filtre, saisissez les critères de filtre, utilisez **Ctrl+Entrée** pour revenir aux lignes, sélectionnez un autre champ, puis utilisez **Alt+F3** pour filtrer selon cette valeur.
Pour plus d'informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Critères et symboles de filtre
Lorsque vous saisissez des critères, vous pouvez utiliser tous les chiffres et toutes les lettres que vous utilisez habituellement dans ce champ. En plus, vous pouvez utiliser des symboles spéciaux pour filtrer davantage les résultats. Les tables suivantes indiquent les symboles qui peuvent être utilisés dans les filtres. Pour les dates et heures, vous pouvez également vous référer à [Utilisation de dates civiles et les heures](ui-enter-date-ranges.md) pour des informations plus détaillées.

> [!IMPORTANT]  
>  Il peut y avoir des instances où les valeurs de champ contiennent ces symboles et vous souhaitez les filtrer. Pour ce faire, vous devez inclure l'expression de filtre qui contient le symbole entre guillemets ("). Par exemple, si vous souhaitez filtrer les enregistrements commençant par le texte *S&R*, l'expression de filtre est `'S&R*'`.  

### <a name="-interval"></a>(..) Intervalle

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`1100..2100`|Numéros de 1100 à 2100|  
|`..2500`|Jusqu'à 2500 inclus|  
|`..12 31 00`|Dates jusqu'au 31/12/00 compris|  
|`P8..`|Informations sur la période comptable 8 et les suivantes|  
|`..23`|Antérieur au 23/mois en cours/année en cours 23:59:59|  
|`23..`|Postérieur au 23/mois en cours/année en cours 0:00:00|  
|`22..23`|Entre le 22/mois en cours/année en cours 0:00:00 et le 23/mois en cours/année en cours 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Et/ou  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`1200|1300`|Numéros incluant 1200 ou 1300|  

### <a name="-not-equal-to"></a>(<>) Différent de  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`<>0`|Tous les numéros à l'exception de 0<br /><br /> La version SQL Server vous permet de combiner ce symbole avec une expression de caractères génériques. Par exemple, <>A* signifie différent de tout texte commençant par A.|  

### <a name="-greater-than"></a>(>) Supérieur à  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`>1200`|Numéros supérieurs à 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Supérieur ou égal à  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`>=1200`|Numéros supérieurs ou égaux à 1200|  

### <a name="-less-than"></a>(<) Inférieur à  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`<1200`|Numéros inférieurs à 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Inférieur ou égal à  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`<=1200`|Numéros inférieurs ou égaux à 1200|  

### <a name="-and"></a>(&) Et  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`>200&<1200`|Nombres supérieurs à 200 et inférieurs à 1200|  

### <a name="-an-exact-character-match"></a>(") Correspondance exacte de caractères  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`'man'`|Texte qui correspond exactement à man et qui respecte la casse.|  

### <a name="-case-insensitive"></a>(@) Non-respect de la casse  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`@man*`|Texte qui commence par man et qui ne respecte pas la casse.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un chiffre quelconque ou des caractères inconnus

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`*Co*`|Texte qui contient « Co » et respecte la casse.|  
|`*Co`|Texte qui se termine par « Co » et respecte la casse.|  
|`Co*`|Texte qui commence par « Co » et respecte la casse.|  

> [!NOTE]  
>   Vous ne pouvez pas utiliser `*` lors du filtrage des champs (énumération) d'option, tels que le champ **Statut** sur les commandes vente. Pour entrer un filtre pour ce type de champ, vous pouvez saisir la valeur numérique comme paramètre de filtre. Par exemple, dans le champ **Statut** sur une commande vente qui a les valeurs **Ouvert**, **Lancé**, **Approbation suspendue** et **Acompte suspendu**, utilisez les valeurs `0`, `1`, `2` et `3` pour filtrer ces options.

### <a name="-one-unknown-character"></a>(?) Un caractère inconnu  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`Hans?n`|Texte tel que Hansen ou Hanson|  

### <a name="combined-format-expressions"></a>Expressions de format combinées  

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Inclure tous les enregistrements ayant pour numéro 5999 ou un numéro de l'intervalle 8100 à 8490.|  
|`..1299|1400..`|Inclure tous les enregistrements qui portent un numéro inférieur ou égal à 1299 ou un numéro supérieur ou égal à 1400 (tous les numéros sauf ceux compris entre 1300 et 1399).|  
|`>50&<100`|Inclure les enregistrements qui portent un numéro supérieur à 50 et inférieur à 100 (numéros 51 à 99).|  


## <a name="FilterTokens"> </a>Jetons de filtre
En saisissant des critères de filtre, vous pouvez également saisir des mots avec un sens particulier, appelés des jetons de filtre. Après avoir saisi le mot de jeton, le mot est remplacé par la ou les valeurs qu'il représente. Cela facilite le filtrage en réduisant la nécessité de naviguer vers d'autres pages pour rechercher des valeurs à ajouter à votre filtre. Les tableaux ci-après décrivent certains des jetons que pouvez saisir comme critères de filtre.

> [!TIP]
> Votre organisation peut utiliser des jetons personnalisés. Pour faire en savoir plus sur l'ensemble complet de jetons disponibles pour vous ou pour ajouter des jetons personnalisés supplémentaires, parlez à votre administrateur. Pour des informations techniques, voir [Ajout de jetons de filtre](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)


### <a name="me-or-userid-records-assigned-to-you"></a>Enregistrements (%me ou %userid) qui vous sont attribués

Utilisez `%me` ou `%userid` en filtrant les champs qui contiennent le code utilisateur, par exemple le champ **Affecté au code utilisateur**, pour afficher tous les enregistrements qui vous sont affectés.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%me`<br />ou<br />`%userid`|Enregistrements affectés à votre compte d'utilisateur. |  

### <a name="mycustomers-customers-in-my-customers"></a>Clients (%mycustomers) dans Mes clients

Utilisez `%mycustomers` dans le champ **N°** client pour afficher tous les enregistrements des clients inclus dans la liste **Mes clients** de votre tableau de bord.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%mycustomers`|Clients dans **Mes clients** de votre tableau de bord. |  

### <a name="myitems-items-in-my-items"></a>Articles (%myitems) dans Mes articles

Utilisez `%myitems` dans le champ **N°** article pour afficher tous les enregistrements des articles inclus dans la liste **Mes articles** de votre tableau de bord.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%myitems`|Articles dans **Mes articles** de votre tableau de bord. |  

### <a name="myvendors-vendors-in-my-vendors"></a>Fournisseurs (%myvendors) dans Mes fournisseurs

Utilisez `%myvendors` dans le champ **N°** fournisseur pour afficher tous les enregistrements des fournisseur inclus dans la liste **Mes fournisseur** de votre tableau de bord.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%myvendors`|Fournisseurs dans **Mes fournisseurs** de votre tableau de bord. |  


## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Questions courantes à propos de la recherche et du filtrage](ui-search-filter-faq.md)

