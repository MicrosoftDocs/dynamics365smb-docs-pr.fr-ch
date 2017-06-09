---
title: "Procédure : configurer une assurance immobilisation| Microsoft Docs"
description: "Décrit comment configurer le système pour l&quot;assurance des immobilisations."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6473b74823f787e6b1eac599bb95b6d100a02c1e
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-insurance"></a>Procédure : configurer une assurance immobilisation
Pour gérer la couverture d'assurance des immobilisations, vous devez tout d'abord configurer certaines informations générales d'assurance ainsi qu'une fiche assurance par police.

## <a name="to-set-up-general-insurance-information"></a>Pour définir des informations générales relatives aux assurances
Pour utiliser les fonctions d'assurance dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous devez définir certaines informations générales relatives aux assurances.  

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Paramètres immobilisations**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Pour définir des types d'assurance
Vous pouvez regrouper vos polices d'assurance en catégories (assurances contre le vol, assurances incendie, etc.). Les types d'assurance sont utilisés sur la fiche assurance.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Types assurance**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

## <a name="to-set-up-insurance-cards"></a>Pour définir des fiches assurance
Vous pouvez rassembler des informations sur chaque police d'assurance dans la fiche assurance.  

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Assurance**, puis sélectionnez le lien associé.  
2. Dans la fenêtre **Assurance**, sélectionnez l'action **Nouveau** pour créer une fiche assurance.  
3. Renseignez les champs selon vos besoins.

## <a name="to-set-up-insurance-journal-templates"></a>Pour définir des modèles feuille assurance
[!INCLUDE[d365fin](includes/d365fin_md.md)] crée automatiquement un modèle feuille assurance la première fois que vous ouvrez la fenêtre **Feuille assurance**. Vous pouvez cependant définir d'autres modèles feuille. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).  

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Modèles feuille assurance**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins.

## <a name="to-set-up-insurance-journal-batches"></a>Pour définir des noms de feuille assurance
Vous pouvez définir des feuilles dans un modèle feuille assurance. Les valeurs de la feuille servent de valeurs par défaut si les champs ne sont pas renseignés dans les lignes feuille. Pour en savoir plus, voir [Utiliser des feuilles comptabilité](ui-work-general-journals.md)  

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Modèles feuille assurance**, puis sélectionnez le lien associé.  
2. Sélectionnez un modèle feuille assurance, puis l'action **Lots**.
3. Dans la fenêtre **Lots feuille assurance**, renseignez les champs selon vos besoins.

**Remarque** : les numéros remplissent une fonction spéciale dans les noms de feuille. Si un nom de feuille ou de modèle feuille indique un numéro, ce numéro est incrémenté automatiquement de 1 à chaque fois que la feuille est validée. Par exemple, si vous saisissez HH1 dans le champ **Nom**, la feuille prend le nom HH2 après validation de la feuille HH1.

## <a name="see-also"></a>Voir aussi
[Paramétrage d'immobilisations](fa-setup.md)  
[Immobilisations](fa-manage.md)  
[Finance](finance.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

