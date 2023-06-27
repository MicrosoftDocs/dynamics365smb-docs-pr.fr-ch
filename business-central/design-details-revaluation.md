---
title: "Détails de conception\_:\_réévaluation"
description: Vous pouvez réévaluer le stock en fonction de la base d’évaluation reflétant le plus précisément la valeur de stock.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-revaluation"></a>Détails de conception : réévaluation
Vous pouvez réévaluer le stock en fonction de la base d’évaluation reflétant le plus précisément la valeur de stock. Vous pouvez également antidater une réévaluation, afin que le coût des biens vendus (COGS) soit correctement mis à jour pour les articles qui ont déjà été vendus. Les articles utilisant le mode évaluation stock standard qui n’ont pas été entièrement facturés peuvent également être réévalués.  

Dans [!INCLUDE[prod_short](includes/prod_short.md)], la flexibilité suivante est prise en charge sur la réévaluation :  

-   La quantité réévaluable peut être calculée pour n’importe quelle date, également dans le passé.  
-   Pour les articles utilisant le mode évaluation stock standard, les écritures coût prévu sont incluses dans la réévaluation.  
-   Des sorties de stock affectées par la réévaluation sont détectées.  

## <a name="calculating-the-revaluable-quantity"></a>Calcul de la quantité réévaluable
 La quantité réévaluable est la quantité restante en stock qui est disponible pour la réévaluation à une date donnée. Elle est calculée comme somme totale des quantités des écritures comptables article entièrement facturées qui ont une date comptabilisation égale ou antérieure à la date comptabilisation de réévaluation.  

> [!NOTE]  
>  Les articles utilisant le mode évaluation stock standard sont traités de façon différente lors du calcul de la quantité réévaluable par article, magasin et variante. Les quantités et les valeurs des écritures comptables articles qui ne sont pas entièrement facturées sont incluses dans la quantité réévaluable.  

Une fois qu’une réévaluation a été validée, vous pouvez valider une entrée de stock ou une sortie de stock avec une date comptabilisation antérieure à la date comptabilisation de la réévaluation. Cependant, cette quantité n’est pas affectée par la réévaluation. Pour équilibrer le stock, seule la quantité initiale réévaluable est considérée.  

Étant donné que la réévaluation peut être effectuée à n’importe quelle date, vous devez avoir des conventions pour le moment où un article est considéré comme une partie du stock du point de vue bancaire. Par exemple, lorsque l’article est en stock et lorsque l’article est encours (WIP).  

### <a name="example"></a>Exemple :
L’exemple suivant montre à quel moment un article TEC se transforme pour devenir une partie du stock. L’exemple est basé sur la production d’une chaîne de 150 liens.  

![Stock et réévaluation TEC.](media/design_details_inventory_costing_10_revaluation_wip.png "Stock et réévaluation TEC")  

**1Q** : l’utilisateur valide les maillons achetés comme étant reçus. Le tableau suivant montre l’écriture comptable article résultante.  

|Date comptabilisation|Article ;|Type écriture|Quantité|Numéro de la séquence|  
|------------------|----------|----------------|--------------|---------------|  
|01/01/20|LIEN|Achats|150|1|  

> [!NOTE]  
>  À présent un article utilisant le mode évaluation stock standard est disponible pour la réévaluation.  

**1V** : l’utilisateur valide les maillons achetés comme étant facturés et les maillons intègrent le stock, d’un point de vue financier. Le tableau suivant montre les écritures valeur résultantes.  

|Date comptabilisation|Type écriture|Date évaluation|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15/01/20|Coût direct|01/01/20|150,00|1|1|  

 **2Q + 2V** : l’utilisateur valide les maillons achetés comme étant consommés pour la production de la chaîne en fer. Du point de vue financier, les liens deviennent une partie du stock encours.  Le tableau suivant montre l’écriture comptable article résultante.  

|Date comptabilisation|Article ;|Type écriture|Quantité|Numéro de la séquence|  
|------------------|----------|----------------|--------------|---------------|  
|01/02/20|LIEN|Consommation|-150|1|  

Le tableau suivant montre l’écriture valeur résultante.  

|Date comptabilisation|Type écriture|Date évaluation|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01/02/20|Coût direct|01/02/20|-150,00|2|2|  

La date d’évaluation est définie sur la date de la validation de la consommation (02-01-20), en sortie de stock classique.  

**3Q** : l’utilisateur valide la chaîne comme étant en production et finit l’ordre de fabrication. Le tableau suivant montre l’écriture comptable article résultante.  

