---
title: Créer un rangement à partir du rangement interne
description: Cette rubrique explique comment prélever et ranger sans document source, à la fois comment créer un prélèvement interne et comment créer un rangement interne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 198c4fb8ead4179667e35957046b3446ce5d8065
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444195"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Prélever et ranger sans document origine
Lorsque les articles ont été rangés et avant d’être prélevés pour répondre aux besoins d’un ordre de fabrication ou d’une expédition, ils sont stockés dans l’entrepôt comme faisant partie du stock disponible.  

Vous pouvez être amené à sortir temporairement des articles des emplacements prélèvement entrepôt, par exemple pour les présenter au cours d’une argumentation. Ces articles appartiennent toujours à la société et font partie du stock ; par contre, ils ne peuvent pas être prélevés. Ils sont enregistrés dans un emplacement spécial que vous créez à cet effet ; techniquement, les articles se trouvent dans l’entrepôt, mais physiquement, ils peuvent se trouver dans une salle de conférences ou d’exposition.  

Il peut également arriver que l’unité de fabrication ait inopinément besoin de quelques pièces pour un processus. Vous pouvez prélever des articles pour les emplacements fabrication à l’aide du prélèvement interne. Une fois le processus terminé et la fabrication réalisée, vous validez la consommation des articles et videz l’emplacement fabrication, ce qui a pour effet de réduire la quantité de l’article dans votre magasin.  

De même, des articles peuvent être retournés à l’entrepôt pour être rangés. Les articles ont pu être prélevés dans le stock disponible pour un ordre de fabrication, puis non utilisés. Pour qu’ils fassent de nouveau partie du stock disponible, ils doivent faire l’objet d’un rangement dans l’emplacement.  

Les **rangements internes** vous permettent d’effectuer des rangements sans avoir à vous référer à un document origine spécifique. Vous pouvez facilement configurer toutes les informations nécessaires pour créer une instruction entrepôt de rangement.  

> [!NOTE]  
>  Lorsque vous n’utilisez pas de prélèvements internes ni de rangements internes, vous pouvez effectuer ces ajustements en déplaçant les articles d’un emplacement à un autre ou en validant les ajustements des quantités d’un emplacement.  
>   
>  Lorsque le magasin utilise les prélèvement et rangement suggérés et, par conséquent, utilise des types emplacement, vous ne pouvez pas déplacer manuellement des articles vers ou depuis un emplacement de type RECEPTIONNER, car les articles dans ce type d’emplacement doivent être enregistrés comme étant rangés avant de faire partie du stock disponible.  

## <a name="to-create-an-internal-pick"></a>Pour créer un prélèvement interne  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvement interne entrepôt**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.
3. Renseignez le champ **N°** le champ **Code magasin** et le champ **Du code emplacement** du raccourci **Général**. Le champ **Du code emplacement** indique où placer les articles prélevés. Pour des raisons de fabrication, cet emplacement représente l’emplacement enlogement ou l’emplacement atelier ouvert. Pour d’autres applications, vous devez choisir un code emplacement d’un type emplacement qui n’est pas utilisé pour le prélèvement (par exemple, un emplacement affectation, expédition ou un emplacement spécial).  
4.  Sélectionnez un article dans le champ **N° article**, puis renseignez les quantités à prélever.  
5. Choisissez l’action **Créer prélèvement**. Une instruction prélèvement entrepôt est maintenant créée pour un magasinier. Vous pouvez également choisir l’action **Lancer** et créer des prélèvements entrepôt à l’aide de la **feuille prélèvements**. Pour plus d’informations, voir [Planifier des prélèvements dans des feuilles](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Pour créer un rangement interne  
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rangement interne entrepôt**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.
3. Renseignez l’en-tête d’un nouveau rangement interne en y indiquant au moins le **N°** et le **Code magasin**.
4. Renseignez une ligne pour chaque article à déplacer vers l’entrepôt. Vous ne devez renseigner que les champs **N° article** et **Quantité**.

  > [!NOTE]  
  > Lorsque vous sélectionnez le champ **N° article**, la **liste des contenus emplacement** s’ouvre à la place de la **liste des articles**. En effet, vous souhaitez ranger un article qui se trouve dans un emplacement particulier, le *contenu d’un emplacement* et pas uniquement un article, et vous connaissez déjà l’emplacement dans lequel l’article doit être prélevé.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Pour compléter les lignes en y indiquant l’ensemble du contenu emplacement ou le contenu emplacement filtré des emplacements du magasin, choisissez l’action **Extraire contenu emplacement**.  
6. Choisissez l’action **Créer rangement**. Une instruction rangement entrepôt est maintenant créée pour un magasinier. Vous pouvez également choisir l’action **Lancer** et créer des rangements entrepôt à l’aide de la **feuille rangement**. Pour plus d’informations, voir [Planifier des rangements dans la feuille](warehouse-how-to-plan-put-aways-in-worksheets.md)

## <a name="see-also"></a>Voir aussi  
[Gestion d’entrepôt](warehouse-manage-warehouse.md)  
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d’entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
