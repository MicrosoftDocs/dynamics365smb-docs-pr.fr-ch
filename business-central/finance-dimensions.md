---
title: Utilisation des dimensions pour suivre et analyser facilement les données
description: Utilisez les axes analytiques pour classer des écritures par catégorie, par exemple, par service ou le projet, afin de facilement suivre et analyser les données pour vous aider à prendre les bonnes décisions commerciales.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: aa97686299648b81e68aef1a3701e0c32d73138a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774095"
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

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Pour configurer des axes analytiques par défaut pour les clients, les fournisseurs et d’autres comptes
Vous pouvez attribuer un axe analytique par défaut pour un compte spécifique. L’axe est copié sur la feuille ou le document lorsque vous saisissez le numéro de compte dans une ligne, mais vous pouvez supprimer ou modifier le code sur la ligne si nécessaire. Vous pouvez également rendre un axe analytique obligatoire pour valider une écriture avec un type de compte spécifique.  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Axes analytiques**, puis sélectionnez le lien associé.  
2.  Sur la page **Axes analytiques** sélectionnez l’axe approprié, puis cliquez sur **Affectations par type compte**.  
4.  Complétez une ligne pour chaque nouvelle affectation analytique à configurer. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Si vous souhaitez rendre un axe requis sans lui affecter de section analytique par défaut, ne renseignez pas le champ **Code section**, puis sélectionnez **Code obligatoire** dans le champ **Contrôle validation**.  

> [!WARNING]  
>  Si un compte doit être utilisé dans le traitement par lots **Ajuster taux de change** ou **Valider coûts ajustés**, ne sélectionnez pas **Code obligatoire** ni **Même code**. Ces traitements par lots ne peuvent pas utiliser de codes axe.  

> [!NOTE]  
>  Si une affectation différente de l’affectation analytique configurée pour ce type de compte doit être associée à un compte, vous devez paramétrer une affectation analytique pour ce compte. L’affectation analytique de ce compte remplace alors celle du type de compte.  

### <a name="to-set-up-default-dimension-priorities"></a>Pour configurer des affectations analytiques prioritaires  
Des types de compte différents, tels qu’un compte client et un compte article, peuvent avoir des affectations analytiques différentes. Par conséquent, plusieurs affectations analytiques peuvent être proposées pour un axe dans une écriture. Pour éviter de tels conflits, vous pouvez appliquer des règles de priorité aux différentes sources.  

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Affect. analytique prioritaire**, puis sélectionnez le lien associé.  
2.  Sur la page **Affect. analytique prioritaire**, dans le champ **Code journal,** entrez le code journal pour la table séquence à laquelle les affectations analytiques prioritaires s’appliquent.  
3.  Complétez une ligne pour chaque affectation analytique prioritaire souhaitée pour le code journal sélectionné.
4.  Répétez la procédure pour chaque code journal pour lequel vous souhaitez configurer des affectations analytiques prioritaires.  

> [!IMPORTANT]  
>  Si vous configurez deux tables avec la même priorité pour le même code journal, [!INCLUDE[prod_short](includes/prod_short.md)] sélectionne la table ayant le plus petit ID.  

### <a name="to-set-up-dimension-combinations"></a>Pour configurer des croisements analytiques  
Pour éviter de valider des écritures avec des axes contradictoires ou inappropriés, vous pouvez bloquer ou limiter des croisements spécifiques de deux axes. Lorsqu’un croisement analytique est bloqué, vous ne pouvez pas valider les deux axes sur la même écriture, quelles que soient les sections analytiques. Lorsqu’un croisement analytique est limité, vous pouvez valider les deux axes sur la même écriture, mais uniquement pour certains croisements de sections analytiques.

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Croisements d’axes**, puis sélectionnez le lien associé.  
2.  Sur la page **Croisements d’axes**, sélectionnez le champ du croisement analytique et sélectionnez l’une des options suivantes.  

    |Champ|Désignation|
    |----------------------------------|---------------------------------------|  
    |**Aucune limite**|Ce croisement analytique n’a pas de restrictions. Toutes les sections analytiques sont autorisées.|  
    |**Limité**|Ce croisement analytique a des restrictions selon les sections analytiques que vous entrez. Vous devez définir ces limites sur la page **Croisement section**.|  
    |**Bloqué**|Ce croisement analytique n’est pas autorisé.|  

