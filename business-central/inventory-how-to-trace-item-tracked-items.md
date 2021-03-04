---
title: Procédure de traçabilité des articles suivis | Microsoft Docs
description: Vous pouvez voir où un article suivi a été utilisé, y compris le mode et le moment de réception ou de production, de transfert, de vente, de consommation ou de retour. Vous pouvez également rechercher toutes les instances d’informations d’un numéro de série ou de lot particulier dans la base de données. Vous procédez à l’aide des fonctionnalités Traçabilité et Naviguer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 21eff2a2c52dfabb3788bb06d1d2f684c34441ce
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750020"
---
# <a name="trace-item-tracked-items"></a>Tracer des articles - Articles suivis
Vous pouvez voir où un article suivi a été utilisé, y compris le mode et le moment de réception ou de production, de transfert, de vente, de consommation ou de retour. Vous pouvez également rechercher toutes les instances d’informations d’un numéro de série ou de lot particulier dans la base de données. Vous procédez à l’aide des fonctionnalités Traçabilité et [Rechercher des écritures](ui-find-entries.md).  

Ces fonctions sont particulièrement utiles pour le contrôle qualité, lorsque vous devez déterminer quels clients ont reçus des produits correspondant à un numéro de lot particulier ou le lot dont provenait un composant défectueux.  

 Sur la page **Traçabilité**, vous pouvez effectuer une traçabilité en aval et en amont dans une série de mouvements de stock validés pour le numéro de lot ou de série.  

 Sur la page **Rechercher des écritures**, vous ne pouvez pas voir la séquence de transactions, mais vous pouvez afficher tous les enregistrements des numéros de série ou de lot, à la fois les écritures validées et les enregistrements ouverts.  

 Les deux fonctions peuvent être utilisées en association en transférant un numéro de série ou de lot suivi sur la page **Rechercher des écritures** pour terminer un scénario complet de suivi. Pour plus d’informations, voir [Procédure pas à pas : suivi des numéros de série et des numéros de lot](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Pour tracer des articles suivis  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Traçabilité**, puis sélectionnez le lien associé.  
2.  Dans les champs de filtre dans le haut de la page, entrez les numéros d’article spécifiques ou un filtre pour les numéros d’article que vous voulez suivre.  
3.  Dans le champ **Afficher composants**, indiquez si vous voulez également voir d’où provenaient les composants des articles. Les options disponibles dans ce champ sont les suivantes.  

    |Champ|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Non**|sélectionnez cette options si vous ne voulez voir aucun composant.|  
    |**Avec traçabilité uniquement**|sélectionnez cette option si vous ne voulez voir que les composants ayant des numéros de lot ou de série.|  
    |**Tout**|sélectionnez cette option si vous voulez voir tous les composants.|  

4.  Dans le champ **Méthode de suivi**, sélectionnez la méthode que vous voulez utiliser pour suivre l’article. Les options sont les suivantes  

    |Champ|Désignation|  
    |----------------------------------|---------------------------------------|  
    |**Utilisation->origine**|Cette méthode suit l’article à partir de l’endroit où il a été utilisé jusqu’à l’endroit d’où il vient. Par exemple, si un article fabriqué a été vendu à un client, la page **Traçabilité** présente ce dernier en montrant d’abord la ligne expédition vente, que vous pouvez développer pour voir l’ordre de fabrication dont il provenait.|  
    |**Origine->utilisation**|cette méthode suit l’article à partir de l’endroit dont il provient dans le stock jusqu’à l’endroit où il a été utilisé. Par exemple, si un article fabriqué a été vendu à un client, la page **Traçabilité** présente ce dernier en montrant d’abord l’ordre de fabrication terminé, que vous pouvez développer pour voir les lignes expédition vente où l’article a été utilisé.|  

5.  Sélectionnez l’action **Suivi** pour exécuter le suivi.  

> [!NOTE]  
>  Si vous avez reçu le même lot sur plusieurs transactions, la page **Traçabilité** peut ne pas afficher toutes les transactions. Seules les transactions lettrées sont indiquées.  

> [!NOTE]  
>  Si l’historique d’une transaction supplémentaire dans une ligne traçabilité a déjà été suivi par une autre ligne au-dessus de celle-ci, la case à cocher **Déjà tracé** est activée. Pour une vue plus simple, ces lignes sous-jacentes ne s’affichent pas.  
>   
>  Pour trouver les lignes traçabilité où l’historique des transactions a déjà été suivi, cliquez sur le bouton **Aller sur déjà tracé**. La ligne traçabilité en question est sélectionnée et toutes les lignes sous-jacentes sont développées.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Pour rechercher des articles suivis avec Rechercher des écritures  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Rechercher des écritures**, puis sélectionnez le lien associé.  
2. Choisissez **Actions** > **Rechercher par** > **Rechercher par référence d’article**.
3. Dans les champs **N° de série** et **N° lot**, entrez les numéros traçabilité que vous voulez suivre.  
4. Sélectionnez l’action **Rechercher** pour rechercher toutes les instances du numéro de série ou de lot dans la base de données.  

## <a name="see-also"></a>Voir aussi  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : traçabilité](design-details-item-tracking.md)
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
[Procédure pas à pas : suivi des numéros de série et des numéros de lot](walkthrough-tracing-serial-lot-numbers.md)  
[Rechercher des écritures](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]