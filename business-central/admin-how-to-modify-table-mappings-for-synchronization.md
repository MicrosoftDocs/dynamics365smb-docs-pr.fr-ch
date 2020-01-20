---
title: Mappage des tables et des champs à synchroniser | Microsoft Docs
description: Découvrez comment mapper des tables et des champs pour synchroniser des données entre Business Central et Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943128"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Mappage des tables et des champs à synchroniser
La base de la synchronisation des données dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des données dans [!INCLUDE[crm_md](includes/crm_md.md)] consiste à mapper les tables et les champs qui contiennent les données de l'un vers l'autre. Le mappage s'effectue via des tables d'intégration. 

## <a name="mapping-integration-tables"></a>Mappage de tables d'intégration
Une table d'intégration est une table dans la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] qui représente une entité, par exemple un compte, dans [!INCLUDE[crm_md](includes/crm_md.md)]. Les tables d'intégration incluent des champs qui correspondent aux champs de la table de l'entité [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, la table d'intégration Compte se connecte à l'entité Comptes dans [!INCLUDE[crm_md](includes/crm_md.md)]. Il doit y avoir un mappage de table d'intégration pour chaque entité dans [!INCLUDE[crm_md](includes/crm_md.md)] à synchroniser avec les données dans [!INCLUDE[d365fin](includes/d365fin_md.md)]].

Lorsque vous créez la connexion entre les applications, [!INCLUDE[d365fin](includes/d365fin_md.md)] configure quelques mappages de table et de champ par défaut. Si vous le souhaitez, vous pouvez modifier les mappages de tables. Pour en savoir plus, reportez-vous à la rubrique [Mappage d'entité Sales standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Si vous avez modifié les mappages par défaut et souhaitez annuler vos modifications, sur la page **Configuration de la connexion Dynamics 365**, choisissez **Utiliser le paramétrage de synchronisation par défaut**.

> [!Note]
> Si vous utilisez une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)], les mappages de tables d'intégration sont stockés dans la table 5335 Mappages de tables d'intégration, et peuvent être affichés et modifiés à partir de la page 5335 Mappages de tables d'intégration. Les règles de synchronisation et mappages complexes sont définis dans le codeunit 5341. 

### <a name="synchronization-rules"></a>Règles de synchronisation
Un mappage de table d'intégration comprend également des règles qui contrôlent comment les travaux de synchronisation d'intégration synchronisent les enregistrements dans une table [!INCLUDE[d365fin](includes/d365fin_md.md)] et une entité dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour plus d'informations, reportez-vous à la rubrique [Règles de synchronisation](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Mappage de champs d'intégration
Le mappage de tables ne constitue que la première étape. Vous devez également mapper les champs des tables. Les mappages de champs d'intégration associent les champs dans les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les champs correspondants dans [!INCLUDE[crm_md](includes/crm_md.md)], et déterminent s'il faut synchroniser les données dans chaque table. Le mappage de table standard fourni par [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut des mappages de champs, mais vous pouvez les modifier si vous le souhaitez. Pour plus d'informations, voir [Affichage des mappages d'entités](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Si vous utilisez une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)], les mappages de champs d'intégration sont définis dans la table 5336 Mappage de champs d'intégration.

## <a name="coupling-records"></a>Enregistrements couplage
Le couplage associe des enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)] à des enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, les comptes dans [!INCLUDE[crm_md](includes/crm_md.md)] sont généralement associés aux clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le couplage d'enregistrements offre les avantages suivants :

* Il rend la synchronisation possible.
* Les utilisateurs peuvent ouvrir des enregistrements dans une application métier puis une autre. Cela exige que la solution d'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] soit installée dans [!INCLUDE[crm_md](includes/crm_md.md)].

