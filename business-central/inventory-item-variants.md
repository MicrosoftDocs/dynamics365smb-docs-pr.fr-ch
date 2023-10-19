---
title: Gérer les variantes de produits
description: 'Découvrez comment vous pouvez enregistrer des produits presque identiques, mais dont la couleur, la taille ou le matériau varient en tant que variantes d’articles.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: bholtorf
---
# <a name="manage-product-variants"></a>Gérer les variantes de produits

Les variantes d’articles sont un excellent moyen de garder votre liste de produits sous contrôle. Par exemple, vous avez un grand nombre d’articles quasiment identiques et dont seule la couleur varie. Vous pouvez définir chaque variante comme un article séparé. Mais vous choisissez de configurer un article et de spécifier les différentes couleurs comme variantes de l’article.  

> [!TIP]
> Pour une introduction pratique à l’utilisation des variantes en production, voir [Procédure pas à pas : variantes](contoso-coffee/manufacturing/variants.md) pour les données de démonstration de Contoso Coffee.  

## <a name="add-variants-to-an-item"></a>Ajouter des variantes à un article

Si votre organisation a décidé d’utiliser des variantes, il est assez facile de définir des variantes pour un article.  

### <a name="to-add-variants"></a>Pour ajouter des variantes

1. Ouvrez [la page **Fiche article**](https://businesscentral.dynamics.com/?page=31), ouvrez l’article approprié.  
2. Sur la page **Fiche article**, sélectionnez l’action **Article**, puis l’action **Variantes**.  
3. Dans la page **Variantes article**, répertoriez les variantes.  

Ensuite, lorsque vous créez un document de vente et ajoutez l’article, vous pouvez spécifier la variante de l’article dans le champs **Code variante**. La même chose s’applique aux documents achat.  

## <a name="item-availability-by-variant"></a>Dispo. article par variante

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Exiger l’utilisation de variantes

À compter de la 2è vague de lancement 2022, les administrateurs peuvent exiger des utilisateurs qu’ils précisent la variante dans les documents et les journaux pour les articles avec des variantes. Pour activer la fonctionnalité, accédez à la page **Paramètres stock**, puis sélectionnez le champ **Variante obligatoire si elle existe**. Vous pouvez remplacer ce paramètre global pour des éléments spécifiques.  

Sur les fiches article, le champ **Variante obligatoire si elle existe** a les options suivantes :

|Valeur de champ |Désignation|
|---------|----|
|Par défaut| La définition de **Paramètres stock** s’applique à cet article.|
|N°| Les utilisateurs ne sont pas tenus de spécifier une variante pour cet article.|
|Oui| Si l’article a une ou plusieurs variantes, les utilisateurs doivent spécifier la variante appropriée. S’ils ne le font pas, ils ne pourront pas publier la transaction.|

> [!NOTE]
> Ces paramètres n’affectent pas les articles qui n’ont pas de variantes.

Si la fonctionnalité est activée, les utilisateurs ne peuvent pas publier d’entrée si la variante n’est pas spécifiée.

## <a name="categories-attributes-and-variants"></a>Catégories, attributs et variantes

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Voir aussi

[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Définir des informations générales relatives aux stocks](inventory-how-setup-general.md)  
[Procédure pas à pas : variantes](contoso-coffee/manufacturing/variants.md)  
