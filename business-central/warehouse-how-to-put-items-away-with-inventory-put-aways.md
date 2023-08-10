---
title: Comment ranger des articles avec le rangement stock
description: Découvrez comment utiliser les documents de rangement stock pour enregistrer et valider les informations de rangement et de réception.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '7375,'
---
# <a name="put-items-away-with-inventory-put-aways"></a>Ranger des articles avec le rangement stock

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous recevez des articles et les rangez en utilisant l’une des quatre méthodes décrites dans le tableau suivant.

|Méthode|Processus entrant|Réceptions requises|Rangements requis|Niveau de complexité (pour plus d’informations, consultez [Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Validation de la réception et du rangement à partir de la ligne commande|||Aucune activité entrepôt dédiée.|  
|B|Validation de la réception et du rangement à partir d’un document de rangement stock||Activé|De base : commande par commande.|  
|A|Validation de la réception et du rangement à partir d’un document réception entrepôt|Activé||De base : envoi/réception regroupés pour plusieurs commandes.|  
|J|Validation de la réception d’un document réception entrepôt et validation du rangement à partir d’un document de rangement entrepôt|Activé|Activé|Avancé|  

Learn more at [Flux d’enlogement](design-details-inbound-warehouse-flow.md).

Cet article fait référence à la méthode B dans le tableau.

Lorsque votre magasin est configuré pour exiger un traitement des rangements, mais qu’il ne l’est pas pour un traitement des réceptions, utilisez un document **Rangement stock** pour enregistrer et valider les informations de rangement et de réception pour vos documents origine. Les documents origine entrants peuvent être des commandes achat, des retours vente et des ordres d’enlogement.

> [!NOTE]
> Les sorties de la production et de l’assemblage représentent également des documents origine entrants. Pour en savoir plus sur la gestion des sorties de la production et de l’assemblage pour les processus internes, consultez [Détails de conception : Flux d’entrepôt internes](design-details-internal-warehouse-flows.md).

Vous pouvez créer un rangement stock de trois manières :  

* Créez le rangement stock directement à partir du document origine proprement dit.  
* Créez des rangements stock pour plusieurs documents origine simultanément en utilisant un traitement par lots.  
* Créez le rangement en deux étapes en publiant d’abord le document origine pour rendre les articles disponibles pour le rangement. Vous pouvez créer le rangement stock sur la base du document origine en utilisant la page **Rangement stock**.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Pour créer un rangement stock à partir du document origine

1. Dans le document origine, qui peut être une commande achat, un retour vente ou un ordre d’enlogement, choisissez l’action **Créer prélèv./rangement stock**.  
2. Activez la case à cocher **Créer prélèv./rangement stock**.
3. Cliquez sur le bouton **OK**. Un nouveau rangement stock est créé.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Pour créer plusieurs rangements stock avec un traitement par lots

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Créer rangement/prélèvement/mouvement stock**, puis choisissez le lien associé. 
2. Sur le raccourci **Demande entrepôt**, utilisez les champs **Document origine** et **N° origine** pour opérer un filtrage sur certains types de documents ou des plages de numéros de document. Par exemple, vous pouvez créer des rangements uniquement pour les commandes achat.
3. Sur le raccourci **Options**, cochez la case **Créer rangement stock**.
4. Cliquez sur le bouton **OK**. Les rangements stock spécifiés sont créés.

## <a name="to-create-the-put-away-in-two-steps"></a>Pour créer le rangement en deux étapes

### <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Pour demander un rangement stock en lançant le document d’origine

Lorsque vous lancez des commandes achat, des retours vente et des ordres de transfert entrants, les articles des commandes deviennent disponibles pour être rangés. Les étapes suivantes décrivent comment rendre les articles d’une commande achat prêts à être rangés.  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat**, puis choisissez le lien associé.
2. Sélectionnez la commande achat que vous voulez lancer, puis sélectionnez l’action **Lancer**.  

### <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Pour créer un rangement stock sur la base du document origine

Un magasinier peut créer un nouveau rangement stock basé sur le document origine émis.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangement stock**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Document origine**, sélectionnez le type de document origine que vous rangez.  
4. Dans le champ **N° origine**, sélectionnez le document origine.  
5. Sinon, choisissez l’action **Extraire document origine** pour sélectionner le document à partir de la liste des documents origine entrants prêts pour le rangement dans le magasin.  
6. Cliquez sur le bouton **OK** pour renseigner les lignes rangement en fonction du document origine sélectionné.  

## <a name="to-record-the-inventory-put-away"></a>Pour enregistrer les rangements stock

1. Sur la page **Rangements stock**, ouvrez un document de rangement créé au préalable.  
2. Dans le champ **Code emplacement** sur les lignes rangement, les emplacements où les articles doivent être rangés sont proposés sur la base de l’emplacement par défaut de l’article. Si nécessaire, vous pouvez modifier l’emplacement.  
3. Exécutez le rangement, puis saisissez la quantité effectivement rangée dans le champ **Quantité à traiter**.

    Si vous devez placer les articles d’une ligne dans plusieurs emplacements, notamment parce que l’emplacement indiqué est plein, utilisez l’action **Eclater ligne** sur le raccourci **Lignes**. L’action crée une ligne pour la quantité restante à gérer.  
4. Après avoir rangé les articles, choisissez l’action **Valider**.  

    * Valider la réception des lignes du document origine qui ont été rangées
    * Si le magasin utilise des emplacements, la validation crée également des écritures entrepôt pour valider les modifications apportées aux quantités emplacement.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/receive-put-away-items/) associée

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
