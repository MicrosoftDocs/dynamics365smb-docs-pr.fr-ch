---
title: Utiliser les nomenclatures
description: Vous créez une nomenclature d’assemblage ou une nomenclature de production pour spécifier les composants ou ressources nécessaires pour assembler l’article que la nomenclature représente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 09/26/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Utiliser les nomenclatures

Les nomenclatures d’assemblage permettent de structurer les articles parents qui doivent être assemblés à partir d’autres articles ou produits par des ressources ou des postes de charge à partir des composants.

## Nomenclatures d’assemblage ou nomenclatures de production

[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge deux types différents de nomenclatures :

| Type de nomenclature | Catégorie générale | Exemple : |
| -------- | ---------------- | ------- |
| [Nomenclatures d’élément d’assemblage](assembly-how-work-assembly-boms.md) | Entrepôt / assemblage | Objets constitués d’autres objets, assemblés avec des ressources de base ou sans ressources. |
| [Nomenclatures de production](production-how-to-create-production-boms.md) | Fabrication / production | Articles constitués de différents composants et sous-ensembles, produits au travail ou dans un poste de charge. |

Vous utilisez des ordres d’assemblage pour fabriquer des produits finis à partir de composants dans le cadre d’un processus simple qui peut être exécuté par une ou plusieurs ressources de base, qui ne sont pas des postes ou centres de charge, ou sans ressource. Par exemple, un processus d’assemblage peut consister à prélever deux bouteilles de vin et un sachet de café puis à les emballer comme article de cadeau.  

Une nomenclature d’assemblage contient les données de base qui définissent les composants d’un produit fini assemblé, ainsi que les ressources utilisées pour assembler l’élément d’assemblage. Lorsque vous entrez un élément d’assemblage et une quantité dans l’en-tête d’un nouvel ordre d’assemblage, les lignes d’ordre d’assemblage sont renseignées automatiquement d’après la nomenclature d’assemblage, avec une ligne d’ordre d’assemblage par composant ou ressource. En savoir plus sur [Gestion des assemblages](assembly-assemble-items.md).

Vous utilisez des ordres de fabrication pour fabriquer des produits finis à partir de composants dans le cadre d’un processus complexe nécessitant une gamme de fabrication et des centres ou postes de charge, qui représentent les capacités de production. Par exemple, un processus de production peut être établi pour découper des plaques d’acier en une opération, les souder lors de l’opération suivante et peindre le produit fini lors de la dernière opération. En savoir plus sur [Fabrication](production-manage-manufacturing.md).

Une nomenclature de production contient les données de base qui définissent un article de production et ses composants. Pour les éléments d’assemblage, la nomenclature de production doit être validée et affectée à l’article de production avant de pouvoir être utilisée dans un ordre de fabrication. Lorsque vous entrez l’article produit dans une ligne O.F., manuellement ou en actualisant la commande, le contenu de la nomenclature de production devient les composants O.F. En savoir plus sur [Créer des nomenclatures de production](production-how-to-create-production-boms.md).

Le concept de ressources est beaucoup plus avancé dans la production que dans la gestion nomenclature d’assemblage. Les centres de charge et les postes de charge fonctionnent comme des ressources, et les étapes de production sont représentées par les opérations qui sont affectées à ces ressources dans des gammes de production. En savoir plus sur l’article [Créer des gammes](production-how-to-create-routings.md).

Les ordres d’assemblage et les ordres de fabrication peuvent être liés directement aux commandes vente. Cependant, vous pouvez uniquement utiliser des ordres d’assemblage pour personnaliser le produit fini directement par rapport à la demande d’un client via la commande vente.

## Voir aussi

[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Gérer les variantes de produits](inventory-item-variants.md)  
[Stock](inventory-manage-inventory.md)  
[Production](production-manage-manufacturing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
