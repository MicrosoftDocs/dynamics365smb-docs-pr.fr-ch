---
title: Détails de conception - Modification des modes évaluation stock pour les articles
description: Découvrez comment attribuer un mode évaluation stock différent à un article bien que vous l’ayez déjà utilisé dans des transactions.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'costing methods, costing, item cost'
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
---

# <a name="design-details-change-the-costing-method-for-items"></a><a name="design-details-change-the-costing-method-for-items"></a>Détails de conception : Modifier le mode évaluation stock pour les articles

Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous ne pouvez pas modifier un mode évaluation stock pour un article après avoir inclus l’article dans une transaction. Par exemple, après avoir acheté ou vendu l’article. Si un mode évaluation stock incorrect a été affecté à l’article ou aux articles, vous ne découvrirez peut-être pas le problème tant que vous n’aurez pas effectué votre génération d’états financiers.

Cette rubrique décrit comment résoudre cette situation. L’approche recommandée consiste à remplacer l’article dont le mode évaluation stock est incorrect par un nouvel article et à utiliser un ordre d’assemblage pour transférer l’inventaire de l’ancien article vers le nouveau.

> [!NOTE]
> L’utilisation des ordres d’assemblage permet aux coûts de continuer à circuler, bien qu’il y ait des factures achat ou des frais d’expédition à payer. De plus, cela vous permet d’annuler la conversion et de récupérer les quantités des articles d’origine, si nécessaire.

> [!TIP]
> Pour vous familiariser avec le processus, nous vous recommandons de démarrer le processus de conversion avec un seul article ou un petit ensemble d’articles.

## <a name="about-costing-methods"></a><a name="about-costing-methods"></a>À propos des modes évaluation stock

Les modes évaluation stock contrôlent les calculs de coûts lorsque les produits sont achetés, reçus en stock et vendus. Les modes évaluation stock affectent le calendrier des montants enregistrés dans les Valeurs sortie stock qui affectent le bénéfice brut. C’est ce flux qui calcule les Valeurs sortie stock. Les Valeurs sortie stock (COGS) et les revenus sont utilisés pour déterminer le bénéfice brut, comme suit :

*bénéfice brut* = *revenus - COGS*

Lorsque vous configurez des articles de stock, vous devez affecter un mode évaluation stock. Le mode peut varier d’une entreprise à l’autre et d’un article à l’autre, il est donc important de choisir le bon. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les modes évaluation stock suivants :

* Moyenne
* FIFO
* LIFO
* Standard
* Spécifique

Pour plus d’informations, [Détails de conception : modes évaluation stock](design-details-costing-methods.md).

## <a name="use-assembly-orders-to-change-costing-method-assignments"></a><a name="use-assembly-orders-to-change-costing-method-assignments"></a>Utiliser des ordres d’assemblage pour modifier les affectations de mode évaluation stock

Cette section décrit les étapes suivantes pour modifier le mode évaluation stock affecté à un article :

1. Définir un mode évaluation stock par défaut.
2. Identifier les articles pour lesquels modifier le mode évaluation stock et les renuméroter.
3. Créer de nouveaux articles avec l’ancien schéma de numérotation et copier les données de base dans un lot.
4. Copier manuellement les données de base associées de l’article existant vers le nouvel article.
5. Déterminer la quantité en stock à convertir de l’article d’origine vers le nouvel article.
6. Transférer le stock vers le nouvel article.
7. Gérer les quantités de stock allouées à la demande.
8. Bloquer l’article d’origine de toute utilisation ultérieure.  

### <a name="define-a-default-costing-method"></a><a name="define-a-default-costing-method"></a>Définir un mode évaluation stock

Pour éviter de futures erreurs, vous pouvez spécifier un mode évaluation stock par défaut pour les nouveaux articles. Chaque fois que quelqu’un crée un nouvel article, [!INCLUDE[prod_short](includes/prod_short.md)] suggérera le mode évaluation stock par défaut. Vous spécifiez le mode par défaut dans le champ **Mode évaluation stock par défaut** sur la page **Paramètres stock**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a><a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Identifier les articles pour lesquels modifier le mode évaluation stock et les renuméroter

