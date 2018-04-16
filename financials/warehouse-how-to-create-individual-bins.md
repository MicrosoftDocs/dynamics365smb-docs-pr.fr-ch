---
title: "Comment créer des emplacements | Microsoft Docs"
description: "La méthode la plus efficace pour créer les emplacements de votre entrepôt consiste à générer des groupes d'emplacements identiques dans la feuille de création d'emplacements, mais vous pouvez également créer vos emplacements séparément."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f8cd19f97c530397dd6b499157e13340331aa3ba
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-bins"></a>Créer emplacements
La méthode la plus efficace pour créer les emplacements de votre entrepôt consiste à générer des groupes d'emplacements identiques dans la feuille de création d'emplacements, mais vous pouvez également créer vos emplacements séparément à partir de la fiche magasin. Vous pouvez également utiliser une fonction de la fenêtre **Feuille création emplacement** pour créer des emplacements automatiquement.  

## <a name="to-create-a-bin-from-the-location-card"></a>Pour créer un emplacement à partir de la fiche magasin  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Magasins**, puis sélectionnez le lien connexe.  
2. Sélectionnez le magasin à partir duquel vous souhaitez créer un emplacement, puis choisissez l'action **Emplacements**.  
3. Sélectionnez l'action **Nouveau**.
4. Renseignez les champs selon vos besoins. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Pour créer séparément des emplacements dans la feuille de création d'emplacements  
1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille création emplacement**, puis choisissez le lien associé.  
2.  Sur chaque ligne, renseignez les champs requis pour nommer et caractériser les emplacements que vous créez.  
3.  Choisissez l'action **Créer emplacements**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Pour créer des emplacements automatiquement dans la feuille de création d'emplacements  
Avant de commencer à créer automatiquement des emplacements dans la feuille, déterminez les types d'emplacement essentiels à vos opérations, ainsi que la circulation des articles la plus pratique dans la structure physique de votre entrepôt.  

> [!NOTE]  
>  Dès que vous utilisez un emplacement, vous ne pouvez pas le supprimer sauf s'il est vide. En revanche, si vous souhaitez utiliser un autre système d'attribution de nom d'emplacement, vous pouvez utiliser la feuille reclassement pour déplacer effectivement vos articles vers un nouveau système d'emplacements. Cependant, ce processus est manuel et prend du temps ; il est donc préférable de configurer correctement vos emplacements dès le début.  

Pour travailler avec la fenêtre **Feuille création emplacement**, vous devez être défini comme magasinier à l'endroit où les emplacements existent. Pour plus d'informations, voir [Configurer des employés d'entrepôt](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille création emplacement**, puis choisissez le lien associé.  
2.  Choisissez l'action **Calculer emplacements**.
3. Dans la fenêtre **Calculer emplacements**, sous **Code modèle emplacement**, sélectionnez le modèle emplacement à utiliser comme modèle pour les emplacements que vous créez.
4.  Saisissez une description pour les emplacements que vous êtes en train de créer.  
5.  Pour créer des codes d'emplacement, renseignez les champs **Du n°** et **Au n°** dans les trois catégories indiquées ci\-dessous : **Travée**, **Section** et **Niveau**. Le code emplacement peut contenir au maximum 20 caractères.  

    > [!NOTE]  
    >  Le nombre de caractères saisis dans les champs des trois catégories \(par exemple, les caractères saisis dans les trois champs **Du n°**\), auxquels s'ajoutent les éventuels séparateurs de champs, doit être inférieur ou égal à 20.  

     Vous pouvez utiliser des lettres dans le code, mais la lettre utilisée doit être identique dans les champs **Du n°** et **Au n°** . Par exemple, vous pouvez définir la partie Travée du code de la manière suivante : **Du n° A01** et **Au n° A10**. Le programme n'est pas configuré pour générer des codes comprenant des suites de lettres (par exemple, de A01 à F05).  

6.  Si vous souhaitez qu'un caractère (par exemple, un trait d'union) sépare les champs des catégories que vous avez définis comme faisant partie du code emplacement, renseignez le champ **Séparateur de champs** avec ce caractère.  
7.  Pour que le programme ne crée pas de ligne pour un emplacement si elle existe déjà, sélectionnez le champ **Vérifier existence emplacement**.  
8. Une fois le remplissage de toutes les lignes terminé, sélectionnez le bouton **OK**.

    Le programme crée dans la feuille une ligne pour chaque emplacement. Vous pouvez maintenant supprimer certains emplacements, par exemple si vous avez un casier qui vous permet d'accéder aux deux premiers niveaux de deux sections.  

9. Lorsque vous avez supprimé tous les emplacements inutiles, choisissez l'action **Créer emplacements** pour que le programme crée des emplacements pour chaque ligne de la feuille.  

Répétez l'opération pour un autre ensemble d'emplacements jusqu'à ce que vous ayez créé tous les emplacements de votre entrepôt.  

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

