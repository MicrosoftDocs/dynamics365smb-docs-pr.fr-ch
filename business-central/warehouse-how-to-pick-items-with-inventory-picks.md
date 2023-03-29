---
title: Comment prélever des articles avec les prélèvements stock
description: Découvrez comment utiliser les prélèvements stock pour enregistrer et valider les informations de prélèvement et d’expédition pour les documents origine.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# Prélever des articles avec les prélèvements stock

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous prélevez et expédiez des articles en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus sortant|Prélèvement requis|Expédition requise|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Validation du prélèvement et de l’expédition à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation du prélèvement et de l’expédition à partir d’un document prélèvement stock|Activé||De base : commande par commande.|  
|A|Validation du prélèvement et de l’expédition à partir d’un document expédition entrepôt||Activé|De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation du prélèvement à partir d’un document prélèvement entrepôt, et validation de l’expédition à partir d’un document expédition entrepôt|Activé|Activé|Avancé|  

Learn more at [Flux de désenlogement](design-details-outbound-warehouse-flow.md).

Cet article fait référence à la méthode B dans le tableau.

Lorsque votre magasin est défini pour exiger un traitement des prélèvements mais pas un traitement des expéditions, utilisez la page **Prélèvement stock** pour enregistrer et valider les informations de prélèvement et d’expédition pour vos documents origine. Les documents origine sortants peuvent être des commandes vente, des retours achat et des ordres de désenlogement.

