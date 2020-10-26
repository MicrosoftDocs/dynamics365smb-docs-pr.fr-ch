---
title: Utiliser les nomenclatures pour gérer les composants| Microsoft Docs
description: Vous créez une nomenclature d’assemblage ou une nomenclature de production pour spécifier les composants ou ressources nécessaires pour assembler l’article que la nomenclature représente.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4aa769c8a2b044f434a9643209eecb97f7f51f13
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919403"
---
# <a name="work-with-bills-of-material"></a>Utiliser les nomenclatures
Les nomenclatures d’assemblage permettent de structurer les articles parents qui doivent être assemblés ou produits par des ressources ou des postes de charge à partir des composants. Une nomenclature d’assemblage peut également être utilisée pour vendre un article parent sous la forme d’un kit constitué de ses composants.

## <a name="assembly-boms-or-production-boms"></a>Nomenclatures d’assemblage ou nomenclatures de production
Vous utilisez des ordres d’assemblage pour fabriquer des produits finis à partir de composants dans le cadre d’un processus simple qui peut être exécuté par une ou plusieurs ressources de base, qui ne sont pas des postes ou centres de charge, ou sans ressource. Par exemple, un processus d’assemblage peut consister à prélever deux bouteilles de vin et un sachet de café puis à les emballer comme article de cadeau.  

Une nomenclature d’assemblage contient les données de base qui définissent les composants d’un produit fini assemblé, ainsi que les ressources utilisées pour assembler l’élément d’assemblage. Lorsque vous entrez un élément d’assemblage et une quantité dans l’en-tête d’un nouvel ordre d’assemblage, les lignes d’ordre d’assemblage sont renseignées automatiquement d’après la nomenclature d’assemblage, avec une ligne d’ordre d’assemblage par composant ou ressource. Pour plus d’informations, voir [Gestion des assemblages](assembly-assemble-items.md).

Les nomenclatures d’assemblage sont décrites dans cette rubrique.

Vous utilisez des ordres de fabrication pour fabriquer des produits finis à partir de composants dans le cadre d’un processus complexe nécessitant une gamme de fabrication et des centres ou postes de charge, qui représentent les capacités de production. Par exemple, un processus de production peut être établi pour découper des plaques d’acier en une opération, les souder lors de l’opération suivante et peindre le produit fini lors de la dernière opération. Pour plus d’informations, voir [Production](production-manage-manufacturing.md).  

Une nomenclature de production contient les données de base qui définissent un article de production et ses composants. Pour les éléments d’assemblage, la nomenclature de production doit être validée et affectée à l’article de production avant de pouvoir être utilisée dans un ordre de fabrication. Lorsque vous entrez l’article produit dans une ligne O.F., manuellement ou en actualisant la commande, le contenu de la nomenclature de production devient les composants O.F. Pour plus d’informations, reportez-vous à [Créer des nomenclatures de production](production-how-to-create-production-boms.md).  

Le concept de ressources est beaucoup plus avancé dans la production que dans la gestion nomenclature d’assemblage. Les centres de charge et les postes de charge fonctionnent comme des ressources, et les étapes de production sont représentées par les opérations qui sont affectées à ces ressources dans des gammes de production. Pour plus d’informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).

Les ordres d’assemblage et les ordres de fabrication peuvent être liés directement aux commandes vente. Cependant, vous pouvez uniquement utiliser des ordres d’assemblage pour personnaliser le produit fini directement par rapport à la demande d’un client via la commande vente.

## <a name="to-create-an-assembly-bom"></a>Pour créer une nomenclature d’assemblage
Pour définir un article parent constitué d’autres articles, et potentiellement des ressources nécessaires pour regrouper les articles parents, vous devez créer une nomenclature d’assemblage.  

Les nomenclatures d’assemblage contiennent généralement des articles mais peuvent également contenir une ou plusieurs ressources requises pour regrouper les articles d’assemblage.

Les nomenclatures d’assemblage peuvent être multi-niveaux, ce qui signifie qu’un composant de la nomenclature d’assemblage peut être un élément d’assemblage proprement dit. Dans ce cas, le champ **Nomencl d’élément d’assemblage** de la ligne nomenclature d’assemblage contient **Oui** .

