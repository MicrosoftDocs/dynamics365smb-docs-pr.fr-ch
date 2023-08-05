---
title: Écritures comptables ouvertes d’articles non disponibles en stock
description: Cet article traite du problème de niveau de stock nul alors qu’il existe des écritures comptables article ouvertes.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Détails de conception : problème de lettrage article connu
Cet article traite du problème de niveau de stock nul alors qu’il existe des écritures comptables article ouvertes dans [!INCLUDE[prod_short](includes/prod_short.md)].  

L’article commence par répertorier les symptômes courants du problème, puis décrit les notions de base du lettrage article pour prendre en charge les raisons décrites pour ce problème. À la fin de l’article, une solution de contournement est proposée pour résoudre ce problème.  

## Symptômes du problème  
 Voici les symptômes courants du problème de stock nul alors qu’il existe des écritures comptables article ouvertes :  

-   Le message suivant s’affiche lorsque vous tentez de clôturer une période d’inventaire : « La période d’inventaire ne peut pas être clôturée en raison d’un stock négatif pour un ou plusieurs articles ».  

-   Il existe une situation d’écriture comptable article où une écriture comptable article sortante et son écriture comptable article entrante associée sont ouvertes.  

     Consultez l’exemple suivant d’une écriture comptable article.  

     |N° écriture|Date comptabilisation|Type écriture|Type de document|N° document|Nombre d’articles|Code magasin|Quantité|Coût total (réel)|Quantité facturée|Quantité restante|Ouvrir|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|28/01/2018|Vente|Expédition vente|102043|TEST|BLEU|-1|-10|-1|-1|Oui|  
     |334|28/01/2018|Vente|Expédition vente|102043|TEST|BLEU|1|10|1|1|Oui|  

## Notions de base du lettrage article  
 Une écriture lettrage article est créée pour chaque mouvement de stock pour lier le destinataire de coût à sa source de coût afin que le coût puisse être transféré en fonction de la méthode d’évaluation du stock. Pour plus d’informations, voir [Détails de conception : traçabilité](design-details-item-application.md).  

-   Pour une écriture comptable article entrante, l’écriture lettrage article est créée lorsque l’écriture comptable article est créée.  

-   Pour une écriture comptable article sortante, l’écriture lettrage article est créée lorsque l’écriture comptable article est validée, à condition qu’il existe une écriture comptable article entrante ouverte avec une quantité disponible à laquelle elle peut être lettrée. S’il n’existe aucune écriture comptable article entrante ouverte à laquelle elle peut être lettrée, l’écriture comptable article sortante reste ouverte jusqu’à ce qu’une écriture comptable article entrante à laquelle elle peut être lettrée soit validée.  

 Il existe deux types de lettrage article :  

-   Lettrage de quantité  

-   Coût lettré  

### Lettrage de quantité  
 Les lettrages de quantité sont effectués pour tous les mouvements de stock et sont créés automatiquement, ou manuellement dans des processus spécifiques. Lorsqu’ils sont effectués manuellement, les lettrages de quantité sont appelés des lettrages fixes.  

 Le schéma suivant décrit la façon dont les lettrages de quantité sont effectués.  

![Flux de l’ajustement des coûts de l’achat à la vente.](media/helene/TechArticleInventoryZero2.png "Flux de l’ajustement des coûts de l’achat à la vente")

 En outre, notez que l’écriture comptable article 1 (Achat) est le fournisseur de l’article et la source de coût de l’écriture comptable article lettrée, c’est-à-dire l’écriture comptable article 2 (Vente).  

> [!NOTE]  
>  Si l’écriture comptable article sortante est évaluée par coût moyen, l’écriture comptable article entrante lettrée n’est pas l’unique source de coût. Elle joue simplement un rôle dans le calcul du coût moyen de la période.  

### Coût lettré  
Les lettrages de coût sont uniquement créés pour les transactions entrantes lorsque le champ **Écriture article à lettrer** est renseigné pour fournir un lettrage fixe. Cela se produit généralement dans le cadre d’un avoir vente ou d’un scénario d’annulation de l’expédition. Le lettrage de coût garantit que l’article retourne dans le stock avec le même coût que lorsqu’il a été livré.  

Le schéma suivant décrit la façon dont les lettrages de coût sont effectués.  

|N° écriture|Date comptabilisation|Type écriture|Type de document|N° document|Nombre d’articles|Code magasin|Quantité|Coût total (réel)|Quantité facturée|Quantité restante|Ouvrir|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|28/01/2018|Vente|Expédition vente|102043|TEST|BLEU|-1|-10|-1|-1|Oui|  
|334|28/01/2018|Vente|Expédition vente|102043|TEST|BLEU|1|10|1|1|Oui|  

 En outre, notez que l’écriture comptable entrante 3 (Retour vente) est un destinataire de coût pour l’écriture comptable article sortante d’origine 2 (Vente).  

## Illustration d’un flux de coûts de base  
 Imaginez un flux de coûts complet où un article est reçu, expédié et facturé, retourné avec la contrepassation du coût exact et réexpédié.  

 Le schéma suivant illustre le flux de coûts.  

