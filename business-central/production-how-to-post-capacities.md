---
title: 'Procédure : valider les capacités'
description: Validez les capacités consommées qui ne sont pas affectées à l’ordre de fabrication dans la feuille capacité et affichez les capacités validées sur la page des écritures comptables des capacités.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 024985cb4a2615f374465e5a387901976509a5db
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444220"
---
# <a name="post-capacities"></a>Valider les capacités
La feuille capacité vous permet de valider les capacités consommées qui ne sont pas affectées à l’ordre de fabrication. Par exemple, les travaux de maintenance doivent être affectés à une capacité, mais non à un ordre de fabrication.  

## <a name="to-post-capacities"></a>Pour valider les capacités  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Feuilles capacité**, puis choisissez le lien associé.  
2.  Renseignez les champs **Date comptabilisation** et **N° document**.  
3.  Dans le champ **Type**, entrez le type de capacité, **Poste de charge** ou **Centre de charge**, que vous validez.  
4.  Dans le champ **N°**, saisissez le nom du centre de charge ou du poste de charge.  
5.  Entrez les données nécessaires dans les autres champs, tels que **Heure début**, **Heure fin**, **Quantité**, et **Rebut**.  
6.  Choisissez l’action **Valider** pour valider les capacités.  

## <a name="to-view-work-center-ledger-entries"></a>Pour afficher les écritures comptables centre de charge  
Sur les pages **Fiche centre de charge** et **Fiche poste de charge**, vous pouvez afficher les capacités validées en tant que résultat des ordres de fabrication terminés.    
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Centres de charge**, puis choisissez le lien associé.  
2.  Ouvrez la fiche **Centre de charge** appropriée dans la liste, puis choisissez l’action **Écritures comptables capacité**.  

La page **Écritures comptables capacité** affiche les écritures validées relatives au centre de charge dans l’ordre de leur validation.   

## <a name="see-also"></a>Voir aussi  
[Production](production-manage-manufacturing.md)    
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)      
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]