3.  Si vous avez sélectionné l’option **Limité**, vous devez définir les croisements de sections analytiques bloqués. Pour cela, sélectionnez le champ pour définir le croisement d’axe.  
4.  Sélectionnez à présent le croisement de sections analytiques bloqué et entrez **Bloqué** dans le champ. Un champ blanc signifie que le croisement de sections est autorisé. Répétez cette procédure si plusieurs croisements sont bloqués.  

> [!NOTE]  
>  Les mêmes axes s’affichent à la fois dans les lignes et les colonnes et, par conséquent, tous les croisements analytiques apparaissent deux fois. [!INCLUDE[prod_short](includes/prod_short.md)] affiche automatiquement le paramètre dans les deux champs. Vous ne pouvez rien sélectionner dans les champs situés dans le coin supérieur gauche et en bas car ces champs ont le même axe de ligne et de colonne.  
>   
>  L’option sélectionnée s’affiche uniquement lorsque vous quittez le champ.  
>   
>  Pour visualiser le nom des axes à la place du code, sélectionnez le champ **Afficher nom colonne**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Pour configurer des axes principaux et des raccourcis axe
Les axes principaux et les raccourcis axe peuvent être utilisés comme filtres dans [!INCLUDE[prod_short](includes/prod_short.md)], y compris sur les états, les traitements par lot, les pages d’écritures comptables et les vues d’analyse. Les axes principaux et les raccourcis axe sont toujours disponibles pour être insérés directement sans ouvrir tout d’abord la page **Axes analytiques**. Sur les lignes feuille et document, vous pouvez sélectionner les axes principaux et les raccourcis axe dans un champ sur la ligne. Vous pouvez définir deux axes principaux et huit raccourcis axe. Sélectionnez les axes que vous utilisez le plus souvent.

