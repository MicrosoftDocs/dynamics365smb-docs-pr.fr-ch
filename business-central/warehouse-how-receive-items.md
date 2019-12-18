---
title: Comment recevoir des articles | Microsoft Docs
description: Lorsque les articles arrivent dans un entrepôt configuré pour appeler un traitement de réception entrepôt, vous devez extraire les lignes du document origine lancé ayant déclenché leur réception.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d007c3a9433807f75e667e130c0b79355a4a051a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876766"
---
# <a name="receive-items"></a>Réceptionner des articles
Lorsque les articles arrivent dans un entrepôt qui n'est pas configuré pour un traitement de réception entrepôt, enregistrez simplement la réception du document d'entreprise associé, comme une commande achat, un retour vente ou un ordre de transfert entrant.

Lorsque les articles arrivent dans un entrepôt configuré pour appeler un traitement de réception entrepôt, vous devez extraire les lignes du document origine lancé ayant déclenché leur réception. En présence d'emplacements, vous pouvez soit accepter l'emplacement par défaut qui est renseigné, soit renseigner l'emplacement de rangement de l'article concerné si cet article n'a jamais été utilisé dans l'entrepôt. Vous devez ensuite renseigner les quantités d'articles reçus et valider la réception.  

## <a name="to-receive-items-with-a-purchase-order"></a>Pour recevoir des articles avec une commande achat
Ce qui suit décrit comment recevoir des articles avec une commande achat. Les étapes sont similaires pour les retours vente et les ordres de transfert.  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat**, puis sélectionnez le lien associé.
2. Ouvrez une commande achat existante, ou créez-en une nouvelle. Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).
3. Dans le champ **Qté à recevoir**, indiquez la quantité reçue.

    La valeur du champ **Qté reçue** est mise à jour en conséquence. Si c'est une réception partielle, la valeur est inférieure à la valeur dans le champ **Quantité**.
4. Sélectionnez l'action **Valider**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Pour recevoir des articles avec une réception entrepôt
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Réceptions entrepôt**, puis sélectionnez le lien associé.  
2.  Sélectionnez l'action **Nouveau**.  

    Renseignez les champs du raccourci **Général**. Lorsque vous récupérez des lignes document origine, certaines des informations de l'en-tête sont copiées dans chaque ligne.  

    Pour une configuration de stockage avec un prélèvement et un rangement suggérés : Si le magasin possède une zone et un emplacement par défaut pour les réceptions, les champs **Code zone** et **Code emplacement** seront renseignés, mais vous pouvez les modifier selon vos besoins.  

    > [!NOTE]  
    >  Pour recevoir des articles portant des codes classe entrepôt différents du code classe de l'emplacement indiqué dans le champ **Code emplacement** de l'en-tête du document, vous devez supprimer la valeur du champ **Code emplacement** de l'en-tête avant d'extraire les lignes des documents origine des articles.  
3.  Choisissez l'action **Extraire documents origine**. La page **Documents origine** s'ouvre.

    À partir d'une réception entrepôt nouvelle ou ouverte, vous pouvez utiliser la page **Filtres pour extr. doc. orig.** afin d'extraire les lignes du document origine lancé qui définissent les articles à recevoir ou à expédier.

    1. Choisissez l'action **Filtrer pour extr. doc. orig.**.  
    2. Pour configurer un nouveau filtre, entrez un code descriptif dans le champ **Code**, puis choisissez l'action **Modifier**.  
    3. Définissez le type de ligne document origine que vous souhaitez extraire en renseignant les champs de filtre appropriés.  
    4. Sélectionnez l'action **Exécuter**.  

    Toutes les lignes du document origine lancé qui correspondent aux critères du filtre sont à présent insérées sur la page **Réception entrepôt** à partir de laquelle vous avez activé la fonction filtre.  

    Les combinaisons de filtres que vous définissez sont stockées sur la page **Filtres pour extr. doc. orig.** jusqu'à la prochaine utilisation. Le nombre de combinaisons de filtres est illimité. Vous pouvez modifier les critères à tout moment en choisissant l'action **Modifier**.

4.  Sélectionnez le document origine pour lequel vous souhaitez réceptionner des articles, puis sélectionnez le bouton **OK**.  

    Les lignes des documents origine s'affichent sur la page **Réception entrepôt**. Le champ **Qté à recevoir** est renseigné avec la quantité restante pour chaque ligne, mais vous pouvez modifier cette quantité selon vos besoins. Si vous avez supprimé la valeur du champ **Code emplacement** du raccourci **Général** avant d'accéder aux lignes, vous devez alors renseigner un code emplacement approprié sur chaque ligne réception.  

    > [!NOTE]  
    >  Pour renseigner le champ **Qté à recevoir** sur toutes les lignes à zéro, choisissez l'action **Supprimer qté à recevoir**. Pour y insérer à nouveau la quantité restante, choisissez l'action **Remplir qté à recevoir**.  

    > [!NOTE]  
    >  Vous ne pouvez pas recevoir un nombre d'articles supérieur au nombre figurant dans le champ **Qté ouverte** de la ligne document origine. Pour recevoir des articles supplémentaires, récupérez un autre document origine contenant une ligne pour l'article concerné en utilisant la fonction filtre afin d'obtenir les documents origine où figure cet article.  

5.  Validez la réception entrepôt. Les champs relatifs à la quantité dans les documents origine sont mis à jour et les articles enregistrés dans le cadre du stock de la société.  

En cas d'utilisation d'un rangement entrepôt, les lignes réception sont transmises à la fonction de rangement entrepôt. Les articles, bien que réceptionnés, ne peuvent pas être prélevés avant d'avoir été rangés. Les articles réceptionnés sont identifiés en tant que stock disponible une fois le rangement enregistré uniquement.  

En cas de non-utilisation d'un rangement entrepôt et d'utilisation d'emplacements, le rangement des articles est enregistré dans l'emplacement spécifié sur la ligne document origine.  

> [!NOTE]  
>  En utilisant la fonction **Valider et Imprimer**, vous effectuez à la fois la validation de la réception et l'impression d'une instruction de rangement qui indique les articles à ranger en stock.  
>   
>  En cas d'utilisation d'un prélèvement et d'un rangement suggérés, les modèles rangement sont utilisés pour procéder au calcul du meilleur emplacement de rangement des articles. Il est ensuite imprimé sur l'instruction de rangement.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
