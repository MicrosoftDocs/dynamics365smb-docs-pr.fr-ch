---
title: 'Inventaire, ajustement et reclassement du stock'
description: Découvrez comment effectuer un comptage physique et faire des ajustements et des reclassements.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Comptabiliser, ajuster et reclasser le stock avec les feuilles

Comptez physiquement tous les articles en stock pour vous assurer que vos quantités sont correctes. Certaines entreprises effectuent un inventaire physique annuel, tandis que d’autres comptent plus souvent tous les articles ou seulement certains d’entre eux. Après avoir compté les articles, utilisez les feuilles pour valider les quantités réelles dans la comptabilité. Par exemple, lorsque vous évaluez le stock à la fin d’une période.

Pour compter certains articles plus souvent que d’autres, peut-être en raison de leur valeur, utilisez des inventaires tournants. Pour les inventaires tournants, attribuez des périodes d’inventaire spéciales aux articles. Learn more at [Pour effectuer un inventaire tournant](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Pour ajuster les quantités après un comptage physique ou à d’autres fins, utilisez une feuille article pour modifier les écritures comptables de stock sans valider les transactions. Vous pouvez également ajuster la quantité d’un seul article sur une fiche article.

Pour modifier les attributs des écritures comptables article, vous pouvez utiliser une feuille reclassement article. Les attributs typiques à reclasser incluent les dimensions et les codes de campagne de vente. Les feuilles reclassement peuvent également être utilisées pour les transferts en reclassant les codes d’emplacement et de magasin. Des étapes spéciales s’appliquent lorsque vous souhaitez reclasser les numéros de série ou de lot et leurs dates d’expiration. Pour plus d’informations, voir [Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md).

> [!NOTE]
> Dans les processus à plusieurs étapes, les articles sont enregistrés dans des emplacements en tant qu’écritures entrepôt, pas en tant qu’écritures comptables article. Par conséquent, vous effectuez l’inventaire, l’ajustement et le reclassement dans des feuilles entrepôt spéciales qui prennent en charge les emplacements. Ensuite, vous utilisez synchronisez les écritures entrepôt nouvelles ou modifiées avec leurs écritures comptables article correspondantes pour refléter les modifications des quantités et valeurs en stock.

## <a name="to-count-physical-inventory"></a>Pour effectuer un inventaire

Faites l’inventaire, c’est-à-dire comptez les articles réellement disponibles, pour vérifier si la quantité enregistrée est la même que la quantité physique en stock. En règle générale, ces comptages ont lieu à la fin d’un exercice financier, mais parfois, ils sont effectués plus souvent. S’il y a des écarts, validez les quantités réelles dans les comptes d’articles <!--accounts, or ledger?--> avant de procéder à l’évaluation du stock.

> [!NOTE]
> Cette procédure explique comment effectuer un inventaire à l’aide d’une feuille sur la page **Feuille inventaire**. Vous pouvez utiliser des documents sur les pages **Ordre d’inventaire** et **Enregistrement d’inventaire**. Ces documents offrent plus de contrôle et prennent en charge la répartition du travail de comptage entre plusieurs employés. Learn more at [Faire l’inventaire à l’aide de documents](inventory-how-count-inventory-with-documents.md).<br /><br />
> Vous remarquerez que vous ne pouvez pas utiliser la fonctionnalité basée sur un document pour comptabiliser les articles dans les emplacements ou les écritures entrepôt.

Le processus de comptage implique également les tâches suivantes :

- Calculer le stock prévu.
- Imprimer l’état à utiliser lors du comptage.
- Saisir et valider les quantités réelles.

En fonction de votre configuration entrepôt, vous pouvez effectuer l’inventaire de l’une des manières suivantes. Pour plus d’informations, voir [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

- Si votre magasin n’utilise pas le rangement et le prélèvement dirigés, utilisez la page **Feuille inventaire**. La procédure est similaire à l’inventaire physique sans inventaire tournant.  
- Si votre magasin utilise le rangement et le prélèvement dirigés, utilisez la page **Feuille inventaire entrepôt**. Utilisez ensuite la page **Feuilles article** pour exécuter l’action **Calculer ajustement entrepôt**. <!--We should say what to do on each of these pages.-->

### <a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a>Pour calculer le stock prévu dans les configurations d’entrepôt de base

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles inventaire**, puis choisissez le lien associé.
2. Choisissez l’action **Calculer stock**.
3. Sur la page **Calculer stock**, indiquez les conditions à utiliser pour créer les lignes feuille, par exemple si vous souhaitez inclure les articles pour lesquels aucun stock n’est enregistré.
4. Définissez des filtres si vous souhaitez uniquement calculer le stock pour certains articles, emplacements, magasins ou axes.
5. Cliquez sur le bouton **OK**.

> [!NOTE]  
> Les écritures article sont traitées en fonction des informations que vous avez indiquées, et les lignes sont créées dans la feuille inventaire. Notez que le champ **Qté (constatée)** contient la même quantité que le champ **Qté (calculée)**. Vous n’avez pas besoin d’entrer la quantité comptée pour les articles où ces valeurs correspondent. Cependant, si la quantité comptée diffère, entrez la quantité qui a été comptée.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Pour imprimer l’état à utiliser lors de l’inventaire

1. Sur la page **Feuille inventaire** contenant le stock prévu calculé, choisissez l’action **Imprimer**.
2. Sur la page **Liste d’inventaire entrepôt**, indiquez si l’état doit indiquer la quantité calculée et les articles en stock par numéros de série et de lot.
3. Définissez des filtres si vous souhaitez uniquement imprimer l’état pour certains articles, emplacements, magasins ou axes.
4. Sélectionnez **Imprimer**.

Les magasiniers peuvent maintenant procéder au comptage du stock et noter les éventuelles différences sur l’état imprimé.

> [!NOTE]
> Plusieurs jours peuvent s’écouler avant que les rapports imprimés reviennent pour traitement final et publication. Lorsque vous spécifiez et validez l’inventaire compté réel, le système ajuste l’inventaire pour refléter la différence entre l’inventaire compté attendu et réel. Vous devez conserver les lignes de journal initialement calculées et ne pas recalculer l’inventaire attendu, car l’inventaire attendu peut changer et entraîner des niveaux de stock incorrects. Si vous devez émettre plusieurs rapports, par exemple pour différents emplacements ou groupes d’éléments, vous devez créer et conserver des lots de journaux distincts.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Pour saisir et valider le stock réel compté dans les configurations d’entrepôt de base

1. Sur chaque ligne de la page **Feuilles inventaire** sur laquelle le stock réellement disponible, comme déterminé par le comptage, diffère de la quantité calculée, saisissez la quantité réellement disponible dans le champ **Qté (constatée)**.
  
  > [!NOTE]  
  > Si le décompte fait apparaître des différences dues à des articles validés avec des magasins incorrects, ne saisissez pas les différences dans la feuille inventaire. Au lieu de cela, utilisez une feuille reclassement ou un ordre de transfert pour rediriger les articles vers les magasins appropriés. 

2. Pour ajuster les quantités calculées avec les quantités comptées réelles, choisissez **Valider**.

    La validation crée les écritures comptables article et les écritures comptables inventaire. Ouvrez la page Fiche article de l’article pour rechercher ses écritures comptables inventaire. <!--Where are they shown on an item?-->

3. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis choisissez le lien associé.
4. Pour vérifier le comptage, ouvrez la fiche article de l’article concerné, puis choisissez l’action **Écritures comptables inventaire**. <!--I don't see this action -->

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Pour calculer le stock prévu dans les configurations d’entrepôt avancées

Synchronisez le registre des articles et l’entrepôt <!--warehouse what?--> avant de compter l’inventaire physique. Sinon, ce que vous validez dans la feuille inventaire et le registre des articles sera le résultat de l’inventaire physique combiné à d’autres ajustements d’entrepôt pour les articles. Learn more at [Synchroniser les quantités dans les écritures article et entrepôt](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille inventaire entrepôt**, puis choisissez le lien associé.  
2. Choisissez l’action **Calculer stock** pour ouvrir la page **Calculer stock entrepôt**.  
3. Définissez les filtres pour spécifier les articles à compter dans la feuille, puis choisissez **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] crée une ligne pour chaque emplacement répondant aux exigences des filtres. Vous pouvez supprimer des lignes, mais si vous souhaitez valider les résultats en tant qu’inventaire, comptez l’article dans tous les emplacements le contenant.  

   Si vous ne comptez qu’un article dans certains emplacements mais pas dans d’autres, vous pouvez saisir les différences et les valider ultérieurement dans la feuille article en utilisant l’action **Calculer ajustement entrepôt**. <!--I don't see this action-->  

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Pour saisir et valider le stock réel compté dans les configurations d’entrepôt avancées

1. Sur la page **Feuille inventaire entrepôt**, saisissez les quantités réelles dans le champ **Qté (constatée)**.  

    > [!NOTE]  
    >  Le champ **Qté (Calculée)** est rempli en fonction des enregistrements d’emplacement. Cette quantité est copiée dans le champ **Qté (Physique)** sur chaque ligne. Si les quantités dans ces champs ne correspondent pas, entrez la quantité réelle.  

2. Après avoir saisi toutes les quantités réelles, choisissez l’action **Enregistrer**.  

    Lorsque vous enregistrez la feuille, [!INCLUDE [prod_short](includes/prod_short.md)] crée dans l’historique entrepôt deux écritures entrepôt pour chaque ligne comptée et enregistrée :  

    - Si les quantités calculées et les quantités réelles sont différentes, une quantité négative ou positive est enregistrée pour l’emplacement, et la quantité d’équilibre est validée dans l’emplacement d’ajustement du magasin.  
    - Si la quantité calculée est égale à la quantité physique, [!INCLUDE [prod_short](includes/prod_short.md)] enregistre **0** à la fois pour l’emplacement et l’emplacement d’ajustement. 

Lorsque vous enregistrez un inventaire physique, vous ne le validez pas dans les registres article, inventaire ou valeur. Cependant, les enregistrements sont disponibles pour le rapprochement en cas de besoin. Pour que les quantités restent exactes, après avoir compté les articles dans tous les emplacements, validez les résultats en tant qu’inventaire physique <!--physical inventory journal-->. Learn more at [Synchroniser les quantités dans les écritures article et entrepôt](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## <a name="to-do-cycle-counting"></a>Pour effectuer un inventaire tournant

Vous pouvez compter les articles aussi souvent que vous le souhaitez. Par exemple, parce qu’ils ont plus de valeur ou parce qu’ils bougent rapidement et représentent une grande partie de votre activité. Spécifiez la fréquence de comptage en attribuant des périodes de comptage spéciales aux articles.

En fonction de votre configuration entrepôt, vous pouvez effectuer un inventaire tournant de l’une des manières suivantes. Learn more at [Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md).  

- Si votre magasin n’utilise pas le rangement et le prélèvement dirigés, utilisez la page **Feuille inventaire**. La procédure est similaire au comptage de l’inventaire physique sans inventaire tournant.  
- Si votre magasin utilise le rangement et le prélèvement dirigés, utilisez la page **Feuille inventaire entrepôt**. Utilisez ensuite la page **Feuilles article** pour exécuter l’action **Calculer ajustement entrepôt**. <!--we should say what to do on each of these pages-->  

### <a name="to-set-up-counting-periods"></a>Pour configurer des périodes d’inventaire

Le comptage d’inventaire est généralement une tâche récurrent, par exemple, tous les mois, tous les trimestres ou tous les ans. Vous pouvez configurer les périodes d’inventaire nécessaires et les affecter à chaque article. Ensuite, utilisez l’action **Calculer la période d’inventaire** sur la page **Feuille inventaire** pour créer automatiquement des lignes pour les articles.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Périodes inventaire**, puis choisissez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Pour affecter une période d’inventaire à un article

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Sélectionnez l’article auquel vous souhaitez affecter une période d’inventaire.  
3. Dans le champ **Code période inventaire stock**, sélectionnez la période d’inventaire.  

> [!NOTE]
> Si vous modifiez la période d’inventaire, un message affiche des informations sur les résultats de la modification. Sélectionnez **Oui** pour modifier le code et calculer la première période d’inventaire de l’article. La prochaine fois que vous choisissez de calculer une période d’inventaire dans la feuille inventaire, l’article s’affichera en tant que ligne sur la page **Sélection article inventaire**. Vous pouvez ensuite compter l’article périodiquement.

### <a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Pour lancer un comptage selon des périodes d’inventaire dans les configurations d’entrepôt de base

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille inventaire**, puis choisissez le lien associé.
2. Choisissez l’action **Calculer la période d’inventaire**.

    La page **Sélection article inventaire** affiche les articles qui doivent être comptés en fonction de leurs périodes de comptage.
3. Comptez l’inventaire physique. Learn more at [Pour effectuer un inventaire](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### <a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Pour lancer un comptage selon des périodes d’inventaire dans les configurations d’entrepôt avancées

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille inventaire entrepôt**, puis choisissez le lien associé.  
2. Choisissez l’action **Calculer la période d’inventaire**.

    La page **Sélection article inventaire** affiche les articles qui doivent être comptés en fonction de leurs périodes de comptage.
3. Comptez l’inventaire physique. Learn more at [Pour effectuer un inventaire](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Comptez l’article dans tous les emplacements qui le contiennent. Si vous supprimez des lignes emplacement qui ont été récupérées pour le comptage sur la page **Inventaire entrepôt**, le comptage sera incorrect lorsque vous le validerez dans une feuille inventaire.  

## <a name="to-adjust-the-quantity-of-one-item"></a>Pour ajuster la quantité d’un article

Après avoir effectué l’inventaire d’un article, utilisez l’action **Ajuster l’inventaire** pour enregistrer la quantité d’inventaire réelle.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article pour lequel vous souhaitez ajuster le stock, puis sélectionnez l’action **Ajuster stock**.
3. Dans le champ **Nouvel inventaire** du magasin, saisissez le résultat du comptage.
4. Cliquez sur le bouton **OK**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Vous pouvez également utiliser l’action **Ajuster stock** comme un moyen simple d’ajouter des articles achetés dans le stock si vous n’utilisez pas des factures achat ou des commandes pour enregistrer vos achats. En savoir plus sur [Enregistrer les achats](purchasing-how-record-purchases.md).

> [!NOTE]  
> Après avoir ajusté l’inventaire, mettez à jour sa valeur actuelle. Pour plus d’informations, voir [Réévaluer le stock](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a>Pour ajuster les quantités de plusieurs articles dans les configurations d’entrepôt de base

Sur la page **feuille article**, vous pouvez valider les transactions article directement pour ajuster le stock en fonction des achats, des ventes et des changements positifs et négatifs sans utiliser de documents.

Si vous utilisez fréquemment la feuille article pour comptabiliser des lignes feuille identiques ou analogues (par exemple, pour la consommation de matériel), la page **Feuille article standard** peut simplifier cette tâche récurrente. Pour plus d’informations, voir [Utiliser des feuilles standard](ui-work-general-journals.md#work-with-standard-journals).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuilles article**, puis choisissez le lien associé.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Choisissez l’action **Valider** pour ajuster les quantités.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Pour ajuster les quantités de l’emplacement dans les configurations d’entrepôt avancées

Si votre magasin utilise le rangement et le prélèvement dirigés, utilisez la page **Feuille article entrepôt** pour valider les modifications de quantité positives et négatives non planifiées. Par exemple, pour les articles signalés comme manquants qui apparaissent de manière inattendue, ou les pertes dues à la casse.  

Les feuilles article entrepôt vous offrent plus de niveaux d’ajustement pour rendre vos quantités plus précises. L’entrepôt sait combien d’articles sont disponibles et où ils sont stockés, mais chaque ajustement n’est pas validé dans le registre des articles. Des crédits ou des débits sont créés pour l’emplacement réel avec l’ajustement de la quantité. Une écriture d’équilibrage est effectuée dans un emplacement d’ajustement. L’emplacement d’ajustement est un emplacement virtuel sans articles réels. Vous spécifiez l’emplacement virtuel dans le champ **Code emplacement ajustement stock** sur les pages **Fiche magasin**.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille article entrepôt**, puis choisissez le lien associé.  
2. Renseignez les informations d’en-tête.  
3. Dans le champ **N° d’article** sur la ligne, choisissez l’article.  
4. Saisissez l’emplacement dans lequel vous placez les articles supplémentaires ou dans lequel des articles sont manquants.  
5. Dans le champ **Quantité**, si vous avez trouvé des articles supplémentaires, entrez une quantité positive. Si des articles sont manquants, saisissez une quantité négative.  
6. Sélectionnez l’action **Enregistrer**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Pour synchroniser les écritures entrepôt ajustées avec les écritures comptables article associées

Validez les enregistrements d’emplacement d’ajustement dans le registre des articles pour les périodes que vous avez définies. Certaines entreprises valident des ajustements quotidiens dans le registre des articles, tandis que d’autres effectuent le rapprochement moins souvent.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille article**, puis choisissez le lien associé.  
2. Renseignez les champs de chaque ligne feuille.  
3. Choisissez l’action **Calculer ajustement entrepôt**, puis ajoutez des filtres sur la page **Calculer ajustement entrepôt**. Les ajustements sont calculés uniquement pour les écritures de l’emplacement ajustement qui répondent aux exigences des filtres.  
4. Sur le raccourci **Options**, entrez manuellement un numéro dans le champ **N° document**. Étant donné qu’aucune souche de numéros n’a été configurée pour ce traitement par lots, utilisez le modèle de numéros configuré par l’entrepôt ou saisissez la date suivie de vos initiales.  
5. Cliquez sur **OK**. Les ajustements positifs et négatifs sont totalisés pour chaque article et des lignes sont créées dans la feuille article.  
6. Validez des lignes feuille pour entrer les différences de quantité dans la feuille article. Les inventaires dans les emplacements et le registre des articles correspondent maintenant.  

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/adjust-inventory/) associée

## <a name="see-also"></a>Voir aussi

[Faire l’inventaire à l’aide de documents](inventory-how-count-inventory-with-documents.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)  
[Ventes](sales-manage-sales.md)  
[Procédure d’achat](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
