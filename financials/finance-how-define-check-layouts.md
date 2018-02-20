---
title: "Spécifier la mise en page d'un chèque| Microsoft Docs"
description: "Vous pouvez concevoir et imprimer vos chèques dans différents formats pour respecter des normes."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd745186e4518c2005e34e6b2cbbc8925fd8931e
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="define-check-layouts"></a>Définir les mises en page de chèques
Vous pouvez concevoir vos chèques de sorte à respecter les normes fixées par les autorités locales. Vous pouvez imprimer des images de chèques en anglais, en français ou en espagnol.

Les chèques sont conçus pour être imprimés aux formats d'image de chèques américains et canadiens, soit au format chèque-talon-chèque, soit au format talon-talon-chèque.

## <a name="to-define-check-layouts"></a>Pour définir les mises en page de chèques
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Sélection des états - Compte bancaire**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Sélection des états : Banque**, dans le champ **Utilisation**, sélectionnez **Chèque**
3. Sélectionnez l'un des ID état suivants.

| ID état | Nom état | Description |
| --- | --- | --- |
| 1401 |Activer |Il s'agit de l'état par défaut. |
| 10401 |Chèque (Talon/Talon/Chèque) |Cet état est conçu pour imprimer des chèques au format talon/talon/chèque. |
| 10411 |Chèque (Talon/Chèque/Talon) |Cet état est conçu pour imprimer des chèques au format chèque/talon/chèque. |

Une fois que vous avez défini les mises en page de chèques, vous pouvez imprimer des chèques à partir de la fenêtre **Feuille paiement**. Pour plus d'informations, reportez-vous à [Utilisation des chèques](payables-how-work-checks.md).

## <a name="see-also"></a>Voir aussi
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)   
[Exécution des processus de clôture d'exercice](year-how-complete-period-end-processes.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

