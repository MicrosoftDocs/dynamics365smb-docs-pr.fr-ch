---
title: Planification d'un état à exécuter à une date et une heure spécifiques | Microsoft Docs
description: En savoir plus sur l'entrée d'un état dans une file d'attente de projets et la planification de son traitement à une date et à une heure spécifiques.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 65fcba3f0222b324f132115ea7f1ec53b75d983f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "921424"
---
# <a name="working-with-reports-and-batch-jobs"></a>Utilisation des états et des traitements par lots
Un état regroupe des informations en fonction d'un ensemble de critères spécifié, et organise et présente les informations dans un format imprimable et facilement lisible. Il existe de nombreux états accessibles tout au long de l'application. Les états fournissent généralement des informations relatives au contexte de la page où vous vous trouvez. Par exemple, la page **Client** comprend des états pour les 10 principaux clients et les statistiques de vente, et plus encore.

Les traitements par lots sont plus ou moins identiques aux états mais ils ont pour objectif d'exécuter un processus. Par exemple, le traitement par lots **Créer des relances** crée des relances pour les clients avec des paiements échus.  

> [!NOTE]
> Cette rubrique fait référence surtout aux « états », mais des informations similaires s'appliquent aux traitements par lots.

Vous pouvez rechercher des états dans l'onglet **États** sur les pages sélectionnées, ou utiliser la recherche ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") pour rechercher les états par nom.


## <a name="specifying-the-data-to-include-in-the-report"></a>Définition des données à inclure dans l'état
Lorsque vous ouvrez un état, une page s'affiche généralement pour vous permettre de définir plusieurs options et filtres qui déterminent les éléments à inclure dans l'état. Cette page est appelée la page de demande de l'état. Par exemple, la page de demande de l'état vous permet de créer un état pour un client spécifique, une plage de dates spécifique, ou encore de définir l'ordre des informations dans l'état. Voici un exemple de page de demande de l'état :

