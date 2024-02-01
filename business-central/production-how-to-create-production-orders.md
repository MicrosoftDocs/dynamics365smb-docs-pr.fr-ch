---
title: Créer des en-têtes O.F.
description: 'Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '9325, 99000815, 99000829, 9900083'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-production-order-headers"></a>Créer des en-têtes O.F.

Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.

Les ordres de fabrication sont généralement créés automatiquement par une fonction de planification pour répondre à une demande connue. Pour plus d’informations, voir [Planification](production-planning.md).  

La procédure suivante s’appuie sur un ordre de fabrication planifié ferme. Vous pouvez aussi créer des ordres de fabrication dotés d’un autre statut.  

## <a name="to-create-a-production-order-header"></a>Pour créer un en-tête O.F.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **N°**, insérez le numéro suivant de la souche.  
4. Dans le champ **Type origine**, sélectionnez la source de l’ordre de fabrication.

    Vous pouvez choisir de produire une famille d’articles. Pour plus d’informations, voir [Utiliser les familles de production](production-how-work-family.md).
5. Dans le champ **N° origine**, sélectionnez le numéro d’article, la famille, ou l’en-tête vente pour lequel l’ordre de fabrication doit être créé.  
6. Renseignez les champs **Quantité** et **Délai** en fonction de vos spécifications.  

Lorsque les exigences de production évoluent, comme les composants ou les opérations, vous pouvez replanifier rapidement l’ordre de fabrication. Pour plus d’informations, voir [Replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md).  

## <a name="see-also"></a>Voir aussi

[Production](production-manage-manufacturing.md)
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
