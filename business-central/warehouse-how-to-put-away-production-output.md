---
title: Ranger la production
description: Cet article décrit comment ranger la sortie de la production.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Rangement du résultat de fabrication ou d’assemblage

Le mode de rangement de la production dépend du mode de configuration de l’entrepôt en tant qu’emplacement. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

Dans les configurations de stockage de base où l’emplacement appelle un traitement de rangement, vous utilisez le document **Rangement stock** pour valider la production et enregistrer son rangement.  

> [!NOTE]  
> Les processus d’assemblage ne prennent pas en charge le rangement de stock. Vous publiez un ordre d’assemblage pour enregistrer le résultat. Si vous utilisez des emplacements, vous pouvez déplacer des éléments d’un emplacement à un autre ultérieurement. Learn more at [Déplacement des articles ad hoc dans les configurations entrepôt de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Dans les configurations de stockage avancées où un magasin nécessite un traitement à la fois de rangement et de réception, vous pouvez créer soit un document rangement interne soit un document mouvement pour ranger la production.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Pour ranger la production avec un rangement stock

La première étape du rangement de la production consiste à créer la demande enlogement entrante. Cette demande indique à l’entrepôt que la production de l’O.F ou de l’assemblage est prête à être rangée.

### <a name="to-create-the-inbound-warehouse-request"></a>Pour créer la demande d’enlogement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. lancé**, puis sélectionnez le lien associé.  
2. Choisissez l’ordre de fabrication qui est prêt pour rangement, puis choisissez l’action **Créer demande d’enlogement**.  

> [!NOTE]  
> Vous pouvez également créer la demande d’enlogement entrepôt en choisissant le champ **Créer demande d’enlogement** lors de l’actualisation de l’ordre de fabrication. Learn more at [Actualiser ou replanifier des ordres de fabrication](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Pour ranger la production avec un rangement stock

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangement stock**, puis choisissez le lien associé.  
2. Créez un rangement stock. Learn more at [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Pour accéder aux composants de la production de l’O.F., choisissez l’action **Extraire documents origine**, puis sélectionnez l’ordre de fabrication lancé.  
4. Renseignez les lignes rangement en fonction des besoins.
5. Lorsque les lignes sont prêtes à être validées, choisissez l’action **Valider**. Les écritures entrepôt nécessaires sont alors créées et la production des articles est validée.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Vous pouvez également créer un **rangement stock** directement à partir de l’ordre de fabrication de lancé. Learn more at [Ranger des articles avec le rangement stock](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Lorsque vous validez un rangement stock, il est supposé que toutes les opérations sont validées selon la gamme standard. C’est-à-dire que la quantité produite est validée conformément à la dernière opération. Vous pouvez utiliser la feuille production pour valider les écarts de quantité produite et les temps d’exécution et de préparation. Si vous devez effectuer une validation partielle après la création d’un rangement stock, vous pouvez le faire au niveau des temps de préparation et des quantités pour toutes les opérations, à l’exception de la dernière. La dernière opération est contrôlée par le rangement stock.  

Si vous devez juste valider le temps d’exécution ou de préparation de la dernière opération, définissez la quantité produite de la dernière opération sur 0. Vous pouvez également choisir de ne pas valider la dernière ligne en la supprimant.

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Pour ranger l’assemblage et la production dans les configurations de stockage avancées

Lorsque vous validez l’ordre de fabrication ou d’assemblage dans un entrepôt qui utilise le prélèvement et le rangement dirigés, la production est placée dans l’emplacement défini dans l’ordre de fabrication ou d’assemblage. Pour en savoir plus sur les différentes manières de déplacer des articles dans l’entrepôt avec des configurations avancées, consultez [Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Vous ne pouvez pas saisir le numéro document origine, tel que le numéro d’ordre de fabrication, dans les documents de rangement interne, rangement ou mouvement pour les processus de sortie de la production ou de l’assemblage.  

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
