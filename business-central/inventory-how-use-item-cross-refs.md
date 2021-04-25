---
title: Utiliser les références externes article
description: Définissez des références entre les descriptions que vous et votre fournisseur utilisez pour un article afin que vous puissiez insérer la description d’article du fournisseur dans les documents achat.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0a9f84522598344435ad9c1263fe8cdea2e2a1e0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785663"
---
# <a name="use-item-cross-references"></a>Utiliser les références externes article
Si vous configurez une référence externe entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l’article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence externe**. . La même fonctionnalité s’applique pour les numéros d’article client sur les documents vente.

Les procédures suivantes décrivent comment utiliser les références externes article côté achat. La procédure est identique côté achat.

> [!NOTE]
> Il est de plus en plus courant que les identificateurs d’articles, tels que les GTIN ou les GUID contiennent 30 caractères ou plus, ce qui est plus que la fonctionnalité actuelle des références croisées d’éléments peut gérer. Si vous devez utiliser des références contenant plus de 30 caractères, votre administrateur peut activer les fonctionnalité **Écrire des références d’articles plus longues** sur la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610) (le lien nécessite que vous ayez un client [!INCLUDE[prod_short](includes/prod_short.md)]). La façon dont vous utilisez les références ne change pas, mais les noms d’articles, tels que les pages et les boutons le seront. Par exemple, la page **Entrées de références croisées d’article** deviendra la page **Entrées de référence d’article**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Pour configurer une référence externe article à la description d’un article fournisseur

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.
2. Ouvrez la fiche correspondant à l’article pour lequel vous souhaitez créer une référence externe à la description de l’article que le fournisseur utilise pour cet article.
3. Choisissez l’action **Références externes**.

     Si vous ne trouvez pas l’action **Références externes**, choisissez d’afficher plus d’options, puis recherchez-la sous **Association** > **Article**.
  
4. Sur une nouvelle ligne de la page **Écritures de référence externe article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Pour saisir une description de l’article d’un fournisseur sur une commande achat

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat**, puis sélectionnez le lien associé.
2. Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence externe article dans la procédure précédente.
3. Créez une ligne achat pour l’article pour lequel vous avez créé une référence externe article dans la procédure précédente.
4. Dans le champ **N° type référence externe**, sélectionnez la référence externe article que vous avez créée, puis choisissez le bouton **OK**.

Le champ **Description** de la ligne est remplacé par la description d’article du fournisseur, tel que configuré dans l’écriture référence externe article.

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]