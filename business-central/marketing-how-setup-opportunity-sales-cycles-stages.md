---
title: Configurer des cycles de vente opportunité et des étapes de cycle| Microsoft Docs
description: Décrit comment définir des étapes de ventes, du contact initial à la clôture, créer un cycle de vente et l'affecter aux opportunités dans Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: ba995628679946810b693184dac191988c7daf65
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181513"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Configurer des cycles de vente opportunité et des étapes de cycle
Avant de pouvoir utiliser les opportunités de vente, vous devez configurer les cycles de vente et les étapes correspondantes. Un cycle de vente est composé d'une série d'étapes allant du contact initial à la fermeture d'une vente. Chaque étape peut avoir certaines exigences à respecter, par exemple pour un devis, avant qu'une opportunité puisse accéder à l'étape suivante. Vous pouvez également spécifier si une étape peut être ignorée. Vous pouvez configurer autant de cycles de vente et d'étapes que nécessaire.

Mettre en œuvre des cycles de vente opportunité implique la création d'un cycle de vente, la définition des différentes étapes du cycle, puis l'affectation du cycle à des opportunités. L'affectation de l'activité ou des tâches correspondantes à l'opportunité peut également faire partie de la configuration d'un cycle de vente.

Cette rubrique décrit également comment configurer des tâches et les activités, et comment affecter des tâches aux activités. Pour plus d'informations, voir [Pour configurer des activités avec des tâches](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Pour configurer des cycles de vente opportunité
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Cycles de vente**, puis sélectionnez le lien associé. La page **Cycles de vente** s'affiche, et répertorie tous les cycles de vente existants.
2. Sélectionnez l'action **Nouveau**, puis renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Répétez ces étapes pour chaque cycle de vente à configurer. Une fois les cycles de vente opportunité configurés, vous pouvez définir les différentes étapes de chaque cycle.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Pour définir les étapes du cycle de vente opportunité
1. Sur la page **Cycles de vente**, sélectionnez le cycle de vente opportunité pour lequel vous souhaitez définir des étapes, puis sélectionnez l'action **Etapes**. La page **Etapes cycle de vente** s'affiche.
2. Sélectionnez l'action **Nouveau** pour intégrer une nouvelle étape dans le cycle de vente.

Répétez ces étapes pour définir toutes les étapes du cycle de vente.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Pour affecter des cycles d'étapes à des opportunités
Après avoir ajouté le cycle d'étapes opportunité, vous pouvez commencer à ajouter des opportunités de vente, puis affecter le cycle d'étapes aux opportunités en définissant le champ **Code cycle de vente**. Pour plus d'informations, voir [Créer des opportunités de vente](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Pour configurer des activités avec des tâches
Vous pouvez combiner plusieurs tâches, par exemple les tâches qui représentent chacune une étape, dans les activités. Les tâches d'activité sont liées entre elles par une formule de date. Vous pouvez affecter des activités aux opportunités, aux vendeurs, ou aux contacts.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Activités**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**, puis renseignez les champs selon vos besoins.
3. Sur le raccourci **Lignes**, renseignez les champs nécessaires pour définir une ou plusieurs tâches dans l'activité.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Pour affecter des tâches ou des activités de tâches liées aux opportunités
Lorsque vous avez créé une tâche, vous pouvez l'affecter à une opportunité de vente et affecter ainsi l'activité à laquelle la tâche appartient.

> [!NOTE]  
>   Cette procédure explique comment affecter des tâches d'activité à des opportunités. les étapes sont similaires lorsque vous affectez des tâches aux vendeurs et aux contacts.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Opportunités**, puis sélectionnez le lien associé.
2. Sélectionnez une opportunité, puis cliquez sur **Tâches**.
3. Sur la page **Liste des tâches**, sélectionnez l'action **Créer Tâche**.
4.  Sur la page **Créer Tâche**, renseignez les champs selon vos besoins.

    Remarquez dans le champ **Opportunité**, que celui est automatiquement affecté à l'opportunité en question.
5. Choisissez le bouton **OK**.
6. Sur la page **Liste des tâches**, sélectionnez la nouvelle tâche, puis sélectionner l'action **Affecter activités**.
7. Sur la page **Affecter activités**, renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Traitement des opportunités de vente](marketing-processing-sales-opportunities.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
