---
title: Paramétrer les statuts des commandes service et des réparations | Microsoft Docs
description: Vous devez paramétrer neuf états réparation qui identifient la progression de la réparation et de la maintenance des articles de service des commandes service.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Paramétrer les statuts des commandes service et des réparations

Vous devez paramétrer des états réparation qui identifient la progression de la réparation et de la maintenance des articles de service des commandes service. Vous devez configurer au moins neuf options de statut réparation identifiant les situations ou les actions effectuées lors de la maintenance des articles de service.  

Vous pouvez définir le niveau de priorité des options de statut commande service. Quatre niveaux de priorité sont disponibles : **Très haute**, **Haute**, **Moyenne** et **Basse**.  

Lorsque vous modifiez le statut réparation d’un article de service d’une commande service, le statut commande service est mis à jour. Le statut réparation de chaque article de service est lié au statut commande service. Si les articles de service sont liés à plusieurs options de statut commande service, le statut de commande service dont la priorité est la plus élevée est sélectionnée.  

Avant de pouvoir configurer un statut de réparation, vous devez définir des priorités de statut de service.

## <a name="to-set-up-service-status-priorities"></a>Pour configurer les priorités statut service

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Statut commande service**, puis choisissez le lien associé.  
2. Sélectionnez le statut commande service pour lequel vous voulez configurer une priorité.  
3. Dans le champ **Priorité**, choisissez la priorité souhaitée pour ce statut commande service.  

Répétez les étapes 2 et 3 pour configurer la priorité des quatre options statut : **Suspendu**, **En cours**, **Terminé** et **En attente**.  

## <a name="to-set-up-a-repair-status"></a>Pour configurer le statut réparation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **État réparation**, puis choisissez le lien associé.
2. Créez un état réparation.  
3. Renseignez les champs **Code** et **Désignation**.  
4. Dans le champ **Statut commande service**, choisissez le statut de la commande auquel lier l’état de réparation. Le champ **Priorité** affiche la priorité du statut commande service que vous avez choisie.  
5. Choisissez un état réparation. Vous ne pouvez en choisir qu’un. Le statut réparation ne peut pas être lié à une option de statut réparation.  
6. Pour valider des commandes service comprenant des articles de service avec cet état réparation, choisissez le champ **Validation autorisée**.  
7. Pour pouvoir faire passer manuellement l’option de statut commande service sur **Suspendu** dans des commandes service comprenant des articles de service avec ce statut réparation, choisissez la case à cocher **Statut Suspendu autorisé**.  
8. Choisissez de la même manière les cases à cocher **Statut En cours autorisé**, **Statut Terminé autorisé** et **Statut En attente autorisé**.

Répétez ces étapes pour chaque option de statut réparation à créer.

## <a name="see-also"></a>Voir aussi

[Statut commande service et statut réparation](service-service-order-status-and-repair-status.md)  
[Paramétrage de la gestion des services](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
