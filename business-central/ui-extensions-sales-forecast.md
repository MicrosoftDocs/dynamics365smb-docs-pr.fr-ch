---
title: Utilisation de l'extension Prévisions des ventes et des stocks pour gérer le stock | Microsoft Docs
description: Cette extension vous aide à prévoir les ventes, avoir un aperçu clair des ruptures de stock prévues, et même de vous aider à créer des demandes de réapprovisionnement aux fournisseurs.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 3ae36c5cb7f1738bded3947c99c197221a621f07
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821338"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>Extension Prévisions des ventes et des stocks
La gestion des stocks est un compromis entre le service client et la gestion de vos coûts. D'une part, un stock faible exige un capital travail inférieur, mais d'autre part, les ruptures de stock mènent potentiellement à des ventes non concrétisées. L'extension Sales and Inventory Forecast prévoit les ventes potentielles à l'aide des données historiques et donne une présentation claire des ruptures de stock prévues. Selon la prévision, l'extension aide à créer des demandes de réapprovisionnement auprès de vos fournisseurs et vous fait gagner du temps.  

## <a name="setting-up-forecasting"></a>Paramétrage des prévisions
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], la connexion à [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) est déjà configurée pour vous. Mais vous pouvez configurer les prévisions pour utiliser un autre type de période pour exécuter votre rapport, par exemple en passant des prévisions mensuelles aux prévisions trimestrielles. Vous pouvez également choisir le nombre de périodes à partir desquelles calculer les prévisions, selon le degré de granularité que vous souhaitez accorder à vos prévisions. Nous vous proposons de faire des prévisions mensuelles avec un horizon à 12 mois.  

## <a name="using-the-forecasts"></a>À l'aide des prévisions
Cette extension utilise Cortana Intelligence pour prévoir les ventes futures en fonction de votre historique des ventes pour vous aider à éviter les ruptures de stock. Par exemple, lorsque vous choisissez un article sur la page **Articles**, le graphique du volet **Prévision des articles** affiche les ventes estimées de cet article dans la période à venir. Ainsi vous pouvez voir si vous risquez d'être bientôt en rupture de stock pour l'article.  

Vous pouvez également utiliser l'extension pour suggérer quand réapprovisionner les stocks. Par exemple, si vous créez un bon de commande pour Fabrikam, car vous souhaitez acheter leur nouvelle chaise de bureau, l'extension Sales and Inventory Forecast vous suggèrera également de réapprovisionner la chaise dactylo LONDON que vous achetez généralement auprès de ce fournisseur. En effet, les prévisions de l'extension indiquent que vous allez arriver en rupture de stocks concernant la chaise dactylo LONDON dans les deux prochaines semaines. Aussi, nous vous recommandons de commander davantage de chaises dès à présent.  

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Stock](inventory-manage-inventory.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)  
