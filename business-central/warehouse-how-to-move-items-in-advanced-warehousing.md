---
title: Dé&placer des articles dans des entrepôts qui utilisent le prélèvement et le rangement dirigés
description: Cet article explique comment déplacer des articles dans des magasins qui utilisent le rangement et le prélèvement dirigés.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
ms.service: dynamics-365-business-central
---

# Déplacer des articles dans les configurations entrepôt avancées qui utilisent le prélèvement et le rangement dirigés

Vous pouvez déplacer des articles entre emplacements sans demande d’un document origine. Par exemple, vous voudrez peut-être le faire dans le cadre des activités suivantes :

* Réorganiser votre entrepôt.
* Apporter des articles à une zone d’inspection.
* Sortir temporairement des articles des emplacements de prélèvement entrepôt, peut-être pour les utiliser dans un show-room.
* Déplacer des articles excédentaires vers la zone de production pour les composants configurés avec certaines méthodes de consommation.
* Déplacer les articles produits ou assemblés de la zone de production ou d’assemblage vers l’entrepôt.
* Déplacer des articles de la zone de stockage en vrac vers des emplacements utilisés pour le prélèvement.

Le mode de prélèvement des articles dépend de la configuration de l’entrepôt en tant que magasin. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Dans les configurations d’entrepôt où le bouton à bascule **Prélèvement et rangement dirigés** est activé pour les magasins, vous pouvez enregistrer des mouvements non planifiés sur les pages suivantes :  

* Feuille mouvement
* Prélèvement entrepôt interne
* Rangement entrepôt interne
* Feuilles reclassement entrepôt

Les pages **Feuille mouvement**, **Prélèvement entrepôt interne** et **Rangement entrepôt interne** fonctionnent de la même manière. Utilisez les pages pour préparer les activités d’entrepôt pour les magasiniers. La différence réside dans les fonctionnalités avancées associées à chaque page et dans les différents types d’activités entrepôt qui sont probablement effectuées par différents employés :

* La feuille mouvement vous permet de remplir les emplacements de prélèvement de haut rang avec des articles provenant d’autres emplacements
* Les rangements utilisent des modèles de rangement
* Le prélèvement utilise le classement et la disponibilité des emplacements

## Feuille mouvements entrepôt

### Pour déplacer des articles avec la feuille mouvement entrepôt

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille mouvement**, puis choisissez le lien associé.  
2. Remplissez manuellement les champs des lignes de la feuille ou utilisez l’une des actions suivantes pour remplir automatiquement les lignes :

    * **Extraire contenu emplacement** remplit les lignes de la feuille avec le contenu du ou des emplacements que vous spécifiez.
    * **Calculer réappro. emplacement** utilise les priorités emplacement pour suggérer le réapprovisionnement des emplacements les mieux classés à partir de ceux les moins bien classés.

    > [!NOTE]  
    > Si l’article répond aux critères de la liste ci-dessous, les champs **Zone provenance** et **Emplacement provenance** seront vides. [!INCLUDE [prod_short](includes/prod_short.md)] calcule d’où déplacer les articles uniquement lorsque vous utilisez l’action **Créer mouvement**.  
    >  
    > * L’article a une date de péremption.  
    > * Le bouton à bascule **Prélèvement selon FEFO** est activé pour l’emplacement.  
    > * Vous utilisez la fonction **Calculer réappro. emplacement**.  

3. Choisissez l’action **Créer mouvement** pour créer le mouvement. Une fois le mouvement terminé, vous pouvez l’enregistrer.  

### Pour enregistrer le mouvement d’entrepôt

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mouvements**, puis sélectionnez le lien associé.  
2. Ouvrez le document de mouvement pour l’enregistrer.  
3. Sur les lignes **Placer**,spécifiez où, quoi et quand déplacer l’article en choisissant les valeurs dans les champs **Code zone**, **Code emplacement**, **Qté à traiter** ou **Date d’échéance**.  
4. Sur les lignes **Prendre**, dans le champ **Qté à traiter**, spécifiez la quantité du contenu emplacement que vous souhaitez déplacer. Vous ne pouvez modifier ce champ que sur les lignes **Prendre**. 

    > [!NOTE]
    > Si vous devez prélever ou placer les articles d’une ligne dans plusieurs emplacements, notamment parce que l’emplacement indiqué est plein, utilisez l’action **Eclater ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.
 
5. Pour enregistrer toutes les quantités proposées comme spécifiées dans le champ **Quantité**, choisissez l’action **Renseigner automatiquement la quantité à traiter**.  
6. Sélectionnez l’action **Enregistrer**.  

> [!NOTE]  
> Pour les emplacements qui utilisent le rangement et le prélèvement dirigés, vous ne pouvez pas déplacer manuellement les articles dans des emplacements de type **RÉCEPTION** car ils ne sont pas encore considérés comme du stock disponible. Vous devez ranger les articles dans ces emplacements avant qu’ils ne soient disponibles pour les mouvements.

## Prélèvement interne  

