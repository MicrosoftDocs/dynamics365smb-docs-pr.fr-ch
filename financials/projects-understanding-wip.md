---
title: "Comprendre les méthodes TEC| Microsoft Docs"
description: "Décrit les différentes méthodes TEC qui peuvent être utilisées pour valider et surveiller les données financières pour les projets en cours."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d6f82b3eb086b53be8a091e7a805c745a74ac10f
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="understanding-wip-methods"></a>Comprendre les méthodes TEC
[!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge les méthodes suivantes pour calculer et enregistrer la valeur des travaux en cours.

| Méthode TEC | Formule de calcul | Description du calcul |
| --- | --- | --- |
| Valeur de coût |Revenus réceptionnés = Facturable (prix facturé)<br /><br /> Coûts totaux estimés = Facturable (prix total) x Coût budgétaire (ratio)<br /><br /> Coûts TEC = \(Pourcentage avancement - % facturé\) x Coûts totaux estimés<br /><br /> Pourcentage avancement = Activité (coûts totaux) / Budget (coûts totaux)<br /> % facturé = Facturable (prix facturé)<br /><br /> Coûts réceptionnés facturables (prix total)= Activité (coûts totaux) - TEC |Le calcul Valeur de coût commence par calculer la valeur du montant fourni en prenant une proportion des coûts totaux estimés basée sur le pourcentage d'achèvement. Les coûts facturés sont soustraits en prenant une proportion des coûts totaux estimés basée sur le pourcentage facturé.<br /><br /> Ce calcule nécessite que le prix total facturable, le prix total du budget et les coûts budgétaires totaux soient correctement renseignés pour l'ensemble du projet. |
| Coût des ventes |Revenus réceptionnés = Facturable (prix facturé)<br /><br /> Coûts réceptionnés = Coût total du budget x Pourcentage facturé<br /><br /> % facturé = Facturable (prix facturé) / Facturable (prix total)<br /><br /> \(Le % facturé apparaît sous forme de colonne dans les lignes tâche projet\)<br /><br /> Coûts TEC = Activité (coûts totaux) – Coûts réceptionnés |Le calcul Coût des ventes commence par calculer les coûts réceptionnés. Les coûts sont réceptionnés proportionnellement sur la base des coûts budgétaires totaux.<br /><br /> Ce calcule nécessite que le prix total facturable et les coûts budgétaires totaux soient correctement renseignés pour l'ensemble du projet. |
| Valeur des ventes |Coûts réceptionnés = Activité (coûts totaux)<br /><br /> Revenus réceptionnés = Activité (prix total) x Facturation prévue (ratio)<br /><br /> % recouvrement des coûts = Facturable (prix total)/Prix total du budget<br /><br /> Vente TEC = Ventes réceptionnées - Facturable (prix facturé) |Le calcul Valeur des ventes réceptionne les revenus proportionnellement sur la base des coûts totaux et le ratio attendu de recouvrement des coûts.<br /><br /> Ce calcule nécessite que le prix total facturable et le prix budgétaire total soient correctement renseignés pour l'ensemble du projet. |
| Pourcentage d'achèvement |Coûts réceptionnés = Activité (coûts totaux)<br /><br /> Revenus réceptionnés = Facturable (prix total) x Pourcentage avancement<br /><br /> Pourcentage avancement = Activité (coûts totaux) / Budget (coûts totaux)<br /> \(Appelé « % achèvement coût » dans les lignes tâche projet\)<br /><br /> Vente TEC = Ventes réceptionnées - Facturable (prix facturé) |Le calcul Pourcentage avancement réceptionne les revenus proportionnellement sur la base du pourcentage d'achèvement, soit les coûts totaux par rapport aux coûts budgétés.<br /><br /> Ce calcule nécessite que le prix total facturable et les coûts budgétaires totaux soient correctement renseignés pour l'ensemble du projet. |
| Contrat complété |Montant TEC = Montant coût TEC = Activité \(Coût total\)<br /><br /> Montant vente TEC = Facturable \(Prix facturé\) |La méthode Fin de contrat ne réceptionne pas les revenus et les coûts avant la fin du projet. Cela peut être utile lorsque l'estimation des coûts et des revenus du projet est excessivement difficile.<br /><br /> L'ensemble de l'activité est validé dans le Compte coûts TEC \(actif\) et toutes les ventes facturées sont validées dans le Compte ventes facturées TEC \(passif\) jusqu'à la fin du projet. |

## <a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Finance](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

