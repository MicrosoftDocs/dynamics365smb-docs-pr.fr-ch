---
title: Procédure d’affectation d’emplacements par défaut à des articles | Microsoft Docs
description: Si vous utilisez des emplacements dans un magasin, l’affectation d’emplacements par défaut à vos articles peut simplifier considérablement leur processus d’expédition, de réception et de déplacement. Lorsqu’un emplacement par défaut est affecté à un article, cet emplacement est suggéré chaque fois que vous lancez une transaction pour cet article.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6777f71e35792b4bb4dfb44d1267b59b90109438
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771894"
---
# <a name="assign-default-bins-to-items"></a>Affecter des emplacements par défaut à des articles
Si vous utilisez des emplacements dans un magasin, l’affectation d’emplacements par défaut à vos articles peut simplifier considérablement leur processus d’expédition, de réception et de déplacement. Lorsqu’un emplacement par défaut est affecté à un article, cet emplacement est suggéré chaque fois que vous lancez une transaction pour cet article. Les emplacements par défaut sont définis sur la page **Contenu emplacement**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Pour affecter un emplacement par défaut à un article
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille création contenu emplacement**, puis choisissez le lien associé.  
2.  Renseignez le code emplacement et les informations article pour chaque emplacement que vous souhaitez définir par défaut pour un article. Veillez à sélectionner le champ **Valeur par défaut**.  
3.  Choisissez l’action **Créer contenu emplacement**. Des emplacements par défaut sont maintenant affectés à votre article.  

> [!NOTE]  
>  Lorsqu’un article est rangé, si un emplacement par défaut ne lui est pas affecté, l’emplacement dans lequel l’article est rangé est affecté par défaut.  

## <a name="to-change-the-default-bin-for-an-item"></a>Pour modifier l’emplacement par défaut pour un article  
Vous pouvez être amené à modifier l’affectation de l’emplacement par défaut pour un article ou à affecter un emplacement par défaut à un nouvel article.    
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Contenu emplacement**, puis sélectionnez le lien associé.  
2.  Dans le champ **Filtre magasin**, sélectionnez le code emplacement approprié.  
3.  Recherchez l’écriture indiquant le contenu de l’emplacement par défaut pour cet article et désactivez la case à cocher **Emplacement par déf.**.  
4.  Recherchez la ligne contenu emplacement de l’emplacement que vous souhaitez paramétrer comme étant le nouvel emplacement par défaut. Cochez la case **Emplacement par défaut**.  

> [!NOTE]  
>  Lorsqu’un article est rangé pour la première fois, et si un emplacement par défaut ne lui est pas affecté, le système lui affecte comme emplacement par défaut celui dans lequel l’article est rangé.  

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]