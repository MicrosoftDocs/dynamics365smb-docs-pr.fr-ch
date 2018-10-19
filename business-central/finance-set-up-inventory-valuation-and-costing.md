---
title: "Configuration de l'évaluation du stock | Microsoft Docs"
description: "Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Configuration de l'évaluation du stock
Pour vous assurer que les coûts ajustés sont enregistrés correctement, vous devez configurer plusieurs champs et fenêtres avant de commencer à effectuer des transactions article.

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer une méthode d'évaluation des stocks au prix coûtant pour chaque article pour régir la manière dont son coût entrant est utilisé pour évaluer la valeur du stock et le coût des biens vendus.|[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)|  
|S'assurer que les coûts sont automatiquement validés dans la comptabilité lorsqu'un mouvement de stock est validé.|Champ **Compta. coûts automatique** de la fenêtre **Paramètres stock**|  
|S'assurer que les coûts prévus sont validés dans la comptabilité afin de visualiser, à partir des comptes généraux en attente, une estimation des montants dus et du coût des articles échangés avant qu'ils ne soient effectivement facturés.|Champ **Compta. coûts prévus** de la fenêtre **Paramètres stock**|  
|Configurer le système afin d'ajuster automatiquement toute modification des coûts chaque fois que vous validez des mouvements de stock.|[Ajuster coûts et prix article](inventory-how-adjust-item-costs.md)|  
|Définir si le coût moyen doit être calculé uniquement par article ou par article pour chaque référence SKU et pour chaque variante de l'article.|Champ **Type calcul coût moyen** de la fenêtre **Paramètres stock**|  
|Sélectionner la période que le programme doit utiliser pour calculer le coût moyen pondéré des articles qui utilisent la méthode évaluation stock Moyen.|Champ **Période coût moyen** de la fenêtre **Paramètres stock**|  
|Définir des périodes inventaire pour contrôler la valeur du stock dans le temps en refusant d'accorder la validation de transactions lorsque les périodes inventaire sont clôturées.|[Utiliser les périodes inventaire](finance-how-to-work-with-inventory-periods.md)|  
|S'assurer que les retours vente sont rapprochés des transactions sortantes afin de préserver la valeur du stock.|Champ**Coût retour identique obligatoire** de la fenêtre **Ventes**|  
|S'assurer que les retours achat sont rapprochés des transactions entrantes afin de préserver la valeur du stock.|Champ**Coût retour identique obligatoire** de la fenêtre **Achats**|
|Configurer les règles d'arrondi à appliquer lors de l'ajustement ou de la proposition des prix article et lors de l'ajustement ou de la proposition des coûts standard.|Fenêtre **Mode arrondi**|  

## <a name="see-also"></a>Voir aussi  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Utilisation de Business Central](ui-work-product.md)  
[Finances](finance.md)  

