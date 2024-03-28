---
title: "Synchronisation de Business\_Central et de Dataverse"
description: "En savoir plus sur la synchronisation des données entre Business\_Central et Dataverse."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.service: dynamics-365-business-central
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Planification d’une synchronisation entre Business Central et Dataverse

Vous pouvez synchroniser [!INCLUDE[prod_short](includes/prod_short.md)] avec [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à des intervalles planifiés en configurant des projets dans la file projets. Les projets de synchronisation permettent de synchroniser les données des enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)] qui sont couplés. Pour les enregistrements qui ne sont pas encore couplés, selon la direction et les règles de synchronisation, les projets de synchronisation peuvent créer des enregistrements et les coupler dans le système de destination.

Plusieurs projets de synchronisation sont disponibles et prêts à l’emploi. Les projets sont exécutés dans l’ordre suivant pour éviter les dépendances de couplage entre les tables. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

1. Projet de synchronisation DEVISE - Common Data Service.
2. Projet de synchronisation FOURNISSEUR - Common Data Service.
3. Projet de synchronisation CONTACT - Common Data Service.
4. Projet de synchronisation CLIENT - Common Data Service.
5. Projet de synchronisation VENDEURS - Common Data Service.

Vous pouvez visualiser les projets sur la page **Écritures file d’attente des travaux**. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Écritures de file projets de synchronisation par défaut

