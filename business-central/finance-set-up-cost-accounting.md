---
title: Paramétrage du contrôle de gestion
description: 'Avant d’utiliser la comptabilité analytique, vous devez effectuer des tâches de paramétrage. Chaque écriture de coût doit avoir un type de coût et un centre de coûts ou un coût associé.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 10/09/2023
ms.author: bholtorf
---
# <a name="setting-up-cost-accounting"></a>Paramétrage du contrôle de gestion

Avant d’utiliser la comptabilité analytique, vous devez effectuer des tâches de paramétrage.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Soldes entre le type de coût, un centre de coûts et les coûts associés

Lorsque vous configurez la comptabilité analytique, vous devez vous assurer que toutes les écritures sont affectées à un type de coût, ainsi qu’à un centre de coûts ou des coûts associés. En d’autres termes, un type de coût, un code de centre de coûts ou un coût associé doivent être affectés à chaque écriture de coûts. Cette règle garantit que chaque écriture de coûts s’affiche dans les centres de coûts ou les coûts associés, mais jamais dans les deux à la fois.  

Ce faisant, vous créez l’équation comptable suivante :  

*Solde type de coût* = *Solde centre de coûts* + *Solde coûts associés*  

Lorsque vous imprimez le plan du type de coût, le plan des centres de coûts et le plan des états de coûts associés, vous pouvez analyser cette relation.

## <a name="setting-up-cost-types"></a>Configuration de types de coûts

Le plan des types de coûts a la même fonction que le plan comptable général. Vous pouvez configurer le plan des types de coûts comme suit :  

- La structure du plan des types de coûts a la même fonction que les comptes de gestion dans le plan comptable général. Vous pouvez ensuite transférer le plan comptable général vers le plan des types de coûts. Vous pouvez effectuer tous les ajustements nécessaires après le transfert.  
- Créez le plan des types de coûts ou ajoutez de nouveaux types de coûts au plan comptable existant des types de coûts. Vous devez créer chaque type de coûts individuellement.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Pour transférer le plan comptable général vers le plan des types de coûts

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable des types de coûts**, puis choisissez le lien associé.  
2. Choisissez l’action **Obtenir les types de coûts à partir du plan comptable**. Dans la boîte de dialogue, cliquez sur **Oui** pour confirmer le transfert. La fonction utilise le plan comptable général pour créer le plan des types de coûts.  

    Le plan des types de coûts contient désormais tous les comptes de gestion en comptabilité, et comprend les titres et les totaux. Vous pouvez modifier le plan des types de coûts, selon vos besoins. Par exemple, vous pouvez supprimer les types de coûts existants en double.  

    > [!IMPORTANT]  
    >  La fonction **Enregistrer les types de coûts dans le plan comptable** met à jour la relation entre le plan comptable et le plan des types de coûts. Le champ **N°** est renseigné et vérifié pour s’assurer que chaque compte général est lié à un seul type de coût. La fonction est automatiquement exécutée avant le transfert des écritures comptables vers la comptabilité analytique.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Pour configurer de nouveaux types de coût sur la page Plan comptable des types de coûts

1. Ouvrez la page **Plan comptable des types de coûts** en mode édition.  
2. Renseignez les champs comme décrit selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Vous pouvez configurer et gérer les types de coût, soit sur la page **Fiche type de coût**, soit sur la page **Plan comptable des types de coûts**. Dans cette procédure, vous configurez de nouveaux types de coût sur la page **Plan comptable des types de coûts**.

3. Après avoir créé tous les types de coûts, choisissez l’action **Indenter les types de coûts**. Dans la boîte de dialogue, cliquez sur **Oui**.  
4. Liez le nouveau type de coût au compte général correspondant.  

    > [!IMPORTANT]  
    >  Si vous avez entré des définitions dans les champs **Totalisation** pour le type de ligne **Fin total** avant d’exécuter la fonction **Indenter les types de coûts**, vous devez les entrer à nouveau car cette fonction remplace les valeurs de tous les champs **Fin total**.  

