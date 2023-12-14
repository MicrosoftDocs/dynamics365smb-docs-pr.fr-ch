---
title: 'Détails de conception - Flux pour la production, l’assemblage et les tâches'
description: 'Découvrez le flux entre les emplacements d’entrepôt pour le prélèvement des composants et le rangement des articles finis pour l’assemblage, la production ou les ordres de travail.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs"></a>Flux pour la production, l’assemblage et les tâches

Les flux internes, tels que le prélèvement de composants et le rangement des articles finis pour l’assemblage, les tâches et les ordres de fabrication, sont similaires aux flux entrants ou sortants. Ainsi, de nombreux processus peuvent sembler familiers. Cet article fournit des informations sur l’utilisation des flux d’entrepôt internes avec différents niveaux de complexité.

## <a name="overview-of-different-configuration-options"></a>Aperçu des différentes options de configuration

Vous pouvez configurer les fonctionnalités d’entrepôt de différentes manières. Il est important que les options que vous choisissez améliorent vos processus sans entraîner de surcharge. Les tableaux suivants décrivent les configurations typiques de traitement des biens physiques pour la production, les tâches et les ordres d’assemblage.

### <a name="inbound-flow-put-away"></a>Flux entrant (rangement)

|Niveau de complexité|Description|Paramètres|Code emplacement|Flux entrant de l’ordre de fabrication|Flux entrant de l’ordre d’assemblage|Flux entrant de tâches|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Aucune activité entrepôt dédiée.|Validation à partir des ordres et des feuilles.||Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Feuille production -> Feuille sortie</br><br/> **REMARQUE** : Vous pouvez valider la sortie à l’aide de la **Feuille production**.|Ordre d’assemblage|Le rangement ne s’applique pas aux tâches|  
|Basique|Commande par commande.|Rangement requis. </br><br/> **REMARQUE** : bien que le paramètre soit appelé **Rangement requis**, vous pouvez toujours publier la sortie des documents origine aux emplacements où vous cochez cette case. |Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Ordre de fabrication -> Rangement stock|Ordre d’assemblage|Le rangement ne s’applique pas aux tâches|
|Avancé|Activités de rangement regroupées pour plusieurs documents origines.|Réception requise + Rangement requis|Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Ordre(s) de fabrication -> Feuille sortie|Ordre(s) d’assemblage -> mouvements internes | Le rangement ne s’applique pas aux tâches|
|Avancé|Comme ci-dessus + activités de prélèvement/rangement dirigées|Prélèvement et rangement dirigés (les boutons à bascule dépendants seront activés automatiquement)|Obligatoire|Comme ci-dessus.|Comme ci-dessus.| Le rangement ne s’applique pas aux tâches|

