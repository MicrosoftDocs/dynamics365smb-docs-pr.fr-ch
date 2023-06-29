---
title: Clôture des écritures comptables article provenant de l’utilisation d’une application fixe
description: Découvrez comment vous pouvez créer un lettrage fixe entre une transaction entrante et la transaction sortante initiale dans la feuille article.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 40
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article

Vous pouvez utiliser le champ **Lettrage à partir écriture** de la page **Feuille article** pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale. Par exemple, pour corriger la transaction sortante ou pour traiter un retour.  

> [!IMPORTANT]  
> Les lettrages fixes exécutés de cette manière s’appliquent uniquement au coût, non à la quantité. Par conséquent, l’écriture comptable article positive enregistrée ne ferme pas l’écriture sortante rapprochée et demeure ouverte elle-même. Cela s’applique également lorsque vous validez un lettrage fixe pour une écriture positive vers une écriture négative qui n’a pas été clôturée par une écriture positive ordinaire ; les écritures négatives et positives restent ouvertes.  
>
> Cela signifie également que vous ne pouvez pas clôturer une période inventaire si une telle écriture existe.  

Vous pouvez modifier et relettrer des écritures lettrage dans certaines conditions à l’aide de la page **Feuille lettrage**.  

La procédure suivante explique comment clôturer des écritures de ce genre au cours de deux validations de correction dans la feuille article.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Pour clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article

1. Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement positif avec la quantité correspondante. Cela permet de clôturer l’écriture négative initiale avec un lettrage fixe.  

    Le champ **Lettrage à partir d’écritures** spécifie le numéro de l’écriture comptable article sortant dont le coût est transmis à l’écriture comptable article entrant lorsque vous validez une transaction entrante de type **Ajustement positif** ou **Achats** avec la feuille article.  
2. Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement négatif. Cela permet de clôturer l’écriture positive de correction initiale avec un lettrage fixe.  

    Le champ **Lettrage à partir d’écritures** spécifie si la quantité dans la ligne feuille article doit être lettrée dans un document déjà validé. Si c’est le cas, entrez le numéro de l’écriture comptable article dans laquelle la ligne feuille article doit être lettrée.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Supprimer et relettrer des écritures comptables article](finance-how-to-remove-and-reapply-item-entries.md)  
[Traiter les retours et annulations de ventes](sales-how-process-sales-returns-cancellations.md)  
[Configuration de l’évaluation du stock](finance-set-up-inventory-valuation-and-costing.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Détails de conception : modes évaluation stock](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
