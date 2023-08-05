---
title: Utilisation des axes analytiques pour suivre et analyser les données
description: 'Utilisez les axes analytiques pour classer des écritures par catégorie, comme par service ou projet, afin de plus facilement suivre et analyser les données pour vous aider à prendre les bonnes décisions commerciales.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# Utiliser les axes analytiques

Les axes analytiques sont des valeurs qui permettent de catégoriser les écritures afin de pouvoir les suivre et les analyser sur les documents, tels que les commandes vente. Ils peuvent par exemple indiquer de quel projet ou département provient une écriture.  

Ainsi, au lieu de configurer des comptes généraux distincts pour chaque service et projet, vous pouvez utiliser les axes analytiques comme base d’analyse et éviter d’avoir à créer un plan comptable compliqué. Pour plus d’informations, consultez [Veille économique](bi.md).

Un autre exemple consiste à configurer un axe analytique appelé *Département* et utiliser cet axe lorsque vous validez des documents vente. Cela vous permet d’utiliser les outils de veille économique pour savoir quel département a vendu quels articles. Plus vous utilisez d’axes analytiques, plus vos décisions commerciales sont basées sur des états détaillés. En fait, une seule écriture vente peut comporter des informations depuis plusieurs axes analytiques :  

* Le compte sur lequel la vente de l’article a été validée.  
* L’endroit où l’article a été vendu.
* Le nom du vendeur.
* Le nom du client qui l’a acheté.

## Analyse par axe analytique

La fonctionnalité Axes analytiques joue un rôle important dans la veille économique, par exemple en définissant des vues d’analyse. Pour plus d’informations, consultez [Analyse des données par axe analytique](bi-how-analyze-data-dimension.md).

> [!TIP]
> Pour analyser rapidement les données transactionnelles par dimensions, vous pouvez filtrer les totaux du plan comptable et les entrées de toutes les pages **Définir le filtre axe** par axes analytiques.

