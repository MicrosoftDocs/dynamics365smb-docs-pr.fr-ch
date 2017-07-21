---
title: Inventaire, ajustement et reclassement du stock| Microsoft Docs
description: "Décrit la manière d'effectuer un inventaire physique, faire des ajustements négatifs ou positifs, et comment modifier des informations, telles que le magasin ou le numéro de lot, sur des écritures comptables article ou des écritures entrepôt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Procédure : Inventaire, ajustement et reclassement du stock
Vous devez effectuer un inventaire (c'est-à-dire compter tous les articles disponibles) au moins une fois par exercice pour vérifier si la quantité enregistrée dans la base de données est identique à la quantité réelle en stock dans les entrepôts. Lorsque vous connaissez la quantité physique réelle, vous devez la valider dans la comptabilité dans le cadre de l' évaluation du stock de fin d'exercice.

Bien que vous comptiez tous les articles du stock au moins une fois par an, vous pouvez avoir décidé de compter certains articles plus souvent, parce qu'ils ont plus de valeur ou parce qu'ils sont très demandés et représentent une partie importante de votre activité. Pour cela, vous pouvez affecter des périodes d'inventaire spéciales à ces articles. Pour plus d'informations, reportez-vous à la section « Effectuer un inventaire tournant ».

Pour ajuster les quantités en stock enregistrées, pour inventaire ou à d'autres fins, vous pouvez utiliser une feuille article pour modifier les écritures comptables inventaire directement sans valider les transactions commerciales. Sinon, vous pouvez ajuster pour un article distinct de la fiche article.

Pour modifier les attributs d'écritures comptables article et les quantités, vous pouvez utiliser la feuille reclassement article. Les attributs courants pour les reclassements incluent les numéros de série et/ou de lot, les dates d'expiration et les dimensions.

## <a name="to-perform-a-physical-inventory"></a>Pour effectuer un inventaire physique
A la fin de l'exercice comptable, ou plus souvent, vous devez effectuer un inventaire, c'est-à-dire compter les articles réellement disponibles, pour vérifier si la quantité enregistrée correspond à la quantité réelle du stock. S'il existe des différences, vous devez les valider dans les comptes article avant de procéder à l'évaluation du stock.

Outre la tâche de comptage réelle, le processus complet implique les trois tâches suivantes :

- Calculer le stock prévu.
- Imprimer l'état à utiliser lors du comptage.
- Saisir et valider le stock réel compté.

### <a name="to-calculate-the-expected-inventory"></a>Pour calculer le stock prévu
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles inventaire**, puis sélectionnez le lien connexe.
2. Choisissez l'action **Calculer stock**.
3. Dans la fenêtre **Calculer stock**, indiquez les conditions à utiliser pour créer les lignes feuille, par exemple si vous souhaitez inclure les articles pour lesquels aucun stock n'est enregistré.
4. Définissez des filtres si vous souhaitez uniquement calculer le stock pour certains articles, emplacements, magasins ou axes.
5. Cliquez sur le bouton **OK**.

> [!NOTE]  
>   Les écritures article sont traitées en fonction des informations que vous avez indiquées, et les lignes sont créées dans la feuille inventaire. Notez que le champ **Qté (constatée)** est renseigné automatiquement avec la même quantité que le champ **Qté (calculée)**. Avec cette fonction, vous n'avez pas besoin d'entrer le stock disponible pour les articles dont le nombre correspond à la quantité calculée. Toutefois, si la quantité comptée diffère de ce qui est saisi dans le champ **Qté (calculée)**, vous devez la remplacer par la quantité réellement comptée.

### <a name="to-print-the-report-used-when-counting"></a>Pour imprimer l'état à utiliser lors du comptage
1. Dans la fenêtre **Feuille inventaire** contenant le stock prévu calculé, choisissez l'action **Imprimer**.
2. Dans la fenêtre **Liste d'inventaire**, indiquez si l'état doit indiquer la quantité calculée et si l'état doit répertorier les articles en stock par numéros de série/lot.
3. Définissez des filtres si vous souhaitez uniquement imprimer l'état pour certains articles, emplacements, magasins ou axes.
4. Cliquez sur le bouton **Imprimer**.

Les employés peuvent maintenant poursuivre le comptage du stock et noter les éventuelles différences sur l'état imprimé.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Pour saisir et valider le stock réel compté
1. Sur chaque ligne de la fenêtre **Feuilles inventaire** sur laquelle le stock réellement disponible, comme déterminé par le comptage, diffère de la quantité calculée, saisissez la quantité réellement disponible dans le champ **Qté (constatée)**.

    Les champs associés sont mis à jour en conséquence.

    > [!NOTE]  
>   Si le décompte fait apparaître des différences dues à des articles validés avec des codes magasin incorrects, n'indiquez pas les différences dans la feuille inventaire. Au lieu de cela, utilisez la feuille reclassement ou un ordre de transfert pour rediriger les articles vers les magasins appropriés. Pour plus d'informations, voir Feuilles reclassement article ou Procédure : Comment créer des ordres de transfert.

2. Pour ajuster les quantités calculées avec les quantités comptées réelles, choisissez **Valider**.

    Les écritures comptables article et les écritures comptables inventaire sont créées. Ouvrez la fiche article pour visualiser les écritures comptables inventaire ainsi obtenues.

3. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
4. Pour vérifier l'inventaire de stock, ouvrez la fiche article en question, puis choisissez **Écritures comptables inventaire**.

# <a name="to-perform-cycle-counting"></a>Pour effectuer l'inventaire périodique
Bien que vous comptiez tous les articles du stock au moins une fois par an, vous pouvez avoir décidé de compter certains articles plus souvent, parce qu'ils ont plus de valeur ou parce qu'ils sont très demandés et représentent une partie importante de votre activité. Pour cela, vous pouvez affecter des périodes d'inventaire spéciales à ces articles.

> [!NOTE]  
>   Si votre magasin est configuré pour le prélèvement et rangement suggérés, vous utilisez d'abord la fenêtre **Feuille inventaire entrepôt**, puis la fonction **Calculer ajustement entrepôt** de la fenêtre **Feuille article**.

## <a name="to-set-up-counting-periods"></a>Pour configurer des périodes d'inventaire
Un inventaire est généralement effectué en fonction d'intervalles réguliers (par exemple, tous les mois, tous les trimestres ou toutes les années). Vous pouvez configurer les périodes d'inventaire nécessaires.

Configurez les périodes d'inventaire que vous souhaitez utiliser, puis affectez-en une à chaque article. Lorsque vous effectuez un inventaire et que vous utilisez **Calculer période d'inventaire** de la feuille inventaire, les lignes des articles sont créées automatiquement.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Périodes inventaire**, puis sélectionnez le lien connexe.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Pour affecter une période d'inventaire à un article  
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.  
2. Sélectionnez l'article auquel vous souhaitez affecter une période d'inventaire.  
3. Dans le champ **Code période inventaire stock**, sélectionnez la période d'inventaire appropriée.  
4. Cliquez sur le bouton **Oui** pour modifier le code et la calculer la première période d'inventaire de l'article. La prochaine fois que vous choisissez de calculer une période d'inventaire dans la feuille inventaire, l'article s'affichera en tant que ligne dans la fenêtre **Sélection article inventaire**. Vous pouvez ensuite commencer à compter l'article sur une base périodique.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Pour lancer un décompte selon des périodes d'inventaire
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille inventaire**, puis sélectionnez le lien connexe.
2. Choisissez l'action **Calculer la période d'inventaire**.

    La fenêtre **Sélection article inventaire** qui s'ouvre affiche les articles auxquels des périodes d'inventaire ont été affectés et qui doivent être comptés en fonction de leurs périodes d'inventaire.
3. Effectuer l'inventaire physique. Pour plus d'informations, voir la section « Pour effectuer un inventaire physique ».

## <a name="to-adjust-the-inventory-of-one-item"></a>Pour ajuster le stock d'un article
Après avoir effectué un inventaire d'un article dans votre module Distribution - Stocks, vous pouvez utiliser la fonction **Ajuster stock** pour enregistrer la quantité réelle en stock.

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Sélectionnez l'article pour lequel vous souhaitez ajuster le stock, puis sélectionnez l'action **Ajuster stock**.
3. Dans le champ **Nouveau stock**, entrez la quantité en stock que vous souhaitez enregistrer pour l'article.
4. Cliquez sur le bouton **OK**.

Le stock de l'article est désormais ajusté. La nouvelle quantité s'affiche dans le champ **Stock actuel** de la fenêtre **Ajuster stock** et dans le champ **Stock** de la fenêtre **Fiche article**.

Vous pouvez également utiliser la fonction **Ajuster stock** comme un moyen simple de placer les articles achetés dans le stock si vous n'utilisez pas des factures achat ou des commandes pour enregistrer vos achats. Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Après avoir ajusté le stock, vous devez le mettre à jour avec la valeur actuelle calculée. Pour plus d'informations, voir [Procédure : réévaluer le stock](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Pour ajuster la quantité en stock d'un ou de plusieurs articles
Dans la fenêtre **feuille article**, vous pouvez valider la transaction article directement pour ajuster le stock en fonction des achats, ventes et d'ajustements positifs et négatifs sans utiliser de documents.

Si vous utilisez fréquemment la feuille article pour comptabiliser des lignes feuille identiques ou analogues (par exemple, des lignes en rapport avec la consommation de matériel), vous pouvez utiliser la fenêtre **Feuille article standard** pour simplifier cette tâche récurrente. Pour plus d'informations, reportez-vous à la section « Feuilles standard » de [Utilisation de feuilles comptabilité](ui-work-general-journals.md).

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles article**, puis sélectionnez le lien connexe.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Choisissez l'action **Valider** pour créer des ajustements de stock.

> [!NOTE]  
>   Après avoir ajusté le stock, vous devez le mettre à jour avec la valeur actuelle calculée. Pour plus d'informations, voir [Procédure : réévaluer le stock](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Pour reclasser le numéro de lot d'un article
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles reclassement article**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Feuilles reclassement article**, renseignez les champs selon vos besoins.
3. Dans le champ **N° lot**, entrez l'actuel numéro de lot de l'article.
4. Dans le champ **N° lot**, entrez le nouveau numéro de lot de l'article.
5. Sélectionnez l'action **Valider**.

## <a name="see-also"></a>Voir aussi
[Stock](inventory-manage-inventory.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

