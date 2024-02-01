---
title: Détails de conception - Lettrage article | Microsoft Docs
description: Cette rubrique décrit où la quantité et la valeur de stock sont enregistrées lorsque vous validez un mouvement stock.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, items, ledger entries, posting, inventory'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-item-application"></a>Détails de conception : lettrage article

Lorsque vous validez une transaction de stock, la validation de quantité est enregistrée dans les écritures comptables article, la validation de valeur dans les écritures valeur. Pour plus d’informations, voir [Détails de conception : comptabilisation stock](design-details-inventory-posting.md).  

De même, un lettrage article est effectué pour lier le destinataire de coût à sa source de coût pour assurer le transfert de coûts en fonction de la méthode d’évaluation du stock. Pour plus d’informations, [Détails de conception : modes évaluation stock](design-details-costing-methods.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] effectue deux types de lettrage article.  

|Type de lettrage|Désignation|  
|----------------------|---------------------------------------|  
|Lettrage de quantité|Créé pour tous les mouvements de stock|  
|Coût lettré|Créé pour les écritures entrantes conjointement à un lettrage de quantité, en tant que résultat de l’interaction utilisateur dans des processus spécifiques.|  

Les lettrages article peuvent être effectués des manières suivantes.  

|Méthode|Désignation|Type de lettrage|  
|------------|---------------------------------------|----------------------|  
|Automatique|Se produit en tant que transfert de coûts général selon le mode évaluation stock|Lettrage de quantité|  
|Statique|Effectué par l’utilisateur lorsque :<br /><br /> -   Traitement des retours<br />-   Validation de corrections<br />-   Annulation des validations de quantité<br />-   Création de livraisons directes **Remarque :**  Le lettrage fixe peut être effectué manuellement en saisissant un numéro de séquence dans le champ **Écriture article à lettrer** ou à l’aide d’une fonction, telle que **Afficher des lignes document validées à contrepasser**.|Lettrage de quantité<br /><br /> Coût lettré **Remarque :**  L’application coût se produit uniquement avec des transactions entrantes dont le champ **Écriture article à lettrer** est renseigné pour créer un lettrage fixe. Consultez la table suivante.|  

La réalisation des applications de quantité ou applications de coût dépend dépend de la direction de la transaction de stock et si l’application d’article est automatique ou fixe, en fonction des processus spécifiques.  

Le tableau suivant montre, à l’aide des champs de lettrage principaux sur les lignes mouvement de stock, la manière dont les coûts circulent en fonction de la direction de transaction. Il indique aussi la date et la raison pour laquelle le lettrage article est de type quantité ou coût.  

|-|Champ Écr. article à lettrer|Champ Écriture article à lettrer|  
|-|--------------------------------|----------------------------------|  
|Lettrage pour écriture sortante|L’écriture sortante extrait le coût de l’écriture entrante ouverte.<br /><br /> **Lettrage de quantité**|Non pris en charge|  
|Lettrage pour écriture entrante|L’écriture entrante impose le coût sur l’écriture sortante ouverte.<br /><br /> L’écriture entrante est la source du coût.<br /><br /> **Lettrage de quantité**|L’écriture entrante extrait le coût de l’écriture sortante. **Remarque :** Lors de la réalisation de cette application fixe, la transaction entrante est traitée comme retour vente. Par conséquent, l’écriture de sortie appliquée reste ouverte. <br /><br /> L’écriture entrante n’est PAS la source du coût.<br /><br /> **Coût lettré**|  

> [!IMPORTANT]  
> Un retour vente n’est PAS considéré comme une source de coût quand il est lettré de façon fixe.  
>
> Les écriture vente restent ouvertes jusqu’à ce que la source réelle soit validée.  

Une écriture lettrage article enregistre les informations suivantes.  

