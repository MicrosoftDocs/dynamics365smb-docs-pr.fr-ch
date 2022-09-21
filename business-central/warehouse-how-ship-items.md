---
title: Expédier des articles
description: Cet article décrit comment expédier des articles depuis votre entrepôt en fonction de la configuration de votre entrepôt pour le traitement des expéditions.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: e31dc7a25ea4bb81019163b057b2f1e4e4a1c1d9
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461172"
---
# <a name="ship-items"></a>Expédier des articles

Lorsque vous expédiez des articles provenant d’un entrepôt qui n’est pas configuré pour un traitement d’expédition entrepôt, enregistrez simplement l’expédition du document d’entreprise associé, comme une commande vente, une commande service, un retour vente ou un ordre de transfert sortant.

Lorsque vous expédiez des articles à partir d’un entrepôt qui est configuré pour un traitement d’expédition entrepôt, vous ne pouvez expédier des articles que sur la base des documents origine que d’autres centres de la société ont lancés et transmis à l’entrepôt en vue d’une action.

> [!NOTE]
> Si votre entrepôt utilise le transbordement, et dispose d’emplacements, vous pouvez visualiser pour chaque ligne la quantité d’articles placés dans les emplacements transbordement. L’application calcule automatiquement ces quantités chaque fois que les champs de l’expédition sont mis à jour. S’il s’agit des articles correspondant à l’expédition que vous préparez, vous pouvez créer un prélèvement pour toutes les lignes, puis terminer l’expédition. En savoir plus sur [ Transborder des articles](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Expédier des articles avec une commande vente

Ce qui suit décrit comment expédier des articles pour une commande vente. Les étapes sont similaires pour les retours achat, les commandes service et les ordres de transfert sortants.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Ouvrez une commande vente existante, ou créez-en une nouvelle. En savoir plus sur [Vendre des produits](sales-how-sell-products.md).
3. Dans le champ **Qté à expédier**, indiquez la quantité expédiée.

    La valeur du champ **Qté expédiée** est mise à jour en conséquence. Si c’est une expédition partielle, la valeur est inférieure à la valeur dans le champ **Quantité**. En savoir plus sur [Traiter les livraisons partielles](sales-how-send-partial-shipments.md).
4. Sélectionnez l’action **Valider**.

> [!NOTE]
> Si votre organisation n’utilise pas de commandes vente, lorsque vous validez la facture vente, [!INCLUDE [prod_short](includes/prod_short.md)] suppose que vous avez expédié la totalité de la quantité. Si cela contredit le fonctionnement de votre organisation, nous vous recommandons d’utiliser les commandes vente et d’enregistrer les expéditions comme expliqué dans cet article.

## <a name="ship-items-with-a-warehouse-shipment"></a>Expédier des articles avec une expédition entrepôt

Premièrement, vous créez un document expédition à partir d’un document origine d’entreprise. Puis, vous prélevez les articles spécifiés pour l’expédition.

### <a name="create-a-warehouse-shipment"></a>Créer une expédition entrepôt

Généralement, l’employé chargé de l’expédition crée une expédition entrepôt. La procédure suivante décrit comment créer l’envoi manuellement dans la version par défaut de [!INCLUDE[prod_short](includes/prod_short.md)]. Cependant, votre organisation peut avoir automatisé une partie du processus, par exemple avec l’utilisation de scanners portables ou montés pris en charge par des fournisseurs externes.  

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expéditions entrepôt**, puis sélectionnez le lien associé.  
2. Choisissez **Nouveau**.  

    Renseignez les champs du raccourci **Général**. Lorsque vous récupérez des lignes document origine, certaines des informations de l’en-tête sont copiées dans chaque ligne.  

    Pour une configuration de stockage avec un prélèvement et un rangement suggérés : Si le magasin possède une zone et un emplacement par défaut pour les expéditions, les champs **Code zone** et **Code emplacement** seront renseignés, mais vous pouvez les modifier selon vos besoins.  

    > [!NOTE]  
    > Pour expédier des articles portant des codes classe entrepôt différents du code classe de l’emplacement indiqué dans le champ **Code emplacement** de l’en-tête du document, vous devez supprimer la valeur du champ **Code emplacement** de l’en-tête avant d’extraire les lignes des documents origine des articles.  
3. Choisissez l’action **Extraire documents origine**. La page **Documents origine** s’ouvre.

    À partir d’une expédition entrepôt nouvelle ou ouverte, vous pouvez utiliser la page **Filtres pour extr. doc. orig.** afin d’extraire les lignes du document origine lancé qui définissent les articles à recevoir ou à expédier.

    1. Choisissez l’action **Filtrer pour extr. doc. orig.**.  
    2. Pour configurer un nouveau filtre, entrez un code descriptif dans le champ **Code**, puis choisissez l’action **Modifier**.  
    3. Définissez le type de ligne document origine que vous souhaitez extraire en renseignant les champs de filtre appropriés.  
    4. Sélectionnez l’action **Exécuter**.  

    Toutes les lignes du document origine lancé qui correspondent aux critères du filtre sont à présent insérées sur la page **Expédition entrepôt** à partir de laquelle vous avez activé la fonction filtre.  

    Les combinaisons de filtres que vous définissez sont stockées sur la page **Filtres pour extr. doc. orig.** jusqu’à la prochaine utilisation. Le nombre de combinaisons de filtres est illimité. Vous pouvez modifier les critères à tout moment en choisissant l’action **Modifier**.

4. Sélectionnez le document origine pour lequel vous souhaitez expédier des articles, puis sélectionnez le bouton **OK**.  

Les lignes des documents origine s’affichent sur la page **Expédition entrepôt**. Le champ **Qté à expédier** est renseigné avec la quantité restante pour chaque ligne, mais vous pouvez modifier cette quantité selon vos besoins. Si vous avez supprimé la valeur du champ **Code emplacement** du raccourci **Général** avant d’accéder aux lignes, vous devez alors renseigner un code emplacement approprié sur chaque ligne expédition.  

> [!NOTE]  
> Vous ne pouvez pas expédier un nombre d’articles supérieur au nombre figurant dans le champ **Qté ouverte** de la ligne document origine. Pour expédier des articles supplémentaires, utilisez la fonction filtre pour récupérer un autre document origine contenant une ligne pour l’article concerné.  

Lorsque vous disposez des lignes à expédier, vous pouvez lancer le processus qui envoie les lignes pour enlèvement aux magasiniers.

### <a name="pick-and-ship"></a>Effectuer un prélèvement et une expédition

Généralement, un magasinier chargé du prélèvement crée un document prélèvement, ou ouvre un document prélèvement déjà créé.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Expéditions entrepôt**, puis sélectionnez le lien associé.
2. Sélectionnez l’expédition entrepôt que vous souhaitez prélever, puis sélectionnez l’action **Créer prélèvement**.
3. Renseignez les champs de la page de demande, puis cliquez sur le bouton **OK**. Le document prélèvement entrepôt spécifié est créé.

    Sinon, ouvrez un prélèvement entrepôt existant.
4. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements**, puis choisissez le lien associé. Sélectionnez le prélèvement entrepôt que vous souhaitez utiliser.

    Si l’entrepôt est configuré pour utiliser des emplacements, alors les lignes prélèvement sont converties en lignes action Prélever et Ranger.

    Si vous utilisez le prélèvement et le rangement suggérés, vous pouvez trier les lignes, attribuer un employé au prélèvement, définir un filtre de déconditionnement et imprimer les instructions de prélèvement.

5. Réalisez le prélèvement effectif des articles et placez-les dans l’emplacement expédition spécifié, ou dans la zone expédition, si vous n’avez pas d’emplacements.
6. Choisissez l’action **Enregistrer prélèvement**.

    Les champs **Qté à expédier** et **Statut document** de l’en-tête du document expédition sont mis à jour. Les articles prélevés ne peuvent plus être prélevés pour d’autres expéditions ou pour des opérations internes.
7. Imprimez les documents expédition, préparez les colis, puis validez l’expédition.

Pour plus d’informations sur le prélèvement pour les expéditions entrepôt, voir [Prélever des articles pour l’expédition entrepôt](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Vous pouvez également utiliser la feuille prélèvement pour regrouper plusieurs instructions de prélèvement en une seule instruction (pour plusieurs expéditions) et optimiser ainsi l'efficacité du prélèvement dans l'entrepôt. En savoir plus sur [Planifier un prélèvement dans des feuilles](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Lorsque vous attendez l’arrivée d’articles spécifiques dans l’entrepôt et que vous utilisez la fonctionnalité de transbordement, [!INCLUDE[prod_short](includes/prod_short.md)] calcule, pour chaque ligne feuille prélèvement ou expédition, la quantité article figurant dans l’emplacement transbordement. Il met à jour ce champ chaque fois que vous fermez ou ouvrez le document d’expédition ou la feuille. En savoir plus sur [ Transborder des articles](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
