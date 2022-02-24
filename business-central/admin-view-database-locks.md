---
title: Afficher les verrouillages base de données
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: abee0f31d66f648f4b0be567d8599b31c536a193
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324117"
---
# <a name="viewing-database-locks"></a>Affichage des verrouillages base de données

## <a name="about-locks"></a>À propos des verrouillages

Les verrouillages base de données contrôlent l'accès simultané de plusieurs utilisateurs aux mêmes données. Pour protéger une transaction contre d'autres transactions modifiant les mêmes données, la première transaction met un verrouillage sur les données. Le verrouillage reste en place jusqu'à la fin de la transaction.

Les utilisateurs peuvent être empêchés d'effectuer des transactions sur les données verrouillées. Ils reçoivent généralement un message indiquant la condition de verrouillage.

## <a name="to-view-database-locks"></a>Pour afficher les verrouillages base de données

Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Verrouillages base de données**, puis sélectionnez le lien associé.

La page **Verrouillages base de données** affiche un aperçu de tous les verrouillages base de données actuels.

Pour en savoir plus sur les verrouillages base de données, consultez [Surveillance des verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) dans l'aide Business Central sur Developer and IT Pro.

## <a name="see-also"></a>Voir aussi

[Surveiller les verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
