---
title: Comment planifier des prélèvements dans des feuilles | Microsoft Docs
description: Lorsque l’entrepôt est configuré pour appeler un traitement de prélèvement et d’expédition, le fonctionnement de l’entrepôt peut être établi de telle sorte que les lignes des documents expédition ne soient pas automatiquement transformées en instructions de prélèvement, mais soient plutôt activées sur la feuille prélèvement.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 250d85308e60f93ccba28e2354e47be185918d52
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756157"
---
# <a name="plan-picks-in-worksheets"></a>Planifier des prélèvements dans la feuille

Lorsque l’entrepôt est configuré pour appeler un traitement de prélèvement et d’expédition, le fonctionnement de l’entrepôt peut être établi de telle sorte que les lignes des documents expédition ne soient pas automatiquement transformées en instructions de prélèvement, mais soient plutôt activées sur la feuille prélèvement.  

> [!NOTE]  
> Si des instructions de prélèvement entrepôt ont déjà été créées et que vous souhaitez les combiner pour former une instruction de prélèvement plus efficace, supprimez les prélèvements entrepôt individuels. Les lignes à prélever sont alors listées dans la feuille.  

Dans la feuille prélèvement, vous pouvez définir des listes de prélèvement pour les employés de manière à réduire au minimum leurs déplacements dans l’entrepôt lors du prélèvement des articles. Les champs contiennent des informations concernant les quantités d’articles disponibles dans les emplacements de transbordement. En cas de transbordement, ces champs vous permettent de planifier l’affectation des tâches, car l’application propose toujours en priorité de prélever un article dans un emplacement de transbordement avant de le prélever dans un autre emplacement, quelle que soit l’unité de mesure de l’article. Les lignes de la feuille peuvent provenir d’un certain nombre de documents origine et être triées par article, numéro emplacement, document origine, date d’échéance ou adresse destinataire.  

Si vous triez par date d’échéance, vous pouvez choisir d’effacer de la feuille toutes les lignes à l’exception de celles nécessitant un traitement immédiat. Les lignes moins urgentes ne sont pas effacées mais renvoyées à la feuille **sélection prélèvement**. Lorsque vous créez le prélèvement, les lignes sont déjà triées par date d’échéance et vous pouvez choisir d’affecter le prélèvement à un employé donné.  

> [!NOTE]  
> Le prélèvement pour l’expédition entrepôt des articles assemblés à la commande vente en cours d’expédition suit les mêmes étapes que les prélèvements entrepôt ordinaires pour l’expédition, comme décrit dans cette rubrique. Cependant, le nombre de lignes prélèvement par quantité à livrer peut grandement varier car le prélèvement entrepôt concerne les composants et non l’élément d’assemblage.  
>
> Les lignes prélèvement entrepôt sont créées suivant la valeur du champ **Quantité restante** sur les lignes de l’ordre d’assemblage associé à la ligne commande vente en cours d’expédition. Ceci garantit le prélèvement de tous les composants en une seule action.  
>
> Pour plus d’informations, reportez-vous à la section « Traitement des articles à assembler pour commande dans les expéditions entrepôt » dans Expédition entrepôt.  
>
> Pour plus d’informations sur le prélèvement de composants pour les ordres d’assemblage en général, notamment les situations où l’élément d’assemblage n’est pas dû dans une expédition vente, voir [Prélever pour l’assemblage ou la production dans les configurations de stockage avancées.](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>Pour planifier des prélèvements dans la feuille

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille prélèvement**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Extraire documents entrepôt**.  
3. Sélectionnez les expéditions pour lesquelles vous souhaitez préparer un prélèvement. Vous pouvez à présent opérer un tri ponctuel, qui ne suivra pas l’instruction globale de prélèvement. Vous pouvez aussi supprimer certaines lignes pour rendre le prélèvement plus efficace. Par exemple, si un certain nombre de lignes comporte des articles situés dans des emplacements de transbordement, vous pouvez, si vous le souhaitez, créer un prélèvement pour toutes les lignes associées à ces lignes. Les articles transbordés seront expédiés, avec les autres articles des expéditions, et les emplacements de transbordement pourront à nouveau recevoir d’autres articles entrants.  
4. Choisissez l’action **Créer prélèvement**, puis remplissez la page de demande **Créer prélèvement**. Le tri que vous demandez ici organisera les lignes prélèvement que vous créez. Par exemple, vous pouvez créer un prélèvement pour chaque zone et trier les lignes selon l’ordre des emplacements au sein de chaque prélèvement.  
5. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Prélèvements entrepôt**, puis sélectionnez le lien associé. La page **Prélèvements entrepôt** s’ouvre.  
6. Vous pouvez à présent trouver le prélèvement affecté que vous venez de créer en sélectionnant le prélèvement doté du numéro le plus élevé.  
7. Dans ce prélèvement, vous pouvez toujours au besoin modifier le code utilisateur de la personne à qui ce prélèvement est affecté, ainsi que le mode de tri des lignes.  
8. Choisissez l’action **Imprimer** pour imprimer les instructions relatives au prélèvement.  
9. Une fois le prélèvement exécuté, choisissez l’action **Enregistrer**.  

Si la numérotation des emplacements reflète la disposition de l’entrepôt, les lignes triées par code emplacement permettent à la personne qui réalise le prélèvement de prélever les articles nécessaires à plusieurs expéditions en ne réalisant qu’un tour de l’entrepôt. L’employé prélève dans chaque emplacement le nombre d’articles requis par chaque ligne expédition et les place avec les autres articles en les organisant par expédition. L’employé gagne ainsi un temps considérable en prélevant en une fois dans un emplacement donné les articles nécessaires à plusieurs expéditions.  

Le classement des emplacements constitue une autre méthode de tri efficace, si l’entrepôt est organisé en fonction du classement des emplacements plutôt que par code emplacement.  

Dans la feuille prélèvement, vous pouvez aussi trier par adresse destinataire, ce qui vous permet de grouper, puis d’expédier en premier les commandes destinées aux clients lointains.  

## <a name="see-also"></a>Voir aussi

[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]