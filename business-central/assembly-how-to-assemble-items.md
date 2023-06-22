---
title: Assembler des articles
description: Découvrez les processus d’assemblage pour commande et d’assemblage pour stock dans Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items" />Assembler des articles

Si le champ **Système réappro.** de la fiche client contient **Assemblage**, la méthode par défaut d’approvisionnement de l’article consiste à l’assembler conformément à une Nomenclature d’élément d’assemblage et potentiellement par une ressource spécifique. En savoir plus sur [Utilisation des Nomenclatures d’élément d’assemblage](assembly-how-work-assembly-boms.md). En savoir plus sur le paramétrage d’un élément d’assemblage dans [Description des processus Assembler pour commande et Assembler pour stock](assembly-assemble-to-order-or-assemble-to-stock.md).

Vous pouvez configurer les éléments d’assemblage pour deux processus d’assemblage.

|Traitement  |Désignation  |
|---------|---------|
|Assembler pour stock     | Articles que vous assemblez et stockez pour de futures ventes. Par exemple, des kits pour une prochaine campagne de vente. Les articles ne sont pas liés à une commande vente, du moins pas encore. En règle générale, ces éléments ne sont pas personnalisés pour les demandes des clients.        |
|Assembler pour commande     | Articles que vous ne souhaitez pas stocker. Par exemple, parce qu’ils sont personnalisés en fonction des commandes des clients ou pour réduire le coût des stocks disponibles. |
  
Cet article décrit les paramètres standard pour l’assemblage pour stock. Cependant, il existe peut-être d’autres moyens plus adaptés à votre entreprise. En savoir plus, voir [Vente d’articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) et [Vente simultanée d’articles à assembler pour commande et d’articles en stock](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Les composants d’assemblage sont gérés d’une manière spéciale dans les configurations entrepôt de base. En savoir plus sur [Traitement des articles à assembler pour commande dans les prélèvements stock](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock" />Pour assembler un article dans le stock

Suivez les étapes de cette procédure pour assembler un article à stocker. Pour en savoir plus sur l’assemblage sur commande, accédez à [Vendre des articles assemblés sur commande](assembly-how-to-sell-items-assembled-to-order.md).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Ordres d’assemblage**, puis sélectionnez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Nouvel ordre d’assemblage** s’ouvre.  
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Dans le champ **N° article**, sélectionnez l’élément à assembler. Vous pouvez sélectionner des articles configurés pour l’assemblage et dotés d’une nomenclature d’élément d’assemblage, ou des articles sans nomenclature d’élément d’assemblage. Ces derniers sont utiles pour les assemblages ou les scénarios non planifiés quand vous souhaitez utiliser la reclassification des articles et suivre les coûts.  
5. Dans le champ **Quantité**, entrez le nombre d’unités de l’article que vous souhaitez assembler.  

    > [!NOTE]  
    >  Si un ou plusieurs composants ne sont pas disponibles pour atteindre la quantité à la date d’échéance, la page **Disponibilité de l’assemblage** s’ouvre. La page indique le nombre d’éléments d’assemblage pouvant être assemblés en fonction de la disponibilité des composants. En savoir plus dans [Voir la disponibilité des articles](inventory-how-availability-overview.md). Quand vous fermez la page, l’ordre d’assemblage est créé avec des alertes de disponibilité sur les lignes des composants concernés.  

    Les lignes contiennent le contenu de la nomenclature d’élément d’assemblage et les quantités spécifiées.  

    > [!NOTE]  
    >  Si la page **Disponibilité assemblage** s’est ouverte au moment où vous avez renseigné l’en-tête d’ordre d’assemblage, chaque ligne d’ordre d’assemblage affectée contient **Oui** dans le champ **Alerte dispo.** avec un lien vers les informations de disponibilité détaillées. <!--check whether this field help is useful For more information, see Check Availability.--> Vous pouvez résoudre un problème de disponibilité de composant en :

    > * Reportez la date de début.
    > * Remplacement du composant par un autre article.
    > * Sélection d’une substitution disponible si une est définie.  

6. Dans le champ **Quantité à assembler**, entrez le nombre d’unités de l’élément d’assemblage à valider comme production la prochaine fois que vous validerez l’ordre d’assemblage. Cette quantité peut être inférieure à la valeur du champ **Quantité** pour refléter une validation partielle de production.  

    > [!NOTE]  
    >  Pour que la validation de la consommation des composants corresponde à la validation de la production d’éléments d’assemblage, les champs de quantité figurant dans les lignes d’ordre d’assemblage sont ajustées automatiquement au niveau de la valeur que vous entrez dans le champ **Quantité à assembler**.  
7. Pour les lignes d’ordre d’assemblage de type **Article** ou **Ressource**, dans le champ **Quantité à consommer**, entrez le nombre d’unités à valider en tant qu’unités consommées la prochaine fois que vous validerez l’ordre de assemblage.
8. Lorsque vous êtes entièrement ou partiellement prêt pour la validation, choisissez l’action **Valider**.  

    > [!NOTE]  
    >  Si des avertissements sont toujours présents dans des lignes ordre d’assemblage, vous ne pouvez pas valider la commande. Un message affiche le ou les composants qui ne sont pas en stock.  

Une fois la validation réussie, l’élément d’assemblage est validé comme production dans le code magasin et le code emplacement potentiel qui sont définis sur l’ordre de assemblage. Pour les ordres d’assemblage créés manuellement, le magasin peut être copié à partir du champ de configuration **Emplacement par défaut pour les commandes**. Pour les flux d’assemblage pour commande, le code magasin peut être copié à partir de la ligne commande vente.  

## <a name="see-related-microsoft-trainingtrainingpathsassemble-items-dynamics--business-central" />Voir la [formation Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Gestion des assemblages](assembly-assemble-items.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
