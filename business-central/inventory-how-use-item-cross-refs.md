---
title: Utiliser références article
description: 'Configurez des références entre les descriptions, les unités et les variantes que vous et votre fournisseur ou client utilisez pour un article.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: edupont
---
# <a name="use-item-references"></a>Utiliser références article

Si vous achetez ou vendez des articles pour lesquels vous et votre fournisseur ou client utilisez des termes différents, vous pouvez définir une référence entre vos termes pour les articles et les termes que le client ou le fournisseur de cet article utilise. De cette façon, la description de l’article du fournisseur ou du client, l’unité ou le code variante est automatiquement inséré sur les documents pertinents lorsque vous remplissez le **Numéro de référence de l’article** .  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Toutes les entreprises n’utilisent pas de références d’articles. Pour minimiser l’encombrement des pages, nous avons masqué les champs et les actions associés par défaut. Si vous décidez de les utiliser, sélectionnez le champ **Utiliser les références article** sur la page **Paramètres stock**. Une fois que vous avez activé les références article, les champs et les actions sont disponibles sur les pages Fiche article, Fiche fournisseur et Fiche client, ainsi que dans les documents de vente et d’achat.
>
> Dans les versions antérieures à la 2e vague de lancement 2021, votre administrateur peut activer les fonctionnalité *Écrire des références d’articles plus longues* sur la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610) (le lien nécessite que vous ayez un abonné [!INCLUDE [prod_short](includes/prod_short.md)]). La façon dont vous utilisez les références ne change pas, mais les noms d’articles, tels que les pages et les boutons le seront. Par exemple, la page **Entrées de références croisées d’article** deviendra la page **Entrées de référence d’article**.

## <a name="to-start-using-item-references"></a>Pour commencer à utiliser les références article

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, saisissez **Paramètres stock**, puis choisissez le lien associé.
2. Sélectionnez le champ **Utiliser les références d’articles**.

## <a name="to-set-up-an-item-reference"></a>Pour configurer une référence article

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un article pour lequel vous voulez créer une référence.
3. Sélectionnez l’action **Références article**.

     Si vous ne trouvez pas l’action **Références article**, choisissez d’afficher plus d’options, puis recherchez-la sous **Association** > **Article**.
  
4. Sur une nouvelle ligne de la page **Écritures de référence article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

La procédure suivante décrit comment spécifier la référence article sur une Commande achat. Les mêmes étapes s’appliquent aux documents vente et autres documents achat.  

## <a name="to-enter-a-vendors-item-description-on-a-document"></a>Pour saisir une description de l’article d’un fournisseur sur un document

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Commandes achat**, puis choisissez le lien associé.
2. Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence article dans la procédure précédente.
3. Créez une ligne achat pour l’article pour lequel vous avez créé une référence article dans la procédure précédente.
4. Dans le champ **N° référence article**, sélectionnez la référence article pertinente, puis choisissez le bouton **OK**.

Le champ **Description** de la ligne est remplacé par la description d’article du fournisseur, telle que configurée dans l’écriture référence article. Si la référence article comprend un code variante ou une unité, ces valeurs sont également copiées dans le document.  

## <a name="see-also"></a>Voir aussi

[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
