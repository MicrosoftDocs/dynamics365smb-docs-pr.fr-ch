---
title: Détails de conception – Coût moyen
description: 'Le coût moyen d’un article est calculé avec une moyenne pondérée périodique, selon la période coût moyen qui est paramétrée dans Business Central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: edupont
---
# Détails de conception : coût moyen
Le coût moyen d’un article est calculé avec une moyenne pondérée périodique, selon la période coût moyen qui est paramétrée dans [!INCLUDE[prod_short](includes/prod_short.md)].  

 La date d’évaluation est définie automatiquement.  

## Configuration du calcul du coût moyen  
 Le tableau suivant décrit les deux champs de la page **Paramètres stock** qui doivent être renseignés pour activer le calcul du coût moyen.  

|Champ|Désignation|  
|---------------------------------|---------------------------------------|  
|**Période coût moyen**|Spécifie à quel moment le coût moyen est calculé. Les options possibles sont les suivantes :<br /><br /> -   **Jour**<br />-   **Semaine**<br />-   **Mois**<br />-   **Période comptable**<br /><br /> Le coût moyen calculé pour cette période est affecté à toutes les sorties de stock validées au cours de la période coût moyen.|  
|**Type calcul coût moyen**|Indique le mode de calcul du coût moyen. Les options possibles sont les suivantes :<br /><br /> -   **Article**<br />-   **Article, variante et magasin**<br /> Avec cette option, le coût moyen est calculé pour chaque article, pour chaque magasin, et pour chaque variante de l’article. Cela signifie que le coût moyen de cet article dépend du lieu de stockage et de la variante de l’article que vous avez sélectionnés (par exemple, la couleur).|  

> [!NOTE]  
>  Vous pouvez uniquement utiliser une période de coût moyen et un type de calcul de coût moyen dans une année fiscale.  
>   
>  La page **Périodes comptables** affiche la période coût moyen et le type de calcul du coût moyen qui est en vigueur au cours de la période, pour chaque période comptable.  

## Calcul du coût moyen  
 Lorsque vous validez une transaction pour un article qui utilise la méthode évaluation stock coût moyen, une écriture est créée dans la table **Point d’entrée ajustement coût moyen**. Cette écriture contient le numéro d’article, le code variante et le code magasin de la transaction. L’écriture contient également le champ **Date évaluation**, qui spécifie la dernière date de la période coût moyen dans laquelle la transaction a été validée.  

> [!NOTE]  
>  Ce champ ne doit pas être confondu avec le champ **Date évaluation** dans le tableau **Ecritures valeur** qui indique la date à laquelle la valeur entre en vigueur et est utilisé pour déterminer la période de coût moyen à laquelle l’écriture valeur appartient.  

 Le coût moyen d’une transaction est calculé lorsque le coût de l’article est ajusté. Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-cost-adjustment.md). Un ajustement des coûts utilise les écritures de la table **Point d’entrée ajustement coût moyen** pour identifier les articles (ou articles, magasins et variantes) pour lesquels calculer les coûts moyens. Pour chaque écriture dont le coût n’a pas été ajusté, l’ajustement des coûts utilise ce qui suit pour déterminer le coût moyen :  

-   calcul du coût de l’article au début de la période coût moyen ;  
-   Ajoute la somme des coûts entrants validés au cours de la période de coût moyen. Ceux-ci incluent les achats, les retours vente, les ajustements positifs, et les résultats de production et d’assemblage.  
-   Soustrait la somme des coûts des transactions sortantes dotées d’un lien fixe avec les réceptions au cours de la période de coût moyen. Ceux-ci incluent généralement des retours achat et les sorties négatives.  
-   Divise par la quantité d’inventaire totale pour la fin de la période coût moyen, sans les sorties de stock qui sont évaluées.  

 Le coût moyen calculé est appliqué aux sorties de stock pour l’article (ou article, magasin et variante) avec des dates comptabilisation qui surviennent au cours de la période coût moyen. S’il y a des entrées de stock lettrées de façon fixe sur des sorties de stock au cours de la période coût moyen, le calcul du coût moyen est transmis de l’entrée à la sortie.  

