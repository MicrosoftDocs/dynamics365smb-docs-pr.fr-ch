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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 709e444d185e6950d6367036db622b30c8062f25
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310627"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Utilisation des états, des traitements par lots et des ports XML
Un état regroupe des informations en fonction d'un ensemble de critères spécifié, et organise et présente les informations dans un format facilement lisible que vous pouvez imprimer ou enregistrer en tant que fichier. Il existe de nombreux états accessibles tout au long de l'application. Les états fournissent généralement des informations relatives au contexte de la page où vous vous trouvez. Par exemple, la page **Client** comprend des états pour les 10 principaux clients et les statistiques de vente, et plus encore.

Les traitements par lots et les ports XML sont plus ou moins identiques aux états mais ils ont pour objectif d'exécuter un processus ou d'exporter des données. Par exemple, le traitement par lots **Créer des relances** crée des relances pour les clients avec des paiements échus.  

> [!NOTE]
> Cette rubrique fait référence surtout aux « états », mais des informations similaires s'appliquent aux traitements par lots et aux ports XML.

Vous pouvez rechercher des états dans l'onglet **États** sur les pages sélectionnées, ou utiliser la recherche ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") pour rechercher les états par nom.

## <a name="specifying-the-data-to-include-in-reports"></a>Définition des données à inclure dans les états
Lorsque vous ouvrez un état, un traitement par lot ou un XMLport, une page de demande s'affiche généralement pour vous permettre de définir plusieurs options et filtres qui déterminent les éléments à inclure dans l'état.

Vous devez définir des filtres dans un état de la même manière que vous le faites sur des listes. Pour plus d'informations, reportez-vous à la rubrique [Filtrage](ui-enter-criteria-filters.md#-filtering).

> [!Caution]
> La section **Filtrer la liste par** sur une page de demande fournit une capacité de filtrage générique pour les états. Ces filtres sont optionnels.<br /><br /> Certains états ignoreront ces filtres, ce qui signifie que quel que soit le filtre défini dans la section **Filtrer la liste par**, la sortie de l'état est identique. Il est impossible de fournir une liste des champs ignorés dans quels états, vous devez expérimenter avec des filtres lorsque les vous utiliserez.<br /><br />
**Exemple** : Lorsque vous utilisez le traitement par lots **Créer relance**, un filtre pour le champ **Écritures comptables client** de **Niveau dernière relance émise** sera ignoré car les filtres sont fixes pour ce traitement par lots.

## <a name="SavedSettings"></a>Utilisation des paramètres enregistrés
La page de demande peut inclure la section **Paramètres enregistrés** qui contient une ou plusieurs entrées dans la zone **Utiliser les valeurs par défaut de**. Un paramètre enregistré est fondamentalement un groupe d'options et de filtres prédéfini que vous pouvez appliquer à l'état avant d'en afficher un aperçu ou de l'envoyer vers un fichier. L'écriture de paramètres enregistrés appelée **Options et filtres récemment utilisés** est toujours disponible. Cette écriture permet de faire en sorte que l'état utilise les options et les filtres qui ont été utilisés la dernière fois que vous l'avez utilisé.

Le fait d'utiliser les paramètres enregistrés est une façon rapide et fiable de générer de façon cohérente des états qui contiennent les données adéquates. Après avoir défini la zone **Utiliser les valeurs par défaut de** sur une entrée de paramètres enregistrés, vous pouvez modifier les options et les filtres avant d'afficher un aperçu ou d'enregistrer l'état. Vos modifications ne seront pas enregistrées dans l'entrée de paramètres enregistrés que vous avez sélectionnée, mais elles seront sauvegardées dans l'entrée **Options et filtres récemment utilisés**.

>[!NOTE]
>Si vous êtes un administrateur, vous pouvez créer et gérer les paramètres enregistrés des états pour tous les utilisateurs. Pour plus d'informations, voir [Gérer les paramètres enregistrés pour les états et les traitements par lots](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Affichage de l'aperçu d'un état
Cliquez sur le bouton **Aperçu** pour afficher l'état. Utilisez la barre de menus dans l'aperçu de l'état pour :

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
Vous pouvez enregistrer un état dans un document PDF, un document Microsoft Word ou un document Microsoft Excel en sélectionnant le bouton **Envoyer à**, puis en effectuant votre sélection.

## <a name="ScheduleReport"></a> Planification d'un état à exécuter
Vous pouvez planifier ou traiter par lots un état à exécuter à une date et une heure spécifiques. Les états prévus ou les traitements par lots sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous devez choisir l'option **Planifié** après avoir cliqué sur le bouton **Envoyer à**, puis vous devez entrer des informations telles que l’imprimante, l’heure et la date. L'état est alors ajouté à la file d'attente des travaux et sera exécuté au moment spécifié. Lorsque l'état a été traité, l'article est supprimé de la file projets. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

Vous pouvez choisir de sauvegarder l'état traité dans un fichier, par exemple, Excel, Word ou PDF, de l'imprimer sur une imprimante sélectionnée ou de traiter l'état uniquement. Si vous choisissez d'enregistrer l'état dans un fichier, alors l'état traité est envoyé à la **Boîte de réception état** sur votre tableau de bord, dans laquelle vous pouvez l'afficher.

## <a name="PrintReport"></a>Impression d'un état
Vous pouvez imprimer un état à l'aide du bouton **Imprimer** de la page d'options qui s'affiche lorsque vous ouvrez l'état ou dans la barre de menu dans l'aperçu.  

### <a name="printing-reports-in-thai"></a>Impression d'états en thaïlandais
Spécifiquement pour la version thaïlandaise de [!INCLUDE[prodshort](includes/prodshort.md)], le bouton **Imprimer** ne peut pas imprimer correctement des états en raison des limitations du service qui génère un fichier PDF imprimable. À la place, vous pouvez ouvrir l'état dans Word puis enregistrer l'état en tant que fichier PDF imprimable.  

Sinon, vous pouvez demander à votre administrateur de créer une présentation état Word pour vos états les plus utilisés. Pour plus d'informations, voir [Gestion des présentations de rapport et de document](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Modification des présentations d'état
Une présentation d'état contrôle les éléments affichés sur un état, leur agencement et leur mise en forme. Si vous souhaitez changer de présentation, voir [Modifier la présentation actuelle de l'état](ui-how-change-layout-currently-used-report.md). Ou, si vous souhaitez personnaliser votre propre présentation d'état, voir [Créer et modifier une présentation de rapport personnalisée](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Voir aussi
[Spécifier la sélection de l'imprimante pour les états](ui-specify-printer-selection-reports.md)  
[Utilisation de dates civiles et les heures](ui-enter-date-ranges.md)  
[Gestion des présentations d'état et de document](ui-manage-report-layouts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
