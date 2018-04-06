---
title: "Procédure : Configurer les conditions, niveaux et textes de relance livraison."
description: "Pour créer des relances livraison, vous devez configurer des conditions de relance livraison, des niveaux de relance livraison et des textes de relance livraison. messages"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 79416fcbb869395a625fa6bdae5ed004922c0250
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-delivery-reminder-terms-levels-and-text"></a>Configurer les conditions, niveaux et textes de relance livraison.
Pour créer des relances livraison, vous devez configurer ce qui suit :  

- Conditions de relance livraison  
- Niveaux de relance livraison  
- Message textuels de relance livraison  

Chaque condition de relance livraison a deux niveaux ou plusieurs niveaux de relance livraison, et pour chaque niveau de relance livraison, vous pouvez spécifier le texte constituant la relance livraison.  

Pour plus d'informations, voir [Relances livraison](delivery-reminders.md).  

## <a name="to-set-up-delivery-reminder-terms"></a>Pour configurer des conditions de relance livraison  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Conditions de relance livraison**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Code de la condition de relance livraison. Vous pouvez entrer 10 caractères alphanumériques maximum.|  
    |**Description**|Description de la condition de relance livraison. Vous pouvez entrer 30 caractères alphanumériques maximum.|  
    |**Nombre max. de relances livraison**|Nombre maximum de relances livraison qui peuvent être créées pour une commande.<br /><br /> **REMARQUE :** C'est le nombre maximal pour tous les niveaux de relance applicable à cette condition de relance. Par exemple, si vous avez configuré trois niveaux, et que vous définissez le **Nombre max. de relances livraison** à 5, la première relance est créée au niveau 1, la seconde au niveau 2, et les trois dernières au niveau 3.|  

4.  Cliquez sur le bouton **OK**.  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a>Pour ajouter des niveaux de relance livraison à une seule condition de relance livraison  

1.  Dans la fenêtre **Conditions de relance livraison**, sélectionnez la condition pour laquelle vous souhaitez configurer des niveaux, puis choisissez l'action **Niveaux**.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N°**|Numéro de niveau de relance livraison. Ce champ est complété automatiquement.|  
    |**Calcul de date d'échéance**|Formule permettant de calculer l'échéance de la relance livraison. Vous pouvez saisir une combinaison de chiffres de 0 à 9999 et des codes de date (J pour le jour, JS pour un jour de la semaine, S pour la semaine, M pour le mois, T pour le trimestre ou A pour l'année). Les codes de date indiquent le calcul de la date d'échéance de la relance livraison. Vous pouvez saisi un maximum de 20 caractères pour la formule de calcul de la date d'échéance.|  

4.  Cliquez sur le bouton **OK**.  

Pour chaque niveau de relance livraison, vous pouvez définir les messages texte qui sont ajoutés à la relance livraison. Vous pouvez définir le texte de début ajouté avant la description de la commande achat en retard et le texte de fin ajouté après la description de la commande achat en retard.  

La procédure suivante décrit comment configurer des messages texte de début, mais les mêmes étapes s'appliquent également pour configurer des messages texte de fin.  

## <a name="to-set-up-delivery-reminder-text-messages"></a>Pour configurer des messages textuels de relance livraison  

1.  Dans la fenêtre **Niveaux de relance livraison**, sélectionnez un niveau, puis sélectionnez l'action **Texte de début**.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Dans le champ **Description**, entrez le message texte de début de la relance livraison.  
4.  Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
 [relances livraison](delivery-reminders.md)   
 [Configurer des relances livraison](how-to-set-up-delivery-reminders.md)   
 [Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Créer manuellement des relances livraison](how-to-create-delivery-reminders-manually.md)   
 [Émettre des relances livraison](how-to-issue-delivery-reminders.md)