### Exemple : période coût moyen = jour  
 L’exemple suivant montre l’effet du calcul du coût moyen basé sur une période coût moyen d’un jour. Le champ **Type calcul coût moyen** de la page **Paramètres stock** est défini sur **Article**.  

 Le tableau suivant montre les écritures comptables pour l’exemple coût article moyen, ARTICLE1, avant que le traitement par lots **Ajuster coûts - Écr. article** ne s’exécute.  

| **Date de validation** | **Type écriture comptable article** | **Quantité** | **Coût total (réel)** | **N° écriture** |
|--|--|--|--|--|
| 01/01/20 | Achats | 1 | 20.00 | 1 |
| 01/01/20 | Achats | 1 | 40.00 | 2 |
| 01/01/20 | Vente | -1 | -20,00 | 3 |
| 01/02/20 | Vente | -1 | -40,00 | 4 |
| 02/02/20 | Achats | 1 | 100,00 | 5 |
| 03/02/20 | Vente | -1 | -100,00 | 6 |

> [!NOTE]  
>  Comme l’ajustement des coûts ne s’est pas encore produit, les valeurs du champ **Coût total (réel)** des diminutions de stock correspondent aux entrées de stock auxquelles elles s’appliquent.  

 Le tableau suivant montre les écritures de la table **Point d’entrée ajustement coût moyen** qui s’appliquent aux écritures valeur résultant des écritures comptables article dans la table précédente.  

| **N° article** | **Code variante** | **Code magasin** | **Date évaluation** | **Coût ajusté** |
|--|--|--|--|--|
| ARTICLE1 |  | BLEU | 01/01/20 | Non |
| ARTICLE1 |  | BLEU | 01/02/20 | Non |
| ARTICLE1 |  | BLEU | 02/02/20 | Non |
| ARTICLE1 |  | BLEU | 03/02/20 | Non |

 Le tableau suivant montre les mêmes écritures comptables une fois le traitement par lots **Ajuster coûts - Écr. article** exécuté. Le coût moyen par jour est calculé et appliqué aux sorties de stock.  

| **Date de validation** | **Type écriture comptable article** | **Quantité** | **Coût total (réel)** | **N° écriture** |
|--|--|--|--|--|--|
| 01/01/20 | Achats | 1 | 20.00 | 1 |
| 01/01/20 | Achats | 1 | 40.00 | 2 |
| 01/01/20 | Vente | -1 | -30,00 | 3 |
| 01/02/20 | Vente | -1 | -30,00 | 4 |
| 02/02/20 | Achats | 1 | 100,00 | 5 |
| 03/02/20 | Vente | -1 | -100,00 | 6 |

### Exemple : période coût moyen = mois  
 L’exemple suivant montre l’effet du calcul du coût moyen basé sur une période coût moyen d’un mois. Le champ **Type calcul coût moyen** de la page **Paramètres stock** est défini sur **Article**.  

 Si la période coût moyen est d’un mois, une seule écriture est créée pour chaque combinaison de numéro article, code variante, code magasin et date évaluation.  

 Le tableau suivant montre les écritures comptables pour l’exemple coût article moyen, ARTICLE1, avant que le traitement par lots **Ajuster coûts - Écr. article** ne s’exécute.  

| **Date de validation** | **Type écriture comptable article** | **Quantité** | **Coût total (réel)** | **N° écriture** |
|--|--|--|--|--|
| 01/01/20 | Achats | 1 | 20.00 | 1 |
| 01/01/20 | Achats | 1 | 40.00 | 2 |
| 01/01/20 | Vente | -1 | -20,00 | 3 |
| 01/02/20 | Vente | -1 | -40,00 | 4 |
| 02/02/20 | Achats | 1 | 100,00 | 5 |
| 03/02/20 | Vente | -1 | -100,00 | 6 |

> [!NOTE]  
>  Comme l’ajustement des coûts ne s’est pas encore produit, les valeurs du champ **Coût total (réel)** des diminutions de stock correspondent aux entrées de stock auxquelles elles s’appliquent.  

 Le tableau suivant montre les écritures de la table **Point d’entrée ajustement coût moyen** qui s’appliquent aux écritures valeur résultant des écritures comptables article dans la table précédente.  

