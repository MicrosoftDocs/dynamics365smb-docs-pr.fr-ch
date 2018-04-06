---
title: "Procédure de création de packages configuration de société personnalisés | Microsoft Docs"
description: "À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7feaa0e41cf5800ffd51d5807a90f6929492804e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a>Créer des packages configuration de société personnalisés
À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.  

En général, créez un package configuration par domaine fonctionnel, par exemple, créez un package pour la fonctionnalité de fabrication. Cela vous permet d’appliquer et de configurer de nouveaux domaines au sein d’une société en fonction de vos besoins  

Autrement, vous pouvez créer un package qui inclut les tables qui définissent la configuration, par exemple :  

-   Paramètres immobilisations  
-   Paramètres comptabilité  
-   Paramètres stock  
-   Paramètres production  
-   Paramètres achats  
-   Paramètres marketing  
-   Paramètres services  
-   Paramètres ventes  
-   Paramètres entrepôt  
-   Paramètres comptabilisation  
-   Paramètres comptabilisation TVA  
-   Paramètres compta. stock  

Pour afficher la liste complète des tables de configuration, choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres**, puis sélectionnez le lien connexe.  

## <a name="to-create-a-custom-company-configuration-package"></a>Pour créer un package configuration de société personnalisé  
1.  Créez une [!INCLUDE[d365fin](includes/d365fin_md.md)]. ***Lien NON POSSIBLE pour aider à la « création d'un abonné »***.   
2.  Créez une société pour le modèle solution ou secteur d'activité. Pour plus d’informations, voir [Créer une société](admin-how-to-create-a-new-company.md).  
3.  Configurez la nouvelle société en tenant compte de vos besoins. Renseignez toutes les tables de configuration nécessaires.  
4.  Ouvrez la nouvelle société.
5. Ouvrez la fenêtre **Feuille configuration**.  
6.  Ajoutez les tables que vous souhaitez transférer vers une autre société à la feuille. Affectez les lignes feuille au package.  
7.  Créez un questionnaire pour les tables de configuration les plus souvent utilisées.  
8.  Créez des modèles de configuration pour faciliter la création de données de base, telles que les clients ou les articles.  
9.  Exportez votre package comme fichier .rapidstart.  

## <a name="see-also"></a>Voir aussi  
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)

