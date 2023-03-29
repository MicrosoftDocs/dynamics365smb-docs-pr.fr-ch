---
title: Utiliser les périodes inventaire
description: Vous pouvez contrôler le délai de validation des modifications du stock en définissant des périodes inventaire.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 04/01/2021
ms.author: edupont
---
# Utiliser les périodes inventaire

Les périodes inventaire sont des périodes au cours desquelles vous pouvez valider des modifications de stock. Une période inventaire est définie par la date à laquelle elle se termine. Lorsque vous clôturez une période inventaire, vous ne pouvez pas valider de modifications de stock, qu’elles soient prévues ou facturées, avant cette date fin. Vous ne pouvez pas valider de nouvelles valeurs dans le stock avant la date fin. Si vous avez des écritures article ouvertes dans la période clôturée, ce qui signifie des quantités positives qui n’ont pas encore été lettrées sur des transactions sortantes, vous pouvez encore lettrer des quantités sortantes sur ces écritures, même si la période est clôturée.  

Les sections suivantes décrivent comment :

* Créer des périodes inventaire.  
* Clôturer des périodes inventaire.  
* Rouvrir des périodes inventaire.  

## Pour créer une période inventaire

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Périodes inventaire**, puis choisissez le lien associé.  
2. Créez une ligne.  
3. Dans le champ **Date fin**, entrez la dernière date que vous voulez définir pour la période inventaire. Une fois la période clôturée, vous ne pouvez plus valider de modifications de stock antérieures à cette date.  
4. Saisissez un nom descriptif dans le champ **Nom**. Cliquez sur le bouton **OK**.  

## Clôture de périodes inventaire

Le champ **Clôturé** indique si la période inventaire est clôturée ou non sur des modifications de valeur de stock. Vous ne pouvez pas modifier ce champ.  

Vous pouvez clôturer toute période inventaire, pour autant que les conditions suivantes soient vraies :  

* Il n’y a pas d’écritures comptables article sortantes ouvertes dans cette période, ce qui signifie que le stock est négatif.  
* Le coût de tous les articles a été ajusté à l’aide du traitement par lots **Ajuster coût écritures article**.  

Cela signifie que toutes les quantités de transaction sortante, telles que celles des commandes vente, désenlogements transfert, factures vente, retours achat ou avoirs achat doivent être lettrées sur la quantité en stock.  

### Pour fermer une période inventaire  

1. Avant de clôturer une période inventaire, sélectionnez l’action **Ajuster coût écritures article** pour vous assurer que tous les ajustements des coûts sont validés.

    Exécutez l’état **Clôturer période inventaire – Test** pour déterminer s’il y a des écritures article sortant ouvertes dans la période inventaire ou des articles dont le coût n’a pas encore été ajusté.  
2. Choisissez l’action **Clôturer période inventaire - Test**.  

    Exécutez le traitement par lots **Valider coûts ajustés** pour vous assurer que tous les coûts sont validés dans la comptabilité.  
3. Cliquez sur l’action **Valider stock en comptabilité**.  
4. Ouvrez la page **Périodes inventaire** et sélectionnez la période inventaire que vous voulez clôturer.  
5. Choisissez l’action **Clôturer période**. Une fois la période inventaire clôturée, vous ne pouvez pas valider de modifications de stock avant la date de fin. Le coût de tous les articles doit être ajusté avec le traitement par lots **Ajuster coût écritures article** avant la clôture de la période inventaire.  
6. Cliquez sur le bouton **Oui** pour confirmer la clôture de la période, ou choisissez **Non** pour annuler la clôture.  
7. La période inventaire est clôturée et un message de confirmation est affiché une fois l’opération terminée.  

## Réouverture de périodes inventaire  
Une fois la période inventaire clôturée, vous ne pouvez plus la supprimer. En revanche, vous pouvez la rouvrir si vous voulez autoriser sa validation avant la date fin. La réouverture d’une période rouvre également toutes les périodes inventaire dont la date fin est postérieure à la fin de la période que vous rouvrez.  

### Pour réouvrir une période inventaire  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Périodes inventaire**, puis choisissez le lien associé.  
2. Sélectionnez la période inventaire que vous voulez rouvrir.  
3. Sélectionnez l’action de la période **Rouvrir période**. Confirmez que vous voulez réouvrir la période.  
4. Toutes les périodes inventaire dont la date fin est postérieure à la fin de la période sélectionnée sont réouvertes.  

## Voir aussi  
[Détails de conception : périodes inventaire](design-details-inventory-periods.md)  
[Finances](finance.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser Financials](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]