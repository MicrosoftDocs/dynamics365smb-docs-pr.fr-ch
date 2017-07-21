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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-the-year-end-closing-entry"></a>Comment valider l'écriture de clôture d'exercice
Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d'exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.

## <a name="to-post-the-year-end-closing-entry"></a>Pour valider l'écriture de clôture d'exercice
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille comptabilité**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Feuille comptabilité**, dans le champ **Nom de la feuille**, sélectionnez la feuille qui contient les écritures de clôture.
3. Examinez les écritures.
4. Pour valider la feuille, sélectionnez l'action **Valider**.

> [!NOTE]  
>   En cas de détection d'une erreur, un message d'erreur s'affiche. Si la validation réussit, les entrées validées sont supprimées de la feuille. Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l'exercice soient transférés vers le bilan.

## <a name="see-also"></a>Voir aussi
[Procédure : clôture des périodes comptables](year-close-account-periods.md)  
[Clôture plans](year-close-books.md)  
[Clôturer exercice comptable](year-close-income-statement.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

