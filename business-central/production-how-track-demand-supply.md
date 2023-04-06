---
title: Suivre les relations entre l’offre et la demande
description: 'Cette rubrique explique les différentes manières de suivre les relations entre la demande et l’offre, telles que le suivi des articles associés et le traitement des éléments de planning non suivis.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5830, 9101, 99000822, 99000855'
ms.date: 06/25/2021
ms.author: edupont
---
# Suivre les relations entre l’offre et la demande

À partir d’un document d’offre ou de demande dans le réseau d’ordres, vous pouvez suivre la demande de commande (quantité chaînée), les prévisions, les commandes ouvertes vente ou les paramètres de planification (quantité non chaînée) qui ont donné lieu à la ligne planning en question.

Les feuilles planning incluent également des informations de planification sur les entités sans rapport avec les commandes pour aider le gestionnaire à obtenir un programme d’approvisionnement optimal. Pour plus d’informations, voir [Éléments planning non chaînés](production-how-track-demand-supply.md#untracked-planning-elements).

## Pour chaîner des articles liés
Par l’intermédiaire des systèmes de planification et de réservation, le chaînage montre le lien entre les commandes vente, les ordres de fabrication et les commandes achat.

La procédure suivante décrit comment chaîner des articles liés sur un ordre de fabrication planifié ferme. La procédure est similaire pour tous les autres types de commande, et à partir des lignes feuille planning.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifié ferme**, puis sélectionnez le lien associé.
2. Ouvrez l’O.F. planifié ferme approprié dans la liste.
3. Sur le raccourci **Lignes**, choisissez l’action **Fonctions**, puis l’action **Chaînage**.

Les lignes de la fenêtre **Chaînage** affichent les documents liés à la ligne de l’ordre de fabrication en cours.

## Éléments planning non chaînés
La page **Éléments planning non chaînés** s’affiche lorsque vous cliquez sur le champ **Qté non chaînée** sur la page **Planification commande**. Elle a deux objectifs :

1. Stockage d’informations sur les quantités non chaînées qui s’affichent lorsque l’utilisateur affiche la page Chaînage.
2. Stockage des messages d’avertissement qui s’affichent lorsque l’utilisateur clique sur l’icône **Avertissement** sur la page **Feuille planning**.

la page inclut les écritures représentant une quantité excédentaire non chaînée du réseau de chaînage. Ces écritures sont générées au cours de l’exécution de la planification et expliquent la provenance de la quantité excédentaire non chaînée des lignes chaînage. Cet excédent non chaîné peut provenir des lignes suivantes :

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

## Voir aussi  
[Planifié](production-planning.md)   
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : réservation, chaînage et message d’action](design-details-reservation-order-tracking-and-action-messaging.md)  
[Détails de conception : planification de l’approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l’approvisionnement](setup-best-practices-supply-planning.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]