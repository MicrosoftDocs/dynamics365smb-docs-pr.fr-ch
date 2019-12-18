---
title: Comment calculer le réapprovisionnement de l'emplacement | Microsoft Docs
description: Lorsque le magasin est configuré pour utiliser le prélèvement et le rangement suggérés, les priorités du modèle de rangement du magasin sont prises en compte lors du rangement des réceptions.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7983969df7f07c82b83698442fedbf1bbd20d0f5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881837"
---
# <a name="calculate-bin-replenishment"></a>Calculer réappro. emplacement
Lorsque le magasin est configuré pour utiliser le prélèvement et le rangement suggérés, les priorités du modèle de rangement du magasin sont prises en compte lors du rangement des réceptions. Les priorités incluent les quantités minimale et maximale du contenu de l'emplacement qui ont été définies pour un emplacement particulier, ainsi que les priorités emplacement. Par conséquent, si des articles arrivent régulièrement, les emplacements prélèvement les plus utilisés sont remplis dès qu'ils sont vides.  

Mais les articles n'arrivent pas toujours de manière régulière. Parfois, votre société achète des articles en grande quantité afin d'obtenir une remise ou votre unité de production fabrique un article en grande quantité afin de réduire le coût unitaire. L'entrepôt ne reçoit aucun article pendant un certain temps et doit périodiquement déplacer des articles de zones de stockage en vrac vers des emplacements prélèvement.  

Il se peut aussi que l'entrepôt attende l'arrivée imminente d'un nouveau stock et veuille vider la zone de stockage en vrac des articles avant l'arrivée de la nouvelle marchandise.  

Enfin, si vous avez défini vos emplacements stockage en vrac avec un emplacement de type **Rangement** uniquement c'est à dire que l'action **Prélèvement** n'est pas activée, vos emplacements prélèvement doivent toujours être réapprovisionnés, étant donné que les prélèvements de stock ne sont pas proposés à partir d'un emplacement de type Rangement uniquement.  

## <a name="to-replenish-pick-bins"></a>Pour réapprovisionner des emplacements prélèvement  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille mouvement**, puis choisissez le lien associé.  
2.  Choisissez l'action **Calculer réappro. emplacement** pour ouvrir la page de demande d'état.  
3.  Renseignez la page de demande de traitement par lots pour limiter la portée des propositions de réapprovisionnement qui sera calculée. Par exemple, vous pouvez vous intéresser à des articles, des zones ou des emplacements particuliers.  
4.  Cliquez sur le bouton **OK**. Des lignes sont créées pour les mouvements réapprovisionnement devant être effectués en fonction des règles configurées pour les emplacements et leur contenu, c'est à dire des articles.  
5.  Pour effectuer tous les réapprovisionnements proposés, choisissez l'action **Créer mouvement**. Les employés peuvent maintenant consulter les instructions à partir de l'élément de menu **Mouvements**, puis les exécuter et les enregistrer.  
6.  Si vous ne souhaitez exécuter que certaines propositions, supprimez les lignes moins importantes, puis créez un mouvement.  

Lorsque vous calculez un nouvel approvisionnement emplacement, les propositions supprimées seront recréées si elles sont toujours valides.  

> [!NOTE]  
>  Si un article répond aux conditions suivantes :  
>   
>  -   l'article a une date d'expiration et  
> -   Le champ **Prélèvement selon FEFO** sur la fiche magasin doit être sélectionné, et  
> -   Vous utilisez la fonction **Calculer réappro. emplacement**,  
>   
>  alors les champs **De zone** et **D'emplacement** sont vides, car l'algorithme qui permet de calculer d'où déplacer les articles est déclenché uniquement lorsque vous activez la fonction **Créer mouvement**.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[Prélèvement par FEFO](warehouse-picking-by-fefo.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
