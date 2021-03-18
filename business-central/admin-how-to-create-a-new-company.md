---
title: Procédure de création d’une société | Microsoft Docs
description: Lorsque vous utilisez RapidStart Services, des tables et des pages sont créées, mais elles ne contiennent pas de données.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 703b70a608bd6b25b9a3218eb59e8666fcd6a0ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378338"
---
# <a name="create-a-new-company"></a>Créer une société
Pour utiliser RapidStart Services pour [!INCLUDE[prod_short](includes/prod_short.md)], vous devez d’abord créer une société pour laquelle vous souhaitez effectuer une implémentation client. Lorsque vous créez une société, les tables et les pages standard de [!INCLUDE[prod_short](includes/prod_short.md)] sont créées, mais elles ne contiennent pas de données.

Vous pouvez également appliquer des données de configuration spécifiques à votre société après l’avoir initialisée. Les informations sont fournies dans un package de configuration, un fichier .rapidstart, qui fournit le contenu sous un format compressé.  

Des exemples de packages de configuration, qui comprennent des fichiers spécifiques à un pays/une région, sont inclus avec la société de démonstration CRONUS. Suivez la procédure suivante pour utiliser l’exemple de package de configuration avec une nouvelle société.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Pour utiliser l’exemple de package de configuration BASICCONFIG  
1. Ouvrez la société CRONUS International Ltd. Pour plus d’informations, voir [Modifier les paramètres de base](ui-change-basic-settings.md).
2. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Packages configuration**, puis choisissez le lien associé.  
3. Sélectionnez le package BASICCONFIG dans la liste, puis sélectionnez l’action **Exporter package**.  

Suivez la procédure suivante pour créer une société, puis utilisez le package BASICCONFIG dans le cadre du processus.  

## <a name="to-create-a-new-company"></a>Création d’une nouvelle société  
1. Créez une nouvelle société. Pour plus d’informations, voir [Création de sociétés dans [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Dans le tableau de bord Responsable de l’implémentation de RapidStart Services, vous pouvez maintenant importer le package de configuration que vous avez exporté de la société CRONUS International Ltd.

Une fois que vous avez créé une société, certaines tables se renseignent automatiquement, même si aucun modèle de société n’est appliqué. Par exemple, vous pouvez consulter les codes standard pour les transactions par lots et la validation sur la page **Code origine**. Si vous disposez d’une version locale de [!INCLUDE[prod_short](includes/prod_short.md)], consultez cette table en tenant compte d’éventuels problèmes de langue locale.

## <a name="about-data-tables"></a>À propos des tables de données
Les tables de données [!INCLUDE[prod_short](includes/prod_short.md)] existent en deux types de base : principale et Paramètres. Lorsque vous paramétrez une configuration de société, vous pouvez utiliser ces types afin de cibler votre stratégie de configuration.  

### <a name="master-data-tables"></a>Tables de données principales  
Le tableau suivant répertorie certaines tables de données principales. Lorsque vous lancez une nouvelle société, ces tables sont vides.  

|N° table|Nom de table|  
|-------------------|--------------------|  
|15|Compte général|  
|18|Client|  
|23|Fournisseur|  
|27|Article|  
|5050|Contact|  

### <a name="setup-data-tables"></a>Tables de données de configuration  
Le tableau suivant répertorie certaines tables de données de configuration à partir desquelles vous capturez les informations de configuration dans le questionnaire de configuration. Ces tables contiennent des informations de base lors de la création de la société.  

|N° table|Nom de table|  
|-------------------|--------------------|  
|98|Paramètres comptabilité|  
|311|Paramètres ventes|  
|312|Paramètres achats|  
|313|Paramètres stock|  

Outre des tables de données de paramétrage, [!INCLUDE[prod_short](includes/prod_short.md)] dispose également de tables de données de type paramétrage qui spécifient des informations de base sur la société et ses processus entreprise. Le tableau suivant répertorie certaines d’entre elles.  

|N° table|Nom de table|  
|-------------------|--------------------|  
|3|Conditions de paiement|  
|4|Devise|  
|6|Groupes prix client|  
|5700|Point de stock|

  

## <a name="see-also"></a>Voir aussi  
[Appliquer des configurations aux nouvelles sociétés](admin-apply-configuration-to-new-companies.md)  
[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]