---
title: "Comment créer des contenus emplacement | Microsoft Docs"
description: "Une fois la configuration des emplacements terminée, vous pouvez configurer leur contenu. En d'autres termes, vous pouvez configurer les articles à stocker dans un emplacement donné et définir les règles qui régissent le remplissage de l'emplacement avec un article spécifique."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1f3a90b9bc9cce2e138e490d3064f6d505a088b9
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-bin-contents"></a>Procédure : créer le contenu d'un emplacement
Une fois la configuration des emplacements terminée, vous pouvez configurer leur contenu. En d'autres termes, vous pouvez configurer les articles à stocker dans un emplacement donné et définir les règles qui régissent le remplissage de l'emplacement avec un article spécifique. Vous pouvez effectuer cette opération manuellement dans la fenêtre **Contenu emplacement** ou automatiquement dans la fenêtre **Créer feuille contenu emplacement**.

## <a name="to-create-bin-content-manually"></a>Pour créer le contenu d'emplacement manuellement  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.  
2.  Sélectionnez le magasin à partir duquel vous souhaitez créer un contenu d'emplacement, puis choisissez l'action **Emplacements**.  
3.  Sélectionnez l'emplacement à partir duquel vous souhaitez créer un contenu, puis choisissez l'action **Contenus**.  
4.  Pour chaque article que vous souhaitez stocker dans l'emplacement, renseignez une ligne de la fenêtre **Contenu emplacement** avec les informations appropriées. Certains champs sont déjà renseignés avec des informations relatives à l'emplacement.  
5.  Renseignez d'abord le champ **N° article**, puis, si vous utilisez un prélèvement et un rangement suggérés, renseignez les autres champs tels que **Code unité**, **Qté max** et **Qté min**.  

Sélectionnez le champ **Fixe** si nécessaire. Si l'emplacement doit être utilisé comme emplacement par défaut pour l'article, sélectionnez le champ **Emplacement par défaut**.  

Si vous utilisez un prélèvement et un rangement suggérés et que vous avez saisi, via la fiche article, les dimensions exactes des unités de mesure de chaque article,la quantité maximale que vous avez saisie dans la fenêtre **Contenu emplacement** est comparée aux capacités physiques de l'emplacement. Les quantités minimales et maximales sont alors utilisées lors du calcul du réapprovisionnement de l'emplacement et des rangements proposés.  

Si vous sélectionnez le champ **Fixe**, vous associez l'article à l'emplacement de manière statique, ce qui signifie que [!INCLUDE[d365fin](includes/d365fin_md.md)] essaie de placer cet article dans l'emplacement si l'espace libre est suffisant et conserve l'enregistrement qui associe l'article de manière statique à l'emplacement, même lorsque la quantité à l'emplacement est égale à 0. Il est possible de placer d'autres articles dans l'emplacement, même si un article a été associé à cet emplacement.  

> [!NOTE]  
>  Vous pouvez configurer simultanément plusieurs contenus emplacement dans la fenêtre **Feuille création contenu emplacement**.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Pour créer le contenu d'un emplacement avec une feuille  
Lorsque vous avez créé vos emplacements, vous pouvez créer le contenu de chaque emplacement dans la feuille de création de contenu d'emplacement.

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille création contenu emplacement**, puis choisissez le lien associé.  
2.  Dans l'en-tête feuille, cliquez dans le champ **Nom** et sélectionnez la feuille du magasin où vous souhaitez créer le contenu d'un emplacement.  
3.  Dans le champ **Code emplacement**, sélectionnez le code de l'emplacement dont vous souhaitez définir le contenu.   

    En cas d'utilisation d'un prélèvement et d'un rangement suggérés dans le magasin, les champs liés à l'emplacement en question ( **Type emplacement**, **Code classe entrepôt** et **Priorité emplacement**) sont renseignés automatiquement. Vous devez prendre en compte ces informations lors de la définition du contenu emplacement.  
4.  Sélectionnez l'article à affecter à l'emplacement et renseignez les champs relatifs au contenu de l'emplacement. Pour pouvoir utiliser la fonction **Calculer réappro. emplacement** dans le cadre d'un prélèvement et d'un rangement suggérés, renseignez les champs **Qté max.** et **Qté min.**  

    Pour définit cet emplacement comme emplacement préféré pour l'article, même si la quantité emplacement est égale à **0** et que tous les autres critères de rangement sont égaux, sélectionnez le champ **Fixe**.  
5.  Répétez les étapes 3 à 4 pour chaque article à affecter à un emplacement.  
6.  Choisissez l'action **Imprimer** pour afficher un aperçu du contenu emplacement que vous avez entré dans la feuille et l'imprimer. Modifiez le contenu de l'emplacement jusqu'à ce qu'il vous convienne.  
7.  Lorsque vous êtes prêt, choisissez l'action **Créer contenu emplacement**.  

Dans cette feuille, vous pouvez utiliser des lignes contenu de l'emplacement pour plusieurs emplacements, afin d'obtenir un aperçu convenable des articles que vous placez dans différents emplacements d'une zone, d'une allée, ou d'un casier donné.  

## <a name="see-also"></a>Voir aussi
[Procédure : calculer réappro. emplacement](warehouse-how-to-calculate-bin-replenishment.md)    
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

