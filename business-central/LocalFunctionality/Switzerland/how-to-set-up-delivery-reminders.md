---
title: 'Procédure : Paramétrer des relances livraison'
description: Dans Business Central, vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07677a711bcc153da7933e42ec80e67a0d50eb35
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "923099"
---
# <a name="set-up-delivery-reminders"></a>Configurer des relances livraison
Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard. Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la page **Paramètres achats**.  

## <a name="to-set-up-delivery-reminders"></a>Pour paramétrer des relances livraison  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.  
2.  Dans le raccourci **Général**, dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.  

    |Option|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Date réception demandée**|Pour indiquer que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.|  
    |**Date réception confirmée**|Pour indiquer que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.|  
    |**Date réception prévue**|Pour indiquer que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.|  

3.  Sur le raccourci **Numérotation**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Numéros relances livraison**|Code souche de numéros pour les relances livraison.|  
    |**Numéros relances livraison émis**|Code souche de numéros pour les relances livraison émises.|  

4.  Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
 [relances livraison](delivery-reminders.md)   
 [Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Créer manuellement des relances livraison](how-to-create-delivery-reminders-manually.md)
