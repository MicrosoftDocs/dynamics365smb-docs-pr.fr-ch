---
title: Configurer des employés d’entrepôt
description: 'Chaque utilisateur exerçant une activité dans un entrepôt doit être configuré en tant qu''employé d''entrepôt affecté à un magasin par défaut, et éventuellement à d''autres magasins.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
ms.service: dynamics-365-business-central
---
# <a name="set-up-warehouse-employees"></a>Configuration des magasiniers

Vous devez configurer chaque utilisateur qui exécute des activités dans un entrepôt en tant qu’employé de l’entrepôt et les affecter à un emplacement par défaut. [!INCLUDE [prod_short](includes/prod_short.md)] filtre les activités de l’entrepôt à l’emplacement par défaut de l’employé. Ils ne peuvent effectuer les activités d’entrepôt qu’à l’emplacement. Vous pouvez aussi affecter un utilisateur à d’autres emplacements. Ils peuvent accéder, mais pas effectuer des activités à ces emplacements.

## <a name="to-set-up-warehouse-employees"></a>Pour configurer des employés d’entrepôt

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Sélectionnez le champ **Code utilisateur**, puis sélectionnez l’utilisateur à ajouter comme magasinier. Cliquez sur le bouton **OK**.  
4. Dans le champ **Code magasin**, entrez le code du magasin dans lequel va travailler l’utilisateur.  
5. Activez le bouton à bascule **Par défaut** pour définir le magasin comme seul emplacement pour les activités entrepôt de l’employé.  
6. Répétez ces étapes pour affecter d’autres employés à des magasins ou affecter d’autres magasins à des employés d’entrepôt existants.  

> [!TIP]
> Vous pouvez également utiliser l’action **M’ajouter en tant qu’employé de l’entrepôt** pour vous ajouter rapidement à la liste des employés de l’entrepôt. Par exemple, cela est utile lorsque vous testez les fonctionnalités.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/get-started-warehouse-management/) associée

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Définir une stratégie de validation des factures pour les utilisateurs](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
