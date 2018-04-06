---
title: "Vérifier et valider l'écriture de clôture d'exercice | Microsoft Docs"
description: "Décrit comment ouvrir la feuille spécifiée dans le traitement par lots Clôturer exercice comptable, puis examiner et valider l'écriture de clôture de fin d'exercice."
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 78039e9387866ce17ff3be5a2ff509545e8439d2
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-the-year-end-closing-entry"></a>Valider l'écriture de clôture d'exercice
Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d'exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.

## <a name="to-post-the-year-end-closing-entry"></a>Pour valider l'écriture de clôture d'exercice
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Feuille comptabilité**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.
3. Examinez les écritures.
4. Pour valider la feuille, sélectionnez l'action **Valider**.

> [!NOTE]  
>   En cas de détection d'une erreur, un message d'erreur s'affiche. Si la validation réussit, les entrées validées sont supprimées de la feuille. Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l'exercice soient transférés vers le bilan.

## <a name="see-also"></a>Voir aussi
[Clôturer des périodes comptables](year-close-account-periods.md)  
[Clôture plans](year-close-books.md)  
[Clôturer exercice comptable](year-close-income-statement.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