### <a name="to-update-cost-types"></a>Pour mettre à jour les types de coûts

1. Sur la page **Paramètres comptabilité analytique**, indiquez si vous souhaitez que le plan des types de coûts soit mis à jour automatiquement lorsque le plan comptable est modifié.  
2. Dans le champ **Aligner compte général**, vous pouvez choisir les options suivantes.  

- **Pas d’alignement** - Il n’existe aucune modification correspondante dans le plan des types de coûts lorsque vous modifiez le plan comptable.  
- **Automatique** - Une modification correspondante est apportée dans le plan des types de coûts lorsque vous modifiez le plan comptable.  
- **Invite** - Un message s’affiche et vous demande si vous voulez apporter une modification correspondante dans le plan des types de coûts lorsque vous modifiez le plan comptable.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Définition de la relation entre les types de coûts et les comptes généraux

Une relation entre le type de coût et le compte général est créée dans le type de coût et le compte général.  

- Le champ **Plage compte général** de la table **Type coût** définit les comptes généraux appartenant à un type de coût.  
- Le champ **N° type coût de solde** du plan comptable définit l’appartenance du compte général à un type de coût.  

Ces deux champs sont renseignés automatiquement lorsque vous utilisez la fonction **Obtenir les types de coûts à partir du plan comptable**.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relations entre les comptes généraux et les types de coûts

Une relation n:1 existe entre les comptes généraux et les types de coûts. Plusieurs comptes généraux peuvent appartenir à un type de coût, mais chaque compte général appartient à un seul type de coût. Le tableau suivant décrit la relation en détails.  

|Relation|**Plage compte général**|**N° type coût**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Un compte général pour chaque type de coût|Un compte général|Un type de coût|  
|Plusieurs comptes généraux pour chaque type de coût|Plage de comptes généraux, par exemple, 7110..7193 pour chaque compte général|Pour chaque compte général de la plage, il n’existe qu’un seul type de coût|  
|Types de coûts sans comptes généraux correspondants|\<Empty\>||  
|Comptes généraux dont les écritures ne seront pas transférées||\<Empty\>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Types de coûts sans relation avec la comptabilité générale

Un type de coût risque de ne pas afficher une relation avec les comptes généraux si une des conditions suivantes est vraie :  

- Les comptes pour la comptabilité opérationnelle, notamment les intérêts et l’amortissement, prennent uniquement les coûts provenant de la comptabilité opérationnelle.  
- Les types de coûts, notamment 9901, 9902 et 9903, dans la base de données [!INCLUDE[prod_short](includes/prod_short.md)] servent de comptes de crédit et de débit pour les affectations.  
- Le compte 9920 dans la base de données [!INCLUDE[prod_short](includes/prod_short.md)] indique les régularisations réelles qui font état de la différence entre les coûts et les frais provenant de la comptabilité.

## <a name="setting-up-cost-centers"></a>Configuration des centres de coûts

Les centres de coûts sont les départements responsables des coûts et des revenus. Le plan des centres de coûts est semblable aux informations sur l’axe analytique pour la comptabilité. Vous pouvez configurer le plan des centres de coûts comme suit :  

- Transférez des sections analytiques de la comptabilité vers le plan des centres de coûts. Vous pouvez effectuer tous les ajustements nécessaires après le transfert.  
- Créez un nouveau plan du centre de coûts, qui est indépendant de la comptabilité ou ajoutez un nouveau centre de coûts à un plan existant du centre de coûts. Vous devez créer chaque centre de coûts individuellement.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Pour transférer des sections analytiques de la comptabilité vers le plan des centres de coûts.

