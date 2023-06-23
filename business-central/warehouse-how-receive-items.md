---
title: Réceptionner des articles
description: Cet article est un aperçu des différentes manières de recevoir des articles dans un entrepôt avec une réception entrepôt.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts" />Réceptionner des articles avec une réception entrepôt

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous recevez des articles et les rangez en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus entrant|Réceptions requises|Rangements requis|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation de la réception et du rangement à partir d’un document de rangement stock||Activé|De base : commande par commande.|  
|A|Validation de la réception et du rangement à partir d’un document réception entrepôt|Activé||De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation de la réception d’un document réception entrepôt et validation du rangement à partir d’un document de rangement entrepôt|Activé|Activé|Avancé|  

Pour en savoir plus sur la gestion des articles entrants, consultez [Flux d’enlogement](design-details-inbound-warehouse-flow.md).

L’article suivant fait référence aux méthodes C et D dans le tableau précédent.

## <a name="receive-items-with-a-warehouse-receipt" />Réceptionner des articles avec une réception entrepôt

Lorsque les articles arrivent dans un entrepôt configuré pour traiter les réceptions entrepôt, vous devez extraire les lignes du document origine lancé ayant déclenché la réception. Si vous utilisez des emplacements, vous pouvez soit accepter l’emplacement par défaut, soit spécifier l’emplacement dans lequel placer les articles. Ce dernier peut être nécessaire lorsque vous recevez un article pour la première fois. Alors, renseignez les quantités d’articles reçus et validez la réception.  

Vous pouvez créer une réception entrepôt de deux manières :

