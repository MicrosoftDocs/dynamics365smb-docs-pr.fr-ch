---
title: Comment configurer des magasins de sorte qu’ils utilisent des emplacements
description: Les emplacements représentent la structure d’entrepôt de base et sont utilisés pour faire des propositions relatives à l’emplacement des articles.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# Configurer des magasins de sorte qu’ils utilisent des emplacements

Les emplacements représentent la structure d’entrepôt de base et sont utilisés pour faire des propositions relatives à l’emplacement des articles. Lorsque vous avez créé vos emplacements, vous pouvez définir précisément le contenu que vous souhaitez placer dans chacun d’entre eux, ou l’emplacement peut être utilisé en tant qu’emplacement dynamique sans contenu spécifié.  

Pour utiliser la fonctionnalité liée au magasin, vous devez d’abord l’activer dans la fiche **magasin**. Ensuite, vous définissez la circulation des articles dans le magasin en spécifiant les codes emplacement dans les champs de configuration qui représentent les différents flux.  

> [!NOTE]  
>  Avant de pouvoir spécifier les codes emplacement sur la fiche magasin, il convient de les créer. Pour plus d’informations, voir [Créer emplacements](warehouse-how-to-create-individual-bins.md).  

## Pour configurer un magasin de sorte qu’il utilise des emplacements

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.  
2.  Sélectionnez le magasin dans lequel vous souhaitez utiliser des emplacements.  
3.  Choisissez l’action **Modifier**.  
4.  Sur le raccourci **Entrepôt**, cochez la case **Emplacement obligatoire**.  
5.  Si vous n’avez pas recours à un prélèvement et à un rangement suggérés dans le magasin, renseignez le champ **Sélection emplacement par déf** en y indiquant la méthode d’attribution d’un emplacement par défaut à un article que le système doit utiliser.  
6.  Ouvrez la fiche de l’emplacement pour lequel vous souhaitez configurer des emplacements.
7.  Sur le raccourci **Emplacements**, sélectionnez les emplacements que vous voulez utiliser par défaut pour les réceptions, les expéditions, les enlogements et les désenlogements, ainsi que pour les emplacements atelier ouverts.  
8.  Les codes emplacement que vous indiquez ici s’affichent automatiquement dans les en-têtes et sur les lignes de différents documents entrepôt. Les emplacements par défaut définissent tous les placements de début ou de fin des articles dans l’entrepôt.  
9.  En cas d’utilisation d’un prélèvement et d’un rangement suggérés, sélectionnez un emplacement pour les ajustements entrepôt. Le code emplacement dans le champ **Code empl. ajustement** définit l’emplacement virtuel dans lequel enregistrer les différences de stock lorsque vous enregistrez soit les différences observées dans la feuille article entrepôt, soit les différences calculées lorsque vous enregistrez un inventaire entrepôt.  
10. Renseignez les champs du raccourci **Config. emplacement** s’ils sont appropriés à votre entrepôt. Les champs les plus importants sont les suivants : **Politique capacité empl**, **Autoriser déconditionnement** et **Code modèle rangement**.  
11. Sur les champs **Entrepôt**, renseignez les champs **Délai désenlogement**, **Délai enlogement** et **Code calendrier principal**. Pour plus d’informations, voir [Configurer des calendriers principaux](across-how-to-assign-base-calendars.md).

## Renseigner l’emplacement consommation

Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

![Organigramme Flux d’emplacement.](media/binflow.png "BinFlow")  

## Voir la [formation Microsoft](/training/modules/configure-bins-location/) associée

## Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de Warehouse Management](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
