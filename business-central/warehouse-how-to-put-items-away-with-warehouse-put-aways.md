---
title: Comment ranger des articles avec le rangement entrepôt
description: Découvrez les différentes manières d’utiliser les rangements entrepôt pour ranger les articles reçus.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# Ranger des articles avec le rangement entrepôt

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous recevez des articles et les rangez en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus entrant|Réceptions requises|Rangements requis|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation de la réception et du rangement à partir d’un document de rangement stock||Activé|De base : commande par commande.|  
|A|Validation de la réception et du rangement à partir d’un document réception entrepôt|Activé||De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation de la réception d’un document réception entrepôt et validation du rangement à partir d’un document de rangement entrepôt|Activé|Activé|Avancé|  

Learn more at [Flux d’enlogement](design-details-inbound-warehouse-flow.md).

Cet article fait référence à la méthode D dans le tableau et suppose que la réception a déjà eu lieu. Learn more at [Réceptionner des articles](warehouse-how-receive-items.md).

Lorsqu’un magasin est configuré pour appeler un traitement de rangement entrepôt et un traitement de réception entrepôt, utilisez un document rangement entrepôt pour contrôler le rangement des articles. Lorsque vous validez une réception entrepôt, les documents origine tels que les commandes achat, les transferts entrant ou les retour vente sont mis à jour. La quantité reçue est validée dans le registre des articles et les lignes des articles reçus sont envoyées à la fonction de rangement dans l’entrepôt.

En fonction de la valeur du champ **Utiliser feuille rangement** de la **Fiche magasin**, les lignes sont soit rendues disponibles pour la feuille rangement, soit utilisées pour générer immédiatement des documents rangement. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

Outre les méthodes standard pour créer les rangements entrepôt qui sont décrits dans cet article, vous pouvez créer des rangements à partir de la réception entrepôt validée associée. Cela est utile si vous avez supprimé des lignes rangement ou si vous décidez de ne pas utiliser la feuille rangement, car vous pouvez créer ou recréer des instructions de rangement à partir des lignes réception validées.

## Codes zone et emplacement

Dans les magasins configurés pour utiliser le rangement et le prélèvement dirigés, les paramètres suivants sont requis pour déterminer le meilleur endroit pour ranger les articles :  

* Un modèle de rangement est configuré. Learn more at [Configurer des modèles rangement](warehouse-how-to-set-up-put-away-templates.md).  
* Le poids, le cubage et les exigences particulières de stockage de l’article ou du point de stock sont définis.
* La capacité, le type et le classement des emplacements sont définis pour les emplacements.  

La priorité emplacement est prise en compte lorsque plusieurs emplacements correspondent aux critères du modèle rangement. Si les critères du modèle rangement et la priorité emplacement coïncident pour plusieurs emplacements, l’emplacement dont le numéro est le plus élevé est alors sélectionné.

## Pour créer des documents rangement en bloc avec la feuille rangement  

Vous pouvez créer des documents rangement pour plusieurs réceptions en même temps sur la page **Feuille rangement**.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles rangement**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Extraire documents entrepôt**. La page **Sélection rangement** s’ouvre.  

    La liste contient toutes les réceptions validées qui sont prêtes à être rangées, y compris celles pour lesquelles des instructions de rangement ont déjà été créées. Les documents dont les lignes rangement ont été entièrement rangées et enregistrées n’apparaissent pas dans cette liste.  
3. Sélectionnez les documents que vous souhaitez utiliser. Vous pouvez utiliser simultanément des lignes de plusieurs documents.  

    > [!NOTE]  
    >  Si vous sélectionnez un document réception ou rangement interne dont toutes les lignes disposent déjà d’instructions, [!INCLUDE[prod_short](includes/prod_short.md)]] vous indique qu’il n’y a rien à gérer.  

4. Renseignez le champ **Méthode de tri** pour trier les lignes.  

    > [!NOTE]  
    >  La façon dont les lignes sont triées dans la feuille ne se répercute pas automatiquement sur l’instruction de rangement. Cependant, les mêmes possibilités de tri et de classement des emplacements existent. Vous pouvez recréer l’ordre des lignes planifié dans la feuille lorsque vous créez ou triez les instructions rangement.

5. Renseignez le champ **Quantité à traiter**. Choisissez l’action **Remplir qté à traiter**, ou renseignez les champs manuellement.  
6. Si nécessaire, vous pouvez modifier les lignes manuellement. Vous pouvez supprimer des lignes (par exemple, si certains articles doivent être rangés dans un emplacement éloigné des emplacements des autres articles).  

    > [!NOTE]  
    > Lorsque vous supprimez des lignes, elles sont uniquement supprimées de cette feuille. Elles ne sont pas supprimées de la sélection de rangement.  

