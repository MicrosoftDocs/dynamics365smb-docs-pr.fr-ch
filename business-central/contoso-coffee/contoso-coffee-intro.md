---
title: Introduction aux données de démonstration Contoso Coffee
description: Vue d’ensemble des scénarios relatifs à la façon dont les données de démonstration Contoso Coffee peuvent vous aider à apprendre à utiliser les capacités dans Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Introduction aux données de démonstration Contoso Coffee

Contoso Coffee est une société fictive qui produit des cafetières grand public et commerciales. Les applications **Contoso Coffee** pour [!INCLUDE [prod_short](../includes/prod_short.md)] ajoutent des données de démonstration que vous pouvez utiliser pour apprendre à utiliser les capacités dans [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Configurer les données de Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Une fois les applications installées, sur la page **Outil de démonstration Contoso**, utilisez l’action **Configurer** pour préparer les modules suivants. Vous pouvez choisir d’installer toutes les données disponibles, y compris les données de configuration et de production, ou uniquement les données de configuration.

 - Le **Module commun** pour préparer les paramètres généraux requis par [!INCLUDE [prod_short](../includes/prod_short.md)]. Par exemple, des éléments comme des séries de numéros. 

La table suivante décrit les paramètres :  

|Champ  |Désignation  |
|---------|---------|
|**Année de début** |Spécifie la première année que vous souhaitez utiliser pour les données de démonstration Contoso Coffee. Selon la configuration de la société, l’année est soit une année civile, soit une année fiscale.|
|**Code pays/région**|Spécifie un code pays/région pour les clients et fournisseurs nationaux.|
|**Type de société**    |Spécifie si la société actuelle doit déclarer la TVA ou la taxe de vente. |
|**Facteur de prix**     |Spécifie un facteur pour convertir un prix USD/EUR en devise locale. *1* signifie que le prix est le même dans n’importe quelle devise. Un nombre plus élevé sera utilisé pour obtenir le prix dans la devise locale. |
|**Précision de l’arrondi**  |Spécifie la précision de l’arrondi avec laquelle vous souhaitez créer les données de démonstration.|

 - Le [Module de production](manufacturing/contoso-coffee-manufacturing-intro.md) pour préparer les [scénarios de production](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - Le [Module d’entreposage](warehousing/contoso-coffee-warehousing-intro.md) pour préparer les [scénarios d’entreposage](warehousing/contoso-coffee-warehousing-intro.md#scenarios).
 - Le [Module de service](service/contoso-coffee-service-intro.md) pour préparer les [scénarios de service](service/contoso-coffee-service-intro.md#scenarios).

Après avoir configuré les modules que vous souhaitez essayer, choisissez l’action **Générer** pour créer les données de démonstration correspondantes.

## Voir aussi

[Fabrication](../production-manage-manufacturing.md)  
[Entreposage](../warehouse-manage-warehouse.md)  
[Service](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