![Options d'état](media/report_options.png "Options d'état")

> [!Caution]
> La section **Afficher résultats** sur une page de demande fournit une capacité de filtrage générique pour les états. Ces filtres sont optionnels.<br /><br /> Certains états ignoreront ces filtres, ce qui signifie que quel que soit le filtre défini dans la section **Afficher résultats**, la sortie de l'état est identique. Il est impossible de fournir une liste des champs ignorés dans quels états, vous devez expérimenter avec des filtres lorsque les vous utiliserez.<br /><br />
**Exemple** : Lorsque vous utilisez le traitement par lots **Créer relance**, un filtre pour le champ **Écritures comptables client** de **Niveau dernière relance émise** sera ignoré car les filtres sont fixes pour ce traitement par lots.

### <a name="SavedSettings"></a>Utilisation des paramètres enregistrés
Avec certains états, selon la manière dont ils sont conçus, la page d'état peut inclure la section **Paramètres enregistrés** qui contient une ou plusieurs entrées dans la zone **Utiliser les valeurs par défaut de**. Les entrées de cette zone sont appelées *paramètres enregistrés*. Un paramètre enregistré est fondamentalement un groupe d'options et de filtres prédéfini que vous pouvez appliquer à l'état avant d'en afficher un aperçu ou de l'envoyer vers un fichier. L'écriture de paramètres enregistrés appelée **Options et filtres récemment utilisés** est toujours disponible. Cette écriture permet de faire en sorte que l'état utilise les options et les filtres qui ont été utilisés la dernière fois que vous l'avez regardé.

Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates. Après avoir défini la zone **Utiliser les valeurs par défaut de** sur une entrée de paramètres enregistrés, vous pouvez modifier les options et les filtres avant d'afficher un aperçu ou d'enregistrer l'état. Vos modifications ne seront pas enregistrées dans l'entrée de paramètres enregistrés que vous avez sélectionnée, mais elles seront sauvegardées dans la zone **Options et filtres récemment utilisés**.

>[!NOTE]
>Si vous êtes un administrateur, vous pouvez créer et gérer les paramètres enregistrés des états pour tous les utilisateurs. Pour plus d'informations, voir [Gestion des paramètres enregistrés dans les états](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Définition des options et des filtres
Si vous souhaitez limiter davantage ou localiser les données incluses dans un état, vous pouvez définir des options et des filtres supplémentaires.

Les filtres vous permettent d'afficher les données selon des critères spécifiques. Les filtres sont regroupés selon l'entité à laquelle ils appartiennent, par exemple **Client** dans l'illustration ci-dessus. Vous spécifiez un filtre en définissant la zone **Où** sur le champ de filtre, puis en ajoutant les critères dans la zone **est :**.

Vous pouvez ajouter davantage de filtres en renseignant les cases **Et** et **est**. Lorsque vous avez plusieurs filtres, seuls les résultats qui répondent aux critères de tous les filtres seront inclus dans l'état.

Selon le champ de type que vous filtrez, vous pouvez spécifier les critères de filtre pour rechercher une correspondance exacte, une correspondance partielle, une plage de valeurs, etc. Pour obtenir de l'aide sur la configuration des filtres, voir :
-   [filtres](ui-enter-criteria-filters.md#FilterCriteria) ;
-   [Utilisation de dates civiles et les heures](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Affichage de l'aperçu d'un état
Sélectionnez **Aperçu** pour visualiser l'état dans le navigateur Internet. Pointez une zone de l'état pour afficher la barre de menu.  

![Barre d'outils Aperçu de l'état](media/report_viewer.png "Barre d'outils Aperçu de l'état")

Utilisez la barre de menus pour :

-   Naviguer entre les pages
-   Effectuer un zoom avant et arrière
-   Redimensionner à la taille de la page
-   Sélectionner du texte

    Vous pouvez copier le texte d'un état puis le coller ailleurs, comme dans une page de [!INCLUDE[d365fin](includes/d365fin_md.md)] ou Microsoft Word.  Avec la souris, par exemple, appuyez et maintenez la pression là où vous souhaitez démarrer, puis déplacez la souris pour sélectionner un ou plusieurs mots, phrases ou paragraphes. Vous pouvez ensuite appuyer sur le bouton droit de la souris et sélectionner **Copier**. Vous pouvez coller le texte sélectionné partout où vous le souhaitez.
-   Faire défiler le document

    Vous pouvez déplacer la zone visible de l'état dans n'importe quelle direction de manière voir d'autres zones ou l'état. Ceci est utile si vous avez effectué un zoom pour observer les détails.  Avec la souris, par exemple, appuyez et maintenez la pression n'importe où dans l'aperçu de l'état, puis déplacez la souris.

-   Téléchargez un fichier PDF sur votre ordinateur ou votre réseau.
-   Imprimer


## <a name="saving-a-report"></a>Enregistrement d'un état
Vous pouvez enregistrer un état dans un document PDF, un document Microsoft Word ou un document Microsoft Excel en sélectionnant **Envoyer à**, puis en effectuant votre sélection.

## <a name="ScheduleReport"></a> Planification d'un état à exécuter
Vous pouvez planifier un état à exécuter à une date et une heure spécifiques. Les états prévus sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous pouvez choisir de sauvegarder l'état traité dans un fichier, par exemple, Excel, Word ou PDF, de l'imprimer sur une imprimante sélectionnée ou de traiter l'état uniquement. Si vous choisissez d'enregistrer l'état dans un fichier, alors l'état traité est envoyé à la **Boîte de réception état** sur votre tableau de bord, dans laquelle vous pouvez l'afficher.

Vous pouvez planifier un état lorsque vous l'ouvrez. Vous devez sélectionner **Planifier** et entrer des informations telles que l'imprimante, ainsi que la date et l'heure. L'état est alors ajouté à la file d'attente des travaux et sera exécuté au moment spécifié. Lorsque l'état a été traité, l'article est supprimé de la file projets. Si vous avez enregistré l'état traité dans un fichier, il est disponible dans la **Boîte de réception état**.

## <a name="PrintReport"></a>Impression d'un état
Vous pouvez imprimer un état à l'aide du bouton **Imprimer** de la page d'options qui s'affiche lorsque vous ouvrez l'état ou dans la barre de menu dans l'aperçu.

## <a name="changing-the-layout-and-look-of-a-report"></a>Modification de la présentation et de l'apparence d'un état
Une présentation d'état contrôle les éléments affichés sur un état, leur agencement et leur mise en forme. Si vous souhaitez changer de présentation, voir [Modification de la présentation actuellement utilisée sur un rapport](ui-how-change-layout-currently-used-report.md). Ou, si vous souhaitez personnaliser votre propre présentation d'état, voir [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Voir aussi
[Spécifier la sélection de l'imprimante pour les états](ui-specify-printer-selection-reports.md)  
[Gestion des présentations de rapport et de document](ui-manage-report-layouts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
