---
title: Détails de conception – Coût moyen
description: Le coût moyen d’un article est calculé avec une moyenne pondérée périodique.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-average-cost"></a>Détails de conception : coût moyen

Le coût moyen d’un article est calculé avec une moyenne pondérée périodique. La moyenne est basée sur la période de coût moyen configurée dans [!INCLUDE[prod_short](includes/prod_short.md)].  

La date d’évaluation est définie automatiquement.  

## <a name="setting-up-average-cost-calculation"></a>Configuration du calcul du coût moyen

Le tableau suivant décrit les deux champs de la page **Paramètres stock** qui doivent être renseignés pour activer le calcul du coût moyen.  

|Champ|Désignation|  
|---------------------------------|---------------------------------------|  
|**Période coût moyen**|Spécifie à quel moment le coût moyen est calculé. Les options possibles sont les suivantes :<br /><br /> - **Jour**<br />- **Semaine**<br />- **Mois**<br />- **Période comptable**<br /><br /> Le coût moyen calculé pour cette période est affecté à toutes les sorties de stock validées au cours de la période coût moyen.|  
|**Type calcul coût moyen**|Indique le mode de calcul du coût moyen. Les options possibles sont les suivantes :<br /><br /> - **Article**<br />- **Article, variante et magasin**<br /> Avec cette option, le coût moyen est calculé pour chaque article, pour chaque magasin, et pour chaque variante de l’article. Le coût moyen de cet article dépend du lieu de stockage et de la variante de l’article que vous avez sélectionnés (par exemple, la couleur).|  

> [!NOTE]  
> Vous pouvez uniquement utiliser une période de coût moyen et un type de calcul de coût moyen dans une année fiscale.  
>
> La page **Périodes comptables** affiche la période coût moyen et le type de calcul du coût moyen qui est en vigueur au cours de la période, pour chaque période comptable.  

## <a name="calculating-average-cost"></a>Calcul du coût moyen

 Lorsque vous validez une transaction pour un article qui utilise la méthode évaluation stock coût moyen, une écriture est créée dans la table **Point d’entrée ajustement coût moyen**. Cette écriture contient le numéro d’article, le code variante et le code magasin de la transaction. L’écriture contient également le champ **Date évaluation**, qui spécifie la dernière date de la période coût moyen dans laquelle la transaction a été validée.  

> [!NOTE]  
> Ce champ ne doit pas être confondu avec le champ **Date évaluation** dans le tableau **Ecritures valeur** qui indique la date à laquelle la valeur entre en vigueur et est utilisé pour déterminer la période de coût moyen à laquelle l’écriture valeur appartient.  

 Le coût moyen d’une transaction est calculé lorsque le coût de l’article est ajusté. Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-cost-adjustment.md). Un ajustement des coûts utilise les écritures de la table **Point d’entrée ajustement coût moyen** pour identifier les articles (ou articles, magasins et variantes) pour lesquels calculer les coûts moyens. Pour chaque écriture dont le coût n’a pas été ajusté, l’ajustement des coûts utilise ce qui suit pour déterminer le coût moyen :  

- calcul du coût de l’article au début de la période coût moyen ;  
- Ajoute la somme des coûts entrants validés au cours de la période de coût moyen. Ceux-ci incluent les achats, les retours vente, les ajustements positifs, et les résultats de production et d’assemblage.  
- Soustrait la somme des coûts des transactions sortantes dotées d’un lien fixe avec les réceptions au cours de la période de coût moyen. Ceux-ci incluent généralement des retours achat et les sorties négatives.  
- division par la quantité en stock totale comme à la fin de la période coût moyen. Exclut les sorties de stock qui sont évaluées.  

 Le coût moyen calculé est appliqué aux sorties de stock pour l’article (ou article, magasin et variante) avec des dates comptabilisation qui surviennent au cours de la période coût moyen. Pour les entrées de stock lettrées de façon fixe sur des sorties de stock au cours de la période coût moyen, [!INCLUDE [prod_short](includes/prod_short.md)] transmet le coût moyen calculé de l’entrée à la sortie.  

### <a name="example-average-cost-period--day"></a>Exemple : période coût moyen = jour

L’exemple suivant montre l’effet du calcul du coût moyen basé sur une période coût moyen d’un jour. Le champ **Type calcul coût moyen** de la page **Paramètres stock** est défini sur **Article**.  

