---
title: "Procédure : annuler la validation d'assemblage | Microsoft Docs"
description: Vous pouvez parfois être amené à annuler un ordre d'assemblage validé, par exemple, si la commande a été validée avec des erreurs qui doivent être corrigées, ou parce qu'il n'aurait pas dû être validé en premier et doit être annulé.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 776a39f10041dc540de53e5aa724db6fd755c2d6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "935534"
---
# <a name="undo-assembly-posting"></a>Annuler la validation d'assemblage
Vous pouvez parfois être amené à annuler un ordre d'assemblage validé, par exemple, si la commande a été validée avec des erreurs qui doivent être corrigées, ou parce qu'il n'aurait pas dû être validé en premier et doit être annulé.

Lorsque vous annulez un ordre d'assemblage validé, un ensemble d'écritures comptables article de correction est créé pour contrepasser les écritures d'origine. Chaque écriture production positive pour l'élément d'assemblage est contrepassée par une écriture production négative. Chaque écriture production négative pour un composant d'assemblage est contrepassée par une écriture production positive. Le lettrage des coûts fixes est créé automatiquement entre les écritures de correction et les écritures d'origine afin de garantir une inversion de même coût.  

Lorsque vous annulez un ordre d'assemblage entièrement validé, vous pouvez choisir de recréer l'ordre d'assemblage à son état d'origine, par exemple, pour apporter des corrections avant une nouvelle validation. Sinon, vous pouvez choisir de ne pas recréer l'ordre d'assemblage.  

Lorsque vous annulez un ordre d'assemblage partiellement validé, tous les champs de quantité concernés, notamment les champs **Quantité assemblée**, **Quantité consommée** et **Quantité restante**, sont restaurés avec leur valeur précédant la validation en question.  

Pour recréer ou restaurer des ordres d'assemblage, il faut que l'élément d'assemblage qui résultait de la validation initiale respecte les conditions suivantes :  

-   Il doit toujours être en stock, c'est-à-dire ne pas avoir été vendu ou consommé par des transactions sortantes.  
-   Il ne doit pas être réservé.  
-   Il doit exister dans l'emplacement dans lequel il a été produit.  

De plus, les ordres d'assemblage existants ne peuvent être restaurés que si le nombre de lignes et la séquence de lignes de l'ordre de assemblage initial ne sont pas modifiés.  

> [!TIP]  
>  Pour résoudre les conflits dus à des modifications de ligne, vous pouvez rétablir manuellement les modifications sur les lignes en question avant d'annuler l'ordre d'assemblage validé associé. Sinon, vous pouvez valider l'ordre d'assemblage entièrement et choisir de le recréer lorsque vous annulez la validation.  

La procédure suivante décrit comment annuler les ordres d'assemblage validés où les articles ont été assemblés pour stockage. Si vous souhaitez annuler les ordres d'assemblage validés pour lesquels les articles ont été assemblés pour une commande vente, vous devez exécuter la fonction **Annuler expédition** sur l'expédition validée qui se rapporte à l'ordre d'assemblage validé. Pour plus d'informations, reportez-vous à [Inversion d'une validation](finance-how-reverse-journal-posting.md). L'annulation de l'ordre d'assemblage validé se produit alors automatiquement de la même manière que celle décrite dans cette rubrique.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Pour annuler la validation d'un ordre d'assemblage  
1.  Pour annuler un ordre d'assemblage validé entièrement ou partiellement, choisissez l'icone ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Ordres d'assemblage validés**, puis sélectionnez le lien associé.  

    La page **Ordres d'assemblage validés** s'ouvre avec un ou plusieurs ordres d'assemblage qui ont été validés à partir de l'ordre d'assemblage en question. Chaque validation partielle crée un ordre d'assemblage validé distinct.  
2.  Ouvrez l'ordre d'assemblage validé que vous souhaitez annuler, puis choisissez **Annuler l'assemblage**.  

    Si l'ordre d'assemblage validé que vous souhaitez annuler est lié à un ordre d'assemblage entièrement validé qui est maintenant supprimé, vous avez la possibilité de le recréer, généralement parce que vous voulez le retraiter.  
3.  Si vous souhaitez recréer l'ordre d'assemblage, cliquez sur le bouton **oui**. Pour annuler la validation sans recréer l'ordre d'assemblage associée, cliquez sur le bouton **Non**.  

Le champ **Contrepassé** de l'en\-tête d'ordre d'assemblage prend la valeur **Oui**. La validation de l'ordre d'assemblage est désormais annulée. Vous pouvez traiter l'ordre d'assemblage dans son intégralité si vous avez choisi de le recréer, ou l'ordre d'assemblage ouvert que vous avez restauré à son état d'origine.  

> [!NOTE]  
>  Pour restaurer les quantités de plusieurs validations partielles dans un ordre d'assemblage, vous devez annuler tous les ordres d'assemblage validés concernés en suivant les étapes 1 à 3 ci-dessus pour chaque ordre d'assemblage validé.  

## <a name="see-also"></a>Voir aussi  
[Gestion des assemblages](assembly-assemble-items.md)  
[Inversion d'une validation](finance-how-reverse-journal-posting.md)  
[Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md)    
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
