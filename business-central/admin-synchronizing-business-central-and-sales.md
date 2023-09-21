---
title: Synchronisation et intégration des données | Microsoft Docs
description: "La synchronisation copie les données entre les tables Microsoft Dataverse et les enregistrements de Business\_Central et conserve les données à jour dans les deux systèmes."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Synchronisation des données dans Business Central avec Microsoft Dataverse

Lorsque vous intégrez [!INCLUDE[prod_short](includes/cds_long_md.md)] avec [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez décider si vous souhaitez synchroniser les données dans les champs sélectionnés des enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] (tels que les clients, contacts et les vendeurs) avec les lignes équivalentes dans [!INCLUDE[prod_short](includes/cds_long_md.md)] (tels que les comptes, les contacts et les utilisateurs). Selon le type de ligne, vous pouvez synchroniser les données de [!INCLUDE[prod_short](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)], ou vice versa. Pour plus d’informations, reportez-vous à la rubrique [Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La synchronisation utilise les éléments suivants :

* Mappages de table d’intégration
* Mappages de champ d’intégration
* Règles de synchronisation
* Enregistrements couplés

Une fois la synchronisation configurée, vous pouvez coupler les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] et les lignes [!INCLUDE[prod_short](includes/cds_long_md.md)] pour synchroniser leurs données. Vous pouvez commencer une synchronisation manuellement, ou selon un calendrier. Le tableau suivant donne un aperçu des méthodes à disposition pour synchroniser.  

|  Type  |  Méthode  |  Voir  |  
|--------|----------|-------|  
|Synchronisation manuelle|Synchronisez sur une base ligne après ligne.<br /><br /> Vous pouvez synchroniser les enregistrements individuels dans [!INCLUDE[prod_short](includes/prod_short.md)], tel qu’un client, avec une ligne [!INCLUDE[prod_short](includes/cds_long_md.md)] correspondante, par exemple un compte. C’est généralement ainsi que les utilisateurs travailleront avec les données [!INCLUDE[prod_short](includes/cds_long_md.md)] dans [!INCLUDE[prod_short](includes/prod_short.md)].|[Coupler et synchroniser des enregistrements manuellement](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchronisez sur une base de mappage de table.<br /><br /> Vous pouvez synchroniser tous les enregistrements dans une table [!INCLUDE[prod_short](includes/prod_short.md)] avec une table [!INCLUDE[prod_short](includes/cds_long_md.md)].|[Synchroniser les mappages de table individuels](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synchronisez tous les enregistrements modifiés pour tous les mappages de table.<br /><br /> Vous pouvez synchroniser toutes les enregistrements qui ont été modifiés dans les tables [!INCLUDE[prod_short](includes/prod_short.md)] depuis la dernière synchronisation.|[Synchronisation de tous les enregistrements modifiés](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Synchronisation complète de toutes les données pour tous les mappages de table.<br /><br /> Vous pouvez synchroniser toutes les données des tables [!INCLUDE[prod_short](includes/prod_short.md)] et des tables [!INCLUDE[prod_short](includes/cds_long_md.md)] mappées et créer de nouveaux enregistrements ou lignes dans la solution de destination pour les enregistrements non couplés dans la solution source.<br /><br /> La synchronisation complète permet de synchroniser toutes les données et d’ignorer le couplage. Généralement, vous effectuez une synchronisation complète lorsque vous configurez l’intégration et lorsqu’une seule des solutions contient des données. Une synchronisation complète peut être également utile dans un environnement de démonstration.|[Exécuter une synchronisation complète](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Synchronisation programmée|Synchronisez tous les changements apportés aux données pour tous les mappages de table.<br /><br /> Vous pouvez synchroniser [!INCLUDE[prod_short](includes/prod_short.md)] avec [!INCLUDE[prod_short](includes/cds_long_md.md)] à des intervalles planifiés en configurant des projets dans la file projets.|[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> La synchronisation entre [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)] est basée sur l’exécution planifiée des entrées de la file d’attente des tâches et ne garantit pas la cohérence des données en temps réel entre deux services. Pour la cohérence des données en temps réel, vous devriez explorer [Tables virtuelles Business Central](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) ou les API Business Central.   


## <a name="standard-table-mapping-for-synchronization"></a>Mappage de table standard pour la synchronisation
Les tables dans [!INCLUDE[prod_short](includes/cds_long_md.md)], telles que des comptes, sont intégrées aux types de tables équivalentes dans [!INCLUDE[prod_short](includes/prod_short.md)], tels que des clients. Pour utiliser les données [!INCLUDE[prod_short](includes/cds_long_md.md)], vous configurez des liens, appelés couplages entre les tables dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)].

Le tableau suivant répertorie le mappage standard entre les tables dans [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Vous pouvez réinitialiser les modifications de configuration apportées aux mappages de table d’intégration et de champ à leurs paramètres par défaut en sélectionnant les mappages, puis en choisissant **Utiliser la configuration de synchronisation par défaut**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Direction de synchronisation | Filtre par défaut |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Vendeur/Acheteur | Utilisateur | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtre contact [!INCLUDE[prod_short](includes/cds_long_md.md)] : le **Statut** est **Non**, l’**Utilisateur sous licence** est **Oui**, le Mode utilisateur de l’intégration est **Non** |
| Client | Compte | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtre compte [!INCLUDE[prod_short](includes/cds_long_md.md)] : le **type de relation** est **Client** et le **statut** est **Actif**. Filtre [!INCLUDE[prod_short](includes/prod_short.md)] : **Bloqué** est vide (le client n’est pas bloqué). |
| Fournisseur | Compte | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtre compte [!INCLUDE[prod_short](includes/cds_long_md.md)] : le **type de relation** est **Fournisseur** et le **statut** est **Actif**. Filtre [!INCLUDE[prod_short](includes/prod_short.md)] : **Bloqué** est vide (le fournisseur n’est pas bloqué). |
| Contact | Contact | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtre contact [!INCLUDE[prod_short](includes/prod_short.md)] : le champ **Type** est défini sur **Personne** et le contact est affecté à une société. Filtre contact [!INCLUDE[prod_short](includes/cds_long_md.md)] : le contact est affecté à une société et le type de client parent est **Client**. |
| Devise | Devise de transaction | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> Les actions **Dataverse** ne sont pas disponibles sur les pages, par exemple, la page Fiche client, pour les enregistrements qui ne respectent pas le filtre de table sur le mappage de table d′intégration.

### <a name="tip-for-admins-viewing-table-mappings"></a>Astuce dédiée aux administrateurs : affichage des mappages de table
Vous pouvez afficher le mappage entre les tables dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et les tables dans [!INCLUDE[prod_short](includes/prod_short.md)] sur la page **Mappages de table d’intégration**, où vous pouvez également appliquer des filtres. Vous définissez le mappage entre les champs des tables [!INCLUDE[prod_short](includes/prod_short.md)] et les colonnes [!INCLUDE[prod_short](includes/cds_long_md.md)] de la page **Mappage de champ d’intégration**, où vous pouvez ajouter une logique de mappage supplémentaire. Par exemple, cela peut être utile si vous devez résoudre un problème de synchronisation.

## <a name="see-also"></a>Voir aussi
[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
