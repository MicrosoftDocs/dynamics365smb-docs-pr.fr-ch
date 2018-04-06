---
title: "Créer des fiches article pour des biens ou des services| Microsoft Docs"
description: "Vous créez des fiches article pour les services que vous vendez en heures et pour les marchandises physiques, comme les éléments d'assemblage, les produits finis, les composants, ou les matières premières que vous vendez de votre stock."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9643e71c29adf4b4be1d9d474832e3e29f2c21d8
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="register-new-items"></a>Enregistrer de nouveaux articles
Les articles, entre autres produits, sont la base de votre activité, les biens ou les services que vous commercialisez. Chaque article doit être enregistré en tant que fiche article.

Les fiches article contiennent les informations nécessaires à l'achat, le stockage, la vente, la livraison et la comptabilisation des articles.

La fiche article peut être de type **Stock** ou **Service** pour spécifier si l'article est une unité physique ou une unité temporelle de main-d'œuvre. Mis à part certains champs liés à l'aspect physique d'un article, tous les champs d'une fiche article fonctionnent de la même manière pour les articles de stock et les services. Pour plus d'informations sur la vente d'un article , reportez-vous à [Vendre des produits](sales-how-sell-products.md) ou à [Facturer les ventes](sales-how-invoice-sales.md).

Un article peut être structuré comme article parent avec les éléments enfants sous-jacents dans une nomenclature. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une nomenclature peut être une nomenclature d'assemblage ou une nomenclature de production, selon son utilisation. Pour plus d'informations, reportez-vous à [Utiliser les nomenclatures](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Si des modèles article existent pour différents types d'articles, une fenêtre s'affiche automatiquement lorsque vous créez une nouvelle fiche article à partir de laquelle vous pouvez sélectionner un modèle article approprié. Si un seul modèle article existe, les nouvelles fiches article utiliseront toujours ce modèle.

Si vous achetez le même article chez plusieurs fournisseurs, vous pouvez lier ces fournisseurs à la fiche article. Les fournisseurs s'affichent alors dans la fenêtre **Catalogue fournisseur articles**, de sorte que vous pouvez facilement sélectionner un autre fournisseur.

## <a name="to-create-a-new-item-card"></a>Pour créer une fiche article
1. Cliquez sur l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Articles**, sélectionnez l'action **Nouveau**.

    Si un seul modèle article existe, une nouvelle fiche article avec certains champs renseignés à l'aide des informations provenant du modèle s'ouvre.
3. Dans la fenêtre **Sélectionnez un modèle pour un nouvel article**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche article.
4. Cliquez sur le bouton **OK**. Une nouvelle fiche article avec certains champs renseignés à l'aide des informations provenant du modèle s'ouvre.
5. Continuez à renseigner ou modifier les champs de la fiche article selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Dans le champ **Mode évaluation stock**, vous configurez la façon dont le coût unitaire de l'article est calculé en estimant le flux d'articles dans votre société. Il existe cinq modes évaluation stock disponibles, selon le type d'article. Pour plus d'informations, [Détails de conception : modes évaluation stock](design-details-costing-methods.md).
>
> Si vous sélectionnez **Moyenne**, le coût unitaire de l'article est calculé comme le coût unitaire moyen à chaque moment après un achat. Le stock est évalué avec la supposition que tous les stocks sont vendus simultanément. Avec ce paramètre, vous pouvez choisir le champ **Coût unitaire**, dans la fenêtre **Aperçu calc. coût moyen** de la fiche article pour afficher l'historique des transactions à partir duquel est calculé le coût moyen

Sur le raccourci **Prix et Validation**, vous pouvez afficher les prix spécifiques ou les remises accordées pour l'article si certains critères sont réunis, par exemple le client, la quantité minimum de commande ou la date de fin. Chaque ligne représente un prix spécial ou une remise ligne. Chaque colonne représente un critère qui doit s'appliquer pour garantir le prix spécial que vous saisissez dans le champ **Prix** ou la remise ligne que vous saisissez dans le champ **% remise ligne**. Pour plus d'informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

L'article est désormais enregistré, et la fiche article est prête à être utilisée sur les documents d'achat et de vente.

Si vous souhaitez utiliser cette fiche article comme modèle lorsque vous créez de nouvelles fiches article, enregistrez-la comme modèle. Pour plus d'informations, reportez-vous à la section suivantes.

## <a name="to-save-the-item-card-as-a-template"></a>Pour enregistrer la fiche article en tant que modèle
1. Dans la fenêtre **Fiche article**, sélectionnez l'action **Sauvegarder comme modèle**. La fenêtre **Modèle article** s'ouvre et affiche la fiche article comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles, sélectionnez l'action **Axes analytiques**. La fenêtre **Modèles axe** s'ouvre et affiche tous les codes axe qui sont définis pour l'article.
4. Modifiez ou entrez les codes axe s'appliquant aux nouvelles fiches article créées à l'aide du modèle.
5. Lorsque vous avez terminé le nouveau modèle article, cliquez sur le bouton **OK**.

Le modèle article est ajouté à la liste des modèles article. Vous pouvez ainsi l'utiliser pour créer des fiches article.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Pour configurer plusieurs fournisseurs pour un article  
Si vous achetez le même article chez plusieurs fournisseurs, vous devez saisir, pour chacun des fournisseurs de cet article des informations concernant, par exemple, ses prix, ses délais, ses escomptes, etc.  

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'article concerné, puis cliquez sur l'action **Modifier**.  
3.  Sélectionnez l'action **Fournisseurs**.  
4.  Cliquez sur le champ **N° fournisseur**, puis sélectionnez le fournisseur à paramétrer pour l'article.  
5.  De manière facultative, renseignez les autres champs.  
6.  Répétez les étapes 2 à 5 pour chaque fournisseur auprès de qui vous souhaitez acheter l'article.

Les fournisseurs s'affichent maintenant dans la fenêtre **Catalogue fournisseur articles** (que vous ouvrez à partir de la fiche article), de sorte que vous pouvez facilement sélectionner un autre fournisseur.

## <a name="see-also"></a>Voir aussi
  [STOCKS ET EN-COURS](inventory-manage-inventory.md)  
  [Achats](purchasing-manage-purchasing.md)  
  [Ventes](sales-manage-sales.md)  
  [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

