---
title: 'Tri, recherche et filtrage de listes'
description: 'Travaillez efficacement dans les listes en parcourant toutes vos données, en triant les colonnes, et en affinant les résultats en utilisant des symboles de filtre et des raccourcis clavier.'
author: jswymer
ms.author: jswymer
ms.topic: conceptual
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 02/20/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="sorting-searching-and-filtering"></a>Tri, recherche et filtrage

Il existe quelques fonctions que vous pouvez utiliser pour vous aider à analyser, rechercher et limiter des enregistrements d’une liste ou dans un état ou un XMLport. Il s’agit notamment du tri, de la recherche et du filtrage. Vous pouvez en appliquer certaines ou toutes simultanément pour trouver rapidement ou analyser vos données.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Pour les états et les XMLports, comme sur des listes, vous pouvez définir des filtres pour délimiter les données à inclure dans l’état ou le XMLport, mais vous ne pouvez pas trier et rechercher.

> [!TIP]
> En affichant vos données en tant que vignettes, vous pouvez rechercher et utiliser le filtrage. Pour utiliser l’ensemble complet de puissantes fonctions de tri, de recherche et de filtrage, choisissez l’icône ![Afficher sous forme de liste.](media/ui_show_as_list_icon.png "Afficher sous forme de liste") pour afficher les enregistrements sous forme de liste.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Tri

Le tri vous permet d’avoir facilement un aperçu de vos données. Par exemple, si vous avez de nombreux clients, vous pouvez choisir de les trier par **N° client**, **Code devise**, **Code pays/région** pour obtenir l’aperçu que vous souhaitez.

Pour trier une liste, vous pouvez soit :

- Choisir un texte d’en-tête de colonne pour basculer entre l’ordre croissant et décroissant, ou
- Choisir la flèche déroulante dans l’en-tête de colonne, puis choisir le **Croissant** ou **Décroissant**.  

> [!NOTE]  
> Le tri n’est pas pris en charge sur les images, les champs de type BLOB, les FlowFilters, et les champs n’appartenant pas à une table.  

## <a name="searching"></a>Recherche

<!--## Searching by using the Quick Filter -->
En haut de chaque page de liste, il y a une ![liste de recherche.](media/ui-search/search-list.png "Icône de liste Rechercher") action **Rechercher** qui fournit une manière rapide et facile de réduire les enregistrements d’une liste et d’afficher uniquement les enregistrements qui contiennent les données que vous souhaitez afficher.

Pour rechercher, sélectionnez simplement l’action **Rechercher**, puis dans la case, entrez le texte souhaité. Vous pouvez saisir des lettres, des chiffres et d’autres symboles.

Généralement, la recherche tente de mettre en correspondance le texte entre tous les champs. Elle ne distingue pas les minuscules et les majuscules (en d’autres termes, ne respecte pas la casse), puis met en correspondance le texte placé n’importe où dans le champ (au début, à la fin, ou au milieu).

> [!TIP]
> Vous pouvez sélectionner <kbd>F3</kbd> pour activer et désactiver la zone de recherche. Pour plus d’informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> La recherche ne correspondra pas aux valeurs des images, des champs de type BLOB, des FlowFilters, et des autres champs n’appartenant pas à une table.


### <a name="fine-tuning-the-search-with-filter-criteria"></a>Affiner la recherche avec des critères de filtre

Vous pouvez effectuer une recherche plus précise en utilisant des opérateurs de filtre, des expressions et des jetons de filtre. Contrairement au filtrage, ceux-ci sont appliqués à tous les champs lorsqu’ils sont utilisés dans la zone de recherche, ce qui les rend moins efficaces que le filtrage.

- Pour rechercher uniquement des valeurs de champ correspondant à tout le texte et à la casse, positionnez le texte de recherche entre apostrophes `''` (par exemple, `'man'`).

- Pour rechercher des valeurs de champ qui commencent par un certain texte et correspondant à la casse, placez `*` après le texte de recherche (par exemple, `man*`).

- Pour rechercher des valeurs de champ qui finissent par un certain texte et correspondant à la casse, placez `*` avant le texte de recherche (par exemple, `*man`).

- Lorsque vous utilisez `''` ou `*`, la recherche respecte la casse. Si vous souhaitez que la recherche ne respecte pas la casse, placez `@` avant le texte de recherche (par exemple `@man*`).

