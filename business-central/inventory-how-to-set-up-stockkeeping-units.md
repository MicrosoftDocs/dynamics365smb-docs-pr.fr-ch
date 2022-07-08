---
title: Comment configurer des points de stock
description: Vous pouvez utiliser des points de stock pour enregistrer des informations relatives à vos articles pour un code magasin ou variante donné.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5704, 5700, 5702, 5701
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5271203a9936f268e23df9b8e38a2373d875e5f9
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076502"
---
# <a name="set-up-stockkeeping-units"></a>Configurer des points de stock

Vous pouvez utiliser des points de stock pour enregistrer des informations relatives aux articles pour un code magasin ou variante.  

Les points de stock représentent un supplément des fiches article. Ils ne les remplacent pas, bien qu’ils soient liés à ces documents. Les points de stock vous permettent de différencier des informations relatives à un article pour un magasin donné, comme un entrepôt ou un centre de distribution, ou une variante donnée, comme plusieurs numéros d’étagère et plusieurs informations de réapprovisionnement, pour un même article.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Pour configurer un point de stock  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de stock**, puis choisissez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Renseignez les champs de la fiche. Les champs suivants sont nécessaires : **N° article**, **Code magasin** et/ou **Code variante**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Après avoir configuré le premier point de stock pour un article, la case à cocher **Point de stock** sur la fiche **Article** est activée.  

Pour créer plusieurs points de stock pour un article, utilisez le traitement par lots **Créer point de stock**.  

> [!NOTE]  
>  Les informations de la fiche **Point de stock** sont prioritaires par rapport à celles de la fiche **Article**.

> [!Warning]
> Si le point de stock est expédié à la fabrication, le champ **Coût standard** n’est pas utilisé lors de la facturation et de l’ajustement du coût réel de l’article fabriqué. Celui utilisé est plutôt le champ **Coût standard** de la fiche article sous-jacente. En outre, tous les écarts sont calculés par rapport aux coûts totaux de l’article.<br /><br />
> Étant donné qu’il n’est pas possible d’affecter les nomenclatures de production et la gamme aux points de stock, le calcul du coût unitaire et le calcul lié des coûts totaux ne sont également pas disponibles sur les points de stock. Pour plus d’informations, voir [À propos du calcul des coûts standard](finance-about-calculating-standard-cost.md)

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/control-inventory-multiple-locations/)

## <a name="see-also"></a>Voir aussi

[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]