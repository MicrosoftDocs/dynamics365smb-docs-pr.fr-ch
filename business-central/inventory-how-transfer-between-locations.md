---
title: Transfert d’articles entre des magasins entrepôt
description: Découvrez comment déplacer un stock d’un lieu ou d’un entrepôt à un autre soit avec la feuille reclassement soit à l’aide des ordres de transfert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# <a name="transfer-inventory-between-locations"></a>Transfert de stock entre des magasins

Vous pouvez transférer des articles en stock entre des magasins en créant des ordres de transfert. Vous pouvez également utiliser la feuille reclassement article.

> [!NOTE]
> Pour transférer des articles, vous devez configurer des magasins et des acheminements transfert. Pour en savoir plus sur la configuration des magasins, consultez [Configurer des magasins](inventory-how-setup-locations.md). Vous ne pouvez pas utiliser d’ordres de transfert pour des magasins *vides*.

## <a name="transfer-orders"></a>Ordres de transfert

Vous pouvez expédier un transfert sortant à partir d’un magasin et recevoir un transfert entrant à destination. Vous pouvez :

* Suivre une quantité en transit
* Définissez les calendriers, les routages et les heures de traitement entrant et sortant pour le calcul et la planification des dates. Pour en savoir plus sur la planification, consultez [À propos de la fonctionnalité de planification](production-about-planning-functionality.md).
* Utilisez différentes fonctionnalités d’entrepôt pour les magasins entrants et sortants.
* Avec certaines limitations, vous pouvez utiliser des ordres de transfert pour les transferts directs.

## <a name="item-reclassification-journals"></a>Feuilles reclassement article