Le tableau suivant décrit les projets de synchronisation par défaut pour [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Écriture file d’attente des travaux | Description | Sens | Mappage de table d’intégration | Fréquence de synchronisation par défaut (minutes) | Temps de veille pour inactivité par défaut (minutes) |
|--|--|--|--|--|--|--|
| Projet de synchronisation CONTACT - Common Data Service | Permet de synchroniser les contacts [!INCLUDE[cds_long_md](includes/cds_long_md.md)] aux contacts [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidirectionnel | CONTACT | 30 | 720 <br>(12 heures) |
| Projet de synchronisation DEVISE - Common Data Service | Permet de synchroniser les devises de transaction [!INCLUDE[cds_long_md](includes/cds_long_md.md)] avec les devises [!INCLUDE[prod_short](includes/prod_short.md)]. | De [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | DEVISE | 30 | 720 <br> (12 heures) |
| Projet de synchronisation CLIENT - Common Data Service | Permet de synchroniser les comptes [!INCLUDE[cds_long_md](includes/cds_long_md.md)] avec les clients [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidirectionnel | CLIENT | 30 | 720<br> (12 heures) |
| Projet de synchronisation FOURNISSEUR - Common Data Service | Permet de synchroniser les comptes [!INCLUDE[cds_long_md](includes/cds_long_md.md)] avec les clients [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidirectionnel | FOURNISSEUR | 30 | 720<br> (12 heures) |
| Projet de synchronisation VENDEURS - Common Data Service | Permet de synchroniser les vendeurs [!INCLUDE[prod_short](includes/prod_short.md)] avec les utilisateurs [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. | De [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)] | VENDEURS | 30 | 1440<br> (24 heures) |

## <a name="synchronization-process"></a>Processus de synchronisation

Chaque écriture de file projets de synchronisation utilise un mappage de table d’intégration spécifique qui indique la table [!INCLUDE[prod_short](includes/prod_short.md)] et la table [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à synchroniser. Les mappages de table incluent également des paramètres qui contrôlent les enregistrements de la table [!INCLUDE[prod_short](includes/prod_short.md)] et de la table [!INCLUDE[cds_long_md](includes/cds_long_md.md)] à synchroniser.  

Pour synchroniser les données, les enregistrements de table [!INCLUDE[cds_long_md](includes/cds_long_md.md)] doivent être couplés à des enregistrements [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, un client [!INCLUDE[prod_short](includes/prod_short.md)] doit être couplé à un compte [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Vous pouvez définir des couplages manuellement, avant d’exécuter les projets de synchronisation, ou laisser les projets de synchronisation définir automatiquement des couplages. La liste suivante décrit la manière dont les données sont synchronisées entre [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et [!INCLUDE[prod_short](includes/prod_short.md)] lorsque vous utilisez les écritures de file projets de synchronisation. Pour en savoir plus, reportez-vous à la rubrique [Coupler et synchroniser manuellement les enregistrements](admin-how-to-couple-and-synchronize-records-manually.md).

- La case à cocher **Synch. uniquement les enregistrements couplés** contrôle si de nouveaux enregistrements sont créés lors de la synchronisation. Par défaut, la case à cocher est activée, ce qui signifie que seuls les enregistrements couplés sont synchronisés. Dans le mappage de la table d’intégration, vous pouvez modifier le mappage de table entre une table [!INCLUDE[cds_long_md](includes/cds_long_md.md)] et une table [!INCLUDE[prod_short](includes/prod_short.md)] afin que les projets de synchronisation de l’intégration créent des enregistrements dans la base de données de destination pour chaque ligne de la base de données source qui n’est pas couplé. Pour plus d’informations, voir [Création d’enregistrements](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Exemple** Si vous désactivez la case à cocher **Synch. uniquement les enregistrements couplés**, lorsque vous synchronisez les clients dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les comptes dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)], un nouveau compte est créé pour chaque client dans [!INCLUDE[prod_short](includes/prod_short.md)] et couplé automatiquement. En outre, puisque la synchronisation est bidirectionnelle dans ce cas, un client est créé et couplé pour chaque compte [!INCLUDE[cds_long_md](includes/cds_long_md.md)] qui n’est pas encore couplé.  

    > [!NOTE]  
    > Des règles et des filtres permettent de déterminer les données synchronisées. Pour plus d’informations, accédez à [Règles de synchronisation](admin-synchronizing-business-central-and-sales.md).

- Lorsque des enregistrements sont créés dans [!INCLUDE[prod_short](includes/prod_short.md)], ils utilisent le modèle défini pour le mappage de table d’intégration ou le modèle par défaut qui est disponible pour le type de ligne. Les champs sont renseignés avec des données depuis [!INCLUDE[prod_short](includes/prod_short.md)] ou [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en fonction du sens de synchronisation. Pour en savoir plus, voir [Modifier les mappages de table pour la synchronisation](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Avec les synchronisations suivantes, seuls les enregistrements qui ont été modifiés ou ajoutés après le dernier projet de synchronisation réussi pour la table seront mis à jour.  

     Les nouveaux enregistrements dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sont ajoutés dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si les données des champs des enregistrements [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ont été modifiées, elles sont copiées dans le champ correspondant de [!INCLUDE[prod_short](includes/prod_short.md)].  

- Avec la synchronisation bidirectionnelle, le projet effectue une synchronisation de [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[cds_long_md](includes/cds_long_md.md)], puis de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>À propos des délais d’inactivité

Certaines écritures de la file d’attente des travaux, comme celles qui planifient la synchronisation entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[cds_long_md](includes/cds_long_md.md)] utilisent le champ **Délai d’inactivité** sur la page **Écriture file d’attente des travaux** pour empêcher l’exécution inutile des écritures de la file d’attente des travaux.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Organigramme de la mise en attente des écritures de la file d’attente des travaux pour cause d’inactivité.":::

Lorsque la valeur de ce champ n’est pas nulle et que la file d’attente des travaux n’a trouvé aucune modification lors de la dernière exécution, [!INCLUDE[prod_short](includes/prod_short.md)] met en attente l’écriture de la file d’attente des travaux. Lorsque cela se produit, le champ **Statut de la file d’attente des travaux** indique **En attente en raison d’une indisponibilité**, et [!INCLUDE[prod_short](includes/prod_short.md)] patiente jusqu’à la fin de la période spécifiée dans le champ **Délai d’inactivité** avant d’exécuter à nouveau l’écriture de la file d’attente des travaux.  

Par exemple, par défaut, l’écriture de la file d’attente des travaux CURRENCY, qui synchronise les devises dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] avec les taux de change dans [!INCLUDE[prod_short](includes/prod_short.md)], recherche des modifications des taux de change toutes les 30 minutes. Si aucune modification n’est trouvée, [!INCLUDE[prod_short](includes/prod_short.md)] met en attente l’écriture de la file d’attente des travaux CURRENCY pendant 720 minutes (douze heures). Si un taux de change est modifié dans [!INCLUDE[prod_short](includes/prod_short.md)] pendant que l’écriture de la file d’attente des travaux est en attente, [!INCLUDE[prod_short](includes/prod_short.md)] réactive automatiquement l’écriture de la file d’attente des travaux et redémarre la file d’attente des travaux. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] active automatiquement les écritures de la file d’attente des travaux qui sont en attente uniquement lorsque des modifications sont apportées dans [!INCLUDE[prod_short](includes/prod_short.md)]. Les modifications dans [!INCLUDE[cds_long_md](includes/cds_long_md.md)] n’activent pas les écritures de la file d’attente des travaux.

## <a name="to-view-the-synchronization-job-log"></a>Pour afficher le journal des projets de synchronisation

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Journal de synchronisation de l’intégration**, puis choisissez le lien associé.
2. Si une ou plusieurs erreurs se sont produites pour un projet de synchronisation, le nombre d’erreurs s’affiche dans la colonne **Échec**. Pour afficher les erreurs pour le projet, sélectionnez le numéro.  

    > [!TIP]  
    > Vous pouvez afficher toutes les erreurs du projet de synchronisation en ouvrant directement le journal des erreurs du projet de synchronisation.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Pour afficher le journal du projet de synchronisation à partir des mappages de table

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Mappages de table d’intégration**, puis choisissez le lien associé.
2. Sur la page **Mappages de table d’intégration**, sélectionnez une écriture, puis choisissez **Journal projet synch. intégration**.  

## <a name="to-view-the-synchronization-error-log"></a>Pour afficher le journal des erreurs de synchronisation

- Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Erreurs de synchronisation d’intégration**, puis choisissez le lien associé.

## <a name="see-also"></a>Voir aussi

[Synchronisation des données dans Business Central et [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synchroniser manuellement les mappages de table](admin-manual-synchronization-of-table-mappings.md)  
[Planification d’une synchronisation entre Business Central et [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[À propos de l’intégration de Dynamics 365 Business Central avec [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
