---
title: "Comment convertir des magasins existants en magasins entrepôt | Microsoft Docs"
description: "Vous pouvez activer un emplacement de manière à ce qu'il utilise les zones et emplacements, et qu'il devienne l'entrepôt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7d4b2c86174386faa86ab6c09faa463d26d3d2ac
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Convertir des magasins existants en magasins entrepôt
Vous pouvez activer un emplacement de manière à ce qu'il utilise les zones et emplacements, et qu'il devienne l'entrepôt.  

Le traitement par lots qui active un emplacement crée des écritures entrepôt pour l'emplacement ajustement du magasin qui sera affecté à tous les articles stockés dans le magasin. Ces écritures sont équilibrées lorsque les écritures inventaire entrepôt sont saisies après chaque traitement par lots.  

Vous pouvez créer des zones et des emplacements avant ou après la conversion. Le seul emplacement devant être créé avant la conversion est celui qui sert ensuite d'emplacement ajustement.  

> [!IMPORTANT]  
>  Pour supprimer toutes les quantités négatives et les éventuels documents entrepôt ouverts avant de convertir le magasin à des fins de gestion d'entrepôt, exécutez un état pour identifier les articles dont la quantité est négative et les documents entrepôt ouverts pour le magasin. Pour plus d'informations, reportez\-vous à la rubrique Vérifiez l'inventaire négatif.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Activation d'un emplacement existant en tant qu'entrepôt  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Création entrepôt**, puis sélectionnez le lien connexe.  
2.  Dans le champ **Code magasin**, indiquez le magasin que vous souhaitez activer pour un traitement d'entrepôt.  
3.  Dans le champ **Code empl. ajustement**, indiquez à quel emplacement du magasin les écritures entrepôt non synchronisées sont enregistrées. Pour plus d'informations, reportez-vous à la section « Pour synchroniser les écritures entrepôt ajustées avec les écritures comptables article associées » dans [Inventaire, ajustement et reclassement du stock](inventory-how-count-adjust-reclassify.md).  

    À l'aide des écritures comptables article ouvertes de l'emplacement, des lignes feuille entrepôt sont créées qui additionnent les combinaisons N° article, Code variante, Code unité et, si nécessaire, N° lot et N° de série des écritures comptables article. Les lignes feuille entrepôt sont ensuite validées. Cette validation crée des écritures entrepôt qui placent le stock dans l'emplacement ajustement entrepôt. Le **code emplacement ajustement** est également défini dans la fiche magasin.  

4.  Pour savoir quels articles ont été ajoutés à l'emplacement ajustement pendant le traitement par lots, vous pouvez exécuter l'état **Emplacement ajust. mag**.  
5.  Une fois le traitement par lots **Création entrepôt** terminé, vous devez effectuer et valider un inventaire physique entrepôt. Pour plus d'informations, voir [Inventaire, ajustement et reclassement du stock](inventory-how-count-adjust-reclassify.md).  

> [!NOTE]  
>  Il est recommandé de lancer le traitement par lots **Création entrepôt** à un moment où il ne risque pas de nuire au fonctionnement habituel du système. Étant donné que ce processus traite chaque écriture de la table **Écriture comptable article**, il peut durer plusieurs heures si cette table en comporte un grand nombre.  

 Dans le cas de magasins n'ayant pas utilisé de documents Gestion d'entrepôt avant la conversion, vous devez rouvrir et relancer les documents source dont la réception ou l'envoi n'était que partiel avant la conversion.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

