---
title: Créer et gérer des articles de catalogue | Microsoft Docs
description: Décrit comment commercialiser des articles de votre liste de fournisseurs d’articles mais pas dans votre propre liste d’articles.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cf6016b2d2f2774807b120ab3d3521af9eaf5f7f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749920"
---
# <a name="work-with-catalog-items"></a>Utiliser des articles de catalogue
Vous pouvez proposer certains articles à vos clients pour leur rendre service, que vous ne souhaitez pas gérer dans votre système tant que vous ne commencez pas à les commercialiser. Lorsque vous souhaitez commencer à gérer de tels articles dans votre système, vous pouvez les convertir en fiches article normales de deux façons.

* Depuis une fiche article de catalogue, créez une nouvelle fiche article basée sur un modèle.
* Depuis une ligne commande vente de type **Article** avec un champ **N°** vide, sélectionnez un article de catalogue. Une fiche article est ensuite automatiquement créée pour l’article de catalogue.

> [!NOTE]  
> Vous ne pouvez pas sélectionner d’article de catalogue à partir de la page **Facture vente**.<br /><br />
> Vous pouvez sélectionner un article de catalogue à partir de la page **Devis**, mais l’article de catalogue ne sera pas converti en un article normal lorsque vous utilisez la fonction **Créer commande**.

Un article de catalogue a généralement le numéro d’article du fournisseur qui le fournit. Pour activer la conversion d’une fiche article de catalogue en une fiche article normale, vous devez tout d’abord configurer comment la numérotation de l’article fournisseur est convertie dans votre propre numérotation d’article.   

> [!Important]
> Les articles de catalogue ne doivent pas être confondus avec les articles hors stock, qui sont des articles normaux qui ont le type **Hors stock** pour les conserver hors les calculs de disponibilité et d’évaluation, par exemple parce qu’ils sont uniquement utilisés en interne et ont un coût bas. Pour plus d’informations sur les types, voir [À propos des types d’articles](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Pour créer un article de catalogue
Les fiches article de catalogue ont moins d’informations que les fiches article normales, car vous ne les utilisez que pour proposer des devis ainsi que pour d’autres procédures. Pour cette raison, elles doivent être converties en fiches article normales, avant que vous puissiez valider les transactions commerciales pour elles.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles de catalogue**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Pour configurer comment les numéros d’article de catalogue sont convertis en votre propre numérotation
Pour activer la conversion d’une fiche article de catalogue en une fiche article normale, vous devez tout d’abord configurer comment la numérotation de l’article fournisseur est convertie dans votre propre format de numérotation d’article.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres article de catalogue**, puis sélectionnez le lien associé.
2. Renseignez les champs selon vos besoins.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Pour convertir un article de catalogue en un article normal
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles de catalogue**, puis sélectionnez le lien associé.
2. Ouvrez la fiche pour un article de catalogue que vous pouvez convertir en un article normal.
3. Sur la page **Fiche article de catalogue**, sélectionnez l’action **Créer un article**.

Une nouvelle fiche article pré-remplie avec les informations de l’article de catalogue ainsi qu’un modèle d’article pertinent sont créés. Vous pouvez ensuite remplir ou modifier les champs sur la nouvelle fiche article, le cas échéant. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Pour vendre un article de catalogue et le convertir en article normal
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**. Complétez les champs du raccourci **Général** comme pour toute commande vente. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
3. Sur une nouvelle ligne vente, dans le champ **Type**, sélectionnez **Article**, mais laissez le champ **N°** vide.
4. Choisissez l’action **Ligne**, puis l’action **Sélectionner articles de catalogue**.

    L’article de catalogue est converti en un article normal. Une nouvelle fiche article pré-remplie avec les informations de l’article de catalogue ainsi qu’un modèle d’article pertinent sont créés.
5. Sur la page **Articles de catalogue**, sélectionnez l’article de catalogue que vous souhaitez vendre, puis choisissez le bouton **OK**.
6. Lorsque les lignes commande vente sont renseignées, sélectionnez l’action **Valider**.

Vous pouvez ensuite remplir ou modifier les champs sur la nouvelle fiche article, le cas échéant. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

> [!NOTE]  
>   Un enregistrement de référence externe article est automatiquement créé pour le fournisseur de l’article entre le numéro article fournisseur et votre nouveau numéro article. Pour plus d’informations, voir [Utiliser les références externes article](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Créer des commandes spéciales](sales-how-to-create-special-orders.md)|  
[Stock](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]