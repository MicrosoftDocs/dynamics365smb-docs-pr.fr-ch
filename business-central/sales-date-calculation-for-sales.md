---
title: Calcul de la date des ventes | Microsoft Docs
description: L’application calcule automatiquement la date à laquelle vous devez commander un article pour l’avoir en stock à une certaine date. Il s’agit de la date à laquelle des articles commandés à une date donnée devraient être disponibles pour le prélèvement.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 49bc91d049ee6c2357323ed4e88f66116322d276
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778912"
---
# <a name="date-calculation-for-sales"></a>Calcul de la date des ventes
[!INCLUDE[prod_short](includes/prod_short.md)] calcule automatiquement la première date possible à laquelle un article d’une ligne commande vente peut être expédié.

Si le client a demandé une date livraison particulière, alors la date à laquelle les articles doivent pouvoir être prélevés est calculée pour permettre une livraison à cette date.

Si le client ne demande pas de date livraison particulière, alors la date à laquelle les articles peuvent être livrés, à partir de la date à laquelle les articles peuvent être prélevés, est calculée.

## <a name="calculating-a-requested-delivery-date"></a>Calcul d’une date de livraison demandée
Si vous spécifiez une date de livraison demandée sur la ligne vente, cette date devient le point de départ du calcul suivant :

- Date livraison demandée - délai d’expédition = date d’expédition planifiée
- Date d’expédition + délai désenlogement = date d’expédition planifiée

Si les articles peuvent être prélevés à la date d’expédition, alors le processus vente peut continuer. Sinon, un avertissement de rupture de stock est affiché.

> [!Note]
> Si votre processus est basé sur un calcul en amont, par exemple, si vous utilisez la date livraison demandée pour obtenir la date livraison planifiée, nous vous recommandons d’utiliser des formules de date ayant des durées fixes, telles que "5D" pendant cinq jours ou "1W" pour une semaine. Les formules de date sans durée fixe, telles que "CW" pour la semaine en cours ou CM pour le mois en cours, peuvent entraîner des calculs de date incorrects. Pour plus d’informations sur les formules de date, voir [Utilisation de dates civiles et des heures](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Calcul de la première date de livraison possible
Si vous ne spécifiez aucune date livraison demandée sur la ligne de commande vente ou si la date livraison demandée ne peut pas être respectée, alors la première date à laquelle les articles sont disponibles est calculée. Cette date est ensuite renseignée dans le champ Date d’expédition sur la ligne, et la date à laquelle vous prévoyez d’expédier les articles, ainsi que la date à laquelle ces derniers seront livrés au client sont calculées via les formules suivantes.

- Date d’expédition + délai désenlogement = date d’expédition planifiée
- Date livraison planifiée - délai d’expédition = date expédition planifiée


## <a name="see-also"></a>Voir aussi  
 [Calcul de la date des achats](purchasing-date-calculation-for-purchases.md)   
 [Calculer des dates promesse livraison](sales-how-to-calculate-order-promising-dates.md)  
 [Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]