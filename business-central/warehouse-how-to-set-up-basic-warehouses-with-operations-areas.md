---
title: Configurer des entrepôts de base avec les zones d’opérations
description: 'Configurez les zones d’opérations d’entrepôt et utilisez les mouvements de stock, les prélèvements et les rangements pour déplacer les marchandises entre elles.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '6774, 6775, 6776'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Configurer des entrepôts de base avec les zones d’opérations

Si les zones Opérations internes telles que la production ou l’assemblage existent dans les configurations entrepôt de base dans lesquelles les magasins utilisent le champ de configuration **Emplacement obligatoire** et éventuellement les champs **Prélèvement requis** et **Rangement requis**, vous pouvez utiliser les documents d’entrepôt de base suivants pour enregistrer vos activités entrepôt pour des zones Opérations internes :  

- Page **Liste de mouvement de stock**.  
- Page **Liste des prélèvements stock**.  
- Page **Liste des rangements stock**.

> [!NOTE]
> Bien que les paramètres soient appelés **Prélèvement requis** et **Rangement requis**, vous pouvez quand même valider les réceptions et les expéditions directement à partir des documents commerciaux origine dans les magasins où vous cochez ces cases.  

Pour utiliser ces pages avec des opérations internes, par exemple pour prélever et déplacer des composants vers la production, vous devez effectuer tout ou partie des étapes de configuration suivantes, en fonction du contrôle que vous souhaitez exercer :  

- Activer les documents de prélèvement stock, de mouvement de stock et de rangement.  
- Définir les structures d’emplacement par défaut pour les composants et les produits finis s’écoulant depuis ou vers les ressources opérationnelles.  
- Créer des emplacements de destination et d’origine dédiés à des ressources opérationnelles spécifiques pour empêcher le prélèvement des articles pour les documents sortants.

