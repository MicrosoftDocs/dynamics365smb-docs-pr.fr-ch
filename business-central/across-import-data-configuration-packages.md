---
title: Utiliser Excel pour importer des données dans Business Central
description: Utilisez le package de configuration par défaut pour ajouter des données client dans Excel et les importer ensuite dans Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'migration, Excel'
ms.date: 05/10/2022
ms.author: edupont
---
# <a name="import-business-data-from-other-finance-systems"></a><a name="import-business-data-from-other-finance-systems"></a>Importer des données métier à partir d’autres systèmes financiers

Lorsque vous effectuez votre inscription à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez choisir de créer une société vierge afin d’être en mesure de télécharger vos propres données et de tester votre société [!INCLUDE[prod_short](includes/prod_short.md)]. En fonction de la solution financière qu’utilise votre société aujourd’hui, vous pouvez transférer des informations sur les clients, les fournisseurs, le stock et les comptes bancaires.  

À partir du tableau de bord, vous pouvez lancer un guide de configuration assistée qui vous aide à transférer les données d’entreprise à partir d’un fichier Excel ou d’autres formats. Le type de fichiers que vous pouvez télécharger dépend des extensions disponibles. Par exemple, vous pouvez migrer des données à partir de QuickBooks, car [!INCLUDE[prod_short](includes/prod_short.md)] comprend une extension qui gère la conversion à partir de QuickBooks. Si vous souhaitez migrer des données à partir d’autres solutions financières, vous devez vérifier qu’une extension est disponible pour cette solution ou effectuer l’importation à partir d’Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] n’inclut pas de modèles pour les comptes, les clients, les fournisseurs ni les articles en stock que vous pouvez choisir d’appliquer lorsque vous importez vos données. Pour importer des images d’article, utilisez une fonction dédiée sur la page **Paramètres stock**. Pour plus d’informations, reportez-vous à la section [Importer plusieurs images d’article](inventory-how-import-item-pictures.md).

> [!TIP]  
> Nous vous recommandons d’utiliser l’assistant de migration de données pour importer des données de Dynamics GP, Dynamics NAV ou de QuickBooks. Pour plus d’informations, voir [Migrer des données locales vers Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) dans le contenu d’administration ou [Migration des données QuickBooks](ui-extensions-quickbooks-data-migration.md).

## <a name="work-with-data-in-excel"></a><a name="work-with-data-in-excel"></a>Utiliser des données dans Excel

Vous pouvez utiliser le module complémentaire pour Excel pour préparer le contenu existant à son utilisation dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Affichage et édition dans Excel depuis Business Central](across-work-with-excel.md).  

## <a name="import-data-from-configuration-packages"></a><a name="import-data-from-configuration-packages"></a>Importer des données à partir des packages de configuration

Pour une implémentation plus large, configurez des packages de configuration spécifiques à la solution. Pour plus d’informations, voir [Configurer les packages de configuration de la société](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (en anglais uniquement) dans le contenu d’administration.  

> [!NOTE]  
> L’utilisation des packages de configuration est une fonctionnalité avancée et il est préférable de contacter votre partenaire revendeur. Pour plus d’informations, voir [Configurer les packages de configuration de la société](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (en anglais uniquement).

Vous pouvez importer des données de base et des données transactionnelles à partir d’autres systèmes financiers basés sur le package de configuration par défaut dans [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Packages configuration**, vous pouvez utiliser le package pour importer et valider les données avant d’appliquer le package. Par exemple, vous pouvez exporter le package de configuration vers Excel et y configurer vos données. Vous pouvez alors importer les données à nouveau à partir d’Excel. Le package se compose de 27 tables, notamment des données de base telles que les clients, les fournisseurs, les articles, et les comptes, d’autres tables de configuration de base telles que les méthodes d’expédition, et les tables de transactions telles que l’en-tête vente et les lignes.  

Lorsque vous exportez le package de configuration par défaut dans Excel, le classeur généré contient une feuille de calcul pour chaque table du package. Pour simplifier vos tâches, vous pouvez mettre à profit les outils de gestion XML qui sont intégrés à Excel. Vous pouvez également utiliser les fonctions intégrées d’Excel pour procéder au formatage des données et placer des données dans la cellule qui convient. Ajoutez par exemple une feuille vide et copiez-y les données héritées. Ensuite, créez une formule Excel permettant d’associer les données de la feuille de calcul de transformation entre les champs de la feuille de calcul exportée et les données héritées du client. Après avoir associé toutes les données, copiez la plage de données dans la feuille de calcul de la table.  

> [!IMPORTANT]  
> Ne modifiez pas les colonnes dans les feuilles de calcul. Si elles sont déplacées, modifiées ou supprimées, la feuille de calcul ne peut pas être importée dans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Les champs de type Blob ne peuvent pas être exportés/importés à l’aide d’Excel.

### <a name="tables-in-the-default-configuration-package"></a><a name="tables-in-the-default-configuration-package"></a>Tables dans le package de configuration par défaut

Le package de configuration par défaut prend en charge les tables suivantes :

- Conditions de paiement
- Groupe prix client
- Conditions de livraison
- Vendeur/Acheteur
- Emplacement
- Compte général
- Client
- Fournisseur
- Article
- En-tête vente
- Ligne vente
- En-tête achat
- Ligne achat
- Groupe. Ligne feuille
- Ligne feuille article
- Groupe compta. client
- Groupe compta. fournisseur
- Groupe compta. stock
- Unité
- Groupe. compta. marché
- Groupe. Groupe compta. produit
- Paramètres comptabilisation
- Secteur
- Catégorie article
- Prix vente
- Prix achat

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Migration des données locales vers Business Central Online (en anglais uniquement)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Configurer les packages de configuration de la société](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[Extension QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md)  
[Importer plusieurs images d’article](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
