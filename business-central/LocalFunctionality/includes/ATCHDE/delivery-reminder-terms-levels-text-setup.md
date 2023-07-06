---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
---

Pour créer des relances livraison, vous devez configurer ce qui suit :  

- Conditions de relance livraison  
- Niveaux de relance livraison  
- Message textuels de relance livraison  

Chaque condition de relance livraison a deux niveaux ou plusieurs niveaux de relance livraison, et pour chaque niveau de relance livraison, vous pouvez spécifier le texte constituant la relance livraison.  

## <a name="to-set-up-delivery-reminder-terms"></a><a name="to-set-up-delivery-reminder-terms"></a><a name="to-set-up-delivery-reminder-terms"></a>Pour configurer des conditions de relance livraison

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Conditions de relance livraison**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3. Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Code de la condition de relance livraison. Vous pouvez entrer 10 caractères alphanumériques maximum.|  
    |**Description**|Description de la condition de relance livraison. Vous pouvez entrer 30 caractères alphanumériques maximum.|  
    |**Nombre max. de relances livraison**|Nombre maximum de relances livraison qui peuvent être créées pour une commande.<br /><br /> **REMARQUE :** C'est le nombre maximal pour tous les niveaux de relance applicable à cette condition de relance. Par exemple, si vous avez configuré trois niveaux, et que vous définissez le **Nombre max. de relances livraison** à 5, la première relance est créée au niveau 1, la seconde au niveau 2, et les trois dernières au niveau 3.|  

4. Cliquez sur le bouton **OK**.  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a><a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a><a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a>Pour ajouter des niveaux de relance livraison à une seule condition de relance livraison

1. Dans la page **Conditions de relance livraison**, sélectionnez la condition pour laquelle vous souhaitez configurer des niveaux, puis choisissez l'action **Niveaux**.  
2. Sélectionnez l'action **Nouveau**.  
3. Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N°**|Numéro de niveau de relance livraison. Ce champ est complété automatiquement.|  
    |**Calcul de date d'échéance**|Formule permettant de calculer l'échéance de la relance livraison. Vous pouvez saisir une combinaison de chiffres de 0 à 9999 et des codes de date (J pour le jour, JS pour un jour de la semaine, S pour la semaine, M pour le mois, T pour le trimestre ou A pour l'année). Les codes de date indiquent le calcul de la date d'échéance de la relance livraison. Vous pouvez saisi un maximum de 20 caractères pour la formule de calcul de la date d'échéance.|  

4. Cliquez sur le bouton **OK**.  

Pour chaque niveau de relance livraison, vous pouvez définir les messages texte qui sont ajoutés à la relance livraison. Vous pouvez définir le texte de début ajouté avant la description de la commande achat en retard et le texte de fin ajouté après la description de la commande achat en retard.  

La procédure suivante décrit comment configurer des messages texte de début, mais les mêmes étapes s'appliquent également pour configurer des messages texte de fin.  

## <a name="to-set-up-delivery-reminder-text-messages"></a><a name="to-set-up-delivery-reminder-text-messages"></a><a name="to-set-up-delivery-reminder-text-messages"></a>Pour configurer des messages textuels de relance livraison

1. Dans la page **Niveaux de relance livraison**, sélectionnez un niveau, puis sélectionnez l'action **Texte de début**.  
2. Sélectionnez l'action **Nouveau**.  
3. Dans le champ **Description**, entrez le message texte de début de la relance livraison.  
4. Cliquez sur le bouton **OK**.  
