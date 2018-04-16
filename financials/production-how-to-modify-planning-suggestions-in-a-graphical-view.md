---
title: "Procédure de modification des propositions planning dans une vue graphique | Microsoft Docs"
description: "Une activité de planification courante est d'ajouter ou de modifier les lignes feuille planning pour modifier les commandes approvisionnement proposées avant de les valider en exécutant la fonction **Traiter message d'action**. Une alternative à utiliser la feuille planning est d'utiliser une vue graphique."
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
ms.openlocfilehash: 9217d8707ab65d231a6759e86f6f2b2866835bb8
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="modify-planning-suggestions-in-a-graphical-view"></a>Modifier les propositions planning dans une vue graphique
Une activité de planification courante est d'ajouter ou de modifier les lignes feuille planning pour modifier les commandes approvisionnement proposées avant de les valider en exécutant la fonction **Traiter message d'action**. Une alternative à utiliser la feuille planning est d'utiliser une vue graphique.

Dans la fenêtre **Disponibilité article par chronologie**, vous pouvez modifier certaines commandes approvisionnement et suggestions en faisant glisser les articles le long de l'axe des abscisses pour modifier la quantité ou le long de l'axe des ordonnées pour modifier la date d'échéance.  

 Dans la fenêtre **Disponibilité article par chronologie** et la fenêtre **Feuille planning**, vous pouvez apporter des modifications suivantes :  

-   Modifier une commande approvisionnement suggérée existant uniquement comme une ligne planning.  
-   Modifier une commande approvisionnement existante que le système de planification suggère de changer.  
-   Créer une commande approvisionnement suggérée et la modifier.  

Pour plus d'informations sur les types de ligne de planification qui sont indiqués, reportez-vous au champ Description du raccourci **Modification des événements**.  

Lorsque vous choisissez **Enregistrer les modifications** dans la fenêtre **Disponibilité article par chronologie**, les modifications apportées sont copiées dans la feuille planning ou la demande achat. Vous pouvez à présent les appliquer à l'aide de la fonction **Traiter msg. action - Planning**.  

La procédure suivante indique comment modifier des propositions d'approvisionnement par glisser-déplacer. Vous pouvez également modifier les champs **Date d'échéance** et **Quantité** sur le raccourci **Modification des événements** et immédiatement visualiser les modifications graphiquement sur le raccourci **Chronologie** de la fenêtre **Feuille planning**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Pour modifier les commandes approvisionnement proposées dans la vue graphique  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Disponibilité article par chronologie**, puis sélectionnez le lien connexe.  

    La fenêtre **Disponibilité article par chronologie** s'ouvre avec le numéro d'article, le magasin et la variante de l'article, figurant sur la ligne planning sélectionnée, préalablement insérés dans le raccourci **Options**. Le raccourci **Chronologie** affiche une représentation graphique du stock prévisionnel de l'article, y compris les propositions planning.  