Le tableau suivant fournit des exemples expliquant comment vous pouvez utiliser la recherche.

|Critères de recherche|Résultat…|
|---------------|----------|
|`man`<br />ou <br />`Man`|Tous les enregistrements avec des champs contenant le texte **man**, quelle que soit la casse. Par exemple, **Manchester**, **manuel** ou **Sportsman**. |
|`'Man'`|Tous les enregistrements avec des champs contenant uniquement **man**, avec la casse correspondante.|
|`Man*`|Tous les enregistrements commençant par le texte <b>Man</b>, avec la casse correspondante. Par exemple, **Manchester**, mais pas **manuel** ni **Sportsman**.|
|`@Man*`|Tous les enregistrements commençant par **man**, quelle que soit la casse. Par exemple, **Manchester** et **manuel** mais pas **Sportsman**.|
|`@*man`|Tous les enregistrements finissant par **man**, quelle que soit la casse. Par exemple, **Sportsman**, mais pas **Manchester** ni **manuel**.|


## <a name="filtering"></a><a name="filtering"></a>Filtrage

Le filtrage fournit une manière plus avancée et plus souple de contrôler les enregistrements affichés dans une liste ou à inclure dans un état ou un XMLport. Il existe deux différences majeures entre rechercher et filtrer, comme décrit dans le tableau ci-dessous.

|| **Recherche** | **Filtrage** |
|--|----------|------------|
| **Champs applicables** | Les recherches entre tous les champs visibles sur la page. | Filtre un ou plusieurs champs individuellement, en sélectionnant parmi tous les champs de la table, y compris les champs qui ne sont pas visibles dans la page. |
| **Correspondance** | Affiche les enregistrements avec des champs correspondants au texte de recherche, indépendamment de la casse ou de l’emplacement de ce texte. | Affiche les enregistrements dont le champ correspond exactement au filtre et respecte la casse, sauf si des symboles de filtre spéciaux sont renseignés.

Le filtrage vous permet de visualiser des enregistrements pour des comptes ou les clients, des dates, des montants, ainsi que d’autres informations spécifiques en spécifiant des critères du filtre. Seuls les enregistrements correspondant aux critères sont affichés dans la liste ou inclus dans l’état, le traitement par lots ou XMLport. Si vous spécifiez des critères pour plusieurs champs, seuls les enregistrements correspondant à tous les critères sont affichés.

Pour les listes, les filtres sont affichés dans un volet Filtre qui apparaît à gauche de la liste lorsque vous l’activez. Pour les états, les traitements par lots et les XMLports, les filtres sont visibles directement sur la page de demande.

### <a name="filtering-with-option-fields"></a>Filtrage avec des champs d’option

