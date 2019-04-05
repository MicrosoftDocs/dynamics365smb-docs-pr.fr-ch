---
title: "Procédure : clôturer les écritures comptables article ouvertes qui résultent d'un lettrage fixe dans la feuille article | Microsoft Docs"
description: Vous pouvez utiliser le champ **Lettrage à partir écriture** de la page **Feuille article** pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale. Par exemple, pour corriger la transaction sortante ou pour traiter un retour.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820722"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Clôturer les écritures comptables article ouvertes qui résultent d'un lettrage fixe dans la feuille article
Vous pouvez utiliser le champ **Lettrage à partir écriture** de la page **Feuille article** pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale. Par exemple, pour corriger la transaction sortante ou pour traiter un retour. Pour plus d'informations, voir Lettrage à partir écriture.  

> [!IMPORTANT]  
>  Les lettrages fixes exécutés de cette manière s'appliquent uniquement au coût, non à la quantité. Par conséquent, l'écriture comptable article positive enregistrée ne ferme pas l'écriture sortante rapprochée et demeure ouverte elle-même. Cela s'applique également lorsque vous validez un lettrage fixe pour une écriture positive vers une écriture négative qui n'a pas été clôturée par une écriture positive ordinaire ; les écritures négatives et positives restent ouvertes.  
>   
>  Cela signifie également que vous ne pouvez pas clôturer une période inventaire si une telle écriture existe.  

La procédure suivante explique comment clôturer des écritures de ce genre au cours de deux validations de correction dans la feuille article.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Pour clôturer les écritures comptables article ouvertes qui résultent d'un lettrage fixe dans la feuille article  

1.  Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement positif avec la quantité correspondante. Cela permet de clôturer l'écriture négative initiale avec un lettrage fixe.  
2.  Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement négatif. Cela permet de clôturer l'écriture positive de correction initiale avec un lettrage fixe.  

## <a name="see-also"></a>Voir aussi  
[Supprimer et relettrer des écritures comptables article](finance-how-to-remove-and-reapply-item-entries.md)  
 [Traiter les retours et annulations de ventes](sales-how-process-sales-returns-cancellations.md)   
 [Configuration de l'évaluation du stock](finance-set-up-inventory-valuation-and-costing.md)   
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)   
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md)
