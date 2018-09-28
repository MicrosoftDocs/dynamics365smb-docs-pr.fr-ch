---
title: "Utiliser Excel pour importer des données dans Business Central| Microsoft Docs"
description: "Utilisez le package de configuration par défaut pour ajouter des données client dans Excel et les importer ensuite dans Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 45a236dfeb7a5ce489cf8917d6a08a92ca5c4e8b
ms.contentlocale: fr-ch
ms.lasthandoff: 06/28/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importation des données métier à partir d'autres systèmes financiers
Lorsque vous effectuez votre inscription à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez choisir de créer une société vierge afin d'être en mesure de télécharger vos propres données et de tester votre société [!INCLUDE[d365fin](includes/d365fin_md.md)]. En fonction de la solution financière qu'utilise votre société aujourd'hui, vous pouvez transférer des informations sur les clients, les fournisseurs, le stock et les comptes bancaires.  

À partir du tableau de bord, vous pouvez lancer un guide de configuration assistée qui vous aide à transférer les données d'entreprise à partir d'un fichier Excel ou d'autres formats. Le type de fichiers que vous pouvez télécharger dépend des extensions disponibles. Par exemple, vous pouvez migrer des données à partir de QuickBooks, car [!INCLUDE[d365fin](includes/d365fin_md.md)] comprend une extension qui gère la conversion à partir de QuickBooks. Si vous souhaitez migrer des données à partir d'autres solutions financières, vous devez vérifier qu'une extension est disponible pour cette solution ou effectuer l'importation à partir d'Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] n'inclut pas de modèles pour les comptes, les clients, les fournisseurs ni les articles en stock que vous pouvez choisir d'appliquer lorsque vous importez vos données.

Vous pouvez importer des données de base et des données transactionnelles à partir d'autres systèmes financiers basés sur le package de configuration par défaut dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans la fenêtre **Packages configuration**, vous pouvez utiliser le package pour importer et valider les données avant d'appliquer le package.  

> [!TIP]  
> Sinon, utilisez l'assistant de migration de données pour importer des données de QuickBooks ou de Dynamics GP. Pour plus d'informations, voir [Migration de données QuickBooks](ui-extensions-quickbooks-data-migration.md) ou [Migration de données Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> Pour des travaux d'implémentation plus importants, vous pouvez utiliser RapidStart Services pour [!INCLUDE[d365fin](includes/d365fin_md.md)], une boîte à outils étendue de configuration de nouvelles solutions basées sur les besoins métier et les données de configuration des clients. Les services RapidStart offrent également une fonctionnalité d'importation des données métier. Pour plus d'informations, voir [Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

## <a name="importing-data-from-configuration-packages"></a>Importation des données à partir des packages configuration
[!INCLUDE[d365fin](includes/d365fin_md.md)] inclut un package de configuration que vous pouvez exporter vers Excel et y installe vos données. Vous pouvez alors importer les données à nouveau à partir d'Excel. Le package se compose de 27 tables, notamment des données de base telles que les clients, les fournisseurs, les articles, et les comptes, d'autres tables de configuration de base telles que les méthodes d'expédition, et les tables de transactions telles que l'en-tête vente et les lignes.  

> [!NOTE]  
>   L'utilisation des packages de configuration est une fonctionnalité avancée, et il est préférable de contacter votre administrateur. Pour plus d'informations, voir [Importation des données à partir du logiciel de comptabilité hérité à l'aide d'un package de configuration](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Utilisation de données dans Excel
Lorsque vous exportez le package de configuration par défaut dans Excel, le classeur généré contient une feuille de calcul pour chaque table du package. Pour simplifier vos tâches, vous pouvez mettre à profit les outils de gestion XML qui sont intégrés à Excel. Vous pouvez également utiliser les fonctions intégrées d'Excel pour procéder au formatage des données et placer des données dans la cellule qui convient. Ajoutez par exemple une feuille vide et copiez-y les données héritées. Ensuite, créez une formule Excel permettant d'associer les données de la feuille de calcul de transformation entre les champs de la feuille de calcul exportée et les données héritées du client. Après avoir associé toutes les données, copiez la plage de données dans la feuille de calcul de la table.  

> [!IMPORTANT]  
>  Ne modifiez pas les colonnes dans les feuilles de calcul. Si elles sont déplacées, modifiées ou supprimées, la feuille de calcul ne peut pas être importée dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Tables dans le package de configuration par défaut
Le package de configuration par défaut prend en charge les tables suivantes :

-   Conditions de paiement
-   Groupe prix client
-   Conditions de livraison
-   Vendeur/Acheteur
-   Emplacement
-   Compte général
-   Client
-   Fournisseur
-   Article
-   En-tête vente
-   Ligne vente
-   En-tête achat
-   Ligne achat
-   Ligne feuille comptabilité
-   Ligne feuille article
-   Groupe compta. client
-   Groupe compta. fournisseur
-   Groupe compta. stock
-   Unité
-   Groupe compta. marché
-   Groupe compta. produit
-   Paramètres comptabilisation
-   Secteur
-   Catégorie article
-   Prix vente
-   Prix achat

## <a name="see-also"></a>Voir aussi
[Configuration d'une société avec RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Extension QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md)  
[Extension Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

