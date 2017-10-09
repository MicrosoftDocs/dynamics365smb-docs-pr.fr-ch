---
title: "Définition des plages de dates dans Dynamics 365 for Financials | Microsoft Docs"
description: "En savoir plus pour obtenir un état affichant les données de périodes spécifiques à l'aide de plages de dates dans Dynamics 365 for Financials."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dc7cd392843ce7c39200bb2331c09cc44c7a394a
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="entering-date-ranges-in-dynamics-365-for-financials"></a>Saisie de plages de dates dans Dynamics 365 for Financials
Vous pouvez définir des filtres contenant une date de début et une date de fin pour afficher uniquement les données contenues dans cette plage de données ou cet intervalle de temps. Des règles spéciales s'appliquent à la définition des plages de dates. Prenons par exemple **Palmarès des clients** :

![Définition d'une plage de dates dans la page de demande de la liste du palmarès des clients](./media/ui-enter-date-ranges/customer-top10-list.png)

Vous pouvez limiter ici l'état à une plage de dates telles que les 2 dernières semaines, ou un total de 6 semaines, ou toute plage de votre choix. Pour définir les plages de dates, vous entrez des dates puis utilisez **..** ou **|** pour définir la plage. Dans notre exemple, pour afficher les 10 clients principaux des deux premières semaines de mai, vous devez définir le filtre de date sur *05 01 17..05 14 17*.
Voici d'autres exemples :

| Signification | Exemple : | Ecritures incluses |
|---|---|---|
|Egal à| 15 12 16 |Uniquement les écritures validées le 15 décembre 2016.|
|Intervalle| 15 12 16..15 17 17<br /><br />..12 15 16|Celles validées entre le 15 décembre 2016 et le 15 janvier 2017 inclus.<br /><br />Écritures validées le 15 décembre 2016 ou à une date antérieure.|
|Et/ou|12 15 16&#124;12 16 16|Celles validées le 15 ou le 16 décembre 2016. Les écritures validées aux deux dates sont également affichées.|

Vous pouvez aussi combiner les divers types de format.

| Exemple : | Ecritures incluses |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Écritures validées le 15 décembre 2016 ou à des dates situées entre le 1er décembre 2016 et le 31 mai 2017 inclus. |
|..12 14 16&#124;12 30 16.. | Les écritures validées le 14 décembre ou avant, ou écritures validées le 30 décembre ou après, c.-à-d. toutes les écritures à l'exception de celles validées à des dates situées entre le 15 et le 29 décembre. |

Remarquez que nous avons utilisé le format de date américaine MMJJAA. A mesure que [!INCLUDE[d365fin](includes/d365fin_md.md)] deviendra disponible sur d'autres marché, vous pourrez utiliser les formats auxquels vous êtes habitué.

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Saisir les critères pour les filtres](ui-enter-criteria-filters.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

