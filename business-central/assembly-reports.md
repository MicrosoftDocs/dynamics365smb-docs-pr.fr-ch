---
title: États et analyses d’assemblage dans Business Central
description: Découvrez les états et analyses d’assemblage disponibles dans la version standard de Business Central afin que vous puissiez suivre votre activité.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216468"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>États et analyses d’assemblage dans Business Central

Les états d’assemblage dans [!INCLUDE [prod_short](includes/prod_short.md)] permettent aux professionnels de la production et des affaires d’obtenir des informations et des statistiques sur les activités d’assemblage actuelles et passées.  

## <a name="reports"></a>États

Le tableau suivant décrit certains des principaux états dans les états d’assemblage.

|État |ID d’objet|Description  |
|---------|---------|---------|
|**Nomenclatures d’élément d’assemblage**|801|Affiche la liste des nomenclatures : nom, numéro de nomenclature, composants de nomenclature, et toutes autres nomenclatures qui font partie de la nomenclature. Les composants de nomenclature sont définis dans la table Composant nomenclature. Vous verrez également ici l’unité de mesure et la quantité nécessaire de chaque composant par unité de base. |
|**Article – Capable de fabriquer (Temps)**|5871|Indique comment cinq chiffres de disponibilité principaux différents évoluent dans le temps pour un article de nomenclature. Ces chiffres sont modifiés en fonction des événements d’offre et de demande prévus et de l’approvisionnement qui est basé sur les composants disponibles qui peuvent être assemblés ou produits.<br>Vous pouvez utiliser l’état pour vérifier si vous pouvez traiter une commande vente d’un article à une date spécifique, en consultant sa disponibilité actuelle ainsi que les quantités potentielles que ses composants peuvent fournir si un ordre d’assemblage est lancé. L’état indique la date et le nombre d’unités d’un élément d’assemblage et de production que vous pouvez fabriquer, en fonction de la disponibilité des composants et de la disponibilité actuelle de l’article. Cela est affiché en tant que quantité totale.<br>Les informations sont affichées dans un graphique dans lequel chaque chiffre de disponibilité est une ligne qui progresse dans la chronologie et se déplace vers le haut ou vers le bas en fonction des modifications des quantités. Les chiffres de quantité proviennent du même moteur qui fournit des informations dans la fenêtre **Disponibilité article par niveau de nomenclature**. |
|**Distribution coût total nomenclature**|5872|Indique graphiquement la manière dont le coût d’un article assemblé ou produit est distribué dans sa nomenclature.<br>Ces informations peuvent être utiles pour décider de changer de fournisseurs de composants, de remplacer une utilisation interne de capacité par un travail externalisé, ou inversement, ou lors de l’examen et de la modification de la nomenclature d’un article, par exemple.<br>Le premier graphique de l’état affiche le coût unitaire total des composants et des ressources de travail de l’article parent, réparti en cinq parts de coût différentes au maximum et représenté graphiquement par des couleurs différentes.<br>Le graphique en secteurs avec la légende *Par matière/travail* affiche la répartition proportionnelle entre les coûts de matériel et de travail de l’article parent, ainsi que ses propres frais généraux de fabrication. La part du coût matière inclut les coûts matière de l’article. La part du coût de travail inclut la capacité, les frais généraux opératoires et les coûts de sous-traitance. Les parts de coûts sont affichées différemment en fonction des choix indiqués dans le champ **Afficher uniquement**.<br>Le graphique en secteurs étiqueté avec la légende *Par direct/indirect* affiche la répartition proportionnelle entre les coûts directs et indirects de la nomenclature. La part des coûts directs inclut les coûts matière, de capacité et les coûts de sous-traitance de l’article. La part des coûts indirects inclut les frais généraux opératoires et les frais généraux de fabrication.<br>Le tableau en bas de l’état est inclus lorsque vous activez la case à cocher Inclure détails. Il affiche les valeurs sélectionnées dans la fenêtre Coûts totaux nomenclature par mono-niveau ou multi-niveau, en fonction de l’option que vous sélectionnez dans le champ Afficher coût total comme.|
|**Liste des cas d’emploi**|809|Affiche la liste des articles sélectionnés qui composent les nomenclatures. Aperçu utile si vous devez modifier un composant dans une nomenclature insérée dans un élément d’assemblage. Par exemple, si votre fournisseur ne peut plus livrer un article spécifique que vous avez utilisé pour votre assemblage/production. Dans ce type de scénario, cet état vous fournit un aperçu simple des nomenclatures dans lesquelles le composant est inclus. Vous pouvez définir un filtre pour le numéro du composant.|
|**Nomenclature – Matières premières**|810|Cet état peut vous donner un aperçu des composants nécessaires, à la fois pour l’assemblage et pour la production. Vous verrez l’inventaire, l’unité de base, le fournisseur principal si le numéro du fournisseur est écrit dans la fiche article elle-même, et le calcul du délai de réapprovisionnement.|
|**Nomenclature – Produits semi-finis**|811|Si vous produisez et/ou assemblez des produits semi-finis, utilisez cet état pour avoir une vue d’ensemble sur ce type de composant. Cet état vous montre l’unité de base, le stock, les coûts unitaires et un autre numéro d’article. |
|**Nomenclature d’élément d’assemblage – Produits finis**|812|Affiche la liste des articles ou des nomenclatures qui ne sont pas des composants de nomenclature. **Remarque** : Cet état n’est pas limité à la nomenclature uniquement, alors n’oubliez pas de définir le filtre dans le champ **Nomenclature d’élément d’assemblage** ou les champs **Système réapprovisionnement**|
|**Assembler pour commande – Ventes**|915|Affiche les principaux chiffres de vente pour les éléments de composants d’assemblage pouvant être vendus en tant qu’éléments d’assemblage dans les ventes assembler pour commande, ou en tant qu’éléments séparés directement à partir du stock.<br>Utilisez cet état pour analyser la quantité, le coût, les ventes et les chiffres du profit se rapportant aux composants d’assemblage pour prendre des décisions, par exemple pour décider si vous devez modifier le prix d’un kit ou cesser ou commencer à utiliser un élément particulier dans les assemblages.<br>La ligne **Assemblage** affiche les chiffres vente pour la quantité totale vendue en tant qu’élément d’assemblage. Les ventes propres à l’élément d’assemblage totalisant cette somme sont affichées si vous sélectionnez le champ **Afficher détails d’assemblage**.<br>La priorité est donnée aux composants d’assemblage, mais les chiffres sont calculés à partir de la marge bénéficiaire de leur parent, l’élément d’assemblage. Par conséquent, le montant des ventes de chaque composant est calculé à partir de son propre coût et de la marge bénéficiaire de son parent à l’aide de la formule suivante.<br>L’état affiche des informations relatives aux éléments répondant à l’un des critères suivants ou aux deux :<br>- Existe dans la nomenclature d’assemblage d’un élément qui utilise la stratégie d’assemblage Assembler pour commande.<br>- A été vendu dans le cadre d’une vente assembler pour commande.|

## <a name="tasks"></a>Tâches

Les articles suivants décrivent certaines des tâches clés pour analyser l’état de votre entreprise :

* [Voir la disponibilité des articles](inventory-how-availability-overview.md)

## <a name="see-also"></a>Voir aussi

[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser les nomenclatures](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
