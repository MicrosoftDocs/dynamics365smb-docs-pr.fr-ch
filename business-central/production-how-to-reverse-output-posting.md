---
title: Contrepasser la validation de production
description: Il arrive qu’une validation de production doive être contrepassée. Cette rubrique décrit la procédure de contrepassation de la validation de production.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5510
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Contrepasser la validation de production

Il arrive qu’une validation de production doive être contrepassée. C’est le cas, par exemple, si une erreur de saisie de données a été commise et qu’une quantité de production incorrecte a été validée pour un ordre de fabrication.  

## Pour contrepasser une validation de production

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille production**, puis choisissez le lien associé. Sélectionnez votre lot.  
2. Renseignez les champs selon vos besoins. Pour plus d’informations, voir [Valider par lots la production et les temps d’exécution](production-how-to-post-output-quantity.md).
3. Dans le champ **Ecriture lettrage**, sélectionnez l’écriture comptable article associée. Cette action contrepasse les écritures comptables capacité et article.  
4. Validez la contrepassation en validant la feuille.  

Les écritures de la feuille production sont validées dans les écritures article comme un ajustement positif.  

## Voir aussi

 [Production](production-manage-manufacturing.md) [Paramétrage de la production](production-configure-production-processes.md)  
 [Planifié](production-planning.md)  
 [Stock](inventory-manage-inventory.md)  
 [Achats](purchasing-manage-purchasing.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]