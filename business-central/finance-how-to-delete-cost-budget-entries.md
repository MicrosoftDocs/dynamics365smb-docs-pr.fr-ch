---
title: 'Procédure : suppression des écritures budget des coûts | Microsoft Docs'
description: Vous utilisez le traitement par lots Supprimer écritures budget des coûts pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 04510e87789e6d69b33009be7ebbaf7a405d0dff
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882723"
---
# <a name="delete-cost-budget-entries"></a>Supprimer écritures budget des coûts
Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.  

Pour empêcher tout écart dans les écritures du budget des coûts et les écritures du registre des coûts, vous ne pouvez pas supprimer une écriture unique ou un lot d'écritures dans la liste des écritures du registre.  

### <a name="to-delete-a-cost-budget-entry"></a>Pour supprimer une écriture budget des coûts  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer écritures budget des coûts**, puis choisissez le lien associé.  

    Le champ **N° hist. transaction de destination** affiche le numéro de la dernière écriture du registre et n'est pas modifiable.  

    Vous pouvez utiliser le champ **N° hist. transaction d'origine** pour sélectionner un numéro d'écriture du registre à partir duquel commencer la suppression.  
2.  Cliquez sur le bouton **OK** pour supprimer les écritures du budget des coûts sélectionnées.  

> [!NOTE]  
>  Pour éviter une suppression accidentelle des écritures du budget des coûts, vous pouvez clôturer les écritures du registre en marquant les lignes comme **Clôturées** dans le champ **Clôturées** de la page **Registre du budget des coûts**.  

## <a name="see-also"></a>Voir aussi  
[Comptabilité pour les coûts](finance-manage-cost-accounting.md)
[Création des budgets des coûts](finance-create-cost-budgets.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
