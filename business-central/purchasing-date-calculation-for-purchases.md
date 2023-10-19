---
title: Calculer les dates des achats
description: Cet article décrit comment vous pouvez calculer les dates des achats.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# <a name="calculate-dates-for-purchases"></a>Calculer les dates des achats

Si vous souhaitez avoir des articles dans le stock à une certaine date, [!INCLUDE[prod_short](includes/prod_short.md)] peut calculer automatiquement la date à laquelle vous devez les commander. 

Le résultat est la date à laquelle vous pouvez prélever les articles que vous avez commandés.  

Si vous spécifiez une date de réception demandée sur une ligne commande achat, la date de commande calculée est la date à laquelle vous devez passer la commande. La date à laquelle les articles pourront être prélevés s’affiche dans le champ **Date réception prévue**.  

Si vous ne spécifiez pas de date réception demandée, la date à laquelle vous prévoyez de recevoir les articles est basée sur la date de commande sur la ligne. 

La date de réception est également la date à laquelle les articles seront disponibles pour être prélevés.  

> [!TIP]
> Par défaut, de nombreux champs de date mentionnés dans cet article sont masqués sur les lignes commande achat. Si un champ n’est pas disponible, vous pouvez l’ajouter en personnalisant la page. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a>Calcul avec une date réception demandée

Si la ligne commande achat indique une date réception demandée, le programme l’utilise comme base pour les calculs suivants :  

- date réception demandée - délai réapprovisionnement = date commande  
- date réception demandée + délai enlogement + délai sécurité = date réception prévue  

Si vous spécifiez une date de réception demandée sur une ligne commande achat, cette date est affectée aux nouvelles lignes au fur et à mesure que vous les créez. Vous pouvez modifier ou supprimer la date sur les lignes.  

> [!NOTE]
> Si votre processus est basé sur un calcul en amont, par exemple, si vous utilisez la date de réception demandée pour obtenir la date de commande, nous vous recommandons d’utiliser des formules de date ayant des durées fixes, telles que "5D" pendant cinq jours ou "1W" pour une semaine. Les formules de date sans durée fixe, telles que « CW » pour la semaine en cours ou CM pour le mois en cours, peuvent entraîner des calculs de date incorrects. Pour plus d’informations sur les formules de date, voir [Utiliser des dates civiles et des heures](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date"></a>Calcul sans date réception demandée

Si vous indiquez une ligne commande achat sans date de réception demandée, le champ **Date commande** sur la ligne indique la date du champ **Date commande** sur l’en-tête commande achat. Cette date est celle que vous avez indiquée ou la date de travail. Les dates sont ensuite calculées pour la ligne commande achat, la date commande étant utilisée comme point de départ, comme suit :  

- date commande + délai réapprovisionnement = date livraison fourn. prévue  
- date livraison fourn. prévue + délai enlogement + délai sécurité = date réception prévue  

Si vous modifiez la date de commande sur la ligne, [!INCLUDE[prod_short](includes/prod_short.md)] recalcule les autres dates.  

## <a name="default-values-for-lead-time-calculation"></a>Valeurs par défaut du délai de réapprovisionnement

[!INCLUDE[prod_short](includes/prod_short.md)] utilise la formule de date dans le champ **Délai de réappro.** sur la ligne commande achat pour calculer la commande et les dates réception prévues.  

Vous pouvez spécifier manuellement la formule de date sur les lignes. Sinon, [!INCLUDE[prod_short](includes/prod_short.md)] utilisera les formules qui sont définies sur les pages suivantes dans l’ordre de priorité suivant :

1. Catalogue d'articles par fournisseur
2. Fiche article
3. Fiche point de stock
4. Fiche fournisseur

## <a name="see-also"></a>Voir aussi

[Calcul de la date des ventes](sales-date-calculation-for-sales.md)  
[Calcul des dates promesse livraison](sales-how-to-calculate-order-promising-dates.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
