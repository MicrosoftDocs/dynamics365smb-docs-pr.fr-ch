---
title: Procédure de création de packages configuration de société personnalisés | Microsoft Docs
description: À mesure que vous développez votre activité, vous êtes susceptible d’utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e1cf9d530c8af95373cfbdef8a3f6822cbba938
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915799"
---
# <a name="create-custom-company-configuration-packages"></a>Créer des packages configuration de société personnalisés
À mesure que vous développez votre activité, vous êtes susceptible d’utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.  

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

Pour visualiser la liste complète des tables de configuration, choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Configuration manuelle** , puis sélectionnez le lien associé.  

> [!IMPORTANT]
> Soyez prudent si vous choisissez des tables ou des champs qui portent le même nom temporel mais sont différenciés par des caractères spéciaux, tels que %, &, <, >, (, et ). Par exemple, la table « XYZ » peut contenir les champs « Champ 1 » et « Champ 1 % ».
>
> Le processeur XML n’accepte que certains caractères spéciaux et supprime ceux qu’il n’accepte pas. Si la suppression d’un caractère spécial, tel que le signe % dans « Champ 1 % », génère deux ou plusieurs tables ou champs avec le même nom, une erreur se produit lorsque vous exportez ou importez un package de configuration.

## <a name="to-create-a-custom-company-configuration-package"></a>Pour créer un package configuration de société personnalisé  
1.  Créez une nouvelle société. Pour plus d’informations, voir [Création de sociétés dans Business Central](about-new-company.md).  
3.  Configurez la nouvelle société en tenant compte de vos besoins. Renseignez toutes les tables de configuration nécessaires.  
4.  Ouvrez la nouvelle société.
5. Ouvrir la page **Feuille configuration** .  
6.  Ajoutez les tables que vous souhaitez transférer vers une autre société à la feuille. Affectez les lignes feuille au package.  
7.  Créez un questionnaire pour les tables de configuration les plus souvent utilisées.  
8.  Créez des modèles de configuration pour faciliter la création de données de base, telles que les clients ou les articles.  
9.  Exportez votre package comme fichier .rapidstart.  

## <a name="see-also"></a>Voir aussi  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]