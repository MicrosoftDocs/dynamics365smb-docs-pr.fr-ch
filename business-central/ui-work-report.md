---
title: Utilisation des états, des traitements par lots et des ports XML
description: En savoir plus sur l’entrée d’un état dans une file d’attente de projets et la planification de son traitement à une date et à une heure spécifiques.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: 9deb7e30e05da74e6ea263a0262680d2e99b8b4b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439965"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Utilisation des états, des traitements par lots et des ports XML

Un rapport rassemble des informations en fonction d’un ensemble spécifié de critères. Il organise et présente les informations dans un format facile à lire que vous pouvez imprimer ou enregistrer sous forme de fichier. Il existe de nombreux états accessibles tout au long de l’application. Les états fournissent généralement des informations relatives au contexte de la page où vous vous trouvez. Par exemple, la page **Client** comprend des états pour les 10 principaux clients et les statistiques de vente, et plus encore.

Les traitements par lots et les ports XML sont plus ou moins identiques aux états mais ils ont pour objectif d’exécuter un processus ou d’exporter des données. Par exemple, le traitement par lots **Créer des relances** crée des relances pour les clients avec des paiements échus.  

> [!NOTE]
> Cette rubrique fait référence surtout aux « états », mais des informations similaires s’appliquent aux traitements par lots et aux ports XML.

## <a name="getting-started"></a>Mise en route

Vous pouvez trouver les états sous l’onglet **États** sur les pages sélectionnées ou utiliser la recherche ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"). pour rechercher des rapports par nom.

Lorsque vous ouvrez un état, un traitement par lot ou un XMLport, une page de demande s’affiche généralement pour vous permettre de définir plusieurs options et filtres qui déterminent les éléments à inclure dans l’état. Les sections suivantes expliquent comment utiliser la page de demande pour créer, afficher un aperçu et imprimer un état.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Utilisation des valeurs par défaut – paramètres prédéfinis 

La plupart des pages de demande incluent le champ **Utiliser les valeurs par défaut de**. Ce champ vous permet de sélectionner des paramètres prédéfinis pour l’état, qui définissent automatiquement les options et les filtres de l’état. Sélectionnez une entrée dans la liste déroulante, et vous verrez les options et les filtres sur la page de demande se modifier en conséquence.

L’entrée appelée **Options et filtres récemment utilisés** est toujours disponible. Cette entrée permet de faire en sorte que l’état utilise les options et les filtres qui ont été utilisés la dernière fois que vous l’avez exécuté.

Le champ **Utiliser les valeurs par défaut de** fournit un moyen rapide et fiable de générer de manière cohérente des états contenant les données correctes. Après avoir sélectionné une entrée, vous pouvez modifier les options et les filtres avant d’afficher un aperçu ou d’imprimer l’état. Vos modifications ne seront pas enregistrées dans l’entrée de paramètres prédéfinis que vous avez sélectionnée, mais elles seront sauvegardées dans l’entrée **Options et filtres récemment utilisés**.

