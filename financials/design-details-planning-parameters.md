---
title: "Détails de conception - Paramètres de planification | Microsoft Docs"
description: "Cette rubrique décrit les différents paramètres de planification que vous pouvez utiliser dans Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 335063984ab5d8ef1cbc9187352aa12287f6ade0
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-planning-parameters"></a>Détails de conception : paramètres de planification
Cette rubrique décrit les différents paramètres de planification que vous pouvez utiliser dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

La façon dont le système de planification contrôle l'approvisionnement d'article est déterminée par divers paramètres de la fiche article ou du point de stock, et des paramètres dans la configuration de la production. Le tableau suivant montre comment ces paramètres sont utilisés pour la planification.  

|Objet|Paramètre|  
|-------------|---------------|  
|Définir si l'article doit être planifié|Méthode de réapprovisionnement = Vide|  
|Définir la date de réapprovisionnement|Intervalle de planification<br /><br /> Point de commande<br /><br /> Délai de sécurité|  
|Définir la quantité à réapprovisionner|Stock de sécurité<br /><br /> Méthode de réapprovisionnement :<br /><br /> -   Qté fixe de commande plus Quantité de réappro.<br />-   Qté maximum plus Stock maximum<br />-   Commande<br />-   Lot pour lot|  
|Optimisez quand et combien réapprovisionner|Période de replanification<br /><br /> Période de groupement de lots<br /><br /> Période tampon|  
|Modifiez les commandes approvisionnement|Qté minimum commande<br /><br /> Qté maximum commande<br /><br /> Commandé par|  
|Délimiter l'article planifié|Mode de lancement :<br /><br /> -   Fabrication sur stock<br />-   Fabrication à la commande|  

## <a name="define-if-the-item-will-be-planned"></a>Définir si l'article doit être planifié  
Pour inclure un article/point de stock dans le processus de planification, il doit avoir une méthode de réapprovisionnement sinon il doit être planifié manuellement, par exemple, avec la fonction Order Planning.  

## <a name="define-when-to-reorder"></a>Définir la date de réapprovisionnement  
Les propositions de commande sont généralement lancées seulement lorsque la quantité disponible prévue est inférieure à une certaine quantité donnée. Cette quantité est définie par le point de commande. Sinon, elle est égale à zéro. Zéro peut être ajusté en saisissant une quantité de stock de sécurité. Si l'utilisateur a défini un délai de sécurité, la proposition sera livrée dans la période précédant la date d'échéance demandée.  

Le champ **Intervalle de planification** est utilisé par les stratégies de point de commande (**Qté fixe de commande** et **Qté maximum**), où le niveau de stock est vérifié après chaque intervalle de planification. Le premier intervalle de planification débute à la date de début de la planification.  

> [!NOTE]  
>  Lors du calcul des intervalles de planification, le système de planification ignore les calendriers de travail définis dans le champ **Code calendrier principal** des fenêtres **Informations société** et **Fiche magasin**.  

Le délai de sécurité par défaut, dans la fenêtre **Paramètres production** doit être défini à au moins un jour. La date d'échéance de la demande peut être connue, mais pas l'heure d'échéance. La planification planifie en amont pour répondre à la demande brute et, si aucun délai de sécurité n'est défini, les marchandises peuvent arriver trop tard pour répondre à la demande.  

Trois champs de période de réapprovisionnement supplémentaires, **Période de replanification**, **Période de groupement de lots** et **Période tampon**, jouent également un rôle en définissant quand commander à nouveau. Pour plus d'informations, reportez-vous à la section « Optimiser quand et combien réapprovisionner ».  

## <a name="define-how-much-to-reorder"></a>Définir la quantité à réapprovisionner  
Si le système de planification détecte un besoin de réapprovisionnement, la méthode de réapprovisionnement sélectionnée est utilisée pour déterminer quand et combien commander.  

Indépendamment de la méthode de réapprovisionnement, le système de planification suit généralement cette logique :  

