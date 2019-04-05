---
title: Procédure de création d'en-têtes d'ordre de fabrication | Microsoft Docs
description: Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 13d699dbeb8fe2c3979a7b6bd330b14f077d2d3c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820482"
---
# <a name="create-production-order-headers"></a>Créer des en-têtes O.F.
Vous pouvez créer manuellement un ordre de fabrication. Pour cela, la première étape est de créer un en-tête O.F.

Les ordres de fabrication sont généralement créés automatiquement par une fonction de planification pour répondre à une demande connue. Pour plus d'informations, voir [Planification](production-planning.md).   

La procédure suivante s'appuie sur un ordre de fabrication planifié ferme. Vous pouvez aussi créer des ordres de fabrication dotés d'un autre statut.  

## <a name="to-create-a-production-order-header"></a>Pour créer un en-tête O.F.  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **O.F. planifiés fermes**, puis sélectionnez le lien associé.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Dans le champ **N°**, insérez le numéro suivant de la souche.  
4.  Dans le champ **Type origine**, sélectionnez la source de l'ordre de fabrication.

    Vous pouvez choisir de produire une famille d'articles. Pour plus d'informations, voir [Utiliser les familles de production](production-how-work-family.md).
5.  Dans le champ **N° origine**, sélectionnez le numéro d'article, la famille, ou l'en-tête vente pour lequel l'ordre de fabrication doit être créé.  
6.  Renseignez les champs **Quantité** et **Délai** en fonction de vos spécifications.  

Lorsque les exigences de production évoluent, comme les composants ou les opérations, vous pouvez replanifier rapidement l'ordre de fabrication. Pour plus d'informations, voir [Replanifier ou actualiser directement des ordres de fabrication](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
