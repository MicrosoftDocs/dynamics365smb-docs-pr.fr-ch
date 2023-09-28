---
title: Exécuter et imprimer des états
description: En savoir plus sur l’entrée d’un état dans une file d’attente de projets et la planification de son traitement à une date et à une heure spécifiques.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 09/09/2022
ms.author: jswymer
---
# Exécuter et imprimer des états

Un rapport rassemble des informations en fonction d’un ensemble spécifié de critères. Il organise et présente les informations dans un format facile à lire que vous pouvez imprimer ou enregistrer sous forme de fichier. Il existe de nombreux états accessibles tout au long de l’application. Les états fournissent généralement des informations relatives au contexte de la page où vous vous trouvez. Par exemple, la page **Client** comprend des états pour les 10 principaux clients et les statistiques de vente, et plus encore.

> [!NOTE]
> Les traitements par lots et les ports XML sont plus ou moins identiques aux états mais ils ont pour objectif d’exécuter un processus ou d’exporter des données. Par exemple, le traitement par lots **Créer des relances** crée des relances pour les clients avec des paiements échus. Cette rubrique fait référence surtout aux « états », mais des informations similaires s’appliquent aux traitements par lots et aux ports XML.

## Mise en route

Vous pouvez trouver les états sous l’onglet **États** sur les pages, listes et fiches sélectionnées ou utiliser la recherche ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"). pour rechercher des rapports par nom. Pour un aperçu des états intégrés que vous pouvez utiliser dans [!INCLUDE[prod_short](includes/prod_short.md)], triés par catégories, voir [États disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Lorsque vous choisissez un état, une page de demande s’affiche généralement avec un titre selon le nom de l’état pour vous permettre de définir plusieurs options et filtres qui déterminent les éléments à inclure dans l’état. Les sections suivantes expliquent comment utiliser la page de demande pour créer, afficher un aperçu et imprimer un état.

## <a name="SavedSettings"></a>Utilisation des valeurs par défaut – paramètres prédéfinis

La plupart des pages de demande incluent le champ **Utiliser les valeurs par défaut de**. Avec ce champ, vous pouvez sélectionner des paramètres prédéfinis pour l’état, qui définissent automatiquement les options et les filtres. Sélectionnez une entrée dans la liste déroulante, et vous verrez les options et les filtres sur la page de demande se modifier en conséquence.

L’entrée appelée **Options et filtres récemment utilisés** est toujours disponible. Cette entrée permet de faire en sorte que l’état utilise les options et les filtres qui ont été utilisés la dernière fois que vous l’avez exécuté.

Le champ **Utiliser les valeurs par défaut de** fournit un moyen rapide et fiable de générer de manière cohérente des états contenant les données correctes. Après avoir sélectionné une entrée, vous pouvez modifier les options et les filtres avant d’afficher un aperçu ou d’imprimer l’état. Vos modifications ne seront pas enregistrées dans l’entrée de paramètres prédéfinis que vous avez sélectionnée, mais elles seront sauvegardées dans l’entrée **Options et filtres récemment utilisés**.

> [!NOTE]
> Les paramètres prédéfinis sont généralement configurés et gérés par un administrateur. En savoir plus sur [Gérer les paramètres enregistrés pour les états et les traitements par lots](reports-saving-reusing-settings.md).

## Définition des données à inclure dans un état

