---
title: Conseils - RapidStart Services | Microsoft Docs
description: Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e301d788fdedacf0fc2ac3ce29946df965bed711
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777081"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Conseils : RapidStart Services

Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.  

## <a name="take-advantage-of-configuration-templates"></a>Optimisation des modèles de société

Les modèles de configuration peuvent vous aider à rationaliser votre processus d’implémentation. Ces modèles vous permettent d’inclure des clients similaires dans des segments, puis de développer un protocole d’implémentation qui traite tous les clients d’un segment de la même façon. Vous pouvez ainsi appliquer un niveau de préconfiguration à chaque segment et procéder rapidement à une implémentation.  

## <a name="configuration-questionnaires"></a>Questionnaires de configuration

Pour faciliter le remplissage d’un questionnaire de configuration, envisagez de définir des réponses par défaut pour indiquer des recommandations.  

## <a name="batch-creation-of-journal-lines"></a>Création de lignes feuille par lots

Il est recommandé d’utiliser les outils de migration de données fournis pour migrer des écritures feuille. Sinon, si vous utilisez le traitement par lots pour créer des lignes feuille, celui-ci a une portée limitée et ne génère que des champs par défaut dans une feuille. Le reste de la feuille doit ensuite être renseigné manuellement.  

## <a name="migrating-transactions"></a>Migration des transactions

Il est recommandé de migrer des soldes ouverts dans l’ordre suivant. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Migrez les soldes ouverts de la comptabilité sans utiliser la comptabilité auxiliaire. Utilisez des comptes de compensation propres aux soldes ouverts, avec une configuration pour chaque comptabilité auxiliaire. Configurez les comptes de compensation de manière à activer les imputations directes.  
2. Migration des écritures comptables client ouvertes.  <!--work on these-->
3. Migrez les écritures comptables article ouvertes.  
4. Migrez les écritures comptables immobilisation ouvertes.  

## <a name="make-each-package-manageable"></a>Rendre chaque paquet gérable

Lorsque vous utilisez des packages de configuration pour migrer des données, séparez les données en packages séparés pour une portabilité plus facile. Par exemple, si vous souhaitez migrer 20 ans d’écritures comptables, l’importation peut prendre plusieurs heures et jours. Au lieu de cela, divisez les données afin que chaque package devienne plus gérable. Actuellement, il n’y a pas de règles fermes pour rendre un package performant, mais si vous rencontrez des problèmes lors de l’importation ou de l’exportation d’un package, essayez de le réduire et voyez si cela aide.  

## <a name="see-also"></a>Voir aussi

[Configuration d’une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]