Certaines configurations ne vous permettent pas d’utiliser des documents d’entrepôt dédiés pour enregistrer les rangements. Toutefois, si votre site utilise des emplacements, vous pouvez utiliser des documents de mouvement génériques pour déplacer les articles produits ou assemblés vers l’entrepôt. Learn more at [Déplacement des articles en interne dans les configurations entrepôt de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a>Flux sortant (prélèvement)

|Niveau de complexité|Description|Paramètres|Code emplacement|Flux sortant de l’ordre de fabrication|Flux sortant de l’ordre d’assemblage|Flux sortant de tâches|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Aucune activité entrepôt dédiée.|Validation à partir des ordres et des feuilles.||Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Feuille production -> Feuille consommation </br><br/> **REMARQUE** : Vous pouvez valider la consommation à l’aide de la **Feuille production**.|Ordre d’assemblage|Tâche -> Feuille projet|  
|Basique|Commande par commande.|Prélèvement requis. </br><br/> **REMARQUE** : bien que le paramètre soit appelé **Prélèvement requis**, vous pouvez toujours publier la sortie des documents origine aux emplacements où vous cochez cette case. <!-- ToDo Test prod output-->|Facultatif. Contrôlé par le bouton à bascule **Code emplacement obligatoire**.|Ordre de fabrication -> Prélèvement stock|Ordre de fabrication -> mouvement de stock</br><br/>Le **Mouvement de stock** ne peut être utilisé qu’avec des emplacements.|Tâche -> Prélèvement stock|
|Avancé|Activités de prélèvement regroupées pour plusieurs documents origines.|Expédition requise + Prélèvement requis|Facultatif. Contrôlé par le bouton à bascule Code emplacement obligatoire|Ordre(s) de fabrication ->Prélèvement entrepôt -> Feuille consommation |Ordre(s) d’assemblage -> Prélèvement entrepôt| Tâche(s) -> Prélèvement entrepôt -> Feuille projet |
|Avancé|Comme ci-dessus + activités de prélèvement/rangement dirigées|Prélèvement et rangement dirigés (les boutons à bascule dépendants seront activés automatiquement)|Obligatoire|Comme ci-dessus.|Comme ci-dessus.| Le prélèvement et le rangement dirigés ne sont pas pris en charge pour les tâches|

Comme pour le flux entrant, certaines configurations ne vous permettent pas d’utiliser des documents d’entrepôt dédiés pour enregistrer les rangements. Si votre site utilise des emplacements, vous pouvez utiliser des documents de mouvement génériques pour déplacer les articles produits ou assemblés. Learn more at [Déplacement d’articles](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Entrepôts sans activité d’entrepôt dédiée

Même si vous n’avez pas d’activités d’entrepôt dédiées, vous souhaiterez probablement toujours suivre des éléments tels que la consommation et la production. Les articles suivants fournissent des informations sur le traitement des réceptions pour les documents origine.

* [Enregistrer la consommation et la production pour une ligne ordre de fabrication lancé](production-how-to-register-consumption-and-output.md)
* [Assembler des articles](assembly-how-to-assemble-items.md)
* [Enregistrer la consommation ou l′utilisation pour les projets](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Configuration d’entrepôt de base

Les flux entrants et sortants dans une configuration d’entrepôt de base impliquent les paramètres suivants sur la page **Fiche magasin** pour l’emplacement :

* Pour le flux entrant (rangement), activez le bouton à bascule **Rangement requis** , mais désactivez le bouton à bascule **Réception requise**.
* Pour le flux sortant (prélèvement), activez le bouton à bascule **Prélèvement requis**, mais désactivez le bouton à bascule **Expédition requise**.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flux vers et depuis la production dans une configuration d’entrepôt de base

Utilisez les documents **Prélèvement stock** pour prélever des composants de production dans le flux vers la production. Pour ranger les produits que vous fabriquez, utilisez les documents **Rangement stock**.

Pour les sites qui utilisent des emplacements, les documents de mouvement de stock sont particulièrement utiles pour la consommation des composants. Pour en savoir plus sur la façon dont la consommation de composants passe des emplacements de consommation aux emplacements atelier ouverts, consultez [Consommation des composants de production dans l’entrepôt](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Les mouvements de stock sont des documents importants si vous utilisez les méthodes de consommation **Prélèvement + Aval** ou **Prélèvement + Amont**. Learn more at [Méthodes de consommation](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Les champs **Code emplacement des consommations**, **Code emplacement après production**, et **Code emplacement atelier ouvert** du magasin ou du poste/centre de charge définissent le flux par défaut depuis ou vers les zones de production.
* Gérez le mouvement des articles produits sur la page **Mouvement interne** sans rapport avec un ordre de fabrication.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flux vers et depuis l’assemblage dans une configuration d’entrepôt de base

Validez le résultat d’assemblage et la consommation directement à partir d’un ordre d’assemblage.

> [!NOTE]
> Les documents **Prélèvement stock** et **Rangement stock** ne sont pas pris en charge pour les ordres d’assemblage.

Pour les sites qui utilisent des emplacements :

* Utilisez les documents **Mouvement stock** pour déplacer les composants d’assemblage vers la zone d’assemblage.
* Les champs **Code empl. vers assemblage**, **Code empl. depuis assemblage** de la fiche magasin définissent les flux par défaut depuis et vers les zones d’assemblage.
* Gérez le mouvement des articles assemblés sur la page **Mouvement interne**, sans rapport avec un ordre d’assemblage.

[!INCLUDE [prod_short](includes/prod_short.md)] prend en charge les flux d’assemblage Assembler pour stock et Assembler pour commande. Learn more at [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). En ce qui concerne la gestion des entrepôts, l’assemblage pour stock fait partie du flux interne de l’entrepôt et l’assemblage pour commande se trouve dans le flux sortant de l’entrepôt. En savoir plus sur [Traitement des articles à assembler pour commande dans les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flux pour la gestion de projet dans une configuration d’entrepôt de base

Utilisez les documents **Prélèvement stock** pour sélectionner les composants de la tâche dans le flux vers la gestion de projet.

Pour un site qui utilise des emplacements, le champ **Code emplacement vers projet** sur l’emplacement définit les flux par défaut vers la gestion de projet.

## <a name="advanced-warehouse-configurations"></a>Configurations d’entrepôt avancées

Les flux entrants et sortants dans une configuration d’entrepôt avancée impliquent les paramètres suivants sur la page **Fiche magasin** pour l’emplacement :

* Pour le flux entrant (rangement), activez les boutons à bascule **Réception requise** et **Rangement requis**.
* Pour le flux sortant (prélèvement), activez les boutons à bascule **Expédition requise** et **Réception requise**.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flux vers et depuis la production dans une configuration d’entrepôt avancée

Utilisez les documents **Prélèvement entrepôt** et la page **Feuille prélèvement** pour prélever des composants pour la production.

Pour les sites qui utilisent des emplacements :

* Les documents **Mouvement entrepôt** et la page **Feuille mouvement** sont particulièrement utiles pour la consommation des composants. Learn more at [Consommation des composants de production dans l’entrepôt](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-a-advanced-warehouse-configuration).
* Les champs **Code emplacement des consommations**, **Code emplacement après production** et **Code emplacement atelier ouvert** du magasin ou du poste/centre de charge définissent le flux par défaut depuis ou vers les zones de production. 
* Gérez le mouvement des articles produits sur les pages **Feuille mouvement** ou **Rangement interne entrepôt** sans rapport avec un ordre de fabrication.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flux vers et depuis l’assemblage dans une configuration d’entrepôt avancée

Utilisez les documents **Prélèvement entrepôt** et la page **Feuille prélèvement** pour prélever des composants pour l’assemblage.

Pour les sites qui utilisent des emplacements :

* Les champs **Code empl. vers assemblage** et **Code empl. depuis assemblage** du magasin définissent le flux par défaut depuis et vers les champs d’assemblage.
* Gérez le mouvement des éléments d’assemblage sur les pages **Feuille mouvement** ou **Rangement interne entrepôt** sans rapport avec un ordre d’assemblage.

[!INCLUDE [prod_short](includes/prod_short.md)] prend en charge les flux d’assemblage Assembler pour stock et Assembler pour commande. Learn more at [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

L’assemblage pour stock fait partie du flux interne de l’entrepôt et l’assemblage pour commande se trouve dans le flux sortant de l’entrepôt. Learn more at [Traitement des articles à assembler pour commande dans les expéditions entrepôt](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flux pour la gestion de projet dans une configuration d’entrepôt avancée

Utilisez les documents **Prélèvement entrepôt** et la page **Feuille prélèvement** pour prélever des composants dans le flux pour la gestion de projet.

Pour les site qui utilisent des emplacements, le champ **Code emplacement vers projet** sur l’emplacement définit les flux par défaut vers la zone du projet.

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
