---
title: Synchronisation manuelle des mappages de table | Microsoft Docs
description: "La synchronisation copie les données entre les tables Microsoft Dataverse et Business\_Central pour conserver les deux systèmes à jour."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="manually-synchronize-table-mappings"></a>Synchroniser manuellement les mappages de table


Un mappage de table d’intégration associe une table [!INCLUDE[prod_short](includes/prod_short.md)], telle qu’un client, à une table [!INCLUDE[prod_short](includes/cds_long_md.md)], telle qu’un compte. Synchroniser un mappage de table d’intégration vous permet de synchroniser les données dans tous les enregistrements de la table [!INCLUDE[prod_short](includes/prod_short.md)] et de la table [!INCLUDE[prod_short](includes/cds_long_md.md)] qui sont couplés. En outre, selon la configuration du mappage de la table, la synchronisation peut créer et coupler de nouveaux enregistrements dans la solution de destination pour les enregistrements non couplés dans le source.  

Synchroniser manuellement les mappages de table d’intégration peut être utile pendant la configuration initiale d’une intégration, et lors du diagnostic des erreurs de synchronisation.  

Cet article décrit trois méthodes pour synchroniser manuellement les mappages de table d’intégration. Chaque méthode fournit un autre niveau de synchronisation.

## <a name="run-a-full-synchronization"></a>Exécuter une synchronisation complète
Une synchronisation complète exécute tous les projets de synchronisation d’intégration par défaut pour synchroniser les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] et les tables [!INCLUDE[prod_short](includes/cds_long_md.md)], comme défini sur la page **Mappages de table d’intégration**. 

Une synchronisation complète exécute les opérations suivantes pour les enregistrements [!INCLUDE[prod_short](includes/prod_short.md)] ou [!INCLUDE[prod_short](includes/cds_long_md.md)] qui :

