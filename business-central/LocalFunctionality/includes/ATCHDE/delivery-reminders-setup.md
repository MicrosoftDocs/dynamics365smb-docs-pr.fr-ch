---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ec32c54dbf87e3594b6587f9cf66141576cad1d9
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959649"
---
Dans [!INCLUDE[d365fin](../../../includes/d365fin_md.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard. Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la page **Paramètres achats**.  

## <a name="to-set-up-delivery-reminders"></a>Pour paramétrer des relances livraison  

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres achats**, puis sélectionnez le lien associé.  
2. Dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Date réception demandée**|Spécifie que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.|  
    |**Date réception confirmée**|Spécifie que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.|  
    |**Date réception prévue**|Spécifie que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.|  

3. Renseignez les champs supplémentaires comme décrit dans le tableau suivant.  

    |Champ|Description|  
    |---------------------------------|---------------------------------------|  
    |**Numéros relances livraison**|Code souche de numéros pour les relances livraison.|  
    |**Numéros relances livraison émis**|Code souche de numéros pour les relances livraison émises.|  

4. Cliquez sur le bouton **OK**.  