---
title: "Détails de conception\_: périodes inventaire"
description: La fonction Périodes inventaire permet d’éviter ces problèmes avec les soldes et les évaluations du stock en ouvrant ou en clôturant des périodes d’inventaire pour limiter la validation dans une période définie.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-inventory-periods" />Détails de conception : périodes inventaire
Des transactions antidatées ou des ajustement des coûts affectent souvent les soldes et les évaluations du stock pour des périodes comptables qui peuvent être considérées comme clôturées. Ceci peut avoir des effets négatifs sur la précision des rapports, notamment dans des sociétés internationales. La fonction Périodes inventaire permet d’éviter ces problèmes en ouvrant ou en clôturant des périodes d’inventaire pour limiter la validation dans une période définie.  

 Une période inventaire est une période, définie par une date de fin, pendant laquelle vous validez des mouvements de stock. Lorsque vous fermez une période d’inventaire, aucun changement de valeur ne peut être validé dans la période clôturée. Cela inclut de nouvelles validations de valeur, des validations prévues ou facturées, des modifications sur les valeurs existantes et des ajustements de coûts. Cependant, vous pouvez toujours lettrer une écriture comptable article ouverte qui se trouve dans la période clôturée. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-application.md).  

 Pour s’assurer que toutes les écritures de transaction dans une période clôturée sont finales, les conditions suivantes doivent être remplies avant qu’une période d’inventaire ne soit fermée :  

-   Toutes les écritures comptables article sortantes de la période doivent être fermées (aucun stock négatif).  
-   Tous les coûts des articles pour la période doivent être ajustés.  
-   Tous les ordres de fabrication lancés et terminés dans la période doivent faire l’objet d’un ajustement des coûts.  

 Lorsque vous fermez une période inventaire, une écriture période d’inventaire est créée à l’aide du numéro du dernier enregistrement article tombant dans la période d’inventaire. En outre, le délai, la date et le code utilisateur de l’utilisateur clôturant la période sont enregistrés dans l’écriture période inventaire. À l’aide des informations associée au dernier historique article de la période précédente, vous pouvez visualiser les mouvements de stock qui ont été validés pour la période inventaire. Il est également possible de rouvrir des périodes inventaire si vous devez valider dans une période clôturée. Lorsque vous rouvrez une période inventaire, une écriture période inventaire est créée.  

## <a name="see-also" />Voir aussi

[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Utilisation de Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
