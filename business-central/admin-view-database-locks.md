---
title: Afficher les verrouillages base de données
description: "Découvrez comment afficher des informations sur les verrouillages de base de données client directement depuis l’interface client de Business\_Central."
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Affichage des verrouillages base de données

Les verrouillages base de données contrôlent l’accès simultané de plusieurs utilisateurs aux mêmes données. Pour protéger une transaction contre d’autres transactions modifiant les mêmes données, la première transaction met un verrouillage sur les données. Le verrouillage reste en place jusqu’à la fin de la transaction.

Les utilisateurs peuvent être empêchés d’effectuer des transactions sur les données verrouillées. Ils reçoivent généralement un message indiquant la condition de verrouillage.

## Pour afficher les verrouillages base de données

Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Verrouillages de base de données**, puis choisissez le lien associé.

La page **Verrouillages base de données** affiche un aperçu de tous les verrouillages base de données actuels.

Pour en savoir plus sur les verrouillages base de données, consultez [Surveillance des verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) dans l’aide Business Central sur Developer and IT Pro.

## Voir aussi

[Surveiller les verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]