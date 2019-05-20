---
title: Utiliser les axes analytiques| Microsoft Docs
description: Utilisez les axes analytiques pour classer des écritures par catégorie, par exemple, par service ou le projet, afin de facilement suivre et analyser les données.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9072bd45d5189ec42e8f1adaa3554fa182c36f1f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244737"
---
# <a name="working-with-dimensions"></a>Utilisation des axes analytiques
Vous pouvez utiliser des axes analytiques pour faciliter l'exécution de l'analyse sur des commandes vente, par exemple. Les axes analytiques sont des attributs et des valeurs qui permettent de catégoriser les écritures afin de pouvoir les suivre et les analyser. Ils peuvent par exemple indiquer de quel projet ou département provient une écriture.  

Vous pouvez également utiliser des axes au lieu de configurer des comptes généraux séparés pour chaque département et projet. Cela donne une bonne opportunité d'analyse, sans créer de plan comptable complexe. Pour plus d'informations, reportez-vous à [Veille économique](bi.md).

Un autre exemple consiste à configurer un axe analytique appelé *Département* et utiliser cet axe lorsque vous validez des documents vente. Cela vous permet d'utiliser les outils de veille économique pour savoir quel département a vendu quels articles.
Plus vous utilisez d'axes analytiques, plus vous pouvez baser vos décisions commerciales sur des états détaillés. Par exemple, une seule écriture vente peut comporter plusieurs informations analytiques :  

* Le compte sur lequel la vente de l'article a été validée  
* L'endroit où l'article a été vendu
* Le nom du vendeur
* Le type de client qui a effectué l'achat  

## <a name="analyzing-by-dimensions"></a>Analyse par axe analytique
La fonctionnalité Axes analytiques joue un rôle important dans la veille économique, par exemple en définissant des vues d'analyse. Pour plus d'informations, reportez vous à [Analyser des données par axe analytique](bi-how-analyze-data-dimension.md).

> [!TIP]
> Pour analyser rapidement les données transactionnelles par dimensions, vous pouvez filtrer les totaux du plan comptable et les entrées de toutes les pages **Entrées** par dimensions. Recherchez l'action **Définir le filtre axe**.

## <a name="dimension-sets"></a>Ensembles de dimensions
Un ensemble de dimensions est une combinaison unique de sections analytiques. Il est stocké comme des écritures de l'ensemble de dimensions dans la base de données. Chaque écriture de l'ensemble de dimensions représente une section analytique unique. L'ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l'ensemble de dimensions.  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d'enregistrer explicitement chaque section analytique dans la base de données, un ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document pour spécifier l'ensemble de dimensions.  

## <a name="setting-up-dimensions"></a>Configuration d'axes
Vous pouvez définir les axes et les sections analytiques pour classer des feuilles et des documents par catégorie, comme des commandes vente et achat. La page **Axes analytiques** permet de créer une ligne pour chaque axe, par exemple *Projet*, *Département*, *Zone* et *Commercial*.

Vous pouvez également définir des valeurs pour des axes. Il peut par exemple s'agir de départements de votre société. Les sections analytiques peuvent être paramétrées sous forme de structure hiérarchique similaire au plan comptable, de manière à ce que les données puissent être réparties en plusieurs niveaux de granularité et à ce que des sous-ensembles de sections analytiques puissent être totalisés. Vous pouvez définir autant d'axes et de sections analytiques que nécessaire, tous les membres de votre société peuvent les utiliser.

