---
title: Archiver les documents vente et les documents achat
description: Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d’origine.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: 2fc414dcd9a8d9c978ee08eb5d19b960fa21a2d9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511872"
---
# <a name="archive-documents"></a>Archiver des documents
Vous pouvez archiver des commandes vente et achat, des devis, des commandes retour, et des commandes ouvertes, par exemple parce que vous voulez enregistrer une copie d’un document pour la réutiliser plus tard. Vous pouvez archiver des documents vente ou achat plusieurs fois, en enregistrant une version archivée différente chaque fois.

Pour les documents vente archivés où l’original existe et n’est pas validé, vous pouvez utiliser la fonction **Restaurer** pour remplacer l’original par la version archivée du document. Ceci est commode si vous devez restaurer le contenu d’un document à un état précédemment.

Pour les documents archivés où l’original est désactivé, vous pouvez réutiliser le contenu uniquement en copiant les données, par exemple avec la fonction **Copier à partir du document**.  

## <a name="to-set-up-automatic-document-archiving"></a>Pour configurer l’archivage automatique des documents

Vous pouvez configurer l’archivage automatique des commandes vente et achat, des devis, des commandes ouvertes et des retours, avant de supprimer des documents.

La procédure suivante décrit comment configurer l’archivage automatique des documents vente. La procédure est identique pour les documents achat.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.
2. Sur la page **Paramètres ventes**, renseignez les champs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Notamment pour le champ **Archiver devis**, le tableau suivant décrit la différence entre les options.

|Option|Description|
|------|-----------|
|**Jamais**| N’archivez jamais les devis lorsqu’ils sont supprimés.|
|**Question**|Sélectionnez pour demander à l’utilisateur s’il souhaite archiver les devis lorsqu’ils sont supprimés.|
|**Toujours**|Sélectionnez pour archiver automatiquement les devis lorsqu’ils sont supprimés.|

## <a name="to-archive-a-sales-order"></a>Pour archiver une commande vente

La procédure suivante décrit comment archiver une commande vente. La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Ouvrez une commande vente que vous souhaitez archiver.  
3. Sélectionnez l’action **Archiver document**.

La commande vente est archivée. Vous pouvez l’afficher sur la page **Commandes vente archivées**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Pour restaurer une commande vente non validée depuis les archives

La procédure suivante décrit comment insérer le contenu d’une commande vente archivée dans la commande vente d’origine. Cela n’est possible que lorsque le document source n’a pas été validé. La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Archives commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez la commande vente archivée, ou une version de celle-ci, que vous voulez restaurer, puis sélectionnez l’action **Restaurer**.  

Le contenu de la commande vente d’origine est remplacé par celui de la version archivée sélectionnée.

## <a name="to-delete-archived-sales-orders"></a>Pour supprimer des commandes vente archivées

La procédure suivante décrit comment supprimer des commandes vente archivées. La procédure est identique pour les autres documents achat et vente archivés.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Archives commandes vente**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Supprimer versions cde vente archivées**, puis, sur la page **Supprimer versions cde vente archivées**, sélectionnez les filtres appropriés.  
3. Choisissez le bouton **OK**.

## <a name="see-also"></a>Voir aussi

[Suivre des lignes document](across-how-to-track-document-lines.md)  
[Ventes](sales-manage-sales.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
