---
title: "Procédure d'archivage des documents vente et achat | Microsoft Docs"
description: "Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d'origine."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Archiver des documents
Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d'origine.

## <a name="to-set-up-automatic-document-archiving"></a>Pour configurer l'archivage automatique des documents  
Vous pouvez configurer l'archivage automatique des commandes vente et achat, des devis, des commandes ouvertes et des retours, avant de supprimer des documents.

La procédure suivante décrit comment configurer l'archivage automatique des documents vente. La procédure est identique pour les documents achat.
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône"), entrez **Paramètres ventes**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Paramètres ventes**, renseignez les champs comme suit.

|Champ|Désignation|
|-----|-----------|
|**Archivage des devis**|**Jamais** pour ne jamais archiver les devis lorsqu'ils sont supprimés. **Question** pour demander à l'utilisateur s'il souhaite archiver les devis lorsqu'ils sont supprimés. **Toujours** pour archiver automatiquement les devis lorsqu'ils sont supprimés.|
|**Archivage des commandes vente ouvertes**|Permet d'archiver automatiquement les commandes ouvertes vente lorsqu'elles sont supprimées.|
|**Arch. commandes et retours**|Permet d'archiver automatiquement les commandes vente lorsqu'elles sont supprimées.|

## <a name="to-archive-a-sales-order"></a>Pour archiver une commande vente
La procédure suivante décrit comment archiver une commande vente. La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente**, puis sélectionnez le lien connexe.  
2.  Ouvrez une commande vente que vous souhaitez archiver.  
3.  Sélectionnez l'action **Archiver document**.

La commande vente est archivée. Vous pouvez l'afficher dans la fenêtre **Commandes vente archivées**. Vous pouvez également l'utiliser pour recréer la commande vente d'origine.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Pour recréer une commande vente à partir de l'archive
La procédure suivante décrit comment recréer une commande vente. La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Commandes vente archivées**, puis sélectionnez le lien connexe.
2.  Sélectionnez la commande vente archivée que vous voulez recréer, puis sélectionnez l'action **Restaurer**.  

La commande vente est créée et ajoutée à la fenêtre **Commandes vente**.

## <a name="to-delete-archived-sales-orders"></a>Pour supprimer des commandes vente archivées
La procédure suivante décrit comment supprimer des commandes vente archivées. La procédure est identique pour les autres documents achat et vente archivés.

1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Supprimer versions cde vente archivées**, puis sélectionnez le lien connexe.  
2.  Dans la fenêtre **Supprimer versions cde vente archivées**, sélectionnez les filtres appropriés.  
3.  Cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Suivre des lignes document](across-how-to-track-document-lines.md)  
[Ventes](sales-manage-sales.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

