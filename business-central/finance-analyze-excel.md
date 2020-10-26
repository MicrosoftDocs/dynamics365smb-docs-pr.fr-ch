---
title: Utiliser des états financiers et des aperçus dans Excel
description: En savoir plus sur la manière dont vous pouvez ouvrir des états financiers dans Microsoft Excel à partir de Business Central pour une meilleure analyse.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 53221cbacb35e7e82077295a6f7098f07c2b02e6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913486"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analyse des états financiers dans Microsoft Excel

Dans [!INCLUDE [prodshort](includes/prodshort.md)], vous pouvez visualiser les KPI et obtenir des aperçus de l’état financier de la société. Vous pouvez également ouvrir des listes dans Excel et analyser les données afférentes. De plus, vous pouvez exporter des états financiers volumineux, tels que le bilan ou les comptes de gestion vers Excel, analyser les données et imprimer les états.  

Depuis les tableaux de bord Gestionnaire d’activité et Comptable, vous pouvez choisir les états financiers à afficher dans Excel à partir d’un menu déroulant dans la section pour personnaliser le ruban. Lorsque vous sélectionnez un état, il est ouvert dans Excel ou Excel Online. Une macro complémentaire connecte les données à [!INCLUDE [prodshort](includes/prodshort.md)]. Cependant, vous devez vous connecter avec le même compte que celui utilisé avec [!INCLUDE [prodshort](includes/prodshort.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Affichage de l’aperçu et des détails dans Excel

Dans le ruban, sélectionnez l’état Excel approprié, et laissez-le ouvert afin d’accéder à l’aperçu que vous recherchiez. Dans cette version de [!INCLUDE [prodshort](includes/prodshort.md)], nous offrons les états Excel suivants :

- Bilan  
- Comptes de gestion  
- Déclaration de trésorerie  
- Déclaration de réserves  
- Comptabilité fournisseur âgée  
- Comptabilité client âgée  

Supposons que vous souhaitiez analyser en profondeur votre trésorerie. Depuis les tableaux de bord Gestionnaire d’activité et Comptable, vous pouvez ouvrir l’état **Déclaration de trésorerie** dans Excel, mais ce qui se produit réellement est que nous exportons les données appropriées pour vous et créons un classeur Excel sur la base d’un modèle prédéfini. Selon votre navigateur, vous pouvez être invité à ouvrir ou enregistrer le classeur.  

Dans Excel, vous pouvez voir un onglet où les données sont présentées sur la première feuille. Toutes les données qui ont été exportées sont également présentes dans d’autres feuilles en cas de besoin. Vous pouvez imprimer l’état immédiatement, ou vous pouvez le modifier jusqu’à ce que vous ayez l’aperçu et les détails que vous souhaitez. Utilisez la macro complémentaire [!INCLUDE [prodshort](includes/prodshort.md)] pour Excel afin de mieux filtrer et analyser les données.  

### <a name="understanding-the-excel-templates"></a>Comprendre les modèles Excel

Les états Excel prédéfinis sont basés sur les données de l’entreprise actuelle. Par exemple, la société de démonstration a mis en place le plan comptable pour répertorier trois comptes règlement sous *Actifs actuels*  : 10100 **Compte chèque** , 10200 **Compte épargne** et 10300 **Fonds de caisse** . Les comptes ont le champ **Sous-catégorie de compte** défini sur *Espèces* , et c’est leur montant combiné qui apparaît comme *Espèces* dans l’état Excel **Bilan** .  

Des feuilles supplémentaires dans le classeur Excel affichent les données derrière l’état. Mais pour savoir ce qui se cache derrière les regroupements dans les états Excel, vous devrez peut-être revenir à [!INCLUDE [prodshort](includes/prodshort.md)] et appliquer des filtres aux listes, par exemple.  

## <a name="the-prodshort-excel-add-in"></a>Module complémentaire [!INCLUDE [prodshort](includes/prodshort.md)] pour Excel

Votre expérience [!INCLUDE [prodshort](includes/prodshort.md)] inclut une macro complémentaire pour Excel. Selon votre abonnement, vous êtes connecté automatiquement, ou vous devez spécifier les mêmes informations de connexion utilisées pour [!INCLUDE [prodshort](includes/prodshort.md)]. Pour plus d’informations, voir [Affichage et édition dans Excel depuis Business Central](across-work-with-excel.md).  

Le module complémentaire vous permet d’obtenir des données actualisées à partir de [!INCLUDE [prodshort](includes/prodshort.md)] et d’appliquer les modifications à [!INCLUDE [prodshort](includes/prodshort.md)]. Toutefois, la possibilité de transférer les données vers la base de données est désactivée pour les états financiers Excel dans la liste ci-dessus.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Affichage et édition dans Excel depuis Business Central](across-work-with-excel.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Comptabilité et plan comptable](finance-general-ledger.md)  
[Utilisation de Business Central](ui-work-product.md)  
