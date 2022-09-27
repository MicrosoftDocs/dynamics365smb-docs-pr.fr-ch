---
title: Configurer une fiche magasin et définir des acheminements de transfert (contient une vidéo)
description: Si vous achetez, enregistrez, ou vendez des articles à plusieurs magasins ou entrepôt, vous devez configurer chaque magasin avec une fiche magasin et définir des acheminements transfert.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 0888a0a47f3a5ae58dcf7712218f801cde1711c5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528319"
---
# <a name="set-up-locations"></a>Configurer des magasins

Les magasins sont des endroits tels que des entrepôts où vous achetez, stockez ou vendez des articles. [!INCLUDE [prod_short](includes/prod_short.md)] utilise des magasins pour aider à suivre les stocks dans les cas simples et complexes dans les processus d’entrepôt.

Vous pouvez ensuite créer des lignes de document pour un magasin spécifique, voir la disponibilité par magasin, et transférer le stock entre magasins. Pour plus d’informations, reportez-vous à [Gestion du stock](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Fiches magasin

Vous spécifiez des informations sur un magasin, par exemple un entrepôt ou un centre de distribution sur la page **Fiche magasin**. Affectez un nom et un code représentatifs à chaque magasin. Il vous suffit ensuite de saisir le code magasin dans d’autres parties du programme lorsque vous souhaitez enregistrer les transactions d’un magasin en particulier.  

Vous pouvez entrer des informations sur les emplacements et les règles entrepôt pour chaque magasin. En fonction des règles entrepôt sélectionnées, vous pouvez utiliser les options du raccourci **Emplacements** pour définir les emplacements utilisés par défaut lorsque vous effectuez des transactions. Si vous utilisez les prélèvements et rangements suggérés, vous pouvez utiliser la plupart des options du raccourci **Config. emplacement** pour définir la façon dont vous souhaitez utiliser les différentes fonctions d’entrepôt avancées.  

Certains champs d’option dépendent des paramètres dans la page **Fiche magasin** pour limiter les combinaisons de paramètres non pris en charge.  

Choisissez les actions **Zones** ou **Emplacements** pour visualiser des informations sur les zones et les emplacements sont définis pour le magasin.

### <a name="to-set-up-a-location"></a>Pour configurer un magasin

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Magasins**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Répétez les étapes 2 et 3 pour chaque magasin dans lequel vous souhaitez conserver le stock.

> [!NOTE]  
> De nombreux champs de la page Fiche magasin se rapportent à la gestion des articles dans les processus enlogement et désenlogement. Ces champs ne sont pas pertinents pour les entreprises qui n’ont pas besoin des fonctionnalités d’entrepôt complexes. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).

Vous pouvez modifier la configuration d’un magasin ultérieurement, mais vous ne pouvez pas modifier la configuration des magasins qui ont des écritures comptables article.  

Si vous avez plusieurs magasins, vous pouvez définir des acheminements transfert entre les magasins. Pour plus d’informations, reportez-vous à [Créer des acheminement transfert ](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Pour créer un acheminement transfert

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Acheminements de transfert**, puis sélectionnez le lien associé.
2. Sinon, à partir de n’importe quelle page **Fiche magasin**, cliquez sur **Acheminements transfert**.
3. Sélectionnez l’action **Nouveau**.
4. Sur la page **Fiche magasin**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Vous pouvez à présent transférer des articles en stock entre deux magasins. Pour plus d’informations, voir [Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Emplacements

Les emplacements représentent la structure d’entrepôt de base et sont utilisés pour faire des propositions relatives à l’emplacement des articles. Lorsque vous avez créé vos emplacements, vous pouvez définir leur contenu ou ils sont utilisés en tant qu’emplacements dynamiques sans contenu spécifié. Les emplacements sont principalement utilisés dans les opérations d’entrepôt de base et avancées. Si vous gérez les stocks dans une configuration plus simple, vous n’avez probablement pas besoin d’emplacements.

Pour utiliser la fonctionnalité d’emplacement liée au magasin, vous devez d’abord activer la fonctionnalité sur la page **Fiche magasin** en sélectionnant le champ **Emplacement obligatoire** sur le raccourci **Entrepôt**. Ensuite, vous définissez la circulation des articles dans le magasin en spécifiant les codes emplacement dans les champs de configuration qui représentent les différents flux.

> [!NOTE]
> Avant de pouvoir spécifier les codes emplacement sur un magasin, vous devez les créer. Pour plus d’informations, voir [Créer des emplacements](warehouse-how-to-create-individual-bins.md) et [Configurer des types d’emplacement](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zones

Si vous souhaitez structurer vos emplacements en zones, vous pouvez le faire dans la page **Zones**.

[!INCLUDE [prod_short](includes/prod_short.md)] copie les champs que vous définissez pour une zone donnée dans les emplacements qui s’y trouvent. Cela signifie que vous pouvez affecter une zone à un emplacement ou à un modèle d’emplacement (filtre de création d’emplacement) et que plusieurs autres champs sont ensuite renseignés automatiquement.

Toutefois, vous pouvez choisir de configurer une seule zone et d’organiser votre entrepôt uniquement en fonction des emplacements. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Axes analytiques par défaut pour les magasins
Pour définir les axes analytiques par défaut pour un magasin, allez sur la page **Fiche magasin** et choisissez **Axes analytiques**. Par la suite, les axes analytiques par défaut du magasin sont attribuées aux documents lorsque vous choisissez l'emplacement sur une ligne. Au besoin, vous pouvez supprimer ou modifier les axes analytiques sur les lignes. Dans le champ **Contrôle validation**, pouvez exiger que les personnes spécifient des axes analytiques pour des magasins spécifiques avant de pouvoir valider une écriture. Si vous souhaitez que les utilisateurs puissent choisir uniquement certaines sections analytiques, vous pouvez spécifier celles-ci dans le champ **Filtre valeurs autorisées**. Vous pouvez également inclure des sections analytiques de magasin sur la page **Affect. analytique prioritaire** et **Croisements analytiques** pour les combinaisons de règles de priorité et d’axe analytique.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/trade-set-up-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Gestion du stock](inventory-manage-inventory.md)  
[Transfert de stock entre des magasins](inventory-how-transfer-between-locations.md)  
[Créer emplacements](warehouse-how-to-create-individual-bins.md)  
[Configurer des types d’emplacement](warehouse-how-to-set-up-bin-types.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