Le tableau suivant montre les écritures comptables pour l’exemple coût article moyen, ARTICLE1, avant que le traitement par lots **Ajuster coûts - Écr. article** ne s’exécute.  

| **Date de validation** | **Type écriture comptable article** | **Quantité** | **Montant (réel)** | **N° séquence** |
|--|--|--|--|--|
| 01/01/23 |   Achats | 0 | 20.00 | 0 |
| 01/01/23 |   Achats | 0 | 40.00 | 2 |
| 01/01/23 |   Vente | -1 | -20,00 | 3 |
| 02/01/23 |   Vente | -1 | -40,00 | 4 |
| 02/02/23 |   Achats | 0 | 100.00 | 5 |
| 02/03/23 |   Vente | -1 | -100,00 | 6 |

> [!NOTE]  
> Comme l’ajustement des coûts ne s’est pas encore produit, les valeurs du champ **Coût total (réel)** des diminutions de stock correspondent aux entrées de stock auxquelles elles s’appliquent.  

 Le tableau suivant montre les écritures de la table **Point d’entrée ajustement coût moyen** qui s’appliquent aux écritures valeur résultant des écritures comptables article dans la table précédente.  

| **N° article** | **Code variante** | **Code magasin** | **Date évaluation** | **Coût ajusté** |
|--|--|--|--|--|
| ARTICLE1 |  | BLEU | 01/01/23 |   N° |
| ARTICLE1 |  | BLEU | 02/01/23 |   N° |
| ARTICLE1 |  | BLEU | 02/02/23 |   N° |
| ARTICLE1 |  | BLEU | 02/03/23 |   N° |

 Le tableau suivant montre les mêmes écritures comptables une fois le traitement par lots **Ajuster coûts - Écr. article** exécuté. Le coût moyen par jour est calculé et appliqué aux sorties de stock.  

| **Date de validation** | **Type écriture comptable article** | **Quantité** | **Montant (réel)** | **N° séquence** |
|--|--|--|--|--|--|
| 01/01/23 |   Achats | 0 | 20.00 | 0 |
| 01/01/23 |   Achats | 0 | 40.00 | 2 |
| 01/01/23 |   Vente | -1 | -30,00 | 3 |
| 02/01/23 |   Vente | -1 | -30,00 | 4 |
| 02/02/23 |   Achats | 0 | 100.00 | 5 |
| 02/03/23 |   Vente | -1 | -100,00 | 6 |

### <a name="example-average-cost-period--month"></a>Exemple : période coût moyen = mois

 Cet exemple suivant montre l’effet du calcul du coût moyen basé sur une période coût moyen d’un mois. Le champ **Type calcul coût moyen** de la page **Paramètres stock** est défini sur **Article**.  

 Si la période coût moyen est d’un mois, [!INCLUDE [prod_short](includes/prod_short.md)] crée une seule écriture pour chaque combinaison de numéro article, code variante, code magasin et date évaluation.  

 Le tableau suivant montre les écritures comptables pour l’exemple coût article moyen, ARTICLE1, avant que le traitement par lots **Ajuster coûts - Écr. article** ne s’exécute.  

| **Date de validation** | **Type écriture comptable article** | **Quantité** | **Montant (réel)** | **N° séquence** |
|--|--|--|--|--|
| 01/01/23 |   Achats | 0 | 20.00 | 0 |
| 01/01/23 |   Achats | 0 | 40.00 | 2 |
| 01/01/23 |   Vente | -1 | -20,00 | 3 |
| 02/01/23 |   Vente | -1 | -40,00 | 4 |
| 02/02/23 |   Achats | 0 | 100.00 | 5 |
| 02/03/23 |   Vente | -1 | -100,00 | 6 |

> [!NOTE]  
> Comme l’ajustement des coûts ne s’est pas encore produit, les valeurs du champ **Coût total (réel)** des diminutions de stock correspondent aux entrées de stock auxquelles elles s’appliquent.  

Le tableau suivant montre les écritures de la table **Point d’entrée ajustement coût moyen** qui s’appliquent aux écritures valeur résultant des écritures comptables article dans la table précédente.  

| **N° article** | **Code variante** | **Code magasin** | **Date évaluation** | **Coût ajusté** |
|--|--|--|--|--|
| ARTICLE1 |  | BLEU | 01/31/23 |   N° |
| ARTICLE1 |  | BLEU | 02/28/23 |   N° |

