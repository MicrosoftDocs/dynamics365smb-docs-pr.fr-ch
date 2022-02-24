---
title: Synchronisation de Business Central et Dynamics 365 Sales | Microsoft Docs
description: En savoir plus sur la synchronisation des données entre Business Central et Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 4b6137f6d5fa057d801a1afe30480017ceadd1c8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879097"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Planification d'une synchronisation entre Business Central et Dynamics 365 Sales
Vous pouvez synchroniser [!INCLUDE[d365fin](includes/d365fin_md.md)] avec [!INCLUDE[crm_md](includes/crm_md.md)] à des intervalles planifiés en configurant des projets dans la file projets. Les projets de synchronisation permettent de synchroniser les données des enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] qui ont été précédemment couplés ensemble. Ou bien, pour les enregistrements qui ne sont pas encore couplés, selon la direction et les règles de synchronisation, les projets de synchronisation peuvent créer des enregistrements et les coupler dans le système de destination. Plusieurs projets de synchronisation sont disponibles et prêts à l'emploi. Vous pouvez les visualiser sur la page **Écritures file d'attente des travaux**. Pour plus d'informations, voir [Utiliser des files d'attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## <a name="synchronization-process"></a>Processus de synchronisation  
Chaque écriture de file projets de synchronisation utilise un mappage de table d'intégration spécifique qui indique la table [!INCLUDE[d365fin](includes/d365fin_md.md)] et l'entité [!INCLUDE[crm_md](includes/crm_md.md)] à synchroniser. Les mappages de table incluent également des paramètres qui contrôlent les enregistrements de la table [!INCLUDE[d365fin](includes/d365fin_md.md)] et de l'entité [!INCLUDE[crm_md](includes/crm_md.md)] à synchroniser.  

Pour synchroniser les données, les enregistrements d'entité [!INCLUDE[crm_md](includes/crm_md.md)] doivent être couplés à des enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)]. Par exemple, un client [!INCLUDE[d365fin](includes/d365fin_md.md)] doit être couplé à un compte [!INCLUDE[crm_md](includes/crm_md.md)]. Vous pouvez définir des couplages manuellement, avant d'exécuter les projets de synchronisation, ou laisser les projets de synchronisation définir automatiquement des couplages. La liste suivante décrit la manière dont les données sont synchronisées entre [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)] lorsque vous utilisez les écritures de file projets de synchronisation. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md).

-   La case à cocher **Synch. uniquement les enregistrements couplés** contrôle si de nouveaux enregistrements sont créés lors de la synchronisation. Par défaut, la case à cocher est activée, ce qui signifie que seuls les enregistrements couplés sont synchronisés. Dans le mappage de la table d'intégration, vous pouvez modifier le mappage de table entre une entité [!INCLUDE[crm_md](includes/crm_md.md)] et une table [!INCLUDE[d365fin](includes/d365fin_md.md)] afin que les projets de synchronisation de l'intégration créent des enregistrements dans la base de données de destination pour chaque enregistrement de la base de données source qui n'est pas couplé. Pour plus d'informations, voir [Création d'enregistrements](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Exemple** Si vous désactivez la case à cocher **Synch. uniquement les enregistrements couplés**, lorsque vous synchronisez les clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les comptes dans [!INCLUDE[crm_md](includes/crm_md.md)], un nouveau compte est créé pour chaque client dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et couplé automatiquement. En outre, puisque la synchronisation est bidirectionnelle dans ce cas, un client est créé et couplé pour chaque compte [!INCLUDE[crm_md](includes/crm_md.md)] qui n'est pas encore couplé.  

    > [!NOTE]  
    > Des règles et des filtres permettent de déterminer les données synchronisées. Pour plus d'informations, reportez-vous à la rubrique [Règles de synchronisation](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Lorsque des enregistrements sont créés dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ils utilisent le modèle défini pour le mappage de table d'intégration ou le modèle par défaut qui est disponible pour le type d'enregistrement. Les champs sont renseignés avec des données depuis [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[crm_md](includes/crm_md.md)] en fonction du sens de synchronisation. Pour en savoir plus, voir [Modifier les mappages de table pour la synchronisation](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Avec les synchronisations suivantes, seuls les enregistrements qui ont été modifiés ou ajoutés après le dernier projet de synchronisation réussi pour l'entité seront mis à jour.  

     Les nouveaux enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)] sont ajoutés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si les données des champs des enregistrements [!INCLUDE[crm_md](includes/crm_md.md)] ont été modifiées, elles sont copiées dans le champ correspondant de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Avec la synchronisation bidirectionnelle, le projet effectue une synchronisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)], puis de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Écritures de file projets de synchronisation par défaut  
