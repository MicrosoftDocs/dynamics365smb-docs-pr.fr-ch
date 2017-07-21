---
title: "Utiliser les nomenclatures pour gérer les composants| Microsoft Docs"
description: "Vous créez une nomenclature d'assemblage pour spécifier les composants ou ressources nécessaires pour monter l'article que la nomenclature d'assemblage représente, et vous pouvez afficher les composants d'un élément d'assemblage."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-bills-of-material"></a>Procédure : utiliser les nomenclatures
> [!NOTE]  
>   La version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] contient uniquement la première partie de la fonction Gestion des assemblages. Pour le moment, vous pouvez uniquement créer des nomenclatures d'assemblage et gérer les articles parents associés comme des articles en stock normaux. Dans une mise à jour future, vous pourrez gérer l'assemblage réel des articles à partir des composants, dans les flux Assembler pour stock ou Assembler pour commande, et vous pourrez vendre des composants comme kits.

Les nomenclatures permettent de structurer les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock.

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une nomenclature est appelée une « nomenclature d'assemblage ». Les nomenclatures d'assemblage spécifient les composants contenus dans les articles parents. Dans cette documentation, un article parent est appelé un « article d'assemblage ».

Les nomenclatures d'assemblage contiennent généralement des articles mais peuvent également contenir une ou plusieurs ressources requises pour regrouper les articles d'assemblage.

Les nomenclatures d'assemblage peuvent être multi-niveaux, ce qui signifie qu'un composant de la nomenclature d'assemblage peut être un élément d'assemblage proprement dit. Dans ce cas, le champ **Nomencl d'élément d'assemblage** de la ligne nomenclature d'assemblage contient **Oui**.

Des exigences spécifiques s'appliquent aux articles des nomenclatures d'assemblage en ce qui concerne la disponibilité. Pour plus d'informations, reportez-vous à la section « Pour afficher la disponibilité d'un article en fonction de son utilisation dans les nomenclatures d'assemblage » dans [Procédure : voir la disponibilité des articles](inventory-how-availability-overview.md).

> [!NOTE]  
>   Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**. Pour plus d'informations, voir [Personnalisation de votre expérience Financials](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Pour créer une nomenclature d'assemblage
Pour définir un article parent constitué d'autres articles, et potentiellement des ressources nécessaires pour regrouper les articles parents, vous devez créer une nomenclature d'assemblage.  

Il y a deux parties pour créer une nomenclature d'assemblage :
- Configuration d'un nouvel article
- Définition de la structure de la nomenclature de l'article d'assemblage.

1. Configurez un nouvel article. Pour plus d'informations, reportez vous à [Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md).

    Entrez maintenant les composants ou les ressources de la nomenclature d'assemblage.  
2. Dans la fenêtre **Fiche article** d'un article d'assemblage, sélectionnez l'action **Assemblage**, puis l'action **Nomencl d'élément d'assemblage**.
3. Dans la fenêtre **Nomencl d'élément d'assemblage**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Pour afficher les composants d'un article d'assemblage indenté selon la structure de la nomenclature
Dans la fenêtre **Nomencl d'élément d'assemblage**, vous pouvez ouvrir une fenêtre distincte qui affiche les composants et les ressources indentés selon la position de leur nomenclature sous l'article d'assemblage.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un article d'assemblage. (Le champ **Nomencl d'élément d'assemblage** dans la fenêtre **Articles** contient **Oui**.)
3. Dans la fenêtre **Fiche article**, sélectionnez l'action **Assemblage**, puis l'action **Nomencl d'élément d'assemblage**.
4. Dans la fenêtre **Nomencl d'élément d'assemblage**, sélectionnez l'action **Afficher nomenclature**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Pour acheter, vendre ou transférer des articles d'assemblage
Comme la version actuelle de [!INCLUDE[d365fin](includes/d365fin_md.md)] permet uniquement de définir et d'affecter des nomenclatures d'assemblage aux articles, vous pouvez gérer les articles d'assemblage des lignes document comme des articles normaux uniquement.

**Attention** : la quantité en stock des composants de nomenclature ne sera pas ajustée dans ce cas.

## <a name="see-also"></a>Voir aussi
[Procédure : enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Procédure : voir la disponibilité des articles](inventory-how-availability-overview.md)     
[Stock](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

