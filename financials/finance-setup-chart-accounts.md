---
title: Configuration du plan comptable| Microsoft Docs
description: "Décrit la manière dont vous pouvez modifier le plan comptable."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 48202a9e9a763dcb22bed9975aa9c4a39d2dc4ae
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Configuration ou modification du plan comptable
Le plan comptable affiche les comptes généraux qui stockent vos données financières. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] inclut un plan comptable standard prêt à prendre en charge votre société.
Cependant, vous pouvez modifier les comptes par défaut, et vous pouvez ajouter de nouveaux comptes.  

## <a name="adding-or-changing-accounts"></a>Ajout ou modification de comptes
À partir du plan comptable, vous pouvez ouvrir chaque compte général et ajouter ou modifier des paramètres.

**Remarque** : vous pouvez supprimer un compte général. Toutefois, avant que de le supprimer, les conditions suivantes doivent être réunies :  

* Le solde du compte doit être nul.  
* Le champ **Autoriser suppr. cpte gén. av.** doit être défini dans la fenêtre **Paramètres comptabilité**, et le compte ne doit pas comporter d'écritures comptables à cette date ou après celle-ci.  
* Si le champ **Vérifier activité cpte général** de la fenêtre **Paramètres comptabilité** est sélectionné, le compte ne doit pas être utilisé dans les groupes comptabilisation ni dans une configuration de la validation.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] vous empêchera de supprimer un compte général qui stocke les données nécessaires au plan comptable.  

## <a name="see-also"></a>Voir aussi
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Axes analytiques](finance-dimensions.md)  
[Importation à partir d'autres systèmes financiers](upload-data.md)  
[Procédure : utilisation des codes IGRF au Canada](ca-finance-work-gifi-codes.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