* Transfert simple et direct d’articles entre magasins.
* Déplacez les articles entre emplacements. Pour en savoir plus sur le transfert d’articles entre emplacements, consultez [Déplacer des articles non planifiés dans les configurations de stockage de base](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Remplacez un numéro de lot ou de série par un nouveau numéro de lot ou de série. Pour en savoir plus sur le reclassement des numéros de série et de lot, consultez [Reclasser les numéros de série ou de lot](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Remplacez la date d’expiration par une nouvelle date.
* Reclasser les articles d’un magasin *vide* vers un magasin réel.
* Les activités d’entrepôt ne sont pas gérées. Des écritures entrepôt seront créées.

## <a name="to-transfer-items-with-a-transfer-order"></a>Pour transférer des articles avec un ordre de transfert

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ordres de transfert**, puis sélectionnez le lien associé.
2. Sur la page **Ordre de transfer**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Si vous avez renseigné les champs **Code transit**, **Code transporteur**, et **Code prestation transporteur** sur la page **Spéc. acheminement transfert** lors de la configuration de l’acheminement transfert, les champs correspondants sur l’ordre de transfert sont renseignés automatiquement.

    Lorsque vous renseignez le champ **Code prestation transporteur**, le programme calcule la date de réception au magasin de destination en ajoutant le délai d’expédition de la prestation transporteur à la date d’expédition.

3. Il existe plusieurs façons de remplir les lignes :

    |Option  |Description  |
    |---------|---------|
    |Manuellement     | Dans le raccourci **Lignes**, complétez une ligne pour un article, ou utilisez l’action **Sélectionner les articles** pour choisir plusieurs articles.        |
    |Automatiquement     | * Choisissez l’action **Extraire contenu emplacement** pour sélectionner des éléments existants dans un emplacement spécifique.<br><br>* Choisissez l’action **Extraire lignes réception** pour sélectionner les éléments qui viennent d’arriver dans le magasin provenance transfert.        |

    Vous pouvez maintenant expédier les articles.
4. Cliquez sur **Valider**, choisissez l’option **Expédition**, puis cliquez sur le bouton **OK**.

    Les articles sont à présent en transit entre les magasins spécifiés, selon l’acheminement transfert spécifié.

    En tant que magasinier dans le magasin provenance transfert, continuez à recevoir les articles. Les lignes Ordre transfert sont les mêmes que lors de l’expédition et ne peuvent pas être modifiées.
5. Cliquez sur **Valider**, choisissez l’option **Réception**, puis cliquez sur le bouton **OK**.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Publier plusieurs ordres transfert dans un lot

La procédure suivante explique comment valider plusieurs ordres transfert dans un lot.

1. 1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Ordres de transfert**, puis sélectionnez le lien associé.  
2. Sur la page **Ordres transfert**, sélectionnez les commandes à valider.
3. Dans le champ **N°**, ouvrez le menu contextuel et choisissez **Sélectionner plus**.
4. Cochez la case pour les lignes pour chaque commande que vous souhaitez valider.
5. Choisissez l’action **Validation**, puis sélectionnez l’action **Valider par lot**.
6. Sur la page **TPL ordre de transfert**, renseignez les champs comme nécessaire.

   > [!TIP]
    > Pour les ordres transfert qui utilisent un lieu de transit, vous pouvez choisir soit **Expédier** ou **Recevoir**. Répétez cette étape si vous devez faire les deux. Pour les commandes où l’option **Validation directe** est activée, les deux options fonctionnent de la même manière et valident intégralement la commande.

7. Sélectionnez **OK**.
8. Pour afficher les problèmes potentiels, ouvrez la page **Registre des messages d’erreur**.

    > [!NOTE]
    > La validation de plusieurs documents peut prendre un certain temps et bloquer d’autres utilisateurs. Envisagez d’activer la validation en arrière-plan. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Planifier une entrée dans la file d’attente des tâches pour publier plusieurs documents dans un lot

Vous pouvez également utiliser la file d’attente des tâches pour programmer la validation à un moment qui convient à votre organisation. Par exemple, il peut sembler raisonnable dans votre activité d’exécuter certaines routines lorsque la plupart de la saisie de données de la journée est achevée.

La procédure suivante décrit comment définir le rapport **TPL valider les ordres transfert** pour une validation automatique des ordres transfert direct lancées à 16 h 00 les jours de semaine. Cette heure n’est qu’un exemple. Les étapes sont similaires pour les autres documents.  

1. Recherchez la page **Écritures file d’attente des tâches**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Type objet à exécuter**, sélectionnez **Rapport**.  
4. Dans le champ **ID objet à exécuter**, sélectionnez **5707, TPL valider ordres transfert**.
5. Activez la case à cocher **Page requête état**.
6. Sur la page de demande **TPL valider ordres de transfert**, choisissez l’option **Expédier**, filtrez sur **Transfert direct**, puis sélectionnez **OK**.

   > [!IMPORTANT]
   > Il est important de définir des filtres. Sinon, [!INCLUDE [prod_short](includes/prod_short.md)] validera tous les documents, même s’ils ne sont pas prêts. Pensez à définir un filtre sur le champ **Statut** pour la valeur **Lancé**, et un filtre sur le champ **Date comptabilisation** pour la valeur **..aujourd’hui**. Pour en savoir plus sur les filtres, accédez à [Trier, rechercher et filtrer](/dynamics365/business-central/ui-enter-criteria-filters).

7. Activez toutes les cases à cocher de **Exécuter le lundi** à **Exécuter le vendredi**.
8. Dans le champ **Heure début**, entrez **16 h 00**.
9. Choisissez l’action **Attribuer le statut Prêt**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Pour transférer des articles avec la feuille reclassement article

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles reclassement article**, puis choisissez le lien associé.
2. Sur la page **Feuilles reclassement article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Dans le champ **Code magasin**, entrez le magasin où les articles sont actuellement stockés.

    > [!NOTE]  
    > Pour transférer les articles qui n’ont aucun code magasin, laissez le champ **Code magasin** vide.
4. Dans le champ **Nouveau Code magasin**, indiquez le magasin vers lequel vous souhaitez transférer les articles.
5. Sélectionnez l’action **Valider**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="undo-a-transfer-shipment"></a>Annuler une expédition transfert

Si vous trouvez une erreur dans une quantité sur un ordre transfert validé, tant que l’expédition n’est pas reçue, vous pouvez facilement corriger la quantité. Sur la page **Expédition de transfert validée**, l’action **Annuler l’expédition** crée des lignes correctives, comme suit :

* La valeur du champ **Quantité expédiée** est diminuée de la quantité que vous avez annulée.
* La valeur du champ **Quantité à expédier** est accrue de la quantité que vous avez annulée.
* La case **Correction** est cochée pour les lignes.

Si la quantité a été expédiée dans une expédition entrepôt, une ligne de correction est créée dans l’expédition entrepôt validée.

Pour terminer la correction, rouvrez l’ordre transfert, entrez la quantité correcte, puis validez l’ordre. Si la commande doit être expédiée à l’aide d’une expédition entrepôt, créez et validez une expédition entrepôt.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/transfer-items/) associée

## <a name="see-also"></a>Voir aussi

[Gestion du stock](inventory-manage-inventory.md)  
[Configurer des magasins](inventory-how-setup-locations.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Modifier les fonctionnalités affichées](ui-experiences.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
