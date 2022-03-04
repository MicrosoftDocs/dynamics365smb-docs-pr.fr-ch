---
title: Utilisation des dimensions pour suivre et analyser facilement les données
description: Utilisez les axes analytiques pour classer des écritures par catégorie, par exemple, par service ou le projet, afin de facilement suivre et analyser les données pour vous aider à prendre les bonnes décisions commerciales.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.search.form: 408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 31e57e20a7ec6492624684fc5973d1ab972b5de9
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145669"
---
# <a name="working-with-dimensions"></a>Utilisation des axes analytiques

Les axes analytiques sont des valeurs qui permettent de catégoriser les écritures afin de pouvoir les suivre et les analyser sur les documents, tels que les commandes vente. Ils peuvent par exemple indiquer de quel projet ou département provient une écriture.  

Par exemple, au lieu de configurer des comptes généraux distincts pour chaque service et projet, vous pouvez utiliser les axes analytiques comme base d’analyse et éviter d’avoir à créer un plan comptable compliqué. Pour plus d’informations, reportez-vous à [Veille économique](bi.md).

Un autre exemple consiste à configurer un axe analytique appelé *Département* et utiliser cet axe lorsque vous validez des documents vente. Cela vous permet d’utiliser les outils de veille économique pour savoir quel département a vendu quels articles. Plus vous utilisez d’axes analytiques, plus vous pouvez baser vos décisions commerciales sur des états détaillés. Par exemple, une seule écriture vente peut comporter des informations depuis plusieurs axes analytiques :  

* Le compte sur lequel la vente de l’article a été validée  
* L’endroit où l’article a été vendu
* Le nom du vendeur
* Le type de client qui a effectué l’achat  

## <a name="analyzing-by-dimensions"></a>Analyse par axe analytique

La fonctionnalité Axes analytiques joue un rôle important dans la veille économique, par exemple en définissant des vues d’analyse. Pour plus d’informations, reportez vous à [Analyser des données par axe analytique](bi-how-analyze-data-dimension.md).

> [!TIP]
> Pour analyser rapidement les données transactionnelles par dimensions, vous pouvez filtrer les totaux du plan comptable et les entrées de toutes les pages **Définir le filtre axe** par axes analytiques.

