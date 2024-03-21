---
title: Introduction à Contoso Coffee
description: Vue d’ensemble des scénarios relatifs à la façon dont les données de démonstration Contoso Coffee peuvent vous aider à apprendre à utiliser les capacités d’entreposage dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Introduction aux entrepôts de Contoso Coffee

Contoso Coffee est une société fictive qui produit des cafetières grand public et commerciales. Les applications **Contoso Coffee** pour Business Central ajoutent des données de démonstration que vous pouvez utiliser pour apprendre à utiliser les capacités d’entreposage dans Business Central. Vous pouvez configurer les fonctionnalités de l’entrepôt de différentes manières, voir [Présentation des différentes options de configuration](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

L’application propose trois emplacements optimisés pour différents scénarios :

- **ARGENT**  

  Cet emplacement est configuré pour utiliser des bacs. Il peut être facilement configuré pour prise en charge de base ou avancée. 

- **JAUNE**  

  Cet emplacement utilise la configuration d’entrepôt avancée, mais n’utilise pas d’emplacements. Il peut être reconfiguré pour prendre en charge les configurations de base.

- **BLANC**  

  Cet emplacement utilise la configuration avancée de l’entrepôt avec des rangements et des prélèvements dirigés, ce qui permet d’appliquer des règles plus avancées sur la façon dont les articles se déplacent dans l’entrepôt.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Configurer les données d’entreposage de Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Une fois que les applications appropriées sont installées, accédez à la page [Outil de démonstration Contoso](https://businesscentral.dynamics.com/?page=5194) dans [!INCLUDE [prod_short](../../includes/prod_short.md)], sélectionnez la ligne *Module d’entrepôt* et utilisez l’action **Configurer** pour préparer les modules. Les tableaux suivants décrivent les paramètres :  

|Champ  |Désignation  |
|---------|---------|
|**Emplacement magasin**  |L’emplacement à utiliser pour les scénarios d’emplacement de base.|
|**Magasin – Avancé**  |L’emplacement à utiliser pour les scénarios d’emplacement simple.|
|**Magasin - Prélèvement et rangement suggérés**  |L’emplacement à utiliser pour les scénarios d’emplacement avancés.|
|**Magasin en transit**  |L’emplacement à utiliser pour l’emplacement en transit dans les scénarios de transfert.|
|**N° client**  |Le client à utiliser pour les scénarios de base et simples dans les opérations de vente.|
|**N° de fournisseur**  |Le fournisseur à utiliser pour tous les scénarios dans les opérations d’achat.|
|**N° article 1**  |Spécifie le numéro principal à utiliser pour tous les scénarios.|
|**N° article 2**  |Spécifie le numéro supplémentaire à utiliser pour tous les scénarios.|
|**N° article 3**  |L’article avec suivi.|

Une fois que vous êtes prêt, choisissez l’action **Créer des données de démonstration**. L’ajout des données à la base de données sous-jacente prend quelques minutes, mais vous êtes ensuite prêt à exécuter les différents scénarios.  

> [!IMPORTANT]
> Si vous exécutez les scénarios, vous souhaiterez peut-être vérifier que votre utilisateur a été ajouté comme pour les emplacements sélectionnés. Pour plus d’informations, voir [Configurer des employés d’entrepôt](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Cas de figure

Les données de démonstration d’entreposage Contoso Coffee prennent actuellement en charge les scénarios suivants pour les tests et la formation :

1.  [Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt de base](warehouse-basic-flow-putaway-pick.md)
2.  [Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt mixtes](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt avancées avec prélèvement et rangement suggérés](warehouse-directed-flow.md)

Lisez les étapes de chaque scénario dans l’article correspondant.  

## <a name="see-also"></a>Voir aussi

[Configuration de stock](../../inventory-setup-inventory.md) 
[Configurer les emplacements](../../inventory-how-setup-locations.md) 
[Entreposage](../../warehouse-manage-warehouse.md) 
[Détails de la conception](../../design-details-warehouse-overview.md) 
