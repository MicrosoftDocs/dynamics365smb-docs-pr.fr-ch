---
title: Modifier les mappages de table pour la synchronisation | Microsoft Docs
description: Découvrez comment modifier les mappages de table utilisés lors de la synchronisation des données entre Business Central et Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: de924baa494ae00c09dcb7657c050f2d9ae3ba87
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247459"
---
# <a name="modify-table-mappings-for-synchronization"></a>Modifier les mappages de table pour la synchronisation
Un mappage de table d'intégration associe une table dans [!INCLUDE[d365fin](includes/d365fin_md.md)] à une table d'intégration pour l'entité [!INCLUDE[crm_md](includes/crm_md.md)]. À chaque entité de [!INCLUDE[crm_md](includes/crm_md.md)] à synchroniser avec les données correspondantes dans [!INCLUDE[d365fin](includes/d365fin_md.md)] doit correspondre un mappage de table d'intégration. Un mappage de table d'intégration comprend plusieurs paramètres qui vous permettent de contrôler comment les enregistrements d'une table [!INCLUDE[d365fin](includes/d365fin_md.md)] et une entité [!INCLUDE[crm_md](includes/crm_md.md)] sont synchronisés par les projets de synchronisation d'intégration correspondants.  

## <a name="filtering-records"></a>Filtrer des enregistrements  
 Si vous ne souhaitez pas synchroniser tous les enregistrements pour une entité spécifique dans [!INCLUDE[crm_md](includes/crm_md.md)] ou une table dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez définir des filtres pour limiter les enregistrements synchronisés. Vous configurez des filtres sur la page **Mappages de table d'intégration**.  

#### <a name="to-filter-records-for-synchronization"></a>Pour filtrer des enregistrements en vue d'une synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mappages de table d'intégration**, puis sélectionnez le lien associé.

2.  Pour filtrer les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)], définissez le champ **Filtre table**.  

3.  Pour filtrer les enregistrements [!INCLUDE[crm_md](includes/crm_md.md)], définissez le champ **Filtre table intégration**.  

## <a name="creating-new-records"></a>Créer des enregistrements  
 Par défaut, seuls les enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] qui sont couplés seront synchronisés par les projets de synchronisation de l'intégration. Vous pouvez définir des mappages de table afin que des enregistrements soient créés dans la destination (par exemple, [!INCLUDE[d365fin](includes/d365fin_md.md)]) pour chaque enregistrement de la source (par exemple, [!INCLUDE[crm_md](includes/crm_md.md)]) qui n'est pas encore couplé.  

 Par exemple, le projet de synchronisation VENDEURS - Dynamics 365 for Sales utilise le mappage de table VENDEURS. Le projet de synchronisation copie les données des enregistrements d'utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)] vers les enregistrements de vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si vous définissez le mappage de table pour créer des enregistrements, pour chaque utilisateur dans [!INCLUDE[crm_md](includes/crm_md.md)] qui n'est pas encore couplé à un vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un enregistrement de vendeur est créé dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Pour créer des enregistrements durant la synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mappages de table d'intégration**, puis sélectionnez le lien associé.

2.  Dans l'écriture de mappage de table de la liste, désactivez le champ **Synch. uniquement les enregistrements couplés**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Utilisation de modèles de configuration dans les mappages de table
Vous pouvez affecter des modèles de configuration aux mappages de table à utiliser pour les enregistrements créés dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[crm_md](includes/crm_md.md)]. Pour chaque mappage de table, vous pouvez spécifier un modèle de configuration à utiliser pour les nouveaux enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et un autre modèle à utiliser pour les nouveaux enregistrements [!INCLUDE[crm_md](includes/crm_md.md)].  

Si vous installez la configuration de synchronisation par défaut, deux modèles de configuration sont automatiquement créés et utilisés dans le mappage de table pour les clients [!INCLUDE[d365fin](includes/d365fin_md.md)] et les comptes [!INCLUDE[crm_md](includes/crm_md.md)] : **CRMCUST** et **CRMACCOUNT**.  

-   **CRMCUST** permet de créer et de synchroniser de nouveaux clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sur la base d'un compte dans [!INCLUDE[crm_md](includes/crm_md.md)].  

     Ce modèle est créé en copiant un modèle de configuration existant pour les clients de l'application. Le compte **CRMCUST** n'est créé que s'il existe un modèle de configuration et que si le champ **Code devise** du modèle est vide. Si un champ du modèle de configuration contient une valeur, celle-ci est utilisée au lieu de la valeur du champ mappé dans le compte [!INCLUDE[crm_md](includes/crm_md.md)]. Par exemple, si le champ **Pays/Région** d'un compte dans [!INCLUDE[crm_md](includes/crm_md.md)] a la valeur *États-Unis* et le champ **Pays/Région** du modèle de configuration a la valeur *Grande-Bretagne*, alors *Grande-Bretagne* est utilisé comme **Pays/Région** pour le client dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Le compte **CRMACCOUNT** permet de créer et de synchroniser de nouveaux comptes dans [!INCLUDE[crm_md](includes/crm_md.md)] sur la base d'un compte dans [!INCLUDE[d365](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Pour spécifier des modèles de configuration dans un mappage de table  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mappages de table d'intégration**, puis sélectionnez le lien associé.

2.  Dans l'écriture de mappage de table de la liste, dans le champ **Code modèle config. table**, choisissez le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Configurez le champ **Code modèle config. table int.** dans le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Voir aussi  
[À propos de l'intégration de Dynamics 365 Business Central avec Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synchronisation de Business Central et de Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
