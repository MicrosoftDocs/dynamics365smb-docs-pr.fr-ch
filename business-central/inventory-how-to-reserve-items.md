---
title: "Procédure : réserver des articles | Microsoft Docs"
description: "Vous pouvez réserver des articles pour les commandes vente, les commandes achat et les ordres de fabrication. Vous pouvez réserver des articles en stock ou entrants sur les lignes document ouvertes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3f99d23f2e4a43aeb1face2f39dd6384ff672214
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="reserve-items"></a>Réserver des articles
Vous pouvez réserver des articles pour les commandes vente, les commandes service, les ordres d'assemblage et les ordres de fabrication. Vous pouvez réserver des articles en stock ou entrants sur les lignes document ou les lignes feuille ouvertes. Vous effectuez le travail dans la fenêtre **Réservation**.

Chaque ligne de la fenêtre **Réservation**, que vous ouvrez pour réserver des articles, donne des informations sur un type de ligne (vente, achat, feuille) ou d'écriture de stock. Les lignes décrivent le nombre d'articles disponibles pour réservation à partir de chaque type de ligne ou d'écriture.

## <a name="to-reserve-items-for-sales"></a>Pour réserver des articles pour des ventes
Ce qui suit décrit comment réserver des articles pour une commande vente. Les étapes sont similaires à celles des commandes achat, service et ordre d'assemblage.  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2.  Dans une commande vente, sur le raccourci **Lignes**, sélectionnez l'action **Réserver**. La fenêtre **Réservation** s'ouvre.  
3. sélectionnez la ligne à partir de laquelle vous souhaitez réserver des articles.  
4. Choisissez l'une des actions suivantes.  

    |**Fonction.**|**Description**|
    |------------------|---------------------|  
    |**Réservation automatique**|Permet de réserver automatiquement des articles dans la fenêtre **Réservation**.|  
    |**Réserver à partir de la ligne courante**|Permet de réserver des articles sur la ligne du document que vous avez sélectionnée.|  
    |**Annuler la réservation de la ligne courante**|Permet d'annuler la réservation d'articles sur la ligne du document que vous avez sélectionnée.|

> [!NOTE]  
>  Si des lignes traçabilité article existent pour la commande vente, le système de réservation vous fera suivre une procédure spéciale : Pour plus d'informations à ce sujet, consultez la rubrique « Pour réserver un numéro de série ou de lot particulier ».  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Pour réserver un article pour une ligne O.F.  
Vous pouvez réserver des articles pour des ordres de fabrication. Vous devez distinguer les lignes O.F., qui correspondant à l'article parent, des composants O.F.

La procédure suivante s'appuie sur un ordre de fabrication planifié ferme.   
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **O.F. planifié ferme**, puis sélectionnez le lien connexe.  
2. Ouvrez l'O.F. planifié ferme pour lequel vous souhaitez réserver des articles parents.  
3. Sélectionnez la ligne ordre de fabrication concernée.  
4. Sur le raccourci **Lignes**, choisissez l'action **Réserver**.
5. Dans la fenêtre **Réservation**, sélectionnez la ligne **Ligne vente, commande**, puis sélectionnez l'action **Réserver à partir de la ligne courante**.  

La quantité entrée dans la ligne O.F. planifié ferme est désormais réservée.

## <a name="to-reserve-items-for-production-order-components"></a>Pour réserver des articles pour des composants O.F.  
Vous pouvez réserver des articles pour des ordres de fabrication. Vous devez distinguer les lignes O.F., qui correspondant à l'article parent, des composants O.F.

La procédure suivante s'appuie sur un ordre de fabrication planifié ferme.    
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **O.F. planifié ferme**, puis sélectionnez le lien connexe.  
2. Ouvrez l'O.F. planifié ferme pour lequel vous souhaitez réserver des articles composant.  
3. Sélectionnez la ligne ordre de fabrication concernée.  
4. Sur le raccourci **Lignes**, choisissez **Ligne**, puis **Composants**.  
5. Sélectionnez la ligne de composant appropriée.  
6. Dans le raccourci **Lignes**, choisissez l'action **Réserver**.  
7. Dans la fenêtre **Réservation**, sélectionnez une ligne, puis sélectionnez l'action **Réserver à partir de la ligne courante**.  

La quantité entrée dans la ligne de composant production planifié ferme est désormais réservée.

## <a name="to-change-a-reservation"></a>Pour modifier une réservation  
Vous pouvez être parfois amené à modifier une réservation d'article.   
1. À partir de la ligne document à partir de laquelle vous avez fait la réservation, dans le raccourci **Lignes**, choisissez l'action **Réserver**.  
2. Dans la fenêtre **Réservation**, choisissez l'action **Écritures réservation**.
3. Dans la fenêtre **Écritures réservation**, mettez à jour le champ **Quantité** de la ligne à modifier.
4. Confirmez le message qui suit en cliquant sur le bouton **OK**.

## <a name="to-cancel-a-reservation"></a>Pour annuler des réservations  
Vous pouvez parfois avoir à annuler une réservation d'article.   
1. À partir de la ligne document à partir de laquelle vous souhaitez annuler une réservation, dans le raccourci **Lignes**, choisissez l'action **Réserver**.  
2. Dans la fenêtre **Réservation**, choisissez l'action **Écritures réservation**.  
3.  Dans la fenêtre **Réservation**, choisissez l'action **Annuler la réservation**.  
4.  Confirmez le message qui suit en cliquant sur le bouton **OK**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Pour réserver un numéro de série ou de lot particulier  
À partir des documents sortants pour les articles suivis, comme des commandes vente ou des listes de composants de production, vous pouvez réserver des numéros de série ou de lot spécifiques. Ceci peut s'avérer utile, par exemple, si vous avez besoin des composants de production d'un lot spécifique pour assurer une cohérence avec des lots de production précédents, ou parce qu'un client demande un numéro de série particulier. Pour plus d'informations, voir [Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md).

Il s'agit d'une réservation spécifique, parce que vous réservez à partir de la quantité de l'article X qui appartient au Lot X. Si vous réservez seulement à partir des quantités de l'article X, la réservation est normale, non spécifique. Pour plus d'informations, reportez-vous à [Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md).

La procédure suivante se base sur une commande vente.    
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2. Créez une ligne commande vente d'un article suivi.  
3. Affectez des numéros de série et de lot à la ligne commande vente. Pour plus d'informations, voir [Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md).
4. Sur la ligne commande vente, sélectionnez l'action **Réserver**.  
5. Choisissez le bouton **Oui** pour réserver des numéros de série ou de lot spécifiques.  
6. Dans la fenêtre **Liste traçabilité**, sélectionnez la combinaison de numéros de série et de lot que vous venez d'affecter.  
7. Choisissez le bouton **OK** pour ouvrir une fenêtre **Réservation** affichant uniquement l'approvisionnement portant le numéro de traçabilité spécifié. S'il y a des réservations non spécifiques sur l'un des numéros traçabilité que vous avez spécifiés pour cette ligne, vous êtes informé que la quantité a déjà été réservée.  
8. Sélectionnez l'action **Réservation automatique** ou **Réserver à partir de la ligne courante** pour créer la réservation sur les numéros traçabilité spécifiques.

## <a name="see-also"></a>Voir aussi
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : réservation, chaînage et message d'action](design-details-reservation-order-tracking-and-action-messaging.md)  
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

