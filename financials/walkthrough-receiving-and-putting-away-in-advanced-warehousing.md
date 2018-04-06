---
title: "Procédure pas à pas : Réception et rangement dans les configurations de stockage avancées | Microsoft Docs"
description: "Dans Finance and Operations, Business edition, les processus entrants de réception et de rangement peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 991256bf2737297710d25f5a25854f4803185fc3
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Procédure pas à pas : Réception et rangement dans les configurations de stockage avancées
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les processus entrants de réception et de rangement peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt.  

|Méthode|Processus entrant|Emplacements|Bons de réception|Rangements|Niveau de complexité (Voir [Détails de conception : paramètres entrepôt](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|X|||2|  
|B|Validation de la réception et du rangement à partir d'un document de rangement stock|||X|3|  
|C|Validation de la réception et du rangement à partir d'un document réception entrepôt||X||5/4/6|  
|J|Validation de la réception d'un document réception entrepôt et validation du rangement à partir d'un document de rangement entrepôt||X|X|5/4/6|  

Pour plus d'informations, reportez\-vous à [Détails de conception : flux d'enlogement](design-details-inbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode D dans la table précédente.  

## <a name="about-this-walkthrough"></a>À propos de cette procédure pas à pas  
Pour les configurations de stockage avancées, lorsqu'un magasin est défini pour exiger un traitement des réceptions en plus du traitement des réceptions, vous utilisez la fenêtre **Réception entrepôt** pour enregistrer et valider la réception d'articles sur plusieurs commandes entrantes. Lorsque la réception entrepôt est validée, un ou plusieurs documents rangement entrepôt sont créés pour indiquer aux magasiniers de prendre l'article reçu et de le placer aux emplacements affichés en fonction de la configuration de l'emplacement ou des autres emplacements. Le placement spécifique des articles est enregistré lorsque le rangement entrepôt est validé. Le document origine entrant peut être une commande achat, un retour vente, un enlogement transfert ou un ordre d'assemblage de fabrication dont la production est prête à être rangée. Si la réception est créée à partir d'une commande entrante, il est possible d'extraire plusieurs documents origine entrant pour la réception. Grâce à cette méthode, vous pouvez enregistrer plusieurs articles provenant de différentes commandes entrantes avec une réception.  

Cette procédure pas à pas présente les tâches suivantes.  

-   Configurez le magasin BLANC pour recevoir et ranger.  
-   Création et publication de deux commandes achat pour la gestion complète de l'entrepôt.  
-   Création et validation d'un document réception entrepôt pour plusieurs lignes commande achat de fournisseurs spécifiques.  
-   Enregistrement du rangement entrepôt pour les articles reçus.  

## <a name="roles"></a>Rôles  
Cette procédure pas à pas présente les tâches effectuées par les rôles utilisateur suivants :  

-   Gestionnaire d'entrepôt  
-   Agent d'achats  
-   Personnel de réception  
-   Magasinier  

## <a name="prerequisites"></a>Conditions préalables  
Pour exécuter ce processus pas à pas, vous devez :  

-   avoir CRONUS International Ltd. installé.  
-   Devenez magasinier dans un magasin BLANC en procédant comme suit :  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Salariés entrepôt**, puis sélectionnez le lien connexe.  
2.  Choisissez le champ **ID utilisateur** et sélectionnez votre propre compte utilisateur dans la fenêtre **Utilisateurs**.  
3.  Dans le champ **Code magasin**, entrez BLANC.  
4.  Sélectionnez le champ **Par défaut**.  

## <a name="story"></a>Scénario  
Ellen, responsable d'entrepôt chez CRONUS International Ltd., crée deux commandes achat pour des articles accessoires des fournisseurs 10000 et 20000 qui doivent être approvisionnées à l'entrepôt BLANC. Lorsque les livraisons arrivent à l'entrepôt, Sammy, qui est chargé de réceptionner les articles des fournisseurs 10000 et 20000, utilise un filtre pour créer des lignes réception pour les commandes achat provenant des deux fournisseurs. Sammy valide les articles comme étant reçus dans le stock dans une réception entrepôt et rend les articles disponibles pour la vente ou les autres demandes. Jean, le magasinier, prélève les articles depuis l'emplacement de réception et les range. Il range toutes les unités dans leurs emplacements par défaut, à l'exception de 40 des 100 charnières reçues, qu'il range dans le département d'assemblage en fractionnant la ligne rangement. Lorsque Jean enregistre le rangement, le contenu d'un emplacement est mis à jour et les articles sont rendus disponibles pour le prélèvement de l'entrepôt.  

## <a name="reviewing-the-white-location-setup"></a>Examen de la configuration du magasin BLANC  
La configuration de la fenêtre **Fiche magasin** définit les flux d'entrepôt de la société.  

### <a name="to-review-the-location-setup"></a>Examen du paramètre de magasin  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.  
2.  Ouvrez la fiche magasin BLANC.  
3.  Notez que sur le raccourci **Entrepôt**, la case à cocher **Prélèv. et rangement suggérés** est activée.  

    Cela signifie que le magasin est configuré pour le niveau de complexité le plus élevé, ce qui est indiqué par le fait que toutes les cases à cocher d'activité entrepôt sur le raccourci sont activées.  

4.  Notez sur le raccourci **Emplacements** que les emplacements sont indiqués dans le champ **Code empl. réception** et **Code empl. expédition**.  

Cela signifie que lorsque vous créez une réception entrepôt, ce code emplacement est copié dans l'en-tête du document réception entrepôt par défaut et les lignes des rangements entrepôt qui en résultent.  

## <a name="creating-the-purchase-orders"></a>Création des commandes achat  
Les commandes achat sont le type de document d'origine entrant le plus répandu.  

### <a name="to-create-the-purchase-orders"></a>Création des commandes achat  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes achat**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Créez une commande achat pour le fournisseur 10000 à la date de travail (23 janvier) comportant les lignes commande achat suivantes.  

    |Article ;|Code magasin|Quantité|  
    |----------|-------------------|--------------|  
    |70200|BLANC|100 PCS|  
    |70201|BLANC|50 PCS|  

    Informez l'entrepôt que la commande achat est prête pour l'activité entrepôt lorsque la livraison sera faire.  

4.  Sélectionnez l'action **Lancer**.  

    Créez la deuxième commande achat.  

5.  Sélectionnez l'action **Nouveau**.  
6.  Créez une commande achat pour le fournisseur 20000 à la date de travail comportant les lignes commande achat suivantes.  

    |Article ;|Code magasin|Quantité|  
    |----------|-------------------|--------------|  
    |70100|BLANC|10 BIDONS|  
    |70101|BLANC|12 BIDONS|  

    Sélectionnez l'action **Lancer**.  

    Les articles envoyés par les fournisseurs 10000 et 20000 sont arrivés à l'entrepôt BLANC. Sammy commence alors le processus de traitement des réceptions achat.  

## <a name="receiving-the-items"></a>Réception des articles  
Dans la fenêtre **Réception entrepôt**, vous pouvez gérer plusieurs commandes entrantes pour les documents d'origine, tel que des commandes achat.  

### <a name="to-receive-the-items"></a>Réception des articles  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Réceptions entrepôt**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Dans le champ **Code magasin**, entrez BLANC.  
4.  Choisissez l'action **Filtrer pour extr. doc. orig.**.  
5.  Dans le champ **Code**, entrez **ACCESSOIRE**.  
6.  Dans le champ **Désignation**, entrez **Fournisseurs 10000 et 20000**.  
7.  Sélectionnez l'option **Modifier**.  
8.  Dans le raccourci **Achats**, dans le champ **Filtre n° fournisseur**, entrez **10000&#124;20000**.  
9. Sélectionnez l'action **Exécuter**. La réception entrepôt est renseignée avec quatre lignes représentant les lignes commande achat pour les fournisseurs spécifiés. Le champ **Qté à recevoir** est renseigné parce que vous n'avez pas activé la case à cocher **Ne pas remplir qté à traiter** dans la fenêtre **Filtres pour extr. doc. orig.**.  
10. Éventuellement, si vous souhaitez utiliser un filtre en procédant de la manière décrite précédemment dans cette section, choisissez l'action **Extraire document origine**, puis sélectionnez les commandes achat des fournisseurs en question.  
11. Choisissez l'action **Valider réception**, puis cliquez sur le bouton **Oui**.  

    Des écritures comptables article positives sont créées et reflètent les réceptions achat validées d'accessoires des fournisseurs 10000 et 20000, et les articles sont prêts à être rangés dans l'entrepôt depuis l'emplacement de réception.  

## <a name="putting-the-items-away"></a>Rangement des articles  
Dans la fenêtre **Rangement entrepôt**, vous pouvez gérer les rangements pour un document réception entrepôt spécifique couvrant plusieurs documents origine. Comme pour tous les documents activité entrepôt, chaque article dans le rangement entrepôt est représenté par une ligne Prélever et une ligne Emplacement. Dans la procédure suivante, le code emplacement sur les lignes Prélever est l'emplacement de réception par défaut au magasin BLANC, W-08-0001.  

### <a name="to-put-the-items-away"></a>Rangement des articles  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Rangements**, puis sélectionnez le lien connexe.  
2.  Sélectionnez le seul document rangement entrepôt dans la liste, puis sous l'onglet **Accueil**, dans le groupe **Gérer**, sélectionnez **Modifier**.  

    Le document rangement entrepôt affiche un total de huit lignes Prélever ou Emplacement pour les quatre lignes commande achat.

    Il est indiqué au magasinier que 40 charnières doivent être amenées au département d'assemblage, et il procède à la répartition de la ligne Emplacement individuelle pour spécifier une seconde ligne Emplacement pour l'emplacement W-02-0001 dans le département d'assemblage, où il place cette partie des charnières reçues.  

3.  Sélectionnez la seconde ligne de la fenêtre **Rangement entrepôt**, la ligne d'emplacement pour l'article 70200.  
4.  Dans le champ **Qté à traiter**, changez la valeur 100 en 60.  
5.  Sur le raccourci **Lignes**, choisissez **Fonctions**, puis sélectionnez **Eclater ligne**. Une nouvelle ligne est insérée pour l'article 70200 et 40 est indiqué dans le champ **Qté à traiter**.  
6.  Dans le champ **Code emplacement**, entrez W-02-0001. Le champ **Code zone** est renseigné automatiquement.  

    Enregistrez le rangement.  

7.  Choisissez l'action **Enregistrer rangement**, puis cliquez sur le bouton **Oui**.  

    Les accessoires reçus sont ensuite rangés dans les emplacements par défaut des articles, et 40 charnières sont placées dans le département d'assemblage. Les articles reçus sont alors disponibles pour le prélèvement pour une demande interne, tel que des ordres d'assemblage, ou une demande externe, telles que des expéditions vente.  

## <a name="see-also"></a>Voir aussi  
 [Ranger des articles avec le rangement entrepôt](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Déplacer des articles dans les configurations de stockage avancées](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Détails de conception : flux d'enlogement](design-details-inbound-warehouse-flow.md)   
 [Procédure pas à pas : Réception et rangement dans les configurations de stockage de base](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)

