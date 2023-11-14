---
title: À propos du calcul des coûts standard
description: Un système de coûts standard détermine le coût unitaire du stock en fonction d’un coût historique ou prévu plausible.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
---
# À propos du calcul des coûts standard

De nombreuses sociétés manufacturières sélectionnent une base d’évaluation du coût standard. Ceci est également vrai pour les sociétés qui effectuent une fabrication légère, comme l’assemblage et le montage. Un système de coûts standard détermine le coût unitaire du stock en fonction d’un coût historique ou prévu plausible. L’analyse des données précédentes et futures en termes de coût peut alors offrir une base pour l’estimation des coûts standard. Ces coûts sont gelés tant que leur modification n’est pas décidée. Le coût réel lié à la production d’un produit peut varier par rapport aux coûts standard estimés. À des fins de contrôle de gestion, le coût réel est comparé au coût standard pour un article spécifique et les différences, ou *écarts*, sont identifiées et analysées.  

Des coûts standard peuvent être conservés pour les articles réapprovisionnés via l’achat, l’assemblage et la production. Pour chaque méthode de réapprovisionnement, les coûts standard peuvent inclure les éléments suivants.  

|Système réappro.|Éléments de coût standard|  
|--------------------------|----------------------------|  
|**Achats**|Coût matière direct et coût matière supplémentaire s’il est nécessaire.|  
|**Assembly**|Coût matière direct, coûts directs ou de main-d’œuvre fixes et frais généraux.|  
|**Ordre de fabrication**|Coût matière direct, coût de main-d’œuvre, coût de sous-traitance et frais généraux.|  

## Configuration des coûts standard

Dans la mesure où le coût standard d’un article produit ou assemblé peut comporter plusieurs éléments de coût, dont les coûts matériels, opératoires (main d’œuvre) et de sous-traitance (coûts directs et frais généraux), il convient d’établir des coûts standard pour chacun de ces éléments.  

La tâche de comptabilité pour une société de traitement d’article utilisant l’évaluation du stock standard consiste à :  

- estimer un coût standard pour l’article fini et le configurer sur la fiche article.  
- enregistrer et affecter le coût réel des éléments de coût clés et identifier les écarts.  

Pour déterminer le coût direct d’un article fini, il convient de calculer le total des coûts composants. Un article assemblé ou produit peut inclure des produits semi-finis, qui sont également composés de plusieurs éléments.  

Les éléments principaux d’un coût constituent le coût direct total d’un article fini :  

- Coûts matière.  
- Coût opératoire.  
- Les coûts de sous-traitance pour les articles produits uniquement.  

### Coûts matière

Les coûts matière sont des coûts associés aux produits semi-finis et aux matières premières achetées. Le coût unitaire matière peut se décomposer en éléments de coût directs et indirects.  

- Le coût matière direct correspond à un montant facturé pour les matières premières achetées ou le coût de traitement d’un produit semi-fini.  
- Le coût matière indirect, ou *frais généraux*, peut correspondre à des éléments tels que les coûts de transport du stock pour l’article fini, une fois que celui-ci est produit.  

La configuration du coût matière pour les articles achetés affectant les coûts directs et indirects dépend du mode d’évaluation du stock que vous avez sélectionné pour l’article concerné. Vous configurez les informations de coût pour chacun des modes d’évaluation du stock sur la fiche article. Pour plus d’informations, reportez-vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

Le coût du rebut (production uniquement) est un facteur supplémentaire à prendre en compte lors du calcul du coût matière total. La mise au rebut d’une certaine quantité de matière première lorsque vous assemblez ou produisez un article entraîne généralement une augmentation de la quantité de composants requis pour produire cet article. Cela conduit à une augmentation du coût matière des composants consommés lors de la production d’un article parent. Vous configurez le coût du rebut pour les matières dans la nomenclature de production ou la gamme.  

Le coût matière d’un article produit peut être représenté de deux façons correspondant aux bases de calcul du coût suivantes.  

