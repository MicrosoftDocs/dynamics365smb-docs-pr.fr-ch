---
title: Afficher les verrouillages base de données
description: Découvrez comment afficher des informations sur les verrouillages de base de données client directement depuis l’interface client de Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 0a2561eea331ffbaeb058dee2ee13caf0a82d18c
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143701"
---
# <a name="viewing-database-locks"></a>Affichage des verrouillages base de données

Les verrouillages base de données contrôlent l’accès simultané de plusieurs utilisateurs aux mêmes données. Pour protéger une transaction contre d’autres transactions modifiant les mêmes données, la première transaction met un verrouillage sur les données. Le verrouillage reste en place jusqu’à la fin de la transaction.

Les utilisateurs peuvent être empêchés d’effectuer des transactions sur les données verrouillées. Ils reçoivent généralement un message indiquant la condition de verrouillage.

## <a name="to-view-database-locks"></a>Pour afficher les verrouillages base de données

Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Verrouillages de base de données**, puis choisissez le lien associé.

La page **Verrouillages base de données** affiche un aperçu de tous les verrouillages base de données actuels.

Pour en savoir plus sur les verrouillages base de données, consultez [Surveillance des verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) dans l’aide Business Central sur Developer and IT Pro.

## <a name="see-also"></a>Voir aussi

[Surveiller les verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]