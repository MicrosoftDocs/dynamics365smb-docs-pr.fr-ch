---
title: Afficher les verrouillages base de données
description: Découvrez comment afficher des informations sur les verrouillages de base de données directement depuis l’interface client de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b53677ab57d6c48b015bb0dd47ea6e315f8e80c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776931"
---
# <a name="viewing-database-locks"></a>Affichage des verrouillages base de données

Les verrouillages base de données contrôlent l’accès simultané de plusieurs utilisateurs aux mêmes données. Pour protéger une transaction contre d’autres transactions modifiant les mêmes données, la première transaction met un verrouillage sur les données. Le verrouillage reste en place jusqu’à la fin de la transaction.

Les utilisateurs peuvent être empêchés d’effectuer des transactions sur les données verrouillées. Ils reçoivent généralement un message indiquant la condition de verrouillage.

## <a name="to-view-database-locks"></a>Pour afficher les verrouillages base de données

Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Verrouillages base de données**, puis sélectionnez le lien associé.

La page **Verrouillages base de données** affiche un aperçu de tous les verrouillages base de données actuels.

Pour en savoir plus sur les verrouillages base de données, consultez [Surveillance des verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) dans l’aide Business Central sur Developer and IT Pro.

## <a name="see-also"></a>Voir aussi

[Surveiller les verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]