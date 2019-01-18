---
title: "Création de budgets comptabilité | Microsoft Docs"
description: "Décrit la création de budgets comptabilité pour prévoir différentes activités financières et affecter des axes analytiques à des fins de veille économique."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4cf8738c7bab09f7bcf900baae54731b6772e7e9
ms.contentlocale: fr-ch
ms.lasthandoff: 11/22/2018

---
# <a name="create-gl-budgets"></a>Créer des budgets comptabilité
Vous pouvez avoir plusieurs budgets pour des périodes identiques en les créant sous des noms différents. Vous indiquez d'abord le nom du budget et entrez les chiffres correspondants. Le nom du budget est ensuite inclus sur toutes les écritures budget que vous créez.  

 Lorsque vous créez un budget, vous pouvez définir quatre axes analytiques par budget. Ces axes analytiques propres au budget sont appelés axes budget. Vous sélectionnez les axes budget pour chaque budget parmi les axes analytiques que vous avez déjà configurés. Les axes budget peuvent être utilisés pour positionner des filtres sur un budget et pour ajouter des informations analytiques aux écritures budget. Pour plus d'informations, reportez-vous à [Utilisation des axes](finance-dimensions.md).

 Les budgets jouent un rôle important dans la veille économique, par exemple dans les états financiers basés sur des tableaux d'analyse incluant des écritures budget ou lors de l'analyse des montants budgétés et des montants réels dans le plan comptable. Pour plus d'informations, reportez-vous à [Veille économique](bi.md).

 Les budgets jouent un rôle important dans la veille économique, par exemple dans les états financiers basés sur des tableaux d'analyse incluant des écritures budget ou lors de l'analyse des montants budgétés et des montants réels dans le plan comptable. Pour plus d'informations, reportez-vous à [Veille économique](bi.md).

En comptabilité analytique, vous travaillez avec des budgets de coûts de manière similaire. Pour plus d'informations, voir [Procédure : Créer des budgets de coûts](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Pour créer un budget comptabilité  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Budgets**, puis choisissez le lien associé.  
2. Cliquez sur **Modifier la liste**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sélectionnez **Modifier budget**.
4. En haut de la page **Budget**, renseignez les champs nécessaires pour définir ce qui est affiché.  

    Seules les écritures contenant le nom du budget entré dans le champ **Nom budget** s'affichent. Étant donné que le nom du budget vient juste d'être créé, aucune écriture ne correspond au filtre. Par conséquent, la page est vide.  
5. Pour entrer un montant, choisissez la cellule appropriée de la matrice. La page **Écritures budget** s'ouvre.  
6. Créez une ligne et renseignez le champ **Montant**. Fermez la page **Écritures budget**.  
7. Répétez les étapes 5 et 6 jusqu'à ce que vous ayez entré tous les montant du budget.  

> [!NOTE]  
>  Sur le raccourci **Filtres**, vous pouvez filtrer les informations sur le budget selon le nombre d'axes budget configurés sous le nom du budget.   

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Veille économique](bi.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

