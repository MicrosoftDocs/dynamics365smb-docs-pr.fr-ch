---
title: Exécuter et imprimer des états
description: En savoir plus sur l’entrée d’un état dans une file d’attente de projets et la planification de son traitement à une date et à une heure spécifiques.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 03/24/2022
ms.author: jswymer
ms.openlocfilehash: fade19b2ecb4d2c17b5d5775074f2f715496a908
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512695"
---
# <a name="run-and-print-reports"></a>Exécuter et imprimer des états

Un rapport rassemble des informations en fonction d’un ensemble spécifié de critères. Il organise et présente les informations dans un format facile à lire que vous pouvez imprimer ou enregistrer sous forme de fichier. Il existe de nombreux états accessibles tout au long de l’application. Les états fournissent généralement des informations relatives au contexte de la page où vous vous trouvez. Par exemple, la page **Client** comprend des états pour les 10 principaux clients et les statistiques de vente, et plus encore.

Les traitements par lots et les ports XML sont plus ou moins identiques aux états mais ils ont pour objectif d’exécuter un processus ou d’exporter des données. Par exemple, le traitement par lots **Créer des relances** crée des relances pour les clients avec des paiements échus.  

> [!NOTE]
> Cette rubrique fait référence surtout aux « états », mais des informations similaires s’appliquent aux traitements par lots et aux ports XML.

## <a name="get-started"></a>Démarrer

Vous pouvez trouver les états sous l’onglet **États** sur les pages sélectionnées ou utiliser la recherche ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"). pour rechercher des rapports par nom.

Lorsque vous ouvrez un état, un traitement par lot ou un XMLport, une page de demande s’affiche généralement pour vous permettre de définir plusieurs options et filtres qui déterminent les éléments à inclure dans l’état. Les sections suivantes expliquent comment utiliser la page de demande pour créer, afficher un aperçu et imprimer un état.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Utilisation des valeurs par défaut – paramètres prédéfinis

La plupart des pages de demande incluent le champ **Utiliser les valeurs par défaut de**. Ce champ vous permet de sélectionner des paramètres prédéfinis pour l’état, qui définissent automatiquement les options et les filtres de l’état. Sélectionnez une entrée dans la liste déroulante, et vous verrez les options et les filtres sur la page de demande se modifier en conséquence.

L’entrée appelée **Options et filtres récemment utilisés** est toujours disponible. Cette entrée permet de faire en sorte que l’état utilise les options et les filtres qui ont été utilisés la dernière fois que vous l’avez exécuté.

Le champ **Utiliser les valeurs par défaut de** fournit un moyen rapide et fiable de générer de manière cohérente des états contenant les données correctes. Après avoir sélectionné une entrée, vous pouvez modifier les options et les filtres avant d’afficher un aperçu ou d’imprimer l’état. Vos modifications ne seront pas enregistrées dans l’entrée de paramètres prédéfinis que vous avez sélectionnée, mais elles seront sauvegardées dans l’entrée **Options et filtres récemment utilisés**.

