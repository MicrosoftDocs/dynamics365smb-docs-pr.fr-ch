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
ms.service: dynamics-365-business-central
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

### <a name="tip-for-admins-viewing-table-mappings"></a>Astuce pour les administrateurs : affichage des mappages de table

Vous pouvez afficher le mappage entre les tables dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et les tables dans [!INCLUDE[prod_short](includes/prod_short.md)] sur la page **Mappages de table d’intégration**, où vous pouvez également appliquer des filtres. Vous définissez le mappage entre les champs des tables [!INCLUDE[prod_short](includes/prod_short.md)] et les colonnes [!INCLUDE[prod_short](includes/cds_long_md.md)] de la page **Mappage de champ d’intégration**, où vous pouvez ajouter une logique de mappage supplémentaire. Par exemple, cela peut être utile si vous devez résoudre un problème de synchronisation.

## <a name="use-virtual-tables-to-get-more-data"></a>Utiliser des tables virtuelles pour obtenir plus de données

Lorsque vous configurez votre intégration, vous pouvez utiliser des tables virtuelles pour rendre plus de données disponibles dans [!INCLUDE[prod_short](includes/cds_long_md.md)], sans l’aide d’un développeur.

Une table virtuelle est une table personnalisée qui dispose de colonnes et de lignes contenant des données d’une source de données externe, comme [!INCLUDE [prod_short](includes/prod_short.md)]. Les colonnes et les lignes d’une table virtuelle ressemblent à une table normale ; cependant, les données ne sont pas stockées dans une table physique dans la base de données [!INCLUDE[prod_short](includes/cds_long_md.md)]. À la place, les données sont récupérées au moment de l’exécution.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] contient des objets qui sont également appelés tables virtuelles. Ces objets de table ne sont pas liés aux tables virtuelles que vous utilisez avec [!INCLUDE[prod_short](includes/cds_long_md.md)].

Pour en savoir plus sur les tables virtuelles, consultez les articles suivants :

* [Création et modification de tables virtuelles qui contiennent des données provenant d’une source de données externe](/power-apps/maker/data-platform/create-edit-virtual-entities) (documentation de Power Apps)
* [Référence de l’administrateur de table virtuelle Business Central pour Microsoft Dataverse](/business-central/dev-itpro/powerplatform/powerplat-admin-reference) (documentation de [!INCLUDE [prod_short](includes/prod_short.md)])

Pour utiliser des tables virtuelles, vous devez installer l’application **Entité virtuelle Business Central** à partir de [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Après avoir installé l’application, vous pouvez activer les tables virtuelles à partir de l’une des pages suivantes dans [!INCLUDE [prod_short](includes/prod_short.md)] :

* Lorsque vous exécutez le guide de configuration assistée **Configurer la connexion Dataverse**, vous pouvez utiliser la page **Tables virtuelles Dataverse disponibles** pour sélectionner plusieurs tables virtuelles. Ensuite, les tables sont disponibles dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et PowerApps Maker Portal. 
* À partir des pages **Configuration de la connexion Dataverse**, **Tables virtuelles** et **Tables virtuelles disponibles**.  
* À partir de Power App Maker Portal.

## <a name="synchronize-data-from-multiple-companies-or-environments"></a>Synchroniser les données de plusieurs sociétés ou environnements

Vous pouvez synchroniser les données de plusieurs sociétés ou environnements [!INCLUDE [prod_short](includes/prod_short.md)] avec un environnement [!INCLUDE[prod_short](includes/cds_long_md.md)]. Dans les scénarios de synchronisation multi-sociétés, plusieurs éléments doivent être pris en compte.

### <a name="set-company-ids"></a>Définir les ID de société

Lorsque vous synchronisez des enregistrements, nous définissons un ID de société dans l’entité [!INCLUDE[prod_short](includes/cds_long_md.md)] pour clarifier la société [!INCLUDE [prod_short](includes/prod_short.md)] d’où proviennent les enregistrements. Les mappages de table d’intégration comportent des champs de filtre de table d’intégration qui prennent en compte l’ID de société. Pour inclure un mappage de table dans une configuration multi-sociétés, sur la page **Mappage de table d’intégration**, choisissez la case à cocher **Synchronisation multi-sociétés activée**. Le paramètre optimise la façon dont les champs de filtre de la table d’intégration filtrent les ID de société dans une configuration multi-sociétés.

Pour les mappages de table d’intégration qui synchronisent des documents, tels que des commandes, devis et opportunités, si vous choisissez la case à cocher **Synchronisation multi-sociétés activée**, l’intégration ne prend en compte que les entités qui ont l’ID de société de la société [!INCLUDE [prod_short](includes/prod_short.md)] actuelle. Pour synchroniser des documents, par exemple entre Business Central et Sales, les utilisateurs de Sales doivent spécifier l’ID de société sur les documents. Sinon, les documents ne sont pas synchronisés.  

Pour tous les autres mappages de table d’intégration, si vous choisissez la case à cocher **Synchronisation multi-sociétés activée**, le filtre de l’ID de société est supprimé. La synchronisation prend en compte les entités associées, quel que soit leur ID de société.

### <a name="specify-the-synchronization-direction"></a>Spécifier la direction de synchronisation

Si vous activez le support multi-sociétés sur un mappage de table d’intégration, nous vous recommandons de définir la direction du mappage sur **FromIntegration**. Si vous définissez la direction sur **ToIntegration** ou **Bidirectional**, il est recommandé d’utiliser **Filtre de table** et **Filtre de table d’intégration** pour contrôler quelles entités sont synchronisées avec quelle société. Il est également recommandé d’utiliser le couplage par correspondance pour éviter de créer des enregistrements en double. Pour en savoir plus sur le couplage par correspondance, consultez [Personnaliser le couplage par correspondance](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### <a name="use-unique-numbers"></a>Utiliser des numéros uniques

Si votre série de numéros ne garantit pas que les valeurs de clé primaire sont uniques à chaque société, nous vous recommandons d’utiliser des préfixes. Pour commencer à utiliser des préfixes, créez une règle de transformation sur le mappage de champ d’intégration. Pour en savoir plus sur les règles de transformation, consultez [Gérer les différences dans les valeurs de champ](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## <a name="see-also"></a>Voir aussi

[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Intégration à Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
