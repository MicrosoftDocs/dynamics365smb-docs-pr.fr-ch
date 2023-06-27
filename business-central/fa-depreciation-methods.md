---
title: Méthodes amortissement pour les immobilisations
description: "Découvrez les différentes méthodes intégrées pour amortir ou déprécier les immobilisations dans la version par défaut de Business\_Central qui comprend huit\_méthodes."
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5629, 5633'
ms.date: 07/05/2021
ms.author: edupont
---
# <a name="depreciation-methods-for-fixed-assets" />Méthodes amortissement pour les immobilisations

Il existe huit méthodes d’amortissement disponibles dans la version par défaut de [!INCLUDE [prod_short](includes/prod_short.md)] :  

* Linéaire  
* Dégressif1  
* Dégressif2  
* Dégr1/Lin  
* Dégr2/Lin  
* Paramétrable  

  > [!NOTE]  
  > Spécifiez votre propre méthode d’amortissement en définissant des tables d’amortissement. Pour plus d’informations sur l’application d’une méthode d’amortissement définie par l’utilisateur, voir [Configurer la méthode d’amortissement définie par l’utilisateur](fa-how-setup-user-defined-depreciation-method.md).
* Manuel  

  > [!NOTE]  
  > Utilisez cette méthode pour les immobilisations qui ne font pas l’objet d’un amortissement, par exemple les terrains. Vous devez saisir l’amortissement dans la feuille validation immobilisation. Le traitement par lots **Calculer amortissement** ignore les immobilisations qui utilisent cette méthode d’amortissement.  
* Règle de la demi-année  

  > [!NOTE]  
  > Lorsque vous utilisez cette méthode, le montant de l’amortissement d’une immobilisation ne varie pas d’une année à l’autre.  

## <a name="straight-line-depreciation" />Amortissement linéaire

Lorsque vous utilisez la méthode linéaire, vous devez indiquer l’une des options suivantes dans la loi d’amortissement immobilisation :  

* Période de l’amortissement (en années ou en mois) ou date fin de l’amortissement  
* Pourcentage annuel fixe  
* Montant annuel fixe  
* Période d’amortissement  

### <a name="depreciation-period" />Période d’amortissement

Si vous saisissez la période d’amortissement (nombre d’années ou de mois d’amortissement, ou date fin d’amortissement), la formule suivante calcule le montant de l’amortissement :  

*Montant de l’amortissement = ((valeur comptable - valeur résiduelle) x nombre de jours d’amortissement)/jours d’amortissement restants*  

Le nombre de jours d’amortissement restants correspond au nombre de jours d’amortissement moins le nombre de jours compris entre la date début de l’amortissement et la date de la dernière écriture immobilisation.  

La valeur comptable peut être diminuée d’un montant de réévaluation, de dépréciation, ou paramétrable 1 ou 2 validé, selon l’état (activé/désactivé) des champs **Inclure dans calcul amort.** et **Élément valeur comptable** sur la page **Type paramètre compta. immo**. Ce calcul garantit l’amortissement complet de l’immobilisation à la date fin de l’amortissement.  

### <a name="fixed-yearly-percentage" />Pourcentage annuel fixe

Si vous saisissez un pourcentage annuel fixe, l’application utilise la formule suivante pour calculer le montant de l’amortissement :  

*Montant de l’amortissement = (% linéaire x base amortissement x nombre de jours d’amortissement)/(100 x 360)*  

### <a name="fixed-yearly-amount" />Montant annuel fixe

Si vous saisissez un montant annuel fixe, l’application utilise la formule suivante pour calculer le montant de l’amortissement :  

*Montant de l’amortissement = (montant d’amortissement fixe x nombre de jours d’amortissement)/360*  

### <a name="example---straight-line-depreciation" />Exemple - Amortissement linéaire

Une immobilisation a un coût d’acquisition de 100 000 DS. Sa durée de vie est estimée à huit ans. Le traitement par lots **Calculer amortissement** est exécuté tous les semestres.  

Pour cet exemple, l’écriture comptable immobilisation se présente comme suit :  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coût acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 30/06/20 |Amortissements |180 |-6 250,00 |93,750.00 |
| 31/12/20 |Amortissements |180 |-6 250,00 |87,500.00 |
| 30/06/21 |Amortissements |180 |-6 250,00 |81,250.00 |
| 31/12/21 |Amortissements |180 |-6 250,00 |75,000.00 |
| 30/06/27 |Amortissements |180 |-6 250,00 |6,250.00 |
| 31/12/27 |Amortissements |180 |-6 250,00 |0 |

## <a name="declining-balance-1-depreciation" />Amortissement dégressif 1

Il s’agit d’une méthode d’amortissement accélérée qui ventile la plus grande portion du coût d’une immobilisation sur les premières années de sa durée de vie. Si vous utilisez cette méthode, vous devez saisir un pourcentage annuel fixe.  

