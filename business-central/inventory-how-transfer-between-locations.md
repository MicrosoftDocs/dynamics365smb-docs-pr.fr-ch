---
title: "Transfert d'articles entre des magasins entrepôt| Microsoft Docs"
description: "Décrit comment déplacer un stock d'un emplacement ou d'un entrepôt à un autre soit avec la feuille reclassement soit à l'aide des ordres de transfert."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0e21299ab25f05f465b8a33d3a12bc35d9037d0b
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-inventory-between-locations"></a>Transfert de stock entre des magasins
Vous pouvez transférer des articles en stock entre des magasins en créant des ordres de transfert. Vous pouvez également utiliser la feuille reclassement article.

Avec des ordres de transfert, vous pouvez expédier un transfert désenlogement à partir d'un magasin et recevoir un transfert enlogement à l'autre magasin. Cela vous permet de gérer les activités entrepôt impliquées et garantit que les quantités en stock sont mises à jour correctement.

Avec la feuille reclassement, il vous suffit de renseigner les champs **Code magasin** et **Nouveau code magasin**. Lorsque vous validez la feuille, les écritures comptables article sont ajustées dans les magasins en question. Avec cette méthode, les activités entrepôt ne sont pas traitées.

> [!NOTE]  
>   Si vous avez des articles stockés dans votre stock sans code magasin, par exemple datant d'une période où vous n'aviez qu'un seul entrepôt, vous ne pouvez pas transférer ces articles en utilisant des ordres de transfert. Au lieu de cela, vous devez utiliser la feuille reclassement pour reclasser les articles à partir d'un code magasin vide ver un code d'emplacement réel.  Pour plus d'informations, voir l'étape 3 dans la section « Pour transférer des articles avec la feuille reclassement article ».

Pour transférer des articles, des acheminements transfert et magasins doivent être créés. Pour plus d'informations, reportez-vous à [Configurer des magasins](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Pour transférer des articles avec un ordre de transfert
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ordres de transfert**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Ordre de transfer**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Si vous avez renseigné les champs **Code transit**, **Code transporteur**, et **Code prestation transporteur** dans la fenêtre **Spéc. acheminement transfert** lors de la configuration de l'acheminement transfert ; ensuite les champs correspondants sur l'ordre de transfert sont renseignés automatiquement.

    Lorsque vous renseignez le champ **Code prestation transporteur**, le programme calcule la date de réception au magasin de destination en ajoutant le délai d'expédition de la prestation transporteur à la date d'expédition.

    En tant que magasinier dans le magasin provenance transfert, continuez à expédier les articles.
3. Cliquez sur **Valider**, choisissez l'option **Expédition**, puis cliquez sur le bouton **OK**.

    Les articles sont à présent en transit entre les magasins spécifiés, selon l'acheminement transfert spécifié.

    En tant que magasinier dans le magasin provenance transfert, continuez à recevoir les articles.
4. Cliquez sur **Valider**, choisissez l'option **Réception**, puis cliquez sur le bouton **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Pour transférer des articles avec la feuille reclassement article
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles reclassement article**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Feuilles reclassement article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Dans le champ **Code magasin**, entrez le magasin où les articles sont actuellement stockés.

    > [!NOTE]  
    >   Pour transférer les articles qui n'ont aucun code magasin, laissez le champ **Code magasin** vide.
4. Dans le champ **Nouveau Code magasin**, indiquez le magasin vers lequel vous souhaitez transférer les articles.
5. Sélectionnez l'action **Valider**.

## <a name="see-also"></a>Voir aussi
[Gestion du stock](inventory-manage-inventory.md)  
[Configurer des magasins](inventory-how-setup-locations.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

