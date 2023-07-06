---
title: Modifier le montant annuel du contrat service ou du devis contrat
description: Vous pouvez modifier le montant facturé annuellement sur des contrats de service ou des devis contrat de service.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a><a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a><a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a>Modifier le montant annuel du contrat service ou du devis contrat
Vous pouvez modifier le montant annuel du contrat service ou du devis contrat afin de rectifier le montant qui sera facturé annuellement.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a><a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a><a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a>Pour modifier le montant annuel du contrat service ou du devis contrat

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service** ou **Devis contrat de service**, puis sélectionnez le lien associé.  
2. Choisissez le contrat ou le devis contrat.  
3. Choisissez l’action **Ouvrir contrat** pour ouvrir le contrat ou le devis contrat et le modifier.  
4. Choisissez la case à cocher **Autoriser montants non soldés** si vous souhaitez modifier le montant annuel et répartir la différence du montant annuel manuellement dans les lignes de contrat. Autrement, décochez la case pour répartir automatiquement la différence du montant annuel dans les lignes contrat après avoir modifié le montant annuel.  
5. Modifiez la valeur du champ **Montant annuel**. Vous ne pouvez pas signer, c’est-à-dire convertir en un contrat service si vous travaillez sur un devis contrat de service, ni verrouiller un contrat service dont le montant annuel est négatif. Si vous paramétrez le montant annuel sur zéro, la valeur du champ **Période de facturation** doit être **Aucune** lors de la signature ou du verrouillage du contrat service.  
6. Selon que la case à cocher du champ **Autoriser montants non soldés** est sélectionnée ou non, exécutez la répartition manuelle ou automatique de la différence du montant annuel. Les lignes contrat sont mises à jour de telle sorte que la valeur du champ **Montant annuel calculé** soit égale au nouveau montant annuel.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts"></a><a name="distributing-differences-between-new-and-calculated-annual-amounts"></a><a name="distributing-differences-between-new-and-calculated-annual-amounts"></a>Distribuer les différences entre les nouveaux montants annuels et les montants annuels calculés
Si vous modifiez le montant annuel d’un contrat de service ou d’un devis contrat de service, vous devrez peut-être répartir la différence entre ses nouveaux montants annuels et ses montants annuels calculés dans les lignes contrat. Il existe trois méthodes de répartition des montants :

* Répartition égale  
* Répartition selon montants ligne  
* Répartition selon marge

### <a name="even-distribution"></a><a name="even-distribution"></a><a name="even-distribution"></a>Répartition égale
Si vous modifiez le montant annuel du contrat service ou du devis contrat, vous voudrez peut-être répartir la différence entre ses nouveaux montants annuels et ses montants annuels calculés dans les lignes contrat. La répartition égale est l’une des méthodes de répartition automatique qui peut vous aider à répartir équitablement la différence nouveaux montants annuels et montants annuels calculés entre les montants ligne des lignes contrat. La liste suivante, qui répertorie les étapes de la procédure de répartition, décrit les grands principes de cette méthode :  

1. La différence entre les nouvelles valeurs des champs **Montant annuel** et **Montant annuel calculé** est divisée par le nombre de lignes contrat dans le contrat service ou le devis contrat.  
2. La valeur du champ **Montant ligne** est mise à jour en ajoutant le résultat de l’opération précédente.  
3. La valeur des champs **Montant remise ligne**, **remise ligne** et **Marge** est mise à jour par rapport à la nouvelle valeur du champ **Montant ligne** de la manière suivante :   
    * Montant remise ligne = Valeur ligne - Montant ligne.  
    * % remise ligne = Montant remise ligne / Valeur ligne * 100.  
    * Marge = Montant ligne - Coût ligne.  

 Les étapes sont répétées pour chaque ligne contrat.  

#### <a name="example"></a><a name="example"></a><a name="example"></a>Exemple :
La case à cocher **Autoriser montants non soldés** n’est pas activé dans le contrat service qui contient trois lignes de contrat avec les informations suivantes.  

|Article ;|Coût ligne|Valeur ligne|% remise ligne|Montant remise ligne|Montant ligne|Marge|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Article 1|30,00|40,00|0.00|0.00|40,00|10,00|  
|Article 2|40,00|50,00|10,00|5,00|45,00|5,00|  
|Article 3|50,00|70,00|10,00|7,00|63,00|13,00|  