|Champ|Désignation|  
|---------------------------------|---------------------------------------|  
|**N° écriture comptable article**|numéro de l’écriture comptable article correspondant à la transaction pour laquelle cette écriture lettrage est créée.|  
|**N° écriture article entrant**|Numéro d’écriture comptable article de l’entrée de stock à laquelle la transaction doit être liée, le cas échéant.|  
|**N° écriture article sortant**|Numéro d’écriture comptable article de la sortie de stock à laquelle la transaction doit être liée, le cas échéant.|  
|**Quantité**|quantité lettrée.|  
|**Date de validation**|date de comptabilisation de la transaction.|  

## <a name="inventory-increase"></a>Entrée de stock
Lorsque vous validez une entrée de stock, une simple écriture lettrage article est enregistrée sans lettrage dans une écriture sortante.  

### <a name="example"></a>Exemple :
Le tableau suivant montre l’écriture lettrage article qui est créée lorsque vous validez une réception achat de 10 unités.  

|Date comptabilisation|N° écriture article entrant|N° écriture article sortant|Quantité|N° écriture comptable article|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01/01/20|1|0|10|1|  

## <a name="inventory-decrease"></a>Sortie de stock
Lorsque vous validez une sortie de stock, une écriture lettrage article qui lie la sortie de stock à une entrée de stock est créée. Ce lien est créé en utilisant le mode évaluation stock de l’article comme base d’instructions. Pour les articles utilisant les modes évaluation du stock FIFO, standard, et moyen, le lien est basé sur le principe du premier entré, premier sorti. La sortie de stock est lettrée avec l’entrée de stock ayant la date comptabilisation la plus proche. Pour les articles utilisant le mode évaluation stock LIFO, le lien est basé sur le principe du dernier entré, premier sorti. La sortie de stock est lettrée avec l’entrée de stock ayant la date comptabilisation la plus récente.  

Dans la table **Ecriture article**, le champ **Quantité restante** présente la quantité qui n’a pas encore été lettrée. Si la quantité restante est supérieure à 0, la case à cocher **Ouvrir** est activée.  

### <a name="example-1"></a>Exemple :
L’exemple suivant montre l’écriture lettrage article créée lors de la validation d’une expédition vente de 5 unités des articles réceptionnés dans l’exemple précédent. La première écriture lettrage article est la réception achat. La deuxième écriture lettrage est l’expédition vente.  

Le tableau suivant montre les deux écritures lettrage article qui résultent de l’entrée de stock et de la sortie de stock, respectivement.  

|Date comptabilisation|N° écriture article entrant|N° écriture article sortant|Quantité|N° écriture comptable article|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01/01/20|1|0|10|1|  
|03/01/20|1|2|-5|2|  

## <a name="fixed-application"></a>Lettrage fixe
Vous effectuez un lettrage fixe lorsque vous spécifiez que le coût d’une entrée de stock doit être lettré sur une sortie de stock spécifique ou inversement. Ce lettrage fixe affecte les quantités restantes des écritures, mais le lettrage fixe rétablit également le coût exact de l’écriture d’origine sur laquelle vous lettrez (ou à partir de laquelle vous lettrez).  

Pour créer un lettrage fixe, vous utilisez les champs **Écr. article de lettrage** ou **Écr. article à lettrer** des lignes document pour spécifier l’écriture comptable article sur laquelle \(ou à partir de laquelle\) vous voulez que la ligne de transaction soit lettrée. Par exemple, vous pouvez effectuer un lettrage fixe lorsque vous voulez créer un coût lettré qui spécifie qu’un retour vente doit être lettré sur une expédition vente spécifique afin de contrepasser le coût de l’expédition vente. Dans ce cas, [!INCLUDE[prod_short](includes/prod_short.md)] ignore le mode d’évaluation du stock et lettre la sortie de stock (ou l’entrée de stock en cas de retour vente) sur l’écriture comptable article que vous spécifiez. L’avantage d’effectuer un lettrage fixe est que le coût de la transaction initiale est transmis à la nouvelle transaction.  

### <a name="example--fixed-application-in-purchase-return"></a>Exemple – lettrage fixe dans le retour achat
L’exemple suivant, qui illustre l’effet du lettrage fixe d’un retour achat d’un article utilisant le mode d’évaluation du stock FIFO, est basé sur le scénario suivant :  