| **N° article** | **Code variante** | **Code magasin** | **Date évaluation** | **Coût ajusté** |
|--|--|--|--|--|
| ARTICLE1 |  | BLEU | 31/01/20 | Non |
| ARTICLE1 |  | BLEU | 28/02/20 | Non |

> [!NOTE]  
>  La date d’évaluation est définie au dernier jour de la période de coût moyen, qui est dans ce cas le dernier jour du mois.  

 Le tableau suivant montre les mêmes écritures comptables une fois le traitement par lots **Ajuster coûts - Écr. article** exécuté. Le coût moyen par mois est calculé et appliqué aux sorties de stock.  

|**Date de validation**|**Type écriture comptable article**|**Quantité**|**Coût total (réel)**|**N° écriture**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01/01/20|Achats|1|20.00|1|  
|01/01/20|Achats|1|40.00|2|  
|01/01/20|Vente|-1|-30,00|3|  
|01/02/20|Vente|-1|-65,00|4|  
|02/02/20|Achats|1|100,00|5|  
|03/02/20|Vente|-1|-65,00|6|  

 Le coût moyen pour l’entrée numéro 3 est calculé dans la période coût moyen pour janvier, et le coût moyen pour les écritures 4 et 6 est calculé dans la période coût moyen pour février.  

 Pour obtenir le coût moyen pour février, le coût moyen de la pièce reçue dans le stock (100,00) est ajouté au coût moyen au début de la période (30,00). La somme des deux (130,00) est ensuite divisée par la quantité totale en stock (2) ce qui permet d’obtenir le coût moyen de l’article dans la période de février (65,00). Le coût moyen est affecté aux sorties de stock dans la période (écritures 4 et 6).  

## Définition de la date d’évaluation  
 Le champ **Date évaluation** de la table **Ecritures valeur** permet de déterminer à quelle période coût moyen appartient une écriture de sortie de stock. Ceci s’applique au stock travail en cours (TEC).  

 Le tableau suivant montre les critères utilisés pour définir la date évaluation.  

|Scénario|Date comptabilisation|Quantité valorisée|Réévaluation|Date évaluation|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positif|Non|Date comptabilisation de l’écriture comptable article|  
|2|Ultérieur à la dernière date évaluation des écritures valeur lettrées|Négatif|Non|Date comptabilisation de l’écriture comptable article|  
|3|Antérieur à la dernière date évaluation des écritures valeur lettrées|Positif|Non|Dernière date évaluation des écritures valeur lettrées|  
|4||Négatif|Oui|Date comptabilisation de l’écriture de valeur de réévaluation.|  

### Exemple :  
 Le tableau suivant d’écritures valeur illustre les différents scénarios.  

|Scénario|Date comptabilisation|Type écriture comptable article|Date évaluation|Quantité valorisée|Coût total (réel)|N° écriture comptable article|N° écriture|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01/01/20|Achats|01/01/20|2|20.00|1|1|  
|2|15/01/20|(Frais annexes)|01/01/20|2|8,00|1|2|  
|3|01/02/20|Vente|01/02/20|-1|-14,00|2|3|  
|4|01/03/20|(Réévaluation)|01/03/20|1|-.4,00|1|4|  
|5|01/02/20|Vente|01/03/20|-1|-10,00|3|5|  

> [!NOTE]  
>  Dans le numéro de séquence 5 dans la table précédente, l’utilisateur a saisi une commande vente avec une date comptabilisation (01/02/20) qui est antérieure à la dernière date évaluation des écritures valeur lettrées (01/03/20). Si la valeur correspondante dans le champ **Coût total (réel)** pour cette date (02-01-20) a été utilisée pour cette entrée, elle est 14,00. Cela donnerait une situation où la quantité en stock est égale à zéro, mais la valeur stock est de -4,00.  
>   
>  Pour éviter une telle erreur quantité-valeur, la date d’évaluation est configurée pour être égale à la dernière date évaluation des écritures valeur appliquées (03-01-20). La valeur du champ **Coût total (réel)** devient 10,00 (après réévaluation), ce qui signifie que la quantité en stock est égale à zéro, et la valeur de stock est également zéro.  

