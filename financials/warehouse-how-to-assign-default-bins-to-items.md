---
title: "Procédure d'affectation d'emplacements par défaut à des articles | Microsoft Docs"
description: "Si vous utilisez des emplacements dans un magasin, l'affectation d'emplacements par défaut à vos articles peut simplifier considérablement leur processus d'expédition, de réception et de déplacement. Lorsqu'un emplacement par défaut est affecté à un article, cet emplacement est suggéré chaque fois que vous lancez une transaction pour cet article."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 826e1392143b166566619c5aef8c28ac2b09bc22
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="assign-default-bins-to-items"></a>Affecter des emplacements par défaut à des articles
Si vous utilisez des emplacements dans un magasin, l'affectation d'emplacements par défaut à vos articles peut simplifier considérablement leur processus d'expédition, de réception et de déplacement. Lorsqu'un emplacement par défaut est affecté à un article, cet emplacement est suggéré chaque fois que vous lancez une transaction pour cet article. Les emplacements par défaut sont définis dans la fenêtre **Contenu emplacement**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Pour affecter un emplacement par défaut à un article
1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille création contenu emplacement**, puis choisissez le lien associé.  
2.  Renseignez le code emplacement et les informations article pour chaque emplacement que vous souhaitez définir par défaut pour un article. Veillez à sélectionner le champ **Valeur par défaut**.  
3.  Choisissez l'action **Créer contenu emplacement**. Des emplacements par défaut sont maintenant affectés à votre article.  

> [!NOTE]  
>  Lorsqu'un article est rangé, si un emplacement par défaut ne lui est pas affecté, l'emplacement dans lequel l'article est rangé est affecté par défaut.  

## <a name="to-change-the-default-bin-for-an-item"></a>Pour modifier l'emplacement par défaut pour un article  
Vous pouvez être amené à modifier l'affectation de l'emplacement par défaut pour un article ou à affecter un emplacement par défaut à un nouvel article.    
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Contenu emplacement**, puis sélectionnez le lien connexe.  
2.  Dans le champ **Filtre magasin**, sélectionnez le code emplacement approprié.  
3.  Recherchez l'écriture indiquant le contenu de l'emplacement par défaut pour cet article et désactivez la case à cocher **Emplacement par déf.**.  
4.  Recherchez la ligne contenu emplacement de l'emplacement que vous souhaitez paramétrer comme étant le nouvel emplacement par défaut. Cochez la case **Emplacement par défaut**.  

> [!NOTE]  
>  Lorsqu'un article est rangé pour la première fois, et si un emplacement par défaut ne lui est pas affecté, le système lui affecte comme emplacement par défaut celui dans lequel l'article est rangé.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