1. Dans la séquence 1, l’utilisateur valide un achat à un coût de 10,00 DS.  
2. Dans la séquence 2, l’utilisateur valide un achat à un coût de 20,00 DS.  
3. Dans la séquence 3, l’utilisateur valide un retour achat. L’utilisateur effectue un lettrage fixe au second achat en saisissant le numéro d’écriture comptable article dans le champ **Écr. article à lettrer** sur la ligne retour achat.  

Le tableau suivant montre des écritures comptables article résultant de ce scénario.  

|**Date de validation**|**Type écriture comptable article**|**Quantité**|**Coût total (réel)**|**N° écriture comptable article**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|04/01/20|Achats|10|10.00|1|  
|05/01/20|Achats|10|20.00|2|  
|06/01/20|Achat (retour)|-10|-20,00|3|  

Comme un lettrage fixe est effectué du retour achat vers la deuxième écriture achat, les articles doivent être retournés au coût correct. Si l’utilisateur n’avait pas effectué le lettrage fixe, l’article retourné serait évalué de façon incorrecte à 10,00 DS parce que le retour aurait été lettré dans la première écriture achat en fonction de la méthode FIFO.  

Le tableau suivant montre l’écriture lettrage article générée par le lettrage fixe.  

|Date comptabilisation|N° écriture article entrant|N° écriture article sortant|Quantité|N° écriture comptable article|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|06/01/20|2|3|10|3|  

Le coût du second achat, 20,00 DS, est ensuite transmis correctement au retour achat.  

### <a name="example--fixed-application-with-average-cost"></a>Exemple – lettrage fixe avec le coût moyen
L’exemple suivant, qui indique l’effet du lettrage fixe, est basé sur le scénario suivant pour un article qui utilise le mode évaluation stock moyen :  

1. Dans les numéros de séquence 1 et 2, l’utilisateur valide deux factures achat. La seconde facture a un coût unitaire direct incorrect de 1000,00 DS.  
2. Dans le numéro de séquence 3, l’utilisateur valide un avoir achat, avec un lettrage fixe appliqué à l’écriture achat avec le coût unitaire direct incorrect. La somme du champ **Coût total (réel)** des deux écritures valeur lettrées fixes devient 0,00  
3. Dans le numéro de séquence 4, l’utilisateur valide une autre facture achat avec le coût unitaire direct correct de 100,00 DS.  
4. Dans le numéro de séquence 5, l’utilisateur valide une facture vente.  
5. La quantité en stock est 0, et la valeur stock est aussi égale à 0,00  

Le tableau suivant montre le résultat du scénario dans les écritures valeur de l’article.  

Le tableau suivant présente le résultat du scénario sur les entrées de valeur de l’article une fois la comptabilisation terminée et l’ajustement des coûts exécuté.

|Date comptabilisation|Type écriture comptable article|Quantité valorisée|Coût total (réel)|Écr. article à lettrer|Valorisé par coût moyen|N° écriture comptable article|N° écriture|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01/01/20|Achats|1|200.00||Non|1|1|  
|01/01/20|Achats|1|1000.00||Non|2|2|  
|01/01/20|Achats|-1|-1 000|2|Non|3|3|  
|01/01/20|Achats|1|100,00||Non|4|4|  
|01/01/20|Vente|-2|-300,00||Oui|5|5|  

Si l’utilisateur n’avait pas effectué le lettrage fixe entre l’avoir achat et l’achat avec le coût unitaire direct incorrect (étape 2 dans le scénario précédent), le coût aurait été ajusté de façon différente.  

Le tableau suivant montre le résultat dans les écritures valeur de l’article si l’étape 2 dans le scénario précédent est effectuée sans lettrage fixe.  

|Date comptabilisation|Type écriture comptable article|Quantité valorisée|Coût total (réel)|Écr. article à lettrer|Valorisé par coût moyen|N° écriture comptable article|N° écriture|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01/01/20|Achats|1|200.00||Non|1|1|  
|01/01/20|Achats|1|1000.00||Non|2|2|  
|01/01/20|Achats|-1|433,33||Oui|3|3|  
|01/01/20|Achats|1|100,00||Non|4|4|  
|01/01/20|Vente|-2|866,67||Oui|5|5|  

