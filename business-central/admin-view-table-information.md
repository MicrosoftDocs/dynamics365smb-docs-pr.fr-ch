---
title: Afficher les informations sur les tables
description: Découvrez comment afficher des informations sur les tables de base de données directement depuis l’interface client de Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: db1a5ef84d4174b960de6f3e20f7d4e29c8c44c8
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133111"
---
# <a name="viewing-table-information"></a>Affichage d’informations sur les tables

La page **Informations sur les tables 8700** fournit des informations sur toutes les tables système et métier d’une solution Business Central. En particulier, la page affiche des informations sur la quantité de données contenues dans les tables.

Ces informations sont utiles pour résoudre les problèmes de performances, car nous allons voir la répartition de la taille des données entre les tables.

## <a name="viewing-table-information"></a>Affichage d’informations sur les tables

Pour ouvrir cette page, sélectionnez l’icône ![Rechercher une page ou un état.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Informations table**, puis choisissez le lien associé.

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