>[!NOTE]
> Les paramètres prédéfinis sont généralement configurés et gérés par un administrateur. Pour en savoir plus, voir [Gérer les paramètres enregistrés pour les états et les traitements par lots](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Définition des données à inclure dans les états

Utilisez les champs sous **Options** et **Filtres** pour modifier ou limiter les informations que vous souhaitez dans l’état. Vous devez définir des filtres dans un état de la même manière que vous le faites sur des listes. Pour plus d’informations, reportez-vous à la rubrique [Filtrage](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La section **Filtrer la liste par** sur une page de demande fournit une capacité de filtrage générique pour les états. Ces filtres sont optionnels.
>
> Certains états ignoreront ces filtres, ce qui signifie que quel que soit le filtre défini dans la section **Filtrer la liste par**, la sortie de l’état est identique. Il est impossible de fournir une liste des champs ignorés dans quels états, vous devez expérimenter avec des filtres lorsque les vous utiliserez.
>
> **Exemple** : Lorsque vous utilisez le traitement par lots **Créer relance**, un filtre pour le champ **Écritures comptables client** de **Niveau dernière relance émise** sera ignoré car les filtres sont fixes pour ce traitement par lots.

## <a name="previewing-a-report"></a>Affichage de l’aperçu d’un état

L’aperçu d’un état vous permet de voir à quoi il ressemblera avant de l’imprimer. L’aperçu n’est pas basé sur le champ **Imprimante** de l’imprimante sélectionnée sur la page de demande. Il est contrôlé par le navigateur. Après l’aperçu, vous pouvez revenir à la page de la demande et apporter des modifications aux options et aux filtres si nécessaire.

Pour afficher l’aperçu d’un état, choisissez le bouton **Aperçu** ou **Aperçu et fermer** sur la page de demande d’état. Le bouton qui s’affiche selon l’état, certains états ont un bouton **Aperçu**, tandis que d’autres ont un bouton **Aperçu et fermer**. Les deux boutons ouvriront un aperçu de l’état. La différence est que l’**Aperçu** garde la page de demande ouverte afin que vous puissiez y revenir, apporter des modifications, afficher à nouveau un aperçu ou imprimer. Avec **Aperçu et fermer**, la page de demande se ferme, vous devrez donc rouvrir l’état pour apporter des modifications ou l’imprimer.

> [!NOTE]
> Si vous utilisez la vague de lancement 1 de 2020 de Business Central ou antérieure, il n’y a qu’un bouton **Aperçu** qui ferme la page de demande lors de l’aperçu, comme décrit pour **Aperçu et fermer**.

### <a name="working-with-the-preview"></a>Utilisation de l’aperçu

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

## <a name="saving-a-report-to-a-file"></a>Enregistrement d’un rapport dans un fichier

Vous pouvez enregistrer un état dans un document PDF, un document Microsoft Word ou une feuille de calcul Microsoft Excel en sélectionnant le bouton **Envoyer à**, puis en effectuant votre sélection.

### <a name="send-to-excel"></a>Envoyer à Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Il existe deux options pour enregistrer les résultats du rapport sous forme de feuille de calcul dans un classeur Excel : **Document Microsoft Excel (données et mise en page)** et **Document Microsoft Excel (données uniquement)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Document Microsoft Excel (données et disposition)](#tab/data-and-layout)

Cette option n’est disponible que pour les rapports qui utilisent une mise en page RDLC. Elle exporte les résultats du rapport avec la mise en page RDLC appliquée. Utilisez cette option si vous souhaitez exporter les données une seule fois et ne souhaitez apporter que des modifications mineures à leur apparence, telles que la police et le schéma de couleurs.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Document Microsoft Excel (données uniquement)](#tab/data-only)

L’option **Document Microsoft Excel (données uniquement)** exporte les résultats du rapport et les critères qui ont été utilisés pour les générer&mdash;, mais il n’inclut pas la mise en page du rapport. Le fichier Excel comprendra l’ensemble de données complet, sous forme de données brutes, disposées en lignes et en colonnes. Toutes les colonnes de données de l’ensemble de données du rapport sont incluses, qu’elles soient ou non utilisées dans la présentation du rapport.  Utilisez cette option lorsque vous souhaitez :

- Faire une analyse ad hoc des données. Par exemple, vous pouvez filtrer les données et utiliser Power Pivot pour les afficher.

  Chaque fois que vous exportez des résultats, une feuille de calcul est créée. En utilisant l’option **Document Microsoft Excel (données uniquement)**, vous pouvez exécuter le même rapport et réutiliser les modifications apportées à la mise en forme. Par exemple, pour Power Pivot, vous pouvez réexécuter le rapport pour une autre période, copier les résultats dans la feuille de calcul, puis actualiser la feuille de calcul. Vous pouvez trouver une application de création de rapports sur [AppSource](https://appsource.microsoft.com/).
- Inspectez le jeu de données du rapport lorsque vous créez ou modifiez des présentations de rapport personnalisées.

  Pour plus d’informations sur la création de présentations de rapport personnalisées, consultez [Création ou modification de présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)
- Diagnostiquez les problèmes de données dans les rapports.

##### <a name="for-administrators"></a>Pour les administrateurs

- **Microsoft Excel Document (données uniquement)** a été introduite en tant que fonctionnalité facultative dans la première vague de version 2021, mise à jour 18.3. Pour permettre aux utilisateurs d’accéder à cette fonction, activez la mise à jour de la fonction **Enregistrer l’ensemble de données du rapport dans le document Microsoft Excel** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management). Dans la deuxième vague de la version 2021, cette fonctionnalité devient permanente, vous n’aurez donc pas à l’activer.

- Les comptes d’utilisateurs ont besoin de l’autorisation **<!--Export Report Dataset To Excel-->Autoriser l’action Exporter le jeu de données de l’état dans Excel**, que vous pouvez demander en utilisant l’ensemble d’autorisations **Outils de dépannage** ou **Exporter le rapport Excel**.  

- Vous ne pouvez pas exporter un rapport contenant plus de 1 048 576 lignes ou 16 384 colonnes.

    > [!NOTE]
    > Avec Business Central sur site, le nombre maximal de lignes exportées peut être encore inférieur. Business Central Server inclut un paramètre de configuration, appelé **Nombre maximal de lignes de données autorisées à envoyer vers Excel**, pour diminuer la limite à partir de la valeur maximale. Pour plus d’informations, consultez [Configuration de Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) ou contactez votre administrateur.

##### <a name="for-developers-and-advanced-users"></a>Pour les développeurs et les utilisateurs avancés

L’option **Microsoft Excel Document (données uniquement)** exporte toutes les colonnes, y compris les colonnes contenant des filtres et des instructions de formatage pour d’autres valeurs. Voici quelques points d’intérêt :

- Les données binaires d’un champ, comme une image, ne sont pas exportées.

  Dans les colonnes contenant des données binaires, les champs incluront le texte **Données binaires ({0} octets)**, où **{0}** indique le nombre d’octets.
- À partir de la deuxième vague de la version 2 de Business Central 2021, le fichier Excel comprend également la feuille de calcul **Métadonnées de l’état**.

  Cette feuille de calcul montre les filtres appliqués à l’état et les propriétés générales de l’état, comme le nom, l’ID et les détails de l’extension. Les filtres sont affichés dans la colonne **Filtre (DataItem::Table::FilterGroupNo::FieldName)**. Les filtres de cette colonne incluent des filtres définis sur la page de demande de l’état. Elle comprend également des filtres définis dans le code AL, par exemple, par la [propriété DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) et la [propriété DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Pour plus d’informations sur la conception d’états, voir [Aperçu de l’état](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Certains états exportent des nombres sous forme de texte, ce qui vous empêche de faire des calculs ou d’utiliser Power Pivot sur les cellules de la feuille de calcul Excel. Après l’exportation, c’est une bonne idée de vérifier les nombres dans la feuille de calcul. Si vous souhaitez effectuer des analyses et des graphiques sur les nombres, modifiez le format des cellules pertinentes de **Texte** sur **Nombre**. Pour plus d’informations sur la mise en forme des nombres dans les cellules, voir cette vidéo [Mise en forme des nombres dans les cellules de Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planification d’un état à exécuter

Vous pouvez planifier ou traiter par lots un état à exécuter à une date et une heure spécifiques. Les états prévus ou les traitements par lots sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l’option **Planifié** après avoir cliqué sur le bouton **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date. L’état est alors ajouté à la file d’attente des travaux et sera exécuté au moment spécifié. Lorsque l’état a été traité, l’article est supprimé de la file projets. Pour en savoir plus, consultez [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

Lorsque vous planifiez l’exécution d’un rapport, vous pouvez spécifier qu’il doit s’exécuter tous les jeudis en définissant le champ **Formule de la date de la prochaine exécution** sur *D4*, par exemple. Pour plus d’informations, voir [Utilisation de formules date](ui-enter-date-ranges.md#using-date-formulas).  

Vous pouvez choisir de sauvegarder l’état dans un fichier, par exemple, Excel, Word ou PDF, de l’imprimer ou uniquement de générer l’état. Si vous choisissez d’enregistrer l’état dans un fichier, alors l’état traité est envoyé à la **Boîte de réception état** sur votre tableau de bord, dans laquelle vous pouvez l’afficher.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Impression d’un état

Pour imprimer un état, cliquez sur le bouton **Imprimer** sur la page de demande d’état ou dans la barre de menu de la page **Aperçu**.

### <a name="printer"></a><a name="Printer"></a>Imprimante

Le champ **Imprimante** de la page de demande d’état affiche le nom de l’imprimante à laquelle l’état sera transmis. Pour changer d’imprimante, sélectionnez simplement l’imprimante dans la liste.

> [!NOTE]
> **(Géré par le navigateur)** indique qu’il n’y a pas d’imprimante désignée pour l’état. Dans ce cas, le navigateur gérera l’impression et affichera une expérience standard, où vous pourrez choisir une imprimante locale connectée à votre appareil. **(Géré par le navigateur)** n’est pas disponible dans l’application mobile [!INCLUDE[prod_short](includes/prod_short.md)] ou application pour Microsoft Teams.

> [!TIP]
> L’imprimante sélectionnée pour vous par défaut est configurée sur la page **Sélections d’imprimantes**. Pour plus d’informations sur la modification de l’imprimante par défaut, reportez-vous à [Sélectionner quelles imprimantes impriment quels rapports](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Impression d’états en thaïlandais

Spécifiquement pour la version thaïlandaise de [!INCLUDE[prod_short](includes/prod_short.md)], le bouton **Imprimer** ne peut pas imprimer correctement des états du fait des limitations du service qui génère un fichier PDF imprimable. À la place, vous pouvez ouvrir l’état dans Word puis enregistrer l’état en tant que fichier PDF imprimable.  

Sinon, vous pouvez demander à votre administrateur de créer une présentation état Word pour vos états les plus utilisés. Pour plus d’informations, voir [Gestion des présentations de rapport et de document](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Modification des présentations d’état

Une présentation d’état contrôle les éléments affichés sur un état, leur agencement et leur mise en forme. Si vous souhaitez changer de présentation, voir [Modifier la présentation actuelle de l’état](ui-how-change-layout-currently-used-report.md). Ou, si vous souhaitez personnaliser votre propre présentation d’état, voir [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md).

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
[Utilisation de dates civiles et les heures](ui-enter-date-ranges.md)  
[Gestion des présentations d’état et de document](ui-manage-report-layouts.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]