---
title: "Configurer les prélèvements et rangements suggérés | Microsoft Docs"
description: "Lorsque vous configurez un entrepôt pour prélèvement et rangement suggérés, vous disposez de nouvelles fonctionnalités pour vous aider à exploiter l'entrepôt le plus efficacement possible."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6c71912f559aa8d1de361a581115ea1eb153cf35
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Configurer des articles et des emplacements pour prélèvement et rangement suggérés
Lorsque vous configurez un entrepôt pour prélèvement et rangement suggérés, vous disposez de nouvelles fonctionnalités pour vous aider à exploiter l'entrepôt le plus efficacement possible. Afin de pouvoir utiliser pleinement cette fonctionnalité, vous devez fournir des informations supplémentaires concernant les articles, permettant ainsi d'exécuter les calculs nécessaires pour suggérer les méthodes les plus efficaces pour gérer les activités de l'entrepôt. Pour plus d'informations, reportez-vous à [Détails de conception : Paramètres entrepôt](design-details-warehouse-setup.md).

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Pour configurer l'article pour prélèvement et rangement suggérés  
1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Ouvrez la fiche de l'article que vous souhaitez configurer pour prélèvement et rangement suggérés.
3. Sur le raccourci **Entrepôt** de la fiche article, renseignez les champs pour définir la façon dont l'article doit être traité dans l'entrepôt.  
4.  Choisissez l'action **Unités de mesure**.
5. Dans la fenêtre **Unités de mesure**, renseignez les champs dans ce formulaire pour définir les différentes unités selon lesquelles l'article peut faire l'objet d'une transaction. Vous devez également remplir dans ce formulaire la hauteur, la largeur, la longueur, le cubage et le poids de l'unité.
6. Choisissez l'action **Contenu emplacement**.
7. Dans la fenêtre **Contenu emplacement**, définissez le magasin et l'emplacement auxquels l'article doit être associé. Le champ **Par défaut** n'est pas utilisé lorsque l'emplacement est configuré pour prélèvement et rangement suggérés.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>Pour activer les fonctionnalités de prélèvement et de rangement suggérés  
Les prélèvement et rangement suggérés permettent d'accéder à des fonctionnalités de configuration entrepôt évoluées qui peuvent améliorer considérablement votre efficacité et la fiabilité de vos données. Pour pouvoir utiliser cette fonctionnalité, vous devez tout d'abord définir divers paramètres dans votre entrepôt.  

Pour utiliser la fonctionnalité prélèvement et rangement suggérés, vous devez l'activer dans la fiche magasin.    
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.  
2.  Sélectionnez le magasin dans lequel vous souhaitez utiliser les prélèvement et rangement suggérés, puis choisissez l'action **Modifier**.  
3.  Sur le raccourci **Entrepôt**, cochez la case **Prélèv. et rangement suggérés**.  

A ce stade de la configuration, il n'est pas nécessaire de renseigner d'autres champs de la fiche magasin.  

> [!NOTE]  
>  Lorsque le magasin possède des écritures comptables article ouvertes, vous ne pouvez pas configurer l'entrepôt pour qu'il utilise des emplacements.  

L'étape suivante consiste à définir le type d'emplacement que vous souhaitez exploiter. Pour plus d'informations, voir [Configurer des types d'emplacement](warehouse-how-to-set-up-bin-types.md). Le type d'emplacement définit la manière d'utiliser un emplacement donné lors du traitement de la circulation des articles dans l'entrepôt. Vous pouvez affecter un type d'emplacement à une zone et à un emplacement.  

Vous pouvez également définir des codes classe entrepôt si l'entrepôt comprend des articles nécessitant différentes conditions de stockage. Les codes classe entrepôt sont utilisés lors de la suggestion du placement des articles dans des emplacements. Vous affectez des codes classe entrepôt à des groupes de produits, qui sont ensuite affectés à des articles et des points de stock, ou à des zones et des emplacements qui prennent en charge les conditions de stockage requises par ces codes classe entrepôt.  

Vous pouvez maintenant configurer des zones, si vous souhaitez en utiliser dans votre entrepôt. L'utilisation de zones réduit le nombre de champs à renseigner lors de la configuration des emplacements, étant donné que les emplacements créés dans une zone héritent de plusieurs propriétés de cette zone. Les zones peuvent également faciliter l'orientation des nouveaux employés ou des intérimaires dans l'entrepôt. Notez que le flux est contrôlé par des emplacements ; vous pouvez donc choisir d'utiliser plusieurs emplacements et une seule zone.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>Pour configurer une zone de l'entrepôt  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.  
2.  Sélectionnez le magasin dans lequel vous souhaitez paramétrer une zone et ouvrez la fiche magasin, puis choisissez l'action **Zones**.  
3.  Dans la fenêtre **Zones**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Lorsque vous modifiez le paramètre d'une zone, tous les emplacements créés par la suite dans cette zone disposent des nouvelles caractéristiques, mais les emplacements d'origine ne sont pas modifiés.  

> [!NOTE]  
>  Si vous ne souhaitez pas utiliser de zones, vous devez néanmoins spécifier un code zone non défini, à l'exception du code.  

L'étape suivante de configuration de l'entrepôt consiste à définir les emplacements. Pour plus d'informations, voir [Comment configurer des magasins de sorte qu'ils utilisent des emplacements](warehouse-how-to-set-up-locations-to-use-bins.md).  

En outre, vous devez créer des modèles et les périodes d'inventaire de rangement. Pour plus d'informations, voir [Configurer des modèles rangement](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