La formule suivante calcule les montants d’amortissement :  

*Montant de l’amortissement = (% dégressif x nombre de jours d’amortissement x base amortissement)/(100 x 360)*  

La base d’amortissement correspond à la valeur comptable moins l’amortissement validé depuis la date début de l’exercice comptable en cours.  

Le montant de l’amortissement validé peut contenir des écritures avec divers types de validation (dépréciation, paramétrable 1 et paramétrable 2) validés depuis la date de début de l’exercice comptable en cours. Ces types de validation sont inclus dans le montant d’amortissement validé si vous avez coché les champs **Type amortissement** et **Élément valeur comptable** sur la page **Type paramètre compta. immo.**.  

### <a name="example---declining-balance-1-depreciation" />Exemple - Amortissement dégressif 1

Une immobilisation a un coût d’acquisition de 100 000 DS. Le champ **% dégressif** indique la valeur 25. Le traitement par lots **Calculer amortissement** est exécuté tous les semestres.  

Le tableau suivant montre à quoi ressemblent les écritures comptables immobilisation.  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coûts d’acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 30/06/20 |Amortissements |180 |-12 500,00 |87,500.00 |
| 31/12/20 |Amortissements |180 |-12 500,00 |75,000.00 |
| 30/06/21 |Amortissements |180 |-9 375,00 |65,625.00 |
| 31/12/21 |Amortissements |180 |-9 375,00 |56,250.00 |
| 30/06/22 |Amortissements |180 |-7 031,25 |49,218.75 |
| 31/12/22 |Amortissements |180 |-7 031,25 |42,187.50 |
| 30/06/23 |Amortissements |180 |-5 273,44 |36,914.06 |
| 31/12/23 |Amortissements |180 |-5 273,44 |31,640.62 |
| 30/06/24 |Amortissements |180 |-3 955,08 |27,685.54 |
| 31/12/24 |Amortissements |180 |-3 955,08 |23,730.46 |

Méthode de calcul :  

* Année 1 : *25 % de 100 000 = 25 000 = 12 500 + 12 500*

* Année 2 : *25 % de 75 000 = 18 750 = 9 375 + 9 375*

* Année 3 : *25 % de 56 250 = 14 062,50 = 7 031,25 + 7 031,25*

Le calcul continue jusqu’à ce que la valeur comptable soit égale à la valeur résiduelle ou au montant final arrondi que vous avez saisi.  

## <a name="declining-balance-2-depreciation" />Amortissement dégressif 2

Les méthodes Dégressif 1 et Dégressif 2 calculent le même montant d’amortissement total chaque année. Toutefois, si vous lancez le traitement par lots **Calculer amortissement** plusieurs fois par an, la méthode Dégressif 1 permet d’obtenir des montants d’amortissement équitables pour chaque période d’amortissement. En revanche, la méthode Dégressif 2 permet d’obtenir des montants d’amortissement qui sont dégressifs pour chaque période.  

### <a name="example---declining-balance-2-depreciation" />Exemple - Amortissement dégressif 2

Une immobilisation a un coût d’acquisition de 100 000 DS. Le champ **% dégressif** indique la valeur 25. Le traitement par lots **Calculer amortissement** est exécuté tous les semestres. Les écritures comptables immobilisation se présentent comme suit :  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coûts d’acquisition |(Date début amortissement)|100 000,00 |100 000,00 |
| 30/06/20 |Amortissements |180 |-13 397,46 |86,602.54 |
| 31/12/20 |Amortissements |180 |-11 602,54 |75,000.00 |
| 30/06/21 |Amortissements |180 |-10 048,09 |64,951.91 |
| 31/12/21 |Amortissements |180 |-8 701,91 |56,250.00 |

Méthode de calcul :  

* *VC* = Valeur comptable  
* *NJ* = Nombre de jours d’amortissement  
* *PD* = Pourcentage dégressif  
* *P* = *PD*/100  
* *J* = *NJ*/360  

La formule de calcul des montants d’amortissement est la suivante :  

*MA* = *VC* x (1 - (1 - P)<sup>J</sup>)

Les valeurs d’amortissement sont les suivantes :  

| Date | Calcul |
| --- | --- |
| 30/06/20 |MA = 100 000,00 (1 - (1 - 0,25)<sup>0,5</sup>) = 13 397,46 |
| 31/12/20 |MA = 86 602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11 602,54 |
| 30/06/21 |MA = 75 000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10 048,09 |
| 31/12/21 |MA = 64 951.91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8 701,91 |

## <a name="db1sl-depreciation" />Amortissement Dégr1/Lin