Lorsque les axes et les valeurs sont configurées, vous pouvez définir les axes principaux et des raccourcis axe sur la page **Paramètres comptabilité** qui seront toujours disponibles pour sélection comme champs sur les lignes feuille et document, sans avoir à ouvrir la page **Axes analytiques** en premier lieu. Pour plus d'informations, reportez-vous à la rubrique [Configurer les axes principaux et les raccourcis axe](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* Les **axes principaux** sont utilisés comme filtres, dans les états et les traitements par lots. Vous pouvez uniquement utiliser deux axes principaux, choisissez donc des axes que vous utilisez souvent.
* Les **raccourcis axe** sont disponibles sous forme de champ dans les lignes feuille et document. Vous pouvez en créer six au maximum.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Pour configurer des axes analytiques par défaut pour les clients, les fournisseurs et d'autres comptes
Vous pouvez attribuer un axe analytique par défaut pour un compte spécifique. L'axe est copié sur la feuille ou le document lorsque vous saisissez le numéro de compte dans une ligne, mais vous pouvez supprimer ou modifier le code sur la ligne si nécessaire. Vous pouvez également rendre un axe analytique obligatoire pour valider une écriture avec un type de compte spécifique.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Dimensions**, puis choisissez le lien associé.  
2.  Sur la page **Axes analytiques** sélectionnez l'axe approprié, puis cliquez sur **Affectations par type compte**.  
4.  Complétez une ligne pour chaque nouvelle affectation analytique à configurer. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Si vous souhaitez rendre un axe requis sans lui affecter de section analytique par défaut, ne renseignez pas le champ **Code section**, puis sélectionnez **Code obligatoire** dans le champ **Contrôle validation**.  

> [!WARNING]  
>  Si un compte doit être utilisé dans le traitement par lots **Ajuster taux de change** ou **Valider coûts ajustés**, ne sélectionnez pas **Code obligatoire** ni **Même code**. Ces traitements par lots ne peuvent pas utiliser de codes axe.  

> [!NOTE]  
>  Si une affectation différente de l'affectation analytique configurée pour ce type de compte doit être associée à un compte, vous devez paramétrer une affectation analytique pour ce compte. L'affectation analytique de ce compte remplace alors celle du type de compte.  

### <a name="to-set-up-default-dimension-priorities"></a>Pour configurer des affectations analytiques prioritaires  
Des types de compte différents, tels qu'un compte client et un compte article, peuvent avoir des affectations analytiques différentes. Par conséquent, plusieurs affectations analytiques peuvent être proposées pour un axe dans une écriture. Pour éviter de tels conflits, vous pouvez appliquer des règles de priorité aux différentes sources.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Affect. analytique prioritaire**, puis sélectionnez le lien associé.  
2.  Sur la page **Affect. analytique prioritaire**, dans le champ **Code journal,** entrez le code journal pour la table séquence à laquelle les affectations analytiques prioritaires s'appliquent.  
3.  Complétez une ligne pour chaque affectation analytique prioritaire souhaitée pour le code journal sélectionné.
4.  Répétez la procédure pour chaque code journal pour lequel vous souhaitez configurer des affectations analytiques prioritaires.  

> [!IMPORTANT]  
>  Si vous configurez deux tables avec la même priorité pour le même code journal, [!INCLUDE[d365fin](includes/d365fin_md.md)] sélectionne la table ayant le plus petit ID.  

### <a name="to-set-up-dimension-combinations"></a>Pour configurer des croisements analytiques  
Pour éviter de valider des écritures avec des axes contradictoires ou inappropriés, vous pouvez bloquer ou limiter des croisements spécifiques de deux axes. Lorsqu'un croisement analytique est bloqué, vous ne pouvez pas valider les deux axes sur la même écriture, quelles que soient les sections analytiques. Lorsqu'un croisement analytique est limité, vous pouvez valider les deux axes sur la même écriture, mais uniquement pour certains croisements de sections analytiques.

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Croisements d'axes**, puis choisissez le lien associé.  
2.  Sur la page **Croisements d'axes**, sélectionnez le champ du croisement analytique et sélectionnez l'une des options suivantes.  

    |Champ|Désignation|
    |----------------------------------|---------------------------------------|  
    |**Aucune limite**|Ce croisement analytique n'a pas de restrictions. Toutes les sections analytiques sont autorisées.|  
    |**Limité**|Ce croisement analytique a des restrictions selon les sections analytiques que vous entrez. Vous devez définir ces limites sur la page **Croisement section**.|  
    |**Bloqué**|Ce croisement analytique n'est pas autorisé.|  

3.  Si vous avez sélectionné l'option **Limité**, vous devez définir les croisements de sections analytiques bloqués. Pour cela, sélectionnez le champ pour définir le croisement d'axe.  
4.  Sélectionnez à présent le croisement de sections analytiques bloqué et entrez **Bloqué** dans le champ. Un champ blanc signifie que le croisement de sections est autorisé. Répétez cette procédure si plusieurs croisements sont bloqués.  