> [!NOTE]
> Les besoins en composants des ordres de fabrication et d’assemblage représentent également des documents origine sortants. Pour en savoir plus sur la gestion des ordres de production et d’assemblage pour les processus internes, consultez [Détails de conception : Flux d’entrepôt internes](design-details-internal-warehouse-flows.md).
>
> Bien que les commandes de service soient également des documents origine sortants, elles ne prennent pas en charge le niveau de complexité commande par commande de base.
>
> En cas de prélèvement et d’expédition de quantités de lignes vente assemblées pour commande, vous devez suivre certaines règles lorsque vous créez les lignes prélèvement stock. En savoir plus sur [Traitement des articles à assembler pour commande dans les prélèvements stock](#handling-assemble-to-order-items-with-inventory-picks).  

Vous pouvez créer un prélèvement stock de trois manières :

* Créez le prélèvement stock directement à partir du document origine.  
* Créez des prélèvements stock pour plusieurs documents origine simultanément en utilisant un traitement par lots.
* Demandez le prélèvement en deux étapes en émettant d’abord le document origine, qui signale à l’entrepôt que le document origine est prêt pour le prélèvement.

Le prélèvement stock peut ensuite être créé à partir de la page **Prélèvement stock** sur la base du document origine.  

## Pour créer un prélèvement stock à partir du document origine

1. Dans le document origine, qui peut être une commande vente, un retour achat ou un désenlogement transfert, choisissez l’action **Créer prélèv./rangement stock**.
2. Activez la case à cocher **Créer prélèvement stock**.  
3. Cliquez sur le bouton **OK**. Un nouveau prélèvement stock sera créé.

## Pour créer plusieurs prélèvements stock avec un traitement par lots

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Créer rangement/prélèvement/mouvement stock**, puis choisissez le lien associé.  
2. Sur le raccourci **Demande entrepôt**, utilisez les champs **Document origine** et **N° origine** pour opérer un filtrage sur certains types de documents ou des plages de numéros de document. Par exemple, vous pouvez créer des prélèvements uniquement pour des commandes vente.  
3. Dans le raccourci **Options**, cochez la case **Créer prélèvement stock**.
4. Cliquez sur le bouton **OK**.

## Pour créer le prélèvement en deux étapes

### Pour demander un prélèvement stock en lançant le document origine

Pour les commandes vente, de retours achat et de désenlogements transfert, vous créez la demande entrepôt en lançant l’ordre. Le lancement de la commande rend les articles disponibles pour le prélèvement.

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez la commande vente que vous voulez lancer, puis sélectionnez l’action **Lancer**.

### Pour créer un prélèvement stock en fonction du document origine

Après avoir lancé une commande, le magasinier peut créer un prélèvement stock.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvements stock**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Document origine**, sélectionnez le type de document origine relatif au prélèvement.  
4. Dans le champ **N° origine**, sélectionnez le document origine.  
5. Sinon, choisissez l’action **Extraire document origine** pour créer une liste de tous les documents origine sortants prêts pour le prélèvement dans le magasin.  
6. Sélectionnez le bouton **OK** pour renseigner les lignes prélèvement en fonction des documents origine sélectionnés.  

## Pour enregistrer les prélèvements stock

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Prélèvement stock**, puis choisissez le lien associé.  
2. Dans le champ **Code emplacement** sur les lignes prélèvement, l’emplacement à partir duquel les articles doivent être prélevés est proposé sur la base d’un emplacement par défaut de l’article. Vous pouvez modifier l’emplacement sur la page, si nécessaire.  
3. Exécutez le prélèvement, puis saisissez la quantité prélevée dans le champ **Quantité à traiter**.

    Si vous devez prélever les articles d’une ligne à partir de plusieurs emplacements, par exemple parce que la quantité totale n’est pas dans l’emplacement, utilisez l’action **Fractionner la ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.

4. Sélectionnez l’action **Valider**.  

    * Validez l’expédition des lignes du document origine qui ont été prélevées.
    * Si le magasin utilise des emplacements, la validation crée également des écritures entrepôt pour valider les modifications apportées aux quantités emplacement.  

## Traitement des articles à assembler pour commande dans les prélèvements stock

Vous pouvez également utiliser la page **Prélèvement stock** pour prélever et expédier les ventes lorsque les articles doivent être assemblés avant de pouvoir être livrés. Learn more at [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).

Les articles à assembler pour commande ne se trouvent pas physiquement dans un emplacement tant qu’ils n’ont pas été assemblés et validés comme sortie vers un emplacement. Le prélèvement des articles à assembler pour commande à partir d’un emplacement en vue de l’expédition suit un flux spécial.

1. Depuis un emplacement, les magasiniers extraient des éléments d’assemblage sur le poste d’accueil de livraison puis valident le prélèvement stock.
2. Le prélèvement stock enregistré valide le résultat d’assemblage, la consommation de composants et l’expédition vente.

Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour créer automatiquement un mouvement stock lors de la création du prélèvement stock pour l’élément d’assemblage. Sélectionnez le champ **Créer des mouvements automatiquement** sur la page **Paramètres d’assemblage**. Learn more at [Configurer des entrepôts de base avec les zones d’opérations](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Les lignes prélèvement stock pour les articles vente sont créées de différentes manières, selon qu’aucune, certaines ou toutes les quantités des lignes vente sont assemblées pour commande. Dans les scénarios où une partie de la quantité est assemblée et une autre est prélevée dans le stock, un minimum de deux lignes prélèvement sont créées.

Pour les ventes où la quantité totale de la ligne commande vente est assemblée pour commande, une ligne prélèvement stock est créée pour cette quantité. La valeur du champ **Quantité à assembler** correspond à la valeur du champ **Qté à expédier**. Le champ **Assembler pour commande** est sélectionné sur la ligne.

Si un flux de résultat d’assemblage est configuré pour le magasin, le champ **Code emplacement** sur la ligne de prélèvement stock contient la valeur des champs suivants, dans l’ordre suivant.

* ***Code empl. exp. ass. pr comm.** <!-- not applicable for inv pick-->
* **Code empl. depuis assemblage**

Si aucun code emplacement n’est spécifié sur la ligne commande vente et qu’aucun flux de résultat d’assemblage n’est paramétré pour le magasin, le champ **Code emplacement** de la ligne prélèvement stock est vide. Le magasinier doit ouvrir la page **Contenu emplacement** et sélectionner l’emplacement où les articles d’assemblage sont assemblés.

Dans les scénarios où une partie de la quantité est assemblée et l’autre doit être prélevée, un minimum de deux lignes prélèvement stock sont créées.

* Une ligne prélèvement pour la quantité à assembler pour commande. [!INCLUDE [prod_short](includes/prod_short.md)] utilise les champs suivants, dans cet ordre, pour déterminer le code emplacement : **Code emplacement**, **Code empl. exp. ass. pr comm.**, puis **Code empl. depuis assemblage**. Si ces champs sont vides, le magasinier doit ouvrir la page **Contenu emplacement** et choisir l’emplacement dans lequel les articles sont assemblés.  
* L’autre ligne prélèvement dépend des emplacements qui peuvent satisfaire la quantité restante. Si l’article est conservé dans plusieurs emplacements, plusieurs lignes seront créées. La ligne Prendre est basée sur la quantité indiquée dans le champ **Qté à expédier**.

> [!NOTE]  
> Si les articles sont assemblés pour commande, le prélèvement stock pour la commande vente liée crée un mouvement de stock pour tous les composants d’assemblage.  

## Voir la [formation Microsoft](/training/paths/pick-ship-items-business-central/) associée

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Procédure pas à pas : Prélèvement et expédition dans les configurations de stockage de base](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