Dans le numéro de séquence 3, la valeur du champ **Coût total (réel)** est évaluée par moyenne et comprend donc la validation erronée de 1000,00. Par conséquent, il prend la valeur -433,33, ce qui représente un coût total gonflé. Le calcul est le suivant 1 300 / 3 = .-433,33.  

Dans le numéro de séquence 5, la valeur du champ **Coût total (réel)** de cette écriture est inexacte également pour le même motif.  

> [!NOTE]  
>  Si vous effectuez un lettrage fixe pour une sortie de stock d’un article qui utilise le mode évaluation stock Moyen, la sortie de stock ne reçoit pas le coût moyen pour l’article comme d’habitude mais reçoit le coût de l’entrée de stock que vous avez spécifiée. Cette sortie de stock ne fait alors plus partie du calcul du coût moyen.  

### <a name="example--fixed-application-in-sales-return"></a>Exemple – lettrage fixe dans le retour vente
Les lettrages fixes sont également un excellent moyen de contrepasser un coût exactement, par exemple avec des retours vente.  

L’exemple suivant, qui indique la manière dont un lettrage fixe garantit la contrepassation du coût exact, est basé sur le scénario suivant :  

1.  L’utilisateur valide une facture achat.  
2.  L’utilisateur valide une facture vente.  
3.  L’utilisateur valide un avoir vente pour l’article retourné, qui s’applique à l’écriture ventes, pour inverser le coût correctement.  
4.  Des frais de transport liés à la commande achat validée précédemment, arrivent. L’utilisateur le valide comme frais article.  

Le tableau suivant montre le résultat des étapes 1 à 3 du scénario dans les écritures valeur de l’article.  

|Date comptabilisation|Type écriture comptable article|Quantité valorisée|Coût total (réel)|Écriture article à lettrer|N° écriture comptable article|N° écriture|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01/01/20|Achats|1|1000.00||1|1|  
|01/02/20|Vente|-1|1000.00||2|2|  
|01/03/20|Vente (avoir)|1|1000|2|3|3|  

Le tableau suivant montre l’écriture valeur résultant de l’étape 4 du scénario, validant les frais annexes.  

|Date comptabilisation|Type écriture comptable article|Quantité valorisée|Coût total (réel)|Écriture article à lettrer|N° écriture comptable article|N° écriture|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01/04/20|(Frais annexes)|1|100.00||1|4|  

Le tableau suivant montre l’effet de la contrepassation du coût exact des écritures valeur de l’article.  

|Date comptabilisation|Type écriture comptable article|Quantité valorisée|Coût total (réel)|Écriture article à lettrer|N° écriture comptable article|N° écriture|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01/01/20|Achats|1|1000.00||1|1|  
|01/02/20|Vente|-1|1100.00||2|2|  
|01/03/20|Vente (avoir)|1|1100.00|2|3|3|  
|01/04/20|(Frais annexes)|1|100.00||1|4|  

Lorsque vous exécutez le traitement par lots **Ajuster coûts - Écr. article**, le coût augmenté de l’écriture achat, dû aux frais annexes, est transmis à l’écriture vente écriture numéro 2. L’écriture vente transfère alors ce coût augmenté à l’écriture vente créditrice (numéro de séquence 3). Le résultat final est que le coût est correctement contrepassé.  

> [!NOTE]  
>  Si vous utilisez des retours ou des avoirs et que vous avez configuré le champ **Coût retour identique obligatoire** sur la page **Paramètres achats** ou **Paramètres ventes**, en fonction de votre situation, [!INCLUDE[prod_short](includes/prod_short.md)] renseigne automatiquement ces champs lorsque vous utilisez la fonction **Copier à partir du document**. Si vous utilisez la fonction **Affichage de lignes document validées à contrepasser**, les champs sont toujours renseignés automatiquement.  