|Base de calcul du coût|Calcul du coût matière|  
|----------------------------|-------------------------------|  
|Mono-niveau|L’article produit est égal au coût total de tous les articles achetés ou semi-finis dans la nomenclature de production de cet article.|  
|Calcul multi-niveau|Article produit correspond à la somme du coût matière des produits semi-finis dans la nomenclature de cet article et du coût des articles achetés dans la nomenclature de production de cet article.|  

### Coûts opératoires

Les coûts opératoires sont les coûts internes associés à la main-d’œuvre et aux machines. Vous devez configurer ces coûts pour chaque ressource (dans la gestion nomenclature d’assemblage) et centre ou poste de charge sur la gamme (dans la production). Comme pour les matières, vous pouvez identifier des éléments de coût opératoire directs et indirects. Par exemple, le coût direct pour un centre de charge peut correspondre au taux usine établi pour exécuter une fonction spécifique. Le coût indirect d’un centre de charge peut correspondre à certaines dépenses générales de l’usine, comme l’éclairage, le chauffage, etc. Comme avec les coûts matière, vous pouvez exprimer les frais généraux opératoires en pourcentage du coût indirect ou frais généraux fixes.  

La configuration des coûts opératoires des articles assemblés est constituée des éléments suivants :  

- Coût unitaire direct et indirect de la ressource.  
- Type d’utilisation fixe ou direct des ressources.  

La configuration des coûts opératoires des articles produits est constituée des éléments suivants :  

- Coût unitaire direct et indirect du poste ou du centre de charge.  
- Configuration du délai et de la taille lot  

Pour calculer le coût opératoire standard, vous devez déterminer les délais standard requis pour effectuer des opérations sur des postes de charge et des centres de charge. Le temps total nécessaire à l’exécution d’une opération comprend généralement le délai lié à la configuration, à l’exécution, ainsi que le délai d’attente et de déplacement.  

Vous configurez les taux établis pour chaque type de délai pour chaque poste de charge ou centre de charge dans une gamme individuelle.  

> [!NOTE]  
>  Si les délais d’exécution s’appliquent à chaque unité d’article produit, les délais de configuration s’appliquent pour chaque lot. Aussi, vous devez distribuer au prorata le délai de configuration de la gamme pour chaque opération par rapport à la taille lot. Vous spécifiez la taille lot dans le champ correspondant sur le raccourci **Réapprovisionnement** de la page **Fiche article**.  

Pour spécifier le délai de configuration dans la gamme à des fins de planification, sans toutefois inclure cette dépense dans le calcul des coûts standard, désactivez le champ **Inclure coût préparation** de la page **Paramètres production**.  

Sur une base mono-niveau, il s’agit du coût de main-d’œuvre requis pour produire l’article produit fini et spécifié dans la gamme de l’article produit. Sur une base multi-niveau, il s’agit du coût opératoire spécifié pour chaque article produit individuellement inclus dans la nomenclature de l’article parent.  

### Coûts de sous-traitance

Les coûts de sous-traitance sont les coûts associés aux services assurés par des sous-traitants ou fournisseurs externes d’une société. Semblables aux coûts matière et opératoires, les coûts de sous-traitance peuvent se décomposer en coûts directs et frais généraux. Le coût de sous-traitance direct correspond à la charge réelle pour chaque unité de services fournie. Par exemple, les frais de sous-traitance généraux peuvent représenter les coûts de fret et de gestion engagés par la société avec une commande sous-traitée.  

Parce que la sous-traitance correspond à une capacité externalisée, vous configurez les coûts liés à la sous-traitance de services directs et indirects dans la fiche centre de charge représentant l’opération de sous-traitance.  

## Mise à jour des coûts standard

Pour mettre à jour ou calculer le coût standard d’éléments d’assemblage, utilisez la fonction de la fiche article.  

Le processus de mise à jour ou de calcul des coûts standard comprend généralement les tâches suivantes :  