> [!NOTE]  
>  Les mêmes axes s'affichent à la fois dans les lignes et les colonnes et, par conséquent, tous les croisements analytiques apparaissent deux fois. [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche automatiquement le paramètre dans les deux champs. Vous ne pouvez rien sélectionner dans les champs situés dans le coin supérieur gauche et en bas car ces champs ont le même axe de ligne et de colonne.  
>   
>  L'option sélectionnée s'affiche uniquement lorsque vous quittez le champ.  
>   
>  Pour visualiser le nom des axes à la place du code, sélectionnez le champ **Afficher nom colonne**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Pour configurer des axes principaux et des raccourcis axe
Les axes principaux et les raccourcis axe peuvent être utilisés comme filtre n'importe où dans [!INCLUDE[d365fin](includes/d365fin_md.md)], y compris sur les états, les traitements par lot et les vues d'analyse. Les axes principaux et les raccourcis axe sont toujours disponibles pour être insérés directement sans ouvrir tout d'abord la page **Axes analytiques**. Sur les lignes feuille et document, vous pouvez sélectionner les axes principaux et les raccourcis axe dans un champ sur la ligne. Vous pouvez définir deux axes principaux et huit raccourcis axe. Sélectionnez les axes que vous utilisez le plus souvent.

> [!Important]  
> Le fait de modifier un axe principal ou un raccourci axe exige que toutes les écritures saisies avec l'axe soient mises à jour. Vous pouvez exécuter cette tâche avec la fonction **Modifier les axes principaux**, mais cela peut se révéler chronophage et peut avoir un impact sur les performances. Par conséquent, sélectionnez vos axes principaux et vos raccourcis axe avec soin afin que vous n'ayez pas à les changer ultérieurement.

> [!Note]
> Lorsque vous ajoutez ou modifiez un axe principal ou un raccourci axe, vous êtes automatiquement déconnecté et la nouvelle valeur est préparée pour un usage dans toute l'application.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres comptabilité**, puis sélectionnez le lien associé.
2. Sur le raccourci **Axes analytiques**, renseignez les champs. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Pour modifier les axes principaux
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modifier les axes principaux**, puis sélectionnez le lien associé.
2. Passez votre souris sur les actions et les champs sur la page pour découvrir comment modifier les axes principaux et les raccourcis axe.

### <a name="example-of-dimension-setup"></a>Exemple de paramétrage d'axe analytique
Imaginons que votre société souhaite suivre les transactions selon la structure organisationnelle et les situations géographiques. Pour ce faire, vous pouvez configurer deux axes sur la page **Axe analytique** :

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

Pour les deux zones géographiques principales, Amériques et Europe, ajoutez des sous-catégories pour les régions en mettant les sections analytiques en retrait. Cela vous permet de déclarer les ventes ou les dépenses dans les régions, et d'obtenir les totaux des zones géographiques plus étendues. Vous pouvez également choisir d'utiliser les pays ou les régions en tant que sections analytiques, ou des régions ou des villes, en fonction de votre entreprise.

> [!NOTE]  
>   Pour configurer une hiérarchie, veillez à trier les codes dans l'ordre alphabétique. Ceci inclut les codes des sections analytiques fournis dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Pour **DÉPARTEMENT**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Name | Type section |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| FABR |Fabrication |Standard |
| VENTES |Ventes |Standard |

Avec ce paramétrage, vous pouvez ensuite ajouter les deux axes en tant qu'axes analytiques principaux sur la page **Paramètres comptabilité**. Cela signifie que vous pouvez utiliser ZONE et DÉPARTEMENT comme filtres pour les écritures comptables de la comptabilité, ainsi que dans tous les états et les tableaux d'analyse. Les deux axes principaux sont mis à disposition automatiquement pour être utilisés dans les lignes écriture et les en-têtes document comme raccourcis axe.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Affichage d'un aperçu des axes utilisés plusieurs fois
La page **Aff. analytiques - Multiples** spécifie la manière dont un groupe de comptes utilise les axes et sections analytiques. Vous pouvez effectuer cette opération en sélectionnant plusieurs comptes, et en spécifiant des axes et sections analytiques par défaut pour tous les comptes sélectionnés dans la liste des comptes. Lorsque vous spécifiez des affectations analytiques pour les comptes sélectionnés, le programme propose ces axes et sections analytiques à chaque fois que l'un de ces comptes est utilisé, par exemple sur une ligne feuille. La validation des écritures est ainsi facilitée, car les champs des axes analytiques sont renseignés automatiquement. Cependant, les sections analytiques proposés peuvent être modifiées, par exemple sur une ligne feuille.

