---
title: Introduction aux données de démonstration Contoso Coffee
description: Vue d’ensemble des scénarios relatifs à la façon dont les données de démonstration Contoso Coffee peuvent vous aider à apprendre à utiliser les capacités dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Introduction aux données de démonstration Contoso Coffee

Contoso Coffee est une société fictive qui produit des cafetières grand public et commerciales. Les applications **Contoso Coffee** pour Business Central ajoutent des données de démonstration que vous pouvez utiliser pour apprendre à utiliser les capacités dans Business Central.  


## Configurer les données de Contoso Coffee

Pour utiliser les données de démonstration Contoso Coffee, vous devez installer deux applications dans la société concernée dans [!INCLUDE [prod_short](../includes/prod_short.md)] :  

- **Jeu de données de démonstration Contoso Coffee**  

    Cette application fournit des données de démonstration pour l’application de base.  
- **Jeu de données de démonstration Contoso Coffee (ID pays)**  

    Cette application ajoute du contenu spécifique au pays en plus de l’application de base.

Ajoutez les applications à une société vide dans un abonnement payant ou dans le cadre d’un essai. Par exemple, créez une société sans exemples de données à partir du guide de configuration assistée **Créer une nouvelle société** que vous pouvez ouvrir dans la liste **Sociétés**. Ajoutez ensuite les applications depuis le [marché](../ui-extensions-install-uninstall.md#install) si elles ne sont pas déjà répertoriées sur la page **Gestion des extensions**.  

Vous devez alors compléter :
 - Les [Paramètres production](manufacturing/contoso-coffee-manufacturing-intro.md) pour préparer l’utilisation des [scénarios de production](#manufacturing-scenarios)
 - Les [Paramètres entrepôt](warehousing/contoso-coffee-warehousing-intro.md) pour préparer l’utilisation des [scénarios d’entrepôt](#warehousing-scenarios)

## Scénarios de production

Les données de démonstration Contoso Coffee prennent actuellement en charge les scénarios de production suivants pour les tests et la formation :

1. [Créer une nomenclature de production et une version de nomenclature](manufacturing/create-new-production-bom-version.md)  
2. [Créer une gamme](manufacturing/create-new-routing.md)  
3. [Créer un ordre de fabrication planifié ferme et le modifier](manufacturing/create-firm-planned-production-order-change.md)  
4. [Combiner la consommation automatique et la consommation manuelle](manufacturing/combine-automatic-manual-flushing.md)  
5. [Utiliser la planification des commandes pour créer et réserver un approvisionnement](manufacturing/order-planning-create-reserve-supply.md)  
6. [Configurer et traiter une opération de sous-traitance](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Configurer une nouvelle capacité](manufacturing/set-up-new-capacity.md)  
8. [Prévoir la demande pour des variantes articles avec différentes nomenclatures affectées](manufacturing/variants.md)  

Lisez les étapes de chaque scénario dans l’article correspondant.  

> [!IMPORTANT]
> Ces procédures de production pas à pas nécessitent que l’expérience utilisateur soit définie sur *Premium* dans la page **Informations société**.

## Scénarios d’entreposage

Les données de démonstration Contoso Coffee prennent actuellement en charge les scénarios d’entreposage suivants pour les tests et la formation :

1.  Configurez les bacs par défaut, recevez et rangez avec le rangement de l’inventaire, prélevez et expédiez avec le prélèvement de l’inventaire de manière commande par commande avec [Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt de base](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Recevez et rangez plusieurs commandes entrantes à la fois avec le récépissé d’entrepôt, expédiez plusieurs commandes à la fois avec l’expédition de l’entrepôt, prélevez avec les prélèvements de l’entrepôt avec [Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt mixtes](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Configurer des bacs fixes pour l’unité de mesure de l’article, le cross-docking des utilisateurs pour réduire les mouvements physiques de marchandises, optimiser le placement des marchandises avec le réapprovisionnement des bacs, répartir les grandes unités de mesure en plus petites, répartir la cueillette entre les employés de l’entrepôt avec une feuille de travail de cueillette avec [Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt avancées avec prélèvement et rangement suggérés](warehousing/warehouse-directed-flow.md)

Lisez les étapes de chaque scénario dans l’article correspondant.
   
## Voir aussi

[Production](../production-manage-manufacturing.md)  
[Entreposage](../warehouse-manage-warehouse.md)  

