---
title: "Utilisez Excel pour entrer les données héritées dans Financials | Microsoft Docs"
description: "Utilisez le package de configuration par défaut pour ajouter des données client dans Excel et les importer ensuite dans Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0151b1c3d8bddd4692c494d1c0e5d1c036da424e
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importation des données à partir du logiciel de comptabilité hérité à l'aide d'un package de configuration
Vous pouvez importer des données de base et des données transactionnelles à partir d'autres systèmes financiers basés sur le package de configuration par défaut dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans la fenêtre **Packages configuration**, vous pouvez utiliser le package pour importer et valider les données avant d'appliquer le package.  

Si vous connaissez les services RapidStart pour Microsoft Dynamics, vous connaissez également les packages de configuration. Le package de configuration par défaut prend en charge les types les plus courants de données à importer à partir d'un système hérité. Dans Excel, vous pouvez ensuite ajouter les données à partir du système hérité et les configurer en fonction de la logique métier du [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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

## <a name="importing-customer-data"></a>Importation de données client
Une fois les données client entrées dans Excel, vous devez les importer dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans la fenêtre **Packages configuration**, vous devez importer les données à partir du fichier Excel et vous pouvez vérifier leur cohérence avec [!INCLUDE[d365fin](includes/d365fin_md.md)] avant d'appliquer le package.

## <a name="see-also"></a>Voir aussi
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
