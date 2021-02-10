---
title: Clôturer des périodes comptables pour un exercice comptable | Microsoft Docs
description: Décrit comment clôturer les périodes comptables de l’exercice comptable.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6acdc86afc195185f66836bf723c83d4a1647927
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755682"
---
# <a name="close-accounting-periods"></a>Clôturer des périodes comptables
Lorsqu’un exercice comptable est terminé, vous devez clôturer les périodes qui le composent.

## <a name="to-close-accounting-periods"></a>Pour clôturer des périodes comptables
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Périodes comptables**, puis sélectionnez le lien associé.
2. Sur la page **Périodes comptables**, sélectionnez l’action **Clôturer exercice**.

    Si plusieurs exercices comptables sont ouverts, le plus ancien est automatiquement sélectionné pour être clôturé. Un message identifiant l’exercice qu’il compte clôturer s’affiche et indique les conséquences de la clôture.
3. Pour clôturer l’exercice, cliquez sur **Oui**.

L’exercice comptable est désormais clôturé, et les champs **Fermé** et **Verrouillage date** sont sélectionnés pour toutes les périodes de l’exercice. Vous ne pouvez pas rouvrir l’exercice comptable ni supprimer la coche des champs **Fermé** et **Verrouillage date**.

> [!NOTE]  
>   Vous ne pouvez pas clôturer un exercice comptable avant d’en créer un nouveau. Sachez que lorsqu’un exercice comptable est clôturé, vous ne pouvez pas modifier la date début de l’exercice comptable suivant.

Même si un exercice comptable a été clôturé, vous pouvez toujours y valider des écritures. Dans ce cas, les écritures sont marquées comme validées dans un exercice comptable clôturé et le champ **Ecr. exercice précédent** est activé.

Une fois qu’un exercice comptable a été clôturé, vous devez clôturer les comptes de gestion et transférer les résultats de l’exercice sur un compte du bilan. Vous pouvez répéter cette opération chaque fois que vous validez dans l’exercice comptable clôturé.

## <a name="see-also"></a>Voir aussi

[Clôture plans](year-close-books.md)  
[Valider l’écriture de clôture d’exercice](year-how-post-year-end-close-entry.md)  
[Utiliser des périodes et exercices comptables](finance-accounting-periods-and-fiscal-years.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
