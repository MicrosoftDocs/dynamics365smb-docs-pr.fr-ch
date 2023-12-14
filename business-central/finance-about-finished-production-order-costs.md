---
title: À propos des coûts des O.F. terminés
description: "La finition de l’ordre de fabrication est essentielle pour terminer le cycle de vie des coûts d’un article de production. Les coûts finaux sont calculés dans le traitement par lots Ajuster coûts\_: Écr. article."
author: brentholtorf
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: bholtorf
---
# À propos des coûts des O.F. terminés

L’achèvement de l’ordre de fabrication est une tâche importante de l’évaluation du cycle de vie de l’article en cours de production. Les coûts finaux, notamment les écarts dans un environnement de coût standard, valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l’aide du traitement par lots **Ajuster coûts - Écr. article** qui permet d’opérer un rapprochement bancaire des coûts de production d’un article. Pour qu’un ordre de fabrication soit pris en considération pour un ajustement de coût, son statut doit être **Produit fini**. Il est donc essentiel qu’au moment de son achèvement, le statut d’un ordre de fabrication soit modifié en **Produit fini**.  

## Exemple :

Dans un environnement de coût standard, lorsque vous consommez des matières pour produire un article, le coût de l’article, celui de la main-d’œuvre et celui des frais généraux sont répertoriés dans le TEC, pour définir simplement les choses. Lorsque l’article est produit, son coût standard est retranché du TEC. Généralement, le résultat de l’opération n’est pas égal à zéro. Pour que le résultat obtenu soit égal à zéro, vous devez exécuter le traitement par lots **Ajuster coûts - Écr. article** en sachant que seuls les ordres de fabrication dont l’état est **Produit fini** seront pris en considération pour l’ajustement.  

## Voir aussi

[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Production](production-manage-manufacturing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]