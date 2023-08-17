---
title: Configurer des attributs article et les affecter aux articles
description: 'Décrit comment configurer les valeurs d’attributs d’articles, par exemple, qui peuvent être utilisées comme mots recherchés, et les affecter aux articles et aux catégories article.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'categories, search words, facets'
ms.search.forms: '7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-item-attributes"></a>Utiliser les attributs d’article

Lorsque les clients recherchent des renseignements au sujet d’un article, par courrier ou via une boutique en ligne, ils peuvent effectuer leur recherche en fonction de caractéristiques, telles que la hauteur et l’année du modèle. Pour assurer le service de ce client, vous pouvez affecter des valeurs attribut article de différents types à vos articles, qui peuvent être utilisées pour rechercher les articles.

Vous pouvez également allouer les attributs d’article aux catégories d’article, qui s’appliquent ensuite aux articles qui utilisent les catégories d’article. Pour plus d’informations, voir [Catégoriser des articles](inventory-how-categorize-items.md).

> [!TIP]  
> Si vous joignez des images aux articles, l’extension Analyseur Image peut détecter les attributs dans l’image, et suggérer des attributs que vous pouvez décider d’affecter ou non. L’extension est prête. Vous devez juste l’activer. Pour plus d’informations, voir [Extension d’analyseur Image](ui-extensions-image-analyzer.md).

## <a name="create-item-attributes"></a>Créer des attributs d’article

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Attributs d’article**, puis choisissez le lien associé.
2. Sur la page **Attributs article**, sélectionnez l’action **Nouveau**.
3. Sur la page **Attribut article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Si vous sélectionnez **Option** dans le champ **Type**, vous pouvez sélectionner l’action **Valeurs attribut article** pour créer des valeurs pour l’attribut d’article. Pour en savoir plus, voir [Pour créer des valeurs pour les attributs d’article de type Option](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="create-values-for-item-attributes-of-type-option"></a>Créer des valeurs pour les attributs d’article de type Option

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Attributs d’article**, puis choisissez le lien associé.
2. Sur la page **Attributs article**, sélectionnez un attribut d’article de type **Option** pour lequel vous souhaitez créer des valeurs, puis sélectionnez l’option **Valeurs attribut article**.
3. Sur la page **Valeurs attribut article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="assign-item-attributes-to-items"></a>Affecter des attributs article à des articles

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis choisissez le lien associé.
2. Sur la page **Articles**, sélectionnez l’article auquel vous souhaitez affecter des attributs article, puis sélectionnez l’action **Attributs**.
3. Sur la page **Valeurs attributs article**, sélectionnez l’action **Nouveau**.
4. Sélectionnez le bouton de recherche dans le champ **Attribut** et sélectionnez un attribut d’article existant. Sinon, sélectionnez l’action **Nouveau** pour créer tout d’abord un nouvel attribut comme expliqué dans [Créer des attributs d’article](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Dans le champ **Valeur**, saisissez la valeur d’attribut article, telle que « 2010 » pour l’attribut **Année modèle**.
6. Pour les attributs d’article de type **Option**, sélectionnez le bouton de recherche dans le champ **Valeur** et sélectionnez une valeur d’attribut d’article. Sinon, sélectionnez l’action **Nouveau** pour créer tout d’abord une nouvelle valeur d’attribut comme expliqué dans [Créer des valeurs pour les attributs d’article de type Option](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Répétez les étapes 4 à 6 pour tous attributs article que vous souhaitez affecter à l’article.

## <a name="assign-item-attributes-to-item-categories"></a>Affecter des attributs article aux catégories article

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Catégories d’article**, puis choisissez le lien associé.
2. Sur la page **Catégories d’article**, sélectionnez la catégorie article à laquelle vous souhaitez affecter des attributs article, puis sélectionnez l’action **Modifier**.
3. Sur la page **Fiche catégorie article**, sur le raccourci **Attributs**, sélectionnez l’action **Nouveau**.
4. Sélectionnez le bouton de recherche dans le champ **Attribut** et sélectionnez un attribut d’article existant. Sinon, sélectionnez l’action **Nouveau** pour créer tout d’abord un nouvel attribut comme expliqué dans [Créer des attributs d’article](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Dans le champ **Valeur par défaut**, cliquez sur le bouton de recherche et sélectionnez une valeur d’attribut d’article.
6. Répétez les étapes 4 et 5 pour tous attributs article que vous souhaitez affecter à la catégorie d’article.

> [!NOTE]  
> Les attributs article pour les catégories d’article seront transmis aux catégories d’article enfant. Cela est indiqué par le champ **Hérité de** sur le raccourci **Attributs**. Pour plus d’informations, voir [Catégoriser des articles](inventory-how-categorize-items.md).

## <a name="filter-by-item-attributes"></a>Filtrer par attribut d’article

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sur la page **Articles**, sélectionnez l’action **Filtrer par attributs**.
3. Sur la page **Filtrer les articles par attribut**, cliquez sur le bouton de recherche du champ **Attribut**, puis sélectionnez un attribut article.
4. Dans le champ **Valeur**, cliquez sur le bouton de recherche et sélectionnez une valeur d’attribut selon laquelle filtrer les articles.

    > [!NOTE]  
    > Vous pouvez uniquement sélectionner des valeurs directement pour les attributs article dotés de valeurs fixes, telles que Couleur. Pour modifier des attributs article dotés de valeurs variables, telles que Largeur, vous devez spécifier la valeur attribut article en sélectionnant d’abord une condition. Reportez-vous à l’étape 5.
5. Dans le champ **Valeur** d’un attribut article variable, cliquez sur le bouton de recherche.
6. Sur la page **Spécifier la valeur du filtre**, dans le champ **Condition**, cliquez sur la flèche déroulante et sélectionnez une condition.
7. Dans le champ **Valeur**, saisissez une valeur attribut selon laquelle filtrer les articles.

    **Exemple** : pour filtrer les articles pour lesquels la description matière se termine par « bleu », renseignez les champs comme suit : champ **Attribut** : Description matière, champ **Condition** : Se termine par, champ **Valeur** : bleu.
8. Choisissez le bouton **OK**.

Les articles de la page **Articles** sont filtrés selon les valeurs attribut article spécifiées.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Catégoriser des articles](inventory-how-categorize-items.md)  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