* En mode « push », lorsque le travail est effectué commande par commande. Sélectionnez l’action **Créer réception entrepôt** dans le document origine, tel qu’une commande achat, un retour vente ou un ordre de transfert pour créer une réception entrepôt pour un document origine.
* En mode « pull », où vous utilisez l’action **Lancer** du document origine, action in the source document, tel qu’une commande achat, un retour vente ou un ordre de transfert pour lancer le document dans l’entrepôt. Un magasinier crée une **Réception entrepôt** pour un ou plusieurs documents origine lancés. La procédure suivante décrit comment créer une réception entrepôt en mode « push ». La procédure suivante décrit comment créer une réception entrepôt en mode « pull ».

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Réceptions entrepôt**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  

    Renseignez le champ **Code magasin** dans le raccourci **Général**. Lorsque vous récupérez des lignes document origine, certaines des informations de l’en-tête sont copiées dans chaque ligne.

    Pour un magasin qui nécessite des emplacements, remplissez le champ **Code emplacement**. Selon votre configuration, [!INCLUDE[prod_short](includes/prod_short.md)] peut ajouter le code emplacement pour vous. Learn more at [Codes zone et emplacement](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Vous pouvez obtenir le document origine de deux manières :

    1. Choisissez l’action **Extraire documents origine**. La page **Documents origine - Entrant** s’ouvre. Ici, vous pouvez sélectionner un ou plusieurs documents origine lancés dans l’entrepôt qui nécessitent une réception.
    2. Choisissez l’action **Filtrer pour extr. doc. orig.**. La page **Filtres pour extr. doc. orig. - Entrants** s’ouvre. Ici, vous pouvez sélectionner le filtre de document origine et l’exécuter. Toutes les lignes du document origine lancé qui répondent aux critères de filtre sont ajoutées sur la page **Réception entrepôt**. Learn more at [Procédure : utiliser des filtres afin d’obtenir des documents origine](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Définissez la quantité à recevoir.

    Le champ **Qté à recevoir** contient la quantité restante pour chaque ligne, mais vous pouvez modifier cette quantité selon vos besoins. 

    Pour définir la valeur dans le champ **Qté à recevoir** sur toutes les lignes à zéro, choisissez l’action **Supprimer qté à recevoir**. Par exemple, définir les quantités sur zéro est utile si vous utilisez un lecteur de code-barres pour mettre à jour les quantités reçues. Pour ajouter à nouveau les quantités restantes à partir du document origine, choisissez l’action **Remplir qté à recevoir**.  

    Sur un document réception entrepôt où la quantité reçue est supérieure à celle commandée, saisissez la quantité réellement reçue dans le champ **Qté à recevoir**. Si l’augmentation est inférieure ou égale à la tolérance indiquée par le code de sur-réception attribué, le champ **Quantité de sur-réception** est mis à jour pour afficher la quantité de dépassement de la valeur dans le champ **Quantité**. Si l’augmentation est supérieure à la tolérance, la sur-réception n’est pas autorisée.

5. Validez la réception entrepôt. Les champs relatifs à la quantité dans les documents origine sont mis à jour et les articles sont ajoutés au stock.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Si vous utilisez le rangement entrepôt, qui fait référence à la méthode D du tableau au début de cet article, les articles sont reçus mais ne peuvent pas être prélevés tant qu’ils n’ont pas été rangés. Pour en savoir plus sur le rangement d’articles, consultez [Ranger des articles avec le rangement entrepôt](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Sinon, envisagez d’utiliser l’action **Valider et imprimer**. L’action validera la réception et l’imprimera en tant qu’instruction de rangement indiquant où placer l’article.

    > [!NOTE]  
    > Si votre entrepôt utilise le transbordement, vous pouvez vérifier si vous pouvez transborder des articles sans les ranger. Pour en savoir plus sur le transbordement, consultez [Transborder des articles](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents" />Procédure : utiliser des filtres afin d’obtenir des documents origine

À partir d’une réception entrepôt, vous pouvez utiliser la page **Filtres pour extr. doc. orig.** afin d’extraire les lignes du document origine lancé qui indiquent les articles à recevoir.

1. Dans la réception entrepôt, choisissez l’action **Filtrer pour extr. doc. orig.**.
2. Pour configurer un nouveau filtre, entrez un code descriptif dans le champ **Code**, puis choisissez l’action **Modifier**.

    La page **Fiche filtre document origine - Entrants** s’ouvre.

3. Utilisez les filtres pour définir le type de lignes du document origine à récupérer. Par exemple, vous pouvez sélectionner des types de documents origine, tels que des commande achat ou des ordres de transfert.
4. Choisir **Exécuter**.  

Toutes les lignes du document origine lancé qui répondent aux critères de filtre sont ajoutées sur la page **Réception entrepôt** sur laquelle vous avez activé les filtres.

Le nombre de combinaisons de filtres est illimité. Les filtres sont enregistrés sur la page **Filtres pour extr. doc. orig.** et seront disponibles la prochaine fois que vous en aurez besoin. Vous pouvez modifier les critères à tout moment en choisissant l’action **Modifier**.

## <a name="zone-and-bin-codes" />Codes zone et emplacement

Pour réceptionner des articles portant des codes classe entrepôt différents du code classe de l’emplacement indiqué dans le champ **Code emplacement** de l’en-tête du document, effacez la valeur du champ **Code emplacement** de l’en-tête avant d’extraire les lignes des documents origine des articles.  
<!-- TBD, table with comparison of various options-->

Si des emplacements sont obligatoires pour un magasin, les codes zone et emplacement sont ajoutés aux documents de réception entrepôt comme suit :

* Pour les configurations avancées qui utilisent le rangement et le prélèvement dirigés, [!INCLUDE [prod_short](includes/prod_short.md)] utilise le code emplacement réception de la page **Fiche magasin** du magasin. Si aucun code emplacement réception n’est spécifié, aucun emplacement n’est spécifié. Si l’article et les emplacements de réception ne correspondent pas, le code emplacement réception est vide.
* Dans d’autres configurations, si aucun code emplacement réception n’est spécifié, [!INCLUDE [prod_short](includes/prod_short.md)] utilise le code emplacement du document origine.

## <a name="see-related-microsoft-trainingtrainingmodulesreceive-invoice-dynamics-d365-business-centralindex" />Voir la [formation Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index) associée.

## <a name="see-also" />Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