La page **Aff. analytiques - Multiples** contient les champs suivants :

|Champ|Désignation|
|-----|-----------|  
|**Code axe analytique**|Affiche tous les axes définis comme affectations analytiques sur un ou plusieurs comptes sélectionnés. Si vous cliquez sur le champ, vous pouvez visualiser la liste de tous les axes analytiques disponibles. Si vous sélectionnez un axe, l'axe sélectionné est défini comme affectation analytique pour tous les comptes sélectionnés.|
|**Code section**|Affiche une section analytique ou le terme (Conflit). Si le champ indique une section analytique, tous les comptes sélectionnés ont la même section analytique par défaut pour un axe donné. Si le champ indique le terme (Conflit), les comptes sélectionnés n'ont pas tous la même section analytique par défaut pour un axe donné. Si vous cliquez sur le champ, vous pouvez visualiser la liste de toutes les sections analytiques disponibles pour un axe donné. Si vous sélectionnez une section analytique, la section sélectionnée est définie comme section par défaut pour tous les comptes sélectionnés.|
|**Contrôle validation**|Affiche une règle de contrôle validation ou le terme (Conflit). Si le champ indique une règle de contrôle validation, tous les comptes sélectionnés ont la même règle pour une section analytique donnée. Si le champ indique le terme (Conflit), les comptes sélectionnés n'ont pas tous la même règle de contrôle validation pour une section analytique donnée. Si vous cliquez sur le champ Contrôle validation, vous pouvez visualiser la liste des règles de contrôle validation. Si vous sélectionnez une règle de contrôle validation, la règle de contrôle validation sélectionnée s'applique à tous les comptes sélectionnés.|

## <a name="using-dimensions"></a>Utilisation des axes analytiques
Dans un document tel qu'une commande vente, vous pouvez ajouter des informations analytiques pour une seule ligne document et pour le document lui-même. Par exemple, sur la page **Commande vente**, vous pouvez saisir des sections analytiques pour les deux premiers raccourcis axe directement sur les lignes vente individuelles et ajouter des informations analytiques complémentaires si vous cliquez sur le bouton **Axes analytiques**.  

Si vous travaillez plutôt sur une feuille, vous pouvez également ajouter à une écriture des informations analytiques de la même manière, si vous avez configuré des raccourcis axe en tant que champs directement dans les lignes feuille.  

Vous pouvez configurer des axes analytiques par défaut pour des comptes ou des types de compte, de sorte que les axes et les sections analytiques soient renseignés automatiquement.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Pour afficher les axes principaux dans des fenêtres écriture comptable  
Les axes principaux sont toujours définis et nommés par la société\-. Pour visualiser les axes principaux de votre société, ouvrez la page **Paramètres comptabilité**.  

Dans une page écriture comptable, vous pouvez voir si des axes principaux sont associés à des écritures. Les deux axes principaux sont différents des autres axes car vous pouvez les utiliser en tant que filtres n'importe où dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Plan comptable**, puis sélectionnez le lien associé.  
2.  Sur la page **Plan comptable**, choisissez l'action **Écritures comptables**.  
3.  Pour ne visualiser que certaines écritures, positionnez au moins un filtre sur la page.  
4.  Pour visualiser tous les axes d'une écriture, sélectionnez l'écriture, puis cliquez sur **Axes analytiques**.  

> [!NOTE]  
>  La page **Analytique - Écritures comptables** affiche les axes d'une écriture comptable à la fois. Lorsque vous faites défiler les écritures comptables, le contenu de la page **Analytique - Écritures comptables** est modifié en conséquence.

## <a name="troubleshooting-dimensions-errors"></a>Résolution des erreurs liées aux axes analytiques
Lorsque vous validez des documents ou des lignes feuille qui contiennent des axes analytiques, différentes erreurs peuvent survenir, généralement liées à un défaut de configuration ou d'affectation des axes.