La valeur du champ **Montant annuel** est égale à celle du champ **Montant annuel calculé**, qui est toujours égale à la somme des montants ligne. Dans ce cas, il est égal à ce qui suit : 40 + 45 + 63 = 148.  

Si vous remplacez le **Montant annuel** par 139, le montant est calculé et doit être ajouté à chaque valeur du champ **Montant ligne**. Ce montant est calculé en retranchant le **Montant annuel calculé** de la nouvelle valeur du champ **Montant annuel** et en divisant le résultat par le nombre de lignes de contrat du contrat de service. Dans ce cas, il sera égal à ce qui suit : (139 - 148) / 3 = 3. Ensuite, le dernier chiffre calculé est ajouter à chaque valeur du champ **Montant ligne** et les valeurs des champs **% remise ligne**, **Montant remise ligne** et **Marge** sont mises à jour à l’aide des formules de la procédure décrite précédemment.  

A la fin, les lignes contrat contiennent les données suivantes.  

|Article ;|Coût ligne|Valeur ligne|% remise ligne|Montant remise ligne|Montant ligne|Marge|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Article 1|30,00|40,00|7,50|3,00|37,00|7,00|  
|Article 2|40,00|50,00|16.00|8.00|42.00|2.00|  
|Article 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount"></a><a name="distribution-based-on-line-amount"></a><a name="distribution-based-on-line-amount"></a>Répartition selon montant ligne
Si vous modifiez le montant annuel du contrat service ou du devis contrat, vous voudrez peut-être répartir la différence entre ses nouveaux montants annuels et ses montants annuels calculés dans les lignes contrat. La répartition basée sur le montant ligne est l’une des méthodes automatiques qui peut vous aider à répartir la différence nouveaux montants annuels et montants annuels calculés entre les montants ligne des lignes contrat. La répartition se fera proportionnellement à leur part montant ligne dans le montant annuel calculé. La liste suivante, qui répertorie les étapes de la procédure de répartition pour chaque ligne contrat, décrit les grands principes de cette méthode :  

1. La marge sur coût variable en pourcentage est calculée comme suit : la valeur du champ **Montant ligne** est divisée par les valeurs du champ **Montant annuel calculé** de toutes les lignes contrat.  
2. La valeur du champ **Montant ligne** est mise à jour en lui ajoutant la différence entre les nouveaux montants annuels et les montants calculés, qui est multipliée par la marge sur coût variable en pourcentage.  
3. La valeur des champs **Montant remise ligne**, **remise ligne** et **Marge** est mise à jour par rapport à la nouvelle valeur du champ **Montant remise ligne** de la manière suivante :  

    * Montant remise ligne = Valeur ligne- Montant ligne.  
    * % remise ligne = Montant remise ligne / Valeur ligne * 100.  
    * Marge = M ontant ligne - Coût ligne.  

Les étapes sont répétées pour chaque ligne contrat.  

#### <a name="example-1"></a><a name="example-1"></a><a name="example-1"></a>Exemple :
La case à cocher **Autoriser montants non soldés** n’est pas activé dans le contrat service qui contient trois lignes de contrat avec les informations suivantes.  

|Article ;|Coût ligne|Valeur ligne|% remise ligne|Montant remise ligne|Montant ligne|Marge|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Article 1|15,00|17,00|3,00|0,51|25,00|1,49|  
|Article 2|20,00|23,00|Aucune|0.00|55,10|3,00|  
|Article 3|24,00|27,00|3,00|0,81|112,70|2,19|  

La valeur du champ **Montant annuel** est égale à celle du champ **Montant annuel calculé** qui est toujours égale à la somme des montants ligne. Dans ce cas, il est égal à ce qui suit : 16,49 + 23,00 + 26,19 = 65,68.  

Si vous remplacez le **Montant annuel** par 60, la marge sur coût variable en pourcentage est calculée pour chaque ligne contrat :  

* Article 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Article 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Article 3 – 12,7 / (5 + 5,1 +12,7) = 0,557  

