---
title: "Taxe sur les ventes et groupes de taxes aux États-Unis et au Canada | Microsoft Docs"
description: "En savoir plus sur la manière dont la Sales Tax est configurée, et sur le fonctionnement des groupes taxes, des zones de recouvrement, des autorités de recouvrement et des spécifications de taxe."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Taxe sur les ventes et groupes de taxes aux États-Unis et au Canada
Lorsque vous commencez à utiliser [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exécuter un guide de configuration assistée afin de rapidement et facilement configurer les informations relatives à la Sales Tax pour votre société, vos clients et vos fournisseurs. En quelques minutes, vous êtes prêt à créer des documents vente et des documents achat pour lesquels la Sales Tax est calculée correctement. Ceci est expliqué [dans notre billet de blog](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Si vous passez à la section Ma société vierge, nous vous recommandons de commencer par utiliser chacun des guides de configuration assistée, y compris celui qui concerne la Sales Tax. Si vous préférez configurer la Sales Tax par vous-même, cet article explique ce que vous devez prendre en compte.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Groupes taxes, zones de recouvrement et autorités de recouvrement
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un groupe taxes représente un groupe d'articles ou de ressources soumis au même conditions pour ce qui est des taxes. Par exemple, vous pouvez configurer un groupe taxes pour les articles soumis à la taxe et un autre pour les articles non soumis à la taxe. Vous devez affecter des codes groupe taxes aux articles en stock et aux comptes généraux. De même, vous devez affecter des codes zone recouvrement aux clients, aux magasins et à vos propres paramètres de société. Le guide de configuration assistée vous aide à effectuer ces opérations.  

Chaque zone recouvrement correspond à un regroupement d'autorités fiscales basé sur une situation géographique particulière. Par exemple, la zone recouvrement de Miami, Floride, comprend trois autorités fiscales de la Sales Tax : la ville (Miami), le comté (Dade) et l'état (Floride). [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut un ensemble limité de zones de recouvrement avec une configuration par défaut, mais vous pouvez les modifier et ajouter de nouvelles zones de recouvrement.  

Si vous configurez de nouvelles zones et juridictions de recouvrement, vous devez veiller à bien remplir les champs correctement. Aux États-Unis, les états, les régions, les villes et les localités peuvent prélever la taxe sur les ventes. Au Canada, le gouvernemental fédéral et les provinces sont en mesure de prélever la Sales Tax. Les sociétés recueillent et la Sales Tax et la versent aux autorités gouvernementales pour les produits vendus aux utilisateurs finaux. La Sales Tax peut également être facturée sur une Sales Tax existante. Par exemple, la taxe peut être calculée sur un montant facture vente qui comprend déjà la taxe imposée par d'autres autorités.  

Au Canada, les montants de taxe doivent être détaillés dans les documents concernant chaque autorité de recouvrement. Jusqu'à quatre autorités de recouvrement peuvent apparaître dans un document, et les autorités dotées du même ordre d'impression sont regroupées lors de l'impression.  

## <a name="tax-details"></a>USA spécifications taxe
La fenêtre **USA spécifications taxe** affiche différentes combinaisons de zones de recouvrement de la Sales Tax et de groupes de taxe afin d'établir les taux de taxe. Pour chaque autorité de recouvrement, nous vous recommandons de configurer un groupe taxes pour la Sales Tax normale, un autre groupe taxes pour les articles ou les services qui ne sont pas soumis à la taxe et un groupe taxes supplémentaire pour chaque type d'article ou de service traité avec un taux de taxe différent dans cette zone de recouvrement.  

Aux États-Unis, lorsque vous vendez à un client dans un magasin où vous n'avez pas de *situs*(ou un magasin légal dans cet état) vous ne percevez pas la Sales Tax. Pour les magasins dans lesquels vous n'avez pas de situs, assurez-vous que la valeur des champs **Taxe inférieure minimum** and **Taxe supérieure maximum** est égale à 0,00.  

## <a name="see-also"></a>Voir aussi
[Finance](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Taxe sur les ventes et taxe sur les biens et les services au Canada](ca-finance-tax.md)  
[Configuration simplifiée de la Sales Tax](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

