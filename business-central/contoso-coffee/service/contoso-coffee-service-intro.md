---
title: Introduction à la gestion des services Contoso Coffee
description: Cet article vous présente les données de démonstration de Contoso Coffee pour la gestion des services.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Introduction à la gestion des services Contoso Coffee

Contoso Coffee est une société fictive qui produit des cafetières grand public et commerciales. Les applications **Contoso Coffee** pour Business Central ajoutent des données de démonstration que vous pouvez utiliser pour apprendre à utiliser les capacités de gestion des services dans Business Central.

Cette application fournit plusieurs éléments qui sont utilisés pour les procédures détaillées principales :

- Ressources avec des compétences attribuées
- Articles configurés pour créer des articles de service
- Articles de prêt

> [!IMPORTANT]
> Avant d’exécuter l’un des scénarios pour Contoso Coffee, validez toutes les lignes feuille article avec soldes d’ouverture. Pour connaître plus d’exigences, voir la section [Configurer les données de Contoso Coffee](#set-up-contoso-coffee-service-management-data).
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Configurer les données de gestion des services Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Une fois que les applications appropriées sont installées, accédez à la page [Outil de démonstration Contoso](https://businesscentral.dynamics.com/?page=5194) dans [!INCLUDE [prod_short](../../includes/prod_short.md)], sélectionnez la ligne *Module de service* et utilisez l’action **Configurer** pour préparer les modules. La table suivante décrit les paramètres :  

|Champ  |Désignation  |
|---------|---------|
|**N° client**  |Le client à utiliser pour les scénarios dans les opérations de vente.|
|**N° de fournisseur**  |Le fournisseur à utiliser pour tous les scénarios dans les opérations d’achat.|
|**N° article 1**  |L’article à utiliser pour les scénarios de réparation et de maintenance.|
|**N° article de service 1**  |L’article de type service à utiliser pour le scénario de réparation.|
|**N° article de service 2**  |L’article de type service à utiliser pour le scénario de réparation.|
|**N° ressource 1**  |La ressource à utiliser pour les scénarios de contrat.|
|**N° ressource 2**  |La ressource à utiliser pour les scénarios de panne-réparation.|
|**Emplacement du service** |Spécifie l’entrepôt que vous souhaitez utiliser pour les opérations de service. La valeur par défaut est *PRINCIPAL*, mais vous pouvez la modifier selon vos besoins.|

Une fois que vous êtes prêt, choisissez l’action **Créer des données de démonstration**. L’ajout des données à la base de données sous-jacente prend quelques minutes, mais vous êtes ensuite prêt à exécuter les différents scénarios.  

## <a name="scenarios"></a>Cas de figure

Les données de démonstration Contoso Coffee prennent actuellement en charge les scénarios de service suivants pour les tests et la formation :

1. Créez une commande de service pour une demande de réparation ad-hoc, placez et recevez des articles de prêt, enregistrez le temps et facturez les clients en suivant la [Procédure pas à pas sur les commandes de service pour les articles de service](service-basic-flow-order.md)
2. Créez des contrats de service, générez des commandes de service, facturez les frais de contrat et affectez des ressources en suivant la [Procédure pas à pas sur les contrats de service pour les articles de service](service-contract-flow.md)

Lisez les étapes de chaque scénario dans l’article correspondant.  

> [!IMPORTANT]
> Ces procédures détaillées de service nécessitent que l’expérience utilisateur soit définie sur **Premium** dans la page **Informations société**.


## <a name="see-also"></a>Voir aussi

[Service](../../service-service.md)