|Date comptabilisation|Article ;|Type écriture|Quantité|N° écriture|  
|------------------|----------|----------------|--------------|---------------|  
|15/02/20|CHAÎNE|Production|1|3|  

**3V** : l’utilisateur exécute le traitement par lots **Ajuster coûts - Écr. article**, qui valide la chaîne comme étant facturée pour indiquer que toute la consommation de matériel a été entièrement facturée. Du point de vue financier, les liens ne font plus partie du stock encours lorsque la production est entièrement facturée et ajustée. Le tableau suivant montre les écritures valeur résultantes.  

|Date comptabilisation|Type écriture|Date évaluation|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15/01/20|Coût direct|01/01/20|150,00|2|2|  
|01/02/20|Coût direct|01/02/20|-150,00|2|2|  
|15/02/20|Coût direct|15/02/20|150,00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Coût prévu de la réévaluation
La quantité réévaluable est calculée comme la somme de la quantité des écritures comptables article entièrement facturées avec une date comptabilisation égale ou antérieure à la date de réévaluation. Cela signifie que lorsque certains articles sont reçus/livrés mais pas facturés, leur valeur de stock ne peut pas être calculée. Les articles utilisant le mode évaluation stock standard ne sont pas limités à cet égard.  

> [!NOTE]  
>  Le stock en-cours est un autre type de coût prévu qui peut être réévalué, dans le cadre de certaines règles. Pour plus d’informations, voir [Réévaluation du stock en-cours](design-details-revaluation.md#wip-inventory-revaluation).  

Lors du calcul de la quantité réévaluable pour les articles utilisant le mode d’évaluation Standard, les écritures comptables article n’ayant pas été complètement facturées sont incluses dans le calcul. Les écritures sont ensuite réévaluées lorsque vous validez la réévaluation. Lorsque vous facturez l’écriture réévaluée, les écritures valeur suivantes sont créées :  

-   L’écriture valeur facturée habituelle avec un type d’écriture **Coût direct**. Le coût total de cette écriture est le coût direct de la ligne origine.  
-   Une écriture valeur avec le type d’écriture **Écart**. Cette écriture enregistre la différence entre le coût facturé et le coût standard réévalué.  
-   Une écriture valeur avec le type d’écriture **Réévaluation**. Cette écriture enregistre l’inversion de la réévaluation du coût prévu.  

### <a name="example-1"></a>Exemple :
L’exemple suivant, basé sur la production de la chaîne dans l’exemple précédent, illustre la manière dont les trois types d’écritures sont créés. Il est basé sur le scénario suivant :  

1.  L’utilisateur valide les liens achetés comme reçus avec un coût unitaire de 2,00 LCY.  
2.  L’utilisateur valide ensuite une réévaluation des liens avec un nouveau coût unitaire de 3,00 LCY, mettant à jour le coût standard à 3,00 LCY.  
3.  L’utilisateur valide l’achat d’origine des liens comme facturés, ce qui crée ce qui suit :  

    1.  Une écriture valeur facturée avec le type d’écriture **Coût direct**.  
    2.  Une écriture valeur avec le type d’écriture **Réévaluation** pour enregistrer la contrepassation de la réévaluation du coût prévu.  
    3.  Une écriture valeur avec le type d’écriture Écart, qui enregistre la différence entre le coût facturé et le coût standard réévalué.  
Le tableau suivant montre les écritures valeur résultantes.  

|Étape|Date comptabilisation|Type écriture|Date évaluation|Coût total (prévu)|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|15/01/20|Coût direct|15/01/20|300,00|0.00|1|1|  
|2.|20/01/20|Réévaluation|20/01/20|150,00|0.00|1|2|  
|3.a.|15/01/20|Coût direct|15/01/20|-300,00|0.00|1|3|  
|3.b.|15/01/20|Réévaluation|20/01/20|-150,00|0.00|1|4|  
|3.c.|15/01/20|Ecart|15/01/20|0.00|450,00|1|5|  

## <a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation"></a>Déterminer si une sortie de stock est liée à la réévaluation
La date de la validation ou de la réévaluation est utilisée pour déterminer si une sortie de stock est affectée par une réévaluation.  

Le tableau suivant montre les critères utilisés pour un article qui n’utilise pas le mode évaluation stock moyen.  

|Scénario|Numéro de la séquence|Timing|Lié à la réévaluation|  
|--------------|---------------|------------|-----------------------------|  
|A|Antérieur au numéro d’écriture réévaluation.|Antérieur à la date de comptabilisation de réévaluation|Non|  
|B|Antérieur au n° d’écriture réévaluation.|Égal à la date comptabilisation de réévaluation|Non|  
|C|Antérieur au n° d’écriture réévaluation.|Ultérieur à la date comptabilisation de réévaluation|Oui|  
|J|Ultérieur au n° d’écriture réévaluation.|Antérieur à la date de comptabilisation de réévaluation|Oui|  
|E|Ultérieur au n° d’écriture réévaluation.|Égal à la date comptabilisation de réévaluation|Oui|  
|F|Ultérieur au n° d’écriture réévaluation.|Ultérieur à la date comptabilisation de réévaluation|Oui|  

### <a name="example-2"></a>Exemple :
L’exemple suivant, qui illustre la réévaluation d’un article qui utilise le mode d’évaluation du stock FIFO, est basé sur le scénario suivant :  

1.  Le 01/01/20, l’utilisateur valide un achat de 6 unités.  
2.  Le 01/02/20, l’utilisateur valide une vente de 1 unité.  
3.  Le 01-03-20, l’utilisateur valide une vente de 1 unité.  
4.  Le 01-04-20, l’utilisateur valide une vente de 1 unité.  
5.  Le 01/03/20, l’utilisateur calcule la valeur de stock pour l’article, et valide une réévaluation du coût unitaire de l’article en devise société de 10,00 à 8,00 DS.  
6.  Le 01/02/20, l’utilisateur valide une vente de 1 unité.  
7.  Le 01-03-20, l’utilisateur valide une vente de 1 unité.  
8.  Le 01-04-20, l’utilisateur valide une vente de 1 unité.  
9. L’utilisateur exécute le traitement par lots **Ajuster coûts - Écr. article**.  

Le tableau suivant montre les écritures valeur résultantes.  

|Scénario|Date comptabilisation|Type écriture|Date évaluation|Quantité valorisée|Coût total (réel)|N° écriture comptable article|Numéro de la séquence|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01/01/20|Achats|01/01/20|6|60,00|1|1|  
||01/03/20|Réévaluation|01/03/20|4|-8,00|1|5|  
|A|01/02/20|Vente|01/02/20|-1|-10,00|2|2|  
|B|01/03/20|Vente|01/03/20|-1|-10,00|3|3|  
|C|01/04/20|Vente|01/04/20|-1|-10,00|4|4|  
||01/04/20|Vente|01/04/20|-1|2,00|4|9|  
|J|01/02/20|Vente|01/03/20|-1|-10,00|5|6|  
||01/02/20|Vente|01/03/20|-1|2,00|5|10|  
|E|01/03/20|Vente|01/03/20|-1|-10,00|6|7|  
||01/03/20|Vente|01/03/20|-1|2,00|6|11|  
|F|01/04/20|Vente|01/04/20|-1|-10,00|7|8|  
||01/04/20|Vente|01/04/20|-1|2,00|7|12|  

## <a name="wip-inventory-revaluation"></a>Réévaluation du stock en-cours
La réévaluation du stock en-cours implique de réévaluer les composants qui sont enregistrés en tant que membres du stock en-cours au moment de la réévaluation.  

Pour cela, il est important d’établir des conventions sur le moment où un article est considéré comme une partie du stock TEC d’un point de vue financier. Dans [!INCLUDE[prod_short](includes/prod_short.md)], les conventions disponibles sont les suivantes :  

-   Un composant acheté fait partie du stock de matières premières dès la validation d’un achat comme étant facturé.  
-   Un composant acheté/semi-fini fait partie du stock en-cours dès la validation de sa consommation par rapport à un ordre de fabrication.  
-   Un composant acheté/semi-fini reste dans le stock en-cours jusqu’au moment où un ordre de fabrication (article fabriqué) est facturé.  

La manière dont la date d’évaluation de l’écriture valeur de la consommation est définie suit les mêmes règles que pour le stock hors TEC. Pour plus d’informations, reportez-vous à la section [Déterminer si une sortie de stock est liée à la réévaluation](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).  

Stock TEC peut être réévalué tant que la date de réévaluation n’est pas ultérieure à la date comptabilisation des écritures comptables article correspondantes de type Consommations et tant que l’ordre de fabrication correspondant n’a pas encore été facturé.  

> [!CAUTION]  
>  L’état **Évaluation du stock - TEC** affiche la valeur des écritures d’ordre de fabrication validées et peut donc créer un peu de confusion pour les articles TEC qui ont été réévalués.  

## <a name="see-also"></a>Voir aussi
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md)   
 [Détails de conception : Évaluation du stock](design-details-inventory-valuation.md) [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