Utilisez les champs sous **Options** et **Filtres** pour modifier ou limiter les informations que vous souhaitez dans l’état. Vous devez définir des filtres dans un état de la même manière que vous le faites sur des listes. Consultez la section [Filtrage](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Le raccourci **Filtrer** sur une page de demande d’état fournit une capacité de filtrage générique pour les états. Ces filtres sont optionnels.
>
> Certains états ignoreront ces filtres, ce qui signifie que quel que soit le filtre défini dans le raccourci **Filtre**, la sortie de l’état est identique. Il est impossible de fournir une liste des champs ignorés dans quels états, vous devez expérimenter avec des filtres lorsque vous les utiliserez.
>
> **Exemple** : Lorsque vous utilisez le traitement par lots **Créer relance**, un filtre pour le champ **Écritures comptables client** de **Niveau dernière relance émise** sera ignoré, car les filtres sont fixes pour ce traitement par lots.

## Affichage de l’aperçu d’un état

En affichant l’aperçu d’un état vous permet de voir à quoi il ressemblera avant de l’imprimer. L’aperçu n’est pas basé sur l’imprimante sélectionnée dans le champ **Imprimante** sur la page de demande. Il est contrôlé par le navigateur. Après l’aperçu, vous pouvez revenir à la page de la demande et apporter des modifications aux options et aux filtres si nécessaire.

Les choix d’aperçu sur la page **Demande d’état** dépendent de l’état. Ainsi, pour certains états, vous pouvez choisir **Aperçu**, tandis que pour d’autres, le choix est **Aperçu et fermer**. Les deux choix ouvrent un aperçu de l’état. La différence est que l’**Aperçu** garde la page de demande ouverte afin que vous puissiez y revenir, apporter des modifications, afficher à nouveau un aperçu ou imprimer. Au contraire, avec **Aperçu et fermer**, la page de demande se ferme, vous devrez donc rouvrir l’état pour apporter des modifications ou l’imprimer.

> [!NOTE]
> Si vous utilisez la vague de lancement 1 de 2020 de Business Central ou antérieure, il n’y a qu’un choix **Aperçu** qui ferme la page de demande lors de l’aperçu, comme décrit pour **Aperçu et fermer**.

### Utiliser l’aperçu

Dans l’Aperçu, utilisez la barre de menus dans l’aperçu de l’état pour :

- Naviguer entre les pages
- Effectuer un zoom avant et arrière
- Redimensionner à la taille de la page
- Sélectionner du texte

    Vous pouvez copier le texte d’un état puis le coller ailleurs, comme dans une page de [!INCLUDE[prod_short](includes/prod_short.md)] ou Microsoft Word. À l’aide d’une souris, par exemple, vous sélectionnez le bouton gauche de la souris et le maintenez enfoncé où vous voulez commencer. Faites glisser la souris pour sélectionner un ou plusieurs mots, phrases ou paragraphes. Puis sélectionnez le bouton droit de la souris et sélectionnez **Copier**. Vous pouvez maintenant coller le texte sélectionné partout où vous le souhaitez.
- Faire défiler le document

    Vous pouvez déplacer la zone visible de l’état dans n’importe quelle direction de manière voir d’autres zones ou l’état. Le défilement est utile si vous avez effectué un zoom pour observer les détails. Avec la souris, par exemple, sélectionnez et maintenez la pression n’importe où dans l’aperçu de l’état, puis déplacez la souris pour sélectionner une section de l’état.

- Téléchargez un fichier PDF sur votre ordinateur ou votre réseau.
- Imprimer

## Enregistrement d’un état dans un fichier

Vous pouvez enregistrer un état dans un document PDF, un document Microsoft Word, un classeur Microsoft Excel ou un document XML en sélectionnant **Envoyer à**, puis en effectuant votre sélection. Un fichier de présentation sera téléchargé sur votre appareil.

Si votre organisation a configuré OneDrive pour les fonctionnalités système, au lieu d’être téléchargés, les classeurs Excel et les documents Word sont ouverts dans votre navigateur à l’aide d’Excel ou de Word pour le Web.

> [!TIP]
> Les options **Document Microsoft Excel (données uniquement)** et **Document XML** concernent principalement le niveau avancé. Vous utiliserez généralement ces options pour effectuer une analyse détaillée des données. En savoir plus [Analyse des données d’état avec Excel et XML](report-analyze-excel.md).
>
> Vous pouvez également utiliser l’option **Document Microsoft Excel (données uniquement)** pour créer des présentations Excel pour un état donné. En savoir plus sur [Utiliser les présentations Excel](ui-excel-report-layouts.md).  

## <a name="ScheduleReport"></a> Planification d’un état pour une exécution ultérieure ou périodique

Vous pouvez planifier ou traiter par lots un état ponctuel ou récurrent à exécuter à une date et une heure spécifiques. Les états prévus sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l’option **Planifié** après avoir cliqué sur le bouton **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date. L’état est alors ajouté à la file d’attente des travaux et sera exécuté au moment spécifié. Lorsque l’état a été traité, l’article est supprimé de la file projets. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

Lorsque vous planifiez l’exécution d’un rapport, vous pouvez spécifier qu’il doit s’exécuter tous les jeudis en définissant le champ **Formule de la date de la prochaine exécution** sur *D4*, par exemple. Pour plus d’informations, voir [Utiliser des formules date](ui-enter-date-ranges.md#use-date-formulas).  

Vous pouvez choisir de sauvegarder l’état dans un fichier (par exemple, Excel, Word ou PDF) de l’imprimer ou uniquement de générer l’état. Si vous choisissez d’enregistrer l’état dans un fichier, alors l’état traité est envoyé à la **Boîte de réception état** sur votre tableau de bord, dans laquelle vous pouvez l’afficher. En savoir plus [Partager et exporter des états avec la boîte de réception état](ui-work-report-inbox.md)

### Gérer les états récurrents planifiés

Les états planifiés sont générés par des traitements par lots gérés sur la page **Écritures de la file d’attente des travaux**. Vous pouvez voir l’état et d’autres informations pour chaque rapport sur la page, interrompre/reprendre le traitement par lots de l’état et générer l’état à la demande.

Depuis la page **Écritures de la file d’attente des travaux**, vous pouvez également modifier certains paramètres d’état, tels que le type de fichier de sortie, la récurrence, la date d’exécution et les heures de début et de fin. Toutefois, avant de modifier un état planifié existant, il est nécessaire de mettre la file d’attente des tâches d’état en attente :

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Écritures file d’attente des travaux**, puis sélectionnez le lien associé.  
2. Sur la page **Écritures file d’attente des travaux**, choisissez l’état souhaité.
3. Choisissez l’action **Définir en attente**.
4. Ouvrez et modifiez l’état planifié en sélectionnant son état (*En attente*).

Après avoir modifié les options de l’état, répétez les deux premières étapes, puis sélectionnez l’action **Définir le statut sur Prêt** pour reprendre la génération de l’état.

En savoir plus sur la gestion de la file d’attente des travaux sur [Utiliser les files d’attente de travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

## <a name="PrintReport"></a>Impression d’un état

Pour imprimer un état, sélectionnez **Imprimer** sur la page de demande d’état ou dans la barre de menu de la page **Aperçu**.

Lorsqu’un état utilise une présentation Excel, le champ **Imprimante** et les boutons **Imprimer** ou **Aperçu** ne sont pas affichés. Au lieu de cela, il y a une option **Télécharger**. Pour imprimer, sélectionnez **Télécharger**, puis ouvrez le fichier téléchargé dans Excel et imprimez à partir de là.

### <a name="Printer"></a>Imprimante

Le champ **Imprimante** de la page de demande d’état affiche le nom de l’imprimante à laquelle l’état sera transmis. Pour changer d’imprimante, sélectionnez simplement l’imprimante dans la liste.

> [!NOTE]
> L’option **(Géré par le navigateur)** indique qu’il n’y a pas d’imprimante désignée pour l’état. Dans ce cas, le navigateur gérera l’impression et affichera une expérience standard, où vous pourrez choisir une imprimante locale connectée à votre appareil. L’option **(Géré par le navigateur)** n’est pas disponible dans l’application mobile [!INCLUDE[prod_short](includes/prod_short.md)] ou application pour Microsoft Teams.

> [!TIP]
> L’imprimante sélectionnée pour vous par défaut est configurée sur la page **Sélections d’imprimantes**. En savoir plus sur la modification de l’imprimante par défaut dans la section [Configurer les imprimantes par défaut](ui-specify-printer-selection-reports.md#default).

### Impression d’états en thaïlandais

Spécifiquement pour la version thaïlandaise de [!INCLUDE[prod_short](includes/prod_short.md)], le bouton **Imprimer** ne peut pas imprimer correctement des états du fait des limitations du service qui génère un fichier PDF imprimable. À la place, vous pouvez ouvrir l’état dans Word puis enregistrer l’état en tant que fichier PDF imprimable.  

Sinon, vous pouvez demander à votre administrateur de créer une présentation état Word pour vos états les plus utilisés. En savoir plus [Gestion des présentations état et document](ui-manage-report-layouts.md).  

## Modifier la présentation de l’état

Une présentation d’état contrôle les éléments affichés sur un état, leur agencement et leur mise en forme. Il explique plusieurs méthodes pour modifier la présentation :

- Lorsque vous configurez l’exécution d’un état, vous voyez la mise en page actuelle dans le champ **Présentation état** sur la page de demande. Pour basculer temporairement vers une autre présentation, sélectionnez le champ **Présentation état**, puis faites votre choix dans la liste des présentations disponibles pour l’état.
- Pour modifier la mise en page par défaut utilisée par un état, accédez aux pages **Présentations état** ou **Sélection présentation état**.

En savoir plus sur [(Hérité) Définir la présentation utilisée par un état](ui-set-report-layout.md). Ou, si vous voulez personnaliser votre propre présentation d’état, voir [Bien démarrer avec la création de présentations](ui-get-started-layouts.md).

## Modifier la langue et le format des nombres, des dates et des heures

Par défaut, la langue du texte et le format des nombres, des dates et des heures dans un rapport sont basés sur vos paramètres de langue de travail et de région, qui sont définis sur la page **Mes paramètres**. Vous pouvez toutefois modifier la langue et la région de format au cas par cas lorsque vous prévisualisez, imprimez ou envoyez un rapport. Sur la page de demande, sélectionnez **Avancé**, puis définissez les options **Langue** et **Région de format** comme vous le souhaitez.

Pour plus d’informations sur la page **Mes paramètres**, accédez à [Modifier les paramètres de base](ui-change-basic-settings.md#region).

## Options avancées

Les champs sous **Avancé** définissent des limites sur l’état généré pour contrôler les ressources de l’imprimante. Vous n’aurez généralement pas à modifier ces paramètres, sauf si vous disposez d’un état volumineux. Si un état dépasse ces limites lorsque vous essayez d’afficher un aperçu ou d’imprimer, un message apparaît vous indiquant quelle limite a été dépassée. Vous pouvez ensuite modifier les paramètres en fonction de votre état. Cependant, chaque champ a une valeur maximale que vous devez connaître :

|Champ|Valeur maximale|
|-----|-------------|
|Durée maximale de l’affichage|12:00:00|
|Nombre maximal de lignes|1 000 000|
|Nombre maximal de documents|500|

> [!NOTE]
> Les valeurs maximales peuvent être différentes pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site et un administrateur peut les modifier. Pour plus d’informations, reportez-vous à la rubrique [Configuration de Business Central Server – États](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Pour un aperçu des limites des états [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, voir [Limites opérationnelles](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## Voir aussi

[États disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Utilisation des rapports dans le travail quotidien](reports-use-reports.md)  
[Vue d’ensemble de Business Intelligence et Reporting](reports-bi-reporting.md)  
[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)  
[Exécuter des traitements par lots et des ports XML](ui-how-run-batch-jobs.md)  
[Utiliser les dates civiles et les heures](ui-enter-date-ranges.md)  
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Décisionnel pour le secteur de la finance](bi.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
