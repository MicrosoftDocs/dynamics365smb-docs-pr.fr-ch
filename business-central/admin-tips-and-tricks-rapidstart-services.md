---
title: Conseils - RapidStart Services | Microsoft Docs
description: "Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation."
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
ms.openlocfilehash: 4e8dc4436b01f69292a01afbc7a5d0381b544a77
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a>Conseils : RapidStart Services
Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.  

## <a name="take-advantage-of-configuration-templates"></a>Optimisation des modèles de société  
Les modèles de configuration peuvent vous aider à rationaliser votre processus d’implémentation. Ces modèles vous permettent d'inclure des clients similaires dans des segments, puis de développer un protocole d'implémentation qui traite tous les clients d'un segment de la même façon. Vous pouvez ainsi appliquer un niveau de préconfiguration à chaque segment et procéder rapidement à une implémentation.  

## <a name="configuration-questionnaires"></a>Questionnaires de configuration  
Pour faciliter le remplissage d’un questionnaire de configuration, envisagez de définir des réponses par défaut pour indiquer des recommandations.  

## <a name="batch-creation-of-journal-lines"></a>Création de lignes feuille par lots  
Il est recommandé d'utiliser les outils de migration de données fournis pour migrer des écritures feuille. Sinon, si vous utilisez le traitement par lots pour créer des lignes feuille, celui-ci a une portée limitée et ne génère que des champs par défaut dans une feuille. Le reste de la feuille doit ensuite être renseigné manuellement.  

## <a name="migrating-transactions"></a>Migration des transactions  
Il est recommandé de migrer des soldes ouverts dans l'ordre suivant.  

1.  Migrez les soldes ouverts de la comptabilité sans utiliser la comptabilité auxiliaire. Utilisez des comptes de compensation propres aux soldes ouverts, avec une configuration pour chaque comptabilité auxiliaire. Configurez les comptes de compensation de manière à activer les imputations directes.  
2.  Migration des écritures comptables client ouvertes.  
3.  Migrez les écritures comptables article ouvertes.  
4.  Migrez les écritures comptables immobilisation ouvertes.  

## <a name="see-also"></a>Voir aussi  
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
