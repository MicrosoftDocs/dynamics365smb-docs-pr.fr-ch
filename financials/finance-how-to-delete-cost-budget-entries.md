---
title: "Procédure : suppression des écritures budget des coûts | Microsoft Docs"
description: "Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ad8ba706ba1b376b78449ba801ed0f4fc4cfe09
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="delete-cost-budget-entries"></a>Supprimer écritures budget des coûts
Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.  

Pour empêcher tout écart dans les écritures du budget des coûts et les écritures du registre des coûts, vous ne pouvez pas supprimer une écriture unique ou un lot d'écritures dans la liste des écritures du registre.  

### <a name="to-delete-a-cost-budget-entry"></a>Pour supprimer une écriture budget des coûts  

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Supprimer écritures budget des coûts**, puis sélectionnez le lien connexe.  

    Le champ **N° hist. transaction de destination** affiche le numéro de la dernière écriture du registre et n'est pas modifiable.  

    Vous pouvez utiliser le champ **N° hist. transaction d'origine** pour sélectionner un numéro d'écriture du registre à partir duquel commencer la suppression.  
2.  Cliquez sur le bouton **OK** pour supprimer les écritures du budget des coûts sélectionnées.  

> [!NOTE]  
>  Pour éviter une suppression accidentelle des écritures du budget des coûts, vous pouvez clôturer les écritures du registre en marquant les lignes comme **Clôturées** dans le champ **Clôturées** de la fenêtre **Registre du budget des coûts**.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)
[Création des budgets des coûts](finance-create-cost-budgets.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

