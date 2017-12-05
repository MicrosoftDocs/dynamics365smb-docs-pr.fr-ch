---
title: "Utiliser des états financiers et des aperçus dans Excel | Microsoft Docs"
description: "En savoir plus sur la manière dont vous pouvez ouvrir des états financiers dans Microsoft Excel à partir de Dynamics 365 Business edition pour une meilleure analyse."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: e58d412b9fb182a8a8f640593f78decf0e6aecc1
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analyse des états financiers dans Microsoft Excel
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez visualiser les KPI et obtenir des aperçus de l'état financier de la société. Vous pouvez également ouvrir des listes dans Excel et analyser les données afférentes. De plus, vous pouvez exporter des états financiers volumineux, tels que le bilan ou les comptes de gestion vers Excel, analyser les données et imprimer les états.  

Depuis les tableaux de bord Gestionnaire d'activité et Comptable, vous pouvez choisir les états financiers à afficher dans Excel à partir d'un menu déroulant dans la section pour personnaliser le ruban. Lorsque vous sélectionnez un état, il est ouvert dans Excel ou Excel Online. Une macro complémentaire connecte les données à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cependant, vous devez vous connecter avec le même compte que celui utilisé avec [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Affichage de l'aperçu et des détails dans Excel
Dans le ruban, sélectionnez l'état Excel approprié, et laissez-le ouvert afin d'accéder à l'aperçu que vous recherchiez. Dans cette version de [!INCLUDE[d365fin](includes/d365fin_md.md)], nous offrons les états Excel suivants :

- Bilan  
- Comptes de gestion  
- Déclaration de trésorerie  
- Déclaration de réserves  
- Comptabilité fournisseur âgée  
- Comptabilité client âgée  

Supposons que vous souhaitiez analyser en profondeur votre trésorerie. Depuis les tableaux de bord Gestionnaire d'activité et Comptable, vous pouvez ouvrir l'état Déclaration de trésorerie dans Excel, mais ce qui se produit réellement est que nous exportons les données appropriées pour vous et créons un classeur Excel sur la base d'un modèle prédéfini. Selon votre navigateur, vous pouvez être invité à ouvrir ou enregistrer le classeur.  

Dans Excel, vous pouvez voir un onglet où les données sont présentées sur la première feuille. Toutes les données qui ont été exportées sont également présentes dans d'autres feuilles en cas de besoin. Vous pouvez imprimer l'état immédiatement, ou vous pouvez le modifier jusqu'à ce que vous ayez l'aperçu et les détails que vous souhaitez. Utilisez la macro complémentaire [!INCLUDE[d365fin](includes/d365fin_md.md)] pour Excel afin de mieux filtrer et analyser les données.  

## <a name="the-included365finincludesd365finmdmd-excel-add-in"></a>Macro complémentaire [!INCLUDE[d365fin](includes/d365fin_md.md)] pour Excel
Votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut une macro complémentaire pour Excel. Selon votre abonnement, vous êtes connecté automatiquement, ou vous devez spécifier les mêmes informations de connexion utilisées pour [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Le module complémentaire vous permet d'obtenir des données actualisées à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)] et d'appliquer les modifications à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Toutefois, la possibilité de transférer les données vers la base de données est désactivée pour les états financiers Excel dans la liste ci-dessus.  

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utilisation de Dynamics 365](ui-work-product.md)  

