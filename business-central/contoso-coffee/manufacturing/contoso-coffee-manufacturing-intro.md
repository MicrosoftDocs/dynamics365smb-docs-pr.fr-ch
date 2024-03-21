---
title: Introduction à la fabrication Contoso Coffee
description: Vue d’ensemble des scénarios relatifs à la façon dont les données de démonstration Contoso Coffee peuvent vous aider à apprendre à utiliser les capacités de fabrication dans Business Central.
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# Introduction à la fabrication Contoso Coffee

Contoso Coffee est une société fictive qui produit des cafetières grand public et commerciales. Les applications **Contoso Coffee** pour Business Central ajoutent des données de démonstration que vous pouvez utiliser pour apprendre à utiliser les capacités de fabrication dans Business Central.  

L’application propose quatre produits optimisés pour différents scénarios :

- **SP-SCM1009 Airpot**  

  Ce produit est une nomenclature (BOM) avec un sous-ensemble, **Gamme**. Utilisez-le pour faire la démonstration du flux de production standard. Il est configuré avec des gammes alternatives que vous pouvez utiliser pour illustrer différents scénarios impliquant des sous-traitants. Le mode d’évaluation stock est *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Ce produit requiert une traçabilité et possède un composant qui requiert également une traçabilité. Le mode d’évaluation stock est *Spécifique*.  

- **SP-SCM1004 Autodrip**  

  Ce produit est une nomenclature avec un sous-ensemble, **Gamme**. Nous le recommandons pour faire la démonstration des différentes méthodes de consommation à la fois pour les composants et les opérations. Le mode d’évaluation stock est *Standard*.

- **SP-SCM1006 AutoDripLite**

  Ce produit comporte trois variantes et trois nomenclatures pouvant être affectées à des points de stock. Le produit utilise le concept de nomenclature fantôme. Le mode d’évaluation stock est *Standard*.

Les activités de fabrication pour tous les scénarios utilisent l’emplacement *PRINCIPAL*.  

> [!IMPORTANT]
> Avant d’exécuter l’un des scénarios pour Contoso Coffee, validez toutes les lignes feuille article avec soldes d’ouverture. Pour connaître plus d’exigences, voir la section [Configurer les données de Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## Configurer les données de fabrication Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Champ  |Désignation  |
|---------|---------|
|**Lieu de production** |Spécifie l’entrepôt que vous souhaitez utiliser pour les opérations de production. La valeur par défaut est *PRINCIPAL*, mais vous pouvez la modifier selon vos besoins.|


Une fois que vous êtes prêt, choisissez l’action **Créer des données de démonstration**. L’ajout des données à la base de données sous-jacente prend quelques minutes, mais vous êtes ensuite prêt à exécuter les différents scénarios.  

## Cas de figure

Les données de démonstration de facturation Contoso Coffee prennent actuellement en charge les scénarios suivants pour les tests et la formation :

1. [Créer une nomenclature de production et une version de nomenclature](create-new-production-bom-version.md)  
2. [Créer une gamme](create-new-routing.md)  
3. [Création d’un ordre de fabrication planifié fixe et le modifier](create-firm-planned-production-order-change.md)  
4. [Combiner la consommation automatique et la consommation manuelle](combine-automatic-manual-flushing.md)  
5. [Utiliser la planification des commandes pour créer et réserver un approvisionnement](order-planning-create-reserve-supply.md)  
6. [Configurer et traiter une opération de sous-traitance](set-up-process-subcontracting-operation.md)  
7. [Configurer une nouvelle capacité](set-up-new-capacity.md)  
8. [Prévoir la demande pour des variantes articles avec différentes nomenclatures affectées](variants.md)  

Lisez les étapes de chaque scénario dans l’article correspondant.  

> [!IMPORTANT]
> Ces procédures pas à pas nécessitent que l’expérience utilisateur soit définie sur *Premium* dans la page **Informations société**.

## Voir aussi

[Production](../../production-manage-manufacturing.md)  
[États de production et analyses dans Business Central](../../production-reports.md)  
