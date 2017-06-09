---
title: "Procédure : configurer des cycles de vente opportunité et des étapes de cycle | Microsoft Docs"
description: "Décrit comment configurer des cycles de vente opportunité et des étapes dans Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Procédure : configurer des cycles de vente opportunité et des étapes de cycle
Avant de pouvoir utiliser les opportunités de vente, vous devez configurer les cycles de vente et les étapes correspondantes. Un cycle de vente est composé d'une série d'étapes allant du contact initial à la fermeture d'une vente. Chaque étape peut avoir certaines exigences à respecter, par exemple pour un devis, avant qu'une opportunité puisse accéder à l'étape suivante. Vous pouvez également spécifier si une étape peut être ignorée. Vous pouvez configurer autant de cycles de vente et d'étapes que nécessaire.

Mettre en œuvre des cycles de vente opportunité implique la création d'un code cycle de vente, la définition des différentes étapes du cycle, puis l'affectation du cycle à des opportunités.

## <a name="to-set-up-an-opportunity-sales-cycle-code"></a>Pour configurer un code cycle de vente opportunité
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Cycles de vente**, puis sélectionnez le lien associé. La fenêtre **Cycles de vente** s'affiche, et répertorie tous les cycles de vente existants.
2. Sélectionnez l'action **Nouveau**, et renseignez les champs .

Répétez ces étapes pour chaque cycle de vente à configurer. Une fois les cycles de vente opportunité configurés, vous pouvez définir les différentes étapes de chaque cycle.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Pour définir les étapes du cycle de vente opportunité
1. Dans la fenêtre **Cycles de vente**, sélectionnez le cycle de vente opportunité pour lequel vous souhaitez définir des étapes, puis sélectionnez l'action **Etapes**. La fenêtre **Etapes cycle de vente** s'affiche.
2. Sélectionnez l'action **Nouveau** pour intégrer une nouvelle étape dans le cycle de vente.

Répétez ces étapes pour définir toutes les étapes du cycle de vente.

## <a name="to-assign-stage-cycle-to-an-opportunity"></a>Pour affecter un cycle d'étapes à une opportunité
Après avoir ajouté le cycle d'étapes opportunité, vous pouvez commencer à ajouter des opportunités de vente, puis affecter le cycle d'étapes aux opportunités en définissant le champ **Code cycle de vente**. Pour plus d'informations, reportez-vous à [Procédure : créer des opportunités de vente](marketing-how-create-opportunities.md).

## <a name="see-also"></a>Voir aussi
[Traitement des opportunités de vente](marketing-processing-sales-opportunities.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