Vous voudrez peut-être donner à vos nouveaux articles les mêmes numéros que ceux qu’ils remplacent. Pour ce faire, modifiez les numéros des articles existants. Par exemple, si le numéro d’article existant est « P1000 », vous pouvez le remplacer par « X-P1000 ». Il s’agit d’une modification manuelle que vous devez effectuer pour chaque article.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a><a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Créer de nouveaux articles avec l’ancien schéma de numérotation et copier les données de base dans un lot

Créez les nouveaux articles à l’aide du schéma de numéros actuel. À l’exception du champ **Mode évaluation stock**, les nouveaux articles doivent contenir les mêmes données de base que les articles existants. Pour transférer les données de base de l’article et les données associées d’autres fonctionnalités, utilisez l’action **Copier article** sur la page **Fiche article**. Pour plus d’informations, voir [Copier des articles existants pour créer de nouveaux articles](inventory-how-copy-items.md).

Après avoir créé les nouveaux articles et transféré les données de base, affectez le mode évaluation stock correct.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a><a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Copier manuellement les données de base associées de l’article existant vers le nouvel article

Pour que les nouveaux articles soient pleinement utiles, vous devez copier manuellement certaines données de base à partir d’autres zones, comme décrit dans la table suivante.

|Région  |Que copier  |Comment le copier  |
|---------|---------|---------|
|Stock |Unités de stockage (points de stock) |Vérifiez si un point de stock est spécifié pour l’article d’origine. Si des paramètres de planning ont été saisis pour chaque fiche de point de stock, vous devez créer manuellement le point de stock pour le nouvel article. Si les paramètres ne sont pas spécifiés, vous pouvez utiliser le traitement par lots **Créer point de stock** à partir de la page **Fiche article** pour créer les données.|
| |Articles de substitution |Vérifiez si des articles de substitution sont définis pour l’article d’origine. S’il y en a, transférez ces données vers le nouvel article. Pour afficher les articles de substitution, utilisez l’action **Substitutions** sur la page **Fiche article**. |
| |Rapports d’analyse |Consultez les rapports d’analyse des articles, d’analyse des ventes et d’analyse des achats. Pour ceux qui font référence aux articles d’origine, vous pouvez soit créer un nouveau rapport d’analyse avec une référence au nouvel article (en conservant le rapport d’analyse d’origine à utiliser comme historique), soit ajuster les rapports afin qu’ils référencent le nouvel article. |
| |Feuilles standard |Vérifiez si les feuilles standard font référence à l’article d’origine et transférez ces données vers le nouvel article si nécessaire. Ces informations se trouvent dans les feuilles standard, qui sont disponibles dans la feuille article.  |
|Ventes |Pourcentage acompte vente | Vérifiez si des pourcentages acompte vente sont définis pour l’article d’origine et transférez ces données vers le nouvel article. Pour afficher les pourcentages acompte, sur la page **Fiche article**, choisissez **Ventes**, puis **Pourcentages acompte**.|
|Achats |Pourcentage acompte achat |Vérifiez si des pourcentages acompte achat sont définis pour l’article d’origine et transférez ces données vers le nouvel article. Pour afficher les pourcentages acompte, sur la page **Fiche article**, choisissez **Achats**, puis **Pourcentages acompte**. |
|Entrepôt |Contenu emplacement |Vérifiez le contenu d’emplacement défini pour l’article d’origine. Si des colonnes telles que Qté min., Qté max., Par défaut et Dédié ont été saisies individuellement, vous devez créer manuellement le contenu d’emplacement pour le nouvel article. Si ce n’est pas le cas, aucune action n’est requise. [!INCLUDE[prod_short](includes/prod_short.md)] conservera les enregistrements lorsque vous enregistrerez les documents et les journaux de l’entrepôt.|
|Projet |Prix projet |Vérifiez si des prix projet sont définis pour l’article d’origine et transférez ces données vers le nouvel article. Ces informations sont disponibles sur la page **Fiche projet** dans la partie **Détails projet - Nbre prix** sur le **volet Récapitulatif**. |
|Service |Compétence ressource de service |Vérifiez si des compétences ressource de service sont définies pour l’article d’origine et transférez ces données vers le nouvel article. Pour afficher les compétences ressource, utilisez l’action **Compétences ressource** sur la page **Fiche article**.  |
| |Composants article de service |Vérifiez si des composants sont définis pour l’article de service d’origine et transférez ces données vers le nouvel article. Pour afficher les composants article de service, sur la page **Fiche article**, utilisez l’action **Article de service** pour ouvrir la liste des articles de service associés, puis choisissez l’action **Composants**.  |
|Fabrication |Nomenclatures de production |Vérifiez si les nomenclatures production contiennent l’article d’origine et remplacez-le par le nouvel article. Pour remplacer l’article d’origine, sur la page **Nomenclatures production**, choisissez l’action **Remplacer article nomenclature production**. |
|Assemblage |Nomenclatures d’élément d’assemblage |Vérifiez si les nomenclatures d’élément d’assemblage contiennent l’article d’origine et remplacez-le manuellement par le nouvel article. |

