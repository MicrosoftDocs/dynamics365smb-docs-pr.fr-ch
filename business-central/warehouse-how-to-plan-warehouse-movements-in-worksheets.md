---
title: Comment planifier des mouvements entrepôt dans la feuille | Microsoft Docs
description: Planifiez les mouvements de la feuille à l’aide de la fonction réapprovisionnement emplacement ou en planifiant manuellement les lignes à créer en tant qu’instructions mouvement.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ae0386c4fc2e3ac216d4228c94e7447a808cf50
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756132"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Planifier des mouvements entrepôt dans la feuille
Planifiez les mouvements de la feuille à l’aide de la fonction réapprovisionnement emplacement ou en planifiant manuellement les lignes à créer en tant qu’instructions mouvement.  

## <a name="to-calculate-a-replenishment-movement"></a>Pour calculer des mouvements de réapprovisionnement  
Au fur et à mesure que l’entrepôt expédie des articles aux clients, les emplacements les mieux classés contiennent de moins en moins d’articles. Pour remplir ces emplacements prélèvement avec des articles issus d’autres emplacements, exécutez la fonction **Calculer réappro. emplacement** sur la page **Feuille mouvements**.

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille mouvement**, puis choisissez le lien associé.  
2.  Choisissez l’action **Calculer réappro. emplacement**.  

    [!INCLUDE[prod_short](includes/prod_short.md)] crée des lignes indiquant précisément le mode de déplacement des articles des emplacements les moins bien classés vers les emplacements les mieux classés.  

    > [!NOTE]  
    >  Un mouvement est proposé selon FEFO lorsque vous activez la fonction **Créer mouvement** si les conditions suivantes sont réunies pour un article :  
    >   
    >  -   L’article a une date de péremption.  
    > -   La case à cocher **Prélèvement selon FEFO** sur la fiche magasin doit être cochée.  
    > -   La case à cocher **Emplacement obligatoire** de la fiche magasin est cochée.  
    > -   Les champs **De zone** et **D’emplacement** sont vides.  

    Pour plus d’informations, voir [Prélèvement par FEFO](warehouse-picking-by-fefo.md).  

3.  Vérifiez ces lignes et modifiez-les si nécessaire, ou supprimez-en certaines si le temps imparti est insuffisant pour les exécuter toutes.  
4.  Choisissez l’action **Créer mouvement** pour créer une instruction entrepôt s’adressant aux magasiniers.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Pour déplacer l’intégralité du contenu d’un ou de plusieurs emplacements à l’aide de la fonction Extraire contenu emplacement  
Vous pouvez également utiliser la feuille mouvements pour planifier d’autres mouvements de stock dans l’entrepôt. Par exemple, lorsque vous souhaitez placer des articles dans un emplacement pour contrôler la qualité, utilisez la feuille mouvements pour planifier cette action et créez un mouvement pour élaborer des instructions destinées à un employé.  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille mouvement**, puis choisissez le lien associé.  
2.  Choisissez l’action **Extraire contenu emplacement**. Vous pouvez utiliser la page de demande pour filtrer les emplacements et les articles que vous souhaitez voir figurer sur les lignes de la feuille mouvement.  
3.  Renseignez les champs pertinents de la page de demande de traitement par lots. Pour visualiser, par exemple, le contenu emplacement de tous les emplacements d’une zone donnée au niveau de l’emplacement, renseignez le champ **Code zone**. Pour extraire les lignes de chaque emplacement qui contient un article spécifique, renseignez le champ **N° article**.  

    > [!NOTE]  
    >  Vous ne pouvez pas déplacer manuellement des articles vers ou depuis un emplacement de type RECEPTIONNER, car les articles dans ce type d’emplacement doivent être enregistrés comme étant rangés avant de faire partie du stock disponible.  

4.  Lorsque vous extrayez plusieurs lignes, sélectionnez **Trier** pour sélectionner une méthode de tri définissant l’ordre d’apparition des lignes dans la feuille, puis sélectionnez le bouton **OK**.  

    > [!NOTE]  
    >  Les lignes mouvement sont récupérées selon FEFO lorsque vous activez la fonction **Extraire contenu emplacement** si les conditions suivantes sont réunies pour un article :  
    >   
    >  -   L’article a une date de péremption.  
    > -   La case à cocher **Prélèvement selon FEFO** sur la fiche magasin doit être cochée.  
    > -   La case à cocher **Emplacement obligatoire** de la fiche magasin est cochée.  
    > -   Les champs **De zone** et **D’emplacement** sont vides.  

5.  Complétez certaines des lignes extraites de manière à indiquer les changements à apporter. Pour chaque article à déplacer, vous devez renseigner les champs **N° article**, **Du code emplacement**, **Vers code emplacement** et **Quantité**.  
6.  Supprimez les lignes incomplètes que vous avez utilisées à des fins d’information.  
7.  Lorsque les lignes de la feuille mouvement correspondent précisément au mouvement devant être effectué par le magasinier, choisissez l’action **Créer mouvement** pour créer les instructions à l’attention de cet employé.  

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