> [!Important]  
> Le fait de modifier un axe principal ou un raccourci axe exige que toutes les écritures saisies avec l’axe soient mises à jour. Pour modifier un axe analytique global, utilisez la fonction **Modifier les axes principaux**, mais cela peut se révéler chronophage et peut avoir un impact sur les performances et les tables peuvent être verrouillées lors de la mise à jour. Par conséquent, sélectionnez vos axes principaux et vos raccourcis axe avec soin afin que vous n’ayez pas à les changer ultérieurement. Pour modifier un axe analytique raccourci, utilisez l’action **Modifier les axes analytiques**. <br /><br />
> Pour plus d’informations, voir [Pour modifier les axes principaux](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Lorsque vous ajoutez ou modifiez un axe principal ou un raccourci axe, vous êtes automatiquement déconnecté et la nouvelle valeur est préparée pour un usage.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres comptabilité**, puis sélectionnez le lien associé.
2. Sur le raccourci **Axes analytiques**, renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Pour modifier les axes principaux
Lorsque vous modifiez un axe principal ou un raccourci, toutes les écritures saisies avec l’axe en question sont mises à jour. Étant donné que ce processus peut prendre du temps et affecter les performances, deux modes différents sont fournis pour adapter le processus à la taille de la base de données.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres comptabilité**, puis sélectionnez le lien associé.
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
7. Déconnectez-vous de [!INCLUDE[prod_short](includes/prod_short.md)], puis reconnectez-vous.
8. Choisissez l’action **Démarrer** pour démarrer le traitement parallèle des changements d’axe. <!--is this also dependent on the mode?-->

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
>   Pour configurer une hiérarchie, veillez à trier les codes dans l’ordre alphabétique. Ceci inclut les codes des sections analytiques fournis dans [!INCLUDE[prod_short](includes/prod_short.md)].  

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

1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Plan comptable**, puis sélectionnez le lien associé.  
2.  Sur la page **Plan comptable**, choisissez l’action **Écritures comptables**.  
3.  Pour ne visualiser que certaines écritures, positionnez au moins un filtre sur la page.  
4.  Pour visualiser tous les axes d’une écriture, sélectionnez l’écriture, puis cliquez sur **Axes analytiques**.  

> [!NOTE]  
>  La page **Analytique - Écritures comptables** affiche les axes d’une écriture comptable à la fois. Lorsque vous faites défiler les écritures comptables, le contenu de la page **Analytique - Écritures comptables** est modifié en conséquence.

## <a name="troubleshooting-dimensions-errors"></a>Résolution des erreurs liées aux axes analytiques
Lorsque vous validez des documents ou des lignes feuille qui contiennent des axes analytiques, différentes erreurs peuvent survenir, généralement liées à un défaut de configuration ou d’affectation des axes.

> [!NOTE]
> Dans la liste suivante des messages d’erreur potentielle, les codes *%X* sont des espaces réservés pour les variables de données qui le message réel contient dans l’interface utilisateur selon le contexte. Par exemple, *%1 %2 est bloqué.* pourrait s’afficher dans l’interface utilisateur comme « La ZONE du code axe est bloquée ».  

|Problème|Message d’erreur|Solution possible|
|-----|-------------|-----------------|
|Axe bloqué|%1 %2 est bloqué.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec l’axe bloqué et débloquez-le.<br />- Supprimez la ligne ensemble de dimensions pour l’axe bloqué.|
|Axe supprimé|%1 %2 est introuvable.|- Restaurez l’axe manquant.<br />- Recherchez les documents non validés contenant l’ensemble de dimensions avec l’axe manquant et ajoutez-le.<br />- Supprimez la ligne ensemble de dimensions pour l’axe manquant.|
|Valeur de l’axe bloqué|%1 %2 - %3 est bloqué.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec la valeur de l’axe bloqué et débloquez-le.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l’axe bloqué.|
|Valeur de l’axe supprimé|    %1 pour %2 est manquant.|- Restaurez la valeur de l’axe manquant.<br />- Recherchez les documents non validés contenant l’ensemble d’axes avec la valeur de l’axe manquant et ajoutez-le.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l’axe manquant.|
|Valeur de l’axe rejeté|Le type de valeur de l’axe pour %1 %2 - %3 ne doit pas être %4.|- Modifiez le champ **Type de valeur de l’axe** sur la page **Valeurs de l’axe** avec **Standard** ou **Début total**.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l’axe bloqué.|
|Croisement analytique bloqué|Les axes analytiques %1 et %2 ne peuvent pas être utilisés ensemble.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec la valeur du croisement analytique bloqué et débloquez-le.<br />- Modifiez une des lignes d’ensembles d’autorisation en conflit pour le croisement analytique.|
|Croisement valeur analytique bloquée|Les croisements analytiques %1 - %2 et %3 - %4 ne peuvent pas être utilisés ensemble.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec la valeur du croisement analytique bloqué et débloquez-le.<br />- Modifiez une des lignes d’ensembles d’autorisation en conflit pour le croisement de la valeur analytique.|
|Code de valeur analytique vierge pour l’axe par défaut où le champ **Contrôle validation** contient **Code obligatoire**|- Sélectionnez un %1 pour le %2 %3.<br />- Sélectionnez un %1 pour le %2 %3 pour %4 %5.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez une valeur analytique non vierge pour l’axe analytique en conflit dans l’ensemble d’axes.|
|Code de valeur analytique erroné pour l’axe par défaut où le champ **Contrôle validation** contient **Code identique**|- Sélectionnez %1 %2 pour le %3 %4.<br />- Sélectionnez %1 %2 pour le %3 %4 pour %5 %6.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez la valeur analytique requise pour l’axe analytique en conflit dans l’ensemble de dimensions.|
|Code de valeur analytique non vierge pour l’axe par défaut vierge où le champ **Contrôle validation** contient **Code identique**|-%1 %2 doit être vierge.<br />-%1 %2 doit être vierge pour %3 %4.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez un code de valeur analytique vierge pour l’axe analytique en conflit dans l’ensemble d’axes.|
|Valeur analytique inattendue pour l’axe par défaut où le champ **Contrôle validation** contient **Aucun code**|-%1 %2 ne doit pas être mentionné.<br />-%1 %2 ne doit pas être mentionné pour %3 %4.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Supprimez la ligne en conflit depuis l’ensemble de dimensions.|
|Une correction d'axe analytique ne se termine pas correctement.||-Choisissez **Réinitialiser** pour rétablir la correction à un état brouillon. Cela réinitialise les modifications et vous pouvez réexécuter la correction.|

## <a name="changing-dimension-assignments-after-posting"></a>Modification des attributions d'axe analytique après la publication
Si vous découvrez qu'une dimension incorrecte a été utilisée sur les écritures comptables comptabilisées, vous pouvez corriger les valeurs d'axe analytique et mettre à jour vos vues d'analyse. Cela vous aidera à garder vos rapports et analyses financières exactes.

### <a name="setting-up-dimension-corrections"></a>Paramétrage des corrections des axes analytiques
Il y a deux choses à prendre en compte lors de la configuration des corrections d'axe analytique :

* Y a-t-il des axes analytiques que vous ne souhaitez pas permettre aux gens de changer ? Sur la page **Paramètres de correction d'axes analytiques**, spécifiez les axes analytiques que vous souhaitez bloquer pour les modifications.
* À qui souhaitez-vous autoriser le changement d'axes analytiques ? Pour autoriser les utilisateurs à apporter des modifications, attribuez l'autorisation **CORRECTION AXE D365** aux utilisateurs. Les autorisations leur permettent de créer des corrections d'axes analytiques, de les exécuter et de les annuler si nécessaire. Ils pourront également spécifier des axes analytiques bloqués. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Correction d’un axe analytique
Vous pouvez sélectionner manuellement une ou plusieurs écritures comptables ou utiliser des filtres pour sélectionner des séries d'entrées. Si nécessaire, vous pouvez également ajouter ou supprimer des axes analytiques. 

1. Pour démarrer une correction d'axes analytiques, utilisez l'une des pages suivantes :

* Sur la page **Comptabilité/Registre**, en sélectionnant un registre, puis en choisissant l'action **Corriger les axes analytiques**. Ceci lance une correction pour les entrées dans le registre sélectionné.
* Sur la page **Écritures comptables**, en choisissant l'action **Correction d'axes analytiques**. 

2. Dans le champ **Description**, entrez les informations sur la modification. D'autres personnes pourraient utiliser ces informations plus tard pour comprendre ce qui a été fait.
3. Sur le Raccourci **Écritures comptables sélectionnées**, choisissez les entrées appropriées.

> [!IMPORTANT]
> Lorsque vous modifiez une sélection, les valeurs du Raccourci **Modifications de correction d'axes analytiques** sont réinitialisées. Par conséquent, sélectionnez toujours les entrées avant de spécifier les changements de valeur d'axes analytiques.

   Le tableau suivant décrit les options.

   |Option  |Description  |
   |---------|---------|
   |Ajouter les écritures associées     |Ajoutez les écritures comptables qui sont dans le même registre comptable.|   
   |Ajouter par filtre     |Utilisez des critères de filtre lors de l'ajout d'écritures comptables.|
   |Sélection manuelle     |Sélectionnez des écritures comptables spécifiques.         |
   |Ajouter par axe analytique     |Filtrez les écritures comptables par axes analytiques.         |
   |Supprimer des écritures     |Désélectionnez des écritures comptables.         |
   |Gérer les critères de sélection     |Suivez le processus de sélection et annulez les sélections si nécessaire.         |

4. Sur le Raccourci **Modifications de correction d'axes analytiques**, choisissez l'axes analytiques que vous souhaitez modifier dans le champ **Code d'axes analytiques** et la nouvelle valeur dans le champ **Nouveau code de valeur d'axes analytiques**.
5. Pour valider que la correction, choisissez **Valider les changements d'axes analytiques**. Pour plus d'informations, consultez [Validation des corrections d'axes analytiques](finance-dimensions.md#validating-dimension-corrections).
6. Choisir **Exécuter**.

### <a name="validating-dimension-corrections"></a>Validation des corrections d'axes analytiques
Avant d'exécuter une correction, il est conseillé de la valider d'abord. La validation vérifie les restrictions sur la comptabilisation des valeurs pour les comptes généraux, les restrictions pour les axes analytiques et si les valeurs des axes analytiques sont bloquées. Lors de la validation, le statut de la correction est défini sur **Validation en cours**. Après avoir validé une correction, le résultat s'affiche dans le champ **Statut de validation**. Si des erreurs ont été trouvées, vous pouvez utiliser l'action **Afficher les erreurs** pour les enquêter. Après avoir corrigé une erreur, vous devez utiliser l'action **Rouvrir** pour exécuter la correction ou une nouvelle validation.

Vous pouvez soit exécuter une correction immédiatement, soit la planifier pour une exécution ultérieure. Si vous exécutez des corrections sur un jeu de données volumineux, nous vous recommandons de le planifier pour qu'il s'exécute en dehors des heures ouvrables. Pour plus d'informations, consultez [Corrections d'axes analytiques sur des jeux de données volumineux](finance-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Annuler une correction
Après avoir corrigé un axe analytique, si vous n'aimez pas ce que vous voyez, vous pouvez utiliser l'action **Annuler** pour réinitialiser la valeur précédente. Cependant, vous ne pouvez annuler que la correction la plus récente. Avant d'annuler une correction, vous pouvez valider les modifications que l'annulation apportera. Par exemple, cela est utile si les restrictions d'axes analytiques ont changé après la correction.

Si l'action Annuler n'est pas disponible, par exemple parce que vous avez effectué de nombreuses corrections, vous pouvez utiliser l'action **Copier dans le brouillon** pour démarrer une nouvelle correction pour les mêmes entrées.

### <a name="dimension-corrections-on-large-data-sets"></a>Corrections d'axes analytiques sur des jeux de données volumineux
Soyez prudent lorsque vous corrigez de grands ensembles d'entrées, par exemple, des ensembles comprenant plus de 10 000 entrées. Si vous le pouvez, nous vous recommandons d'utiliser les filtres pour exécuter les corrections sur des jeux de données plus petits. Il est également judicieux d'exécuter des corrections en dehors des heures normales de bureau. 

### <a name="using-analysis-views-with-dimension-corrections"></a>Utilisation des vues d'analyse avec des corrections d'axes analytiques
Si **Mise à jour sur la publication** est activé pour une vue d'analyse, [!INCLUDE[prod_short](includes/prod_short.md)] peut afficher la vue lorsque les documents et les journaux sont publiés. Vous pouvez également mettre à jour les vues avec ce paramètre activé avec les résultats des corrections d'axes analytiques. Pour ce faire, activez le bouton de basculement **Mettre à jour les vues d'analyse**. La mise à jour des vues d'analyse peut avoir un impact sur les performances, en particulier pour les grands jeux de données, c'est pourquoi nous vous recommandons de mettre à jour les vues d'analyse uniquement pour les petits jeux de données.  

### <a name="viewing-historical-dimension-corrections"></a>Affichage des corrections de axes analytiques historiques
Si une écriture comptable a été corrigée, vous pouvez étudier la modification en utilisant l'action **Historique des corrections d'axes analytiques**.

### <a name="handling-incomplete-corrections"></a>Traitement des corrections incomplètes
Si une correction ne se termine pas, un avertissement s'affiche sur la carte de correction. Si cela se produit, vous pouvez utiliser l'action **Réinitialiser** pour rétablir la correction à un statut de brouillon et annuler les modifications. Vous pouvez ensuite exécuter à nouveau la correction.

> [!NOTE]
> La réinitialisation d'une correction incomplète n'affectera pas les mises à jour des vues d'analyse, car celles-ci se produisent à la fin du processus de correction.

### <a name="using-cost-accounting-with-corrected-gl-entries"></a>Utilisation de la comptabilité analytique avec les écritures comptables corrigées
Une fois les axes analytiques corrigés, vos données pour la comptabilité analytique seront désynchronisées. La comptabilité analytique utilise des axes analytiques pour agréger les montants des centres de coûts et des coûts associés, et pour exécuter les répartitions de coûts. La modification des axes analytiques des écritures comptables signifiera probablement que vous réexécuterez vos modèles de comptabilité analytique. Que vous deviez simplement supprimer quelques registres de coûts et réexécuter les allocations, ou que vous deviez tout supprimer et réexécuter tous vos modèles, cela dépend des données qui ont été mises à jour et de la configuration de vos capacités de comptabilité analytique. Identifier où les corrections d'axes analytiques auront un impact sur la comptabilité analytique et où des mises à jour sont nécessaires est un processus manuel. [!INCLUDE[prod_short](includes/prod_short.md)] ne propose pas actuellement de moyen automatisé de le faire.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Finances](finance.md)  
[Analyse des données par axe analytique](bi-how-analyze-data-dimension.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]