---
title: "Procédure de traçabilité des articles suivis | Microsoft Docs"
description: "Vous pouvez voir où un article suivi a été utilisé, y compris le mode et le moment de réception ou de production, de transfert, de vente, de consommation ou de retour. Vous pouvez également rechercher toutes les instances d'informations d'un numéro de série ou de lot particulier dans la base de données. Vous procédez à l'aide des fonctionnalités Traçabilité et Naviguer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 15676c264736b4547dd32cd7a37b252757f73b2a
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="trace-item-tracked-items"></a>Tracer des articles - Articles suivis
Vous pouvez voir où un article suivi a été utilisé, y compris le mode et le moment de réception ou de production, de transfert, de vente, de consommation ou de retour. Vous pouvez également rechercher toutes les instances d'informations d'un numéro de série ou de lot particulier dans la base de données. Vous procédez à l'aide des fonctionnalités Traçabilité et Naviguer.  

 Ces fonctions sont particulièrement utiles pour le contrôle qualité, lorsque vous devez déterminer quels clients ont reçus des produits correspondant à un numéro de lot particulier ou le lot dont provenait un composant défectueux.  

 Dans la fenêtre **Traçabilité**, vous pouvez effectuer une traçabilité en aval et en amont dans une série de mouvements de stock validés pour le numéro de lot ou de série.  

 Dans la fenêtre **Naviguer**, vous ne pouvez pas voir la séquence de transactions, mais vous pouvez afficher tous les enregistrements des numéros de série ou de lot, à la fois les écritures validées et les enregistrements ouverts.  

 Les deux fonctions peuvent être utilisées en association en transférant un numéro de série ou de lot suivi dans la fenêtre **Naviguer** pour terminer un scénario complet de suivi. Pour plus d'informations, voir [Procédure pas à pas : suivi des numéros de série et des numéros de lot](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Pour tracer des articles suivis  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Traçabilité**, puis sélectionnez le lien connexe.  
2.  Dans les champs de filtre dans le haut de la fenêtre, entrez les numéros d'article spécifiques ou un filtre pour les numéros d'article que vous voulez suivre.  
3.  Dans le champ **Afficher composants**, indiquez si vous voulez également voir d'où provenaient les composants des articles. Les options disponibles dans ce champ sont les suivantes.  

    |Champ|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Non**|sélectionnez cette options si vous ne voulez voir aucun composant.|  
    |**Avec traçabilité uniquement**|sélectionnez cette option si vous ne voulez voir que les composants ayant des numéros de lot ou de série.|  
    |**Tout**|sélectionnez cette option si vous voulez voir tous les composants.|  

4.  Dans le champ **Méthode de suivi**, sélectionnez la méthode que vous voulez utiliser pour suivre l'article. Les options sont les suivantes  

    |Champ|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Utilisation->origine**|Cette méthode suit l'article à partir de l'endroit où il a été utilisé jusqu'à l'endroit d'où il vient. Par exemple, si un article fabriqué a été vendu à un client, la fenêtre **Traçabilité** présente ce dernier en montrant d'abord la ligne expédition vente, que vous pouvez développer pour voir l'ordre de fabrication dont il provenait.|  
    |**Origine->utilisation**|cette méthode suit l'article à partir de l'endroit dont il provient dans le stock jusqu'à l'endroit où il a été utilisé. Par exemple, si un article fabriqué a été vendu à un client, la fenêtre **Traçabilité** présente ce dernier en montrant d'abord l'ordre de fabrication terminé, que vous pouvez développer pour voir les lignes expédition vente où l'article a été utilisé.|  

5.  Sélectionnez l'action **Suivi** pour exécuter le suivi.  

> [!NOTE]  
>  Si vous avez reçu le même lot sur plusieurs transactions, la fenêtre **Traçabilité** peut ne pas afficher toutes les transactions. Seules les transactions lettrées sont indiquées.  

> [!NOTE]  
>  Si l'historique d'une transaction supplémentaire dans une ligne traçabilité a déjà été suivi par une autre ligne au-dessus de celle-ci, la case à cocher **Déjà tracé** est activée. Pour une vue plus simple, ces lignes sous-jacentes ne s'affichent pas.  
>   
>  Pour trouver les lignes traçabilité où l'historique des transactions a déjà été suivi, cliquez sur le bouton **Aller sur déjà tracé**. La ligne traçabilité en question est sélectionnée et toutes les lignes sous-jacentes sont développées.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Pour rechercher des articles suivis avec Naviguer  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Naviguer**, puis sélectionnez le lien connexe.  
2.  Sur le raccourci **Traçabilité**, dans les champs **N° de série** et **N° lot**, entrez les numéros traçabilité que vous voulez suivre.  
3.  Sélectionnez l'action **Rechercher** pour rechercher toutes les instances du numéro de série ou de lot dans la base de données.  

## <a name="see-also"></a>Voir aussi  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : traçabilité](design-details-item-tracking.md)
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Procédure pas à pas : suivi des numéros de série et des numéros de lot](walkthrough-tracing-serial-lot-numbers.md)

