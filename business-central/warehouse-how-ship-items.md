---
title: Expédier des articles
description: Cet article décrit comment expédier des articles depuis votre entrepôt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# <a name="ship-items-with-a-warehouse-shipment" />Expédier des articles avec une expédition entrepôt

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous prélevez et expédiez des articles en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus sortant|Prélèvement requis|Expédition requise|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l’expédition à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock|Activé||De base : commande par commande.|  
|A|Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt||Activé|De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation du prélèvement à partir d’un document prélèvement entrepôt, et validation de l’expédition à partir d’un document expédition entrepôt|Activé|Activé|Avancé|  

Pour en savoir plus sur l’expédition d’articles, consultez [Flux de désenlogement](design-details-outbound-warehouse-flow.md).

Cet article fait référence aux méthodes C et D dans le tableau. Dans les deux méthodes, vous commencez par créer un document d’expédition à partir d’un document origine commercial. Puis, vous prélevez les articles spécifiés pour l’expédition.

Lorsqu’un magasin nécessite des expéditions entrepôt, vous pouvez expédier des articles en fonction des documents origine qui ont été émis dans l’entrepôt. L’émission des documents origine rend les articles qu’ils contiennent prêts à être manipulés dans l’entrepôt. Voici des exemples de documents origine :

* Commandes vente
* Retours achat
* Ordres de transfert
* Commandes service

Vous pouvez créer une expédition entrepôt de deux manières :

* En mode « push », lorsque le travail est effectué commande par commande. Choisissez l’action **Créer expédition entrepôt** dans le document origine pour créer une expédition entrepôt pour le document.
* En mode « pull », où vous utilisez l’action **Lancer** dans le document origine pour le lancer dans l’entrepôt. Un magasinier crée une **Expédition entrepôt** pour un ou plusieurs documents origine lancés. La procédure suivante décrit comment créer une expédition entrepôt en mode « pull ».

## <a name="to-ship-items-using-a-warehouse-shipment-document" />Pour expédier des articles avec un document d’expédition entrepôt

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Expéditions entrepôt**, puis sélectionnez le lien associé.  
2. Choisissez **Nouveau**.  
3. Dans le champ **N°**, choisissez la série de numéros à utiliser pour créer un identifiant pour l’expédition.  
4. Dans le champ **Code magasin**, choisissez le magasin à partir duquel vous expédiez. 

    Lorsque vous récupérez des lignes document origine, certaines des informations du magasin sont copiées dans chaque ligne.  
