---
title: Réceptionner des articles
description: Cet article donne un aperçu des différentes manières de recevoir des articles dans un entrepôt, par exemple des articles avec une commande achat ou des articles avec un reçu d’entrepôt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 6cca8d8f9b0ec28b149532581f9bc458022c3cd5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529530"
---
# <a name="receive-items"></a>Réceptionner des articles

Lorsque les articles arrivent dans un entrepôt qui n’est pas configuré pour un traitement de réception entrepôt, enregistrez simplement la réception du document d’entreprise associé, comme une commande achat, un retour vente ou un ordre de transfert entrant.

Lorsque les articles arrivent dans un entrepôt configuré pour appeler un traitement de réception entrepôt, vous devez extraire les lignes du document origine lancé ayant déclenché leur réception. En présence d’emplacements, vous pouvez soit accepter l’emplacement par défaut qui est renseigné, soit renseigner l’emplacement de rangement de l’article concerné si cet article n’a jamais été utilisé dans l’entrepôt. Vous devez ensuite renseigner les quantités d’articles reçus et valider la réception.  

## <a name="receive-items-with-a-purchase-order"></a>Pour réceptionner des articles avec une commande achat

Ce qui suit décrit comment réceptionner des articles avec une commande achat. Les étapes sont similaires pour les retours vente et les ordres de transfert.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.
2. Ouvrez une commande achat existante, ou créez-en une nouvelle. En savoir plus sur [Enregistrer les achats](purchasing-how-record-purchases.md).
3. Dans le champ **Qté à recevoir**, indiquez la quantité reçue.

   > [!NOTE]
   > Si la quantité reçue est supérieure à celle commandée sur la commande achat, selon le champ **Quantité**, et que le fournisseur a été configuré pour autoriser les sur-réceptions, utilisez le champ **Sur-réception** pour gérer la quantité excédentaire. Pour en savoir plus, consultez la section [Pour réceptionner plus d’articles que commandés](warehouse-how-receive-items.md#receive-more-items-than-ordered).
4. Sélectionnez l’action **Valider**.

  La valeur du champ **Qté reçue** est mise à jour en conséquence. Si c’est une réception partielle, la valeur est inférieure à la valeur dans le champ **Quantité**.

> [!NOTE]
> Si vous utilisez un document entrepôt pour valider la réception, vous ne pouvez pas utiliser l’action **Valider** sur la commande achat. Au lieu de cela, un magasinier a déjà validé la quantité de la commande achat telle qu’elle a été reçue. En savoir plus, [Pour réceptionner des articles avec une réception entrepôt](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Réceptionner des articles avec une réception entrepôt

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réceptions entrepôt**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  

    Renseignez les champs du raccourci **Général**. Lorsque vous récupérez des lignes document origine, certaines des informations de l’en-tête sont copiées dans chaque ligne.  

    Pour une configuration de stockage avec un prélèvement et un rangement suggérés : Si le magasin possède une zone et un emplacement par défaut pour les réceptions, les champs **Code zone** et **Code emplacement** seront renseignés, mais vous pouvez les modifier selon vos besoins.  

    > [!NOTE]  
    > Pour réceptionner des articles portant des codes classe entrepôt différents du code classe de l’emplacement indiqué dans le champ **Code emplacement** de l’en-tête du document, vous devez supprimer la valeur du champ **Code emplacement** de l’en-tête avant d’extraire les lignes des documents origine des articles.  
3. Choisissez l’action **Extraire documents origine**. La page **Documents origine** s’ouvre.

    À partir d’une réception entrepôt nouvelle ou ouverte, vous pouvez utiliser la page **Filtres pour extr. doc. orig.** afin d’extraire les lignes du document origine lancé qui définissent les articles à recevoir ou à expédier.

    1. Choisissez l’action **Filtrer pour extr. doc. orig.**.  
    2. Pour configurer un nouveau filtre, entrez un code descriptif dans le champ **Code**, puis choisissez l’action **Modifier**.  
    3. Définissez le type de ligne document origine que vous souhaitez extraire en renseignant les champs de filtre appropriés.  
    4. Choisir **Exécuter**.  

    Toutes les lignes du document origine lancé qui correspondent aux critères du filtre sont à présent insérées sur la page **Réception entrepôt** à partir de laquelle vous avez activé la fonction filtre. 

    Les combinaisons de filtres que vous définissez sont stockées sur la page **Filtres pour extr. doc. orig.** jusqu’à la prochaine utilisation. Le nombre de combinaisons de filtres est illimité. Vous pouvez modifier les critères à tout moment en choisissant l’action **Modifier**.

4. Sélectionnez le document origine pour lequel vous souhaitez recevoir des articles, puis sélectionnez le bouton **OK**.  

    Les lignes des documents origine s’affichent sur la page **Réception entrepôt**. Le champ **Qté à recevoir** est renseigné avec la quantité restante pour chaque ligne, mais vous pouvez modifier cette quantité selon vos besoins. Si vous avez supprimé la valeur du champ **Code emplacement** du raccourci **Général** avant d’accéder aux lignes, vous devez alors renseigner un code emplacement approprié sur chaque ligne réception.  

    > [!NOTE]  
    >  Pour renseigner le champ **Qté à recevoir** sur toutes les lignes à zéro, choisissez l’action **Supprimer qté à recevoir**. Pour y insérer à nouveau la quantité restante, choisissez l’action **Remplir qté à recevoir**.  
    >
    >  Vous ne pouvez pas réceptionner un nombre d’articles supérieur au nombre figurant dans le champ **Qté ouverte** de la ligne document origine. Pour expédier des articles supplémentaires, utilisez la fonction filtre pour récupérer un autre document origine contenant une ligne pour l’article concerné.  

5. Validez la réception entrepôt. Les champs relatifs à la quantité dans les documents origine sont mis à jour et les articles enregistrés dans le cadre du stock de la société.  

En cas d’utilisation d’un rangement entrepôt, les lignes réception sont transmises à la fonction de rangement entrepôt. Les articles, bien que réceptionnés, ne peuvent pas être prélevés avant d’avoir été rangés. Les articles réceptionnés sont identifiés en tant que stock disponible une fois le rangement enregistré uniquement.  

En cas de non-utilisation d’un rangement entrepôt et d’utilisation d’emplacements, le rangement des articles est enregistré dans l’emplacement spécifié sur la ligne document origine.  

> [!NOTE]  
> En utilisant la fonction **Valider et Imprimer**, vous effectuez à la fois la validation de la réception et l’impression d’une instruction de rangement qui indique les articles à ranger en stock.  
>
> En cas d’utilisation d’un prélèvement et d’un rangement suggérés, les modèles rangement sont utilisés pour procéder au calcul du meilleur emplacement de rangement des articles. Il est ensuite imprimé sur l'instruction de rangement.

## <a name="receive-more-items-than-ordered"></a>Réceptionner plus d’articles que commandés

Lorsque vous recevez plus de produits que commandés, vous pouvez les réceptionner au lieu d’annuler la réception. Par exemple, il peut être moins coûteux de conserver les stocks excédentaires que de les retourner ou votre fournisseur peut vous proposer un rabais pour les conserver.

### <a name="set-up-over-receipts"></a>Configurer des sur-réceptions

Vous devez définir un pourcentage de dépassement autorisé de la quantité commandée lors de la réception. Vous le définissez sous un code de sur-réception, qui contient le pourcentage dans le champ **% de tolérance de sur-réception**. Vous affectez ensuite le code aux fiches des articles et/ou fournisseurs concernés.  

Ce qui suit décrit comment configurer un code de sur-réception et l’attribuer à un article. La procédure est identique pour la configuration pour un fournisseur.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche pour un article que vous soupçonnez parfois d’être livré avec une quantité supérieure à celle commandée.
3. Cliquez sur **Recherche** dans le champ **Code de sur-réception**.
4. Sélectionnez l’action **Nouveau**.
5. Sur la page **Codes de sur-réception**, créez une ou plusieurs lignes définissant différentes stratégies de sur-réception. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Sélectionnez une ligne, puis sélectionnez **OK**.

Le code de sur-réception est affecté à l’article. Toute commande achat ou réception entrepôt pour l’article permet désormais de réceptionner une quantité supérieure à celle commandée selon le pourcentage de tolérance de sur-réception indiqué.

> [!NOTE]
> Vous pouvez configurer un flux de travail approbation pour exiger l’approbation des sur-réceptions avant leur traitement. Dans ce cas, vous devez sélectionner le champ **Approbation requise** sur la page **Codes de sur-réception**. En savoir plus sur [Créer des flux de projet](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Effectuer une sur-réception

Sur les lignes achat et les lignes réception entrepôt, le champ **Quantité de sur-réception** permet d’enregistrer les quantités excédentaires reçues, c’est-à-dire les quantités dépassant la valeur dans le champ **Quantité**, la quantité commandée.

Lorsque vous traitez une sur-réception, vous pouvez augmenter la valeur dans le champ **Qté à recevoir** pour la faire correspondre à la quantité réellement reçue. Le champ **Quantité de sur-réception** est ensuite mis à jour pour afficher la quantité excédentaire. Vous pouvez également saisir la quantité excédentaire dans le champ **Quantité de sur-réception**. Le champ **Qté à recevoir** est ensuite mis à jour pour afficher la quantité commandée augmentée de la quantité excédentaire. La procédure suivante décrit comment renseigner le champ **Qté à recevoir**.  

1. Sur une commande achat ou un document réception entrepôt où la quantité reçue est supérieure à celle commandée, saisissez la quantité réellement reçue dans le champ **Qté à recevoir**.

    Si l’augmentation est inférieure ou égale à la tolérance indiquée par le code de sur-réception attribué, le champ **Quantité de sur-réception** est mis à jour pour afficher la quantité de dépassement de la valeur dans le champ **Quantité**.

    Si l’augmentation est supérieure à la tolérance indiquée, la sur-réception n’est pas autorisée. Dans ce cas, vous pouvez rechercher s’il existe un autre code de sur-réception qui l’autorisera. Sinon, seule la quantité commandée peut être réceptionnée et la quantité excédentaire doit être traitée autrement, par exemple en la renvoyant au fournisseur.

2. Validez la réception comme vous le feriez pour toute autre réception.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] n’inclut pas de fonctionnalité permettant d’initier automatiquement l’administration financière des sur-réceptions. Vous devez gérer cela manuellement en accord avec le fournisseur, qui peut par exemple vous envoyer une facture nouvelle ou mise à jour.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/index) associée.

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
