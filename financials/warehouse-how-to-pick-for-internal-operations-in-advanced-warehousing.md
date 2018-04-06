---
title: "Comment prélever pour des opérations internes dans les configurations de stockage avancées | Microsoft Docs"
description: "Dans les configurations de stockage avancées, dans lequel le magasin est configuré pour utiliser le prélèvement ainsi que l'expédition, vous pouvez prélever des composants pour les activités de fabrication et d'assemblage à l'aide de la fenêtre **Prélèvement entrepôt**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0a18e88ae9bb34b3cf5aa9d4a28e1d087ba9aa40
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a>Prélever pour l'assemblage ou la fabrication dans les configurations de stockage avancées.
Dans les configurations de stockage avancées, dans lequel le magasin est configuré pour utiliser le prélèvement ainsi que l'expédition, vous pouvez prélever des composants pour les activités de fabrication et d'assemblage à l'aide de la fenêtre **Prélèvement entrepôt**.  

Vous pouvez également utiliser la fenêtre **Feuille mouvement** pour déplacer des articles entre emplacements ad hoc, c'est-à-dire sans référence à un document origine. Pour plus d'informations, voir [Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Pour plus d'informations sur le prélèvement d'articles pour des opérations internes dans les entrepôts de base qui sont configurés uniquement pour le prélèvement, voir [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Vous ne pouvez pas créer de toutes pièces un document prélèvement entrepôt car une activité de prélèvement fait toujours partie d'un flux de travail, soit dans un scénario d'extraction, soit dans un scénario de déplacement.  

Vous pouvez créer le document prélèvement entrepôt par déplacement en sélectionnant **Créer prélèvement ent.** dans le document origine, par exemple, un ordre d'assemblage ou une expédition entrepôt lancé. Pour plus d'informations, voir [Prélever des articles avec les prélèvements entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Sinon, vous pouvez créer le document prélèvement entrepôt par extraction à l'aide de la fenêtre **Feuille prélèvement** pour détecter les demandes de prélèvement, à la fois pour l'expédition et les opérations internes, puis créer les documents prélèvement entrepôt requis.  

La procédure suivante explique un scénario d'extraction dans lequel vous prélevez des composants d'un ordre de fabrication lancé via la fenêtre **Feuille prélèvement**. Cette procédure s'applique également pour un ordre d'assemblage.  

Pour créer des demandes de prélèvement dans le cadre de scénarios d'extraction et de déplacement, il faut que les documents origine en question soient lancés. Lancez les documents origine des opérations internes en procédant comme suit.  

|Document origine|Méthode de lancement|  
|---------------------|--------------------|  
|Ordre de fabrication|Remplacez le type commande par un ordre de fabrication lancé.|  
|Ordre d'assemblage|Remplacez le statut actuel par le statut Lancé.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Pour prélever des composants à partir des feuilles prélèvement  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille prélèvement**, puis sélectionnez le lien connexe.  
2.  Choisissez l'action **Extraire documents entrepôt**, puis sélectionnez les lignes composant de l'ordre de fabrication lancé.  
3.  Vérifiez les lignes, triez-les pour assurer un prélèvement optimisé et, si nécessaire, combinez les avec d'autres lignes de la feuille pour utiliser au mieux la disponibilité de l'employé.  
4.  Choisissez l'action **Créer prélèvement**.  
5.  Définissez le mode de création des documents prélèvement entrepôt et la manière de trier les lignes prélèvement en renseignant les champs de la fenêtre **Créer prélèvement** .  
6.  Cliquez sur le bouton **OK**. Les documents prélèvement entrepôt sont créés avec des lignes prélèvement pour chaque composant requis dans l'opération interne.  

Si la zone Opérations internes (par exemple, un atelier de production) est configurée avec un emplacement par défaut pour les composants à utiliser dans l'opération, ce code emplacement est inséré dans les lignes Emplacement qui figurent sur le document prélèvement entrepôt pour indiquer aux magasiniers où placer les articles. Pour plus d'informations, voir le champ **Code empl. des consommations** ou le champ **Code empl. vers assemblage**.

## <a name="filling-the-consumption-bin"></a>Renseigner l'emplacement consommation
Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d'emplacement](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Voir aussi
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