Pour les champs « ordinaires » contenant des données, une date de configuration ou des données métier, vous pouvez définir des filtres en sélectionnant des données et en tapant des valeurs de filtre. Vous pouvez également utiliser des symboles pour définir des critères de filtrage avancés. Pour plus d’informations, voir [Saisie de critères de filtre](ui-enter-criteria-filters.md#entering-filter-criteria).

Pour les champs de type **Option**, toutefois, vous ne pouvez définir un filtre qu’en sélectionnant une ou plusieurs options dans une liste déroulante des options disponibles. Parmi les exemples de champ d’option, on trouve le champ **Statut** de la page **Commandes vente**.

> [!NOTE]
> Lorsque vous sélectionnez plusieurs options en tant que valeur de filtre, la relation entre les options est définie comme *OU*. Par exemple, si vous cochez les deux cases **Ouvert** et **Lancé** dans le champ de filtre **Statut** sur la page **Commande vente**, cela signifie que les commandes vente ouvertes ou validées sont affichées.

### <a name="setting-filters-on-lists"></a>Définition de filtres sur les listes

Sur les listes, vous devez définir les filtres à l’aide du volet Filtre. Pour afficher le volet Filtre d’une liste, choisissez la flèche déroulante en regard du nom de la page, puis choisissez l’action **Afficher le volet Filtre**. Vous pouvez également sélectionner <kbd>Maj</kbd>+<kbd>F3</kbd>.

Pour afficher le volet Filtre d’une colonne d’une liste, choisissez la flèche déroulante, puis choisissez l’action **Filtre**. Vous pouvez également sélectionner <kbd>Maj</kbd>+<kbd>F3</kbd>. Le volet Filtre s’ouvre avec la colonne sélectionnée affichée sous forme de champ de filtre dans la section **Filtrer la liste par**.

Le volet Filtre affiche les filtres actuels de la liste, et permet de définir vos propres filtres personnalisés sur un ou plusieurs champs en choisissant l’action **+ Filtre**.

 Un volet filtre est divisé en trois sections : **Vues**, **Filtrer la liste par** et **Filtrer les totaux** :

- **Vues**

  Certaines listes incluent la section **Vues**. Les vues sont des variations de la liste qui ont été préconfigurées avec les filtres. Vous pouvez définir et enregistrer autant de vues que vous le souhaitez par liste. Les vues seront disponibles sur n’importe quel appareil auquel vous vous connectez. Pour plus d’informations, voir [Enregistrer et personnaliser les vues de liste](ui-views.md).

- **Filtrer la liste par**

  Cette section vous permet d’ajouter des filtres sur des champs spécifiques pour réduire le nombre d’enregistrements affichés. Pour ajouter un filtre, choisissez l’action **+ Filtre**. Puis, tapez le nom du champ pour lequel vous souhaitez filtrer la liste ou choisissez un champ dans la liste déroulante.

- **Filtrer les totaux par**

  Certaines listes qui affichent des champs calculés, comme des montants et des quantités, incluent la section **Filtrer les totaux par** où vous pouvez ajuster les différents axes qui ont une incidence sur les calculs. Pour ajouter un filtre, choisissez l’action **+ Filtre**. Puis, tapez le nom du champ pour lequel vous souhaitez filtrer la liste ou choisissez un champ dans la liste déroulante.

  > [!NOTE]
  > Les filtres de la section **Filtrer les totaux par** sont contrôlés par les FlowFilters sur la conception de page. Pour des informations techniques, voir [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Vous pouvez définir un filtre simple directement sur une liste à l’aide du volet Filtre, à savoir un filtre qui n’affiche que les enregistrements ayant la même valeur que dans la cellule sélectionnée. Sélectionnez une cellule dans la liste, choisissez la flèche déroulante, puis choisissez l’action **Filtrer sur cette valeur**. Vous pouvez également sélectionner <kbd>Alt</kbd>+<kbd>F3</kbd>.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Définition de filtres dans les états, les traitements par lots et les XMLports

Pour les états et les XMLports, les filtres sont visibles directement sur la page de demande. La page de demande affiche les derniers filtres utilisés en fonction de votre sélection dans le champ **Utiliser les valeurs par défaut de**. Pour plus d’informations, voir [Utiliser des paramètres enregistrés](ui-work-report.md#SavedSettings).

La section **Filtre** principale affiche les champs de filtre par défaut que vous utilisez pour délimiter les enregistrements à inclure dans l’état ou le XMLport. Pour ajouter un filtre, choisissez l’action **+ Filtre**. Puis, tapez le nom du champ pour lequel vous souhaitez filtrer la liste ou choisissez un champ dans la liste déroulante.

Dans la section **Filtrer les totaux par**, vous pouvez ajuster diverses dimensions qui influencent les calculs dans l’état ou le XMLport. Pour ajouter un filtre, choisissez l’action **+ Filtre**. Puis, tapez le nom du champ pour lequel vous souhaitez filtrer la liste ou choisissez un champ dans la liste déroulante.

## <a name="entering-filter-criteria"></a>Saisie des critères de filtre

Dans le volet Filtre et sur une page de demande, vous devez entrer vos critères de filtrage dans la zone située sous le champ Filtre.

Le type de champ à filtrer détermine les critères que vous pouvez entrer. Par exemple, filtrer un champ avec des valeurs fixes vous permet uniquement de choisir parmi ces valeurs. Pour plus d’informations sur les symboles de filtre spéciaux, consultez [Critères de filtre](#FilterCriteria) et [Jetons de filtre](#FilterTokens).

Les colonnes qui ont déjà des filtres sont signalées par l’![Icône de filtre](media/ui-search/filter-icon.png "Icône de filtre"). dans l’en-tête de la colonne. Pour supprimer un filtre, choisissez la flèche déroulante du titre de la page, puis choisissez l’action **Effacer le filtre**.

> [!TIP]
> Accélérez la recherche et l’analyse de vos données en utilisant des combinaisons des raccourcis clavier. Par exemple, sélectionnez un champ, utilisez <kbd>Maj</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd> pour ajouter ce champ au volet Filtre, saisissez les critères de filtre, utilisez <kbd>Ctrl</kbd>+<kbd>Entrée</kbd> pour revenir aux lignes, sélectionnez un autre champ, puis utilisez <kbd>Alt</kbd>+<kbd>F3</kbd> pour filtrer selon cette valeur. Pour plus d’informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#KeyboardFilter).

### <a name="a-namefiltercriteria-afilter-criteria-and-operators"></a><a name="FilterCriteria"> </a>Critères et opérateurs de filtre

Lorsque vous saisissez des critères, vous pouvez utiliser tous les chiffres et toutes les lettres que vous utilisez habituellement dans ce champ. Mais il existe également un ensemble de symboles spéciaux que vous pouvez utiliser comme opérateurs pour filtrer davantage les résultats. Les sections suivantes décrivent ces symboles et comment les utiliser comme opérateurs dans les filtres.

> [!TIP]
> Pour plus d’informations sur les dates et heures de filtrage, voir [Utiliser des dates civiles et des heures](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Il peut y avoir des situations où la valeur sur laquelle vous souhaitez filtrer contient un symbole qui est un opérateur. Pour plus d’informations sur la gestion de ces situations, consultez [Filtrage des valeurs contenant des symboles](#symbols) pour plus d’instructions sur la gestion de cette situation.
>
> - S’il y a plus de 200 opérateurs dans un seul filtre, le système regroupera automatiquement certaines expressions entre parenthèses `()` à des fins de traitement. Cela n’a aucun effet sur le filtre ou les résultats.  

#### <a name="-interval"></a>(..) Intervalle

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`1100..2100`|Numéros de 1100 à 2100|  
|`..2500`|Jusqu'à 2500 inclus|  
|`..12 31 00`|Dates jusqu'au 31/12/00 compris|  
|`Bicycle..Car`| Enchaîne Bicycle à Car sur commande lexiographique|  
|`P8..`|Informations sur la période comptable 8 et les suivantes|  
|`..23`|Antérieur au 23/mois en cours/année en cours 23:59:59|  
|`23..`|Postérieur au 23/mois en cours/année en cours 0:00:00|  
|`22..23`|Entre le 22/mois en cours/année en cours 0:00:00 et le 23/mois en cours/année en cours 23:59:59| 

> [!TIP]
> Si vous utilisez un pavé numérique, la touche de séparateur décimal peut produire un caractère autre qu’un point (.). Pour choisir un point, sélectionnez les touches <kbd>Alt</kbd>+<kbd>séparateur décimal</kbd> du pavé numérique. Pour revenir en arrière, sélectionnez à nouveau <kbd>Alt</kbd>+<kbd>séparateur décimal</kbd>. Pour plus d’informations, voir [Définition du séparateur décimal utilisé par les claviers numériques](ui-enter-data.md#decimal).

> [!NOTE]  
> Si le champ sur lequel vous filtrez est de type Texte, l’ordre lexiographique est utilisé pour déterminer ce qui est inclus dans l’intervalle. Pour les champs utilisés pour stocker des entiers, cela peut conduire au résultat (inattendu) qu’un filtre sur 10000..10042 inclut également les valeurs 100000 et 1000042.

#### <a name="124-eitheror"></a>(&#124;) Et/ou

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`1200|1300`|Numéros incluant 1200 ou 1300|  

#### <a name="-not-equal-to"></a>(<>) Différent de

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`<>0`|Tous les numéros à l’exception de 0<br /><br /> La version SQL Server vous permet de combiner ce symbole avec une expression de caractères génériques. Par exemple, <>A* signifie différent de tout texte commençant par A.|  

#### <a name="-greater-than"></a>(>) Supérieur à

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`>1200`|Numéros supérieurs à 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Supérieur ou égal à

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`>=1200`|Numéros supérieurs ou égaux à 1200|  

#### <a name="-less-than"></a>(<) Inférieur à

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`<1200`|Numéros inférieurs à 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Inférieur ou égal à

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`<=1200`|Numéros inférieurs ou égaux à 1200|  

#### <a name="-and"></a>(&) Et

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`>200&<1200`|Nombres supérieurs à 200 et inférieurs à 1200|  

#### <a name="-an-exact-character-match"></a>(") Correspondance exacte de caractères

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`'man'`|Texte qui correspond exactement à **man** et qui respecte la casse.|  
|`''`|Texte vide.|  

#### <a name="-case-insensitive"></a>(@) Non-respect de la casse

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`@man*`|Texte qui commence par **man** et qui ne respecte pas la casse.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un chiffre quelconque ou des caractères inconnus

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`*Co*`|Texte qui contient **Co** et respecte la casse.|  
|`*Co`|Texte qui se termine par **Co** et respecte la casse.|  
|`Co*`|Texte qui commence par **Co** et respecte la casse.|  

#### <a name="-one-unknown-character"></a>(?) Un caractère inconnu

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`Hans?n`|Texte tel que **Hansen** ou **Hanson**|  

#### <a name="combined-format-expressions"></a>Expressions de format combinées

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Inclure tous les enregistrements ayant pour numéro 5999 ou un numéro de l'intervalle 8100 à 8490.|  
|`..1299|1400..`|Inclure tous les enregistrements qui portent un numéro inférieur ou égal à 1299 ou un numéro supérieur ou égal à 1400 (tous les numéros sauf ceux compris entre 1300 et 1399).|  
|`>50&<100`|Inclure les enregistrements qui portent un numéro supérieur à 50 et inférieur à 100 (numéros 51 à 99).|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a>Filtrage des valeurs contenant des symboles

Il peut y avoir des cas où les valeurs de champ contiennent l’un des symboles suivants :

- &
- (
- )
- =
- &#124;

Pour filtrer sur l’un de ces symboles, placez l’expression de filtre entre apostrophes (`'<expression with symbol>'`). Par exemple, si vous souhaitez filtrer les enregistrements commençant par le texte *J & V*, l’expression de filtre serait `'J & V*'`.

Cette exigence n’est pas nécessaire pour les autres symboles.

### <a name="a-namefiltertokens-afilter-tokens"></a><a name="FilterTokens"> </a>Jetons de filtre

En saisissant des critères de filtre, vous pouvez également saisir des mots avec un sens particulier, appelés des jetons de filtre. Après avoir saisi le mot de jeton, le mot est remplacé par la ou les valeurs qu’il représente. Filtrer les jetons facilite le filtrage en réduisant la nécessité de naviguer vers d’autres pages pour rechercher des valeurs à ajouter à votre filtre. Les tableaux ci-après décrivent certains des jetons que pouvez saisir comme critères de filtre.

> [!TIP]
> Votre organisation peut utiliser des jetons personnalisés. Pour faire en savoir plus sur l’ensemble complet de jetons disponibles pour vous ou pour ajouter des jetons personnalisés supplémentaires, parlez à votre administrateur. Pour des informations techniques, voir [Ajout de jetons de filtre](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)

#### <a name="me-or-user-records-assigned-to-you"></a>Enregistrements (%me ou %user) qui vous sont attribués

Utilisez `%me` ou `%user` en filtrant les champs qui contiennent le code utilisateur, par exemple le champ **Affecté au code utilisateur**, pour afficher tous les enregistrements qui vous sont affectés.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%me`<br />ou<br />`%user`|Enregistrements affectés à votre compte d’utilisateur. |  

#### <a name="mycustomers-customers-in-my-customers"></a>Clients (%mycustomers) dans Mes clients

Utilisez `%mycustomers` dans le champ **N°** client pour afficher tous les enregistrements des clients inclus dans la liste **Mes clients** de votre tableau de bord.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%mycustomers`|Clients dans **Mes clients** de votre tableau de bord. |  

#### <a name="myitems-items-in-my-items"></a>Articles (%myitems) dans Mes articles

Utilisez `%myitems` dans le champ **N°** article pour afficher tous les enregistrements des articles inclus dans la liste **Mes articles** de votre tableau de bord.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%myitems`|Articles dans **Mes articles** de votre tableau de bord. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>Fournisseurs (%myvendors) dans Mes fournisseurs

Utilisez `%myvendors` dans le champ **N°** fournisseur pour afficher tous les enregistrements des fournisseurs inclus dans la liste **Mes fournisseur** de votre tableau de bord.

|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|`%myvendors`|Fournisseurs dans **Mes fournisseurs** de votre tableau de bord. |  

## <a name="see-also"></a>Voir aussi

[FAQ sur la recherche et le filtrage](ui-search-filter-faq.yml)  
[Enregistrement et personnalisation des vues de liste](ui-views.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