1. La quantité de la proposition de commande est calculée pour atteindre le niveau de stock minimum spécifié de l'article, généralement le stock de sécurité. Si aucune valeur n'est spécifiée, le niveau de stock minimum est égal à zéro.  
2. Si le stock disponible projeté est inférieur au stock de sécurité, une commande approvisionnement planifiée en amont est suggérée. La quantité de commande remplira au moins le stock de sécurité, et peut être augmentée par une demande brute dans l'intervalle de planification, par la méthode de réapprovisionnement, ainsi que par les modificateurs de commande.  
3. Si le stock prévisionnel est égal ou inférieur au point de commande (calculé à partir des modifications agrégées dans l'intervalle de planification) et supérieur au stock de sécurité, une commande d'exception planifiée en aval est suggérée. La demande brute à satisfaire et la méthode de réapprovisionnement détermineront la quantité de commande. Au minimum, la quantité commandée doit être égale au point de commande.  
4. S'il y a plus de demande brute due avant la date de fin de la proposition commande planifiée en aval, et si cette demande amène le stock disponible projeté calculé actuellement en dessous du stock de sécurité, la quantité commandée est augmentée pour compenser le déficit. La commande approvisionnement suggérée est alors planifiée en amont à partir de la date d'échéance de la demande brute qui aurait entamé le stock de sécurité.  
5. Si le champ **Intervalle de planification** n'est pas renseigné, seule la demande brute à la même date d'échéance sera ajoutée.  

     Les champs de période de réapprovisionnement suivants jouent également un rôle dans la définition de la quantité à réapprovisionner : **Période de replanification**, **Période de groupement de lots** et **Période tampon**. Pour plus d'informations, reportez-vous à la section « Optimiser quand et combien réapprovisionner ».  

### <a name="reordering-policies"></a>Méthodes de réapprovisionnement  
Les méthodes de réapprovisionnement suivantes affectent la quantité en cours de réapprovisionnement.  

|Méthode de réapprovisionnement|Désignation|  
|-----------------------|---------------------------------------|  
|**Qté fixe de commande.**|Au minimum, la quantité commandée est égale à la quantité de réapprovisionnement. Il est possible de l'augmenter pour répondre à la demande ou atteindre le niveau de stock voulu. Cette méthode de réapprovisionnement est généralement utilisée avec un point de commande.|  
|**Qté maximum**|La quantité commande est calculée pour répondre au stock maximum. Si des modificateurs de quantité sont utilisés, le stock maximum peut être dépassé. Nous vous recommandons de ne pas utiliser l'intervalle de planification avec la quantité maximale. L'intervalle de planification est généralement outrepassé. Cette méthode de réapprovisionnement est généralement utilisée avec un point de commande.|  
|**Commande**|La quantité commande est calculée pour répondre à chacun des événements de demande, et l'ensemble demande-approvisionnement reste lié jusqu'à l'exécution. Aucun paramètres de planification n'est pris en compte.|  
|**Lot pour lot**|La quantité est calculée pour satisfaire la somme de la demande qui arrive à échéance dans l'intervalle de planification.|  

##  <a name="optimize-when-and-how-much-to-reorder"></a>Optimisez quand et combien réapprovisionner  
Pour obtenir un programme d'approvisionnement rationnel, un gestionnaire réglera avec précision les paramètres de planification afin de limiter les suggestions de replanification, accumuler les demandes (quantité de réappro. dynamique) ou éviter les actions de planification insignifiantes. Les champs de période de réapprovisionnement suivants permettent d'optimiser le moment où réapprovisionner et la quantité à réapprovisionner.  

|Champ|Désignation|  
|---------------------------------|---------------------------------------|  
|**Période de replanification**|Ce champ est utilisé pour déterminer si le message d'action doit replanifier une commande existante ou l'annuler et créer une nouvelle commande. L'ordre existant sera replanifié dans une période de replanification avant l'approvisionnement actif et jusqu'à une période de replanification après la date d'approvisionnement actif.|  
|**Période de groupement de lots**|Avec la méthode de réapprovisionnement lot pour lot, ce champ est utilisé pour regrouper plusieurs besoins d'approvisionnement dans une commande d'approvisionnement. À partir du premier approvisionnement prévu, le système cumule tous les besoins d'approvisionnement dans la période de groupement de lots suivante en un approvisionnement unique, effectuée lors de la date du premier approvisionnement. La demande effectuée en dehors de la période de groupement de lots n'est pas couverte par cet approvisionnement.|  
|**Période tampon**|Ce champ permet d'éviter une replanification mineure de l'approvisionnement existant dans le temps. Les modifications de la date approvisionnement jusqu'à une période tampon de la date approvisionnement ne génèrent aucun message d'action.<br /><br /> Par conséquent, un delta positif entre la nouvelle date d'approvisionnement proposée et la date d'approvisionnement d'origine est toujours supérieur à la période tampon.|  

Le temps de la période de replanification, de la période tampon, ainsi que de la période de groupement de lots est basée sur une date d'approvisionnement. L'intervalle de planification est basé sur la date de début de la planification, comme l'indique la figure suivante.  

![Éléments de la fréquence de vérification](media/supply_planning_5_time_bucket_elements.png "supply_planning_5_time_bucket_elements")  

Dans les exemples suivants, les flèches noires représentent l'approvisionnement existant (vers le haut) et la demande (vers le bas). Les flèches rouge, verte et orange sont des suggestions de planification.  

**Exemple 1** : la date modifiée est en dehors de la période de replanification, ce qui entraîne l'annulation de l'approvisionnement existant. Un nouvel approvisionnement est proposé pour répondre à la demande dans la période de groupement de lots.  

![Période de replanification, Période de groupement de lots](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "supply_planning_5_recheduling_period_lot_accumulation_period")  

**Exemple 2** : la date modifiée se trouve dans la période de replanification, ce qui entraîne la replanification de l'approvisionnement existant. Un nouvel approvisionnement est proposé pour répondre à la demande hors de la période de groupement de lots.  

![Période de replanification, Période de groupement de lots, Replanification](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "supply_planning_5_recheduling_period_lot_accum_period_reschedule")  

**Exemple 3** : il existe une demande pour la période tampon et la quantité d'approvisionnement dans la période de groupement de lots correspond à la quantité d'approvisionnement. La demande suivante n'est pas couverte et un nouvel approvisionnement est proposé.  

![Période tampon, Période de groupement de lots](media/supply_planning_5_dampener_period_lot_accumulation_period.png "supply_planning_5_dampener_period_lot_accumulation_period")  

**Exemple 4** : il existe une demande pour la période tampon et l'approvisionnement reste à la même date. Toutefois, la quantité d'approvisionnement actif n'est pas suffisante pour répondre à la demande dans la période de groupement de lots, donc une action de modification de quantité pour la commande approvisionnement existante est suggérée.  

![Période tampon, Période de groupement de lots, Changer qté](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "supply_planning_5_dampener_period_lot_accumulation_period")  

**Valeurs par défaut :** la valeur par défaut du champ **Intervalle de planification** et des trois champs de période de réapprovisionnement est vide. Pour tous les champs, sauf le champ **Période tampon**, cela signifie 0D (zéro jours). Si le champ **Période tampon** est vide, la valeur globale du champ **Période tampon par défaut** de la fenêtre **Paramètres production** sera utilisée.  

## <a name="modify-the-supply-orders"></a>Modifiez les commandes approvisionnement  
Lorsque la quantité de la proposition de commande a été calculée, un ou plusieurs modificateurs de commande peuvent l'ajuster. Par exemple, la quantité maximum commande est supérieure ou égale à la quantité minimum commande, qui est supérieure ou égale au multiple de commande.  

La quantité est diminuée si elle dépasse la quantité maximum commande. Ensuite, il est augmenté s'il est inférieur à la quantité de commande minimale. Enfin, elle est arrondie par excès de façon à correspondre à un multiple spécifié de commande. La quantité restante utilise les mêmes ajustements jusqu'à ce que la demande totale ait été convertie en propositions commande.  

## <a name="delimit-the-item"></a>Délimiter l'article  
L'option **Mode de lancement** définit les commandes supplémentaires qui seront proposées par le calcul MRP.  

Si l'option **Fabrication sur stock** est utilisée, les commandes se rapportent uniquement à l'article en question.  

Si l'option **Fabrication à la commande** est utilisée, le système de planification analyse la nomenclature de l'article et crée des propositions commande liées supplémentaires pour les articles de niveau inférieur qui sont également définis comme Fabrication à la commande. Cela se poursuit tant que il existe des articles make-to-order dans les structures de nomenclature décroissantes.  

## <a name="see-also"></a>Voir aussi  
[Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md)   
[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md)   
[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md)

