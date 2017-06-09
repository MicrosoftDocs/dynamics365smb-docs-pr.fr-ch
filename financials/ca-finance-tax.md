---
title: Taxe sur les ventes et taxe sur les biens et les services au Canada | Microsoft Docs
description: En savoir plus sur les taxes GST et HST.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Taxe sur les ventes et taxe sur les biens et les services au Canada
Au Canada, si un fournisseur n'a pas de présence commerciale dans la province dans laquelle les achats sont effectués, le fournisseur facture la taxe sur les biens et des services (Goods and Services Tax - GST) ou la taxe harmonisée (Harmonized Sales Tax - HST) uniquement. Toutefois, si la province applique une taxe provinciale sur les ventes (Provincial Sales Tax - PST), l'acheteur doit tout de même calculer le montant de la PST et le payer directement à la province. Lorsqu'un code zone de recouvrement provincial est sélectionné, [!INCLUDE[d365fin](includes/d365fin_md.md)] l'utilise pour calculer la PST et la valider de sorte que l'impôt à payer apparaisse à la fois dans la comptabilité et dans les enregistrement d'écriture TVA. Par conséquent, le code zone de recouvrement sélectionné ici doit uniquement inclure la PST et non la GST.  

Pour plus d'informations de la taxe sur les ventes, reportez-vous à [Taxe sur les ventes et groupes de taxes aux États-Unis et au Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Envoi du fichier GST/HST
Les informations sur les taxes dans les documents achat permettent de générer un transfert de fichier GST/HST en ligne que vous devez transmettre aux autorités fiscales. Ce champ inclut la taxe sur les biens et les services (GST) et la taxe harmonisée (HST). Le fichier est créé dans un format de fichier .tax, qui peut être transféré en ligne.  

## <a name="see-also"></a>Voir aussi
[Finance](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Taxe sur les ventes et groupes de taxes aux États-Unis et au Canada](us-finance-sales-tax.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

