---
title: Utilisation de l'extension C5 Data Migration | Microsoft Docs
description: "Utilisez cette extension pour migrer des clients, des fournisseurs, des articles et des comptes généraux de Microsoft Dynamics C5 2012 vers Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a>L'extension C5 Data Migration pour Dynamics 365 for Finance and Operations, Business Edition
Cette extension facilite la migration de clients, de fournisseurs, d'articles et de vos comptes généraux de Microsoft Dynamics C5 2012 vers [!INCLUDE[d365fin](includes/d365fin_md.md)].  
  
> [!Note] 
> La société dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ne doit pas contenir de données. En outre, après avoir commencé une migration, ne créez pas de clients, de fournisseurs, d'articles, ou de comptes jusqu'à la fin de la migration.

## <a name="to-migrate-data"></a>Pour migrer des données
Quelques étapes suffisent pour exporter des données de C5 et les importer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]:  
  
1. Dans C5, utilisez la fonctionnalité **Exporter la base de données** pour exporter les données. Envoyez ensuite le fichier d'exportation vers un fichier compressé (zippé).  
2. Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Migration de données**, puis sélectionnez **Migration de données**.  
3. Exécutez les étapes du guide de configuration assistée. Veillez à choisir **Importer à partir de Microsoft Dynamcis C5 2012** comme source de données.  

> [!Note] 
> Les sociétés ajoutent souvent des champs pour personnaliser C5 pour leur activité spécifique. [!INCLUDE[d365fin](includes/d365fin_md.md)] n'effectue pas la migration de données à partir des champs personnalisés. En outre, la migration échouera si vous avez plus de 10 champs personnalisés. 

## <a name="viewing-the-status-of-the-migration"></a>Affichage du statut de la migration
Utilisez la page **Vue d’ensemble de la migration des données** pour contrôler la réussite de la migration. La page affiche des informations telles que le nombre d'entités incluses dans la migration, le statut de la migration, ainsi que le nombre d'articles qui ont été migrés et l'état de réussite de leur migration. Elle affiche également le nombre d'erreurs, ce qui vous permet d'étudier ce qui ne s'est pas passé correctement et, si possible, d'accéder facilement à l'entité pour résoudre les problèmes. Pour plus d'informations, voir la section suivante de cette rubrique. 

> [!Note] 
> Pendant que vous attendez les résultats de la migration, vous devez actualiser la page pour afficher les résultats.

## <a name="correcting-errors"></a>Correction des erreur
Si quelque chose se passe mal et qu'une erreur survient, le champ **Statut** affiche **Terminé avec des erreurs**, et le champ **Nombre d'erreurs** en indique le nombre. Pour afficher la liste des erreurs, vous pouvez ouvrir la page **Erreurs de migration des données** en sélectionnant :

* le nombre dans le champ **Nombre d'erreurs** pour l'entité. 
* l'entité, puis l'action **Afficher les erreurs**. 

Dans la page **Erreurs de migration des données**, pour corriger une erreur vous pouvez sélectionner un message d'erreur, puis **Modifier l'enregistrement** pour ouvrir une page qui affiche les données migrées pour l'entité. Après avoir corrigé une ou plusieurs erreurs, vous pouvez sélectionner **Migrer** pour migrer uniquement les entités que vous avez corrigées, sans entièrement redémarrer la migration.  

> [!Tip]
> Si vous avez corrigé plusieurs erreur, vous pouvez utiliser la fonctionnalité **Sélectionner davantage** pour sélectionner plusieurs lignes à migrer. Sinon, s'il existe des erreurs qu'il n'est pas important de corriger, vous pouvez les sélectionner, puis cliquer sur **Ignorer les sélections**.

> [!Note]
> Si vous avez des articles inclus dans une nomenclature, vous pouvez être amené à effectuer la migration plus d'une fois si l'article d'origine n'est pas créé avant les variantes qui y font référence. Si une variante article est créée en premier lieu, la référence à l'article d'origine peut entraîner un message d'erreur.  

## <a name="verifying-data-after-migrating"></a>Vérifier les données après avoir effectué une migration 
Si vous souhaitez vérifier que vos données ont été migrées correctement, vous pouvez consulter les pages suivantes dans C5 et [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Écritures client| Feuilles comptabilité|
|Écritures fournisseur| Feuilles comptabilité|
|Ecritures article| Feuilles article|

Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le lot des données migrées est nommé **C5MIGRATE**. 

## <a name="stopping-data-migration"></a>Arrêter la migration des données
Vous pouvez arrêter de migrer les données en sélectionnant **Arrêter toutes les migrations**. Si vous le faites, toutes les migrations en attente sont également arrêtées.

## <a name="see-also"></a>Voir aussi
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)  
[Bienvenue dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