7. Choisissez l’action **Créer rangement**. La page **Créer document** s’ouvre, où vous pouvez ajouter des informations supplémentaires au rangement que vous créez.  

    * Vous pouvez affecter le rangement à un employé donné.  
    * Vous pouvez trier les lignes instruction rangement comme dans la feuille ou par classement emplacement. Lorsque vous triez selon la priorité emplacement, les lignes *Prendre* apparaissent en premier, car la plupart des emplacements de réception ont une priorité emplacement de 0. Les lignes *Placer* apparaissent en dernier, en commençant par les emplacements avec le classement le plus bas. Si vous avez structuré votre entrepôt de façon à ce que les emplacements de même niveau soient les uns à côté des autres et si vous utilisez cette méthode de tri, les magasiniers auront moins de distance à parcourir.  
    * Vous pouvez choisir de ne pas afficher les lignes créées par [!INCLUDE[prod_short](includes/prod_short.md)]] lorsqu’il a converti une grande unité de mesure en unités plus petites en sélectionnant le champ **Filtrer déconditionnement**. Pour plus d’informations sur le déconditionnement, consultez [Activer le déconditionnement automatique avec le prélèvement et le rangement dirigés](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Vous pouvez faire en sorte que le champ **Quantité à traiter** des instructions rangement ne soit pas renseigné automatiquement.  
    * Vous pouvez imprimer immédiatement le document.  

8. Sélectionnez **OK** pour créer le rangement.  

## Pour créer un rangement à partir d’une réception validée

Si un magasin utilise à la fois le traitement du rangement et de la réception et que vous avez supprimé des lignes rangement, ou si vous utilisez le prélèvement et le rangement dirigés et avez décidé de ne pas utiliser la feuille rangement, vous pouvez créer ou recréer des instructions de rangement pour les lignes réception validées.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Réceptions entrepôt enregistrées**, puis sélectionnez le lien associé.  
2. Sélectionnez une réception validée à ranger.  
3. Sélectionnez l’action **Fiche**.  

    Si le champ **Statut document** est blanc, la réception n’a pas été rangée. Sinon, le champ indique que la réception est partiellement ou entièrement rangée.  

4. Si la réception est partiellement rangée ou n’est pas rangée du tout, choisissez l’action **Créer rangement**.  
5. Renseignez les champs selon vos besoins, puis sélectionnez **OK**.  

## Pour ranger les articles

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Rangements entrepôt**, puis sélectionnez le lien associé.

2. Ouvrez le rangement entrepôt qui est prêt à être traité.  
3. Si votre entrepôt le requiert, saisissez votre ID utilisateur lorsque vous commencez à travailler sur un rangement.  

    Vous pouvez trier les lignes rangement en fonction de critères divers, tels que l’article, le numéro emplacement ou la date d’échéance. Le tri peut aider à optimiser le processus de rangement, par exemple :

    * Si les lignes Prendre et Placer de chaque ligne réception ne se suivent pas directement et que vous souhaitez qu’elles se suivent, triez-les en sélectionnant **Article** dans le champ **Méthode de tri**.  
    * Si les classements des emplacements reflètent la disposition physique de l’entrepôt, utilisez la méthode de tri **Priorité emplacement** pour organiser le travail par emplacements.

4. Effectuez les actions.

    Si un code emplacement est obligatoire pour le magasin, chaque ligne réception devient au moins deux lignes dans le rangement entrepôt, comme suit.  

    * la première ligne, correspondant au champ **Type action** **Prélèvement**, indique l’endroit où se trouvent les articles dans la zone de réception. Vous ne pouvez pas modifier la zone et l’emplacement de cette ligne.  
    * La ligne suivante, avec **Placer** dans le champ **Type d’action**, indique l’endroit où vous devez placer les articles dans l’entrepôt. Si vous recevez un grand nombre d’articles sur une ligne réception, vous devrez peut-être ranger les articles dans plusieurs emplacements, pour qu’il y ait une ligne Placer pour chaque emplacement. 

    > [!NOTE]
    > Si vous devez placer les articles d’une ligne dans plusieurs emplacements, notamment parce que l’emplacement indiqué est plein, utilisez l’action **Eclater ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.

5. Après avoir placé tous les articles dans des emplacements selon les instructions, choisissez l’action **Enregistrer rangement**.  

## Voir la [formation Microsoft](/training/modules/receive-put-away-items/) associée

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
