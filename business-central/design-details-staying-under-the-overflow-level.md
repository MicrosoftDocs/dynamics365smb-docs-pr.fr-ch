---
title: Détails de conception - Rester sous le niveau de dépassement de capacité | Microsoft Docs
description: Lors de l'utilisation de Maximum Qty. et Fixed Reorder Qty., le système de planification se concentre sur le stock prévisionnel dans l'intervalle de planification donné uniquement. Cela signifie que le système de planification peut vous proposer l'approvisionnement superflu lorsqu'une demande négative ou des changements d'approvisionnement positifs se produisent en dehors de l'intervalle de planification donné.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: bf602a0a7688c0459b4f7a3711e4f3d75bd8ef00
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306811"
---
# <a name="design-details-staying-under-the-overflow-level"></a>Détails de conception : rester sous le niveau de dépassement de capacité
Lors de l'utilisation des méthodes Qté maximum et Qté fixe de commande, le système de planification se concentre sur le stock prévisionnel dans l'intervalle de planification donné uniquement. Cela signifie que le système de planification peut vous proposer l'approvisionnement superflu lorsqu'une demande négative ou des changements d'approvisionnement positifs se produisent en dehors de l'intervalle de planification donné. Si, pour cette raison, un approvisionnement superflu est proposé, le système de planification calcule la quantité à soustraire (ou supprimer) de l'approvisionnement pour éviter l'approvisionnement superflu. Cette quantité est appelée « niveau de dépassement de capacité ». Le dépassement de capacité est communiqué comme ligne de planification avec une action **Changer qté (diminuer)** ou **Annuler** et le message d'avertissement suivant :  

*Attention : le stock prévisionnel [xx] est supérieur au niveau de dépassement de capacité [xx] à la date d'échéance [xx].*  

![Niveau de dépassement de capacité](media/supplyplanning_2_overflow1_new.png "Niveau de dépassement de capacité")  

##  <a name="calculating-the-overflow-level"></a>Calcul du niveau de dépassement de capacité  
Le niveau de dépassement de capacité est calculé de différentes manières en fonction de la configuration de planification.  

### <a name="maximum-qty-reordering-policy"></a>Méthode de réapprovisionnement Qté maximum  
Niveau de dépassement de capacité = stock maximum  

> [!NOTE]  
>  Si une quantité minimum commande existe, alors elle sera ajoutée comme suit : Niveau de dépassement de capacité = Stock maximum + Quantité minimum commande.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Méthode de réapprovisionnement Qté fixe de commande  
Niveau de dépassement de capacité = Quantité de réappro. + Point de commande  

> [!NOTE]  
>  Si la quantité minimum commande est supérieure au point de commande, alors elle remplace comme suit : Niveau de dépassement de capacité = Quantité de réappro. + Quantité minimum commande  

### <a name="order-multiple"></a>Commandé par  
Si un multiple de commande existe, il ajuste le niveau de dépassement de capacité pour les deux méthodes de réapprovisionnement Qté maximum et Qté fixe de commande.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Création de la ligne planning avec l'avertissement de dépassement capacité  
Lorsqu'un approvisionnement existant rend le stock prévisionnel supérieur au niveau de dépassement de capacité à la fin d'un intervalle de planification, une ligne de planification est créée. Pour avertir sur le potentiel approvisionnement superflu, la ligne de planification a un message d'avertissement, le champ **Accepter message d'action** n'est pas sélectionné, et le message d'action est Cancel ou Change Qty.  

### <a name="calculating-the-planning-line-quantity"></a>Calcul de la Quantité pour la ligne planning  
Quantité pour la ligne planning = Quantité d'approvisionnement actif – (Stock prévisionnel – Niveau de dépassement de capacité)  

> [!NOTE]  
>  Comme pour toutes les lignes d'avertissement, les quantités maximales/minimales de commande ou les multiples de commande sont ignorés.  

### <a name="defining-the-action-message-type"></a>Définir le type de message d'action  

-   Si la quantité de la ligne planning est supérieure à 0, le message d'action est Changer qté.  
-   Si la quantité de la ligne planning est égale ou inférieure à 0, le message d'action est Annuler  

### <a name="composing-the-warning-message"></a>Composition du message d'avertissement  
Dans le cas d'un dépassement de capacité, la page **Éléments planning non chaînés** affiche un message d'avertissement avec les informations suivantes :  

-   Le niveau de stock prévisionnel qui a déclenché l'alerte  
-   Niveau de dépassement de capacité calculé  
-   Date d'échéance d'un événement d'approvisionnement.  

Exemple : « Le stock projeté 120 est supérieur au niveau de dépassement de capacité 60 au 28/01/11 »  

## <a name="scenario"></a>Scénario  
Dans ce scénario, un client modifie une commande vente de 70 à 40 pièces entre deux exécutions de planification. La fonction de dépassement de capacité intervient pour réduire l'achat qui a été proposé pour la quantité de ventes initiale.  

### <a name="item-setup"></a>Paramétrage de l'article  

|Méthode de réapprovisionnement|Qté maximum|  
|-----------------------|------------------|  
|Qté maximum commande|100|  
|Point de commande|50|  
|Stocks|80|  

### <a name="situation-before-sales-decrease"></a>Situation avant la sortie de vente  

|Événement|Changer qté|Stocks projetés|  
|-----------|-----------------|-------------------------|  
|Un jour|Aucune|80|  
|Vente|-70|10|  
|Fin de l'intervalle de planification|Aucune|10|  
|Suggérer une nouvelle commande achat|+90|100|  

### <a name="situation-after-sales-decrease"></a>Situation après la sortie de vente  

|Activer|Changer qté|Stocks projetés|  
|------------|-----------------|-------------------------|  
|Un jour|Aucune|80|  
|Vente|-40|40|  
|Achats|+90|130|  
|Fin de l'intervalle de planification|Aucune|130|  
|Proposer de réduire l'achat<br /><br /> achat de 90 à 60|-30|100|  

### <a name="resulting-planning-lines"></a>Lignes planning résultantes  
 Une ligne planning (avertissement) est créée pour réduire l'achat de 30 pour passer de 90 à 60 pour conserver le stock prévisionnel à 100 conformément au niveau de dépassement de capacité.  

![Planifier en fonction de niveau de dépassement de capacité](media/nav_app_supply_planning_2_overflow2.png "Planifier en fonction de niveau de dépassement de capacité")  

> [!NOTE]  
>  Sans la fonction Overflow, aucune alerte n'est créée si le niveau de stock prévisionnel est au-dessus du stock maximum. Cela pourrait entraîner un approvisionnement superflu de 30.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : méthodes de réapprovisionnement](design-details-reordering-policies.md)   
[Détails de conception : paramètres de planification](design-details-planning-parameters.md)   
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)
