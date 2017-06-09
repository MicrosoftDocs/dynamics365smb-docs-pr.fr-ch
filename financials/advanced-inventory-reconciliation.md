---
title: "Avancé : Rapprochement stock| Microsoft Docs"
description: "Décrit la manière dont la valeur du stock fait l&quot;objet d&quot;un rapprochement avec la comptabilité"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: post inventory cost to G/L, reconcile inventory
ms.date: 02/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7eb07530fe80f871ef113c95e48bf89da6c29db0
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
## <a name="advanced-inventory-reconciliation"></a>Avancé : Rapprochement compta.
Lorsque vous validez des mouvements de stock, tels que des expéditions vente, des factures achat ou des ajustements de stock, les coûts article modifiés sont enregistrés dans les écritures valeur. Pour refléter ces modifications de la valeur stock dans vos livres financiers, les coûts stocks sont automatiquement validés dans les comptes stock associés dans les écritures comptables. Pour chaque mouvement stock que vous validez, les valeurs appropriées sont validées dans le compte stocks, le compte ajustement et le compte validation stock dans la comptabilité.

Bien que les coûts soient automatiquement validés en comptabilité, il est malgré tout nécessaire de vous assurer que les coûts des biens sont transmis à la transaction de vente sortante associée, notamment dans les situations où vous vendez des biens avant de facturer l'achat. Il s'agit d'un ajustement des coûts. Le coût des articles est ajusté automatiquement lorsque vous validez des transactions article, mais vous pouvez également les ajuster manuellement. Pour en savoir plus, voir [Procédure : Ajuster coûts article](inventory-how-adjust-item-costs.md).

## <a name="see-also"></a>Voir aussi
[Stock](inventory-manage-inventory.md)  
[Avancé : Calcul du meilleur prix](advanced-best-price-calculation.md)

