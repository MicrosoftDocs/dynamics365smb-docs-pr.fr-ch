---
title: Mappage des tables et des champs à synchroniser | Microsoft Docs
description: Découvrez comment mapper des tables et des champs pour synchroniser des données entre Business Central et Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/20/2020
ms.author: bholtorf
ms.openlocfilehash: 0b814c18c328ea0647e38b6a837577b277ca4e63
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527950"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Mappage des tables et des champs à synchroniser
La base de la synchronisation des données dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des données dans [!INCLUDE[d365fin](includes/cds_long_md.md)] consiste à mapper les tables et les champs qui contiennent les données de l'un vers l'autre. Le mappage s'effectue via des tables d'intégration. 

## <a name="mapping-integration-tables"></a>Mappage de tables d'intégration
Une table d'intégration est une table dans la base de données [!INCLUDE[d365fin](includes/d365fin_md.md)] qui représente une entité, par exemple un compte, dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Les tables d'intégration incluent des champs qui correspondent aux champs de la table de l'entité [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Par exemple, la table d'intégration Compte se connecte à l'entité Comptes dans [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Il doit y avoir un mappage de table d'intégration pour chaque entité dans [!INCLUDE[cds_short_md](includes/cds_short_md.md)] à synchroniser avec les données dans [!INCLUDE[prodshort](includes/prodshort.md)].

Lorsque vous créez la connexion entre les applications, [!INCLUDE[d365fin](includes/d365fin_md.md)] configure quelques mappages de table et de champ par défaut. Si vous le souhaitez, vous pouvez modifier les mappages de tables. Pour en savoir plus, consultez [Mappage d'entité standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Si vous avez modifié les mappages par défaut et souhaitez annuler vos modifications, choisissez **Utiliser le paramétrage de synchronisation par défaut** sur la page **Configuration de la connexion [!INCLUDE[d365fin](includes/cds_long_md.md)]**.

> [!Note]
> Si vous utilisez une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)], les mappages de tables d'intégration sont stockés dans la table 5335 Mappages de tables d'intégration, et peuvent être affichés et modifiés à partir de la page 5335 Mappages de tables d'intégration. Les règles de synchronisation et mappages complexes sont définis dans le codeunit 5341. 

