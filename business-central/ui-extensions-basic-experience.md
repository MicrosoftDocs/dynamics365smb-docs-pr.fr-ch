---
title: Extension d’expérience de base | Microsoft Docs
description: Cette extension est une alternative modernisée à Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="the-basic-experience-extension"></a><a name="the-basic-experience-extension"></a><a name="the-basic-experience-extension"></a>Extension d’expérience de base

Si vous utilisez Microsoft Dynamics C5, les partenaires Microsoft peuvent vous aider à effectuer la transition vers une solution plus moderne basée sur [!INCLUDE[prod_short](includes/prod_short.md)], afin que vous puissiez continuer à profiter des mêmes fonctionnalités rationalisées que Dynamics C5.

Cette extension est destinée aux petites entreprises et peut prendre en charge jusqu’à trois utilisateurs. Si vous avez besoin de plus d’utilisateurs, vous devez passer à une licence [!INCLUDE[prod_short](includes/prod_short.md)] et désinstallez cette extension.

> [!NOTE]
> À partir de maintenant, cette extension n’est disponible que pour les clients au Danemark et en Islande.

## <a name="whats-available"></a><a name="whats-available"></a><a name="whats-available"></a>Ce qui est disponible

Le tableau suivant décrit les fonctionnalités disponibles si vous installez l’extension d’expérience de base.

|Zone  |Fonctionnalité  |
|---------|---------|
|**Écritures comptables** |Finance de base, Calendriers de comptes, Immobilisations, Gestion bancaire, Rapprochement bancaire, Paiements, Prélèvement, Axes analytiques, Devises multiples, Budgets, Workflow, Gestion de documents/OCR, Consolidation, Sociétés illimitées|
|**Comptabilités client/Ventes** |Comptabilité client de base, Facturation des ventes, Remises sur les ventes, Tarification, Taxe, Gestion des contacts |
|**Comptabilité fournisseur/Achats** |Comptabilité fournisseur de base, Facturation des achats |
|**Gestion de projets** |Projets, Tarification de projet, Feuilles de temps, Affectation, Tâches, Ressources |
|**Stock** |Stock de base, Substitutions d’articles, Références croisées d’articles |

## <a name="getting-started"></a><a name="getting-started"></a><a name="getting-started"></a>Mise en route

Cette extension est un peu différente de la plupart des autres, et vous aurez besoin de l’aide d’un partenaire Microsoft pour l’installer et la configurer. Juste pour que vous sachiez à quoi vous attendre, voici une vue d’ensemble de ce que fera le partenaire Microsoft.

1. Créer un abonné [!INCLUDE[prod_short](includes/prod_short.md)]. Il peut s’agir d’une version d’essai ou d’une version CSP.
2. Ajoutez au moins un utilisateur affecté à une licence d’expérience de base dans votre compte Azure Active Directory.
3. Supprimez toutes les sociétés, y compris l’exemple de société Cronus.
4. Créez une société qui ne contient aucun exemple de données ou de configuration.
5. Ajoutez le package **Démo RapidStart**. <!--what does the package contain?-->
6. Téléchargez et installez l’extension d’expérience de base à partir de AppSource.

## <a name="migrating-data"></a><a name="migrating-data"></a><a name="migrating-data"></a>Migration des données

Importez vos données Dynamics C5. Une fois que votre partenaire Microsoft a installé l’extension d’expérience de base, vous aurez une société vide. Un moyen simple de déplacer vos données de Dynamics C5 vers l’expérience de base consiste à utiliser l’extension de migration de données C5, incluse dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’extension migre les clients, les fournisseurs, les articles et vos comptes généraux et leurs écritures.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Extension C5 Data Migration](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
