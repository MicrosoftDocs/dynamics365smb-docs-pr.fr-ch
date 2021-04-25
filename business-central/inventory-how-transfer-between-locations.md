---
title: Transfert d’articles entre des magasins entrepôt| Microsoft Docs
description: Décrit comment déplacer un stock d’un emplacement ou d’un entrepôt à un autre soit avec la feuille reclassement soit à l’aide des ordres de transfert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 008b9a50f2374b13e30114769520c7b18bba8e0e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785688"
---
# <a name="transfer-inventory-between-locations"></a>Transfert de stock entre des magasins
Vous pouvez transférer des articles en stock entre des magasins en créant des ordres de transfert. Vous pouvez également utiliser la feuille reclassement article.

Avec des ordres de transfert, vous pouvez expédier un transfert désenlogement à partir d’un magasin et recevoir un transfert enlogement à l’autre magasin. Cela vous permet de gérer les activités entrepôt impliquées et garantit que les quantités en stock sont mises à jour correctement.

Avec la feuille reclassement, il vous suffit de renseigner les champs **Code magasin** et **Nouveau code magasin**. Lorsque vous validez la feuille, les écritures comptables article sont ajustées dans les magasins en question. Avec cette méthode, les activités entrepôt ne sont pas traitées.

> [!NOTE]  
>   Si vous avez des articles stockés dans votre stock sans code magasin, par exemple datant d’une période où vous n’aviez qu’un seul entrepôt, vous ne pouvez pas transférer ces articles en utilisant des ordres de transfert. Au lieu de cela, vous devez utiliser la feuille reclassement pour reclasser les articles à partir d’un code magasin vide ver un code d’emplacement réel.  Pour plus d’informations, voir l’étape 3 dans [Pour transférer des articles avec la feuille reclassement article](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Pour transférer des articles, des acheminements transfert et magasins doivent être créés. Pour plus d’informations, reportez-vous à [Configurer des magasins](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Pour transférer des articles avec un ordre de transfert
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ordres de transfert**, puis sélectionnez le lien associé.
2. Dans l’en-tête de la page **Ordre de transfert**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Si vous avez renseigné les champs **Code transit**, **Code transporteur**, et **Code prestation transporteur** sur la page **Spéc. acheminement transfert** lors de la configuration de l’acheminement transfert ; ensuite les champs correspondants sur l’ordre de transfert sont renseignés automatiquement.

    Lorsque vous renseignez le champ **Code prestation transporteur**, le programme calcule la date de réception au magasin de destination en ajoutant le délai d’expédition de la prestation transporteur à la date d’expédition.

3. Pour renseigner les lignes, saisissez manuellement les données ou choisissez l’une des options suivantes sous l’action **Fonctions** :
    - Choisissez l’action **Extraire contenu emplacement** pour sélectionner des éléments existants dans un emplacement spécifique.
    - Choisissez l’action **Extraire lignes réception** pour sélectionner les éléments qui viennent d’arriver dans le magasin provenance transfert.   

    En tant que magasinier dans le magasin provenance transfert, continuez à expédier les articles.
4. Cliquez sur **Valider**, choisissez l’option **Expédition**, puis cliquez sur le bouton **OK**.

    Les articles sont à présent en transit entre les magasins spécifiés, selon l’acheminement transfert spécifié.

    En tant que magasinier dans le magasin provenance transfert, continuez à recevoir les articles. Les lignes Ordre transfert sont les mêmes que lors de l’expédition et ne peuvent pas être modifiées.
5. Cliquez sur **Valider**, choisissez l’option **Réception**, puis cliquez sur le bouton **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Pour transférer des articles avec la feuille reclassement article
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles reclassement article**, puis sélectionnez le lien associé.
2. Sur la page **Feuilles reclassement article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Dans le champ **Code magasin**, entrez le magasin où les articles sont actuellement stockés.

    > [!NOTE]  
    >   Pour transférer les articles qui n’ont aucun code magasin, laissez le champ **Code magasin** vide.
4. Dans le champ **Nouveau Code magasin**, indiquez le magasin vers lequel vous souhaitez transférer les articles.
5. Sélectionnez l’action **Valider**.

## <a name="see-also"></a>Voir aussi
[Gestion du stock](inventory-manage-inventory.md)  
[Configurer des magasins](inventory-how-setup-locations.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]