---
title: Prélever pour la fabrication, l’assemblage ou les tâches dans l’entrepôt de base
description: Lorsque l’entrepôt appelle un traitement de prélèvement sans appeler de traitement d’expédition, vous pouvez utiliser la page Prélèvement stock pour organiser et enregistrer le prélèvement des composants.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617892"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Prélever pour la fabrication, l’assemblage ou les tâches dans les configurations de stockage de base

Le mode de rangement de vos composants de prélèvement pour les ordres de fabrication ou d’assemblage dépend de la configuration du stockage en tant qu’emplacement. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Prélever pour la fabrication dans les configurations de stockage de base

Si un emplacement exige un traitement de prélèvement, mais pas de traitement d’expédition, vous pouvez utiliser la page **Prélèvement stock**. La page **Prélèvement stock** vous permet d’organiser et d’enregistrer le prélèvement des articles dont le mode de consommation est défini sur **Manuel**. Lorsque vous enregistrez un prélèvement stock, la consommation des composants prélevés est enregistrée. Vous pouvez également utiliser un **Mouvement de stock** avec une référence à un document source pour amener les composants avec la méthode de consommation définie sur **Manuel**, **Prélever + Transférer**, **Prélever + en arrière** aux ordres de fabrication.

Lorsque des opérations de fabrication sont intégrées dans les processus entrepôt, par des emplacements ou des prélèvement ou rangement suggérés, l’emplacement à partir duquel les composants sont consommés est l’emplacement qui est défini sur chaque ligne composant O.F. Tous les composants requis doivent être disponibles dans cet emplacement. Autrement, la validation manuelle ou par consommation du composant est annulée.

> [!NOTE]  
> Les différences importantes suivantes existent entre les prélèvements de stock, les mouvements de stock et les prélèvements en entrepôt :  
>
> - Lorsque vous enregistrez un prélèvement stock pour une opération interne, telles que la production, la consommation des composants sélectionnés est validée en même temps. Lorsque vous enregistrez un mouvement stock ou un prélèvement en entrepôt pour une opération interne, vous enregistrez seulement le mouvement physique des articles requis dans un emplacement de la zone Opérations sans valider la consommation.  
> - Lorsque vous utilisez des prélèvements stock, le champ **Code emplacement** sur une ligne composant d’ordre de fabrication. définit l’emplacement de *prélèvement* où les composants sont déduits lors de la validation de la consommation. Lorsque vous utilisez des mouvements de stock ou un prélèvement en entrepôt, le **Code emplacement** sur des lignes composant d’ordre cde fabrication définit l’emplacement *placement* dans la zone Opérations où l’employé du magasin doit placer les composants.  

Pour prélever ou déplacer des composants, une demande d’entrepôt sortante doit notifier la zone d’entrepôt du besoin de composant. La demande d’entrepôt sortante est créée lorsque vous procédez comme suit :

- Modifier le statut d’un ordre de fabrication sur Lancé.
- Créez un ordre de fabrication lancé.  

