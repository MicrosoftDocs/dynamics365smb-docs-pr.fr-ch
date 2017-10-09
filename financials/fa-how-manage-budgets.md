---
title: "Gérer les budgets immo.| Microsoft Docs"
description: "Vous paramétrez les informations sur de futurs investissements, cessions, et amortissements d'immobilisations pour préparer les budgets et les prévisions."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2185a1fc40ddae772e20994f6531b02d7e703e17
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-budgets-for-fixed-assets"></a>Procédure : gérer les budgets pour les immobilisations
Vous pouvez paramétrer des immobilisations budgétées. Cela vous permet par exemple d'inclure dans des états des acquisitions et des ventes anticipées.  

Pour préparer le compte de gestion budgété, le compte de bilan budgété et le budget de trésorerie, vous avez besoin d'informations sur les investissements, les cessions et les amortissements futurs des immobilisations. Vous pouvez obtenir ces informations dans l'état **Immo. - Valeur projetée**. Avant d'imprimer cet état, vous devez préparer le budget.  

> [!NOTE]  
>   Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Pour budgéter le coût d'acquisition d'une immobilisation
Pour préparer un budget, vous devez définir des fiches immobilisation pour les immobilisations que vous souhaitez acheter. Les immobilisations du budget sont configurées comme immobilisations ordinaires, mais elles doivent être configurées pour ne pas être validées en comptabilité.

Lorsque vous validez le coût d'acquisition, vous saisissez le numéro de l'immobilisation budgétée dans le champ **N° immo. budgétée** Cela permet de valider un coût d'acquisition avec un signe opposé pour l'immobilisation budgétée. Le coût d'acquisition total de l'immobilisation budgétée est donc la différence entre le coût d'acquisition budgété et le coût réel.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Immobilisations**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau** pour créer une fiche immobilisation pour l'immobilisation budgétée.
3. Cochez la case **Actif budgété** pour empêcher la validation en comptabilité.
4. Complétez les champs restants, attribuez une loi d'amortissement, puis validez le premier coût d'acquisition avec l'immobilisation budgétée saisie dans le champ **N° immo. budgétée** de la ligne feuille. Pour en savoir plus, voir [Procédure : acquérir les immobilisations](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Pour budgéter la cession d'une immobilisation
Si vous prévoyez de vendre des immobilisations dans la période correspondant au budget, vous pouvez indiquer des informations concernant le prix et la date de vente.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Immobilisations**, puis sélectionnez le lien connexe.
2. Sélectionnez l'immobilisation à céder, puis sélectionnez l'action **Lois d'amortissement**.
3. Dans la fenêtre **Lois d'amortissement immo.**, complétez les champs **Date cession prévue** et **Produit de cession prévu**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Pour visualiser des valeurs de cession prévues
Pour visualiser les valeurs de cession prévues et effectuer le calcul des gains et des pertes, vous pouvez utiliser l'état **Immo. - Valeur projetée**.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Immo. - Valeur projetée**, puis sélectionnez le lien connexe.
2. Renseignez les champs selon vos besoins.
3. Cliquez sur le bouton **Imprimer** ou **Aperçu**.

## <a name="to-budget-depreciation"></a>Pour budgéter des amortissements
Vous pouvez utiliser l'état **Immo. - Valeur projetée** pour calculer l'amortissement à venir. L'état affiche la valeur comptable et l'amortissement cumulé au début et à la fin de la période sélectionnée, ainsi que les modifications apportées durant cette période.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Immo. - Valeur projetée**, puis sélectionnez le lien connexe.
2. Renseignez les champs selon vos besoins.
3. Pour voir les valeurs totales de tous les actifs, décochez la case **Imprimer par immobilisation**.
4. Ne renseignez pas le raccourci **Immobilisation** pour inclure toutes les immobilisations. Dans le champ **Immo. budgétée**, vous pouvez saisir **Non** afin d'exclure les immobilisations budgétées ou sur **Oui** pour les visualiser.
5. Cliquez sur le bouton **Imprimer** ou **Aperçu**.

## <a name="see-also"></a>Voir aussi
[Immobilisations](fa-manage.md)  
[Paramétrage d'immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

