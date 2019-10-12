---
title: Configuration du plan comptable
description: Vous modifiez les comptes par défaut dans le plan comptable, et vous pouvez ajouter de nouveaux comptes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 97db6065f405397dbc4a077f571883a28bda8c3c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300052"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Configuration ou modification du plan comptable
Le plan comptable affiche les comptes généraux qui stockent vos données financières. [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut un plan comptable standard prêt à prendre en charge votre société.
Cependant, vous pouvez modifier les comptes par défaut, et vous pouvez ajouter de nouveaux comptes.  

## <a name="adding-or-changing-accounts"></a>Ajout ou modification de comptes
À partir du plan comptable, vous pouvez ouvrir chaque compte général et ajouter ou modifier des paramètres.

> [!NOTE]  
>   Vous pouvez supprimer un compte général. Toutefois, avant que de le supprimer, les conditions suivantes doivent être réunies :  
>  
>   * Le solde du compte doit être nul.  
>   * Le champ **Autoriser suppr. cpte gén. av.** doit être défini sur la page **Paramètres comptabilité**, et le compte ne doit pas comporter d'écritures comptables à cette date ou après celle-ci.  
>   * Si le champ **Vérifier activité cpte général** de la page **Paramètres comptabilité** est sélectionné, le compte ne doit pas être utilisé dans les groupes comptabilisation ni dans une configuration de la validation.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] vous empêchera de supprimer un compte général qui stocke les données nécessaires au plan comptable.  

## <a name="see-also"></a>Voir aussi
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Importation des données à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Utilisation des tableaux d'analyse](bi-how-work-account-schedule.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
