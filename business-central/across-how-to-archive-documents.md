---
title: Procédure d'archivage des documents vente et achat | Microsoft Docs
description: Vous pouvez archiver des commandes vente et achat, des devis, des retours et des commandes ouvertes, et vous pouvez utiliser le document archivé pour recréer le document d'origine.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8a3bda8a7f4f953265e4191ac65b052e5af80157
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305515"
---
# <a name="archive-documents"></a>Archiver des documents
Vous pouvez archiver des commandes vente et achat, des devis, des commandes retour, et des commandes ouvertes, par exemple parce que vous voulez enregistrer une copie d'un document pour la réutiliser plus tard. Vous pouvez archiver des documents vente ou achat plusieurs fois, en enregistrant une version archivée différente chaque fois.

Pour les documents archivés où l'original existe et n'est pas validé, vous pouvez utiliser la fonction **Restaurer** pour remplacer l'original par la version archivée du document. Ceci est commode si vous devez restaurer le contenu d'un document à un état précédemment.

Pour les documents archivés où l'original est désactivé, vous pouvez réutiliser le contenu qu'en copiant les données, par exemple avec la fonction **Copier document**.   

## <a name="to-set-up-automatic-document-archiving"></a>Pour configurer l'archivage automatique des documents  
Vous pouvez configurer l'archivage automatique des commandes vente et achat, des devis, des commandes ouvertes et des retours, avant de supprimer des documents.

La procédure suivante décrit comment configurer l'archivage automatique des documents vente. La procédure est identique pour les documents achat.
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres ventes**, puis sélectionnez le lien associé.
2. Sur la page **Paramètres ventes**, renseignez les champs comme suit.

|Champ|Désignation|
|-----|-----------|
|**Archivage des devis**|**Jamais** pour ne jamais archiver les devis lorsqu'ils sont supprimés. **Question** pour demander à l'utilisateur s'il souhaite archiver les devis lorsqu'ils sont supprimés. **Toujours** pour archiver automatiquement les devis lorsqu'ils sont supprimés.|
|**Archivage des commandes vente ouvertes**|Permet d'archiver automatiquement les commandes ouvertes vente lorsqu'elles sont supprimées.|
|**Arch. commandes et retours**|Permet d'archiver automatiquement les commandes vente lorsqu'elles sont supprimées.|

## <a name="to-archive-a-sales-order"></a>Pour archiver une commande vente
La procédure suivante décrit comment archiver une commande vente. La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.  
2.  Ouvrez une commande vente que vous souhaitez archiver.  
3.  Sélectionnez l'action **Archiver document**.

La commande vente est archivée. Vous pouvez l'afficher sur la page **Commandes vente archivées**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Pour restaurer une commande vente non validée depuis les archives
La procédure suivante décrit comment insérer le contenu d'une commande vente archivée dans la commande vente d'origine. Cela n'est possible que lorsque le document source n'a pas été validé. La procédure est identique pour les commandes, les commandes ouvertes, les retours et les devis.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente archivées**, et sélectionnez le lien associé.
2. Sélectionnez la commande vente archivée, ou une version de celle-ci, que vous voulez restaurer, puis sélectionnez l'action **Restaurer**.  

Le contenu de la commande vente d'origine est remplacé par celui de la version archivée sélectionnée.

## <a name="to-delete-archived-sales-orders"></a>Pour supprimer des commandes vente archivées
La procédure suivante décrit comment supprimer des commandes vente archivées. La procédure est identique pour les autres documents achat et vente archivés.

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer versions cde vente archivées**, et sélectionnez le lien associé.  
2.  Sur la page **Supprimer versions cde vente archivées**, sélectionnez les filtres appropriés.  
3.  Choisissez le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Suivre des lignes document](across-how-to-track-document-lines.md)  
[Ventes](sales-manage-sales.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
