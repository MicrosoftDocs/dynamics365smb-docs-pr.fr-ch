---
title: 'Gestion des stocks, Suisse [CH]'
description: Cet article décrit les améliorations apportées aux fonctions spéciales de gestion des stocks dans Business Central en Suisse.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/21/2021
ms.author: edupont
---
# <a name="swiss-inventory-management"></a><a name="swiss-inventory-management"></a><a name="swiss-inventory-management"></a>Gestion des stocks, Suisse
[!INCLUDE[prod_short](../../includes/prod_short.md)] comprend les améliorations apportées à la gestion des stocks en Suisse. Notamment :  

- Génération d'état détaillé.  Pour plus d'informations, voir État Stock - Statistiques vente et État Stock - Liste.  
- Possibilité de suivre une facture pour plusieurs expéditions.  
- Y compris un code d'emplacement de fiche article en tant que code d'emplacement par défaut pour les lignes de vente et les feuilles articles. Pour plus d'informations, reportez-vous à [Configurer des magasins](../../inventory-how-setup-locations.md).

## <a name="managing-item-details"></a><a name="managing-item-details"></a><a name="managing-item-details"></a>Gestion des détails article
Les sociétés peuvent avoir différents entrepôts pour différentes catégories de produits. Dans ce cas, vous devez utiliser le code d'emplacement par défaut récupéré à partir de la fiche article. Lorsque vous définissez un code d'emplacement pour un article, il est transféré vers les lignes de vente et les feuilles article en tant que code d'emplacement d'article par défaut. Pour plus d'informations, voir la table Ligne feuille article et Ligne vente.  

Les informations, telles que le numéro du client, le code adresse destinataire et le code personne des ventes client, sont enregistrées dans les écritures comptables article. Ces informations vous permettent de créer des critères de rapport personnalisés, tels que le revenu par client et les dispositions relatives aux articles ou aux ventes pour les commerciaux. Pour plus d'informations, voir la table Écriture comptable article.  

## <a name="invoices-with-multiple-shipments"></a><a name="invoices-with-multiple-shipments"></a><a name="invoices-with-multiple-shipments"></a>Factures pour plusieurs expéditions
Si plusieurs expéditions ont été validées pour un client, vous pouvez créer une facture regroupée avec la fonction **Extraire lignes expédition**. Pour plus d'informations, voir la page Extraire lignes expédition. Lorsque vous utilisez cette fonction, le texte créé sur les lignes de facture inclut des informations sur le numéro d'expédition et la date d'expédition. Par exemple, le texte peut paraître comme Expédition N° 102040 sur 25.01.01. Cela vous permet de suivre facilement les factures avec plusieurs expéditions.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi
 [Fonctionnalité locale, Suisse](switzerland-local-functionality.md)   
 [Configurer des magasins](../../inventory-how-setup-locations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