> [!NOTE]  
> La date d’évaluation est définie au dernier jour de la période de coût moyen, qui est dans ce cas le dernier jour du mois.  

Le tableau suivant montre les mêmes écritures comptables une fois le traitement par lots **Ajuster coûts - Écr. article** exécuté. Le coût moyen par mois est calculé et appliqué aux sorties de stock.  

|**Date de validation** | **Type écriture comptable article** | **Quantité** | **Montant (réel)** | **N° séquence** |
|--|--|--|--|--|
| 01/01/23 | Achats | 0 | 20.00 | 0 |
| 01/01/23 | Achats | 0 | 40.00 | 2 |
| 01/01/23 | Vente | -1 | -30,00 | 3 |
| 02/01/23 | Vente | -1 | -65,00 | 4 |
| 02/02/23 | Achats | 0 | 100.00 | 5 |
| 02/03/23 | Vente | -1 | -65,00 | 6 |

Le coût moyen de l’entrée numéro 3 est calculé dans la période de coût moyen de janvier. Le coût moyen des entrées numéro 4 et 6 est calculé dans la période de coût moyen de février.  

Pour obtenir le coût moyen pour février, [!INCLUDE [prod_short](includes/prod_short.md)] ajoute le coût moyen de l’article reçu dans le stock (100,00) est ajouté au coût moyen au début de la période (30,00). La somme (130,00) est ensuite divisée par la quantité totale en stock (2). Ce calcul donne le coût moyen résultant de l’article au cours de la période de février (65,00). Le coût moyen est affecté aux sorties de stock dans la période (écritures 4 et 6).  

## <a name="setting-the-valuation-date"></a>Définition de la date d’évaluation

 Le champ **Date évaluation** de la table **Ecritures valeur** détermine la période du coût moyen à laquelle une écriture de sortie de stock appartient. Ce paramètre s’applique au stock travail en cours (TEC).  

 Le tableau suivant montre les critères utilisés pour définir la date évaluation.  

| Scénario | Date comptabilisation | Quantité valorisée | Réévaluation | Date évaluation |
|--|--|--|--|--|
| 1 |  | Positif | Non | Date comptabilisation de l’écriture comptable article |
| 2 | Ultérieur à la dernière date évaluation des écritures valeur lettrées | Négatif | Non | Date comptabilisation de l’écriture comptable article |
| 3 | Antérieur à la dernière date évaluation des écritures valeur lettrées | Positif | Non | Dernière date évaluation des écritures valeur lettrées |
| 4 |  | Négatif | Oui | Date comptabilisation de l’écriture de valeur de réévaluation. |

### <a name="example"></a>Exemple :

Le tableau suivant d’écritures valeur illustre les différents scénarios.  

| Scénario | Date comptabilisation | Type écriture comptable article | Date évaluation | Quantité valorisée | Coût total (réel) | N° écriture comptable article | N° écriture |
|--|--|--|--|--|--|--|--|
| 1 | 01/01/20 | Achats | 01/01/20 | 2 | 20.00 | 1 | 1 |
| 2 | 15/01/20 | (Frais annexes) | 01/01/20 | 2 | 8,00 | 1 | 2 |
| 3 | 01/02/20 | Vente | 01/02/20 | -1 | -14,00 | 2 | 3 |
| 4 | 01/03/20 | (Réévaluation) | 01/03/20 | 1 | -.4,00 | 1 | 4 |
| 5 | 01/02/20 | Vente | 01/03/20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> Dans le numéro de séquence 5 dans la table précédente, l’utilisateur a saisi une commande vente avec une date comptabilisation (01/02/20) qui est antérieure à la dernière date évaluation des écritures valeur lettrées (01/03/20). Si la valeur correspondante dans le champ **Coût total (réel)** pour cette date (02-01-20) a été utilisée pour cette entrée, elle est 14,00. Cela donnerait une situation où la quantité en stock est égale à zéro, mais la valeur stock est de -4,00.  
>
> Pour éviter une telle erreur quantité-valeur, la date d’évaluation est configurée pour être égale à la dernière date évaluation des écritures valeur appliquées (03-01-20). La valeur du champ **Coût total (réel)** devient 10,00 (après réévaluation), ce qui signifie que la quantité en stock est égale à zéro, et la valeur de stock est également zéro.  

