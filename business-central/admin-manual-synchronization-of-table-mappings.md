---
title: Synchronisation manuelle des mappages de table | Microsoft Docs
description: La synchronisation copie les données entre les écritures Dynamics 365 for Sales et Business Central pour conserver les deux systèmes à jour.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 368bfc191aea4ae00c53d0c7ee892f3cc82c0ff7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245746"
---
# <a name="manually-synchronize-table-mappings"></a>Synchroniser manuellement les mappages de table
Un mappage de table d'intégration associe une table [!INCLUDE[d365fin](includes/d365fin_md.md)] (type d'enregistrement), telle qu'un client, à une entité [!INCLUDE[crm_md](includes/crm_md.md)], telle qu'un compte. Synchroniser un mappage de table d'intégration vous permet de synchroniser les données dans tous les enregistrements de la table [!INCLUDE[d365fin](includes/d365fin_md.md)] et de l'entité [!INCLUDE[crm_md](includes/crm_md.md)] qui sont couplés. En outre, selon la configuration du mappage de la table, la synchronisation peut créer et coupler de nouveaux enregistrements dans la solution de destination pour les enregistrements non couplés dans le source.  

Synchroniser manuellement les mappages de table d'intégration peut être utile pendant la configuration initiale d'une intégration, et lors du diagnostic des erreurs de synchronisation.  

Cet article décrit trois méthodes pour synchroniser manuellement les mappages de table d'intégration. Chaque méthode fournit un autre niveau de synchronisation.

## <a name="run-a-full-synchronization"></a>Exécuter une synchronisation complète
Une synchronisation complète exécute tous les projets de synchronisation d'intégration par défaut pour synchroniser les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] et les entités [!INCLUDE[crm_md](includes/crm_md.md)], comme défini sur la page **Mappages de table d'intégration**. 

Une synchronisation complète exécute les opérations suivantes pour les enregistrements [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[crm_md](includes/crm_md.md)] qui :

* ne sont pas couplés ; un nouvel enregistrement de correspondance est créé et couplé à la solution opposée.
La condition de création d'un enregistrement et son emplacement de création dépendent du sens de la synchronisation. Par exemple, lors de la synchronisation des données depuis les clients [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les comptes [!INCLUDE[crm_md](includes/crm_md.md)], si un client n'est pas couplé à un compte, un compte est automatiquement ajouté dans [!INCLUDE[crm_md](includes/crm_md.md)] et couplé au client dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. L'opposé se vérifie également lorsque le sens de synchronisation va de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour chaque compte qui n'est pas déjà couplé à un client, un nouveau client correspondant est créé dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et associé au compte dans [!INCLUDE[crm_md](includes/crm_md.md)].  

     > [!NOTE]  
     >  Pour y parvenir, l'opération de synchronisation complète désactive temporairement l'option **Synch. uniquement les enregistrements couplés** sur le mappage de la table d'intégration qui est utilisé par le projet de synchronisation. À la fin du processus de synchronisation complet, vous êtes invité à indiquer si vous souhaitez conserver cette option désactivée pour tous les projets.  

* Couplé, le sens de synchronisation (par exemple, de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)] ou de [!INCLUDE[crm_md](includes/crm_md.md)]vers [!INCLUDE[d365fin](includes/d365fin_md.md)]) est prédéterminé par les mappages de table d'intégration. Pour en savoir plus, reportez-vous à la rubrique [Mappage d'entité Sales standard pour la synchronisation](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization).  

Les projets sont exécutés dans l'ordre suivant pour éviter les dépendances de couplage entre les entités.  

1.  Projet de synchronisation DEVISE - Dynamics 365 for Sales  
2.  Projet de synchronisation VENDEURS - Dynamics 365 for Sales  
3.  Projet Synchronisation UNITÉ DE MESURE - Dynamics 365 for Sales  
4.  Projet de synchronisation CLIENT - Dynamics 365 for Sales  
5.  Projet de synchronisation CONTACTS - Dynamics 365 for Sales  
6.  Projet de synchronisation RESSOURCE-PRODUIT - Dynamics 365 for Sales  
7.  Projet de synchronisation ARTICLE-PRODUIT - Dynamics 365 for Sales  

> [!IMPORTANT]  
>  Généralement, vous utilisez uniquement la synchronisation complète lors de la configuration initiale de l'intégration entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)] et lorsqu'une seule des solutions contient des données que vous souhaitez copier vers l'autre solution. Une synchronisation complète peut être utile dans un environnement de démonstration. Parce que la synchronisation complète crée et couple automatiquement les enregistrements entre les solutions, il est plus rapide de commencer à travailler avec la synchronisation des données entre les enregistrements. D'autre part, vous devez exécuter une synchronisation complète uniquement si vous souhaitez un enregistrement dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour chaque enregistrement dans [!INCLUDE[crm_md](includes/crm_md.md)] pour les mappages de table donnés. Sinon, vous vous exposez à un risque d'enregistrements non désirés ou en double dans [!INCLUDE[d365fin](includes/d365fin_md.md)] ou [!INCLUDE[crm_md](includes/crm_md.md)].  