Dégr1/Lin est l’abréviation combinée de Dégressif 1 et de Linéaire. Le calcul continue jusqu’à ce que la valeur comptable soit égale à la valeur résiduelle ou au montant final arrondi que vous avez saisi.  

Le traitement par lots **Calculer amortissement** calcule un montant linéaire et un montant dégressif, mais seul le montant le plus élevé des deux est transmis à la feuille.  

Vous pouvez utiliser divers pourcentages pour calculer le montant dégressif.  

Si vous utilisez cette méthode, saisissez la durée de vie estimée et un pourcentage dégressif sur la page **Loi d’amortissement**.  

### <a name="example---db1-sl-depreciation" />Exemple - Amortissement Dégr1/Lin

Une immobilisation a un coût d’acquisition de 100 000 DS. Sur la page **Loi d’amortissement**, le champ **% dégressif** indique la valeur 25 et le champ **Nombre années amortissement** indique la valeur 8. Le traitement par lots **Calculer amortissement** est exécuté tous les semestres.  

Les écritures comptables immobilisation se présentent comme suit :  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/01/20 |Coûts d’acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 30/06/20 |Amortissements |180 |-12 500,00 |87,500.00 |
| 31/12/20 |Amortissements |180 |-12 500,00 |75,000.00 |
| 30/06/21 |Amortissements |180 |-9 375,00 |65,625.00 |
| 31/12/21 |Amortissements |180 |-9 375,00 |56,250.00 |
| 30/06/22 |Amortissements |180 |-7 031,25 |49,218.75 |
| 31/12/22 |Amortissements |180 |-7 031,25 |42,187.50 |
| 30/06/23 |Amortissements |180 |-5 273,44 |36,914.06 |
| 31/12/23 |Amortissements |180 |-5 273,44 |31,640.62 |
| 30/06/24 |Amortissements |180 |-3 955,08 |27,685.54 |
| 31/12/24 |Amortissements |180 |-3 955,08 |23,730.46 |
| 30/06/25 |Amortissements |180 |-3 955,08 |19.775,38 Lin. |
| 31/12/25 |Amortissements |180 |-3 955,08 |15.820,30 Lin. |
| 30/06/26 |Amortissements |180 |-3 955,08 |11.865,22 Lin. |
| 31/12/26 |Amortissements |180 |-3 955,07 |7.910,15 Lin. |
| 30/06/27 |Amortissements |180 |-3 955,08 |3.955,07 Lin. |
| 31/12/27 |Amortissements |180 |-3 955,07 |0,00 Lin. |

La mention `SL` qui suit la valeur comptable indique que la méthode linéaire a été utilisée.  

Méthode de calcul :  

* Année 1 (2020) :  

    *Montant dégressif : 25 % de 100 000 = 25 000 = 12 500 + 12 500*  

    *Montant linéaire = 100 000/8 = 12 500 = 6 250 + 6 250*  

    Le montant dégressif est utilisé car il s’agit de la valeur la plus élevée.  

* Année 5 (2025) :  

    *Montant dégressif : 25 % de 23 730,46 = 4 943,85 = 2 471,92 + 2 471,92*  

    *Montant linéaire = 23 730,46/3 = 7 910,15 = 3 995,07 + 3 995,08*  

    Le montant linéaire est utilisé car il s’agit de la valeur la plus élevée.  

## <a name="half-year-convention-depreciation" />Amortissement selon la règle de la demi-année

La règle de la demi-année n’est appliquée que si vous avez coché le champ **Utiliser règle demi-année** sur la page **Plan amortissement**.  

Cette méthode d’amortissement peut être utilisée en combinaison avec les méthodes d’amortissement suivantes dans l’application :  

* Linéaire  
* Dégressif1  
* Dégr1/Lin  

Lorsque vous appliquez la règle de la demi-année, une immobilisation a un amortissement de six mois lors du premier exercice comptable, quelle que soit la valeur du champ **Date début amortissement**.  

> [!NOTE]  
> Avec la règle de la demi-année, la durée de vie restante estimée pour l’immobilisation à la fin de l’exercice comptable indique toujours une demi-année. Par conséquent, pour que la méthode Utiliser règle de la demi-année soit appliquée correctement, le champ **Date fin amortissement** de la **loi d’amortissement de l’immobilisation** doit toujours contenir une date antérieure de six mois à la date fin de l’exercice comptable au cours duquel l’immobilisation sera complètement amortie.  

### <a name="example---half-year-convention-depreciation" />Exemple - Amortissement selon la règle de la demi-année

Une immobilisation a un coût d’acquisition de 100 000 DS. Le champ **Date début amortissement** indique la valeur 01/03/20. La durée de vie est estimée à cinq ans, ce qui implique que le champ **Date fin amortissement** doit impérativement être paramétré sur la valeur 30/06/25. Le traitement par lots **Calculer amortissement** est exécuté tous les ans. Cet exemple est basé sur un exercice comptable.  

