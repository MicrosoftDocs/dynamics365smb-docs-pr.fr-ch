---
title: "Gérer les absences des salariés | Microsoft Docs"
description: "Décrit comment enregistrer les absences des salariés et analyser les statistiques d'indisponibilité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f445ae26c3586016b350cfee2c594a4f7d636595
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="manage-employee-absence"></a>Gérer les absences des salariés
Pour gérer l'absence d'un salarié, vous devez l'enregistrer dans la fenêtre **Saisie des absences**. Elle peut alors être affichée de différentes façons à des fins d'analyse ou de génération d'état.

Vous pouvez afficher les absences des salariés dans deux fenêtres différentes :

* La fenêtre **Saisie des absences** est la fenêtre dans laquelle vous enregistrez les absences de tous les salariés, avec une ligne par absence.
* La fenêtre **Absences salarié** affiche les absences d'un seul salarié. Les informations affichées sont celles que vous avez entrées dans la fenêtre **Saisie des absences**, filtrées pour ce salarié.

Pour obtenir des statistiques significatives, vous devez toujours utiliser la même unité de mesure (heure ou jour) lors de l'enregistrement des absences des salariés.

## <a name="to-register-employee-absence"></a>Pour enregistrer les absences des salariés
Vous pouvez enregistrer les absences des salariés quotidiennement ou à un autre intervalle qui répond aux besoins de votre organisation.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche**, entrez **Saisie des absences**, puis sélectionnez le lien connexe.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez une ligne pour chaque absence salarié que vous souhaitez enregistrer.
4. Fermez la fenêtre.

    > [!Tip]
    > Pour obtenir des statistiques pertinentes, utilisez toujours la même unité de mesure, heure ou journée, lors de l'enregistrement des absences.

## <a name="to-view-an-individual-employees-absence"></a>Pour visualiser les absences d'un salarié
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche**, entrez **Employés**, puis sélectionnez le lien connexe.
2. Sélectionnez l'employé concerné, puis cliquez sur **Absences**.

    La fenêtre **Absences salariés** affiche toutes les absences et les dates de début et de fin.

## <a name="to-view-an-employees-absence-by-categories"></a>Pour afficher les absences d'un salarié par catégorie
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche**, entrez **Employés**, puis sélectionnez le lien connexe.
2. Sélectionnez l'employé concerné, puis cliquez sur **Absences par catégories**.
3. Dans la fenêtre **Absences salariés par cat.**, renseignez les champs selon vos besoins, puis cliquez sur **Afficher matrice**.

    La fenêtre **Matrice Abs. Salariés par Cat.** s'ouvre et affiche toutes les absences, classées par motif d'absence.

## <a name="to-view-all-employee-absences-by-category"></a>Pour afficher toutes les absences des salariés par catégorie
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche**, entrez **Saisie des absences**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Saisie des absences**, cliquez sur **Détail par catégorie**.
3. Dans la fenêtre **Détail absences par catégorie**, définissez un filtre dans le champ **Filtre n° salarié** afin de visualiser les absences d'un individu ou d'un groupe de salariés.
4. Choisissez l'action **Afficher matrice**.

    La fenêtre **Détail absences par catégorie** s'ouvre et affiche les absences des salariés par motif d'absence.

## <a name="to-view-all-employee-absences-by-period"></a>Pour afficher toutes les absences des salariés par période
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche**, entrez **Saisie des absences**, puis sélectionnez le lien connexe.
   Dans la fenêtre **Saisie des absences**, cliquez sur **Détail par période**.
2. Dans la fenêtre **Détail absences par période**, définissez un filtre dans le champ **Filtre motif absence** afin de visualiser les absences des salariés liées à un motif particulier.
3. Choisissez l'action **Afficher matrice**.

    La fenêtre **Détail absences par période** s'ouvre et affiche les absences des salariés réparties par période.

## <a name="see-also"></a>Voir aussi
[Gérer les ressources humaines](hr-manage-human-resources.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)