### Pour créer un prélèvement interne  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvement interne entrepôt**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.
3. Renseignez le champ **N°** le champ **Code magasin** et le champ **Du code emplacement** du raccourci **Général**. Le champ **Du code emplacement** indique où placer les articles prélevés. Pour des raisons de fabrication, cet emplacement représente l’emplacement enlogement ou l’emplacement atelier ouvert. Pour d’autres applications, vous devez choisir un code emplacement d’un type emplacement qui n’est pas utilisé pour le prélèvement (par exemple, un emplacement affectation, expédition ou un emplacement spécial).  
4. Sélectionnez un article dans le champ **N° article**, puis renseignez les quantités à prélever.  
5. Choisissez l’action **Créer prélèvement**. Une instruction prélèvement entrepôt est maintenant créée pour un magasinier. Vous pouvez également choisir l’action **Lancer** et créer des prélèvements entrepôt à l’aide de la page **Feuille prélèvement**. Pour plus d’informations sur les feuilles prélèvement, consultez [Créer des documents de prélèvement en bloc avec la feuille prélèvement](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Une fois le prélèvement terminé, vous pouvez l’enregistrer.  

### Pour enregistrer le prélèvement d’entrepôt

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements**, puis choisissez le lien associé.  

    Pour travailler à un prélèvement particulier, sélectionnez-le dans la liste ou filtrez cette dernière afin de trouver les prélèvements qui vous ont été affectés.  
2. Si le champ **ID utilisateur affecté** est vide, entrez votre ID pour vous identifier, si nécessaire.  
3. Prélevez les articles.  

    Comme l’entrepôt est configuré pour utiliser le rangement et le prélèvement dirigés, le classement des emplacements détermine les emplacements pour le prélèvement. Les emplacements sont suggérés sur les lignes prélèvement. Les instructions contiennent au moins deux lignes distinctes pour les actions Prendre et Placer.  

4. Après avoir prélevé et placé les articles dans la zone ou l’emplacement d’expédition, choisissez l’action **Enregistrer prélèvement**.  

## Rangement interne  

### Pour créer un rangement interne  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangements internes entrepôt**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.
3. Renseignez le champ **N°** et le **Code magasin**.
4. Renseignez une ligne pour chaque article à déplacer vers l’entrepôt. Les champs **N° article** et **Quantité** sont obligatoires.

    > [!NOTE]  
    > Lorsque vous sélectionnez un article dans le champ **N° article**, la page **Contenus emplacement** s’ouvre à la place de la page **Articles**. Cette page s"ouvre parce que vous rangez un article qui se trouve affecté à un emplacement particulier, le *contenu d’un emplacement* et pas uniquement un article, et vous connaissez déjà l’emplacement dans lequel l’article doit être prélevé. Si vous avez rempli le champ **Code emplacement de provenance**, le contenu de l’emplacement sera filtré par cette valeur.

5. Pour compléter les lignes en y indiquant l’ensemble du contenu emplacement ou le contenu filtré des emplacements du magasin, choisissez l’action **Extraire contenu emplacement**.  
6. Choisissez l’action **Créer rangement**. Une instruction rangement entrepôt est maintenant créée pour un magasinier. Vous pouvez également choisir l’action **Lancer** pour créer des rangements entrepôt à l’aide de la page **Feuille rangement**. Pour plus d’informations sur les feuilles rangement, consultez [Créer des documents de rangement en bloc avec la feuille rangement](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Une fois le rangement terminé, vous pouvez l’enregistrer.  

### Pour enregistrer le rangement entrepôt

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Rangements**, puis sélectionnez le lien associé.
2. Ouvrez le rangement entrepôt qui est prêt à être traité.  
3. Si nécessaire, saisissez votre ID utilisateur lorsque vous commencez à travailler sur un rangement.  

    Pour optimiser le processus de rangement, vous pouvez trier les lignes de rangement selon différents critères. Par exemple, par article, numéro de rayon ou date d’échéance.

    * Si les lignes Prendre et Placer de chaque ligne réception ne se suivent pas directement et que vous souhaitez qu’elles se suivent, triez-les en sélectionnant **Article** dans le champ **Méthode de tri**.  
    * Si les classements des emplacements reflètent la disposition physique de l’entrepôt, utilisez la méthode de tri **Priorité emplacement** pour organiser le travail autour des emplacements.  

4. Réalisez le rangement.

    Chaque ligne de rangement interne donne lieu à deux lignes au moins dans le rangement entrepôt.  

    * la première ligne, correspondant au champ **Type action** **Prélèvement**, indique l’endroit où se trouvent les articles dans la zone de réception. Vous ne pouvez pas modifier la zone et l’emplacement de cette ligne.  
    * La ligne suivante, avec **Placer** dans le champ **Type d’action**, indique l’endroit où placer les articles dans l’entrepôt. Si vous recevez un grand nombre d’articles sur une ligne réception, vous devrez peut-être ranger les articles dans plusieurs emplacements, pour qu’il y ait une ligne Placer pour chaque emplacement.  

5. Après avoir placé tous les articles dans des emplacements selon les instructions, choisissez l’action **Enregistrer rangement**.  

## Pour enregistrer un mouvement qui a déjà eu lieu

Si vous devez enregistrer le fait que des articles ont déjà été déplacés vers d’autres emplacements sans rangement, prélèvement ou mouvement, vous pouvez utiliser la page **Feuille reclassement entrepôt** pour enregistrer le mouvement.

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille reclassement entrepôt**, puis sélectionnez le lien associé.  
2. Renseignez les champs **N° article**, **Du code zone**, **Du code emplacement**, **Vers code zone** et **Du code emplacement**.  
3. Sélectionnez l’action **Enregistrer**.  

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
