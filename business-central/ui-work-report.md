---
title: Planification d'un état à exécuter à une date et une heure spécifiques | Microsoft Docs
description: En savoir plus sur l'entrée d'un état dans une file d'attente de projets et la planification de son traitement à une date et à une heure spécifiques.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: sgroespe
ms.openlocfilehash: 11c3fa284a457db1de272a3d92ebc7fc873ad933
ms.sourcegitcommit: 99cecd005f8ede70e9a3d163a457fcb9aadb6843
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/10/2020
ms.locfileid: "3549907"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Utilisation des états, des traitements par lots et des ports XML

Un état regroupe des informations en fonction d'un ensemble de critères spécifié, et organise et présente les informations dans un format facilement lisible que vous pouvez imprimer ou enregistrer en tant que fichier. Il existe de nombreux états accessibles tout au long de l'application. Les états fournissent généralement des informations relatives au contexte de la page où vous vous trouvez. Par exemple, la page **Client** comprend des états pour les 10 principaux clients et les statistiques de vente, et plus encore.

Les traitements par lots et les ports XML sont plus ou moins identiques aux états mais ils ont pour objectif d'exécuter un processus ou d'exporter des données. Par exemple, le traitement par lots **Créer des relances** crée des relances pour les clients avec des paiements échus.  

> [!NOTE]
> Cette rubrique fait référence surtout aux « états », mais des informations similaires s'appliquent aux traitements par lots et aux ports XML.

Vous pouvez rechercher des états dans l'onglet **États** sur les pages sélectionnées ou utiliser la recherche ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") pour rechercher les états par nom.

## <a name="specifying-the-data-to-include-in-reports"></a>Définition des données à inclure dans les états
Lorsque vous ouvrez un état, un traitement par lot ou un XMLport, une page de demande s'affiche généralement pour vous permettre de définir plusieurs options et filtres qui déterminent les éléments à inclure dans l'état.

Vous devez définir des filtres dans un état de la même manière que vous le faites sur des listes. Pour plus d'informations, reportez-vous à la rubrique [Filtrage](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La section **Filtrer la liste par** sur une page de demande fournit une capacité de filtrage générique pour les états. Ces filtres sont optionnels.
>
> Certains états ignoreront ces filtres, ce qui signifie que quel que soit le filtre défini dans la section **Filtrer la liste par**, la sortie de l'état est identique. Il est impossible de fournir une liste des champs ignorés dans quels états, vous devez expérimenter avec des filtres lorsque les vous utiliserez.
>
> **Exemple** : Lorsque vous utilisez le traitement par lots **Créer relance**, un filtre pour le champ **Écritures comptables client** de **Niveau dernière relance émise** sera ignoré car les filtres sont fixes pour ce traitement par lots.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Utilisation des paramètres enregistrés
La page de demande peut inclure la section **Paramètres enregistrés** qui contient une ou plusieurs entrées dans la zone **Utiliser les valeurs par défaut de**. Un paramètre enregistré est fondamentalement un groupe d'options et de filtres prédéfini que vous pouvez appliquer à l'état avant d'en afficher un aperçu ou de l'envoyer vers un fichier. L'écriture de paramètres enregistrés appelée **Options et filtres récemment utilisés** est toujours disponible. Cette écriture permet de faire en sorte que l'état utilise les options et les filtres qui ont été utilisés la dernière fois que vous l'avez utilisé.

Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates. Après avoir défini la zone **Utiliser les valeurs par défaut de** sur une entrée de paramètres enregistrés, vous pouvez modifier les options et les filtres avant d'afficher un aperçu ou d'enregistrer l'état. Vos modifications ne seront pas enregistrées dans l'entrée de paramètres enregistrés que vous avez sélectionnée, mais elles seront sauvegardées dans l'entrée **Options et filtres récemment utilisés**.

>[!NOTE]
>Si vous êtes un administrateur, vous pouvez créer et gérer les paramètres enregistrés des états pour tous les utilisateurs. Pour plus d'informations, voir [Gérer les paramètres enregistrés pour les états et les traitements par lots](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Affichage de l'aperçu d'un état

Cliquez sur le bouton **Aperçu** pour afficher l'état dans la page de demande d'état. Utilisez la barre de menus dans l'aperçu de l'état pour :

- Naviguer entre les pages
- Effectuer un zoom avant et arrière
- Redimensionner à la taille de la page
- Sélectionner du texte

    Vous pouvez copier le texte d'un état puis le coller ailleurs, comme dans une page de [!INCLUDE[d365fin](includes/d365fin_md.md)] ou Microsoft Word.  Avec la souris, par exemple, appuyez et maintenez la pression là où vous souhaitez démarrer, puis déplacez la souris pour sélectionner un ou plusieurs mots, phrases ou paragraphes. Vous pouvez ensuite appuyer sur le bouton droit de la souris et sélectionner **Copier**. Vous pouvez coller le texte sélectionné partout où vous le souhaitez.
