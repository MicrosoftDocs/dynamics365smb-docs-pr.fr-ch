---
title: "Comment configurer des employés d'entrepôt | Microsoft Docs"
description: "Chaque utilisateur exerçant une activité dans un entrepôt doit être configuré en tant qu'employé d'entrepôt affecté à un magasin par défaut, et éventuellement à d'autres magasins."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6fb0aa48352bc35c2e9ee399a3d0b17032a5ed7e
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-warehouse-employees"></a>Procédure : configurer des employés d'entrepôt
Chaque utilisateur exerçant une activité dans un entrepôt doit être configuré en tant qu'employé d'entrepôt affecté à un magasin par défaut, et éventuellement à d'autres magasins. Cette configuration d'utilisateur filtre toutes les activités entrepôt dans la base de donnée pour le magasin de l'employé, de sorte que l'employé peut uniquement effectuer les activités entrepôt dans le magasin par défaut. Un utilisateur peut être affecté à d'autres magasins pour lesquels il peut consulter les lignes activité sans pour autant exécuter les activités.

## <a name="to-set-up-warehouse-employees"></a>Pour configurer des employés d'entrepôt  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Salariés entrepôt**, puis sélectionnez le lien connexe.  
2. Sélectionnez l'action **Nouveau**.  
3. Sélectionnez le champ **Code utilisateur**, puis sélectionnez l'utilisateur à ajouter comme magasinier. Cliquez sur le bouton **OK**.  
6.  Dans le champ **Code magasin**, entrez le code du magasin dans lequel va travailler l'utilisateur.  
7.  Activez la case à cocher **Par défaut** pour définir le magasin comme seul emplacement pour les activités entrepôt de l'employé.  
8.  Répétez ces étapes pour affecter d'autres employés à des magasins ou affecter d'autres magasins à des employés d'entrepôt existants.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