>[!NOTE]
> Les paramètres prédéfinis sont généralement configurés et gérés par un administrateur. Pour en savoir plus, voir [Gérer les paramètres enregistrés pour les états et les traitements par lots](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Définition des données à inclure dans un état

Utilisez les champs sous **Options** et **Filtres** pour modifier ou limiter les informations que vous souhaitez dans l’état. Vous devez définir des filtres dans un état de la même manière que vous le faites sur des listes. Pour plus d’informations, reportez-vous à la rubrique [Filtrage](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La section **Filtrer la liste par** sur une page de demande fournit une capacité de filtrage générique pour les états. Ces filtres sont optionnels.
>
> Certains états ignoreront ces filtres, ce qui signifie que quel que soit le filtre défini dans la section **Filtrer la liste par**, la sortie de l’état est identique. Il est impossible de fournir une liste des champs ignorés dans quels états, vous devez expérimenter avec des filtres lorsque les vous utiliserez.
>
> **Exemple** : Lorsque vous utilisez le traitement par lots **Créer relance**, un filtre pour le champ **Écritures comptables client** de **Niveau dernière relance émise** sera ignoré car les filtres sont fixes pour ce traitement par lots.

## <a name="previewing-a-report"></a>Affichage de l’aperçu d’un état

L’aperçu d’un état vous permet de voir à quoi il ressemblera avant de l’imprimer. L’aperçu n’est pas basé sur l’imprimante sélectionnée dans le champ **Imprimante** sur la page de demande. Il est contrôlé par le navigateur. Après l’aperçu, vous pouvez revenir à la page de la demande et apporter des modifications aux options et aux filtres si nécessaire.

Pour afficher l’aperçu d’un état, choisissez le bouton **Aperçu** ou **Aperçu et fermer** sur la page de demande d’état. Le bouton qui s’affiche selon l’état, certains états ont un bouton **Aperçu**, tandis que d’autres ont un bouton **Aperçu et fermer**. Les deux boutons ouvriront un aperçu de l’état. La différence est que l’**Aperçu** garde la page de demande ouverte afin que vous puissiez y revenir, apporter des modifications, afficher à nouveau un aperçu ou imprimer. Avec **Aperçu et fermer**, la page de demande se ferme, vous devrez donc rouvrir l’état pour apporter des modifications ou l’imprimer.

> [!NOTE]
> Si vous utilisez la vague de lancement 1 de 2020 de Business Central ou antérieure, il n’y a qu’un bouton **Aperçu** qui ferme la page de demande lors de l’aperçu, comme décrit pour **Aperçu et fermer**.

### <a name="work-with-the-preview"></a>Utiliser l’Aperçu

Dans l’Aperçu, utilisez la barre de menus dans l’aperçu de l’état pour :

- Naviguer entre les pages
- Effectuer un zoom avant et arrière
- Redimensionner à la taille de la page
- Sélectionner du texte

    Vous pouvez copier le texte d’un état puis le coller ailleurs, comme dans une page de [!INCLUDE[prod_short](includes/prod_short.md)] ou Microsoft Word.  À l’aide d’une souris, par exemple, vous appuyez et maintenez là où vous voulez commencer. Déplacez ensuite la souris pour sélectionner un ou plusieurs mots, phrases ou paragraphes. Appuyez sur le bouton droit de la souris et sélectionnez **Copier**. Ensuite, collez le texte sélectionné partout où vous le souhaitez.
- Faire défiler le document

    Vous pouvez déplacer la zone visible de l’état dans n’importe quelle direction de manière voir d’autres zones ou l’état. Le défilement est utile si vous avez effectué un zoom pour observer les détails.  Avec la souris, par exemple, appuyez et maintenez la pression n’importe où dans l’aperçu de l’état, puis déplacez la souris.

- Téléchargez un fichier PDF sur votre ordinateur ou votre réseau.
- Imprimer

## <a name="saving-a-report-to-a-file"></a>Enregistrement d’un état dans un fichier

Vous pouvez enregistrer un état dans un document PDF, un document Microsoft Word, une feuille de calcul Microsoft Excel ou un document XML en cliquant sur le bouton **Envoyer à**, puis en effectuant votre sélection.

> [!TIP]
> Les options **Document Microsoft Excel (données uniquement)** et **Document XML** concernent principalement le niveau avancé. Vous utiliserez généralement ces options pour effectuer une analyse détaillée des données. Pour plus d’informations, voir [Analyse des données d’état avec Excel et XML](report-analyze-excel.md).
>
> Vous pouvez également utiliser l’option **Document Microsoft Excel (données uniquement)** pour créer de présentations Excel pour un rapport donné. Pour plus d’informations, voir [Utiliser des présentations Excel](ui-excel-report-layouts.md).  
  
<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="scheduling-a-report-to-run-later"></a><a name="ScheduleReport"></a> Planification d’un état pour une exécution ultérieure

Vous pouvez planifier ou traiter par lots un état à exécuter à une date et une heure spécifiques. Les états prévus ou les traitements par lots sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l’option **Planifié** après avoir cliqué sur le bouton **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date. L’état est alors ajouté à la file d’attente des travaux et sera exécuté au moment spécifié. Lorsque l’état a été traité, l’article est supprimé de la file projets. Pour en savoir plus, consultez [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

Lorsque vous planifiez l’exécution d’un rapport, vous pouvez spécifier qu’il doit s’exécuter tous les jeudis en définissant le champ **Formule de la date de la prochaine exécution** sur *D4*, par exemple. Pour plus d’informations, voir [Utiliser des formules date](ui-enter-date-ranges.md#use-date-formulas).  

Vous pouvez choisir de sauvegarder l’état dans un fichier, par exemple, Excel, Word ou PDF, de l’imprimer ou uniquement de générer l’état. Si vous choisissez d’enregistrer l’état dans un fichier, alors l’état traité est envoyé à la **Boîte de réception état** sur votre tableau de bord, dans laquelle vous pouvez l’afficher.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Impression d’un état

Pour imprimer un état, cliquez sur le bouton **Imprimer** sur la page de demande d’état ou dans la barre de menu de la page **Aperçu**.

Lorsqu’un état utilise une présentation Excel, les champs **Imprimante**, le bouton **Imprimer** ou le bouton **Aperçu** ne sont pas affichés. Au lieu de cela, il y a un bouton **Télécharger**. Pour imprimer, sélectionnez **Télécharger**, puis ouvrez le fichier téléchargé dans Excel et imprimez à partir de là.

### <a name="printer"></a><a name="Printer"></a>Imprimante

Le champ **Imprimante** de la page de demande d’état affiche le nom de l’imprimante à laquelle l’état sera transmis. Pour changer d’imprimante, sélectionnez simplement l’imprimante dans la liste.

> [!NOTE]
> **(Géré par le navigateur)** indique qu’il n’y a pas d’imprimante désignée pour l’état. Dans ce cas, le navigateur gérera l’impression et affichera une expérience standard, où vous pourrez choisir une imprimante locale connectée à votre appareil. **(Géré par le navigateur)** n’est pas disponible dans l’application mobile [!INCLUDE[prod_short](includes/prod_short.md)] ou application pour Microsoft Teams.

> [!TIP]
> L’imprimante sélectionnée pour vous par défaut est configurée sur la page **Sélections d’imprimantes**. Pour plus d’informations sur la modification de l’imprimante par défaut, reportez-vous à [Sélectionner quelles imprimantes impriment quels rapports](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Impression d’états en thaïlandais

Spécifiquement pour la version thaïlandaise de [!INCLUDE[prod_short](includes/prod_short.md)], le bouton **Imprimer** ne peut pas imprimer correctement des états du fait des limitations du service qui génère un fichier PDF imprimable. À la place, vous pouvez ouvrir l’état dans Word puis enregistrer l’état en tant que fichier PDF imprimable.  

Sinon, vous pouvez demander à votre administrateur de créer une présentation état Word pour vos états les plus utilisés. Pour plus d’informations, voir [Gestion des présentations de rapport et de document](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Modifier la présentation de l’état

Une présentation d’état contrôle les éléments affichés sur un état, leur agencement et leur mise en forme. Pour changer de présentation, voir [Définir la présentation utilisée par un état](ui-set-report-layout.md). Ou, si vous voulez personnaliser votre propre présentation d’état, voir [Bien démarrer avec la création de présentations](ui-get-started-layouts.md).

## <a name="advanced-options"></a>Options avancées

Les champs sous **Avancé** définissent des limites sur l’état généré pour contrôler les ressources de l’imprimante. Vous n’aurez généralement pas à modifier ces paramètres, sauf si vous disposez d’un état volumineux. Si un état dépasse ces limites lorsque vous essayez d’afficher un aperçu ou d’imprimer, un message apparaît vous indiquant quelle limite a été dépassée. Vous pouvez ensuite modifier les paramètres en fonction de votre état. Cependant, chaque champ a une valeur maximale que vous devez connaître :

|Champ|Valeur maximale|
|-----|-------------|
|Durée maximale de l’affichage|12:00:00|
|Nombre maximal de lignes|1 000 000|
|Nombre maximal de documents|500|

> [!NOTE]
> Les valeurs maximales peuvent être différentes pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site et un administrateur peut les modifier. Pour plus d’informations, reportez-vous à la rubrique [Configuration de Business Central Server – États](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Pour un aperçu des limites des états [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, voir [Limites opérationnelles](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Voir aussi

[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)  
[Utiliser les dates civiles et les heures](ui-enter-date-ranges.md)  
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]