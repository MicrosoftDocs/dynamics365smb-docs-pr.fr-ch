---
title: Créer une fiche suiveuse pour un projet et spécifier des tâches| Microsoft Docs
description: Pour un nouveau projet, vous créez une fiche projet qui contient les tâches projet et les lignes planning, pour vous aider à gérer la progression et les budgets.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management, task
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c109e9dca32e83ace97b773be97da8e463af5f0e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758782"
---
# <a name="create-jobs"></a>Créer des projets
Lorsque vous démarrez un nouveau projet, vous devez créer une fiche projet avec des tâches intégrées et des lignes planning structurées en deux couches.  

La première couche inclut les tâches du projet. Vous devez créer au moins une tâche par projet car toutes les validations font référence à une tâche de projet. Cela permet de configurer les lignes planning projet et de valider la consommation dans le projet.

La seconde couche inclut les lignes planning projet, qui spécifient l’utilisation détaillée des ressources, articles et diverses charges de comptabilité.

La structure de couche permet de séparer le projet en tâches plus petites et ainsi d’utiliser des détails plus spécifiques dans l’établissement du budget, les devis et l’enregistrement. En outre, elle vous donne un aperçu de la progression d’un projet. Par exemple, vous pouvez rechercher si vous respectez les étapes importantes fixées ou si vous êtes en passe de satisfaire les attentes budgétaires.

> [!TIP]
> Choisissez l’action **Nouveau projet** du tableau de bord **Chef de projet** pour lancer un guide de configuration assistée qui vous dirige à travers les étapes de création d’un projet avec des tâches intégrées et des lignes planning. La procédure suivante décrit comment exécuter les étapes manuellement. Pour obtenir un exemple de la procédure pour créer manuellement un projet, reportez-vous à la rubrique [Vidéo : Créer un projet dans Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

## <a name="to-create-a-job-card"></a>Pour créer une fiche projet
Vous devez créer une fiche projet, puis créez des Lignes tâche projet et des lignes planning projet pour ce projet.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.  
2. Cliquez sur **Nouveau**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour spécifier le projet avec les informations d’autres projets, cliquez sur **Copier projet**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.

> [!NOTE]  
>   Si vous utilisez des feuilles de temps dans le projet, vous devez également indiquer une personne responsable. Cette personne peut approuver les feuilles de temps pour les tâches des salariés associées à ce projet. Pour plus d’informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Pour créer une tâche pour un projet
L’une des clés de la création d’un projet consiste à spécifier les différentes tâches impliquées dans le projet. Pour ce faire, ajoutez de nouvelles lignes dans le raccourci **Tâches** de la page **Fiche projet**, une tâche par ligne. Chaque projet doit avoir au minimum une tâche.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.
2. Ouvrez la fiche projet pour un projet concerné.
3. Sur le raccourci **Tâches**, renseignez les champs, le cas échéant sur une ligne.
4. Pour indenter des tâches et créer une hiérarchie, cliquez sur **Tâches**, puis sur **Indenter tâches projet**.
5. Répétez les étapes 3 et 4 pour toutes les tâches dont vous avez besoin pour le projet.
6. Pour spécifier les tâches du projet avec les informations d’autres tâches de projet, cliquez sur **Copier les tâches projet de**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Pour créer des lignes planning pour un projet
Vous pouvez redéfinir vos nouvelles tâches projet sur les lignes planning projet. Une ligne planning peut être utilisée pour extraire toute information que vous souhaitez suivre pour un projet. Vous pouvez utiliser des lignes planning pour ajouter des informations telles que les ressources nécessaires ou pour capturer les articles nécessaires pour exécuter le projet. Par exemple, si vous avez une tâche pour obtenir l’accord d’un client sur un projet, vous pouvez associer cette tâche à des lignes planning article, comme un rendez-vous avec le client ou l’affectation d’une ressource.  

Une ligne planning projet peut avoir l’un des types suivants :  

| Type | Désignation |
| --- | --- |
| **Budget** |Permet d’obtenir les activités et coûts prévus pour le projet, généralement dans le cadre d’un projet de régie. Les lignes planning de ce type ne peuvent pas être facturées. |
| **Facturable** |Permet de fournir un devis au client, généralement utilisé dans le cadre d’un projet à prix fixe. |
| **Budget et Facturable** |Permet de faire correspondre l’activité budgétée au montant que vous souhaitez facturer. |

**Remarque**. Au fur et à mesure de l’ajout d’informations sur les lignes planning projet, le coût est automatiquement mis à jour. Par exemple, le coût, le prix et la remise relatifs aux ressources et aux articles sont initialement calculés sur la base des informations définies dans les fiches ressource et article.

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.
2. Ouvrez la fiche projet appropriée.
3. Sélectionnez une tâche projet pour laquelle le champ **Type tâche projet** contient **Validation** puis, cliquez sur **Lignes planning projet**.  
4. Sur la page **Lignes planning projet**, renseignez les champs, le cas échéant sur une nouvelle ligne.
5. Répétez les étapes 3 et 4 pour toutes les lignes planning dont vous avez besoin pour la tâche projet.

## <a name="see-also"></a>Voir aussi

[Gestion de projets](projects-manage-projects.md)  
[Vidéo : Créer un projet dans Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finances](finance.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]