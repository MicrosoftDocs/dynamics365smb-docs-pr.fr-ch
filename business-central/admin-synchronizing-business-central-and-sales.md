---
title: Synchronisation et intégration des données | Microsoft Docs
description: La synchronisation copie les données entre les entités Common Data Service et les enregistrements Business Central, et conserve les données à jour dans les deux systèmes.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0763119e323a8bae6d2b7ce3db0780284befa292
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484124"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Synchronisation des données dans Business Central avec Common Data Service
Lorsque vous intégrez [!INCLUDE[d365fin](includes/cds_long_md.md)] avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez décider si vous souhaitez synchroniser les données dans les champs sélectionnés des enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] (tels que les clients, contacts et les vendeurs) avec les enregistrements équivalents dans [!INCLUDE[d365fin](includes/cds_long_md.md)] (tels que les comptes, les contacts et les utilisateurs). Selon le type d'enregistrement, vous pouvez synchroniser les données de [!INCLUDE[d365fin](includes/cds_long_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)], ou vice versa. Pour plus d'informations, reportez-vous à la rubrique [Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La synchronisation utilise les éléments suivants :

* Mappages de table d'intégration
* Mappages de champ d'intégration
* Règles de synchronisation
* Enregistrements couplés

Une fois la synchronisation configurée, vous pouvez coupler les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et les enregistrements [!INCLUDE[d365fin](includes/cds_long_md.md)] pour synchroniser leurs données. Vous pouvez commencer une synchronisation manuellement, ou selon un calendrier. Le tableau suivant donne un aperçu des méthodes à disposition pour synchroniser les enregistrements.  

|  Type  |  Méthode  |  Voir  |  
|--------|----------|-------|  
|Synchronisation manuelle|Synchronisez sur une base enregistrement après enregistrement.<br /><br /> Vous pouvez synchroniser les enregistrements individuels dans [!INCLUDE[d365fin](includes/d365fin_md.md)], tel qu'un client, avec un enregistrement [!INCLUDE[d365fin](includes/cds_long_md.md)] correspondant, par exemple un compte. C'est généralement ainsi que les utilisateurs travailleront avec les données [!INCLUDE[d365fin](includes/cds_long_md.md)] dans [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Coupler et synchroniser des enregistrements manuellement](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchronisez sur une base de mappage de table.<br /><br /> Vous pouvez synchroniser tous les enregistrements dans une table [!INCLUDE[d365fin](includes/d365fin_md.md)] avec une entité [!INCLUDE[d365fin](includes/cds_long_md.md)].|[Synchroniser les mappages de table individuels](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synchronisez tous les enregistrements modifiés pour tous les mappages de table.<br /><br /> Vous pouvez synchroniser toutes les enregistrements qui ont été modifiés dans les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis la dernière synchronisation.|[Synchronisation de tous les enregistrements modifiés](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Synchronisation complète de toutes les données pour tous les mappages de table.<br /><br /> Vous pouvez synchroniser toutes les données des tables [!INCLUDE[d365fin](includes/d365fin_md.md)] et des entités [!INCLUDE[d365fin](includes/cds_long_md.md)] mappées et créer de nouveaux enregistrements dans la solution de destination pour les enregistrements non couplés dans la solution source.<br /><br /> La synchronisation complète permet de synchroniser toutes les données et d'ignorer le couplage. Généralement, vous effectuez une synchronisation complète lorsque vous configurez l'intégration et lorsqu'une seule des solutions contient des données. Une synchronisation complète peut être également utile dans un environnement de démonstration.|[Exécuter une synchronisation complète](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Synchronisation programmée|Synchronisez tous les changements apportés aux données pour tous les mappages de table.<br /><br /> Vous pouvez synchroniser [!INCLUDE[d365fin](includes/d365fin_md.md)] avec [!INCLUDE[d365fin](includes/cds_long_md.md)] à des intervalles planifiés en configurant des projets dans la file projets.|[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Mappage d'entité standard pour la synchronisation
Les entités dans [!INCLUDE[d365fin](includes/cds_long_md.md)], telles que des comptes, sont intégrées aux types d'entités équivalents dans [!INCLUDE[d365fin](includes/d365fin_md.md)], tels que des clients. Pour utiliser les données [!INCLUDE[d365fin](includes/cds_long_md.md)], vous configurez des liens, appelés couplages entre les entités dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)].

Le tableau suivant répertorie le mappage standard entre les entités dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)] que [!INCLUDE[d365fin](includes/d365fin_md.md)] fournit.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)]|Direction de synchronisation|Filtre par défaut|
|-------------------------------------------|-----|-------------------------|--------------|
|Vendeur/Acheteur|Utilisateur|[!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtre contact [!INCLUDE[d365fin](includes/cds_long_md.md)] : le **Statut** est **Non**, l'**Utilisateur sous licence** est **Oui**, le Mode utilisateur de l'intégration est **Non**|
|Client|Compte|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtre compte [!INCLUDE[d365fin](includes/cds_long_md.md)] : le **type de relation** est **Client** et le **statut** est **Actif**. Filtre [!INCLUDE[d365fin](includes/d365fin_md.md)] : **Bloqué** est vide (le client n'est pas bloqué).|
|Fournisseur|Compte|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtre compte [!INCLUDE[d365fin](includes/cds_long_md.md)] : le **type de relation** est **Fournisseur** et le **statut** est **Actif**. Filtre [!INCLUDE[d365fin](includes/d365fin_md.md)] : **Bloqué** est vide (le fournisseur n'est pas bloqué).|
|Contact|Contact|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtre contact [!INCLUDE[d365fin](includes/d365fin_md.md)] : le champ **Type** est défini sur **Personne** et le contact est affecté à une société. Filtre contact [!INCLUDE[d365fin](includes/cds_long_md.md)] : le contact est affecté à une société et le type de client parent est **Compte**|
|Devise|Devise de transaction|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)]| |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Astuce dédiée aux administrateurs : affichage des mappages d'entité
Vous pouvez afficher le mappage entre les entités dans [!INCLUDE[d365fin](includes/cds_long_md.md)] et les tables dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sur la page **Mappages de table d'intégration**, où vous pouvez également appliquer des filtres. Vous définissez le mappage entre les champs des tables [!INCLUDE[d365fin](includes/d365fin_md.md)] et les champs des entités [!INCLUDE[d365fin](includes/cds_long_md.md)] de la page **Mappage de champ d'intégration**, où vous pouvez ajouter une logique de mappage supplémentaire. Par exemple, cela peut être utile si vous devez résoudre un problème de synchronisation.

## <a name="see-also"></a>Voir aussi  
[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