1. Définissez un axe analytique pour être celui de la dimension des centres de coûts sur la page **Paramètres comptabilité analytique**. Seules les valeurs de cet axe analytique sont transférées.
Vous pouvez choisir **Actions** > **Fonctions** > **Mettre à jour les axes analytiques de comptabilité analytique** pour mettre à jour les dimensions de comptabilité analytique.
1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable des centres de coûts**, puis choisissez le lien associé.  
1. Sous l’onglet **Actions**, dans le groupe **Fonctions**, choisissez **Extraire les centres de coûts de l’axe analytique** pour transférer des sections du plan des centres de coûts. La fonction transfère les sections analytiques que vous avez définis dans l’étape 1.  

    > [!NOTE]  
    >  Vous pouvez configurer le champ **Aligner axe centre de coûts** pour définir la synchronisation unidirectionnelle des sections analytiques à partir de la comptabilité vers le plan des centres de coûts. Vous ne pouvez pas définir une synchronisation du plan des centres de coûts avec les sections analytiques issues de la comptabilité.  

Le plan des centres de coûts comprend désormais toutes les sections analytiques spécifiées provenant de la comptabilité. Il inclut les titres et les sous-totaux.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Pour créer de nouveaux centres de coût sur la page Plan comptable des centres de coûts

Vous pouvez configurer et gérer les centres de coût, soit sur la page **Fiche centre de coût**, soit sur la page **Plan comptable des centres de coûts**. Dans cette procédure, vous configurez de nouveaux centres de coût sur la page **Plan comptable des centres de coûts**.  

