---
title: Comment déplacer des articles dans les configurations de stockage avancées | Microsoft Docs
description: Dans des configurations d’entrepôt avancées, c’est-à-dire des magasins avec prélèvement et rangement dirigé, des mouvements entrepôt entre emplacements sont exécutés par un cadre qui prépare des mouvements entrepôt dans la feuille mouvement, puis crée les mouvements entrepôt que les magasiniers doivent exécuter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e843b048c117539d077dc4a8ecba33f265a2e826
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782649"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Déplacer des articles dans les configurations de stockage avancées
Dans des configurations d’entrepôt avancées, c’est-à-dire des magasins avec prélèvement et rangement dirigé, des mouvements entrepôt entre emplacements sont exécutés par un cadre qui prépare des mouvements entrepôt dans la feuille mouvement, puis crée les mouvements entrepôt que les magasiniers doivent exécuter.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Pour déplacer des articles avec la feuille mouvement entrepôt
La page **Feuille mouvement** a deux fonctions qui peuvent vous aider à renseigner automatiquement les lignes. La première est la fonction **Calculer réappro. emplacement**. Cette fonction utilise les priorités emplacement pour suggérer le réapprovisionnement des emplacements les mieux classés à partir de ceux moins bien classés. La seconde est la fonction de **Extraire contenu emplacement**, qui renseigne les lignes feuille avec tout le contenu des emplacements que vous spécifiez.

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille mouvement**, puis choisissez le lien associé.  
2.  Renseignez comme il convient les informations de mouvement d’entrepôt dans les lignes de la feuille.  
3. Choisissez l’action **Créer mouvement** pour créer un document mouvement entrepôt qui pourra être ensuite enregistré lorsque le mouvement sera terminé.  

### <a name="to-register-the-warehouse-movement"></a>Pour enregistrer le mouvement d’entrepôt  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mouvements**, puis sélectionnez le lien associé.  
2.  Ouvrez le mouvement entrepôt que vous souhaitez traiter.  
3.  Sur les lignes dont le type d’action est **Emplacement**, spécifiez où, quoi et quand déplacer l’article concerné en modifiant les champs **Code zone**, **Code emplacement** ou **Qté à traiter**, ou **Date d’échéance** .  

    Si votre entrepôt a été configuré de façon à ce que les codes emplacement suivent la structure physique de l’entrepôt, vous pouvez prendre des quantités de plusieurs articles dans des emplacements consécutifs, puis les placer dans des emplacements de prélèvement se trouvant en aval et pouvant être proches les uns des autres.  
4.  Sur les lignes dont le type d’action est **Prélever**, indiquez dans le champ **Qté à traiter** une quantité du contenu emplacement que vous souhaitez déplacer. Tous les autres champs sur les lignes dont le type d’action est **Prélever** sont en lecture seule.  
5.  Pour déplacer toutes les quantités proposées comme spécifiées dans le champ **Quantité**, choisissez l’action **Renseigner automatiquement la quantité à traiter**.  
6. Sélectionnez l’action **Enregistrer**.  

> [!NOTE]  
>  Si le magasin utilise des prélèvement et rangement suggérés, vous ne pouvez pas déplacer manuellement des articles vers ou depuis un emplacement de type RÉCEPTIONNER, car les articles dans ce type d’emplacement doivent être enregistrés comme étant rangés avant de faire partie du stock disponible.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Pour enregistrer un mouvement d’un article déjà terminé  
Si, en cas d’utilisation d’un prélèvement et d’un rangement suggérés dans le magasin, vous devez déplacer des articles vers d’autres emplacements sans rangement, prélèvement ou mouvement entrepôt préexistant, vous pouvez alors enregistrer l’emplacement exact des articles dans l’entrepôt à l’aide de la fonction **Feuille reclassement entrepôt**.

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille reclassement entrepôt**, puis choisissez le lien associé.  
2.  Renseignez les champs **N° article**, **Du code zone**, **Du code emplacement**, **Vers code zone** et **Du code emplacement**.  
3.  Sélectionnez l’action **Enregistrer**.  

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]