* ne sont pas couplés ; une nouvelle ligne de correspondance est créée et couplée à la solution opposée.
La condition de création d’une ligne et son emplacement de création dépendent du sens de la synchronisation. Par exemple, lors de la synchronisation des données depuis les clients [!INCLUDE[prod_short](includes/prod_short.md)] avec les comptes [!INCLUDE[prod_short](includes/cds_long_md.md)], si un client n’est pas couplé à un compte, un compte est automatiquement ajouté dans [!INCLUDE[prod_short](includes/cds_long_md.md)] et couplé au client dans [!INCLUDE[prod_short](includes/prod_short.md)]. L’opposé se vérifie également lorsque le sens de synchronisation va de [!INCLUDE[prod_short](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)]. Pour chaque compte qui n’est pas déjà couplé à un client, un nouveau client correspondant est créé dans [!INCLUDE[prod_short](includes/prod_short.md)] et associé au compte dans [!INCLUDE[prod_short](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  Pour y parvenir, l’opération de synchronisation complète désactive temporairement l’option **Synch. uniquement les enregistrements couplés** sur le mappage de la table d’intégration qui est utilisé par le projet de synchronisation. À la fin du processus de synchronisation complet, vous êtes invité à indiquer si vous souhaitez conserver cette option désactivée pour tous les projets.  

* Couplé, le sens de synchronisation (par exemple, de [!INCLUDE[prod_short](includes/prod_short.md)] vers [!INCLUDE[prod_short](includes/cds_long_md.md)] ou de [!INCLUDE[prod_short](includes/cds_long_md.md)] vers [!INCLUDE[prod_short](includes/prod_short.md)]) est prédéterminé par les mappages de table d’intégration. Pour en savoir plus, consultez [Mappage de table standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Généralement, vous utilisez uniquement la synchronisation complète lors de la configuration initiale de l’intégration entre [!INCLUDE[prod_short](includes/prod_short.md)] et [!INCLUDE[prod_short](includes/cds_long_md.md)] et lorsqu’une seule des solutions contient des données que vous souhaitez copier vers l’autre solution. Une synchronisation complète peut être utile dans un environnement de démonstration. Parce que la synchronisation complète crée et couple automatiquement les enregistrements entre les solutions, il est plus rapide de commencer à travailler avec la synchronisation des données entre les enregistrements. D’autre part, vous devez exécuter une synchronisation complète uniquement si vous souhaitez une ligne dans [!INCLUDE[prod_short](includes/prod_short.md)] pour chaque ligne dans [!INCLUDE[prod_short](includes/cds_long_md.md)] pour les mappages de table donnés. Sinon, vous vous exposez à un risque d’enregistrements non désirés ou en double dans [!INCLUDE[prod_short](includes/prod_short.md)] ou [!INCLUDE[prod_short](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Pour exécuter une synchronisation complète
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion Dataverse**, puis choisissez le lien associé.

    > [!NOTE]
    > Si vous souhaitez exécuter une synchronisation complète pour les tables au moyen de Dynamics 365 Sales, utilisez plutôt la page **Paramètres de la connexion Microsoft Dynamics 365 for Sales**.

2.  Choisissez l’action **Exécuter une synchronisation complète**, puis cliquez sur le bouton **Oui**.  
3.  Une fois la synchronisation complète terminée, vous pouvez préciser si vous laissez les projets de synchronisation prévus créer de nouveaux enregistrements.  

    Si vous souhaitez que tous les projets de synchronisation créent de nouveaux enregistrements dans la destination pour des enregistrements non couplés dans la source, sélectionnez **Oui**. Cela définit le champ **Synch. uniquement les enregistrements couplés** sur les mappages de table utilisés par les projets de synchronisation.  

    Si vous souhaitez que les projets de synchronisation s’exécutent comme précédemment avant la synchronisation complète par rapport à la création de nouveaux enregistrements, sélectionnez **Non**. Cela définit le champ **Synch. uniquement les enregistrements couplés** sur le paramètre précédent pour la synchronisation complète.  

Vous pouvez afficher les résultats de la synchronisation complète sur la page **Projets de synchronisation d’intégration**. Pour plus d’informations, voir [Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synchronisation de tous les enregistrements modifiés
Vous pouvez utiliser la page **Configuration de la connexion Common Data Service** pour synchroniser les modifications des données dans tous les mappages de table d’intégration. Ce processus est similaire à une synchronisation complète. Cela synchronisera les données dans tous les enregistrements couplés dans les tables [!INCLUDE[prod_short](includes/prod_short.md)] et les tables [!INCLUDE[prod_short](includes/cds_long_md.md)] définies dans les mappages de table. Par défaut, seules les données qui ont été modifiées depuis la dernière synchronisation seront synchronisés. Les projets de synchronisation permettente de synchroniser les mappages de table dans l’ordre suivant pour éviter les dépendances de couplage entre les tables :  

1.  DEVISE  
2.  VENDEURS  
3.  FOURNISSEUR  
4.  CLIENT  
5.  CONTACTS  

Vous pouvez afficher les résultats de la synchronisation sur la page **Projets de synchronisation d’intégration**. Pour plus d’informations, voir [Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  En modifiant le mappage de table d’intégration à l’avance, vous pouvez créer des filtres pour contrôler les données à synchroniser, ou configurer les mappages pour créer de nouvelles données dans la solution de destination pour les enregistrements ou les lignes non couplés dans la source. Pour en savoir plus, voir [Modifier les mappages de table pour la synchronisation](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables"></a>Pour synchroniser les données pour toutes les tables
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration de la connexion Microsoft Dynamics 365 Sales**, puis choisissez le lien associé.
2.  Choisissez l’action **Synchroniser les enregistrements modifiés**, puis sélectionnez **Oui**.  

## <a name="synchronize-individual-table-mappings"></a>Synchroniser les mappages de table individuels
Vous pouvez utiliser la page **Mappages de table d’intégration** pour exécuter des mappages de table à un projet de synchronisation. Cela synchronisera les données dans tous les enregistrements et lignes couplés dans les tables [!INCLUDE[prod_short](includes/prod_short.md)] et l’entité [!INCLUDE[prod_short](includes/cds_long_md.md)] définies dans le mappage de table. Par défaut, seules les données qui ont été modifiées depuis la dernière synchronisation seront synchronisés.  

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Pour synchroniser les enregistrements d’un mappage de table d’intégration
1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Mappages de table d’intégration**, puis choisissez le lien associé.
2.  Choisissez l’action **Synchroniser les enregistrements modifiés**, puis sélectionnez **Oui**.  

## <a name="see-also"></a>Voir aussi
[Synchronisation de Business Central et Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Configuration des comptes d’utilisateur pour l’intégration à Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