Les écritures comptables immobilisation se présentent comme suit :  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/03/20 |Coût acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 31/12/20 |Amortissements |270 |-10 000,00 |90,000.00 |
| 31/12/21 |Amortissements |360 |-20 000,00 |70,000.00 |
| 31/12/22 |Amortissements |360 |-20 000,00 |50,000.00 |
| 31/12/23 |Amortissements |360 |-20 000,00 |30,000.00 |
| 31/12/24 |Amortissements |360 |-20 000,00 |10,000.00 |
| 31/12/25 |Amortissements |180 |-10 000,00 |0.00 |

## <a name="example---db1sl-depreciation-using-half-year-convention" />Exemple - Amortissement dégressif 1/linéaire selon la règle de la demi-année

Une immobilisation a un coût d’acquisition de 100 000 DS. Le champ **Date début amortissement** indique la valeur 01/11/20. La durée de vie est estimée à cinq ans, ce qui implique que le champ **Date fin amortissement** doit impérativement être paramétré sur la valeur 30/06/25. Sur la page **Loi d’amortissement**, le champ **% dégressif** indique la valeur 40. Le traitement par lots **Calculer amortissement** est exécuté tous les ans. Cet exemple est basé sur un exercice comptable.  

Les écritures comptables immobilisation se présentent comme suit :  

| Date | Type compta. immo. | Jours | Montant | Valeur comptable |
| --- | --- | --- | --- | --- |
| 01/11/20 |Coût acquisition |(Date début amortissement) |100 000,00 |100 000,00 |
| 31/12/20 |Amortissements |60 |-20 000,00 |80,000.00 |
| 31/12/21 |Amortissements |360 |-32 000,00 |48,000.00 |
| 31/12/22 |Amortissements |360 |-19 200,00 |28,800.00 |
| 31/12/23 |Amortissements |360 |-11 520,00 |17,280.00 |
| 31/12/24 |Amortissements |360 |-11 520,00 |5.760,00 Lin. |
| 31/12/25 |Amortissements |180 |-5 760,00 |0,00 Lin. |

La mention `SL` qui suit la valeur comptable indique que la méthode linéaire a été utilisée.  

Méthode de calcul :  

* Année 1 :  

    *Montant dégressif = Montant total année = 40 % de 100 000 = 40 000.* Soit pour une demi-année 40 000 / 2 = 20 000  

    *Montant linéaire = Montant total année = 100 000/5 = 20 000.* Soit pour une demi-année = 20 000 / 2 =10 000  

    Le montant dégressif est utilisé car il s’agit de la valeur la plus élevée.  

* Année 5 (2024) :  

    *Montant dégressif = 40 % de 17 280,00 = 6 912,00*  

    *Montant linéaire = 28 800 / 1,5 = 11 520,00*  

    Le montant linéaire est utilisé car il s’agit de la valeur la plus élevée.  

## <a name="duplicating-entries-to-more-depreciation-books" />Duplication des écritures dans davantage de lois d’amortissement

Si vous disposez de trois lois d’amortissement, B1, B2 et B3, et que vous souhaitiez dupliquer des écritures de B1 vers B2 et B3, vous pouvez activer le champ **Inclure dans liste duplication** sur les fiches loi d’amortissement de B2 et de B3. Cela peut être utile si la loi d’amortissement B1 est intégrée en comptabilité et utilise la feuille validation immobilisation, et si les lois d’amortissement B2 et B3 ne sont pas intégrées en comptabilité et utilisent la feuille immobilisation.  

Lorsque vous saisissez une écriture pour B1 dans la feuille validation immobilisation et sélectionnez le champ **Utiliser liste duplication**, l’application duplique l’écriture pour les lois B2 et B3 dans la feuille immobilisation lors de la validation de l’écriture.  

> [!NOTE]  
> Vous ne pouvez pas utiliser la feuille d’origine comme destination de la duplication. Si vous validez des écritures dans la feuille validation immobilisation, vous pouvez les dupliquer dans la feuille immobilisation ou dans la feuille validation immobilisation en utilisant une autre feuille.  

> [!NOTE]  
> Vous ne pouvez pas utiliser la même souche de numéros dans la feuille validation immobilisation et la feuille immobilisation. Lorsque vous validez des écritures dans la feuille validation immobilisation, vous devez laisser le champ **N° document** vide. Si vous saisissez un numéro dans le champ, il est copié dans la feuille immobilisation. Vous devez modifier manuellement le numéro de document avant de pouvoir valider la feuille.  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/configure-depreciation-books/) associée

## <a name="see-also" />Voir aussi

[COMPTES D’IMMOBILISATIONS](fa-manage.md)  
[Paramétrage d’immobilisations](fa-setup.md)  
[Finances](finance.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