![Flux de l’ajustement des coûts de la vente au retour vente.](media/helene/TechArticleInventoryZero4.png "Flux de l’ajustement des coûts de la vente au retour vente")

 En outre, notez que le coût est transféré vers l’écriture comptable article 2 (Vente), puis vers l’écriture comptable article 3 (Retour vente) et enfin vers l’écriture comptable article 4 (Vente 2).  

## Raisons du problème  
 Les scénarios suivants peuvent être à l’origine d’un problème de stock nul alors qu’il existe des écritures comptables article ouvertes :  

-   Scénario 1 : une expédition et une facture sont validées bien que l’article ne soit pas disponible. La validation est ensuite contrepassée du coût exact avec un avoir vente.  

-   Scénario 2 : une expédition est validée bien que l’article ne soit pas disponible. La validation est ensuite annulée avec la fonction Annuler expédition.  

 Le schéma suivant illustre la façon dont les lettrages article sont effectués dans les deux scénarios.  

![Le flux de l’ajustement des coûts va dans les deux directions.](media/helene/TechArticleInventoryZero6.png "Le flux de l’ajustement des coûts va dans les deux directions")  

 En outre, notez qu’un lettrage de coût est effectué (représenté par les flèches bleues) pour garantir que l’écriture comptable article 2 (Retour vente) a les mêmes coûts que l’écriture comptable article qu’elle contrepasse, c’est-à-dire l’écriture comptable article 1 (Vente 1). Toutefois, un lettrage de quantité (représenté par les flèches rouges) n’est pas créé.  

 L’écriture comptable article 2 (Retour vente) ne peut pas être un destinataire de coût de l’écriture comptable article d’origine et en même temps un fournisseur d’articles et leur source de coûts. Par conséquent, l’écriture comptable article d’origine 1 (Vente 1) reste ouverte jusqu’à ce qu’une source valide s’affiche.  

## Identification du problème  
 Pour déterminer si les écritures comptables article ouvertes sont créées, procédez comme suit pour le scénario respectif :  

 Pour le scénario 1, identifiez le problème comme suit :  

-   Sur la page **Avoir vente enregistré** ou **Réception retour enregistrée**, recherchez le champ **Écriture article à lettrer** pour voir si le champ est renseigné, et auquel cas, à quelle écriture comptable article le coût de la réception retour est lettré.  

 Pour le scénario 2, identifiez le problème de l’une des manières suivantes :  

-   Recherchez une écriture comptable article sortante ouverte et une écriture comptable article entrante avec le même numéro dans le champ **N° document**, et Oui dans le champ **Correction**. Consultez l’exemple suivant d’une écriture comptable article.  

|N° écriture|Date comptabilisation|Type écriture|Type de document|N° document|Nombre d’articles|Code magasin|Quantité|Coût total (réel)|Quantité facturée|Quantité restante|Ouvrir|Correction|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|28/01/2018|Vente|Expédition vente|102043|TEST|BLEU|-1|-10|-1|-1|Oui|Non|  
|334|28/01/2018|Vente|Expédition vente|102043|TEST|BLEU|1|10|1|1|Oui|**Oui**|  

-   Sur la page **Expédition vente enregistrée**, recherchez le champ **Écriture article à lettrer** pour voir si le champ est renseigné, et auquel cas, à quelle écriture comptable article le coût de la réception retour est lettré.  

> [!NOTE]  
>  Les lettrages de coût ne peuvent pas être identifiés sur la page **Écritures article lettrées**, car cette page affiche uniquement les lettrages de quantité.  

 Pour les deux scénarios, identifiez le lettrage de coût concerné comme suit :  

1.  Ouvrez la table **Écriture lettrage article**.  

2.  Filtrez le champ **N° écriture comptable article** à l’aide du numéro de l’écriture comptable article (Retour vente).  

3.  Analysez l’écriture lettrage article, en tenant compte de ce qui suit :  

     Si le champ **N° écriture article sortant** est renseigné pour une écriture comptable article entrante (quantité positive), cela signifie que l’écriture comptable article entrante est le destinataire de coût de l’écriture comptable article sortante.  

     Consultez l’exemple suivant d’une écriture lettrage article.  

     |N° écriture|N° écriture comptable article|N° écriture article entrant|N° écriture article sortant|Quantité|Date comptabilisation|Coût lettré|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|28/01/2018|Oui|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 En outre, notez que le coût de l’écriture comptable article entrante 334 est lettré à l’écriture comptable article sortante 333.  

## Solution de contournement du problème  
 Sur la page **Feuille article**, validez les lignes suivantes pour l’article concerné :  

-   Un ajustement positif pour clôturer l’écriture comptable article sortante ouverte.  

-   Un ajustement négatif avec la même quantité.  

     Cet ajustement équilibre l’augmentation du stock causée par l’ajustement positif et clôture l’écriture comptable article entrante ouverte.  

 Le stock devient nul et toutes les écritures comptables article sont clôturées.  

## Voir aussi  
[Détails de conception : lettrage article](design-details-item-application.md)   
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]