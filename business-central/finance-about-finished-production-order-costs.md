---
title: À propos des coûts des O.F. terminés | Microsoft Docs
description: L'achèvement de l'ordre de fabrication est une tâche importante de l'évaluation du cycle de vie de l'article en cours de production. Les coûts finaux, notamment les écarts dans un environnement de coût standard, les valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l'aide du traitement par lots Ajuster coûts - Écr. article.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96cf025bbac137f61f41a65cbd2f9520f2c5e787
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "925368"
---
# <a name="about-finished-production-order-costs"></a>À propos des coûts des O.F. terminés
L'achèvement de l'ordre de fabrication est une tâche importante de l'évaluation du cycle de vie de l'article en cours de production. Les coûts finaux, notamment les écarts dans un environnement de coût standard, valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l'aide du traitement par lots **Ajuster coûts - Écr. article** qui permet d'opérer un rapprochement bancaire des coûts de production d'un article. Pour qu'un ordre de fabrication soit pris en considération pour un ajustement de coût, son statut doit être **Produit fini**. Il est donc essentiel qu'au moment de son achèvement, le statut d'un ordre de fabrication soit modifié en **Produit fini**.  

## <a name="example"></a>Exemple :  
 Dans un environnement de coût standard, lorsque vous consommez des matières pour produire un article, le coût de l'article, celui de la main-d'œuvre et celui des frais généraux sont répertoriés dans le TEC, pour définir simplement les choses. Lorsque l'article est produit, son coût standard est retranché du TEC. Généralement, le résultat de l'opération n'est pas égal à zéro. Pour que le résultat obtenu soit égal à zéro, vous devez exécuter le traitement par lots **Ajuster coûts - Écr. article** en sachant que seuls les ordres de fabrication dont l'état est **Produit fini** seront pris en considération pour l'ajustement.  

## <a name="see-also"></a>Voir aussi  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Production](production-manage-manufacturing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
