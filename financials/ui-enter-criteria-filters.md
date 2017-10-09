---
title: "Recherche de données et saisie de critères de filtre | Microsoft Docs"
description: "Décrit comment utiliser les filtres, par exemple le filtre rapide, pour préciser les résultats que vous obtenez lorsque vous recherchez des données."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a>Recherche, filtrage et tri de données
Il existe quelques fonctions que vous pouvez utiliser pour vous aider à rechercher, identifier et analyser des enregistrements d'une liste. Ce sont notamment le tri, la recherche et le filtrage.

Lorsque vous souhaitez rechercher des données, telles que des noms de client, des adresses ou des groupes de produits, vous saisissez des critères. Dans vos critères de recherche, vous pouvez utiliser tous les chiffres et toutes les lettres que vous utilisez habituellement dans ce champ spécifique. En plus, vous pouvez utiliser des symboles spéciaux pour filtrer davantage les résultats. Il existe deux façons d'effectuer des recherches : en utilisant le filtre rapide ou les filtres de colonne.

## <a name="sorting"></a>Tri
Le tri vous permet d'avoir facilement un aperçu de vos données. Si vous avez de nombreux clients, par exemple, vous pouvez choisir de les trier par **N° client**, **Groupe compta. client**, **Code devise**, **Code pays/région** ou **N° d'enregistrement Sales Tax** pour obtenir l'aperçu que vous souhaitez.

Pour trier une liste, vous pouvez choisir un texte d'en-tête de colonne pour permuter entre l'ordre croissant et décroissant, ou cliquer sur la petite flèche vers le bas dans l'en-tête de colonne et choisir **Croissant** ou **Décroissant**.  

> [!NOTE]  
>   Le tri n'est pas pris en charge sur les images, les champs de type BLOB, les FlowFilters, et les champs n'appartenant pas à une table.  

## <a name="searching-by-using-the-quick-filter"></a>Recherche à l'aide du filtre rapide
Vous pouvez ajouter des filtres pour l'ensemble des pages en utilisant le filtre rapide. Vous activez le filtre rapide sélectionnant l'icône de loupe dans le coin supérieur droit d'une page. Ce type de filtre est utilisé pour une saisie rapide des critères.

> [!IMPORTANT]  
>   Le Filtre rapide facilite l'accès aux données de filtre par la saisie de texte simple, mais fournit également un grand nombre d'options de critères de recherche. Selon que vous saisissez du texte simple ou du texte comprenant des symboles, le Filtre rapide se comporte de façon différente.  

* Si vous saisissez du texte simple dans les critères de recherche, le critère de recherche est interprété comme une recherche insensible à la casse qui contient un certain texte.  
* Si vous saisissez du texte comprenant des symboles dans les critères de recherche, le critère de recherche est interprété exactement comme vous l'avez saisi, et la recherche distingue les majuscules et les minuscules.

### <a name="quick-filter-criteria"></a>Critères de filtre rapide
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Critères de recherche</TH>
    <TH>Interprété comme...</TH>
    <TH>Renvoie...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Tous les enregistrements qui contiennent le texte <b>man</b> et ne respectent pas la casse.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Tous les enregistrements qui contiennent le texte <b>se</b> et ne respectent pas la casse.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Commence par <b>Man</b> avec respect de la casse.</TD>
    <TD>Tous les enregistrements qui commencent par le texte <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Texte exact avec respect de la casse.</TD>
    <TD>Tous les enregistrements qui correspondent exactement à <b>man</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Commence par et ne respecte pas la casse.</TD>
    <TD>Tous les enregistrements qui commencent par <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Se termine par et respecte la casse.</TD>
    <TD>Tous les enregistrements qui se terminent par <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Vous ne pouvez pas utiliser de caractères génériques lors du filtrage des champs d'énumération, tels que le champ **Statut** sur les commandes vente. Pour entrer un filtre pour ce type de champ, vous pouvez saisir la valeur numérique comme paramètre de filtre. Par exemple, dans le champ **Statut** sur une commande vente qui a les valeurs **Ouvert**, **Lancé**, **Approbation suspendue** et **Acompte suspendu**, utilisez les valeurs **0**, **1**, **2** et **3** pour filtrer ces options. 

## <a name="searching-by-using-column-filters"></a>Recherche à l'aide des filtres de colonne
Vous pouvez ajouter un filtre sur une ou plusieurs colonnes d'une liste. Le filtrage des colonnes est une fonction plus flexible et améliorée que le filtre rapide. 

