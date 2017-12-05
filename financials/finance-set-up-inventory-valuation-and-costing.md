---
title: "Configuration de l'évaluation du stock | Microsoft Docs"
description: "Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 86fd8f6b15b8a2f868db2938278df6147a092725
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Configuration de l'évaluation du stock
Pour vous assurer que les coûts ajustés sont enregistrés correctement, vous devez configurer plusieurs champs et fenêtres avant de commencer à effectuer des transactions article.

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer une méthode d'évaluation des stocks au prix coûtant pour chaque article pour régir la manière dont son coût entrant est utilisé pour évaluer la valeur du stock et le coût des biens vendus.|[Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md)|  
|S'assurer que les coûts sont automatiquement validés dans la comptabilité lorsqu'un mouvement de stock est validé.|Champ **Compta. coûts automatique** de la page **Paramètres stock**|  
|S'assurer que les coûts prévus sont validés dans la comptabilité afin de visualiser, à partir des comptes généraux en attente, une estimation des montants dus et du coût des articles échangés avant qu'ils ne soient effectivement facturés.|Champ **Compta. coûts prévus** de la page **Paramètres stock**|  
|Configurer le système afin d'ajuster automatiquement toute modification des coûts chaque fois que vous validez des mouvements de stock.|[Procédure : ajustement des coûts article](inventory-how-adjust-item-costs.md)|  
|Définir si le coût moyen doit être calculé uniquement par article ou par article pour chaque référence SKU et pour chaque variante de l'article.|Champ **Type calcul coût moyen** de la page **Paramètres stock**|  
|Sélectionner la période que le programme doit utiliser pour calculer le coût moyen pondéré des articles qui utilisent la méthode évaluation stock Moyen.|Champ **Période coût moyen** de la page **Paramètres stock**|  
|Définir des périodes inventaire pour contrôler la valeur du stock dans le temps en refusant d'accorder la validation de transactions lorsque les périodes inventaire sont clôturées.|[Procédure : utiliser les périodes inventaire](finance-how-to-work-with-inventory-periods.md)|  
|S'assurer que les retours vente sont rapprochés des transactions sortantes afin de préserver la valeur du stock.|Champ**Coût retour identique obligatoire** de la page **Ventes**|  
|S'assurer que les retours achat sont rapprochés des transactions entrantes afin de préserver la valeur du stock.|Champ**Coût retour identique obligatoire** de la page **Achats**|
|Configurer les règles d'arrondi à appliquer lors de l'ajustement ou de la proposition des prix article et lors de l'ajustement ou de la proposition des coûts standard.|Page **Mode arrondi**|  

## <a name="see-also"></a>Voir aussi  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Utilisation de Dynamics 365](ui-work-product.md)  
[Finances](finance.md)  

