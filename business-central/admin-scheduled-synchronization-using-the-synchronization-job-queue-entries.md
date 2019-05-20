---
title: Synchronisation de Business Central et Dynamics 365 for Sales | Microsoft Docs
description: En savoir plus sur la synchronisation des données entre Business Central et Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: b3fb3d2680cd85da8b2def7e82fbf62c0046fcc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247436"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Planification d'une synchronisation entre Business Central et Dynamics 365 for Sales
Vous pouvez synchroniser [!INCLUDE[d365fin](includes/d365fin_md.md)] avec [!INCLUDE[crm_md](includes/crm_md.md)] à des intervalles planifiés en configurant des projets dans la file projets. Les projets de synchronisation permettent de synchroniser les données des enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] qui ont été précédemment couplés ensemble. Ou bien, pour les enregistrements qui ne sont pas encore couplés, selon la direction et les règles de synchronisation, les projets de synchronisation peuvent créer des enregistrements et les coupler dans le système de destination. Plusieurs projets de synchronisation sont disponibles et prêts à l'emploi. Vous pouvez les visualiser sur la page **Écritures file d'attente des travaux**. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Processus de synchronisation  
Chaque écriture de file projets de synchronisation utilise un mappage de table d'intégration spécifique qui indique la table [!INCLUDE[d365fin](includes/d365fin_md.md)] et l'entité [!INCLUDE[crm_md](includes/crm_md.md)] à synchroniser. Les mappages de table incluent également des paramètres qui contrôlent les enregistrements de la table [!INCLUDE[d365fin](includes/d365fin_md.md)] et de l'entité [!INCLUDE[crm_md](includes/crm_md.md)] à synchroniser.  

Pour synchroniser les données, les enregistrements d'entité [!INCLUDE[crm_md](includes/crm_md.md)] doivent être couplés à des enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, un client [!INCLUDE[d365fin](includes/d365fin_md.md)] doit être couplé à un compte [!INCLUDE[crm_md](includes/crm_md.md)]. Vous pouvez définir des couplages manuellement, avant d'exécuter les projets de synchronisation, ou laisser les projets de synchronisation définir automatiquement des couplages. La liste suivante décrit la manière dont les données sont synchronisées entre [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsque vous utilisez les écritures de file projets de synchronisation. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Par défaut, seuls les enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] qui sont couplés à des enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)] sont synchronisés. Vous pouvez modifier le mappage de table entre une entité [!INCLUDE[crm_md](includes/crm_md.md)] et une entité [!INCLUDE[d365fin](includes/d365fin_md.md)] afin que les projets de synchronisation de l'intégration créent des enregistrements dans la base de données de destination pour chaque enregistrement de la base de données source qui n'est pas couplé. Les nouveaux enregistrements sont également couplés aux enregistrements correspondants dans la source. Par exemple, lorsque vous synchronisez les clients avec des comptes [!INCLUDE[crm_md](includes/crm_md.md)], un enregistrement de compte est créé pour chaque client dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Les nouveaux comptes sont automatiquement couplés aux clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puisque la synchronisation est bidirectionnelle dans ce cas, un client est créé et couplé pour chaque compte [!INCLUDE[crm_md](includes/crm_md.md)] qui n'est pas encore couplé.  

    > [!NOTE]  
    >  Des règles et des filtres permettent de déterminer les données synchronisées. Pour plus d'informations, reportez-vous à la rubrique [Règles de synchronisation](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Lorsque des enregistrements sont créées dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ils utilisent le modèle défini pour le mappage de table d'intégration ou le modèle par défaut qui est disponible pour le type d'enregistrement. Les champs sont renseignés avec des données depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[crm_md](includes/crm_md.md)] en fonction du sens de synchronisation. Pour en savoir plus, reportez-vous à la rubrique [Procédure : Modifier les mappages de table pour la synchronisation](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Avec les synchronisations suivantes, seuls les enregistrements qui ont été modifiés ou ajoutés après le dernier projet de synchronisation réussi pour l'entité seront mis à jour.  

     Les nouveaux enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)] sont ajoutés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si les données des champs des enregistrements [!INCLUDE[crm_md](includes/crm_md.md)] ont été modifiées, elles sont copiées dans le champ correspondant de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Avec la synchronisation bidirectionnelle, le projet effectue une synchronisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)], puis de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Écritures de file projets de synchronisation par défaut  
Le tableau suivant décrit les projets de synchronisation par défaut.  