Les couplages peuvent être configurés automatiquement à l'aide des projets de synchronisation, ou manuellement en modifiant l'enregistrement dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Synchronisation des données dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) et [Couplage et synchronisation manuels d'enregistrements](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtrer des enregistrements  
Si vous ne souhaitez pas synchroniser tous les enregistrements pour une entité spécifique dans [!INCLUDE[crm_md](includes/crm_md.md)] ou une table dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez définir des filtres pour limiter les enregistrements synchronisés. Vous configurez des filtres sur la page **Mappages de table d'intégration**.  

#### <a name="to-filter-records-for-synchronization"></a>Pour filtrer des enregistrements en vue d'une synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.

2.  Pour filtrer les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)], définissez le champ **Filtre table**.  

3.  Pour filtrer les enregistrements [!INCLUDE[crm_md](includes/crm_md.md)], définissez le champ **Filtre table intégration**.  

## <a name="creating-new-records"></a>Créer des enregistrements  
 Par défaut, seuls les enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] qui sont couplés seront synchronisés par les projets de synchronisation de l'intégration. Vous pouvez définir des mappages de table afin que des enregistrements soient créés dans la destination (par exemple, [!INCLUDE[d365fin](includes/d365fin_md.md)]) pour chaque enregistrement de la source (par exemple, [!INCLUDE[crm_md](includes/crm_md.md)]) qui n'est pas encore couplé.  

 Par exemple, le projet de synchronisation Dynamics 365 Sales - VENDEURS utilise le mappage de table VENDEURS. Le projet de synchronisation copie les données des enregistrements d'utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)] vers les enregistrements de vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si vous définissez le mappage de table pour créer des enregistrements, pour chaque utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)] qui n'est pas encore couplé à un vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un enregistrement de vendeur est créé dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Pour créer des enregistrements durant la synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.

2.  Dans l'écriture de mappage de table de la liste, désactivez le champ **Synch. uniquement les enregistrements couplés**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Utilisation de modèles de configuration dans les mappages de table
Vous pouvez affecter des modèles de configuration aux mappages de table à utiliser pour les enregistrements créés dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[crm_md](includes/crm_md.md)]. Pour chaque mappage de table, vous pouvez spécifier un modèle de configuration à utiliser pour les nouveaux enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et un autre modèle à utiliser pour les nouveaux enregistrements [!INCLUDE[crm_md](includes/crm_md.md)].  

Si vous installez la configuration de synchronisation par défaut, deux modèles de configuration sont automatiquement créés et utilisés dans le mappage de table pour les clients [!INCLUDE[d365fin](includes/d365fin_md.md)] et les comptes [!INCLUDE[crm_md](includes/crm_md.md)] : **CRMCUST** et **CRMACCOUNT**.  

-   **CRMCUST** permet de créer et de synchroniser de nouveaux clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sur la base d'un compte dans [!INCLUDE[crm_md](includes/crm_md.md)].  

     Ce modèle est créé en copiant un modèle de configuration existant pour les clients de l'application. Le compte **CRMCUST** n'est créé que s'il existe un modèle de configuration et que si le champ **Code devise** du modèle est vide. Si un champ du modèle de configuration contient une valeur, celle-ci est utilisée au lieu de la valeur du champ mappé dans le compte [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, si le champ **Pays/Région** d'un compte dans [!INCLUDE[crm_md](includes/crm_md.md)] a la valeur *États-Unis* et le champ **Pays/Région** du modèle de configuration a la valeur *Grande-Bretagne*, alors *Grande-Bretagne* est utilisé comme **Pays/Région** pour le client dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Le compte **CRMACCOUNT** permet de créer et de synchroniser de nouveaux comptes dans [!INCLUDE[crm_md](includes/crm_md.md)] sur la base d'un compte dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Pour spécifier des modèles de configuration dans un mappage de table  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.

2.  Dans l'écriture de mappage de table de la liste, dans le champ **Code modèle config. table**, choisissez le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Configurez le champ **Code modèle config. table int.** dans le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Voir aussi  
[À propos de l'intégration de Dynamics 365 Business Central avec Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synchronisation de Business Central et Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
