---
title: Afficher les informations sur les tables
description: Découvrez comment afficher des informations sur les tables de base de données directement depuis l’interface client de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776906"
---
# <a name="viewing-table-information"></a>Affichage d’informations sur les tables

La page **Informations sur les tables 8700** fournit des informations sur toutes les tables système et métier d’une solution Business Central. En particulier, la page affiche des informations sur la quantité de données contenues dans les tables.

Ces informations sont utiles pour résoudre les problèmes de performances, car nous allons voir la répartition de la taille des données entre les tables.

## <a name="viewing-table-information"></a>Affichage d’informations sur les tables

Pour ouvrir cette page, sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Informations sur les tables**, puis sélectionnez le lien connexe.

Le tableau suivant décrit les informations fournies pour chaque table :

|Colonne|Description|
|------|-----------|
|Nom de la société|Nom de la société, si existant, à laquelle appartient la table.|
|Nom de la table|Nom de la table.|
|Numéro table|ID unique de la table|
|Non. d’enregistrements|Nombre total d’enregistrements stockés dans la table.|
|Taille enregistrement|La taille d’enregistrement moyenne en Ko/enregistrement. La valeur est calculée à l’aide de la formule suivante : 1024 (Taille)/N° d’enregistrements)`. |

## <a name="see-also"></a>Voir aussi

[Inspection des pages](across-inspect-page.md)  
[Articles sur les performances pour les développeurs](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]