### <a name="see-the-process-for-a-full-synchronization"></a>Voir le processus pour une synchronisation complète
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### <a name="to-run-a-full-synchronization"></a>Pour exécuter une synchronisation complète  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de la connexion Microsoft Dynamics 365 for Sales**, puis choisissez le lien associé.
2.  Choisissez l'action **Exécuter une synchronisation complète**, puis cliquez sur le bouton **Oui**.  
3.  Une fois la synchronisation complète terminée, vous pouvez préciser si vous laissez les projets de synchronisation prévus créer de nouveaux enregistrements.  

    Si vous souhaitez que tous les projets de synchronisation créent de nouveaux enregistrements dans la destination pour des enregistrements non couplés dans la source, sélectionnez **Oui**. Cela définit le champ **Synch. uniquement les enregistrements couplés** sur les mappages de table utilisés par les projets de synchronisation.  

    Si vous souhaitez que les projets de synchronisation s'exécutent comme précédemment avant la synchronisation complète par rapport à la création de nouveaux enregistrements, sélectionnez **Non**. Cela définit le champ **Synch. uniquement les enregistrements couplés** sur le paramètre précédent pour la synchronisation complète.  

Vous pouvez afficher les résultats de la synchronisation complète sur la page **Projets de synchronisation d'intégration**. Pour plus d'informations, voir [Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synchronisation de tous les enregistrements modifiés
Vous pouvez utiliser la page **Configuration de la connexion Microsoft Dynamics 365 for Sales** pour synchroniser les modifications des données dans tous les mappages de table d'intégration. Ce processus est similaire à une synchronisation complète. Cela synchronisera les données dans tous les enregistrements couplés dans les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] et les entités [!INCLUDE[crm_md](includes/crm_md.md)] définies dans les mappages de table. Par défaut, seuls les enregistrements qui ont été modifiés depuis la dernière synchronisation seront synchronisés. Les mappages de table sont synchronisés dans l'ordre suivant pour éviter les dépendances de couplage entre les entités :  

1.  Projet de synchronisation DEVISE - Dynamics 365 for Sales  
2.  Projet de synchronisation VENDEURS - Dynamics 365 for Sales  
3.  Projet Synchronisation UNITÉ DE MESURE - Dynamics 365 for Sales  
4.  Projet de synchronisation CLIENT - Dynamics 365 for Sales  
5.  Projet de synchronisation CONTACTS - Dynamics 365 for Sales  
6.  Projet de synchronisation RESSOURCE-PRODUIT \- Dynamics 365 for Sales  
7.  Projet de synchronisation ARTICLE-PRODUIT - Dynamics 365 for Sales  

Vous pouvez afficher les résultats de la synchronisation sur la page **Projets de synchronisation d'intégration**. Pour plus d'informations, voir [Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  En modifiant le mappage de table d'intégration à l'avance, vous pouvez configurer la synchronisation avec des filtres pour contrôler quels enregistrements sont synchronisés ou configurez-le pour créer de nouveaux enregistrements dans la solution de destination pour les enregistrements non couplés dans la source. Pour en savoir plus, voir [Modifier les mappages de table pour la synchronisation](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Pour synchroniser les enregistrements pour toutes les tables  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de la connexion Microsoft Dynamics 365 for Sales**, puis choisissez le lien associé.
2.  Choisissez l'action **Synchroniser les enregistrements modifiés**, puis sélectionnez **Oui**.  

## <a name="synchronize-individual-table-mappings"></a>Synchroniser les mappages de table individuels
Vous pouvez utiliser la page **Mappages de table d'intégration** pour exécuter des mappages de table spécifiques à un projet de synchronisation. Cela synchronisera les données dans tous les enregistrements couplés dans la table [!INCLUDE[d365fin](includes/d365fin_md.md)] et l'entité [!INCLUDE[crm_md](includes/crm_md.md)] définies dans le mappage de table. Par défaut, seuls les enregistrements qui ont été modifiés depuis la dernière synchronisation seront synchronisés.  

En modifiant le mappage de la table d'intégration à l'avance, vous pouvez configurer le projet de synchronisation pour créer de nouveaux enregistrements dans la solution de destination pour les enregistrements non couplés dans la source.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Pour synchroniser les enregistrements d'un mappage de table d'intégration  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mappages de table d'intégration**, puis sélectionnez le lien associé.
2.  Choisissez l'action **Synchroniser les enregistrements modifiés**, puis sélectionnez **Oui**.  

## <a name="see-also"></a>Voir aussi  
[Synchronisation de Business Central et de Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Configuration de l'intégration de Dynamics 365 for Sales dans Business Central](admin-setting-up-integration-with-dynamics-sales.md)   