Le tableau suivant décrit les projets de synchronisation par défaut.  

|Écriture file d'attente des travaux|Description|Sens|Correspondance table intégration|Fréquence de synchronisation par défaut (minutes)|Temps de veille pour inactivité par défaut (minutes)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Projet de synchronisation Dynamics 365 Sales - CONTACT|Permet de synchroniser les contacts [!INCLUDE[crm_md](includes/crm_md.md)] aux contacts [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirectionnel|CONTACT|30|720 <br>(12 heures)| 
|Projet de synchronisation Dynamics 365 Sales - DEVISE|Permet de synchroniser les devises de transaction [!INCLUDE[crm_md](includes/crm_md.md)] avec les devises [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|DEVISE|30|720 <br> (12 heures)| 
|Projet de synchronisation Dynamics 365 Sales - CLIENT|Permet de synchroniser les comptes [!INCLUDE[crm_md](includes/crm_md.md)] avec les clients [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidirectionnel|CLIENT|30|720<br> (12 heures)|
|Projet de synchronisation Dynamics 365 Sales - GRPPRXCLI-PRIX|Permet de synchroniser les listes de prix de vente [!INCLUDE[crm_md](includes/crm_md.md)] avec les groupes de prix client [!INCLUDE[d365fin](includes/d365fin_md.md)].| |GROUPES DE PRIX CLIENT - LISTES DE PRIX DE VENTE|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - ARTICLE - PRODUIT|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les articles [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|ARTICLE-PRODUIT|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - FACTVENTEVALIDEES-FACT|Permet de synchroniser les factures [!INCLUDE[crm_md](includes/crm_md.md)] avec les factures vente [!INCLUDE[d365fin](includes/d365fin_md.md)] validées.|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|FACTURES - FACTURES VENTE VALIDÉES|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - RESSOURCE-PRODUIT|Permet de synchroniser les produits [!INCLUDE[crm_md](includes/crm_md.md)] avec les ressources [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUIT|30|720<br> (12 heures)|  
|Projet de synchronisation Dynamics 365 Sales - VENDEURS|Permet de synchroniser les vendeurs [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les utilisateurs [!INCLUDE[crm_md](includes/crm_md.md)].|De [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)]|VENDEURS|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - PRXVENTE-PRXPRODUIT|Permet de synchroniser les prix de produit [!INCLUDE[crm_md](includes/crm_md.md)] avec les prix de vente [!INCLUDE[d365fin](includes/d365fin_md.md)].||PRIX DE PRODUIT - PRIX DE VENTE|30|1440<br> (24 heures)|
|Projet de synchronisation Dynamics 365 Sales - UNITÉ DE MESURE|Permet de synchroniser les groupes d'unités [!INCLUDE[crm_md](includes/crm_md.md)] avec les unités de mesure [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)]|UNITÉ DE MESURE|30|720<br> (12 heures)|  
|Synchronisation Statistiques client - Dynamics 365 Sales|Permet de mettre à jour les comptes [!INCLUDE[crm_md](includes/crm_md.md)] avec les données client [!INCLUDE[d365fin](includes/d365fin_md.md)] les plus récentes. Dans [!INCLUDE[crm_md](includes/crm_md.md)], ces informations s'affichent dans le formulaire de vue rapide **Statistiques de compte Business Central** des comptes couplés avec les clients [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Ces données peuvent être également mises à jour manuellement depuis chaque enregistrement du client. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Remarque :** cette file d'attente de projets est pertinente uniquement si la solution d'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] est installée dans [!INCLUDE[crm_md](includes/crm_md.md)]. Pour en savoir plus, reportez-vous à la rubrique [À propos de la solution d'intégration Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Non applicable|Non applicable|30|Non applicable|   

## <a name="about-inactivity-timeouts"></a>À propos des délais d'inactivité
Certaines écritures de la file d'attente des travaux, comme celles qui planifient la synchronisation entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] utilisent le champ **Délai d'inactivité** sur la carte Écriture file d'attente des travaux pour empêcher l'exécution inutile des écritures de la file d'attente des travaux.  
<br><br>

> ![Organigramme de la mise en attente des écritures de la file d'attente des travaux pour cause d'inactivité.](media/on-hold-with-inactivity-timeout.png)

Lorsque la valeur de ce champ n'est pas nulle et que la file d'attente des travaux n'a trouvé aucune modification lors de la dernière exécution, [!INCLUDE[d365fin](includes/d365fin_md.md)] met en attente l'écriture de la file d'attente des travaux. Lorsque cela se produit, le champ **Statut de la file d'attente des travaux** indique **En attente en raison d'une indisponibilité**, et [!INCLUDE[d365fin](includes/d365fin_md.md)] patiente jusqu'à la fin de la période spécifiée dans le champ **Délai d'inactivité** avant d'exécuter à nouveau l'écriture de la file d'attente des travaux. 

Par exemple, par défaut, l'écriture de la file d'attente des travaux CURRENCY, qui synchronise les devises dans [!INCLUDE[crm_md](includes/crm_md.md)] avec les taux de change dans [!INCLUDE[d365fin](includes/d365fin_md.md)], recherche des modifications des taux de change toutes les 30 minutes. Si aucune modification n'est trouvée, [!INCLUDE[d365fin](includes/d365fin_md.md)] met en attente l'écriture de la file d'attente des travaux CURRENCY pendant 720 minutes (six heures). Si un taux de change est modifié dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pendant que l'écriture de la file d'attente des travaux est en attente, [!INCLUDE[d365fin](includes/d365fin_md.md)] réactive automatiquement l'écriture de la file d'attente des travaux et redémarre la file d'attente des travaux. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] active automatiquement les écritures de la file d'attente des travaux qui sont en attente uniquement lorsque des modifications sont apportées dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Les modifications dans [!INCLUDE[crm_md](includes/crm_md.md)] n'activent pas les écritures de la file d'attente des travaux.

## <a name="to-view-the-synchronization-job-log"></a>Pour afficher le journal des projets de synchronisation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Journal de synchronisation d'intégration**, puis choisissez le lien associé.
2.  Si une ou plusieurs erreurs se sont produites pour un projet de synchronisation, le nombre d'erreurs s'affiche dans la colonne **Échec**. Pour afficher les erreurs pour le projet, sélectionnez le numéro.  

    > [!TIP]  
    > Vous pouvez afficher toutes les erreurs du projet de synchronisation en ouvrant directement le journal des erreurs du projet de synchronisation.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Pour afficher le journal du projet de synchronisation à partir des mappages de table  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Mappages de table d'intégration**, puis choisissez le lien associé.
2.  Sur la page **Mappages de table d'intégration**, sélectionnez une écriture, puis choisissez **Journal projet synch. intégration**.  

## <a name="to-view-the-synchronization-error-log"></a>Pour afficher le journal des erreurs de synchronisation  
* Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Erreurs de synchronisation d'intégration**, puis choisissez le lien associé.

## <a name="see-also"></a>Voir aussi  
[Synchronisation des données dans Business Central et Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synchroniser manuellement les mappages de table](admin-manual-synchronization-of-table-mappings.md)  
[Planification d'une synchronisation entre Business Central et Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[À propos de l'intégration de Dynamics 365 Business Central avec Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
