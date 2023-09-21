---
title: Utiliser les familles de production dans la fabrication
description: 'Lorsque vous personnalisez un calendrier principal pour votre société ou pour l’un de ses partenaires commerciaux, votre tâche consiste essentiellement à modifier le statut des jours ouvrés et chômés.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000790, 99000791, 99000792, 99000793'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="work-with-production-families"></a>Utiliser les familles de production

Une famille de production est un groupe d’articles distincts dont la relation repose sur la similitude de leur processus de fabrication. Si vous formez des familles de production, certains articles peuvent être fabriqués plusieurs fois au cours d’une production, ce qui optimise la consommation de matière.

Dans le champ **Quantité** de la page **Famille**, entrez la quantité à produire lorsque l’ensemble de la famille a été fabriquée une fois.

## <a name="example"></a>Exemple :

Dans les processus de découpe, quatre pièces du même article et dix pièces d’un autre peuvent être fabriquées simultanément à partir d’une plaque. La machine à découpe découpe les 14 pièces en une seule fois.

Le regroupement d’éléments en familles de production permet de réduire la quantité perte car ce qui devrait normalement constituer un rebut définitif, lors de la fabrication de grosses pièces, est utilisé pour fabriquer de petits articles.

## <a name="to-set-up-a-production-family"></a>Pour configurer une famille de production

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Familles**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Pour produire selon une famille de production

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.
2. Créez un ordre de fabrication. Pour plus d’informations, voir [Créer des ordres de fabrication](production-how-to-create-production-orders.md).
3. Dans le champ **Type origine**, sélectionnez **Famille**.  
4. Dans le champ **N° origine**, sélectionnez la famille de production appropriée.

## <a name="see-also"></a>Voir aussi

[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)
[Planification](production-planning.md)   
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