- Faire défiler le document

    Vous pouvez déplacer la zone visible de l'état dans n'importe quelle direction de manière voir d'autres zones ou l'état. Ceci est utile si vous avez effectué un zoom pour observer les détails.  Avec la souris, par exemple, appuyez et maintenez la pression n'importe où dans l'aperçu de l'état, puis déplacez la souris.

- Téléchargez un fichier PDF sur votre ordinateur ou votre réseau.
- Imprimer

## <a name="saving-a-report"></a>Enregistrement d'un état
Vous pouvez enregistrer un état dans un document PDF, un document Microsoft Word ou un document Microsoft Excel en sélectionnant le bouton **Envoyer à**, puis en effectuant votre sélection.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planification d'un état à exécuter

Vous pouvez planifier ou traiter par lots un état à exécuter à une date et une heure spécifiques. Les états prévus ou les traitements par lots sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l'option **Planifié** après avoir cliqué sur le bouton **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date. L'état est alors ajouté à la file d'attente des travaux et sera exécuté au moment spécifié. Lorsque l'état a été traité, l'article est supprimé de la file projets. Pour en savoir plus, consultez [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

Lorsque vous planifiez l'exécution d'un rapport, vous pouvez spécifier qu'il doit s'exécuter tous les jeudis en définissant le champ **Formule de la date de la prochaine exécution** sur *D4*, par exemple. Pour plus d'informations, voir [Utilisation de formules date](ui-enter-date-ranges.md#using-date-formulas).  

Vous pouvez choisir de sauvegarder l'état traité dans un fichier, par exemple, Excel, Word ou PDF, de l'imprimer sur une imprimante sélectionnée ou de traiter l'état uniquement. Si vous choisissez d'enregistrer l'état dans un fichier, alors l'état traité est envoyé à la **Boîte de réception état** sur votre tableau de bord, dans laquelle vous pouvez l'afficher.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Impression d'un état

Vous imprimez un état en cliquant sur le bouton **Impression** sur la page de demande d'état ou dans la barre de menu sur la page **Aperçu**.

### <a name="printer-selection"></a>Sélection de l'imprimante

L'état est imprimé sur l'imprimante indiquée dans le champ **Imprimante sélectionnée** de la page de demande d'état. Vous ne pouvez pas changer d'imprimante sur cette page.

L'imprimante sélectionnée est définie sur la page **Sélections d'imprimantes** ou il s'agit de l'imprimante par défaut configurée sur la page **Gestion des imprimantes**. Si vous souhaitez utiliser une autre imprimante, consultez [Paramétrage imprimantes](ui-specify-printer-selection-reports.md).

Si aucune imprimante n'est spécifiée sur la page **Sélections d'imprimantes** ou n'est définie par défaut sur la page **Gestion des imprimantes**, la fonction d'impression du navigateur est utilisée. Dans ce cas, **Navigateur** s'affiche dans le champ **Imprimante sélectionnée** de la page de demande d'état. 

### <a name="browser-printing"></a>Impression du navigateur

Comme [!INCLUDE[prodshort](includes/prodshort.md)] est un service cloud, il ne peut pas atteindre les imprimantes locales connectées à votre ordinateur. Cependant, il peut se connecter aux imprimantes cloud. Dans la version générique de [!INCLUDE[prodshort](includes/prodshort.md)], une imprimante cloud nommée **Imprimante par e-mail** est installée en tant qu'extension et prête à l'emploi après la configuration initiale.

Si aucune imprimante cloud n'est installée et configurée ou si une imprimante installée échoue, l'impression reprend par défaut les options d'impression du navigateur.

> [!NOTE]
> Les options d'impression du navigateur fonctionnent indépendamment de [!INCLUDE[prodshort](includes/prodshort.md)]. Les paramètres d'imprimante qui auraient pu être configurés à partir des imprimantes dans [!INCLUDE[prodshort](includes/prodshort.md)] ne sont pas répercutés dans les options d'impression du navigateur.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Impression d'états en thaïlandais
Spécifiquement pour la version thaïlandaise de [!INCLUDE[prodshort](includes/prodshort.md)], le bouton **Imprimer** ne peut pas imprimer correctement des états en raison des limitations du service qui génère un fichier PDF imprimable. À la place, vous pouvez ouvrir l'état dans Word puis enregistrer l'état en tant que fichier PDF imprimable.  

Sinon, vous pouvez demander à votre administrateur de créer une présentation état Word pour vos états les plus utilisés. Pour plus d'informations, voir [Gestion des présentations de rapport et de document](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Modification des présentations d'état
Une présentation d'état contrôle les éléments affichés sur un état, leur agencement et leur mise en forme. Si vous souhaitez changer de présentation, voir [Modifier la présentation actuelle de l'état](ui-how-change-layout-currently-used-report.md). Ou, si vous souhaitez personnaliser votre propre présentation d'état, voir [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Voir aussi

[Paramétrage imprimantes](ui-specify-printer-selection-reports.md)  
[Utilisation de dates civiles et les heures](ui-enter-date-ranges.md)  
[Gestion des présentations d'état et de document](ui-manage-report-layouts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
