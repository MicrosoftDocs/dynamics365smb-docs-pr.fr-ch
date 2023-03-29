---
title: Mappage des tables et des champs à synchroniser | Microsoft Docs
description: "Découvrez comment mapper des tables et des champs pour synchroniser des données entre Business\_Central et Microsoft Dataverse."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Mappage des tables et des champs à synchroniser


La base de la synchronisation des données consiste à mapper les tables et les champs dans [!INCLUDE[prod_short](includes/prod_short.md)] avec des tables et des colonnes dans [!INCLUDE[prod_short](includes/cds_long_md.md)] afin qu’ils échangent les données. Le mappage s’effectue via des tables d’intégration. 

## Mappage de tables d’intégration
Une table d’intégration est une table dans la base de données [!INCLUDE[prod_short](includes/prod_short.md)] qui représente une table, par exemple un compte, dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Les tables d’intégration incluent des champs qui correspondent aux colonnes de la table [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Par exemple, la table d’intégration Compte se connecte à la table Comptes dans [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Il doit y avoir un mappage de table d’intégration pour chaque table dans [!INCLUDE[cds_short_md](includes/cds_short_md.md)] à synchroniser avec les données dans [!INCLUDE[prod_short](includes/prod_short.md)].

Lorsque vous créez la connexion entre les applications, [!INCLUDE[prod_short](includes/prod_short.md)] configure quelques mappages par défaut. Si vous le souhaitez, vous pouvez modifier les mappages de tables. Pour en savoir plus, consultez [Mappage de table standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Si vous avez modifié les mappages par défaut et souhaitez annuler vos modifications, sur la page **Intégration des mappages de table**, choisissez **Utiliser le paramétrage de synchronisation par défaut**.

> [!Note]
> Si vous utilisez une version locale de [!INCLUDE[prod_short](includes/prod_short.md)], les mappages de tables d’intégration sont stockés dans la table 5335 Mappages de tables d’intégration, où vous pouvez afficher et modifier les mappages. Les règles de synchronisation et mappages complexes sont définis dans le codeunit 5341. 

### Mappages supplémentaires 
Les conditions de paiement, les méthodes d’expédition et les transporteurs peuvent changer, et il peut être important de pouvoir les ajuster. Si vous activez la fonctionnalité **Mise à jour de la fonctionnalité : Mapper aux ensembles d’options dans Dataverse sans code** sur la page [Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610), vous pouvez ajouter manuellement des mappages de table d’intégration pour les conditions de paiement (PAYMENT TERMS), les méthodes d’expédition (SHIPMENT METHOD) et les transporteurs (SHIPPING AGENT). Ce mappage peut vous aider à vous assurer que vos stratégies sont les mêmes pour ces configurations dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

### Règles de synchronisation
Un mappage de table d’intégration comprend également des règles qui contrôlent comment les travaux de synchronisation d’intégration synchronisent les enregistrements dans une table dans [!INCLUDE[prod_short](includes/prod_short.md)] et une entité dans [!INCLUDE[prod_short](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

### Stratégies de résolution automatique des conflits
Les conflits de données peuvent facilement se produire lorsque les applications métier échangent des données de manière continue. Par exemple, quelqu’un peut supprimer ou modifier une ligne dans l’une des applications, ou les deux. Pour réduire le nombre de conflits que vous devrez résoudre manuellement, vous pouvez spécifier des stratégies de résolution et [!INCLUDE[prod_short](includes/prod_short.md)] résoudra automatiquement les conflits selon les règles des stratégies.

Les mappages de table d’intégration incluent des règles qui contrôlent la façon dont les tâches travaux de synchronisation synchronisent les enregistrements. Sur la page **Mappage de tables d’intégration**, dans les colonnes **Résoudre les conflits de suppression** et **Résoudre les conflits de mise à jour**, vous pouvez spécifier comment [!INCLUDE[prod_short](includes/prod_short.md)] résoudra les conflits qui se produisent parce que les enregistrements ont été supprimés dans les tables de l’une ou l’autre application métier, ou mis à jour dans les deux. 

Dans la colonne **Résoudre les conflits de suppression**, vous pouvez choisir que [!INCLUDE[prod_short](includes/prod_short.md)] restaure automatiquement les enregistrements supprimés, supprime le couplage entre les enregistrements ou ne fasse rien. Si vous ne faites rien, vous devez résoudre manuellement les conflits. 

Dans la colonne **Résoudre les conflits de mise à jour**, vous pouvez choisir que [!INCLUDE[prod_short](includes/prod_short.md)] envoie automatiquement une mise à jour des données à la table d’intégration lors de l’envoi de données à [!INCLUDE[prod_short](includes/cds_long_md.md)], obtienne une mise à jour des données à partir de la table d’intégration lors de l’obtention de données à partir de [!INCLUDE[prod_short](includes/cds_long_md.md)] ou ne fasse rien. Si vous ne faites rien, vous devez résoudre manuellement les conflits.

Après avoir spécifié la stratégie, sur la page **Erreurs de synchronisation de données couplées**, vous pouvez choisir l’action **Réessayer tout** pour résoudre automatiquement les conflits. 

## Mappage de champs d’intégration
Le mappage de tables ne constitue que la première étape. Vous devez également mapper les champs des tables. Les mappages de champs d’intégration associent les champs dans les tables [!INCLUDE[prod_short](includes/prod_short.md)] avec les colonnes correspondantes dans [!INCLUDE[prod_short](includes/cds_long_md.md)], et déterminent s’il faut synchroniser les données dans chaque table. Le mappage de table standard fourni par [!INCLUDE[prod_short](includes/prod_short.md)] inclut des mappages de champs, mais vous pouvez les modifier si vous le souhaitez. Pour plus d’informations, voir [Affichage des mappages de tables](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Si vous utilisez une version locale de [!INCLUDE[prod_short](includes/prod_short.md)], les mappages de champs d’intégration sont définis dans la table 5336 Mappage de champs d’intégration.

Vous pouvez mapper manuellement les champs, ou automatiser le processus en mappant plusieurs champs en même temps en fonction de critères de correspondance de leurs valeurs. Pour plus d’informations, consultez [Pour coupler plusieurs enregistrements en fonction de la correspondance de leurs valeurs de champ](admin-how-to-couple-and-synchronize-records-manually.md).

### Gestion des différences de valeurs de champ
Parfois, les valeurs des champs que vous souhaitez associer sont différentes. Par exemple, le code langue pour les États-Unis est « U.S. » dans [!INCLUDE[crm_md](includes/crm_md.md)], mais « US » dans [!INCLUDE[prod_short](includes/prod_short.md)]. Autrement dit, vous devez transformer la valeur lorsque vous synchronisez des données. Cela se fait via les règles de transformation que vous définissez pour les champs. Vous définissez des règles de transformation sur la page **Mappages de table d’intégration** en choisissant **Mappage**, puis **Champs**. Des règles prédéfinies sont fournies, mais vous pouvez également créer les vôtres. Pour plus d’informations, voir [Règles de transformation](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### Gestion des valeurs option manquantes dans Mappage
[!INCLUDE[prod_short](includes/cds_long_md.md)] contient des colonnes d’ensembles d’options qui fournissent des valeurs que vous pouvez mapper à des champs [!INCLUDE[prod_short](includes/prod_short.md)] de type **Option** pour la synchronisation automatique. Lors de la synchronisation, les options non mappées sont ignorées et les options manquantes sont ajoutées à la table [!INCLUDE[prod_short](includes/prod_short.md)] associée et à la table système **Mappage option CDS** pour une gestion manuelle ultérieure. Par exemple, en ajoutant les options manquantes dans l’un ou l’autre des produits, puis en mettant à jour le mappage. Pour en savoir plus, consultez [Gestion des valeurs option manquantes](admin-cds-missing-option-values.md).

## Enregistrements couplage
Le couplage associe des lignes dans [!INCLUDE[prod_short](includes/cds_long_md.md)] à des enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, les comptes dans [!INCLUDE[prod_short](includes/cds_long_md.md)] sont généralement associés aux clients dans [!INCLUDE[prod_short](includes/prod_short.md)]. Le couplage d’enregistrements offre les avantages suivants :

* Il rend la synchronisation possible.
* Les utilisateurs peuvent ouvrir des enregistrements ou des lignes dans une application métier, puis une autre. Les applications doivent déjà être intégrées.

Les couplages peuvent être configurés automatiquement à l’aide des projets de synchronisation, ou manuellement en modifiant l’enregistrement dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Synchronisation des données dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) et [Couplage et synchronisation manuels d’enregistrements](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## Filtrage des enregistrements et des lignes  
Si vous ne souhaitez pas synchroniser toutes les lignes pour une table spécifique dans [!INCLUDE[prod_short](includes/cds_long_md.md)] ou une table dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez définir des filtres pour limiter les données synchronisées. Vous configurez des filtres sur la page **Mappages de table d’intégration**.  

#### Pour filtrer des enregistrements ou lignes en vue d’une synchronisation  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Mappages de table d’intégration**, puis choisissez le lien associé.

2.  Pour filtrer les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)], définissez le champ **Filtre table**.  

3.  Pour filtrer les lignes [!INCLUDE[prod_short](includes/cds_long_md.md)], définissez le champ **Filtre table intégration**.  

## Créer des enregistrements  
Par défaut, seuls les enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)] et les lignes dans [!INCLUDE[prod_short](includes/cds_long_md.md)] qui sont couplés seront synchronisés par les projets de synchronisation de l’intégration. Vous pouvez définir des mappages de table afin que des enregistrements ou lignes soient créés dans la destination (par exemple, [!INCLUDE[prod_short](includes/prod_short.md)]) pour chaque ligne de la source (par exemple, [!INCLUDE[prod_short](includes/cds_long_md.md)]) qui n’est pas encore couplé.  

Par exemple, le projet de synchronisation Dynamics 365 Sales - VENDEURS utilise le mappage de table VENDEURS. Le projet de synchronisation copie les données des utilisateurs dans [!INCLUDE[prod_short](includes/cds_long_md.md)] vers les vendeurs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si vous définissez le mappage de table pour créer des enregistrements, pour chaque utilisateur dans [!INCLUDE[prod_short](includes/cds_long_md.md)] qui n’est pas encore couplé à un vendeur dans [!INCLUDE[prod_short](includes/prod_short.md)], une ligne de vendeur est créée dans [!INCLUDE[prod_short](includes/prod_short.md)].  

#### Pour créer des enregistrements durant la synchronisation  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Mappages de table d’intégration**, puis choisissez le lien associé.

2.  Dans l’écriture de mappage de table de la liste, désactivez le champ **Synch. uniquement les enregistrements couplés**.  

## Utiliser des modèles de configuration dans les mappages de table
Vous pouvez affecter des modèles de configuration aux mappages de table à utiliser pour les enregistrements ou lignes créés dans [!INCLUDE[prod_short](includes/prod_short.md)] ou [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour chaque mappage de table, vous pouvez spécifier un modèle de configuration à utiliser pour les nouveaux enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] et un autre modèle à utiliser pour les nouvelles lignes [!INCLUDE[prod_short](includes/cds_long_md.md)].  

Si vous installez la configuration de synchronisation par défaut, deux modèles de configuration sont automatiquement créés et utilisés dans le mappage de table pour les clients [!INCLUDE[prod_short](includes/prod_short.md)] et les comptes [!INCLUDE[crm_md](includes/crm_md.md)] : **CDSCUST** et **CDSACCOUNT**.  

-   **CDSCUST** permet de créer et synchroniser de nouveaux clients dans [!INCLUDE[prod_short](includes/prod_short.md)] sur la base d’un compte dans [!INCLUDE[crm_md](includes/crm_md.md)].  

     Ce modèle est créé en copiant un modèle de configuration existant pour les clients de l’application. Le compte **CDSCUST** est créé seulement s’il existe un modèle de configuration et si le champ **Code devise** du modèle est vide. Si un champ du modèle de configuration contient une valeur, celle-ci est utilisée au lieu de la valeur de colonne mappée dans le compte [!INCLUDE[prod_short](includes/cds_long_md.md)]. Par exemple, si la colonne **Pays/Région** d’un compte dans [!INCLUDE[prod_short](includes/cds_long_md.md)] a la valeur *États-Unis* et le champ **Pays/Région** du modèle de configuration a la valeur *Grande-Bretagne*, alors *Grande-Bretagne* est utilisé comme **Pays/Région** pour le client dans [!INCLUDE[prod_short](includes/prod_short.md)].  

-   Le compte **CDSACCOUNT** permet de créer et synchroniser de nouveaux comptes dans [!INCLUDE[prod_short](includes/cds_long_md.md)] sur la base d’un compte dans [!INCLUDE[prod_short](includes/prod_short.md)].  

#### Pour spécifier des modèles de configuration dans un mappage de table  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Mappages de table d’intégration**, puis choisissez le lien associé.

2.  Dans l’écriture de mappage de table de la liste, dans le champ **Code modèle config. table**, choisissez le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)].  

3.  Configurez le champ **Code modèle config. table int.** dans le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Voir aussi  
[À propos de l’intégration de Dynamics 365 Business Central avec [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synchronisation de Business Central et de [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]