1. Ouvrez la page **Plan comptable des centres de coûts** en mode édition.  
2. Dans le champ **Code**, entrez le code centre de coûts. Tous les centres de coûts doivent avoir un code.  
3. Dans le champ **Nom**, saisissez le nom du centre de coûts.  
4. Sélectionnez la flèche déroulante dans le champ **Type ligne** pour spécifier l’objectif du centre de coûts.  

    - Pour les centres de coûts de type **Total**, vous devez renseigner le champ **Totalisation**. Utilisez l’opérateur **or**, qui est une ligne verticale (**&#124;**) pour définir les plages des centres de coûts.  
    - Pour les centres de coûts de type de ligne **Fin total**, ce champ est renseigné automatiquement lorsque vous utilisez la fonction d’indentation.  
5. Renseignez les champs **Ordre de tri** et **Sous-type coût**.  
6. Choisissez la ligne vide suivante pour créer un centre de coûts, puis répétez les étapes 2 à 5.  
7. Après avoir défini tous les centres de coûts, choisissez l’action **Indenter les centres de coûts**. Cliquez sur le bouton **Oui**.  

> [!IMPORTANT]  
> Si vous avez saisi des définitions dans les champs **Totalisation** pour les centres de coûts **Fin total** avant d’exécuter la fonction d’indentation, vous devez les saisir à nouveau. La fonction remplace les valeurs dans tous les champs **Fin total**.

## <a name="setting-up-cost-objects"></a>Configuration des coûts associés

Les coûts associés sont les projets, les biens ou les services d’une société. Le plan des coûts associés est semblable aux informations sur l’axe analytique pour la comptabilité. Vous pouvez configurer le plan des coûts associés comme suit :  

* Transférez des sections analytiques de la comptabilité vers le plan comptable des coûts associés. Vous pouvez effectuer tous les ajustements nécessaires après le transfert.  
* Créez un nouveau plan des coûts associés, qui est indépendant de la comptabilité ou ajoutez un nouveau coût associé à un plan existant des coûts associés. Vous devez créer chaque coût associé individuellement.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Pour transférer des sections analytiques depuis la comptabilité vers le plan comptable des coûts associés

1.  Définissez un axe analytique pour être celui des coûts associés sur la page **Actualiser axes analytiques CA**. Seules les valeurs de cet axe analytique sont transférées.  
2.  Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 3.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable des coûts**, puis choisissez le lien associé.  
3.  Choisissez l’action **Extraire les coûts associés de l’axe analytique** pour transférer des sections analytiques du plan comptable de coûts associés. La fonction transfère les axes analytiques que vous avez définis dans l’étape 1.  

    > [!NOTE]  
    >  Vous pouvez configurer le champ **Aligner axe coûts associés** pour définir la synchronisation unidirectionnelle des sections analytiques à partir de la comptabilité vers le plan des coûts associés. Vous ne pouvez pas définir une synchronisation du plan de coûts associés avec les sections analytiques issues de la comptabilité.  

Le plan comptable de coûts associés comprend désormais toutes les sections analytiques spécifiées provenant de la comptabilité. Il inclut les titres et les sous-totaux.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Pour créer de nouveaux coûts associés sur la page Plan comptable des coûts associés

Vous pouvez configurer et gérer les coûts associés, soit sur la page **Fiche coûts associés**, soit sur la page **Plan comptable des coûts associés**. Dans cette procédure, vous configurez de nouveaux coûts associés sur la page **Plan comptable des coûts associés**.  

1.  Ouvrez la page **Plan comptable des coûts associés** en mode édition.  
2.  Dans le champ **Code**, entrez le code coût associé. Tous les coûts associés doivent avoir un code.  
3.  Dans le champ **Nom**, saisissez le nom du coût associé.  
4.  Sélectionnez la flèche déroulante dans le champ **Type ligne** pour spécifier l’objectif du coût associé.  

    * Pour les coûts associés de type de ligne **Total**, renseignez le champ **Total De/À**. Utilisez l’opérateur **or**, qui est une ligne verticale (**&#124;**), pour définir les plages des coûts associés.  
    * Pour les coûts associés de type de ligne **Fin total**, ce champ est renseigné automatiquement lorsque vous utilisez la fonction d’indentation.  
5.  Renseignez le champ **Ordre de tri**.  
6.  Choisissez la ligne vide suivante pour créer un coût associé, puis répétez les étapes 2 à 5.  
7.  Après avoir défini tous les coûts associés, choisissez l’action **Indenter les coûts associés**. Cliquez sur le bouton **Oui**.  

> [!IMPORTANT]  
>  Si vous avez saisi des définitions dans les champs **Total De/À** pour les coûts associés **Fin total** avant d’exécuter la fonction d’indentation, vous devez les saisir à nouveau. La fonction remplace les valeurs dans tous les champs **Fin total**.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Définition des centres de coûts et des coûts associés pour le plan comptable

Vous pouvez transférer automatiquement les écritures de dépenses et de revenus à partir de la comptabilité générale vers la comptabilité analytique, que ce soit pour la validation comptable ou avec un traitement par lots. Lors du transfert, [!INCLUDE[prod_short](includes/prod_short.md)] transfère uniquement les écritures déjà liées à un centre de coûts ou aux coûts associés. Pour préparer un transfert pertinent, assurez-vous que les centres de coûts et les coûts associés sont définis correctement.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Définition des sections analytiques par défaut pour des comptes généraux

Pour chaque compte général, vous pouvez définir des sections analytiques par défaut dans la table **Affectation analytique**. L’exemple suivant décrit la configuration requise pour avoir un centre de coût DÉPARTEMENT sans jamais avoir de coûts associés PROJET lors de la validation d’un compte général.  

|**Code axe analytique**|**Contrôle validation**|  
|------------------------------------------|-----------------------------------------|  
|Département|Code obligatoire|  
|Dossier|Pas de code|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Définition des sections analytiques pour les frais généraux et les coûts directs

 Vous pouvez transférer des frais généraux à un centre de coûts, et des coûts directs aux coûts associés. Le tableau suivant décrit comment optimiser la combinaison des valeurs de paramétrage des axes analytiques.  

|Transférer vers|Validation du centre de coûts|Validation des coûts associés|  
|-----------------|-------------------------|-------------------------|  
|Centre de coûts|Code obligatoire|Pas de code|  
|Coûts associés|Pas de code|Code obligatoire|  

> [!NOTE]  
>  Pour vous assurer que le centre de coûts et les coûts associés prédéfinis et configurés en comptabilité générale sont reportés automatiquement dans la comptabilité analytique, cochez la case **Vérifier validations compta** sur la page Paramètres comptabilité analytique.

## <a name="see-also"></a>Voir aussi

[Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
[Transfert et validation des écritures de coûts](finance-transfer-and-post-cost-entries.md)  
[Définition et répartition des coûts](finance-define-and-allocate-costs.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
