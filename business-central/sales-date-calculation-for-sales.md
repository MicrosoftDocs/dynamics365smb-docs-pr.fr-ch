---
title: Calcul de la date de livraison des ventes
description: L’application calcule automatiquement la date à laquelle vous devez commander un article pour l’avoir en stock à une certaine date et disponible pour prélèvement.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/22/2022
ms.author: edupont
---
# Calcul de la date de livraison des ventes

[!INCLUDE[prod_short](includes/prod_short.md)] calcule automatiquement la première date possible à laquelle un article d’une ligne commande vente peut être expédié.

* Si le client a demandé une date livraison particulière, alors la date à laquelle les articles doivent pouvoir être prélevés est calculée pour permettre une livraison à cette date.
* Si le client a demandé une date livraison particulière, alors la date à laquelle les articles peuvent être livrés est calculée. Le calcul commence à partir de la date à laquelle les articles sont disponibles pour le prélèvement.

## Calcul d’une date de livraison demandée

Si vous spécifiez une date de livraison demandée sur la ligne vente, cette date devient le point de départ du calcul suivant :

- *Date livraison demandée - délai d’expédition = date d’expédition planifiée*
- *date d’expédition planifiée + délai désenlogement = date d’expédition*

Si les articles peuvent être prélevés à la date d’expédition, alors le processus vente peut continuer. Sinon, un avertissement de rupture de stock est affiché.

> [!NOTE]
> Si votre processus est basé sur un calcul en amont, par exemple, si vous utilisez la date livraison demandée pour obtenir la date livraison planifiée, nous vous recommandons d’utiliser des formules de date ayant des durées fixes, telles que "5D" pendant cinq jours ou "1W" pour une semaine. Les formules de date sans durée fixe, telles que « CW » pour la semaine en cours ou CM pour le mois en cours, peuvent entraîner des calculs de date incorrects. En savoir plus sur les formules de date en lisant la rubrique [Utiliser des dates civiles et des heures](ui-enter-date-ranges.md).

## Calcul de la première date de livraison possible

Si vous ne spécifiez aucune date livraison demandée sur une ligne de commande vente ou si la date livraison demandée ne peut pas être respectée, alors la première date à laquelle les articles sont disponibles est calculée. Cette date est ensuite renseignée dans le champ **Date d’expédition** sur la ligne, et la date à laquelle vous prévoyez d’expédier les articles, ainsi que la date à laquelle ces derniers seront livrés au client sont calculées via les formules suivantes.

- *Date d’expédition + délai désenlogement = date d’expédition planifiée*
- *Date livraison planifiée - délai d’expédition = date expédition planifiée*

## Voir la [formation Microsoft](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/) associée.

## Voir aussi

[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md)  
[Calculer des dates promesse livraison](sales-how-to-calculate-order-promising-dates.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