1.  Mise à jour des coûts aux niveaux des composants et de la capacité. Pour plus d’informations, consultez les traitements par lots **Proposer coût standard article** et **Suggérer le coût standard de la capacité**.  
2.  Consolidation et calcul multi-niveau des coûts des composants et de capacité pour déterminer le coût d’assemblage ou de fabrication des articles. Pour plus d’informations, consultez [Pour calculer le coût standard d’un élément d’assemblage](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Application des coûts standard entrés lorsque vous exécutez les traitements par lots précédents. Les coûts standard n’entrent en vigueur que lorsqu’ils sont mis en œuvre. Utilisez le traitement par lots **Appliquer nouv. coût standard**, qui met à jour les modifications du coût standard sur les éléments en fonction de ceux figurant dans la table Feuille coût standard.  
4.  Application des modifications pour mettre à jour le champ **Coût unitaire** sur la fiche article et effectuer une réévaluation du stock. Pour plus d’informations, voir [Réévaluer le stock](inventory-how-revalue-inventory.md).

## Utiliser des tâches par lots pour mettre à jour les coûts standard
Les sections suivantes décrivent les tâches par lots que vous pouvez utiliser pour mettre à jour les coûts standard.
### Proposer coût standard article

 Crée des propositions pour modifier les coûts et partages des coûts de coûts standard sur des fiches article. Lorsque le traitement par lots est terminé, vous pouvez en visualiser le résultat dans la fenêtre Feuille coût standard.

> [!NOTE]  
> Ce traitement par lots est prévu uniquement pour les articles achetés. Si vous souhaitez mettre à jour un article avec une nomenclature de production ou d’assemblage, vous devez d’abord renseigner la feuille avec tous les composants, avant d’exécuter le traitement par lots Déployer le coût standard.

Ce traitement par lots ne crée que des propositions. Il n’applique pas les modifications suggérées. Si les propositions vous conviennent et que vous souhaitez les appliquer, c’est-à-dire les mettre à jour dans les fiches article et les insérer dans la , cliquez sur Appliquer nouv. coût standard dans la fenêtre Feuille coût standard.
#### Options

**Coût standard** : Saisissez le facteur appliqué que vous souhaitez utiliser pour mettre le coût standard à jour. Vous pouvez également sélectionner un mode arrondi pour le nouveau coût standard. Vous devez renseigner le champ à l’aide d’une valeur décimale pour l’augmentation du pourcentage, par exemple 1,1.

**% coût indirect** : Saisissez le facteur appliqué que vous souhaitez utiliser pour mettre le % coût indirect à jour. Vous pouvez également sélectionner un mode arrondi pour le nouveau % coût indirect. Vous devez renseigner le champ à l’aide d’une valeur décimale pour l’augmentation du pourcentage, par exemple 1,1.

**Frais généraux** : Saisissez le facteur appliqué que vous souhaitez utiliser pour mettre les frais généraux à jour. Vous pouvez également sélectionner un mode arrondi pour les nouveaux frais généraux. Vous devez renseigner le champ à l’aide d’une valeur décimale pour l’augmentation du pourcentage, par exemple 1,1.

### Prop. coût std ctr./poste ch.

Crée des propositions pour modifier les coûts et partages des coûts de coûts standard sur centre de charge, poste de charge ou fiches ressource. Lorsque le traitement par lots est terminé, vous pouvez en visualiser le résultat dans la fenêtre **Feuille coût standard**.

Ce traitement par lots ne crée que des propositions. Il n’applique pas les modifications suggérées. Si les propositions vous conviennent et que vous souhaitez les appliquer, c’est-à-dire les mettre à jour dans les fiches travail/poste de charge et ressource et les insérer dans la fenêtre Feuille réévaluation, cliquez sur **Appliquer nouv. coût standard** dans la fenêtre **Feuille coût standard**.

Lorsque vous avez exécuté le traitement par lots et que vous souhaitez voir l’impact sur vos départements Production et Assemblage, vous lancez le traitement par lots **Déployer le coût standard** pour mettre à jour les coûts standard des centres de charge, postes de charge, ressources d’assemblage, nomenclatures de production et nomenclatures d’assemblage.
#### Options
**Coût standard** : Saisissez le facteur appliqué que vous souhaitez utiliser pour mettre le coût standard à jour. Vous pouvez également sélectionner un **mode arrondi** pour le nouveau coût standard. Vous devez renseigner le champ à l’aide d’une valeur décimale pour l’augmentation du pourcentage, par exemple 1,1.

**% coût indirect** : Saisissez le facteur appliqué que vous souhaitez utiliser pour mettre le % coût indirect à jour. Vous pouvez également sélectionner un mode arrondi pour le nouveau % coût indirect. Vous devez renseigner le champ à l’aide d’une valeur décimale pour l’augmentation du pourcentage, par exemple 1,1.

**Frais généraux** : Saisissez le facteur appliqué que vous souhaitez utiliser pour mettre les frais généraux à jour. Vous pouvez également sélectionner un mode arrondi pour les nouveaux frais généraux. Vous devez renseigner le champ à l’aide d’une valeur décimale pour l’augmentation du pourcentage, par exemple 1,1.

### Valider coûts ajustés

 Enregistre les changements de quantité et de valeur en stock dans les écritures comptables article et les écritures valeur lorsque vous validez des mouvements de stocks, tels que des expéditions vente ou des réceptions achat.

Sauf si vous avez coché la case **Compta. coûts automatiques** de la fenêtre **Paramètres stock**, les coûts ajustés ne sont pas enregistrés de façon dynamique dans la comptabilité. Par ailleurs, la valeur sortie stock n’est pas calculée en relation avec une vente. Par conséquent, vous devez effectuer manuellement la validation dans la comptabilité en exécutant le traitement par lots **Valider le coût de stock en comptabilité** pour mettre à jour les écritures comptables et éventuellement imprimer un état des écritures valeur validées.

Le traitement par lots utilise les entrées valeur comme base. Pour calculer la valeur à valider, il utilise la différence entre les champs **Coût total (réel)** et **Coût validé en comptabilité** dans les entrées valeur. Si vous avez coché la case **Validation du coût prévu en comptabilité** de la fenêtre **Paramètres stock**, le traitement par lots valide également la différence entre les champs **Coût total (prévu)** et **Coût prévu validé en comptabilité** sur les comptes d’attente dans la comptabilité.

> [!NOTE]
> Si vous n’avez pas coché la case **Validation du coût prévu en comptabilité** dans la fenêtre **Paramètres stock**, la dernière section de l’état répertorie les écritures valeur qui sont ignorées, car elles représentent des coûts prévus.

> [!NOTE] 
> Si le traitement par lots rencontre une erreur impliquant des dimensions ou une configuration de dimension, il ignore cette erreur et valide l’entrée en comptabilité en utilisant les dimensions de l’écriture valeur.

Pour faire en sorte que le traitement par lots ne rencontre pas d’erreur, exécutez l’état **Valider coûts ajust. - Test** pour consulter toutes les erreurs possibles. Vous pouvez ainsi corriger ces erreurs avant d’exécuter le traitement par lots **Valider coûts ajustés** qui traite alors toutes les entrées.
 
> [!IMPORTANT]  
> Avant d’utiliser ce traitement par lots, vous devez lancer le traitement par lots **Ajuster coûts : Écr. article**. Ainsi, lorsque vous lancez ce traitement par lots, les coûts validés en comptabilité sont assurément à jour.
#### Options

|Option  |Désignation  |
|--------------|---------|
|**Méthode comptabilisation**|Le traitement par lots peut valider la valeur stock en comptabilité par groupe comptabilisation ou par écriture enregistrée. Si vous validez par écriture, vous obtenez une spécification détaillée de l’influence du stock sur la comptabilité, mais vous obtenez également de nombreuses écritures. Si vous validez par groupe comptabilisation, le traitement par lots crée une écriture comptable par date comptabilisation par combinaison de groupes comptabilisation. Cela signifie qu’une écriture comptable est créée pour chaque combinaison de dates validation, groupes comptabilisation marché, groupes comptabilisation produit, groupes comptabilisation stock et codes magasin. En outre, le traitement par lots crée des écritures comptables séparées pour les coûts de signe différent.|
|**Numéro de document**|Dans ce champ, vous pouvez entrer un numéro de document si vous avez choisi l’option de validation Par groupe compta. stock. Le numéro de document est affiché sur les écritures validées.|
|**Valider**|Sélectionnez ce champ si vous souhaitez que le traitement par lots valide en comptabilité automatiquement. Si vous choisissez de ne pas valider les coûts en comptabilité, le traitement par lots n’effectuera qu’une impression test présentant les valeurs qui peuvent être validées en comptabilité et l’état indiquera : **Impression test (non validée)**.|

### Calculer coût std multi-niv.

Calcule les coûts standard des articles assemblés et fabriqués. Ceux-ci seront influencés par la modification des coûts standard des composants proposée par le traitement par lots **Proposer coût standard article**. En outre, ceux-ci seront influencés par la modification du coût standard de la capacité de production et des ressources d’assemblage proposée par le traitement par lots **Prop. coût std ctr./poste ch.**.

Lorsque vous avez exécuté l’un ou l’autre de ces traitements par lots (ou les deux) et que vous procédez à la remontée des informations, toutes les modifications des coûts standard dans la feuille sont introduites dans les nomenclatures de production ou d’assemblage associées et les coûts sont appliqués à chaque niveau de nomenclature.

> [!NOTE] 
> Cette fonction ne calcule le coût standard multi-niveau que sur les fiches article, pas sur les fiches point de stock.

Ce traitement par lots ne crée que des propositions. Il n’applique pas les modifications suggérées. Si les propositions vous conviennent et que vous souhaitez les appliquer, c’est-à-dire les mettre à jour dans les fiches article et les insérer dans la fenêtre **Feuille réévaluation**, vous pouvez utiliser le traitement par lots **Appliquer nouv. coût standard**. Vous accédez à ce traitement par lots à partir de la fenêtre **Feuille coût standard**.
#### Options

**Date de calcul** : Saisissez la date qui s’applique à la version de la nomenclature de production pour laquelle vous souhaitez faire remonter l’information.
 
### Appliquer nouv. coût standard

Mettez à jour les modifications du coût standard dans la table **Article** en fonction de celles figurant dans la table **Feuille coût standard**. Les propositions de modification des coûts standard peuvent être créées avec le traitement par lots **Proposer coût standard article** et/ou **Prop. coût std ctr./poste ch.**, et elles peuvent également être modifiées. La valeur de tous les champs de la proposition de modification de coût standard est transférée. Lorsque vous appliquez des propositions de modification des coûts standard, vous pouvez les afficher dans la fiche article et/ou dans les fiches poste/centre de charge. Une feuille de réévaluation est également créée pour vous permettre de mettre à jour la valeur du stock existant.
#### Options

**Date comptabilisation** : Saisissez la date d’entrée en vigueur de la réévaluation.

**N° document** : Saisissez le numéro des lignes feuille réévaluation. Si une série de nombres est définie sur le nom feuille article, le numéro du document sera fonction des écritures comptables effectuées par la validation de la feuille réévaluation. Sinon, vous pouvez saisir un numéro manuellement.

**Modèle feuille article** : Saisissez le nom du modèle feuille réévaluation.

**Nom feuille article** : Saisissez le nom de la feuille réévaluation réelle

Cliquez sur **OK** pour démarrer le traitement par lots. Si vous ne souhaitez pas exécuter le traitement par lots immédiatement, cliquez sur **Annuler** pour fermer la fenêtre.

## Voir aussi

[Détails de conception : méthodes de calcul des coûts](design-details-costing-methods.md)  
[Mise à jour des coûts standard](finance-how-to-update-standard-costs.md)  
[Détails de conception : Évaluation stock](design-details-inventory-costing.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Créer des nomenclatures de production](production-how-to-create-production-boms.md)  
[Utiliser les nomenclatures](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
