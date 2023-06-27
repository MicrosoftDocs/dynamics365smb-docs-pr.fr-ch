---
title: Utiliser les états intracommunautaires
description: Découvrez comment enregistrer les transactions avec des sociétés d’autres pays de l’UE à l’aide du système d’états intracommunautaires.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 09/02/2022
ms.author: altotovi
---
# <a name="work-with-intrastat-reporting"></a>Utiliser les états intracommunautaires

Toutes les sociétés de l’Union européenne (UE) doivent déclarer leurs échanges avec les autres pays/régions de l’Union européenne. Vous devez déclarer les mouvements de marchandises aux autorités statistiques de votre pays/région mensuellement et la déclaration doit être remise aux autorités fiscales. Intrastat est le système de collecte des statistiques du commerce des biens au sein de ces pays/régions. Vous utilisez un **État intracommunautaire** pour effectuer des déclarations intracommunautaires périodiques (généralement mensuelles), collecter, enregistrer et déclarer le commerce de marchandises conformément à la législation administrative locale.

La déclaration intracommunautaire Intrastat est basée sur les réglementations de base de l’UE qui s’appliquent à tous les pays ; cependant, dans la pratique, il existe certaines différences au sein des différents pays. Chaque pays a ses règles édictant exactement quoi déclarer et comment.

