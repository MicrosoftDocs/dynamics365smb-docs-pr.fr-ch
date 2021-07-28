---
title: Procédure de création d’en-têtes d’ordre de fabrication | Microsoft Docs
description: Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6b13be85c47cc2a280b2cf2e7cf3bf4866633343
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438617"
---
# <a name="create-production-order-headers"></a>Créer des en-têtes O.F.
Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.

Les ordres de fabrication sont généralement créés automatiquement par une fonction de planification pour répondre à une demande connue. Pour plus d’informations, voir [Planification](production-planning.md).   

La procédure suivante s’appuie sur un ordre de fabrication planifié ferme. Vous pouvez aussi créer des ordres de fabrication dotés d’un autre statut.  

## <a name="to-create-a-production-order-header"></a>Pour créer un en-tête O.F.  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.  
2.  Sélectionnez l’action **Nouveau**.  
3.  Dans le champ **N°**, insérez le numéro suivant de la souche.  
4.  Dans le champ **Type origine**, sélectionnez la source de l’ordre de fabrication.

    Vous pouvez choisir de produire une famille d’articles. Pour plus d’informations, voir [Utiliser les familles de production](production-how-work-family.md).
5.  Dans le champ **N° origine**, sélectionnez le numéro d’article, la famille, ou l’en-tête vente pour lequel l’ordre de fabrication doit être créé.  
6.  Renseignez les champs **Quantité** et **Délai** en fonction de vos spécifications.  

Lorsque les exigences de production évoluent, comme les composants ou les opérations, vous pouvez replanifier rapidement l’ordre de fabrication. Pour plus d’informations, voir [Replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]