> [!NOTE]
> Les vues d′analyse utilisent souvent les données des axes analytiques. Si vous découvrez qu′un axe analytique incorrect a été utilisé sur des écritures comptables validées, vous pouvez corriger les valeurs d′axes analytiques et mettre à jour les vues d′analyse. Cela vous aidera à garder vos rapports et analyses financières exactes. Pour plus d’informations, voir [Dépannage et correction des axes analytiques](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="dimension-sets"></a>Ensembles de dimensions

<!--we describe what they are, but not their value.-->
Un ensemble de dimensions est une combinaison unique de sections analytiques. Il est stocké comme des écritures de l’ensemble de dimensions dans la base de données. Chaque écriture de l’ensemble de dimensions représente une section analytique unique. L’ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l’ensemble de dimensions.  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d’enregistrer explicitement chaque section analytique dans la base de données, un ID d’ensemble de dimensions est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document pour spécifier l’ensemble de dimensions.  

## <a name="setting-up-dimensions"></a>Configuration d’axes

Vous pouvez définir les axes et les sections analytiques pour classer des feuilles et des documents par catégorie, comme des commandes vente et achat. La page **Axes analytiques** permet de créer une ligne pour chaque axe, par exemple *Projet*, *Département*, *Zone* et *Commercial*.

Vous pouvez également définir des valeurs pour des axes. Il peut par exemple s’agir de départements de votre société. Les sections analytiques peuvent être paramétrées sous forme de structure hiérarchique similaire au plan comptable, de manière à ce que les données puissent être réparties en plusieurs niveaux de granularité et à ce que des sous-ensembles de sections analytiques puissent être totalisés. Vous pouvez définir autant d’axes et de sections analytiques que nécessaire, tous les membres de votre société peuvent les utiliser.

Lorsque les axes et les valeurs sont configurées, vous pouvez définir les axes principaux et des raccourcis axe sur la page **Paramètres comptabilité** qui seront toujours disponibles pour sélection comme champs sur les lignes feuille et document, et les écritures comptables sans avoir à ouvrir la page **Axes analytiques** en premier lieu. Pour plus d’informations, reportez-vous à la rubrique [Configurer les axes principaux et les raccourcis axe](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* Les **Axes principaux** sont utilisés comme filtres, par exemple, dans les états, les traitements par lots et les XMLports. Vous pouvez uniquement utiliser deux axes principaux, choisissez donc des axes que vous utilisez souvent.
* Les **Raccourcis axe** sont disponibles sous forme de champ dans les lignes feuille et document et les écritures comptables. Vous pouvez en créer huit au maximum.  

> [!NOTE]
> Après avoir utilisé une nouvelle dimension dans une écriture, telle qu’une ligne ou un nouvel enregistrement, vous ne pouvez pas supprimer la dimension, même si vous ne validez pas l’entrée. Ceci est dû au fait que [!INCLUDE[prod_short](includes/prod_short.md)] crée immédiatement un ensemble de dimensions pour la ligne ou l’enregistrement. Pour plus d’informations, voir [Ensembles de dimensions](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Pour configurer des axes analytiques par défaut pour les clients, les fournisseurs et d’autres comptes

Vous pouvez attribuer un axe analytique par défaut pour un compte spécifique. L’axe est copié sur la feuille ou le document lorsque vous saisissez le numéro de compte dans une ligne, mais vous pouvez supprimer ou modifier le code sur la ligne si nécessaire. Vous pouvez également rendre un axe analytique obligatoire pour valider une écriture avec un type de compte spécifique.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Dimensions**, puis sélectionnez le lien associé.  
2. Sur la page **Axes analytiques** sélectionnez l’axe approprié, puis cliquez sur **Affectations par type compte**.  
3. Complétez une ligne pour chaque nouvelle affectation analytique à configurer. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Si vous souhaitez rendre un axe requis sans lui affecter de section analytique par défaut, ne renseignez pas le champ **Code section**, puis sélectionnez **Code obligatoire** dans le champ **Contrôle validation**.  

> [!WARNING]  
> Si un compte doit être utilisé dans le traitement par lots **Ajuster taux de change** ou **Valider coûts ajustés**, ne sélectionnez pas **Code obligatoire** ni **Même code**. Ces traitements par lots ne peuvent pas utiliser de codes axe.  

> [!NOTE]  
> Si une affectation différente de l’affectation analytique configurée pour ce type de compte doit être associée à un compte, vous devez paramétrer une affectation analytique pour ce compte. L’affectation analytique de ce compte remplace alors celle du type de compte.  

### <a name="to-set-up-default-dimension-priorities"></a>Pour configurer des affectations analytiques prioritaires

Des types de compte différents, tels qu’un compte client et un compte article, peuvent avoir des affectations analytiques différentes. Par conséquent, plusieurs affectations analytiques peuvent être proposées pour un axe dans une écriture. Pour éviter de tels conflits, vous pouvez appliquer des règles de priorité aux différentes sources.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Affect. analytique prioritaire**, puis sélectionnez le lien associé.  
2. Sur la page **Affect. analytique prioritaire**, dans le champ **Code journal,** entrez le code journal pour la table séquence à laquelle les affectations analytiques prioritaires s’appliquent.  
3. Complétez une ligne pour chaque affectation analytique prioritaire souhaitée pour le code journal sélectionné.
4. Répétez la procédure pour chaque code journal pour lequel vous souhaitez configurer des affectations analytiques prioritaires.  

> [!IMPORTANT]  
> Si vous configurez deux tables avec la même priorité pour le même code journal, [!INCLUDE[prod_short](includes/prod_short.md)] sélectionne la table ayant le plus petit ID.  

### <a name="to-set-up-dimension-combinations"></a>Pour configurer des croisements analytiques

Pour éviter de valider des écritures avec des axes contradictoires ou inappropriés, vous pouvez bloquer ou limiter des croisements spécifiques de deux axes. Lorsqu’un croisement analytique est bloqué, vous ne pouvez pas valider les deux axes sur la même écriture, quelles que soient les sections analytiques. Lorsqu’un croisement analytique est limité, vous pouvez valider les deux axes sur la même écriture, mais uniquement pour certains croisements de sections analytiques.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Croisements analytiques**, puis sélectionnez le lien associé.  
2. Sur la page **Croisements d’axes**, sélectionnez le champ du croisement analytique et sélectionnez l’une des options suivantes.  

    |Champ|Désignation|
    |----------------------------------|---------------------------------------|  
    |**Aucune limite**|Ce croisement analytique n’a pas de restrictions. Toutes les sections analytiques sont autorisées.|  
    |**Limité**|Ce croisement analytique a des restrictions selon les sections analytiques que vous entrez. Vous devez définir ces limites sur la page **Croisement section**.|  
    |**Bloqué**|Ce croisement analytique n’est pas autorisé.|  

3. Si vous avez sélectionné l’option **Limité**, vous devez définir les croisements de sections analytiques bloqués. Pour cela, sélectionnez le champ pour définir le croisement d’axe.  
4. Sélectionnez à présent le croisement de sections analytiques bloqué et entrez **Bloqué** dans le champ. Un champ blanc signifie que le croisement de sections est autorisé. Répétez cette procédure si plusieurs croisements sont bloqués.  

> [!NOTE]  
> Les mêmes axes s’affichent à la fois dans les lignes et les colonnes et, par conséquent, tous les croisements analytiques apparaissent deux fois. [!INCLUDE[prod_short](includes/prod_short.md)] affiche automatiquement le paramètre dans les deux champs. Vous ne pouvez rien sélectionner dans les champs situés dans le coin supérieur gauche et en bas car ces champs ont le même axe de ligne et de colonne.  
>
> L’option sélectionnée s’affiche uniquement lorsque vous quittez le champ.  
>
> Pour visualiser le nom des axes à la place du code, sélectionnez le champ **Afficher nom colonne**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Pour configurer des axes principaux et des raccourcis axe

Les axes principaux et les raccourcis axe peuvent être utilisés comme filtres dans [!INCLUDE[prod_short](includes/prod_short.md)], y compris sur les états, les traitements par lot, les pages d’écritures comptables et les vues d’analyse. Les axes principaux et les raccourcis axe sont toujours disponibles pour être insérés directement sans ouvrir tout d’abord la page **Axes analytiques**. Sur les lignes feuille et document, vous pouvez sélectionner les axes principaux et les raccourcis axe dans un champ sur la ligne. Vous pouvez définir deux axes principaux et huit raccourcis axe. Sélectionnez les axes que vous utilisez le plus souvent.

> [!Important]  
> Le fait de modifier un axe principal ou un raccourci axe exige que toutes les écritures saisies avec l’axe soient mises à jour. Pour modifier un axe analytique global, utilisez la fonction **Modifier les axes principaux**, mais cela peut se révéler chronophage et peut avoir un impact sur les performances et les tables peuvent être verrouillées lors de la mise à jour. Par conséquent, sélectionnez vos axes principaux et vos raccourcis axe avec soin afin que vous n’ayez pas à les changer ultérieurement. Pour modifier un axe analytique raccourci, utilisez l’action **Modifier les axes analytiques**. <br /><br />
> Pour plus d’informations, voir [Pour modifier les axes principaux](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Lorsque vous ajoutez ou modifiez un axe principal ou un raccourci axe, vous êtes automatiquement déconnecté et la nouvelle valeur est préparée pour un usage.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.
2. Sur le raccourci **Axes analytiques**, renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Pour modifier les axes principaux

Lorsque vous modifiez un axe principal ou un raccourci, toutes les écritures saisies avec l’axe en question sont mises à jour. Étant donné que ce processus peut prendre du temps et affecter les performances, deux modes différents sont fournis pour adapter le processus à la taille de la base de données.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.
2. Choisissez l’action **Modifier les axes principaux**.
3. En haut de la page, sélectionnez l’une des options suivantes pour définir dans quel mode le travail par lots est exécuté.

    |Option|Description|
    |-|-|
    |**Séquentiel**|(Par défaut) Le changement est effectué en une seule transaction en ramenant toutes les écritures aux axes qu’elles avaient avant le changement.<br /><br />Cette option est recommandée si la société contient relativement peu d’écritures publiées où il faudra plus de temps pour s’effectuer. Le processus verrouille plusieurs tables et bloque les autres utilisateurs jusqu’à ce qu’il soit terminé. Notez que sur les grandes bases de données, le processus peut ne pas être en mesure de s’effectuer dans ce mode. Dans ce cas, utilisez l’option **Parallèle**.|
    |**Parallèle**|Le changement de dimension se produit dans plusieurs sessions d’arrière-plan et l’opération est divisée en plusieurs transactions. Pour utiliser cette option, activez le bouton bascule **Traitement parallèle**. <br /><br />Cette option est recommandée pour les grandes bases de données ou les sociétés avec de nombreuses écritures publiées où il faudra plus de temps pour l’exécution. Notez qu’avec ce mode, le processus de mise à jour ne démarre pas s’il existe plusieurs sessions de base de données actives.|  

4. Dans les champs **Code Axe principal 1** et/ou **Code Axe principal 2**, entrez les nouveaux axes. Les axes actuels sont affichés en gris derrière les champs.
5. En fonction du mode, effectuez l’une des opérations suivantes :
    * Dans mode **Séquentiel**, choisissez l’action **Démarrer**.
    * Dans mode **Parallèle**, choisissez l’action **Préparer**.

    L’onglet **Écritures journal** contient des informations sur les axes qui seront modifiés.
6. Déconnectez-vous de [!INCLUDE[prod_short](includes/prod_short.md)], puis reconnectez-vous.
7. Choisissez l’action **Démarrer** pour démarrer le traitement parallèle des changements d’axe. <!--is this also dependent on the mode?-->

### <a name="example-of-dimension-setup"></a>Exemple de paramétrage d’axe analytique

Imaginons que votre société souhaite suivre les transactions selon la structure organisationnelle et les situations géographiques. Pour ce faire, vous pouvez configurer deux axes sur la page **Axes analytiques** :

* **REGION**  
* **DEPARTEMENT**  

| Code | Name | Libellé code | Libellé filtre |
| --- | --- | --- | --- |
| REGION |Région |Zone de recouvrement |Filtre zone |
| DEPARTEMENT |Département |Code emplacement immo |Filtre département |

Pour **ZONE**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Name | Type section |
| --- | --- | --- |
| 10 |Amériques |Début total |
| 20 |Amérique du Nord |Standard |
| 30 |Pacifique |Standard |
| 40 |Amérique du Sud |Standard |
| 50 |Amériques, Total |Fin total |
| 60 |Europe |Début total |
| 70 |INTRA |Standard |
| 80 |Non-UE |Standard |
| 90 |Europe, Total |Fin total |

Pour les deux zones géographiques principales, Amériques et Europe, ajoutez des sous-catégories pour les régions en mettant les sections analytiques en retrait. Cela vous permet de déclarer les ventes ou les dépenses dans les régions, et d’obtenir les totaux des zones géographiques plus étendues. Vous pouvez également choisir d’utiliser les pays ou les régions en tant que sections analytiques, ou des régions ou des villes, en fonction de votre entreprise.

> [!NOTE]  
> Pour configurer une hiérarchie, veillez à trier les codes dans l’ordre alphabétique. Ceci inclut les codes des sections analytiques fournis dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Pour **DÉPARTEMENT**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Name | Type section |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| FABR |Fabrication |Standard |
| VENTES |Ventes |Standard |

Avec ce paramétrage, vous pouvez ensuite ajouter les deux axes en tant qu’axes analytiques principaux sur la page **Paramètres comptabilité**. Cela signifie que vous pouvez utiliser ZONE et DÉPARTEMENT comme filtres pour les écritures comptables de la comptabilité, ainsi que dans tous les états et les tableaux d’analyse. Les deux axes principaux sont mis à disposition automatiquement pour être utilisés dans les lignes écriture et les en-têtes document comme raccourcis axe.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Affichage d’un aperçu des axes utilisés plusieurs fois

La page **Aff. analytiques - Multiples** spécifie la manière dont un groupe de comptes utilise les axes et sections analytiques. Vous pouvez effectuer cette opération en sélectionnant plusieurs comptes, et en spécifiant des axes et sections analytiques par défaut pour tous les comptes sélectionnés dans la liste des comptes. Lorsque vous spécifiez des affectations analytiques pour les comptes sélectionnés, l’application propose ces axes et sections analytiques à chaque fois que l’un de ces comptes est utilisé, par exemple sur une ligne feuille. La validation des écritures est ainsi facilitée, car les champs des axes analytiques sont renseignés automatiquement. Cependant, les sections analytiques proposés peuvent être modifiées, par exemple sur une ligne feuille.

La page **Aff. analytiques - Multiples** contient les champs suivants :

|Champ|Désignation|
|-----|-----------|  
|**Code axe analytique**|Affiche tous les axes définis comme affectations analytiques sur un ou plusieurs comptes sélectionnés. Si vous cliquez sur le champ, vous pouvez visualiser la liste de tous les axes analytiques disponibles. Si vous sélectionnez un axe, l’axe sélectionné est défini comme affectation analytique pour tous les comptes sélectionnés.|
|**Code section**|Affiche une section analytique ou le terme (Conflit). Si le champ indique une section analytique, tous les comptes sélectionnés ont la même section analytique par défaut pour un axe donné. Si le champ indique le terme (Conflit), les comptes sélectionnés n’ont pas tous la même section analytique par défaut pour un axe donné. Si vous cliquez sur le champ, vous pouvez visualiser la liste de toutes les sections analytiques disponibles pour un axe donné. Si vous sélectionnez une section analytique, la section sélectionnée est définie comme section par défaut pour tous les comptes sélectionnés.|
|**Contrôle validation**|Affiche une règle de contrôle validation ou le terme (Conflit). Si le champ indique une règle de contrôle validation, tous les comptes sélectionnés ont la même règle pour une section analytique donnée. Si le champ indique le terme (Conflit), les comptes sélectionnés n’ont pas tous la même règle de contrôle validation pour une section analytique donnée. Si vous cliquez sur le champ Contrôle validation, vous pouvez visualiser la liste des règles de contrôle validation. Si vous sélectionnez une règle de contrôle validation, la règle de contrôle validation sélectionnée s’applique à tous les comptes sélectionnés.|

## <a name="using-dimensions"></a>Utilisation des axes analytiques

Dans un document tel qu’une commande vente, vous pouvez ajouter des informations analytiques pour une seule ligne document et pour le document lui-même. Par exemple, sur la page **Commande vente**, vous pouvez saisir des sections analytiques pour les deux premiers raccourcis axe directement sur les lignes vente individuelles et ajouter des informations analytiques complémentaires si vous cliquez sur le bouton **Axes analytiques**.  

Si vous travaillez plutôt sur une feuille, vous pouvez également ajouter à une écriture des informations analytiques de la même manière, si vous avez configuré des raccourcis axe en tant que champs directement dans les lignes feuille.  

Vous pouvez configurer des axes analytiques par défaut pour des comptes ou des types de compte, de sorte que les axes et les sections analytiques soient renseignés automatiquement.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Pour afficher les axes principaux dans des fenêtres écriture comptable

Les axes principaux sont toujours définis et nommés par la société\-. Pour visualiser les axes principaux de votre société, ouvrez la page **Paramètres comptabilité**.  

Dans une page écriture comptable, vous pouvez voir si des axes principaux sont associés à des écritures. Les deux axes principaux sont différents des autres axes car vous pouvez les utiliser en tant que filtres n’importe où dans [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, choisissez l’action **Écritures comptables**.  
3. Pour ne visualiser que certaines écritures, positionnez au moins un filtre sur la page.  
4. Pour visualiser tous les axes d’une écriture, sélectionnez l’écriture, puis cliquez sur **Axes analytiques**.  

> [!NOTE]  
> La page **Analytique - Écritures comptables** affiche les axes d’une écriture comptable à la fois. Lorsque vous faites défiler les écritures comptables, le contenu de la page **Analytique - Écritures comptables** est modifié en conséquence.

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Veille économique](bi.md)  
[Finances](finance.md)  
[Analyse des données par axe analytique](bi-how-analyze-data-dimension.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]