### <a name="to-add-a-filter-on-a-column"></a>Pour ajouter un filtre à une colonne
1.  Avant d'ajouter un filtre, choisissez l'icône ![Afficher sous forme de liste](media/ui_show_as_list_icon.png "Afficher sous forme de liste") pour passer à la vue de liste.
2. Cliquez sur la flèche vers le bas dans l'en-tête de colonne, puis choisissez **Filtrer**.
3. Exécutez l'une des opérations suivantes : 
  -  Choisissez *…* en regard de la zone pour sélectionner une valeur dans la liste.
  -  Entrez les critères de filtre dans la zone. Consultez la section suivante pour plus de détails.
4. Cliquez sur le bouton **OK**.

## <a name="filter-criteria-and-symbols"></a>Critères et symboles de filtre
Lorsque vous saisissez des critères, vous pouvez utiliser tous les chiffres et toutes les lettres que vous utilisez habituellement dans ce champ. En plus, vous pouvez utiliser des symboles spéciaux pour filtrer davantage les résultats. Les tables suivantes indiquent les symboles qui peuvent être utilisés dans les filtres.  
  
> [!IMPORTANT]  
>  Il peut y avoir des instances où les valeurs de champ contiennent ces symboles et vous souhaitez les filtrer. Pour ce faire, vous devez inclure l'expression de filtre qui contient le symbole entre guillemets ("). Par exemple, si vous souhaitez filtrer les enregistrements commençant par le texte *S&R*, l'expression de filtre est **'S&R*'**.  
  
### <a name="-interval"></a>(..) Intervalle  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|1100..2100|Numéros de 1100 à 2100|  
|..2500|Jusqu'à 2500 inclus|  
|..31 12 00|Dates jusqu'au 31/12/00 compris|  
|P8..|Informations sur la période comptable 8 et les suivantes|  
|..23|Antérieur au 23/mois en cours/année en cours 23:59:59|  
|23..|Postérieur au 23/mois en cours/année en cours 0:00:00|  
|22..23|Entre le 22/mois en cours/année en cours 0:00:00 et le 23/mois en cours/année en cours 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) Et/ou  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|1200&#124;1300|Numéros incluant 1200 ou 1300|  
  
### <a name="-not-equal-to"></a>(<>) Différent de  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|<>0|Tous les numéros à l'exception de 0<br /><br /> La version SQL Server vous permet de combiner ce symbole avec une expression de caractères génériques. Par exemple, <>A* signifie différent de tout texte commençant par A.|  
  
### <a name="-greater-than"></a>(>) Supérieur à  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|>1200|Numéros supérieurs à 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Supérieur ou égal à  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|>=1200|Numéros supérieurs ou égaux à 1200|  
  
### <a name="-less-than"></a>(<) Inférieur à  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|<1200|Numéros inférieurs à 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Inférieur ou égal à  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|<=1200|Numéros inférieurs ou égaux à 1200|  
  
### <a name="-and"></a>(&) Et  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|>200&<1200|Nombres supérieurs à 200 et inférieurs à 1200|  
  
### <a name="-an-exact-character-match"></a>(") Correspondance exacte de caractères  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|'man'|Texte qui correspond exactement à man et qui respecte la casse.|  
  
### <a name="-case-insensitive"></a>(@) Non-respect de la casse  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|@man*|Texte qui commence par man et qui ne respecte pas la casse.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un chiffre quelconque ou des caractères inconnus  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|*Co*|Texte qui contient « Co » et respecte la casse.|  
|*Co|Texte qui se termine par « Co » et respecte la casse.|  
|Co*|Texte qui commence par « Co » et respecte la casse.|  
  
### <a name="-one-unknown-character"></a>(?) Un caractère inconnu  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|Hans?n|Texte tel que Hansen ou Hanson|  
  
### <a name="combined-format-expressions"></a>Expressions de format combinées  
  
|Expression|Enregistrements affichés|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Inclure tous les enregistrements ayant pour numéro 5999 ou un numéro de l'intervalle 8100 à 8490.|  
|..1299&#124;1400..|Inclure tous les enregistrements qui portent un numéro inférieur ou égal à 1299 ou un numéro supérieur ou égal à 1400 (tous les numéros sauf ceux compris entre 1300 et 1399).|  
|>50&<100|Inclure les enregistrements qui portent un numéro supérieur à 50 et inférieur à 100 (numéros 51 à 99).|  
 
## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