> [!CAUTION]  
> Comme l’état **Évaluation du stock** est basé sur la date comptabilisation, l’état reflète toutes les erreurs de correspondance de quantité-valeur dans les scénarios comme dans l’exemple ci-dessus. Pour plus d’informations, voir [Détails de conception : évaluation du stock](design-details-inventory-valuation.md).  

Si la quantité en stock est inférieure à zéro après avoir validé la sortie de stock, la date évaluation est d’abord définie à la date comptabilisation de la sortie du stock. Vous pouvez modifier cette date lorsque l’entrée de stock est appliquée, conformément aux règles décrites dans la remarque précédente dans cette section.  

## <a name="recalculating-average-cost"></a>Recalcul du coût moyen

L’évaluation des sorties de stock sous forme de moyenne pondérée serait simple dans plusieurs scénarios :

- Les achats sont toujours facturés avant les ventes.
- Les publications ne sont jamais antidatées.
- Vous n’avez jamais fait d’erreurs.

Cependant, la réalité est différente.  

Comme cela est illustré dans les exemples de cet article, la date d’évaluation est définie comme la date à partir de laquelle l’écriture valeur est incluse dans le calcul du coût moyen. Ce paramètre vous permet de faire plusieurs choses pour les articles avec la méthode de coût moyen :  

- Facturer la vente d’un article avant que l’achat de l’article aient été facturé.  
- Antidater une validation.  
- Rétablir une validation incorrecte.  

> [!NOTE]  
> Un autre motif de cette flexibilité est le lettrage fixe. Pour plus d’informations sur le lettrage fixe, voir [Détails de conception : lettrage article](design-details-item-application.md).  

En raison de cette flexibilité, vous pouvez être amené à recalculer le coût moyen après que la validation associée s’est produite. Par exemple, si vous validez une entrée de stock ou une sortie avec une date évaluation antérieure à une ou plusieurs sorties de stock. Le nouveau calcul du coût moyen se produit automatiquement lorsque vous exécutez le traitement par lots **Ajuster coûts - Écr. article**, manuellement ou automatiquement.  

Vous pouvez modifier la base d’évaluation du stock au cours d’une période comptable en modifiant les valeurs des champs **Période coût moyen** et **Type calcul coût moyen**. Cependant, nous vous recommandons d’être prudent et de consulter votre auditeur.  

### <a name="example-of-recalculated-average-cost"></a>Exemple de coût moyen recalculé

Cet exemple montre comment [!INCLUDE [prod_short](includes/prod_short.md)] recalcule le coût moyen lorsque vous validez à une date antérieure à une sortie de stock. L’exemple est basé sur une période coût moyen **Jour**.  

Le tableau suivant montre les écritures valeur qui existent pour l’article avant la validation.  

| Date évaluation | Quantité | Coût total (réel) | N° écriture |
|--|--|--|--|
| 01/01/20 | 1 | 10.00 | 1 |
| 02/01/20 | 1 | 20.00 | 2 |
| 15/02/20 | -1 | -15,00 | 3 |
| 16/02/20 | -1 | -15,00 | 4 |

L’utilisateur valide une entrée de stock (écriture numéro 5) avec une date évaluation (01-03-20) intervenant avant une sortie de stock. Pour équilibrer le stock, le coût moyen doit être recalculé et ajusté à 17,00.  

Le tableau suivant montre les écritures valeur qui existent pour l’article après la saisie du numéro de séquence 5.  

| Date évaluation | Quantité | Coût total (réel) | N° écriture |
|--|--|--|--|
| 01/01/20 | 1 | 10.00 | 1 |
| 02/01/20 | 1 | 20.00 | 2 |
| 03/01/20 | 1 | 21.00 | 5 |
| 15/02/20 | -1 | -17,00 | 3 |
| 16/02/20 | -1 | -17,00 | 4 |

## <a name="see-also"></a>Voir aussi

[Détails de conception : mode d’évaluation stock](design-details-inventory-costing.md)  
[Détails de conception : méthodes de calcul des coûts](design-details-costing-methods.md)  
[Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)  
[Détails de conception : lettrage article](design-details-item-application.md)  
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Finance](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glossaire des termes dans les processus métier Dynamics 365](/dynamics365/guidance/business-processes/glossary)  
[Vue d’ensemble Définir les coûts des produits et des services](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
