---
title: "Procédure : enregistrer de nouveaux articles| Microsoft Docs"
description: "Créez des fiches pour les nouveaux produits physiques que vous vendez à partir du stock en pièces, ou pour les services que vous vendez sous formes d&quot;heures."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 582e006291e51e19d80304d24ae055ce6ac8d698
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-items"></a>Procédure : enregistrer de nouveaux articles
Les articles, entre autres produits, sont la base de votre activité, les biens ou les services que vous commercialisez. Chaque article doit être enregistré en tant que fiche article.

Les fiches article contiennent les informations nécessaires à l'achat, le stockage, la vente, la livraison et la comptabilisation des articles.

La fiche article peut être de type **Stock** ou **Service** pour spécifier si l'article est une unité physique ou une unité temporelle de main-d'œuvre. Mis à part certains champs liés à l'aspect physique d'un article, tous les champs d'une fiche article fonctionnent de la même manière pour les articles de stock et les services. Pour plus d'informations sur la vente d'un article , reportez-vous à [Procédure : vendre des produits](sales-how-sell-products.md) ou à [Procédure : facturer les ventes](sales-how-invoice-sales.md).

Un article peut être structuré comme article parent avec les éléments enfants sous-jacents dans une nomenclature. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une nomenclature est appelée une nomenclature d'assemblage. Les nomenclatures d'assemblage permettent de structurer les articles parents que vous vendez sous forme de kits constitués des composants du parent ou que vous assemblez pour commande ou stock. Pour plus d'informations, reportez-vous à [Procédure : utiliser les nomenclatures](inventory-how-work-BOMs.md).

**Remarque** : si des modèles article existent pour différents types d'articles, une fenêtre s'affiche automatiquement lorsque vous créez une nouvelle fiche article à partir de laquelle vous pouvez sélectionner un modèle article approprié. Si un seul modèle article existe, les nouvelles fiches article utiliseront toujours ce modèle.

## <a name="to-create-a-new-item-card"></a>Pour créer une fiche article
1. Sur la page d'accueil, sélectionnez l'action **Articles** pour ouvrir la liste des article existants.  
2. Dans la fenêtre **Articles**, sélectionnez l'action **Nouveau**.

    Si un seul modèle article existe, une nouvelle fiche article avec certains champs renseignés à l'aide des informations provenant du modèle s'ouvre.
3. Dans la fenêtre **Sélectionnez un modèle pour un nouvel article**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche article.
4. Cliquez sur le bouton **OK**. Une nouvelle fiche article avec certains champs renseignés à l'aide des informations provenant du modèle s'ouvre.
5. Continuez à renseigner ou modifier les champs de la fiche article selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sur le raccourci **Prix et Validation**, vous pouvez afficher les prix spécifiques ou les remises accordées pour l'article si certains critères sont réunis, par exemple le client, la quantité minimum de commande ou la date de fin. Chaque ligne représente un prix spécial ou une remise ligne. Chaque colonne représente un critère qui doit s'appliquer pour garantir le prix spécial que vous saisissez dans le champ **Prix** ou la remise ligne que vous saisissez dans le champ **% remise ligne**. Pour plus d'informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

L'article est désormais enregistré, et la fiche article est prête à être utilisée sur les documents d'achat et de vente.

Si vous souhaitez utiliser cette fiche article comme modèle lorsque vous créez de nouvelles fiches article, enregistrez-la comme modèle. Pour plus d'informations, reportez-vous à la section suivantes.

## <a name="to-save-the-item-card-as-a-template"></a>Pour enregistrer la fiche article en tant que modèle
1. Dans la fenêtre **Fiche article**, sélectionnez l'action **Sauvegarder comme modèle**. La fenêtre **Modèle article** s'ouvre et affiche la fiche article comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles **, sélectionnez l'action **Axes analytiques**. La fenêtre **Modèles axe** s'ouvre et affiche tous les codes axe qui sont définis pour l'article.
4. Modifiez ou entrez les codes axe s'appliquant aux nouvelles fiches article créées à l'aide du modèle.
5. Lorsque vous avez terminé le nouveau modèle article, cliquez sur le bouton **OK**.

Le modèle article est ajouté à la liste des modèles article. Vous pouvez ainsi l'utiliser pour créer des fiches article.

## <a name="see-also"></a>Voir aussi
  [Stock](inventory-manage-inventory.md)  
  [Achats](purchasing-manage-purchasing.md)  
  [Ventes](sales-manage-sales.md)  
  [Utilisation de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