Des exigences spécifiques s’appliquent aux articles des nomenclatures d’assemblage en ce qui concerne la disponibilité. Pour plus d’informations, voir [Pour afficher la disponibilité d’un article en fonction de son utilisation dans les nomenclatures d’assemblage](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Il y a deux parties pour créer une nomenclature d’assemblage :
- Configuration d’un nouvel article
- Définition de la structure de la nomenclature de l’article d’assemblage.

1. Configurez un nouvel article. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

    Entrez maintenant les composants ou les ressources de la nomenclature d’assemblage.  
2. Sur la page **Fiche article** d’un article d’assemblage, sélectionnez l’action **Assemblage** , puis l’action **Nomencl d’élément d’assemblage** .
3. Renseignez les champs nécessaires sur la page **Nomenclature d’élément d’assemblage** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-edit-assembly-boms"></a>Pour modifier les nomenclatures d’assemblage
Vous pouvez modifier les lignes d’une nomenclature d’assemblage à tout moment. Mais sachez que la nomenclature peut être utilisée sur les ventes en cours ou les assemblages du parent, qui peuvent être affectés par le changement. Sélectionnez l’action **Cas d’emploi** pour voir dans quels articles elle est utilisée et si les ordres d’assemblage ou de vente peuvent être affectés.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles** , puis sélectionnez le lien associé.
2. Sélectionnez **Oui** dans la colonne **Nomenclature d’assemblage** .
3. Sur la page **Nomenclature d’assemblage** , sélectionnez l’action **Modifier la liste** , puis modifiez n’importe quel champ selon vos besoins.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Pour afficher les composants et les ressources indentés selon la structure de la nomenclature
Sur la page **Nomenclature d’élément d’assemblage** , vous pouvez ouvrir une page distincte qui affiche les composants et les ressources indentés selon la position de leur nomenclature sous l’article d’assemblage.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles** , puis sélectionnez le lien associé.
2. Ouvrez la fiche d’un article d’assemblage. (Le champ **Nomenclature d’élément d’assemblage** sur la page **Articles** contient **Oui** .)
3. Sur la page **Fiche article** , sélectionnez l’action **Assemblage** , puis l’action **Nomenclature d’élément d’assemblage** .
4. Sur la page **Nomenclature d’élément d’assemblage** , sélectionnez l’action **Afficher nomenclature** .

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Pour remplacer l’article d’assemblage par ses composants dans les lignes document
Dans n’importe quel document vente et achat qui contient un élément d’assemblage, vous pouvez utiliser une fonction spéciale pour remplacer la ligne de l’élément d’assemblage par de nouvelles lignes pour ses composants. Cette option est utile, par exemple, si vous souhaitez vendre des composants sous forme de kit représentant l’élément d’assemblage.

La fonction Éclater nomenclature est également disponible sur la page **Nomenclature d’élément d’assemblage** en tant que méthode pour afficher les éléments enfants de tous les sous-assemblages d’une nomenclature d’élément d’assemblage.

> [!CAUTION]  
>  Lorsque vous avez utilisé la fonction **Éclater nomenclature** , vous ne pouvez pas facilement l’annuler. Vous devez supprimer les lignes commande vente représentant les composants puis réentrer une ligne commande vente de l’élément d’assemblage.

La procédure suivante se base sur une facture vente. Les mêmes étapes s’appliquent à d’autres documents vente et à tous les documents achat.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente** , puis sélectionnez le lien associé.
2. Ouvrez une facture vente qui contient une ligne pour un élément d’assemblage.
3. Sélectionnez la ligne pour un élément d’assemblage, puis la ligne d’action **Éclater nomenclature** .

Tous les champs de la ligne facture vente pour l’élément d’assemblage sont désactivés sauf les champs **Article** et **Description** . Les lignes facture vente renseignées sont insérées pour les composants et les éventuelles ressources qui composent l’élément d’assemblage.

> [!NOTE]
> Le rapport **Liste de prélèvement par ordre** est également modifié pour afficher uniquement les composants. Cela signifie qu’un magasinier qui choisit l’article parent, l’élément d’assemblage, ne le verra pas dans la liste de prélèvement. Pour plus d’informations, voir [Imprimer la liste de prélèvement](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Pour calculer le coût standard d’un élément d’assemblage
Vous calculez le coût unitaire d’un élément d’assemblage en regroupant le coût unitaire de chaque composant et ressource dans la nomenclature d’assemblage de l’article.

Vous pouvez également calculer et mettre à jour le coût standard pour un ou plusieurs articles sur la page **Feuille coût standard** . Pour plus d’informations, voir [Mise à jour des coûts standard](finance-how-to-update-standard-costs.md).  

Le coût unitaire d’une nomenclature d’assemblage équivaut toujours au total des coûts unitaires de ses composants, y compris ceux d’autres nomenclatures d’assemblage, et des ressources.

1. Dans le coin supérieur droit, sélectionnez l’icône **Page ou état pour la recherche** , entrez **Articles** , puis sélectionnez le lien connexe.
2. Ouvrez la fiche d’un article d’assemblage. (Le champ **Nomenclature d’élément d’assemblage** sur la page **Articles** contient **Oui** .)
3. Sur la page **Fiche article** , sélectionnez l’action **Assemblage** , puis l’action **Nomenclature d’élément d’assemblage** .
4. Sur la page **Nomenclature d’élément d’assemblage** , sélectionnez l’action **Calculer coût standard** .
5. Sélectionnez l’une des options suivantes, puis choisissez le bouton **OK** .

|Option |Désignation |
|-------|------------|
|**Niveau supérieur**|Calcule le coût standard de l’élément d’assemblage en tant que coût total de tous les articles achetés ou assemblés de cette nomenclature d’assemblage sans tenir compte de toutes les nomenclatures d’assemblage sous-jacentes.|
|**Tous niveaux**|Calcule le coût standard de l’élément d’assemblage comme la somme des éléments suivants : 1) Coût calculé de toutes les nomenclatures d’assemblage sous-jacentes dans la nomenclature d’assemblage. 2) Coût de tous les articles achetés dans la nomenclature d’assemblage.|



Les coûts des articles constituant la nomenclature d’assemblage sont copiés à partir des fiches article du composant. Le coût de chaque article est multiplié par sa quantité, et le coût total est affiché dans le champ **Coût unitaire** sur la fiche article.

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Voir la disponibilité des articles](inventory-how-availability-overview.md)     
[Stock](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