5. Si le magasin nécessite des emplacements, remplissez le champ **Code emplacement**. Selon votre configuration, [!INCLUDE[prod_short](includes/prod_short.md)]] peut ajouter le code emplacement pour vous. Learn more at [Codes zone et emplacement](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Vous pouvez obtenir le document origine de deux manières :

    * Choisissez l’action **Extraire documents origine**. La page **Documents origine - Sortants** s’ouvre. Ici, vous pouvez sélectionner un ou plusieurs documents origine lancés dans l’entrepôt qui nécessitent une expédition.
    * Choisissez l’action **Filtrer pour extr. doc. orig.**. La page **Filtres pour extr. doc. orig.** s’ouvre. Vous pouvez sélectionner le filtre de document origine et l’appliquer. Toutes les lignes du document origine lancé qui répondent aux critères de filtre sont ajoutées sur la page **Expédition entrepôt**. Learn more at [Procédure : utiliser des filtres afin d’obtenir des documents origine](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Si votre magasin utilise le transbordement, et dispose d’emplacements pour chaque ligne, vous pouvez examiner la quantité d’articles placés dans les emplacements transbordement. [!INCLUDE [prod_short](includes/prod_short.md)] calcule les quantités chaque fois que les champs de l’expédition sont mis à jour. S’il s’agit des articles correspondant à l’expédition que vous préparez, vous pouvez créer un prélèvement pour tous les articles, puis terminer l’expédition. En savoir plus sur [ Transborder des articles](warehouse-how-to-cross-dock-items.md).

7. Créez un prélèvement entrepôt. Si le magasin nécessite un prélèvement, vous pouvez créer des activités de prélèvement pour les expéditions d’entrepôt de l’une des deux manières suivantes :

    * En mode « push », où vous utilisez l’action **Créer prélèvement**. Sélectionnez les lignes à prélever et spécifiez les informations sur les prélèvements. Par exemple, dans quels emplacements prendre et placer, et combien d’unités manipuler. Les emplacements peuvent être prédéfinis pour l’entrepôt ou la ressource.
    * En mode « pull », où vous utilisez l’action **Lancer**. Sur la page **Feuille prélèvement**, utilisez l’action **Extraire documents entrepôt** pour récupérer les prélèvements qui vous ont été attribués. Lorsque les prélèvements entrepôt sont entièrement enregistrés, les lignes dans la **Feuille prélèvement** sont supprimées. Learn more at [Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Pour un magasin qui ne nécessite pas de prélèvement, vous pouvez imprimer l’expédition entrepôt et l’utiliser comme liste de prélèvement.

8. Spécifiez la quantité à expédier.  

    Pour un magasin nécessitant le prélèvement, le champ **Qté à expédier** est mis à jour automatiquement lorsque le prélèvement est enregistré. Sinon, le champ **Qté à expédier** est rempli avec la quantité restante pour chaque ligne lorsque la ligne d’expédition entrepôt est créée.

    Vous pouvez modifier la quantité, mais vous ne pouvez pas expédier plus d’articles que le nombre indiqué dans le champ **Qté restante** sur la ligne du document origine ou le champ **Qté prélevée** si le prélèvement est requis.

    Pour définir la valeur dans le champ **Qté à expédier** sur toutes les lignes à zéro, choisissez l’action **Supprimer qté à expédier**. Par exemple, définir les quantités sur zéro est utile si vous utilisez un lecteur de code-barres pour mettre à jour les quantités d’expédition. Pour ajouter la quantité disponible pour l’expédition, choisissez l’action **Remplir qté à expédier**.

9. Validez la livraison.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## <a name="how-to-use-filters-to-get-source-documents" />Procédure : utiliser des filtres afin d’obtenir des documents origine

À partir d’une expédition entrepôt, vous pouvez utiliser la page **Filtres pour extr. doc. orig.** afin d’extraire les lignes du document origine lancé qui définissent les articles à recevoir ou à expédier.

1. Dans l’expédition entrepôt, choisissez l’action **Filtrer pour extr. doc. orig.**. 
2. Pour configurer un nouveau filtre, entrez un code descriptif dans le champ **Code**, puis choisissez l’action **Modifier**.

    La page **Fiche filtre document origine - Sortants** s’ouvre.

3. Utilisez les filtres pour définir le type de lignes du document origine à récupérer. Par exemple, vous pouvez sélectionner des types de documents origine, tels que des commande vente ou des ordres de transfert.
4. Choisir **Exécuter**.  

Toutes les lignes du document origine lancé qui répondent aux critères de filtre sont ajoutées sur la page **Expédition entrepôt** sur laquelle vous avez défini les filtres.

Le nombre de combinaisons de filtres est illimité. Les filtres sont enregistrés sur la page **Filtres pour extr. doc. orig.** et seront disponibles la prochaine fois que vous en aurez besoin. Vous pouvez modifier les critères à tout moment en choisissant l’action **Modifier**.

## <a name="zone-and-bin-codes" />Codes zone et emplacement

Si les emplacements sont obligatoires dans le magasin, [!INCLUDE [prod_short](includes/prod_short.md)] suggère un code zone et un code emplacement sur le document d’expédition entrepôt.

* Pour les configurations avancées dans lesquelles un magasin utilise le rangement et le prélèvement dirigés, [!INCLUDE [prod_short](includes/prod_short.md)] utilise l’emplacement spécifié dans le champ **Code emplacement expédition** sur la **Fiche magasin**. Si aucun **Code emplacement expédition** n’est spécifié, le champ est vide. Si l’article et l’emplacement d’expédition ne correspondent pas, [!INCLUDE [prod_short](includes/prod_short.md)] laisse l’emplacement d’expédition vide.
* Dans les autres cas, [!INCLUDE [prod_short](includes/prod_short.md)] utilise toujours en premier l’emplacement spécifié dans le champ **Code emplacement expédition** sur la **Fiche magasin**. Si aucun code emplacement d’expédition n’est spécifié, [!INCLUDE [prod_short](includes/prod_short.md)] utilise le code emplacement du document origine.

## <a name="handling-assemble-to-order-items-in-warehouse-shipments" />Traitement des articles à assembler pour commande dans les expéditions entrepôt

Dans des scénarios d’assemblage pour commande, utilisez le champ **Qté à expédier** sur les lignes expédition entrepôt pour enregistrer le nombre d’unités assemblées. La quantité est validée comme résultat d’assemblage lorsque vous validez l’expédition entrepôt. Pour d’autres lignes expédition entrepôt, la valeur du champ **Qté à expédier** est zéro.

Lorsque les ouvriers ont fini d’assembler une partie ou la totalité de la quantité à assembler pour commande, enregistrez la quantité dans le champ **Qté à expédier** sur la ligne d’expédition entrepôt. Sélectionnez ensuite l’action **Valider expédition**. Le résultat d’assemblage est validé, y compris la consommation des composants. Une expédition vente pour la quantité est validée pour la commande vente.

À partir de l’ordre d’assemblage, vous pouvez choisir **Ligne expédition entrepôt Assembler pour commande** pour accéder à la ligne expédition entrepôt.

Une fois l’expédition entrepôt validée, divers champs de la ligne commande vente sont mis à jour pour afficher la progression dans l’entrepôt. Les champs suivants sont également mis à jour pour afficher le nombre de quantités à assembler pour commande qui restent à être assemblées et expédiées :

* **Qté restante entrepôt ATO**
* **Qté restante entrepôt ATO (base)**

> [!NOTE]
> Dans les scénarios de combinaison, où une partie de la quantité doit être assemblée et l’autre doit être expédiée à partir des stocks, deux lignes expédition entrepôt sont créées. L’une est pour la quantité à assembler pour commande et l’autre est destinée à la quantité en stock.
>
> La quantité assemblée pour commande est gérée comme décrit dans cet article. La quantité provenant du stock est traitée comme une ligne d’expédition entrepôt standard. Pour plus d’informations sur les scénarios de combinaison, consultez [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/ship-invoice-items-dynamics-365-business-central/) associée.

## <a name="see-also" />Voir aussi

[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