> [!IMPORTANT]
> Si le nouveau mode évaluation stock est Standard, vous devez saisir une valeur dans le champ **Coût standard** sur la page **Fiche article**. Vous pouvez utiliser la page **Feuille coût standard** pour définir les coûts totaux en conséquence. Pour plus d’informations, voir [Mise à jour des coûts standard](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a><a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Déterminer la quantité en stock à convertir de l’article d’origine vers le nouvel article

> [!NOTE]
> Cette étape ne prend pas en compte les quantités incluses dans les commandes non expédiées. Pour plus d’informations, voir [Gérer les quantités de stock allouées à la demande](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Utilisez un journal d’inventaire pour produire une liste des quantités en stock. Selon la configuration de l’emplacement de l’entrepôt, utilisez l’une des options suivantes :

* Feuilles d’inventaire
* Feuilles d’inventaire entrepôt

Les deux journaux peuvent calculer la quantité en stock de l’article, y compris l’emplacement, la variante, et l’emplacement de stockage. Pour plus d’informations, voir [Inventaire, ajustement et reclassement du stock avec les journaux](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a><a name="transfer-the-inventory-to-the-new-item"></a>Transférer le stock vers le nouvel article

Créez et validez des ordres d’assemblage pour transférer le coût et la quantité de stock de l’article d’origine vers le nouvel article. Les ordres d’assemblage peuvent convertir un article en un autre tout en préservant les coûts. Cela permet de garantir que les totaux nets du compte de stock et de la COGS ne sont pas affectés (sauf lorsque le nouveau mode évaluation stock est Standard, auquel cas les coûts peuvent être répartis dans les comptes d’écart). Pour plus d’informations, voir [Gestion des assemblages](assembly-assemble-items.md).

Lorsque vous créez des ordres d’assemblage, utilisez les informations des Feuilles d’inventaire ou des Feuilles d’inventaire entrepôt. Les tables suivantes décrivent les informations des rapports à saisir dans l’en-tête et les lignes de l’ordre d’assemblage.

#### <a name="header"></a><a name="header"></a>En-tête

|Champ  |Valeur à saisir  |
|---------|---------|
|N° article |Le numéro du nouvel article. |
|Quantité |La quantité dans la feuille inventaire.<br> **REMARQUE :** les quantités calculées par les feuilles inventaire n’incluent pas les quantités qui se trouvent sur des commandes qui n’ont pas encore été expédiées.  |
|Code variante |Idem à la feuille inventaire.  |
|Code magasin |Idem à la feuille inventaire. |
|Code unité |Idem à la feuille inventaire. |
|Code emplacement |Idem à la feuille inventaire. |

#### <a name="lines"></a><a name="lines"></a>Lignes

|Champ  |Valeur à saisir  |
|---------|---------|
|Type |Article ; |
|Non. |Le numéro de l’article d’origine. |
|Quantité par |1 |
|Code variante |Idem à la feuille inventaire. |
|Code magasin |Idem à la feuille inventaire. |
|Code unité |Idem à la feuille inventaire. |

> [!NOTE]
> Un ordre d’assemblage ne peut gérer qu’un seul point de stock d’un article à la fois. Vous devez créer un ordre d’assemblage pour chaque combinaison de point de stock ayant une quantité en stock.

> [!NOTE]
> Pour un emplacement d’entrepôt, vous devrez peut-être créer des prélèvements avant de pouvoir valider l’ordre d’assemblage. Pour étudier cela, passez en revue la configuration pour le prélèvement sur la page **Fiche magasin**. Pour plus d’informations, voir [Procédure : configurer des articles et des emplacements pour prélèvement et rangement suggérés](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a><a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Gérer les quantités de stock allouées à la demande

Idéalement, l’inventaire de l’article d’origine devrait être remis à zéro après le transfert des quantités en stock. Cependant, il peut y avoir des commandes, des feuilles de calcul et des journaux en attente (voir la table ci-dessous) qui nécessitent toujours une quantité de l’article d’origine. La quantité peut également être bloquée par une réservation ou une traçabilité.

**Exemple** Il y a 1 000 pièces en stocke et 20 pièces sont réservées pour une commande vente non encore livrée. Dans ce cas, vous pourriez décider de conserver les 20 pièces dans l’ancien article afin que vous puissiez exécuter la commande en cours.

> [!NOTE]
> Il existe des domaines fonctionnels qui peuvent affecter la quantité, comme indiqué dans la table ci-dessous, il peut donc être difficile de trouver le montant correct. Pour être sûr, en utilisant l’exemple ci-dessus, vous pouvez choisir de conserver 100 pièces et de transférer les 900 pièces restantes à la place. Une autre façon de procéder serait de traiter les documents et les journaux de manière à n’en conserver que quelques-unes. Une autre alternative consiste à transférer la totalité de la quantité vers le nouvel article, puis à en transférer une partie vers l’article d’origine à l’aide de l’ordre d’assemblage.

La table suivante répertorie les domaines fonctionnels où il peut y avoir des quantités en suspens.

|Région  |Où chercher des quantités en suspens  |
|---------|---------|
|Ventes |Documents de vente, y compris commandes, retours, factures, devis, commandes cadre et avoirs |
|Stock |Feuilles article, réservations, traçabilité et feuille coût standard |
|Achats |Documents achat, y compris commandes, retours, factures, devis, commandes cadre et avoirs |
|Planning |Demande achat, feuille planning et planification commande |
|Entrepôt |Ordres transfert, expéditions en entrepôt, feuilles entrepôt, prélèvements, rangements et mouvements entrepôt, prélèvements et rangements internes, et feuilles création emplacement |
|Assemblage |Documents d’assemblage, y compris les commandes, les retours et les commandes cadre |
|Projets |Lignes planning projet et lignes feuille projet |
|Service |Documents de service et contrats de service |
|Fabrication |Ordres de fabrication (planifiés, et planifiés fermes et lancés) |

### <a name="block-the-original-item-from-further-use"></a><a name="block-the-original-item-from-further-use"></a>Bloquer l’article d’origine de toute utilisation ultérieure

Lorsque le stock de l’article d’origine est nul, vous pouvez bloquer l’article pour éviter qu’il ne soit utilisé dans de nouvelles transactions. Pour bloquer l’article, sur la page **Fiche objet**, activez le bouton bascule **Bloqué**. Pour plus d’informations, voir [Bloquer les articles des ventes ou des achats](inventory-how-block-items.md).

## <a name="summary"></a><a name="summary"></a>Résumé

La modification du mode évaluation stock des articles qui ont été utilisés dans des transactions est un traitement et non une action standard dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez utiliser les étapes décrites dans cette rubrique comme modèle pour le traitement.

Le traitement peut prendre du temps car il existe plusieurs étapes manuelles. Cependant, en prenant le temps de le terminer, vous minimiserez l’impact des erreurs sur votre comptabilité.

Nous recommandons ce qui suit :

1. Évaluez la faisabilité du traitement en prenant un ou peut-être quelques articles représentatifs tout au long du traitement.
2. Envisagez de contacter un partenaire expérimenté qui puisse vous aider dans le traitement.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Détails de conception : modes évaluation stock](design-details-costing-methods.md)  
[Aperçu](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
