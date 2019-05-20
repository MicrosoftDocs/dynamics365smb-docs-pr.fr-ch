---
title: Gestion des stocks, Suisse
description: Les améliorations comprennent les fonctions spéciales de gestion des stocks en Suisse.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 697e9501ba09daf63eecc2e17f7695f757bafb5a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245627"
---
# <a name="swiss-inventory-management"></a>Gestion des stocks, Suisse
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] comprend les améliorations apportées à la gestion des stocks en Suisse. Notamment :  

- Génération d'état détaillé.  Pour plus d'informations, voir État Stock - Statistiques vente et État Stock - Liste.  
- Possibilité de suivre une facture pour plusieurs expéditions.  
- Y compris un code d'emplacement de fiche article en tant que code d'emplacement par défaut pour les lignes de vente et les feuilles articles. Pour plus d'informations, reportez-vous à [Configurer des magasins](../../inventory-how-setup-locations.md).

## <a name="managing-item-details"></a>Gestion des détails article  
Les sociétés peuvent avoir différents entrepôts pour différentes catégories de produits. Dans ce cas, vous devez utiliser le code d'emplacement par défaut récupéré à partir de la fiche article. Lorsque vous définissez un code d'emplacement pour un article, il est transféré vers les lignes de vente et les feuilles article en tant que code d'emplacement d'article par défaut. Pour plus d'informations, voir la table Ligne feuille article et Ligne vente.  

Les informations, telles que le numéro du client, le code adresse destinataire et le code personne des ventes client, sont enregistrées dans les écritures comptables article. Ces informations vous permettent de créer des critères de rapport personnalisés, tels que le revenu par client et les dispositions relatives aux articles ou aux ventes pour les commerciaux. Pour plus d'informations, voir la table Écriture comptable article.  

## <a name="invoices-with-multiple-shipments"></a>Factures pour plusieurs expéditions  
Si plusieurs expéditions ont été validées pour un client, vous pouvez créer une facture regroupée avec la fonction **Extraire lignes expédition**. Pour plus d'informations, voir la page Extraire lignes expédition. Lorsque vous utilisez cette fonction, le texte créé sur les lignes de facture inclut des informations sur le numéro d'expédition et la date d'expédition. Par exemple, le texte peut paraître comme Expédition N° 102040 sur 25.01.01. Cela vous permet de suivre facilement les factures avec plusieurs expéditions.  

## <a name="see-also"></a>Voir aussi  
 [Copier des articles existants pour créer de nouveaux articles](how-to-copy-existing-items-to-new-items.md)  
 [Fonctionnalité locale, Suisse](switzerland-local-functionality.md)   
 [Configurer des magasins](../../inventory-how-setup-locations.md)
