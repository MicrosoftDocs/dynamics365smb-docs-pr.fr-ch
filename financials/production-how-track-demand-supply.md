---
title: "Procédure de suivi des relations entre l'offre et la demande | Microsoft Docs"
description: "À partir d'un document d'offre ou de demande dans le réseau d'ordres, vous pouvez suivre la demande de commande (quantité chaînée), les prévisions, les commandes ouvertes vente ou les paramètres de planification (quantité non chaînée) qui ont donné lieu à la ligne planning en question."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8c53878418592daf9179d6864da4447ca8ad1262
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="track-relations-between-demand-and-supply"></a>Suivre les relations entre l'offre et la demande
À partir d'un document d'offre ou de demande dans le réseau d'ordres, vous pouvez suivre la demande de commande (quantité chaînée), les prévisions, les commandes ouvertes vente ou les paramètres de planification (quantité non chaînée) qui ont donné lieu à la ligne planning en question.

Les feuilles planning incluent également des informations de planification sur les entités sans rapport avec les commandes pour aider le gestionnaire à obtenir un programme d'approvisionnement optimal. Pour plus d'informations, voir la section « Éléments planning non chaînés ».

## <a name="to-track-linked-items"></a>Pour chaîner des articles liés
Par l'intermédiaire des systèmes de planification et de réservation, le chaînage montre le lien entre les commandes vente, les ordres de fabrication et les commandes achat.

La procédure suivante décrit comment chaîner des articles liés sur un ordre de fabrication planifié ferme. La procédure est similaire pour tous les autres types de commande, et à partir des lignes feuille planning.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **O.F. planifié ferme**, puis sélectionnez le lien connexe.
2. Ouvrez l'O.F. planifié ferme approprié dans la liste.
3. Sur le raccourci **Lignes**, choisissez l'action **Fonctions**, puis l'action **Chaînage**.

Les lignes de la fenêtre **Chaînage** affichent les documents liés à la ligne de l'ordre de fabrication en cours.

## <a name="untracked-planning-elements"></a>Éléments planning non chaînés
La fenêtre **Éléments planning non chaînés** s'affiche lorsque vous cliquez sur le champ **Qté non chaînée** dans la fenêtre **Planification commande**. Elle a deux objectifs :

1. Stockage d'informations sur les quantités non chaînées qui s'affichent lorsque l'utilisateur affiche la fenêtre Chaînage.
2. Stockage des messages d'avertissement qui s'affichent lorsque l'utilisateur clique sur l'icône **Avertissement** dans la fenêtre **Feuille planning**.

La fenêtre inclut les écritures représentant une quantité excédentaire non chaînée du réseau de chaînage. Ces écritures sont générées au cours de l'exécution de la planification et expliquent la provenance de la quantité excédentaire non chaînée des lignes chaînage. Cet excédent non chaîné peut provenir des lignes suivantes :

- Prévisions production ;
- Commandes ouvertes ;
- Stock de sécurité ;
- Point de commande ;
- Stock maximum ;
- Quantité de réappro. ;
- Qté maximum commande ;
- Qté minimum commande ;
- Commandé par ;
- Seuil (% taille lot).

## <a name="see-also"></a>Voir aussi  
[Planifié](production-planning.md)   
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : réservation, chaînage et message d'action](design-details-reservation-order-tracking-and-action-messaging.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