Les modes de consommation affectent également le flux des composants en production. Pour plus d’informations, voir [Consommer en aval des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md). **Mouvement de stock** avec des références au document source et **Prélèvement en entrepôt** ne peut pas être utilisé pour sélectionner des composants avec des modes de consommation *Amont* et *Aval*. **Prélèvement stock** ne peut pas être utilisé pour sélectionner des composants avec une méthode de consommation, mais *Manuel*. Pour gérer les composants restants, utilisez **Mouvement stock** sans référence à un document source. Pour plus d’informations, voir [Déplacer les composants vers une zone opérations dans les configurations de stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Dans les configurations d’entrepôt avancées où les emplacements nécessitent à la fois des prélèvements et des expéditions, vous devez utiliser la page **Prélèvement en entrepôt** pour amener les composants avec la méthode de consommation définie sur *Manuel*, *Prélever + Transférer*, *Prélever + en arrière* aux ordres de fabrication. Pour plus d’informations, consultez [Prélever pour la fabrication ou l’assemblage dans les configurations de stockage avancées](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Pour prélever les composants pour la fabrication et les tâches dans les configurations entrepôt de base

Dans les configurations de stockage de base, dans lesquelles le magasin est configuré pour utiliser uniquement le prélèvement ainsi que l’expédition, vous pouvez prélever des composants pour les activités de fabrication et les lignes planning des tâches sur la page **Prélèvement entrepôt**. Pour plus d’informations, voir [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> La possibilité de sélectionner des composants pour les lignes de planning des tâches a été ajoutée à [!INCLUDE[d365fin](includes/d365fin_md.md)] dans la 2è vague de lancement 2022. Pour commencer à utiliser la capacité, un administrateur doit activer **Mise à jour des fonctionnalités : activer prélèvement stock et entrepôt à partir des projets** sur la page **Gestion des fonctionnalités**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] utilise la valeur dans le champ **Quantité restante** sur la ligne de planning des tâches lorsqu’il crée des prélèvements stock. Pour utiliser les prélèvements d’inventaire pour les tâches, vous devez activer le bouton à bascule **Appliquer le lien d’utilisation** sur la page **Fiche projet** pour les tâches. Cela vous permet de suivre l’utilisation par rapport à votre forfait. Si vous n’activez pas le bouton à bascule, la quantité restante restera à **0** et le choix de stock ne sera pas créé. Pour plus d’informations, voir [Configurer le suivi de l’utilisation des tâches](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements stock**, puis choisissez le lien associé.  
2. Pour accéder aux composants de l’ordre de fabrication, choisissez l’action **Extraire documents origine**, puis sélectionnez l’ordre de fabrication lancé.  
3. Prélevez le composant, puis enregistrez les informations sur le prélèvement réel dans le champ **Qté à traiter**.  
4. Lorsque les lignes sont prêtes à être validées, choisissez l’action **Valider**. Les écritures entrepôt nécessaires sont alors créées et la consommation des articles est validée.  

Vous pouvez également créer un **Prélèvement de stock** directement à partir de la commande de fabrication lancée. Choisissez l’action **Créer prélèv./rangement stock/mouvement**, cochez la case **Créer prélèvement stock**, puis choisissez le bouton **OK**.

Sinon, utilisez un **Mouvement stock** en référence au document source pour déplacer des articles entre les conteneurs. Vous devrez enregistrer la consommation séparément. Pour plus d’informations, voir [Valider la consommation post production](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Prélever pour l’Assemblage dans les configurations de stockage de base

Utilisez les pages suivantes pour prélever des ordres d’assemblage :

- La page **Mouvement de stock**.
- Si l’emplacement exige des prélèvements, mais pas d’expéditions, utilisez la page **Prélvmt invent** pour prélever, assembler et expédier les ventes client lorsque les articles doivent être assemblés avant de pouvoir être livrés. Pour plus d’informations, voir [Traitement des articles à assembler pour commande dans les prélèvements stock](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Dans les configurations d’entrepôt avancées où les magasins requièrent des prélèvements et des expéditions, vous devez utiliser la page **Prélèvement entrepôt** pour ajouter des composants aux Ordres d’assemblage. Pour plus d’informations, consultez [Prélever pour la fabrication ou l’assemblage dans les configurations de stockage avancées](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Traitement des articles à assembler pour commande dans les prélèvements stock

La page **Prélvmt invent** est également utilisée pour prélever et livrer les ventes lorsque les articles doivent être assemblés avant de pouvoir être livrés. Pour plus d’informations, reportez-vous à [Vente d’articles à assembler pour commande](assembly-how-to-sell-items-assembled-to-order.md).

Les articles à expédier ne sont pas physiquement présents dans un emplacement tant qu’ils ne sont pas assemblés et enregistrés comme production dans un emplacement de la zone d’assemblage. Par conséquent, le prélèvement de ces articles pour l’expédition suit un flux spécial. Depuis un emplacement, les magasiniers extraient des éléments d’assemblage sur le poste d’accueil de livraison puis valident le prélèvement stock. Le prélèvement stock enregistré valide ensuite les résultats d’assemblage, la consommation de composants et l’expédition vente.

Vous pouvez configurer [!INCLUDE[prod_short](includes/prod_short.md)] pour créer automatiquement un mouvement stock lors de la création du prélèvement stock pour l’élément d’assemblage. Pour créer automatiquement des mouvements, sélectionnez le champ **Créer des mouvements automatiquement** sur la page **Paramètres d’assemblage**. Pour plus d’informations, voir [Déplacer les composants vers une zone opérations dans le stockage de base](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] crée des lignes prélèvement stock pour les articles vente de différentes manières, selon qu’aucune, certaines ou toutes les quantités des lignes vente sont assemblées pour commande.

- Dans les ventes où vous utilisez des prélèvements de stock pour valider l’expédition de stock, [!INCLUDE[prod_short](includes/prod_short.md)] crée une ligne de prélèvement de stock pour chaque ligne de commande client. Si l’article est placé dans différents emplacements, plusieurs lignes seront créées. Les lignes prélèvement sont basées sur la quantité indiquée dans le champ **Qté à expédier**.
- Dans les ventes où la quantité totale de la ligne commande vente est assemblée pour commande, une ligne prélèvement stock est créée pour cette quantité. La valeur du champ Quantité à assembler correspond à la valeur du champ **Qté à expédier**. Le champ **Assembler pour commande** est sélectionné sur la ligne.

Si un flux de résultats d’assemblage est paramétré pour le magasin, la valeur du champ **Code empl. exp. ass. pr comm.** ou la valeur du champ **Code empl. depuis assemblage**, de cette commande, est insérée dans le champ **Code emplacement** de la ligne prélèvement stock.

Si aucun code magasin n’est spécifié sur la ligne commande vente et qu’aucun flux résultats d’assemblage n’est paramétré pour le magasin, le champ **Code emplacement** de la ligne prélèvement stock est vide. Le magasinier doit ouvrir la page **Contenu emplacement** et sélectionner l’emplacement où les articles d’assemblage sont assemblés.

Si une partie de la quantité doit d’abord être assemblée tout d’abord, et l’autre doit être prélevée des stocks, [!INCLUDE[prod_short](includes/prod_short.md)] crée au minimum deux lignes prélèvement stock. Une ligne prélèvement est calculée pour la quantité à assembler pour commande. L’autre ligne prélèvement dépend des magasins dans lesquels les emplacements peuvent satisfaire la quantité restante du stock. Les codes emplacement sur les deux lignes sont renseignés de différentes manières comme indiqué pour les deux types vente différents respectivement. Pour plus d’informations, voir la section « Scénarios de combinaison » dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Renseigner l’emplacement consommation

Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d’emplacement.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/pick-ship-items-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : Warehouse Management](design-details-warehouse-management.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