2.  Assurez-vous que le champ **Inclure propositions planning** est sélectionné.  
3.  Sélectionnez la commande approvisionnement suggérée à modifier. Vous pouvez identifier les éléments modifiables par le cercle vert et l'icône représentant un disque. Pour plus d'informations sur les différents symboles, voir la section « Symboles et icônes sur le raccourci Chronologie ».  
4.  Placez le pointeur sur le cercle vert jusqu'à ce qu'il s'agrandisse et le pointeur prend la forme Déplacement (quatre flèches).  
5.  Appuyez sur et maintenez enfoncé le bouton de la souris lorsque vous faites glisser le pointeur vers le haut ou le bas pour modifier la quantité. Appuyez sur et maintenez enfoncé le bouton de la souris lorsque vous faites glisser le pointeur à gauche ou à droite pour modifier la date d'échéance.  
6.  Outre le déplacement d'éléments par glisser-déplacer, vous pouvez modifier les propositions planning à l'aide d'un certain nombre d'options de menu déroulant. Accédez au menu déroulant associé au cercle vert d'un élément d'approvisionnement proposé et sélectionnez l'une des fonctions suivantes  

    |Fonction|Désignation|  
    |--------------|---------------------------------------|  
    |**Créer un approvisionnement**|Crée un nouvel élément au point où vous accédez au menu déroulant, qui représente une commande approvisionnement suggérée. Il devient une nouvelle ligne de la feuille planning lorsque vous choisissez **Enregistrer les modifications**.<br /><br /> **REMARQUE :** si les champs **Filtre magasin** ou **Filtre variante** sur le raccourci **Options** sont vides ou ont plusieurs valeur de filtre, le nouvel approvisionnement est créé et validé ultérieurement à la planification ou sur la feuille demande d'achat avec les codes suivants :<br /><br /> * Si le champ filtre est vide, le nouvel approvisionnement est créé sans magasin ou code variante.<br /><br /> * Si plusieurs valeurs de filtre sont définies, le nouvel approvisionnement est créé pour la première valeur du filtre en fonction de la méthode de tri.<br /><br /> Si vous souhaitez utiliser un autre code variante ou magasin, vous devez manuellement le modifier sur la ligne planning.|  
    |**Ajuster automatiquement l'approvisionnement**|Optimise un nouvel approvisionnement que vous avez créé dans le graphique en vérifiant qu'il est de stock zéro avant l'approvisionnement suivant.|  
    |**Supprimer l'approvisionnement**|Supprime l'élément dans le raccourci **Chronologie** puis supprime la ligne planning lorsque vous choisissez **Enregistrer les modifications**. L'icône prend la forme d'un disque avec une croix rouge lorsque l'approvisionnement a été supprimé.<br /><br /> **REMARQUE :** Vous ne pouvez supprimer un approvisionnement que si son message d'action est de type **Nouveau**. Une fois que vous avez sélectionné **Enregistrer les modifications**, vous devez supprimer manuellement la ligne planning en question la feuille planning ou demande achat.|  

7.  Choisissez l'action **Recharger** si vous voulez réinitialiser toutes les modifications apportées après avoir ouvert pour la dernière fois la fenêtre **Disponibilité article par chronologie**, ou sélectionnez **Recharger**.  
8. Lorsque les éléments sont stockés où vous le souhaitez dans le schéma, sélectionnez **Enregistrer les modifications** pour copier la quantité et la date modifiées dans la feuille planning ou demande achat représentant les éléments graphiques.  

Pour appliquer les modifications du programme d'approvisionnement, vous devez suivre les messages d'action qui en résultent de la feuille planning ou demande achat. Pour plus d'informations, voir Traiter msg. action - Planning.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symboles et icônes sur le raccourci Chronologie

 |Symbole/icône|Désignation|  
 |------------------|---------------------------------------|  
 |Commandes avec|une croix noire (offre et demande).<br /><br /> -   Modification impossible.<br />-   Visible lorsque le champ **Afficher le stock prévisionnel** est sélectionné (graphique orange).|  
 |Cercle rouge|Commandes approvisionnement existantes qui ne sont pas dans les propositions planning.<br /><br /> -   Modification impossible.<br />-   Visible lorsque le champ **Afficher le stock prévisionnel** est sélectionné (graphique orange).|  
 |Étoile jaune|Demande prévue.<br /><br /> -   Modification impossible.<br />-   Visible lorsque le champ **Nom prévision** a une valeur.<br /><br /> Lorsque les champs **Afficher le stock prévisionnel** et **Inclure propositions planning** sont sélectionnés, chaque étoile jaune possède un homologue lié dans le graphique opposé. Cela illustre la manière dont un approvisionnement proposé répond à la demande prévue.|  
 |Cercle vert avec une icône en forme de disque avec une croix rouge|Commande approvisionnement suggérée avec le message d'action *Annuler*.<br /><br /> -   Modification impossible.<br />-   Visible lorsque le champ **Inclure propositions planning** est sélectionné (graphique vert).|  
 |Cercle vert avec une icône en forme de disque avec une étoile|Commandes approvisionnement suggérées avec le message d'action *Nouveau*.<br /><br /> -   Modification possible.<br />-   Visible lorsque le champ **Inclure propositions planning** est sélectionné (graphique vert).|  
 |Cercle vert avec une icône en forme de disque avec une ou deux flèches|Commandes approvisionnement proposées avec le message d'action *Replanifier*, *Changer qté*, ou *Replan. et changer qté*<br /><br /> -   Modification possible.<br />-   Visible lorsque le champ **Inclure propositions planning** est sélectionné (graphique vert).<br /><br /> Les flèches reflètent la direction de la proposition planning. Par exemple, une flèche gauche conjointement à une flèche vers le haut indique un message d'action *Replanifier & changer qté* qui consiste à replanifier en amont et à augmenter la quantité.|  