> [!IMPORTANT]
> Cet article décrit la nouvelle expérience d’états intracommunautaires disponible dans [!INCLUDE[prod_short](includes/prod_short.md)] à partir de la 2e vague de lancement 2022, qui comprend des fonctionnalités étendues et [doit être activée pour les entreprises existantes](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Contactez votre administrateur pour activer et configurer la nouvelle fonctionnalité.
>
> Lisez l’article sur la configuration et l’utilisation des états intracommuncautaires de la version précédente ici : [Configurer et enregistrer un état intracommunautaire](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]
> Les informations intracommunautaires ne s’appliquent pas aux mouvements de services entre pays, mais uniquement aux biens (articles et immobilisations). Si le gouvernement local exige l’enregistrement du mouvement des services entre les pays, cela est possible en utilisant la fonctionnalité **Déclaration de service**.
>
> Nous prévoyons actuellement que cette fonctionnalité sera disponible à partir de novembre 2022 en tant qu’application sur [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). A ce moment, pour l’utiliser, vous devrez d’abord l’installer sur la page **Gestion des extensions**.

## <a name="fill-in-the-intrastat-report"></a>Remplir un état intracommunautaire

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Liste de la déclaration d’échanges de biens**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau** pour créer un nouvel **État intracommunautaire**.
3. Si vous devez saisir des informations internes sur **l’état intracommunautaire**, renseignez ces informations dans le champ **Description**.
4. Dans le champ **Période statistique**, spécifiez le mois pour lequel rapporter les données. Entrez la période sous la forme d’un nombre à quatre chiffres sans espaces ni symboles. Selon votre pays, entrez soit le mois d’abord, puis l’année, soit l’inverse. Par exemple; saisissez soit *2206*, soit *0622* pour juin 2022.
5. Choisissez l’action **Proposer lignes**. Les champs **Date début** et **Date fin** contiennent déjà les dates spécifiées dans l’en-tête de l’état intracommunautaire pour la période statistique.
6. Dans le champ **% régulation coût**, entrez un pourcentage pour couvrir le transport et l’assurance. Lorsque vous saisissez un pourcentage, la valeur du champ **Valeur statistique** de la feuille augmente proportionnellement. Mais si vous voulez utiliser cette fonction, vous devez changer le champ **Montant frais annexes inclus** en **Oui**.
7. Vous pouvez éventuellement configurer des configurations supplémentaires sur le raccourci **Supplémentaire** :
   1. **Ignorer le recalcul des montants nuls** pour spécifier que les lignes sans montant ne seront pas recalculées lors du traitement par lots.
   2. **Ignorer les montants nuls** pour spécifier que les écritures comptables article sans montant ne sont pas incluses dans le traitement par lots.
   3. **Afficher les écritures de frais annexes** pour spécifier si vous souhaitez afficher coûts directs que votre société a affectés et validés en tant que frais annexes.
   4. **Ignorer écritures non facturées** pour spécifier si les écritures comptables article expédiées ou reçues mais pas encore facturées doivent être exclues du traitement.
8. Cliquez sur **OK** pour démarrer le traitement par lots.

Le traitement par lots récupère toutes les écritures article de la période statistique et les insère sous forme de lignes dans **l’état intracommunautaire**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Modifier l’état intracommunautaire

Si nécessaire, vous pouvez modifier les lignes, mais chaque fois que vous modifiez une valeur dans une ligne de l’état intracommunautaire, le champ **Correction** est automatiquement marqué comme **Oui**. Vous pouvez éventuellement ajouter une nouvelle ligne manuellement s’il y a une raison à cela. Pour ajouter une nouvelle ligne manuellement :

1. Sur la page **État intracommunautaire**, sur le raccourci **Lignes**, sélectionnez l’action **Nouvelle ligne**.
2. Sélectionnez l’option **Réception** ou **Expédition** dans le champ **Type**.
3. Dans le champ **Type de source**, choisissez l’une des sources : **Écriture article**, **Écriture immo.** ou **Écriture projet**.
4. Sur la base du **Type de source** dans le champ **Numéro d’article**, vous pouvez choisir un **Article** (dans les deux cas,**Écriture article** ou **Écriture projet**) ou des **Immobilisations**.
5. Remplissez les autres champs dont vous avez besoin pour l’état intracommunautaire.

> [!NOTE]
> Lorsque vous ajoutez manuellement une nouvelle ligne à l’état intracommunautaire, le champ **Date** de la ligne doit être à l’intérieur de la **Période statistique** que vous avez ajoutée dans l’en-tête.

## <a name="validate-intrastat-lines"></a>Valider les lignes intracommunautaires

Après avoir renseigné **l’état intracommunautaire**, vous pouvez exécuter l’action **État : Liste de contrôle** pour vérifier que toutes les informations de **l’état intracommunautaire** sont correctes. Les champs obligatoires que vous avez définis sur la page **Liste de contrôle des états intracommunautaires** auxquels il manque des valeurs seront affichés dans le récapitulatif **Erreurs et avertissements** de la page **État intracommunautaire**.

Exécutez l’état **Liste de contrôle des états intracommunautaires** pour vérifier les lignes de l’état intracommunautaire avant leur exportation au format requis. La vérification est exécutée dans **l’état intracommunautaire**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Recalculer le poids ou l’unité de mesure supplémentaire

Si vous recevez le message d’erreur *Le Poids total dans la ligne de l’état intracommunautaire ne doit pas être vide*, c’est probablement parce que vous n’avez pas défini le champ **Poids net** sur la source, l’article ou l’immobilisation utilisée. Dans ce cas, recherchez la fiche article ou immobilisation et ajoutez la valeur requise. Après cela, il vous suffit de rouvrir **l’état intracommunautaire** et de suivre ces étapes :

1. Sélectionnez l’action **Recalc. Poids/Unité suppl.** pour recalculer le **Poids total** et/ou la **Quantité supplémentaire**.
2. Choisissez l’une des options suivantes :

    1. **Poids** : pour ne recalculer que le **Poids total**, sur la base des informations actuelles sur le **Poids net** sur les fiches article et immobilisation.
    2. **Quantité d’unité de mesure supplémentaire** : pour ne recalculer que la **Quantité supplémentaire** sur la ligne **État intracommunautaire** si elle existe, sur la base des informations actuelles sur **l’Unité de mesure supplémentaire** sur les fiches article et immobilisation.
    3. **Les deux** : pour recalculer à la fois le **Poids total** et la **Quantité supplémentaire** sur la base des informations actuelles sur les fiches article et immobilisation.
3. Cliquez sur **OK** pour démarrer le traitement par lots.

## <a name="report-intrastat-in-a-file"></a>Enregistrer un état intracommunautaire sur un fichier

Vous pouvez soumettre l’état intracommunautaire sous forme de fichier en fonction des exigences des différentes autorités locales. Avant de créer le fichier, vous devez exécuter la **Liste de contrôle des états intracommunautaires** pour vérifier si toutes les lignes contiennent toutes les informations nécessaires et valides. Pour créer un fichier :

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Liste de la déclaration d’échanges de biens**, puis choisissez le lien associé.
2. Sélectionnez **l’état intracommunautaire** vous souhaitez convertir en fichier.
3. Si ce n’est déjà fait, renseignez **l’état intracommunautaire** manuellement ou sélectionnez l’action **Proposer lignes**.
4. Choisissez l’action **Créer fichier**.
5. Le fichier d’état intracommunautaire sera enregistré au format souhaité.

Une fois le fichier créé, [!INCLUDE[prod_short](includes/prod_short.md)] remplira automatiquement les détails suivants concernant la génération d’états :

* La **Date d’exportation** pour spécifier la date à laquelle l’état a été exporté.
* L’**Heure d’exportation** pour spécifier l’heure à laquelle l’état a été exporté.

> [!NOTE]
> La prochaine fois que vous créerez un fichier, les champs **Date d’exportation** et **Heure d’exportation** ne conserveront que les informations sur le dernier fichier que vous avez créé.

## <a name="intrastat-rules"></a>Règles des états intracommunautaires

### <a name="grouping-lines"></a>Regrouper des lignes

Dans les lignes d’un **état intracommunautaire**, il n’existe aucun regroupement par champ. Toutes les écritures sont copiées de la source d’origine, vous pouvez donc les localiser rapidement en fonction de la combinaison du **Type de Source** et du **N° séquence origine**.

Le regroupement requis par les autorités sera fourni dans le fichier exporté. Vous devez le configurer dans la **Définition d’échange de données**, qui est entièrement configurable. Pour plus d’informations, consultez [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Génération d’états sur les immobilisations

Les immobilisations seront affichées dans les lignes des états intracommunautaires uniquement si :

* Le **Type compta. immo.** dans le champ **Écriture comptable TVA** est **Coût acquisition** et si le **Type de document** est **Facture** dans le cas des achats, et
* Le **Type compta. immo.** dans le champ **Écriture comptable TVA** est **Produit de cession** et si le **Type de document** est **Facture** dans le cas des ventes.

### <a name="intrastat-report-statuses"></a>Statuts de l’état intracommunautaire

Lorsque vous travaillez avec **l’état intracommunautaire**, vous voyez un champ **Statut** dans l’en-tête du document. Vous pouvez trouver les statuts suivants ainsi que les règles associées :

* *Ouvert* : ce statut est créé automatiquement lorsque vous créez un nouvel état intracommunautaire et vous pouvez effectuer toutes les opérations dans ce statut.
* *Publié* : [!INCLUDE[prod_short](includes/prod_short.md)] change automatiquement le statut en *Publié* lorsque vous créez un fichier. A partir de ce moment, vous ne pouvez plus modifier votre **État intracommunautaire**. Si vous devez modifier quelque chose, vous pouvez utiliser l’action **Rouvrir** pour rouvrir l’état intracommunautaire. Une fois le document rouvert, vous pouvez utiliser l’action **Publier** pour publier à nouveau le document.
* **Déclaré** : spécifie si l’écriture a déjà été déclarée aux administrations fiscales. Ce n’est pas un statut normal mais un champ indépendant, et même si vous rouvriez l’état intracommunautaire, cela montrerait toujours que le fichier est déjà créé pour cet état.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Voir aussi

[Paramétrer les états intracommunautaires](finance-how-setup-report-intrastat.md)  
[Gestion financière](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