### <a name="synchronization-rules"></a>Règles de synchronisation
Un mappage de table d'intégration comprend également des règles qui contrôlent comment les travaux de synchronisation d'intégration synchronisent les enregistrements dans une table [!INCLUDE[d365fin](includes/d365fin_md.md)] et une entité dans [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

## <a name="mapping-integration-fields"></a>Mappage de champs d'intégration
Le mappage de tables ne constitue que la première étape. Vous devez également mapper les champs des tables. Les mappages de champs d'intégration associent les champs dans les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les champs correspondants dans [!INCLUDE[d365fin](includes/cds_long_md.md)], et déterminent s'il faut synchroniser les données dans chaque table. Le mappage de table standard fourni par [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut des mappages de champs, mais vous pouvez les modifier si vous le souhaitez. Pour plus d'informations, voir [Affichage des mappages d'entités](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Si vous utilisez une version locale de [!INCLUDE[d365fin](includes/d365fin_md.md)], les mappages de champs d'intégration sont définis dans la table 5336 Mappage de champs d'intégration.

### <a name="handling-differences-in-field-values"></a>Gestion des différences de valeurs de champ
Parfois, les valeurs des champs que vous souhaitez associer sont différentes. Par exemple, le code langue pour les États-Unis est « U.S. » dans [!INCLUDE[crm_md](includes/crm_md.md)], mais « US » dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Autrement dit, vous devez transformer la valeur lorsque vous synchronisez des données. Cela se fait via les règles de transformation que vous définissez pour les champs. Vous définissez des règles de transformation sur la page **Mappages de table d'intégration** en choisissant **Mappage**, puis **Champs**. Des règles prédéfinies sont fournies, mais vous pouvez également créer les vôtres. Pour plus d'informations, voir [Règles de transformation](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Gestion des valeurs option manquantes dans Mappage
[!INCLUDE[d365fin](includes/cds_long_md.md)] contient des champs d'ensembles d'options qui fournissent des valeurs que vous pouvez mapper à des champs [!INCLUDE[d365fin](includes/d365fin_md.md)] de type **Option** pour la synchronisation automatique. Lors de la synchronisation, les options non mappées sont ignorées et les options manquantes sont ajoutées à la table [!INCLUDE[d365fin](includes/d365fin_md.md)] associée et à la table système **Mappage option CDS** pour une gestion manuelle ultérieure. Par exemple, en ajoutant les options manquantes dans l'un ou l'autre des produits, puis en mettant à jour le mappage. Pour en savoir plus, consultez [Gestion des valeurs option manquantes](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Enregistrements couplage
Le couplage associe des enregistrements dans [!INCLUDE[d365fin](includes/cds_long_md.md)] à des enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, les comptes dans [!INCLUDE[d365fin](includes/cds_long_md.md)] sont généralement associés aux clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Le couplage d'enregistrements offre les avantages suivants :

* Il rend la synchronisation possible.
* Les utilisateurs peuvent ouvrir des enregistrements dans une application métier puis une autre. Les applications doivent déjà être intégrées.

Les couplages peuvent être configurés automatiquement à l'aide des projets de synchronisation, ou manuellement en modifiant l'enregistrement dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Synchronisation des données dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) et [Couplage et synchronisation manuels d'enregistrements](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtrer des enregistrements  
Si vous ne souhaitez pas synchroniser tous les enregistrements pour une entité spécifique dans [!INCLUDE[d365fin](includes/cds_long_md.md)] ou une table dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez définir des filtres pour limiter les enregistrements synchronisés. Vous configurez des filtres sur la page **Mappages de table d'intégration**.  

#### <a name="to-filter-records-for-synchronization"></a>Pour filtrer des enregistrements en vue d'une synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.

2.  Pour filtrer les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)], définissez le champ **Filtre table**.  

3.  Pour filtrer les enregistrements [!INCLUDE[d365fin](includes/cds_long_md.md)], définissez le champ **Filtre table intégration**.  

## <a name="creating-new-records"></a>Créer des enregistrements  
Par défaut, seuls les enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[d365fin](includes/cds_long_md.md)] qui sont couplés seront synchronisés par les projets de synchronisation de l'intégration. Vous pouvez définir des mappages de table afin que des enregistrements soient créés dans la destination (par exemple, [!INCLUDE[d365fin](includes/d365fin_md.md)]) pour chaque enregistrement de la source (par exemple, [!INCLUDE[d365fin](includes/cds_long_md.md)]) qui n'est pas encore couplé.  

Par exemple, le projet de synchronisation Dynamics 365 Sales - VENDEURS utilise le mappage de table VENDEURS. Le projet de synchronisation copie les données des enregistrements d'utilisateur dans [!INCLUDE[d365fin](includes/cds_long_md.md)] vers les enregistrements de vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si vous définissez le mappage de table pour créer des enregistrements, pour chaque utilisateur dans [!INCLUDE[d365fin](includes/cds_long_md.md)] qui n'est pas encore couplé à un vendeur dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un enregistrement de vendeur est créé dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Pour créer des enregistrements durant la synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.

2.  Dans l'écriture de mappage de table de la liste, désactivez le champ **Synch. uniquement les enregistrements couplés**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Utilisation de modèles de configuration dans les mappages de table
Vous pouvez affecter des modèles de configuration aux mappages de table à utiliser pour les enregistrements créés dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pour chaque mappage de table, vous pouvez spécifier un modèle de configuration à utiliser pour les nouveaux enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et un autre modèle à utiliser pour les nouveaux enregistrements [!INCLUDE[d365fin](includes/cds_long_md.md)].  

Si vous installez la configuration de synchronisation par défaut, deux modèles de configuration sont automatiquement créés et utilisés dans le mappage de table pour les clients [!INCLUDE[d365fin](includes/d365fin_md.md)] et les comptes [!INCLUDE[crm_md](includes/crm_md.md)] : **CDSCUST** et **CDSACCOUNT**.  

-   **CDSCUST** permet de créer et synchroniser de nouveaux clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sur la base d'un compte dans [!INCLUDE[crm_md](includes/crm_md.md)].  

     Ce modèle est créé en copiant un modèle de configuration existant pour les clients de l'application. Le compte **CDSCUST** est créé seulement s'il existe un modèle de configuration et si le champ **Code devise** du modèle est vide. Si un champ du modèle de configuration contient une valeur, celle-ci est utilisée au lieu de la valeur du champ mappé dans le compte [!INCLUDE[d365fin](includes/cds_long_md.md)]. Par exemple, si le champ **Pays/Région** d'un compte dans [!INCLUDE[d365fin](includes/cds_long_md.md)] a la valeur *États-Unis* et le champ **Pays/Région** du modèle de configuration a la valeur *Grande-Bretagne*, alors *Grande-Bretagne* est utilisé comme **Pays/Région** pour le client dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Le compte **CDSACCOUNT** permet de créer et synchroniser de nouveaux comptes dans [!INCLUDE[d365fin](includes/cds_long_md.md)] sur la base d'un compte dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Pour spécifier des modèles de configuration dans un mappage de table  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.

2.  Dans l'écriture de mappage de table de la liste, dans le champ **Code modèle config. table**, choisissez le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Configurez le champ **Code modèle config. table int.** dans le modèle de configuration à utiliser pour les nouveaux enregistrements dans [!INCLUDE[d365fin](includes/cds_long_md.md)].

## <a name="see-also"></a>Voir aussi  
[À propos de l'intégration de Dynamics 365 Business Central avec [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synchronisation de Business Central et de [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Programmer une synchronisation](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
