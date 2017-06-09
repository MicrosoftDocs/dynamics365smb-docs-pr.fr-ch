---
title: "Saisir les critères pour les filtres | Microsoft Docs"
description: "En savoir plus sur la manière dont les filtres fonctionnent dans Financials."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1a94e2ead59a40081920a0b11ed545a895d89910
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="entering-criteria-in-filters"></a>Saisir les critères pour les filtres
Lorsque vous souhaitez rechercher des données, telles que des noms de client, des adresses ou des groupes de produits, vous saisissez des critères. Dans vos critères de recherche, vous pouvez utiliser tous les chiffres et toutes les lettres que vous utilisez habituellement dans ce champ spécifique. En plus, vous pouvez utiliser des symboles spéciaux pour filtrer davantage les résultats.

## <a name="searching-using-the-quick-filter"></a>Rechercher à l'aide du filtre rapide
Vous pouvez ajouter des filtres pour l'ensemble des pages en utilisant le filtre rapide. Vous activez le filtre rapide sélectionnant l'icône de loupe dans le coin supérieur droit d'une page. Ce type de filtre est utilisé pour une saisie rapide des critères.

**Important** : le filtre rapide facilite l'accès aux données de filtre par la saisie de texte simple, mais fournit également un grand nombre d'options de critères de recherche. Selon que vous saisissez du texte simple ou du texte comprenant des symboles, le Filtre rapide se comporte de façon différente.  

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

**Remarque**: vous ne pouvez pas utiliser de caractères génériques lors du filtrage des champs d'énumération, tels que le champ **Statut** sur les commandes vente. Pour entrer un filtre pour ce type de champ, vous pouvez saisir la valeur numérique comme paramètre de filtre. Par exemple, dans le champ **Statut** sur une commande vente qui a les valeurs **Ouvert**, **Lancé**, **Approbation suspendue** et **Acompte suspendu**, utilisez les valeurs **0**, **1**, **2** et **3** pour filtrer ces options.  

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

