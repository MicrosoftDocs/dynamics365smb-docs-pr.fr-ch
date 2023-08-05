---
title: Configurer une fiche magasin et définir des acheminements de transfert (contient une vidéo)
description: 'Si vous achetez, stockez ou commercialisez des articles à plusieurs endroits, vous pouvez configurer chaque lieu en tant qu’emplacement.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
---
# Configurer des magasins

Les magasins sont des endroits tels que des entrepôts où vous achetez, stockez ou vendez des articles. [!INCLUDE [prod_short](includes/prod_short.md)] utilise des magasins pour aider à suivre les stocks dans les cas simples et complexes dans les processus d’entrepôt.

Vous pouvez ensuite créer des lignes de document pour un magasin spécifique, voir la disponibilité par magasin, et transférer le stock entre magasins. Pour en savoir plus, accédez à la [Gérer le stock](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## Fiches magasin

Vous spécifiez des informations sur un magasin, par exemple un entrepôt ou un centre de distribution sur la page **Fiche magasin**. Affectez un nom et un code représentatifs à chaque magasin. Il vous suffit ensuite de saisir le code magasin dans d’autres parties du programme lorsque vous souhaitez enregistrer les transactions d’un magasin en particulier.  

Vous pouvez entrer des informations sur les emplacements et les règles entrepôt pour chaque magasin. En fonction de vos stratégies d’entrepôt, vous pouvez utiliser les options sur le raccourci **Emplacements** pour spécifier lesquels utiliser par défaut pour les transactions. Si vous utilisez les prélèvements et rangements suggérés, vous pouvez utiliser la plupart des options du raccourci **Config. emplacement** pour définir la façon dont vous souhaitez utiliser les différentes fonctions d’entrepôt avancées.  

Certains champs d’option dépendent des paramètres dans la page **Fiche magasin** pour limiter les combinaisons de paramètres non pris en charge.  

Choisissez les actions **Zones** ou **Emplacements** pour visualiser des informations sur les zones et les emplacements sont définis pour le magasin.

### Pour configurer un magasin

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Magasins**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Répétez les étapes 2 et 3 pour chaque magasin dans lequel vous souhaitez conserver le stock.

> [!NOTE]  
> De nombreux champs de la page Fiche magasin se rapportent à la gestion des articles dans les processus enlogement et désenlogement. Ces champs ne sont pas pertinents pour les entreprises qui n’ont pas besoin des fonctionnalités d’entrepôt complexes. Pour en savoir plus, accédez à [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Vous pouvez modifier la configuration d’un emplacement tant qu’il n’a pas d’écritures comptables article.  

Si vous avez plusieurs magasins, vous pouvez définir des acheminements transfert entre les magasins. Pour en savoir plus sur les itinéraires de transfert, accédez à [Pour créer un itinéraire de transfert](inventory-how-setup-locations.md#to-create-a-transfer-route).

### Pour créer un acheminement transfert

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Acheminements de transfert**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
4. Sur la page **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Vous pouvez à présent transférer des articles en stock entre deux magasins. Pour en savoir plus sur les transferts, accédez à [Transférer le stock entre les magasins](inventory-how-transfer-between-locations.md).

## Emplacements

Les emplacements représentent la structure de base de l’entrepôt et peuvent suggérer où placer les articles. Vos emplacements peuvent avoir du contenu ou être flottants sans contenu spécifique.

Pour utiliser la fonctionnalité d’emplacement liée au magasin, vous devez d’abord activer la fonctionnalité sur la page **Fiche magasin** sur le raccourci **Entrepôt** en activant le bouton à bascule **Emplacement obligatoire**. Vous pouvez concevoir le flux d’articles à l’emplacement en spécifiant des codes d’emplacement dans les champs des processus d’entrepôt sur les raccourcis **Emplacements** et **Stratégies d’emplacement**.

> [!NOTE]
> Avant de pouvoir spécifier les codes emplacement sur un magasin, vous devez les créer. Pour en savoir plus sur les emplacements, accédez à [Créer des emplacements](warehouse-how-to-create-individual-bins.md) et [Configurer les types d’emplacements](warehouse-how-to-set-up-bin-types.md).  

## Zones

Si vous souhaitez structurer vos emplacements en zones, vous pouvez le faire dans la page **Zones**. Lorsque vous affectez une zone à des emplacements, [!INCLUDE [prod_short](includes/prod_short.md)] copie les informations de la zone vers les emplacements. Vous pouvez également choisir de configurer une zone et d’utiliser des emplacements seuls pour organiser votre entrepôt. Pour en savoir plus sur les zones, accédez à [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

## Axes analytiques par défaut pour les magasins

Les axes analytiques sont des valeurs qui permettent de catégoriser les écritures afin de pouvoir les suivre et les analyser avec différents outils de création de rapports. Par exemple, les axes analytiques peuvent indiquer le service ou le projet dont est issue une écriture. Le fait d’avoir des axes analytiques par défaut aide les gens à éviter de faire des erreurs et d’avoir à saisir manuellement les axes analytiques au niveau de la transaction si toutes les marchandises proviennent d’un seul magasin et d’un même service.

Pour définir les axes analytiques par défaut pour un magasin, allez sur la page **Fiche magasin** et choisissez **Axes analytiques**. Par la suite, les axes analytiques par défaut du magasin sont attribuées aux documents suivants lorsque vous choisissez l’emplacement sur une ligne.

* Ordres de transfert
* Commandes d’inventaire
* Expéditions stock
* Réceptions stock
* Feuilles article

Au besoin, vous pouvez supprimer ou modifier les axes analytiques sur les lignes. Dans le champ **Contrôle validation**, pouvez exiger que les personnes spécifient des axes analytiques pour des magasins spécifiques avant de pouvoir valider une écriture. Si vous souhaitez que les utilisateurs puissent choisir uniquement certaines sections analytiques, vous pouvez spécifier celles-ci dans le champ **Filtre valeurs autorisées**. Vous pouvez également inclure des sections analytiques de magasin sur la page **Affect. analytique prioritaire** et **Croisements analytiques** pour les combinaisons de règles de priorité et d’axe analytique.

Puisque les documents d’ordre transfert et les feuilles de reclassement traitent de plusieurs magasins, l’ordre dans lequel vous saisissez les données est important. Les axes analytiques par défaut sont copiés à partir du dernier champ d’emplacement (l’emplacement en transit est ignoré).

### Exemple des axes analytiques par défaut sur les emplacements

Les exemples suivants illustrent comment l’axe analytique par défaut est utilisé.

Vous avez les paramètres d’axe analytique suivants :

* Magasin EST. L’axe analytique du service est ADM
* Magasin OUEST. L’axe analytique du service est PROD

Vous spécifiez le magasin sur un ordre transfert comme suit :

1. Magasin de provenance = EST
2. Magasin de destination = OUEST

L’axe analytique PROD est copié à partir du magasin OUEST.

Vous remplissez les champs dans l’ordre inverse, comme suit :

1. Magasin de destination = OUEST
2. Magasin de provenance = EST

L’axe analytique ADM est copié à partir du magasin EST.

## Voir la formation associée sur [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## Voir aussi

[Gestion du stock](inventory-manage-inventory.md)  
[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)  
[Créer emplacements](warehouse-how-to-create-individual-bins.md)  
[Configurer des types d’emplacement](warehouse-how-to-set-up-bin-types.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
