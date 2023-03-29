---
title: "Configuration de meilleures pratiques\_: mode évaluation stock"
description: Le champ Mode évaluation stock de la fiche article spécifie la manière dont le flux des coûts de l’article est enregistré et si une valeur réelle ou budgétée est capitalisée et utilisée dans le calcul des coûts.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '30, 31'
ms.date: 04/01/2021
ms.author: edupont
---
# Configuration de meilleures pratiques : mode évaluation stock

Le champ **Mode évaluation stock** de la fiche article spécifie la manière dont le flux des coûts de l’article est enregistré et si une valeur réelle ou budgétée est capitalisée et utilisée dans le calcul des coûts.  

La définition du mode évaluation stock correct en fonction du type d’article et de l’environnement d’entreprise est importante pour assurer des stocks économiques.  

Le tableau suivant fournit les meilleures pratiques sur la procédure de configuration du champ **Mode évaluation stock**. Pour plus d’informations, [Détails de conception : modes évaluation stock](design-details-costing-methods.md).  

|Option de configuration|Meilleure pratique|Commentaire|  
|------------------|-------------------|-------------|  
|FIFO|Utilisez ceci lorsque le coût du produit est stable.<br /><br /> Utilisez ceci pour les articles à durée de conservation limitée, car les produits les plus anciens doivent être vendus avant que leur date limite de vente ne soit dépassée.|Le coût unitaire d’un article est la valeur réelle de toute réception de l’article, sélectionnée par la règle FIFO.<br /><br /> Dans l’évaluation du stock, nous considérons que les premiers articles stockés sont ceux vendus en premier. **Note :** lorsque les prix augmentent, le bilan indique une valeur plus élevée. Cela signifie que les impôts à payer augmentent, mais que les cotes de crédit et la capacité à emprunter de la trésorerie s’améliorent.|  
|LIFO|Utilisez ceci lorsque les niveaux de stock sont maintenus ou augmentés de façon continue dans le temps.|Le coût unitaire d’un article est la valeur réelle de toute réception de l’article, sélectionnée par la règle LIFO.<br /><br /> Dans l’évaluation du stock, nous considérons que les derniers articles stockés sont ceux vendus en premier. **Note :** lorsque les prix augmentent, la valeur du compte de gestion diminue. Cela signifie que les impôts à payer diminuent, mais que la capacité à emprunter de la trésorerie se détériore. **Important :** interdit dans de nombreux pays/régions, car cela peut être utilisé pour réduire la marge.|  
|Moyenne|Utilisez ceci lorsque le coût du produit n’est pas stable.<br /><br /> Utilisez ceci lorsque les stocks sont compilés ou mélangés ensemble et ne peuvent pas être différenciés (par exemple, des produits chimiques).|Le coût unitaire d’un article est calculé comme le coût unitaire moyen à chaque moment après un achat.<br /><br /> Pour l’évaluation du stock, on part de l’hypothèse que tous les stocks sont vendus simultanément.|
|Spécifique|Utilisez ceci pour la fabrication ou la transaction d’articles facilement identifiables ayant des coûts unitaires assez élevés.<br /><br /> Utiliser pour des articles soumis à une régulation.<br /><br /> Utilisez ceci pour les articles ayant des numéros de série.|Le coût unitaire d’un article est le coût exact auquel l’unité particulière a été reçue.|
|Standard|Utilisez ceci lorsque le contrôle des coûts est primordial.<br /><br /> Utilisez ceci pour la fabrication répétitive, afin d’évaluer les coûts matière directs, les frais de main-d’œuvre directs, et les frais généraux matière.<br /><br /> Utilisez ceci lorsqu’il existe une discipline et du personnel pour le maintien des standards.|Le coût unitaire d’un article est prédéfini sur la base d’une estimation.<br /><br /> Lorsque le coût réel est réalisé plus tard, le coût standard doit être ajusté au coût réel à l’aide des valeurs d’écart.|  

## Voir aussi

[Détails de conception : modes évaluation stock](design-details-costing-methods.md)  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Configurer des domaines d’application complexes à l’aide des meilleures pratiques](set-up-complex-application-areas-using-best-practices.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]