La valeur du champ **Montant ligne** est ensuite mise à jour dans chaque ligne contrat à l’aide de la formule suivante : Montant ligne = Montant ligne + différence entre les nouveaux montants annuels et les montants annuels calculés * Contribution en pourcentage. Après quoi, les valeurs des champs **Montant remise ligne**, **% remise ligne** et **Marge** sont mises à jour à l’aide des formules décrites dans la procédure précédente.  

A la fin, les lignes contrat contiennent les données suivantes.  

|Article ;|Coût ligne|Valeur ligne|% remise ligne|Montant remise ligne|Montant ligne|Marge|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Article 1|15,00|17,00|11,41|1,94|15,06|0,06|  
|Article 2|20,00|23,00|8.65|1.99|21.01|1.01|  
|Article 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit"></a><a name="distribution-based-on-profit"></a><a name="distribution-based-on-profit"></a>Répartition selon marge
Si vous modifiez le montant annuel du contrat service ou du devis contrat, vous voudrez peut-être répartir la différence entre ses nouveaux montants annuels et ses montants annuels calculés dans les lignes contrat. La répartition basée sur la marge est l’une des méthodes automatiques qui peut vous aider à répartir la différence nouveaux montants annuels et montants calculés entre les montants ligne des lignes contrat. Cette répartition se fera proportionnellement à leurs parts de marge dans le contrat total ou à la marge du devis contrat. La liste suivante, qui répertorie les étapes de la procédure de répartition pour chaque ligne contrat, décrit les grands principes de cette méthode :  

1. La marge sur coût variable en pourcentage est calculée comme suit : La valeur du champ **Marge** est divisé par la somme des valeurs du champ **Marge** dans toutes les lignes contrat.  
2. La valeur du champ **Montant ligne** est mise à jour en lui ajoutant la différence nouveaux montants annuels et montants annuels calculés, qui est multipliée par la marge sur coût variable.  
3. La valeur des champs Montant remise ligne, % remise ligne et Marge est mise à jour par rapport à la nouvelle valeur du champ **Montant ligne** de la manière suivante :  

    * Montant remise ligne = Valeur ligne- Montant ligne.  
    * % remise ligne = Montant remise ligne / Valeur ligne * 100.  
    * Marge = Montant ligne - Coût ligne.  

#### <a name="example-2"></a><a name="example-2"></a><a name="example-2"></a>Exemple :
La case à cocher **Autoriser montants non soldés** n’est pas activé dans le contrat service qui contient trois lignes de contrat avec les informations suivantes.  

|Article ;|Coût ligne|Valeur ligne|% remise ligne|Montant remise ligne|Montant ligne|Marge|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Article 1|20,00|25,00|0.00|0.00|25,00|5,00|  
|Article 2|50,00|58,00|5,00|2,90|55,10|5,10|  
|Article 3|100,00|115,00|2,00|2,30|112,70|12,70|  

La valeur du champ **Montant annuel** est égale à celle du champ **Montant annuel calculé**, qui est toujours égale à la somme des montants ligne. Dans ce cas, elle est égale à ce qui suit : 25,00 + 55,10 + 112,70 = 192,80.  

 Si vous remplacez le **Montant annuel** par 180, la marge sur coût variable en pourcentage est calculée pour chaque ligne contrat :  

* Article 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Article 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Article 3 – 12,7 / (5 + 5,1 +12,7) = 0,557  

La valeur du champ **Montant ligne** est ensuite mise à jour dans chaque ligne contrat à l’aide de la formule suivante : Montant ligne = Montant ligne + différence entre les nouveaux montants annuels et les montants annuels calculés * Contribution en pourcentage. Après quoi, les valeurs des champs **Montant remise ligne**, **% remise ligne** et **Marge** sont mises à jour à l’aide des formules de l’étape 3 de la procédure décrite précédemment.  

A la fin, les lignes contrat contiennent les données suivantes.  

|Article ;|Coût ligne|Valeur ligne|% remise ligne|Montant remise ligne|Montant ligne|Marge|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Article 1|20,00|25,00|11,24|2,81|22,19|2,19|  
|Article 2|50,00|58,00|9.93|5.76|52.24|2.24|  
|Article 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
[Créer des devis et contrats de service](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Paramétrage de la gestion des services](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
