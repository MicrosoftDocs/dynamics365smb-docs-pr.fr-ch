---
title: Spécifier la mise en page d'un chèque| Microsoft Docs
description: Vous pouvez concevoir et imprimer vos chèques dans différents formats pour respecter des normes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: fea52bfa75d953b96aecc0f3e354806324f77d83
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306331"
---
# <a name="select-a-check-layout"></a>Sélectionner une mise en page de chèque
Vous pouvez concevoir vos chèques de sorte à respecter les normes fixées par les autorités locales. Vous pouvez imprimer des images de chèques en anglais, en français ou en espagnol.

Les chèques sont conçus pour être imprimés aux formats d'image de chèques américains et canadiens, soit au format chèque-talon-chèque, soit au format talon-talon-chèque.

## <a name="to-select-a-check-layout"></a>Pour sélectionner une mise en page de chèque
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Sélection des états - Compte bancaire**, puis sélectionnez le lien associé.
2. Sur la page **Sélection des états : Banque**, dans le champ **Utilisation**, sélectionnez **Chèque**
3. Sélectionnez l'un des ID état suivants.

| ID état | Nom état | Description |
| --- | --- | --- |
| 1401 |Activer |Il s'agit de l'état par défaut. |
| 10411 |Chèque (Talon/Talon/Chèque) |Cet état est conçu pour imprimer des chèques au format talon/talon/chèque. |
| 10412 |Chèque (Talon/Chèque/Talon) |Cet état est conçu pour imprimer des chèques au format talon/chèque/talon. |
| 10413 |Trois chèques par page |Cet état est conçu pour imprimer trois chèques sur chaque page. |

Une fois que vous avez défini les mises en page de chèques, vous pouvez imprimer des chèques à partir de la page **Feuille paiement**. Pour plus d'informations, reportez-vous à [Utilisation des chèques](payables-how-work-checks.md).

Pour modifier l'une de ces mises en page de chèque par défaut, utilisez l'intégration Word ou RDLC. Pour plus d'informations, voir [Créer et modifier une présentation de rapport ou de document personnalisée](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Voir aussi
[Créer et modifier une présentation de rapport ou de document personnalisée](ui-how-create-custom-report-layout.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)   
[Exécution des processus de clôture d'exercice](year-how-complete-period-end-processes.md)  
[Utilisation de [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)