Lorsque vous accédez au menu déroulant du raccourci **Chronologie**, les fonctions suivantes s'affichent en fonction de votre choix  

 |Fonction|Désignation|  
 |--------------|---------------------------------------|  
 |**Créer un approvisionnement**|Crée un nouvel élément sur le point où vous accédez au menu déroulant, qui représente une commande approvisionnement suggérée. Elle devient une nouvelle ligne de la feuille planning lorsque vous choisissez **Enregistrer les modifications** sur l'onglet **Processus**.<br /><br /> Toutes les valeurs de filtre qui sont définies dans les champs **Filtre magasin** ou **Filtre variante** dans le raccourci **Options** seront appliquées à la nouvelle commande d'approvisionnement. **Note :** si les champs de filtre sont vides ou ont plusieurs valeur de filtre, la commande approvisionnement est créée à l'aide des codes suivants : <ul><li>Si le champ filtre est vide, le nouvel approvisionnement est créé sans magasin ou code variante.</li><li>Si plusieurs valeur de filtre sont définies, le nouvel approvisionnement est créé à l'aide de la première valeur du filtre en fonction de l'ordre de tri.</li></ul> Si vous souhaitez utiliser un autre code variante ou magasin dans la nouvelle commande approvisionnement, vous devez le modifier manuellement sur la nouvelle ligne planning.|  
 |**Ajuster automatiquement l'approvisionnement**|Optimise un nouvel approvisionnement que vous avez créé dans le graphique en vérifiant qu'il crée un stock zéro avant l'approvisionnement suivant.|  
 |**Supprimer l'approvisionnement**|Supprime l'élément dans le raccourci **Chronologie** puis supprime la ligne planning lorsque vous choisissez **Enregistrer les modifications** sous l'onglet **Processus**. L'icône se change en disque avec une croix rouge lorsque l'approvisionnement est supprimé. **Note :** vous ne pouvez supprimer un approvisionnement que si son message d'action est de type *Nouveau*. Une fois que vous avez sélectionné **Enregistrer les modifications** sous l'onglet **Processus**, vous devez supprimer manuellement la ligne planning en question dans la feuille planning ou demande achat.|  
 |**Afficher document**|Ouvre la commande, la ligne planning ou la prévision que l'élément représente.|  
 |**Zoom arrière (Ctrl++)**|Agrandit l'échelle de l'axe X, de façon à afficher moins de jours. **Remarque** : vous pouvez également effectuer cette opération en appuyant sur Ctrl + la molette de défilement de la souris.|  
 |**zoom avant (Ctrl+-)**|Réduit l'échelle de l'axe X, de façon à afficher plus de jours. **Remarque** : vous pouvez également effectuer cette opération en appuyant sur Ctrl + la molette de défilement de la souris.|  
 |**Réinitialiser le zoom (Ctrl+0)**|Remet l'échelle de l'axe X à celle utilisée avant de zoomer.|  

Outre les actions de clavier qui ont été citées précédemment, vous pouvez également utiliser les actions de clavier suivantes dans le raccourci **Chronologie**.  

 |Action de clavier|Désignation|  
 |---------------------|---------------------------------------|  
 |CTRL + molette de défilement de la souris|Modifie l'échelle de l'axe X.|  
 |Sélectionnez un élément, puis appuyez sur Maj+Flèche|Déplace l'élément dans la direction de la touche flèche utilisée.|  
 |Tab|Déplace à l'élément suivant.|  
 |MAJ+Tab|Déplace à l'élément précédent.|  
 |Lors du déplacement d'un élément, appuyez sur la touche Échap.|Annule le déplacement. **Note :** ne fonctionne pas si vous avez relâché le bouton de la souris.|

## <a name="see-also"></a>Voir aussi  
[Planifié](production-planning.md)   
[Paramétrage de la production](production-configure-production-processes.md)  
[Production](production-manage-manufacturing.md)    
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md)   
[Pratiques de configuration recommandées : planification de l'approvisionnement](setup-best-practices-supply-planning.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

