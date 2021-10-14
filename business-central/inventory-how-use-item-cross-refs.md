---
title: Utiliser références article
description: Définissez des références entre les descriptions que vous et votre fournisseur utilisez pour un article afin que vous puissiez insérer la description d’article du fournisseur dans les documents achat.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588616"
---
# <a name="use-item-references"></a>Utiliser références article
Si vous configurez une référence entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l’article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence article**. . La même fonctionnalité s’applique pour les numéros d’article client sur les documents vente.

Les procédures suivantes décrivent comment utiliser les références article côté achat. La procédure est identique côté achat.

> [!NOTE]
> Toutes les entreprises n’utilisent pas de références article. Pour minimiser l’encombrement des pages, nous avons masqué les champs et les actions associés. Si vous décidez de les utiliser, vous pouvez activer le bouton à bascule **Utiliser les références article** sur la page **Paramètres stock**. Une fois que vous avez activé les références article, les champs et les actions sont disponibles sur les pages Fiche article, Fiche fournisseur et Fiche client, ainsi que dans les documents de vente et d’achat.

## <a name="to-start-using-item-references"></a>Pour commencer à utiliser les références article
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres stock**, puis choisissez le lien associé.
2. Activez le bouton à bascule **Utiliser références article**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Pour configurer une référence article sur la description d’un article fournisseur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche correspondant à l’article pour lequel vous souhaitez créer une référence sur la description de l’article que le fournisseur utilise pour cet article.
3. Sélectionnez l’action **Références article**.

     Si vous ne trouvez pas l’action **Références article**, choisissez d’afficher plus d’options, puis recherchez-la sous **Association** > **Article**.
  
4. Sur une nouvelle ligne de la page **Écritures de référence article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Pour saisir une description de l’article d’un fournisseur sur une commande achat

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes achat**, puis choisissez le lien associé.
2. Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence article dans la procédure précédente.
3. Créez une ligne achat pour l’article pour lequel vous avez créé une référence article dans la procédure précédente.
4. Dans le champ **N° référence article**, sélectionnez la référence article que vous avez créée, puis choisissez le bouton **OK**.

Le champ **Description** de la ligne est remplacé par la description d’article du fournisseur, telle que configurée dans l’écriture référence article.

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]