Les codes emplacement qui sont paramétrés dans les fiches magasin définissent un flux entrepôt par défaut pour des activités spécifiques, telles que les composants d’un département assemblage. Des fonctionnalités supplémentaires existent pour s’assurer que des articles placés dans un emplacement particulier ne peuvent ni être déplacés vers d’autres activités, ni être prélevés pour ces dernières. Pour plus d’informations, voir [Pour créer des emplacements composants dédiés](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Les procédures suivantes sont basées sur la configuration d’activités entrepôt de base autour d’une zone de production. Les étapes sont similaires pour d’autres zones Opérations, telles que l’assemblage, la gestion des services et les projets.  

> [!NOTE]  
>  Dans la procédure suivante, le champ de configuration **Emplacement obligatoire** dans les fiches magasin est sélectionné en tant que condition préalable car il est considéré comme point de départ de tout niveau de gestion d’entrepôt.  

## Pour activer les documents de stock pour les activités d’opérations internes

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.
2. Ouvrez la fiche magasin que vous voulez configurer.  
3.  Sur le raccourci **Entrepôt**, cochez la case **Rangement requis** pour indiquer que lorsqu’un document origine entrant ou interne avec un code emplacement est lancé, il est possible de créer un document rangement stock ou mouvement de stock.  
4.  Cochez la case **Prélèvement requis** pour indiquer que lorsqu’un document origine sortant ou interne avec un code emplacement est créé, il est obligatoire de créer un document prélèvement stock ou mouvement de stock.  

## Pour définir une structure d’emplacement par défaut dans la zone de fabrication

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.
2. Ouvrez l’emplacement que vous voulez configurer.  
3.  Sur le raccourci **Emplacements**, dans le champ **Code empl. atelier ouvert**, entrez le code de l’emplacement dans la zone de production comportant des composants en nombre suffisant que l’opérateur machine peut consommer sans demander une activité entrepôt pour les apporter à l’emplacement. Les articles qui sont stockés dans cet emplacement sont habituellement configurés pour la validation automatique ou la consommation. Cela signifie que le champ **Méthode consommation** indique **Aval** ou **Amont**.  
4. Dans le champ **Emplacement des consommations** saisissez le code de l’emplacement dans la zone de production où les composants qui sont prélevés pour la production dans ce magasin sont stockés par défaut avant de pouvoir être consommés. Les articles qui sont stockés dans cet emplacement sont habituellement configurés pour la validation manuelle de la consommation. Cela signifie que le champ **Méthode consommation** indique **Manuel**, **Prélèvement + Aval** ou **Prélèvement + Amont** pour les prélèvements entrepôt et les mouvements de stock.  

    > [!NOTE]  
    > Lorsque vous utilisez des prélèvements stock, le champ **Code emplacement** sur une ligne composant d’ordre de fabrication. définit l’emplacement de *prélèvement* où les composants sont déduits lors de la validation de la consommation. Lorsque vous utilisez des mouvements de stock, le **Code emplacement** sur des lignes composant d’ordre cde fabrication définit l’emplacement *placement* dans la zone Opérations où l’employé du magasin doit placer les composants.  

5. Sur le raccourci **Emplacements**, dans le champ **Code empl. après production**, entrez le code de l’emplacement dans la zone de production où les produits finis terminés sont extraits par défaut si le processus implique une activité entrepôt. Dans les configurations entrepôt de base, l’activité est enregistrée en tant que rangement stock ou mouvement de stock.  

désormais, les lignes composant O.F. présentant ce code emplacement par défaut nécessitent que les composants consommés en aval soient stockés dans cet emplacement. Toutefois, jusqu’à la consommation des composants de cet emplacement, d’autres demandes de composant peuvent y effectuer un prélèvement ou une consommation, car elles sont encore considérées comme du contenu emplacement disponible. Pour vous assurer que le contenu de l’emplacement est uniquement disponible à une demande de composant qui utilise cet emplacement des consommations, vous devez sélectionner le champ **Dédié** sur la ligne de ce code emplacement sur la page **Emplacements** à laquelle vous accédez à partir de la fiche magasin.

Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de votre configuration.  

![Organigramme Flux d’emplacement.](media/binflow.png "BinFlow")

## Pour définir une structure d’emplacement par défaut dans la zone d’assemblage

Les composants pour les commandes d’assemblage ne peuvent pas être prélevés ni validés avec des prélèvements stock. À la place, utilisez la page **Mouvement de stock**. Pour plus d’informations, consultez [Prélever ou déplacer pour la fabrication, l’assemblage ou les projets dans les configurations de stockage de base](warehouse-how-to-pick-for-production.md).

En cas de prélèvement et d’expédition de quantités de lignes vente assemblées pour commande, vous devez suivre certaines règles en créant les lignes prélèvement stock. Pour plus d’informations, reportez-vous à la section « Traitement des articles à assembler pour commande dans les prélèvements stock » dans [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).

Pour plus d’informations, voir [Gestion des assemblages](assembly-assemble-items.md).

### Pour configurer la création automatique d’un mouvement stock lors de la création du prélèvement stock pour l’élément d’assemblage

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration d’assemblage**, puis choisissez le lien associé.
2. Cochez la case **Créer des mouvements automatiquement**.

### Pour configurer l’emplacement dans la zone d’assemblage où les composants sont stockés par défaut avant de pouvoir être consommés dans l’assemblage

La valeur de ce champ est automatiquement insérée dans le champ **Code emplacement** des lignes d’ordre d’assemblage lorsque ce magasin est saisi dans le champ **Code magasin** de la ligne d’ordre d’assemblage.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.
2. Ouvrez l’emplacement que vous voulez configurer.
3. Renseignez le champ **Code empl. vers assemblage**.

### Pour configurer l’emplacement de zone d’assemblage au niveau duquel les éléments d’assemblage terminés sont validés lorsqu’ils sont associés au stock

La valeur de ce champ est automatiquement insérée dans le champ **Code emplacement** des en-têtes d’ordre d’assemblage lorsque ce code de magasin est saisi dans le champ **Code magasin** de l’en-tête d’ordre d’assemblage.

Les codes emplacement qui sont paramétrés dans les fiches magasin définissent un flux entrepôt par défaut pour des activités entrepôt spécifiques, telles que la consommation des composants d’une zone d’assemblage. Des fonctionnalités supplémentaires existent pour s’assurer que des articles placés dans un emplacement par défaut ne peuvent ni être déplacés vers d’autres activités, ni être prélevés pour ces dernières.

> [!NOTE]
> Cette configuration s’applique uniquement aux magasins pour lesquels le champ Emplacement obligatoire est sélectionné.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.
2. Ouvrez l’emplacement que vous voulez configurer.
3. Renseignez le champ **Code empl. depuis assemblage**.

### Pour configurer l’emplacement au niveau duquel les éléments d’assemblage terminés sont validés lorsqu’ils sont associés à une commande vente

Les articles d’assemblage sont expédiés immédiatement à partir de cet emplacement, via un prélèvement stock, afin d’honorer la commande vente.

> [!NOTE]
> Ce champ n’est pas disponible si le magasin est configuré pour utiliser les prélèvement et rangement suggérés.

Le code emplacement est copié de la ligne commande vente vers l’en-tête ordre d’assemblage pour indiquer aux travailleurs à la chaîne où placer la production pour préparer son expédition. Il est également copié dans la ligne prélèvement stock pour indiquer aux magasiniers où le récupérer au moment de l’expédition.

> [!NOTE]
> L’emplacement expédition Assembler pour commande est toujours vide. Lorsque vous validez une ligne vente assembler pour commande, le contenu de l’emplacement fait d’abord l’objet d’un ajustement positif basé sur le résultat d’assemblage. Ensuite, il fait immédiatement l’objet d’un ajustement négatif basé sur la quantité expédiée.

La valeur de ce champ est automatiquement insérée dans le champ Code emplacement des lignes commande vente dont le champ **Qté vers Assembler pour commande** contient une quantité. Cela se produit également si le champ a la valeur **Assembler pour commande** dans le champ **Système réappro.**.

Si **Code empl. exp. ass. pr comm.** est vide, alors le champ **Code empl. depuis assemblage** est utilisé. Si vous laissez les deux champs de configuration vides, le dernier emplacement utilisé incluant une valeur est utilisé dans le champ **Code emplacement** des lignes commande vente.

Le même code emplacement est également copié vers le champ **Code emplacement** de la ligne prélèvement stock qui gère l’expédition de la quantité à assembler pour commande. Pour plus d’informations, reportez-vous à la section « Traitement des articles à assembler pour commande dans les prélèvements stock » dans [Prélever des articles avec les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.
2. Ouvrez l’emplacement que vous voulez configurer.
3. Renseignez le champ **Code empl. exp. ass. pr comm.**.

## Pour créer des emplacements composants dédiés

Vous pouvez spécifier que les quantités d’un emplacement soient protégées des prélèvements d’autres demandes que la demande de leurs objectifs actuels.

Les quantités des magasins réservés peuvent encore être réservées. Par conséquent, les quantités figurant dans des magasins réservés sont incluses dans le champ **Quantité totale disponible** de la page **Réservation**.

Par exemple, si un centre de charge est configuré avec un code emplacement dans le champ **Code empl. des consommations**. Les lignes composant O.F. présentant ce code emplacement nécessitent que les composants consommés en aval soient stockés dans cet emplacement. Toutefois, jusqu’à la consommation des composants de cet emplacement, d’autres demandes de composant peuvent y effectuer un prélèvement ou une consommation, car elles sont encore considérées comme du contenu emplacement disponible. Pour vous assurer que le contenu de l’emplacement est uniquement disponible à une demande de composant qui utilise cet emplacement des consommations, vous devez sélectionner le champ **Dédié** sur la ligne de ce code emplacement sur la page **Emplacements** à laquelle vous accédez à partir de la fiche magasin.

La réservation d’un emplacement fournit la même fonctionnalité permettant d’utiliser les types emplacement, disponible uniquement dans l’entreposage avancé. Pour plus d’informations, voir [Configurer des types d’emplacement](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Des articles dans des magasins réservés ne sont pas protégés lorsqu’ils sont prélevés et consommés comme composants de production à l’aide de la page Prélvmt invent.

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé. Sélectionnez le magasin que vous voulez mettre à jour.  
2.  Choisissez l’action **Emplacements**.  
3.  Sélectionnez le champ **Dédié** pour chaque emplacement à utiliser exclusivement pour certaines opérations internes et si vous souhaitez que les quantités soient réservées pour ces opérations internes une fois placées à cet endroit.  

> [!NOTE]  
>  L’emplacement doit être vide avant que vous puissiez sélectionner ou désactiver le champ **Dédié**.

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