|Écriture file d'attente des travaux|Description|Sens|Correspondance table intégration|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|Projet de synchronisation CONTACT - Dynamics 365 for Sales|Permet de synchroniser les contacts [!INCLUDE[crm_md](includes/crm_md.md)] aux contacts [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirectionnel|CONTACT|  
|Projet de synchronisation DEVISE - Dynamics 365 for Sales|Permet de synchroniser les devises de transaction [!INCLUDE[crm_md](includes/crm_md.md)] avec les devises [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|DEVISE|  
|Projet de synchronisation CLIENT - Dynamics 365 for Sales|Permet de synchroniser les comptes [!INCLUDE[crm_md](includes/crm_md.md)] avec les clients [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirectionnel|CLIENT|  
|Projet de synchronisation GRPPRXCLI-PRIX - Dynamics 365 for Sales|Permet de synchroniser les listes de prix de vente [!INCLUDE[crm_md](includes/crm_md.md)] avec les groupes de prix client [!INCLUDE[d365fin](includes/d365fin_md.md)].| |GROUPES DE PRIX CLIENT - LISTES DE PRIX DE VENTE|
|Projet de synchronisation ARTICLE-PRODUIT - Dynamics 365 for Sales|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les articles [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|ARTICLE-PRODUIT|
|Projet de synchronisation FACTVENTEVALIDEES-FACT - Dynamics 365 for Sales|Permet de synchroniser les factures [!INCLUDE[crm_md](includes/crm_md.md)] avec les factures vente [!INCLUDE[d365fin](includes/d365fin_md.md)] validées.|De [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)]|FACTURES - FACTURES VENTE VALIDÉES|
|Projet de synchronisation RESSOURCE-PRODUIT - Dynamics 365 for Sales|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les ressources [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUIT|  
|Projet de synchronisation VENDEURS - Dynamics 365 for Sales|Permet de synchroniser les vendeurs [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les utilisateurs [!INCLUDE[crm_md](includes/crm_md.md)].|De [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)]|VENDEURS|
|Projet de synchronisation PRXVENTE-PRXPRODUIT - Dynamics 365 for Sales|Permet de synchroniser les prix de produit [!INCLUDE[crm_md](includes/crm_md.md)] avec les prix de vente [!INCLUDE[d365fin](includes/d365fin_md.md)].||PRIX DE PRODUIT - PRIX DE VENTE|
|Projet Synchronisation UNITÉ DE MESURE - Dynamics 365 for Sales|Permet de synchroniser les groupes d'unités [!INCLUDE[crm_md](includes/crm_md.md)] avec les unités de mesure [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|UNITÉ DE MESURE|  
|Synchronisation Statistiques client - Dynamics 365 for Sales|Permet de mettre à jour les comptes [!INCLUDE[crm_md](includes/crm_md.md)] avec les données client [!INCLUDE[d365fin](includes/d365fin_md.md)] les plus récentes. Dans [!INCLUDE[crm_md](includes/crm_md.md)], ces informations s'affichent dans le formulaire de vue rapide **Statistiques de compte Business Central** des comptes couplés avec les clients [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Ces données peuvent être également mises à jour manuellement depuis chaque enregistrement du client. Pour en savoir plus, reportez-vous à la rubrique [Procédure : coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Remarque :** cette file d'attente de projets est pertinente uniquement si la solution d'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] est installée dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, reportez-vous à la rubrique [À propos de la solution d'intégration Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Non applicable.|Non applicable.|   

## <a name="to-view-the-synchronization-job-log"></a>Pour afficher le journal des projets de synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Journal de synchronisation d'intégration**, puis sélectionnez le lien associé.
2.  Si une ou plusieurs erreurs se sont produites pour un projet de synchronisation, le nombre d'erreurs s'affiche dans la colonne **Échec**. Pour afficher les erreurs pour le projet, sélectionnez le numéro.  

    > [!TIP]  
    >  Vous pouvez afficher toutes les erreurs du projet de synchronisation en ouvrant directement le journal des erreurs du projet de synchronisation.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Pour afficher le journal du projet de synchronisation à partir des mappages de table  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mappages de table d'intégration**, puis sélectionnez le lien associé.
2.  Sur la page **Mappages de table d'intégration**, sélectionnez une écriture, puis choisissez **Journal projet synch. intégration**.  

## <a name="to-view-the-synchronization-error-log"></a>Pour afficher le journal des erreurs de synchronisation  
* Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Erreurs de synchronisation d'intégration**, puis sélectionnez le lien associé.

## <a name="see-also"></a>Voir aussi  
[Synchronisation des données dans Business Central et Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Synchroniser manuellement les mappages de table](admin-manual-synchronization-of-table-mappings.md)  
[Planification d'une synchronisation entre Business Central et Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[À propos de l'intégration de Dynamics 365 Business Central avec Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



