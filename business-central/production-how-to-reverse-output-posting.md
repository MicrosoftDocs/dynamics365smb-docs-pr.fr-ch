---
title: Contrepasser la validation de production
description: Il arrive qu’une validation de production doive être contrepassée. Cette rubrique décrit la procédure de contrepassation de la validation de production.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: ed45facfc64dda670d0e1e4d7dd9b396b4c11fae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132800"
---
# <a name="reverse-output-posting"></a>Contrepasser la validation de production

Il arrive qu’une validation de production doive être contrepassée. C’est le cas, par exemple, si une erreur de saisie de données a été commise et qu’une quantité de production incorrecte a été validée pour un ordre de fabrication.  

## <a name="to-reverse-an-output-posting"></a>Pour contrepasser une validation de production

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille production**, puis choisissez le lien associé. Sélectionnez votre lot.  
2. Renseignez les champs selon vos besoins. Pour plus d’informations, voir [Valider par lots la production et les temps d’exécution](production-how-to-post-output-quantity.md).
3. Dans le champ **Ecriture lettrage**, sélectionnez l’écriture comptable article associée. Cette action contrepasse les écritures comptables capacité et article.  
4. Validez la contrepassation en validant la feuille.  

Les écritures de la feuille production sont validées dans les écritures article comme un ajustement positif.  

## <a name="see-also"></a>Voir aussi

 [Production](production-manage-manufacturing.md) [Paramétrage de la production](production-configure-production-processes.md)  
 [Planifié](production-planning.md)  
 [Stock](inventory-manage-inventory.md)  
 [Achats](purchasing-manage-purchasing.md)  
 [Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]