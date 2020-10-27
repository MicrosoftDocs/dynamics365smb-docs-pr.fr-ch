---
title: Vérifier et valider l’écriture de clôture d’exercice | Microsoft Docs
description: Décrit comment ouvrir la feuille spécifiée dans le traitement par lots Clôturer exercice comptable, puis examiner et valider l’écriture de clôture de fin d’exercice.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 3181fe2bfa72897a4e8db8dd1bae6b0f235c6eaa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923185"
---
# <a name="post-the-year-end-closing-entry"></a>Valider l’écriture de clôture d’exercice
Après avoir utilisé le traitement par lots **Solder les comptes de gestion** pour générer les écritures de clôture d’exercice, vous devez ouvrir la feuille spécifiée dans le traitement par lots, puis consulter et valider les écritures.

## <a name="to-post-the-year-end-closing-entry"></a>Pour valider l’écriture de clôture d’exercice
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille comptabilité** , puis sélectionnez le lien associé.
2. Sur la page **Feuille comptabilité** , dans le champ **Nom de la feuille** , sélectionnez la feuille qui contient les écritures de clôture.
3. Examinez les écritures.
4. Pour valider la feuille, sélectionnez l’action **Valider** .

> [!NOTE]  
>   En cas de détection d’une erreur, un message d’erreur s’affiche. Si la validation réussit, les entrées validées sont supprimées de la feuille. Une fois la validation terminée, une entrée est validée dans chaque compte résultats, de façon à ce que son solde indique zéro et à ce que les résultats de l’exercice soient transférés vers le bilan.

## <a name="see-also"></a>Voir aussi
[Clôturer des périodes comptables](year-close-account-periods.md)  
[Clôture plans](year-close-books.md)  
[Clôturer exercice comptable](year-close-income-statement.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
