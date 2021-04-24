---
title: À propos des coûts des O.F. terminés | Microsoft Docs
description: L’achèvement de l’ordre de fabrication est une tâche importante de l’évaluation du cycle de vie de l’article en cours de production. Les coûts finaux, notamment les écarts dans un environnement de coût standard, les valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l’aide du traitement par lots Ajuster coûts - Écr. article.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b250a495504272b93565752043c23e1988ca1dab
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781076"
---
# <a name="about-finished-production-order-costs"></a>À propos des coûts des O.F. terminés
L’achèvement de l’ordre de fabrication est une tâche importante de l’évaluation du cycle de vie de l’article en cours de production. Les coûts finaux, notamment les écarts dans un environnement de coût standard, valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l’aide du traitement par lots **Ajuster coûts - Écr. article** qui permet d’opérer un rapprochement bancaire des coûts de production d’un article. Pour qu’un ordre de fabrication soit pris en considération pour un ajustement de coût, son statut doit être **Produit fini**. Il est donc essentiel qu’au moment de son achèvement, le statut d’un ordre de fabrication soit modifié en **Produit fini**.  

## <a name="example"></a>Exemple :  
 Dans un environnement de coût standard, lorsque vous consommez des matières pour produire un article, le coût de l’article, celui de la main-d’œuvre et celui des frais généraux sont répertoriés dans le TEC, pour définir simplement les choses. Lorsque l’article est produit, son coût standard est retranché du TEC. Généralement, le résultat de l’opération n’est pas égal à zéro. Pour que le résultat obtenu soit égal à zéro, vous devez exécuter le traitement par lots **Ajuster coûts - Écr. article** en sachant que seuls les ordres de fabrication dont l’état est **Produit fini** seront pris en considération pour l’ajustement.  

## <a name="see-also"></a>Voir aussi  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Production](production-manage-manufacturing.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]