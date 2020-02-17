---
title: Méthodes TEC pour calculer et enregistrer la progression d'un projet| Microsoft Docs
description: Décrit les différentes méthodes de travaux en cours (TEC) qui peuvent être utilisées pour valider, surveiller et calculer les données financières des projets en cours.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 02/04/2020
ms.author: sgroespe
ms.openlocfilehash: ac6b41d9fe03968531b7d99e534055b6a9955f57
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030307"
---
# <a name="understanding-wip-methods"></a>Comprendre les méthodes TEC
Au fur et à mesure de la progression du projet, les matières, ressources et autres frais sont consommés et doivent être validés dans le projet. La fonctionnalité Travaux en cours (TEC) permet d'estimer la valeur financière des projets dans la comptabilité au cours des projets. Dans de nombreux cas, vous pouvez valider les frais pour un projet avant de le facturer. Lorsque seuls les frais sont validés, l'état financier est incorrect.

Pour effectuer le suivi de la valeur dans la comptabilité, vous pouvez calculer les TEC et valider la valeur en comptabilité. Pour plus d'informations, voir [Surveiller la progression et les performances](projects-how-monitor-progress-performance.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge les méthodes suivantes pour calculer et enregistrer la valeur des travaux en cours.

| Méthode TEC | Formule de calcul | Description du calcul |
| --- | --- | --- |
| Valeur de coût |Revenus réceptionnés = Facturable (prix facturé)<br /><br /> Coûts totaux estimés = Facturable (prix total) x Coût budgétaire (ratio)<br /><br /> Coûts TEC = (Pourcentage avancement - % facturé) x Coûts totaux estimés<br /><br /> Pourcentage avancement = Activité (coûts totaux) / Budget (coûts totaux)<br /> % facturé = Facturable (prix facturé)<br /><br /> Coûts réceptionnés facturables (prix total)= Activité (coûts totaux) - TEC |Le calcul Valeur de coût commence par calculer la valeur du montant fourni en prenant une proportion des coûts totaux estimés basée sur le pourcentage d'achèvement. Les coûts facturés sont soustraits en prenant une proportion des coûts totaux estimés basée sur le pourcentage facturé.<br /><br /> Ce calcule nécessite que le prix total facturable, le prix total du budget et les coûts budgétaires totaux soient correctement renseignés pour l'ensemble du projet. |
| Coût des ventes |Revenus réceptionnés = Facturable (prix facturé)<br /><br /> Coûts réceptionnés = Coût total du budget x Pourcentage facturé<br /><br /> % facturé = Facturable (prix facturé) / Facturable (prix total)<br /><br /> (Le % facturé apparaît sous forme de colonne dans les lignes tâche projet)<br /><br /> Coûts TEC = Activité (coûts totaux) – Coûts réceptionnés |Le calcul Coût des ventes commence par calculer les coûts réceptionnés. Les coûts sont réceptionnés proportionnellement sur la base des coûts budgétaires totaux.<br /><br /> Ce calcule nécessite que le prix total facturable et les coûts budgétaires totaux soient correctement renseignés pour l'ensemble du projet. |
| Valeur des ventes |Coûts réceptionnés = Activité (coûts totaux)<br /><br /> Revenus réceptionnés = Activité (prix total) x Facturation prévue (ratio)<br /><br /> % recouvrement des coûts = Facturable (prix total)/Prix total du budget<br /><br /> Vente TEC = Ventes réceptionnées - Facturable (prix facturé) |Le calcul Valeur des ventes réceptionne les revenus proportionnellement sur la base des coûts totaux et le ratio attendu de recouvrement des coûts.<br /><br /> Ce calcule nécessite que le prix total facturable et le prix budgétaire total soient correctement renseignés pour l'ensemble du projet. |
| Pourcentage d'achèvement |Coûts réceptionnés = Activité (coûts totaux)<br /><br /> Revenus réceptionnés = Facturable (prix total) x Pourcentage avancement<br /><br /> Pourcentage avancement = Activité (coûts totaux) / Budget (coûts totaux)<br /> (Appelé « % achèvement coût » dans les lignes tâche projet)<br /><br /> Vente TEC = Ventes réceptionnées - Facturable (prix facturé) |Le calcul Pourcentage avancement réceptionne les revenus proportionnellement sur la base du pourcentage d'achèvement, soit les coûts totaux par rapport aux coûts budgétés.<br /><br /> Ce calcule nécessite que le prix total facturable et les coûts budgétaires totaux soient correctement renseignés pour l'ensemble du projet. |
| Contrat complété |Montant TEC = Montant coût TEC = Activité (coût total)<br /><br /> Montant vente TEC = Facturable (Prix facturé) |La méthode Fin de contrat ne réceptionne pas les revenus et les coûts avant la fin du projet. Cela peut être utile lorsque l'estimation des coûts et des revenus du projet est excessivement difficile.<br /><br /> L'ensemble de l'activité est validé dans le compte Coûts TEC (actif) et toutes les ventes facturées sont validées dans le compte Ventes facturées TEC (passif) jusqu'à la fin du projet. |

## <a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
