---
title: Migrer des données de Dynamics GP avec l'extension de migration de données | Microsoft Docs
description: Utilisez Migration de données Dynamics GP pour migrer des clients, des fournisseurs, des articles en stock, des comptes généraux, des transactions fournisseurs ouvertes et des transactions clients ouvertes de Dynamics GP vers Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: c5798baec1130c3fc662a8751aee87bb8b438146
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311299"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Migration de données Dynamics GP 
Cette extension permet de migrer des clients, des fournisseurs, des articles en stock, des comptes généraux, des transactions fournisseurs ouvertes et des transactions clients ouvertes de Dynamics GP vers [!INCLUDE[prodshort](includes/prodshort.md)]. Si votre entreprise utilise Dynamics GP aujourd'hui, vous pouvez exporter les enregistrements appropriés, puis ouvrir un guide de configuration assistée pour ajouter les données vers [!INCLUDE[prodshort](includes/prodshort.md)]. L'extension de migration fonctionne pour toutes les versions prises en charge de Microsoft Dynamics GP. Pour plus d'informations, voir [Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportation de données à partir de Dynamics GP
Vous devez avoir exporté certains ou tous vos clients, fournisseurs, articles de stock, et comptes généraux à l'aide de la fonctionnalité pour l'exportation de données dans Dynamics GP. Lorsque vous sélectionnez les données à exporter, les types suivants peuvent être sélectionnés :

* Compte  
* Client  
* Article  
* Fournisseur  

Lorsque le fichier d'exportation est créé, vous avez un fichier zip contenant plusieurs fichiers txt qui sont déterminés selon ce que vous avez sélectionnée lors du processus d'exportation de données.  Il y a aussi des fichiers txt supplémentaires qui sont générés qui contiennent la prise en charge des informations nécessaires à la configuration au sein de votre société [!INCLUDE[prodshort](includes/prodshort.md)].

La migration de données Dynamics GP mappe automatiquement les données exportées afin qu'elles soient rapidement disponibles dans votre nouvelle société [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="whats-new-in-the-october-2018-release"></a>Nouveautés de la version d'octobre 2018

Dans cette version, nous avons étendu la quantité de données introduite dans [!INCLUDE[prodshort](includes/prodshort.md)] depuis Dynamics GP.

Dans l'Assistant de migration, vous pouvez maintenant choisir comment vous souhaitez migrer le plan comptable de Dynamics GP. Vous pouvez migrer le plan comptable existant, ou en créez un selon le plan comptable existant.  

Si vous choisissez d'utiliser le plan comptable existant, les comptes sont configurés comme segment principal de compte de Dynamics GP et les segments supplémentaires sont configurés en tant qu'axes dans [!INCLUDE[prodshort](includes/prodshort.md)].  

Si vous choisissez de créer un plan comptable, vous obtenez une page d'informations sur le compte supplémentaire dans l'assistant afin de pouvoir télécharger le classeur, apporter les modifications appropriées, puis réimporter le classeur pour modifier vos comptes.  

Vous devez télécharger le classeur Excel et mapper un nouveau numéro de compte à chaque numéro de compte du classeur Excel. Chaque compte doit avoir son propre numéro, ou la migration renvoie une erreur. Lorsque vous avez renseigné le mappage, vous pouvez continuer dans l'assistant de migration en important le classeur Excel que vous venez de mettre à jour. L'assistant valide que chaque ligne a un numéro de compte unique et qu'aucune ligne ne contient un nouveau numéro de compte vide.  

Avec la modification du mappage des options du plan comptable, vous noterez également une modification du type de données qui se trouvent dans la feuille comptabilité des numéros de compte.  

- Si vous choisissez d'utiliser des numéros de compte existants, nous apporterons le solde de début du segment principal (nouveau numéro de compte) comme somme du numéro de compte principal au moment de la migration.  
- Si vous choisissez de créer des numéros de compte, nous apporterons des informations récapitulatives pour l'équivalent de deux exercices fiscaux selon les périodes fiscales où vous avez configuré Dynamics GP.

Dans les versions antérieures de [!INCLUDE[prodshort](includes/prodshort.md)], l'assistant migrait une transaction récapitulative pour le solde client/fournisseur dans Dynamics GP. À présent nous apportons les transactions en cours détaillées pour les clients et les fournisseurs au moment de la migration. Qu'est-ce que cela signifie ? Si votre client fait enregistrer 3 transactions restantes enregistrées dans le module Comptes clients, l'assistant migre ces transactions dans [!INCLUDE[prodshort](includes/prodshort.md)] avec le montant restant comme montant de document. C'est la même chose pour le module Fournisseurs des fournisseurs.  

Les articles de stock sont importés avec la méthode d'évaluation du coût sélectionnée lorsque l'assistant de configuration de société a été exécuté. La méthode d'évaluation FIFO est automatiquement affectée aux articles de service. Actuellement nous migrons la Quantité disponible pour les articles au moment de la migration.  Cette quantité est insérée dans le magasin vide.  

La dernière option qui apparaît dans l'assistant Migration de données pour Dynamics GP est la capacité à spécifier votre option de validation. Ce paramètre indique si vous souhaitez valider automatiquement toutes les transactions dans les feuilles comptabilité dès que la migration entre les données vers [!INCLUDE[prodshort](includes/prodshort.md)], ou si vous souhaitez valider manuellement afin que toutes les transactions soient placés en lots dans la page Feuille comptabilité afin de pouvoir vérifier les informations avant de valider. Cette option est visible sur la page Options du plan comptable.


## <a name="see-also"></a>Voir aussi
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Personnalisation de [!INCLUDE[prodshort](includes/prodshort.md)] à l'aide des extensions ](ui-extensions.md)  