> [!NOTE]  
>  Si vous validez une transaction avec un lettrage fixe et si l’écriture comptable article que vous lettrez doit être clôturée, ce qui signifie que la quantité restante est égale à zéro, l’ancien lettrage est automatiquement annulé et l’écriture comptable article est réappliquée à l’aide du lettrage fixe que vous avez spécifié.  

## <a name="transfer-application"></a>Application de transfert
Lorsqu’un article est transféré d’un magasin à un autre, dans le stock de la société, alors une application est créée entre les deux écritures de transfert. L’évaluation d’une écriture de transfert dépend du mode d’évaluation. Pour les articles utilisant le mode évaluation stock moyen, l’évaluation est créée à l’aide du coût moyen dans la période coût moyen où se trouve la date évaluation du transfert. Pour les articles utilisant d’autres modes évaluation stock, l’évaluation est effectuée en remontant jusqu’au coût de l’entrée de stock d’origine.  

### <a name="example--average-costing-method"></a>Exemple – mode évaluation stock moyen
L’exemple suivant, qui indique comment les écritures de transfert sont lettrées, est basé sur le scénario suivant pour un article utilisant le mode évaluation stock moyen et une période coût moyen Jour.  

1. L’utilisateur achète l’article à un montant de 10,00 LCY.  
2. L’utilisateur achète à nouveau l’article à un montant de 20,00 LCY.  
3. L’utilisateur transfère l’article du magasin EAST vers le magasin WEST.  

Le tableau suivant montre l’effet du transfert sur les écritures valeur de l’article.  

|Date comptabilisation|Type écriture comptable article|Code magasin|Quantité valorisée|Coût total (réel)|Numéro de la séquence|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01/01/20|Achats|EAST|1|10,00|1|  
|01/01/20|Achats|EAST|1|20,00|2|  
|01/02/20|Transfert|EAST|-1|15,00|3|  
|01/02/20|Transfert|WEST|1|15,00|4|  

### <a name="example--standard-costing-method"></a>Exemple – Mode d’évaluation du stock Standard
L’exemple suivant, qui indique comment les écritures de transfert sont lettrées, est basé sur le scénario suivant pour un article utilisant le mode évaluation stock Standard et une période coût moyen Jour.  

1. L’utilisateur achète l’article à un montant standard de 10,00 LCY.  
2. L’utilisateur transfère l’article à partir du magasin EAST vers le magasin WEST à un coût standard de 12,00 DS.  

Le tableau suivant montre l’effet du transfert sur les écritures valeur de l’article.  

|Date comptabilisation|Type écriture comptable article|Code magasin|Quantité valorisée|Coût total (réel)|Numéro de la séquence|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01/01/20|Achats|EAST|1|10,00|1|  
|01/02/20|Transfert|EAST|-1|10,00|2|  
|01/02/20|Transfert|WEST|1|10,00|3|  

Étant donné que la valeur de l’entrée de stock d’origine est de 10,00 DS, le transfert est évalué à ce coût, et non à 12,00 DS.  

## <a name="reapplication"></a>Relettrage
En raison du mode de calcul du coût unitaire d’un article, un lettrage article incorrect peut produire un coût moyen ou un coût unitaire erroné. Les scénarios suivants peuvent générer des lettrages article incorrects, qui nécessitent d’annuler des lettrages article et relettrer des écritures comptables article :  

* Vous avez oublié d’effectuer un lettrage fixe.  
* Vous avez effectué un lettrage incorrect.  
* Vous souhaitez annuler le lettrage créé automatiquement lors de la validation, en fonction du mode d’évaluation stock de l’article.  
* Vous devez retourner un article sur lequel une vente a déjà été appliquée manuellement, sans utiliser la fonction **Afficher des lignes document validées à contrepasser** et vous devez donc annuler l’application.  

[!INCLUDE[prod_short](includes/prod_short.md)] propose une fonction pour analyser et corriger des lettrages article. Cela s’effectue sur la page **Feuille lettrage**.  

## <a name="see-also"></a>Voir aussi
[Détails de conception : problème de lettrage article connu](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : modes évaluation stock](design-details-costing-methods.md)  
[Détails de conception : coût moyen](design-details-average-cost.md)   
[Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finances](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