> [!NOTE]
> Dans la liste suivante des messages d'erreur potentielle, les codes *%X*sont des espaces réservés pour les variables de données qui le message réel contient dans l'interface utilisateur selon le contexte. Par exemple, *%1 %2 est bloqué.* pourrait s'afficher dans l'interface utilisateur comme « La ZONE du code axe est bloquée ».  

|Problème|Message d'erreur|Solution possible|
|-----|-------------|-----------------|
|Axe bloqué|%1 %2 est bloqué.|- Recherchez les documents non validés contenant l'ensemble de dimensions avec l'axe bloqué et débloquez-le.<br />- Supprimez la ligne ensemble de dimensions pour l'axe bloqué.|
|Axe supprimé|%1 %2 est introuvable.|- Restaurez l'axe manquant.<br />- Recherchez les documents non validés contenant l'ensemble de dimensions avec l'axe manquant et ajoutez-le.<br />- Supprimez la ligne ensemble de dimensions pour l'axe manquant.|
|Valeur de l'axe bloqué|%1 %2 - %3 est bloqué.|- Recherchez les documents non validés contenant l'ensemble de dimensions avec la valeur de l'axe bloqué et débloquez-le.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l'axe bloqué.|
|Valeur de l'axe supprimé|   %1 pour %2 est manquant.|- Restaurez la valeur de l'axe manquant.<br />- Recherchez les documents non validés contenant l'ensemble d'axes avec la valeur de l'axe manquant et ajoutez-le.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l'axe manquant.|
|Valeur de l'axe rejeté|Le type de valeur de l'axe pour %1 %2 - %3 ne doit pas être %4.|- Modifiez le champ **Type de valeur de l'axe** sur la page **Valeurs de l'axe** avec **Standard** ou **Début total**.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l'axe bloqué.|
|Croisement analytique bloqué|Les axes analytiques %1 et %2 ne peuvent pas être utilisés ensemble.|- Recherchez les documents non validés contenant l'ensemble de dimensions avec la valeur du croisement analytique bloqué et débloquez-le.<br />- Modifiez une des lignes d'ensembles d'autorisation en conflit pour le croisement analytique.|
|Croisement valeur analytique bloquée|Les croisements analytiques %1 - %2 et %3 - %4 ne peuvent pas être utilisés ensemble.|- Recherchez les documents non validés contenant l'ensemble de dimensions avec la valeur du croisement analytique bloqué et débloquez-le.<br />- Modifiez une des lignes d'ensembles d'autorisation en conflit pour le croisement de la valeur analytique.|
|Code de valeur analytique vierge pour l'axe par défaut où le champ **Contrôle validation** contient **Code obligatoire**|- Sélectionnez un %1 pour le %2 %3.<br />- Sélectionnez un %1 pour le %2 %3 pour %4 %5.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez une valeur analytique non vierge pour l'axe analytique en conflit dans l'ensemble d'axes.|
|Code de valeur analytique erroné pour l'axe par défaut où le champ **Contrôle validation** contient **Code identique**|- Sélectionnez %1 %2 pour le %3 %4.<br />- Sélectionnez %1 %2 pour le %3 %4 pour %5 %6.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez la valeur analytique requise pour l'axe analytique en conflit dans l'ensemble de dimensions.|
|Code de valeur analytique non vierge pour l'axe par défaut vierge où le champ **Contrôle validation** contient **Code identique**|-%1 %2 doit être vierge.<br />-%1 %2 doit être vierge pour %3 %4.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez un code de valeur analytique vierge pour l'axe analytique en conflit dans l'ensemble d'axes.|
|Valeur analytique inattendue pour l'axe par défaut où le champ **Contrôle validation** contient **Aucun code**|-%1 %2 ne doit pas être mentionné.<br />- %1 %2 ne doit pas être mentionné pour %3 %4.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Supprimez la ligne en conflit depuis l'ensemble de dimensions.|

## <a name="see-also"></a>Voir aussi
[Veille économique](bi.md)  
[Finances](finance.md)  
[Analyse des données par axe analytique](bi-how-analyze-data-dimension.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