> [!CAUTION]  
>  Comme l’état **Évaluation du stock** est basé sur la date comptabilisation, l’état reflète toutes les erreurs de correspondance de quantité-valeur dans les scénarios comme dans l’exemple ci-dessus. Pour plus d’informations, voir [Détails de conception : évaluation du stock](design-details-inventory-valuation.md).  

 Si la quantité en stock est inférieure à zéro après avoir validé la sortie de stock, la date évaluation est d’abord définie à la date comptabilisation de la sortie du stock. Cette date peut être modifiée plus tard, en fonction des règles décrites dans la remarque précédente dans cette section, lorsque l’augmentation de stock est appliquée.  

## Recalcul du coût moyen  
 L’évaluation des diminutions de stock en tant que moyenne pondérée serait directe si les achats étaient facturés avant la facturation des ventes, que les validations n’étaient jamais antidatées, et que vous ne commettiez jamais d’erreurs. Toutefois, la réalité est un peu différente de cet idéal.  

 Comme cela est illustré dans les exemples de cette rubrique, la date d’évaluation est définie comme la date à partir de laquelle l’écriture valeur est incluse dans le calcul du coût moyen. Cela vous offre la flexibilité d’effectuer les opérations suivantes pour les articles utilisant la méthode de coûts Average :  

-   Facturer la vente d’un article avant que l’achat de l’article aient été facturé.  
-   Antidater une validation.  
-   Rétablir une validation incorrecte.  

> [!NOTE]  
>  Un autre motif de cette flexibilité est le lettrage fixe. Pour plus d’informations sur le lettrage fixe, voir [Détails de conception : lettrage article](design-details-item-application.md).  

 En raison de cette flexibilité, vous pouvez être amené à recalculer le coût moyen après que la validation associée s’est produite. Par exemple, si vous validez une entrée de stock ou une sortie avec une date évaluation antérieure à une ou plusieurs sorties de stock. Le nouveau calcul du coût moyen se produit automatiquement lorsque vous exécutez le traitement par lots **Ajuster coûts - Écr. article**, manuellement ou automatiquement.  

 Vous pouvez modifier la base d’évaluation du stock au cours d’une période comptable en modifiant le champ **Période coût moyen** et le champ **Type calcul coût moyen**. Cependant, cette action doit être menée avec soin et en accord avec un auditeur.  

### Exemple :  
 L’exemple suivant illustre la manière dont le coût moyen est recalculé lorsqu’une validation en retard est introduite à une date qui se trouve avant une ou plusieurs sorties de stock. L’exemple est basé sur une période coût moyen **Jour**.  

 Le tableau suivant montre les écritures valeur qui existent pour l’article avant la validation.  

|Date évaluation|Quantité|Coût total (réel)|N° écriture|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01/01/20|1|10.00|1|  
|02/01/20|1|20.00|2|  
|15/02/20|-1|-15,00|3|  
|16/02/20|-1|-15,00|4|  

 L’utilisateur valide une entrée de stock (écriture numéro 5) avec une date évaluation (01-03-20) intervenant avant une ou plusieurs sorties de stock. Pour équilibrer le stock, le coût moyen doit être recalculé et ajusté à 17,00.  

 Le tableau suivant montre les écritures valeur qui existent pour l’article après la saisie du numéro de séquence 5.  

|Date évaluation|Quantité|Coût total (réel)|N° écriture|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01/01/20|1|10.00|1|  
|02/01/20|1|20.00|2|  
|03/01/20|1|21.00|5|  
|15/02/20|-1|-17,00|3|  
|16/02/20|-1|-17,00|4|  

## Voir aussi  
 [Détails de conception : évaluation stock](design-details-inventory-costing.md)   
 [Détails de conception : modes évaluation stock](design-details-costing-methods.md)   
 [Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)   
 [Détails de conception : lettrage article](design-details-item-application.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
 [Finances](finance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]