---
title: Prélever pour des opérations internes dans les configurations de stockage avancées
description: Si vos sites utilisent le prélèvement et l’expédition, choisissez des composants pour les activités de production et d’assemblage dans la page Sélection d’entrepôt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d0e7db8e4aeade9865114769c659075971dd3c8d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518642"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Prélever pour la fabrication ou l’assemblage dans les configurations de stockage avancées.
Dans les configurations de stockage avancées, dans lequel le magasin est configuré pour utiliser le prélèvement ainsi que l’expédition, vous pouvez prélever des composants pour les activités de fabrication et d’assemblage à l’aide de la page **Prélèvement entrepôt**.  

Vous pouvez également utiliser la page **Feuille mouvement** pour déplacer des articles entre emplacements ad hoc, c’est-à-dire sans référence à un document origine. Pour plus d’informations, voir [Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Pour plus d’informations sur le prélèvement d’articles pour des opérations internes dans les entrepôts de base qui sont configurés uniquement pour le prélèvement, voir [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Vous ne pouvez pas créer de toutes pièces un document prélèvement entrepôt car une activité de prélèvement fait toujours partie d’un flux de travail, soit dans un scénario d’extraction, soit dans un scénario de déplacement.  

Vous pouvez créer le document prélèvement entrepôt par déplacement en sélectionnant **Créer prélèvement ent.** dans le document origine, par exemple, un ordre d’assemblage ou une expédition entrepôt lancé. Pour plus d’informations, voir [Prélever des articles avec les prélèvements entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Sinon, vous pouvez créer le document prélèvement entrepôt par extraction à l’aide de la page **Feuille prélèvement** pour détecter les demandes de prélèvement, à la fois pour l’expédition et les opérations internes, puis créer les documents prélèvement entrepôt requis.  

La procédure suivante explique un scénario d’extraction dans lequel vous prélevez des composants d’un ordre de fabrication lancé via la page **Feuille prélèvement**. Cette procédure s’applique également pour un ordre d’assemblage.  

Pour créer des demandes de prélèvement dans le cadre de scénarios d’extraction et de déplacement, il faut que les documents origine en question soient lancés. Lancez les documents origine des opérations internes en procédant comme suit.  

|Document origine|Méthode de lancement|  
|---------------------|--------------------|  
|Ordre de fabrication|Remplacez le type commande par un ordre de fabrication lancé.|  
|Ordre d’assemblage|Remplacez le statut actuel par le statut Lancé.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Pour prélever des composants à partir des feuilles prélèvement  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille prélèvement**, puis choisissez le lien associé.  
2.  Choisissez l’action **Extraire documents entrepôt**, puis sélectionnez les lignes composant de l’ordre de fabrication lancé.  
3.  Vérifiez les lignes, triez-les pour assurer un prélèvement optimisé et, si nécessaire, combinez les avec d’autres lignes de la feuille pour utiliser au mieux la disponibilité de l’employé.  
4.  Choisissez l’action **Créer prélèvement**.  
5.  Définissez le mode de création des documents prélèvement entrepôt et la manière de trier les lignes prélèvement en renseignant les champs de la page **Créer prélèvement** .  
6.  Choisissez le bouton **OK**. Les documents prélèvement entrepôt sont créés avec des lignes prélèvement pour chaque composant requis dans l’opération interne.  

Si la zone Opérations internes (par exemple, un atelier de production) est configurée avec un emplacement par défaut pour les composants à utiliser dans l’opération, ce code emplacement est inséré dans les lignes Emplacement qui figurent sur le document prélèvement entrepôt pour indiquer aux magasiniers où placer les articles. Pour plus d’informations, voir le champ **Code empl. des consommations** ou le champ **Code empl. vers assemblage**.

## <a name="filling-the-consumption-bin"></a>Renseigner l’emplacement consommation
Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d’emplacement.](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Voir aussi
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de Warehouse Management](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]