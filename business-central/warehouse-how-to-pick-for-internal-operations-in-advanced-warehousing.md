---
title: Prélever pour des opérations internes dans les configurations de stockage avancées
description: Si vos sites utilisent le prélèvement et l’expédition, choisissez des composants pour les activités de production, d’assemblage et les tâches dans la page Sélection d’entrepôt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607570"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Prélever pour la fabrication, l’assemblage ou les tâches dans les configurations de stockage avancées

Dans les configurations de stockage avancées, dans lequel le magasin est configuré pour utiliser le prélèvement ainsi que l’expédition, vous pouvez prélever des composants pour les activités de fabrication et d’assemblage à l’aide de la page **Prélèvement entrepôt**.  

Vous pouvez également utiliser la page **Feuille mouvement** pour déplacer spontanément des articles entre emplacements, c’est-à-dire sans référence à un document origine. Pour plus d’informations, voir [Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Pour plus d’informations sur le prélèvement d’articles dans les entrepôts de base qui sont configurés uniquement pour le prélèvement, voir [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> Vous ne pouvez pas créer de toutes pièces un document prélèvement entrepôt, car une activité de prélèvement fait toujours partie d’un flux de travail, soit dans un scénario d’extraction, soit dans un scénario de déplacement.  

Vous pouvez créer le document prélèvement entrepôt par déplacement en sélectionnant **Créer prélèvement ent.** dans le document origine, par exemple, un ordre d’assemblage ou une expédition entrepôt lancé. Pour plus d’informations, voir [Prélever des articles avec les prélèvements entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Vous pouvez également créer un document de prélèvement entrepôt en mode pull en utilisant la page **Feuille prélèvement** pour détecter les demandes de prélèvement. Cette méthode est utile pour l’expédition et les opérations internes. Vous pouvez ensuite créer les documents de prélèvement magasin requis.  

La procédure suivante explique un scénario d’extraction dans lequel vous prélevez des composants d’un ordre de fabrication lancé via la page **Feuille prélèvement**. Cette procédure s’applique également pour un ordre d’assemblage.  

Pour créer des demandes de prélèvement dans le cadre de scénarios d’extraction et de déplacement, il faut que les documents origine en question soient lancés. Lancez les documents origine des opérations internes en procédant comme suit.  

|Document origine|Méthode de lancement|  
|---------------------|--------------------|  
|Ordre de fabrication|Remplacez le type commande par un ordre de fabrication lancé.|  
|Ordre d’assemblage|Remplacez le statut actuel par le statut Lancé.|
|Projets | Remplacez le statut actuel par le statut En cours.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Pour prélever des composants à partir des feuilles prélèvement

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille prélèvement**, puis choisissez le lien associé.  
2. Choisissez l’action **Extraire documents entrepôt**, puis sélectionnez les lignes composant de l’ordre de fabrication lancé.  
3. Triez les lignes pour assurer un prélèvement efficace. Vous voudrez peut-être combiner les lignes pour faire gagner du temps aux employés.  
4. Choisissez l’action **Créer prélèvement**.  
5. Définissez le mode de création des documents prélèvement entrepôt et la manière de trier les lignes prélèvement en renseignant les champs de la page **Créer prélèvement** .  
6. Choisissez le bouton **OK**. Les documents prélèvement entrepôt sont créés avec des lignes prélèvement pour chaque composant requis dans l’opération interne.  

Les zones d’exploitation telles que les ateliers de production peuvent avoir un emplacement par défaut pour les composants dont ils ont besoin. Si c’est le cas, le code emplacement par défaut est ajouté au document prélèvement entrepôt pour indiquer où placer les articles. Pour plus d’informations, voir les info-bulles pour les champs **Code empl. des consommations** ou le champ **Code empl. vers assemblage**.

## <a name="filling-the-consumption-bin"></a>Renseigner l’emplacement consommation

Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d’emplacement.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/pick-ship-items-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