> [!NOTE]
> Les vues d′analyse utilisent souvent les données des axes analytiques. Si vous découvrez qu’une dimension incorrecte a été utilisée sur les écritures comptables comptabilisées, vous pouvez corriger les valeurs d’axe analytique et mettre à jour vos vues d’analyse. Cela vous aide à garder vos états et analyses financiers exacts. Pour plus d’informations, consultez [Dépannage et correction des axes analytiques](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Ensembles d’axes analytiques

Un ensemble de dimensions est une combinaison unique de sections analytiques. Elles sont stockées comme des écritures de l’ensemble d’axes analytiques dans la base de données. Chaque écriture de l’ensemble de dimensions représente une section analytique unique. De plus, chaque ensemble d’axes analytiques et l’entrée d’ensemble d’axes analytiques qu’il contient sont identifiés par un ID d’ensemble d’axes analytiques commun.  

Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques. Au lieu d’enregistrer explicitement chaque section analytique dans la base de données, un ID d’ensemble de dimensions est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document pour spécifier l’ensemble de dimensions.  

## Configuration d’axes analytiques

Vous pouvez définir les axes et les sections analytiques pour classer des feuilles et des documents par catégorie, comme des commandes vente et achat. La page **Axes analytiques** permet de créer une ligne pour chaque axe, par exemple *Projet*, *Département*, *Zone* et *Commercial*.

Vous pouvez également définir des valeurs pour des axes. Disons que les valeurs représentent les départements de votre entreprise. Les valeurs d’axe analytique peuvent être configurées selon une structure hiérarchique similaire au plan comptable. Cela signifie que les données peuvent être décomposées en différents niveaux de granularité et que des sous-ensembles de valeurs d’axes analytiques peuvent être totalisés. Vous pouvez définir autant d’axes et de sections analytiques que nécessaire, tous les membres de votre société peuvent les utiliser.

Une fois les axes analytiques et les valeurs configurés, vous pouvez définit des axes analytiques globaux et de raccourci sur la page **Paramètres comptabilité**. Ces axes analytiques sont alors toujours disponibles pour que vous puissiez les sélectionner en tant que champs sur les lignes de journal et de document ainsi que sur les écritures comptables, sans ouvrir au préalable la page **Axes analytiques**. Pour plus d’informations, consultez la section [Configurer les axes analytiques globaux et de raccourci](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* Les **Axes principaux** sont utilisés comme filtres, par exemple, dans les états, les traitements par lots et les XMLports. Vous pouvez uniquement utiliser deux axes principaux, choisissez donc des axes que vous utilisez souvent.
* Les **Raccourcis axe** sont disponibles sous forme de champ dans les lignes feuille et document et les écritures comptables. Vous pouvez en créer huit au maximum.  

> [!NOTE]
> Après avoir utilisé une nouvelle dimension dans une écriture, telle qu’une ligne ou un nouvel enregistrement, vous ne pouvez pas supprimer la dimension, même si vous ne validez pas l’entrée. Ceci est dû au fait que [!INCLUDE[prod_short](includes/prod_short.md)] crée immédiatement un ensemble de dimensions pour la ligne ou l’enregistrement. Pour plus d’informations, consultez la section [Ensembles d’axes analytiques](finance-dimensions.md#dimension-sets).

### Pour configurer des axes analytiques par défaut pour les clients, les fournisseurs et d’autres comptes

Vous pouvez attribuer un axe analytique par défaut pour un compte spécifique. L’axe est copié sur la feuille ou le document lorsque vous saisissez le numéro de compte dans une ligne, mais vous pouvez supprimer ou modifier le code sur la ligne si nécessaire. Vous pouvez également rendre un axe analytique obligatoire pour valider une écriture avec un type de compte spécifique. > 

> [!NOTE]
> Les priorités d’axe analytique par défaut s’ouvrent pour des scénarios de vente et d’achat auxquels vous souhaiterez peut-être accorder une attention particulière. Lorsque vous utilisez les priorités d’axe analytique par défaut sur des documents de vente et d’achat, [!INCLUDE [prod_short](includes/prod_short.md)] considère toujours les axes analytiques dans l’en-tête comme provenant du client ou du fournisseur. Cela est vrai pour les axes analytiques que vous définissez manuellement ou par défaut, et est particulièrement pertinent lorsque vous utilisez des axes analytiques par défaut sur des magasins et des articles, mais pas sur des clients ou des fournisseurs.
>
> **Exemple :**
>
> Vous avez un scénario avec les paramètres d’axe analytique suivants :
>
> * Un client sans axes analytiques par défaut
> * Un article avec ADM comme valeur de dimension pour l’axe analytique DÉPARTEMENT
> * Un magasin avec PROD comme valeur de dimension pour l’axe analytique DÉPARTEMENT
> * Les priorités d’axe analytique par défaut sont définies sur Client > Article > Magasin
>
> Lorsque vous créez un nouveau document dans ce scénario, les axes analytiques sont utilisés comme suit :
>
> * Si vous créez un document et ajoutez un magasin, la valeur par défaut pour les nouvelles lignes sera PROD. Lorsque vous ajoutez des lignes avec des articles, [!INCLUDE [prod_short](includes/prod_short.md)] conservera PROD car il provient de l’en-tête du document.
>
> * Si vous créez un document et ajoutez des articles qui ont la valeur d’axe analytique ADM, puis spécifiez un magasin dans l’en-tête du document, [!INCLUDE [prod_short](includes/prod_short.md)] vous demandera si vous souhaitez écraser les lignes existantes en raison d’un conflit.
>
> Nous vous recommandons de tester la configuration de vos axes analytiques par défaut, les priorités d’axe analytique et l’ordre dans lequel vous saisissez les données dans les documents.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Axes analytiques**, puis sélectionnez le lien associé.  
2. Sur la page **Axes analytiques** sélectionnez l’axe approprié, puis sélectionnez l’action **Affectations par type compte**.  
3. Complétez une ligne pour chaque nouvel axe analytique à configurer. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Si vous souhaitez rendre un axe obligatoire sans lui affecter de valeur par défaut, ne renseignez pas le champ **Code section**, puis sélectionnez **Code obligatoire** dans le champ **Contrôle validation**.  

> [!WARNING]  
> Si un compte doit être utilisé dans un traitement par lots **Ajuster taux de change** ou **Valider coûts ajustés**, ne sélectionnez pas **Code obligatoire** ni **Même code**. Ces traitements par lots ne peuvent pas utiliser de codes axe.  

> [!NOTE]  
> Si un compte doit avoir un axe analytique différent de l’axe analytique par défaut affecté à ce type de compte, vous devez paramétrer un nouvel axe analytique pour ce compte. L’affectation analytique de ce compte remplace alors celle du type de compte.  

### Pour configurer des affectations analytiques prioritaires

Des types de compte différents, tels qu’un compte client et un compte article, peuvent avoir des axes analytiques différents. Par conséquent, une écriture peut avoir plusieurs axes analytiques proposés par défaut. Pour éviter de tels conflits, vous pouvez appliquer des règles de priorité aux différentes sources.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Affect. analytique prioritaire**, puis sélectionnez le lien associé.  
2. Sur la page **Affect. analytique prioritaire**, dans le champ **Code journal,** entrez le code journal pour la table séquence à laquelle les affectations analytiques prioritaires s’appliquent.  
3. Complétez une ligne pour chaque affectation analytique prioritaire souhaitée pour le code journal sélectionné.
4. Répétez la procédure pour chaque code journal pour lequel vous souhaitez configurer des affectations analytiques prioritaires.  

> [!IMPORTANT]  
> Si vous configurez deux tables avec la même priorité pour le même code journal, [!INCLUDE[prod_short](includes/prod_short.md)] sélectionne toujours la table ayant le plus petit ID.  

### Pour configurer des croisements analytiques

Pour éviter de valider des écritures avec des axes contradictoires ou inappropriés, vous pouvez bloquer ou limiter des croisements spécifiques de deux axes. Lorsqu’un croisement analytique est bloqué, vous ne pouvez pas valider les deux axes sur la même écriture, quelles que soient les sections analytiques. A contrario, lorsqu’un croisement analytique est limité, vous pouvez valider les deux axes sur la même écriture, mais uniquement pour certains croisements de sections analytiques.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Croisements analytiques**, puis sélectionnez le lien associé.  
2. Sur la page **Croisements d’axes**, sélectionnez le champ du croisement analytique souhaité parmi les options suivantes.  

    |Champ|Désignation|
    |----------------------------------|---------------------------------------|  
    |**Aucune limite**|Ce croisement analytique n’a pas de restrictions. Toutes les sections analytiques sont autorisées.|  
    |**Limité**|Ce croisement analytique a des restrictions selon les sections analytiques que vous entrez. Vous devez définir ces limites sur la page **Croisement section**.|  
    |**Bloqué**|Ce croisement analytique n’est pas autorisé.|  

3. Si vous avez sélectionné l’option **Limité**, vous devez définir les croisements de sections analytiques bloqués. Pour cela, sélectionnez le champ pour définir le croisement de sections.  
4. Sélectionnez à présent le croisement de sections analytiques bloqué et entrez **Bloqué** dans le champ. Un champ vide signifie que le croisement de sections est autorisé. Répétez cette procédure si plusieurs croisements sont bloqués.  

> [!NOTE]  
> Les mêmes axes s’affichent à la fois dans les lignes et les colonnes et, par conséquent, tous les croisements analytiques apparaissent deux fois. [!INCLUDE[prod_short](includes/prod_short.md)] affiche automatiquement le paramètre dans les deux champs. Vous ne pouvez rien sélectionner dans les champs situés dans le coin supérieur gauche et en bas car ces champs ont le même axe de ligne et de colonne.  
>
> L’option sélectionnée s’affiche uniquement lorsque vous quittez le champ.  
>
> Pour visualiser le nom des axes à la place du code, sélectionnez le champ **Afficher nom colonne**.

### Pour configurer des axes principaux et des raccourcis axe

Les axes principaux et les raccourcis axe peuvent être utilisés comme filtres dans [!INCLUDE[prod_short](includes/prod_short.md)], y compris sur les états, les traitements par lot, les pages d’écritures comptables et les vues d’analyse. Les axes principaux et les raccourcis axe peuvent toujours être insérés directement sans ouvrir tout d’abord la page **Axes analytiques**. Sur les lignes feuille et document, vous pouvez sélectionner les axes principaux et les raccourcis axe dans un champ sur la ligne. Vous pouvez définir deux axes principaux et huit raccourcis axe. Sélectionnez les axes que vous utilisez le plus souvent.

> [!IMPORTANT]
> Le fait de modifier un axe principal ou un raccourci axe exige que toutes les écritures saisies avec l’axe soient mises à jour. Pour modifier un axe analytique global, vous pouvez utiliser la fonction **Modifier les axes principaux**, mais cela peut se révéler chronophage et peut avoir un impact sur les performances et les tables peuvent être verrouillées lors de la mise à jour. Assurez-vous de sélectionner vos axes principaux et vos raccourcis axe avec soin afin que vous n’ayez pas à les changer ultérieurement. Pour modifier un axe analytique raccourci, utilisez l’action **Modifier les axes analytiques**.
>
> Pour plus d’informations, consultez la section [Pour modifier les axes principaux](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Lorsque vous ajoutez ou modifiez un axe principal ou un raccourci axe, vous êtes automatiquement déconnecté et la nouvelle valeur est préparée.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.
2. Sur le raccourci **Axes analytiques**, renseignez les champs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Pour modifier les axes principaux

Lorsque vous modifiez un axe principal ou un raccourci, toutes les écritures saisies avec cet axe sont mises à jour. Étant donné que ce processus peut prendre du temps et affecter les performances, deux modes différents sont fournis pour adapter le processus à la taille de la base de données.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.
2. Choisissez l’action **Modifier les axes principaux**.
3. En haut de la page, sélectionnez l’un des deux modes suivants pour exécuter le traitement par lots.

    |Option|Désignation|
    |-|-|
    |**Séquentiel**|(Par défaut) Le changement est effectué en une seule transaction en ramenant toutes les écritures aux axes qu’elles avaient avant le changement.<br /><br />Cette option est recommandée si la société a relativement peu d’écritures publiées, auquel cas le traitement par lots prend moins de temps pour s’effectuer. Le processus verrouille plusieurs tables et bloque les autres utilisateurs jusqu’à ce qu’il soit terminé. Notez qu’avec les grandes bases de données, le processus peut ne pas être en mesure de s’effectuer dans ce mode. Dans ce cas, utilisez l’option **Parallèle**.|
    |**Parallèle**|Le changement de dimension se produit dans plusieurs sessions d’arrière-plan et l’opération est divisée en plusieurs transactions. Pour utiliser cette option, activez le bouton bascule **Traitement parallèle**. <br /><br />Cette option est recommandée pour les grandes bases de données ou les sociétés ayant de nombreuses écritures publiées, car c’est ainsi que le processus prendra le moins de temps. Notez que dans ce mode, le processus de mise à jour ne démarrera pas s’il existe plusieurs sessions de base de données actives.|  

4. Dans les champs **Code Axe principal 1** et/ou **Code Axe principal 2**, entrez les nouveaux axes. Les axes actuels sont affichés en gris derrière les champs.
5. En fonction du mode, effectuez l’une des opérations suivantes :
    * Dans mode **Séquentiel**, choisissez l’action **Démarrer**.
    * Dans mode **Parallèle**, choisissez l’action **Préparer**.

    L’onglet **Écritures journal** contient des informations sur les axes à modifier.
6. Déconnectez-vous de [!INCLUDE[prod_short](includes/prod_short.md)], puis reconnectez-vous.
7. Choisissez l’action **Démarrer** pour commencer le traitement parallèle des changements d’axe.

### Exemple de paramétrage d’axe analytique

Imaginons que votre société souhaite suivre les transactions selon la structure organisationnelle et les situations géographiques. Pour ce faire, vous pouvez configurer deux axes sur la page **Axes analytiques** :

* **REGION**  
* **DEPARTEMENT**  

| Code | Name | Libellé code | Libellé filtre |
| --- | --- | --- | --- |
| REGION |Région |Zone de recouvrement |Filtre zone |
| DEPARTEMENT |Département |Code emplacement immo |Filtre département |

Pour **ZONE**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Nom | Type section analytique |
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

Pour les deux zones géographiques principales, Amériques et Europe, ajoutez des sous-catégories pour les régions en mettant les sections analytiques en retrait. Cela vous permet de déclarer les ventes ou les dépenses dans les régions, et d’obtenir les totaux des zones géographiques plus étendues. Vous pouvez également choisir d’utiliser les pays, les régions, les comtés ou les villes en tant que sections analytiques, en fonction de votre entreprise.

> [!NOTE]  
> Pour configurer une hiérarchie, veillez à trier les codes dans l’ordre alphabétique. Ceci inclut les codes des sections analytiques fournis dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Pour **DÉPARTEMENT**, vous pouvez ajouter les sections analytiques suivantes :

| Code | Nom | Type section analytique |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| FABR |Fabrication |Standard |
| VENTES |Ventes |Standard |

Avec ce paramétrage, vous pouvez ensuite ajouter les deux axes en tant qu’axes analytiques principaux sur la page **Paramètres comptabilité**. Cela signifie que vous pouvez utiliser ZONE et DÉPARTEMENT comme filtres pour les écritures comptables de la comptabilité, ainsi que dans tous les états. Les deux axes principaux sont mis à disposition automatiquement pour être utilisés dans les lignes écriture et les en-têtes document comme raccourcis axe.

## Affichage d’un aperçu des axes utilisés plusieurs fois

La page **Aff. analytiques - Multiples** spécifie la manière dont un groupe de comptes utilise les axes et sections analytiques. Vous pouvez configurer cela en mettant en surbrillance plusieurs comptes, puis en spécifiant les axes et les sections analytiques par défaut pour eux. Après cela, l’application suggère ces axes et sections analytiques chaque fois que l’un de ces comptes est utilisé, par exemple dans une ligne feuille. La validation des écritures est ainsi facilitée, car les champs des axes analytiques sont renseignés automatiquement. Notez toutefois que les sections analytiques proposées peuvent être modifiées, par exemple sur une ligne feuille.

La page **Aff. analytiques - Multiples** contient les champs suivants :

|Champ|Désignation|
|-----|-----------|  
|**Code axe analytique**|Affiche tous les axes définis comme axes par défaut sur un ou plusieurs comptes sélectionnés. Si vous sélectionnez ce champ, vous pouvez visualiser la liste de tous les axes analytiques disponibles. Si vous sélectionnez un axe, celui-ci est défini comme affectation analytique pour tous les comptes en surbrillance.|
|**Code section**|Affiche une section analytique ou le terme (Conflit). Si le champ indique une section analytique, tous les comptes sélectionnés ont la même section analytique par défaut pour un axe donné. Si le champ indique le terme (Conflit), les comptes sélectionnés n’ont pas tous la même section analytique par défaut pour un axe donné. Lorsque vous sélectionnez le champ **Code axe analytique**, vous voyez une liste de toutes les sections analytiques disponibles pour un axe donné. Si vous sélectionnez une section analytique, elle est définie comme section par défaut pour tous les comptes sélectionnés.|
|**Contrôle validation**|Affiche une règle de contrôle validation ou le terme (Conflit). Si le champ indique une règle de contrôle validation, tous les comptes sélectionnés ont la même règle pour une section analytique donnée. Si le champ indique le terme (Conflit), les comptes sélectionnés n’ont pas tous la même règle de contrôle validation pour une section analytique donnée. Lorsque vous sélectionnez le champ **Contrôle validation**, vous voyez la liste des règles de contrôle validation pour un axe. Si vous sélectionnez une règle de contrôle validation, elle s’applique à tous les comptes sélectionnés.|

## Utiliser des axes analytiques

Dans un document tel qu’une commande vente, vous pouvez ajouter des informations analytiques pour une seule ligne document et pour le document lui-même. Sur la page **Commande vente**, vous pouvez saisir des sections analytiques pour les deux premiers raccourcis axe directement sur les lignes vente individuelles et ajouter des informations analytiques complémentaires si vous cliquez sur le bouton **Axes analytiques**.  

Si vous travaillez plutôt sur une feuille, vous pouvez également ajouter à une écriture des informations analytiques de la même manière, si vous avez configuré des raccourcis axe en tant que champs directement dans les lignes feuille.  

Vous pouvez également configurer des axes analytiques par défaut pour des comptes ou des types de compte, de sorte que les axes et les sections analytiques soient renseignés automatiquement.

### Pour afficher les axes principaux dans des fenêtres écriture comptable

Les axes principaux sont toujours définis et nommés par la société. Pour visualiser les axes principaux de votre société, ouvrez la page **Paramètres comptabilité**.

Dans une page écriture comptable, vous pouvez voir si des axes principaux sont associés à des écritures. Les deux axes principaux sont différents des autres axes car vous pouvez les utiliser en tant que filtres n’importe où dans [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
2. Sur la page **Plan comptable**, choisissez l’action **Écritures comptables**.  
3. Pour ne visualiser que certaines écritures, positionnez au moins un filtre sur la page.  
4. Pour visualiser tous les axes d’une écriture, sélectionnez l’écriture, puis sélectionnez l’action **Axes analytiques**.  

> [!NOTE]  
> La page **Analytique - Écritures comptables** affiche les axes d’une écriture comptable à la fois. Lorsque vous faites défiler les écritures comptables, le contenu de la page **Analytique - Écritures comptables** est modifié en conséquence.

## Voir la [formation Microsoft](/training/modules/dimensions-dynamics-365-business-central/index) associée

## Voir aussi

[Veille économique](bi.md)  
[Finances](finance.md)  
[Analyse des données par axe analytique](bi-how-analyze-data-dimension.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
