---
title: Créer emplacements
description: 'Générez des groupes d’emplacements similaires dans la feuille de calcul prévue à cet effet, créez des emplacements individuellement sur la fiche magasin ou automatiquement sur la feuille de calcul de création des emplacements.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: bholtorf
---
# Créer emplacements

La méthode la plus efficace pour créer les emplacements de votre entrepôt consiste à générer des groupes d’emplacements identiques dans la feuille de création d’emplacements, mais vous pouvez également créer vos emplacements séparément à partir de la fiche magasin. Vous pouvez également utiliser une fonction de la page **Feuille création emplacement** pour créer des emplacements automatiquement.  

## Pour créer un emplacement à partir de la fiche magasin

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.  
2.  Sélectionnez le magasin à partir duquel vous souhaitez créer un emplacement, puis choisissez l’action **Emplacements**.  
3. Sélectionnez l’action **Nouveau**.
4. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Le champ Réservé

Le champ **Réservé** sur la page **Emplacements** indique que les quantités de l’emplacement sont protégées des prélèvements d’autres demandes. Toutefois, les quantités des magasins réservés peuvent encore être réservées. Par conséquent, les quantités figurant dans des magasins réservés sont incluses dans le champ **Quantité totale disponible** de la page **Réservation**.

La réservation d’un emplacement fournit la même fonctionnalité dans l’entreposage de base permettant d’utiliser les types emplacement, disponible uniquement dans l’entreposage avancé. Pour plus d’informations, voir [Configurer des types d’emplacement](warehouse-how-to-set-up-bin-types.md).

### Exemple :

Un centre de charge est configuré avec un code emplacement dans le champ **Code empl. des consommations**. Les lignes composant O.F. présentant ce code emplacement nécessitent que les composants consommés en aval soient stockés dans cet emplacement. Toutefois, jusqu’à la consommation des composants de cet emplacement, d’autres demandes de composant peuvent y effectuer un prélèvement ou une consommation, car elles sont encore considérées comme du contenu emplacement disponible. Pour vous assurer que le contenu de l’emplacement est uniquement disponible à une demande de composant qui utilise cet emplacement des consommations, vous devez sélectionner le champ **Réservé** sur la ligne de ce code emplacement.

> [!Caution]
> Des articles dans des magasins réservés ne sont pas protégés lorsqu’ils sont prélevés et consommés comme composants d’assemblage ou de production sur la page **Prélvmt invent**. Pour plus d’informations, consultez [Prélever pour la fabrication ou l’assemblage dans les configurations de stockage de base](warehouse-how-to-pick-for-production.md).

## Pour créer séparément des emplacements dans la feuille de création d’emplacements

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille création emplacement**, et choisissez le lien associé.  
2.  Sur chaque ligne, renseignez les champs requis pour nommer et caractériser les emplacements que vous créez.  
3.  Choisissez l’action **Créer emplacements**.  

## Pour créer des emplacements automatiquement dans la feuille de création d’emplacements

Avant de commencer à créer automatiquement des emplacements dans la feuille, déterminez les types d’emplacement essentiels à vos opérations, ainsi que la circulation des articles la plus pratique dans la structure physique de votre entrepôt.  

> [!NOTE]  
> Dès que vous utilisez un emplacement, vous ne pouvez pas le supprimer sauf s’il est vide. En revanche, si vous souhaitez utiliser un autre système d’attribution de nom d’emplacement, vous pouvez utiliser la feuille reclassement pour déplacer effectivement vos articles vers un nouveau système d’emplacements. Cependant, ce processus est manuel et prend du temps ; il est donc préférable de configurer correctement vos emplacements dès le début.  

Pour travailler avec la page **Feuille création emplacement**, vous devez être défini comme magasinier à l’endroit où les emplacements existent. Pour plus d’informations, voir [Configurer des employés d’entrepôt](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille création emplacement**, et choisissez le lien associé.  
2.  Choisissez l’action **Calculer emplacements**.
3. Sur la page **Calculer emplacements**, sous **Code modèle emplacement**, sélectionnez le modèle emplacement à utiliser comme modèle pour les emplacements que vous créez.
4.  Saisissez une description pour les emplacements que vous êtes en train de créer.  
5.  Pour créer des codes d’emplacement, renseignez les champs **Du n°** et **Au n°** dans les trois catégories indiquées sur la page : **Travée**, **Section** et **Niveau**. Le code emplacement peut contenir au maximum 20 caractères.  

    > [!NOTE]  
    >  Le nombre de caractères saisis dans les champs des trois catégories \(par exemple, les caractères saisis dans les trois champs **Du n°**\), auxquels s’ajoutent les éventuels séparateurs de champs, doit être inférieur ou égal à 20.  

     Vous pouvez utiliser des lettres dans le code, mais la lettre utilisée doit être identique dans les champs **Du n°** et **Au n°** . Par exemple, vous pouvez définir la partie Travée du code de la manière suivante : **Du n° A01** et **Au n° A10**. L’application n’est pas configurée pour générer des codes comprenant des suites de lettres (par exemple, de A01 à F05).  

6.  Si vous souhaitez qu’un caractère (par exemple, un trait d’union) sépare les champs des catégories que vous avez définis comme faisant partie du code emplacement, renseignez le champ **Séparateur de champs** avec ce caractère.  
7.  Pour que l’application ne crée pas de ligne pour un emplacement si elle existe déjà, sélectionnez le champ **Vérifier existence emplacement**.  
8. Une fois le remplissage de toutes les lignes terminé, sélectionnez le bouton **OK**.

    L’application crée dans la feuille une ligne pour chaque emplacement. Vous pouvez maintenant supprimer certains emplacements, par exemple si vous avez un casier qui vous permet d’accéder aux deux premiers niveaux de deux sections.  

9. Lorsque vous avez supprimé tous les emplacements inutiles, choisissez l’action **Créer emplacements** pour que l’application crée des emplacements pour chaque ligne de la feuille.  

Répétez l’opération pour un autre ensemble d’emplacements jusqu’à ce que vous ayez créé tous les emplacements de votre entrepôt.  

## Voir la [formation Microsoft](/training/modules/create-new-bins/) associée

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
