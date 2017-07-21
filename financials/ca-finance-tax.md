---
title: Taxe sur les ventes au Canada| Microsoft Docs
description: En savoir plus sur la taxe sur les ventes et la taxe sur les biens et les services au Canada.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a>Déclaration de la taxe sur les ventes et taxe sur les biens/services au Canada
Au Canada, si un fournisseur n'a pas de présence commerciale dans la province dans laquelle les achats sont effectués, le fournisseur facture la taxe sur les biens et des services (Goods and Services Tax - GST) ou la taxe harmonisée (Harmonized Sales Tax - HST) uniquement. Toutefois, si la province applique une taxe provinciale sur les ventes (Provincial Sales Tax - PST), l'acheteur doit tout de même calculer le montant de la PST et le payer directement à la province. Lorsqu'un code zone de recouvrement provincial est sélectionné, [!INCLUDE[d365fin](includes/d365fin_md.md)] l'utilise pour calculer la PST et la valider de sorte que l'impôt à payer apparaisse à la fois dans la comptabilité et dans les enregistrement d'écriture TVA. Par conséquent, le code zone de recouvrement sélectionné ici doit uniquement inclure la PST et non la GST.  

Pour plus d'informations de la taxe sur les ventes, reportez-vous à [Taxe sur les ventes et groupes de taxes aux États-Unis et au Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Envoi du fichier GST/HST
Les informations sur les taxes dans les documents achat permettent de générer un transfert de fichier GST/HST en ligne que vous devez transmettre aux autorités fiscales. Ce champ inclut la taxe sur les biens et les services (GST) et la taxe harmonisée (HST). Le fichier est créé dans un format de fichier .tax, qui peut être transféré en ligne.  

## <a name="see-also"></a>Voir aussi
[Finance](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Taxe sur les ventes et groupes de taxes aux États-Unis et au Canada](us-finance-sales-tax.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

