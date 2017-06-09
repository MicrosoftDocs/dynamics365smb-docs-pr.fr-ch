---
title: "Procédure : valider une écriture de clôture d&quot;exercice | Microsoft Docs"
description: "Explique comment valider l&quot;écriture de clôture d&quot;exercice."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fe04f75ed84a959cbacd9e9d4806d43d41186edb
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-post-year-end-closing-entry"></a>Procédure : valider une écriture de clôture d'exercice
Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d'exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.

## <a name="to-post-the-year-end-closing-entry"></a>Pour valider l'écriture de clôture d'exercice
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuille comptabilité**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.
3. Examinez les écritures.
4. Pour valider la feuille, sélectionnez l'action **Valider**.

**Remarque** : en cas de détection d'une erreur, un message d'erreur s'affiche. Si la validation réussit, les entrées validées sont supprimées de la feuille. Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l'exercice soient transférés vers le bilan.

## <a name="see-also"></a>Voir aussi
[Procédure : clôture des périodes comptables](year-close-account-periods.md)  
[Clôture plans](year-close-books.md)  
[Solder les comptes de gestion](year-close-income-statement.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

