---
title: Afficher le statut des projets de synchronisation (contient une vidéo)
description: Utilisez la page Erreurs de synchronisation de données couplées pour afficher l’état des projets de synchronisation exécutés pour les enregistrements couplés dans des intégrations.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
---

# <a name="view-the-status-of-synchronization-jobs"></a>Afficher le statut des projets de synchronisation


Utilisez la page **Erreurs de synchronisation des données couplées** pour afficher le statut des projets de synchronisation exécutés pour les enregistrements couplés dans une intégration Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Cela inclut les projets ayant été exécutés à partir de la file projets et les projets de synchronisation manuels qui ont été exécutés sur les enregistrements à partir du client [!INCLUDE[prod_short](includes/prod_short.md)]. Par exemple, l’affichage de leur statut est utile lors du dépannage, car il vous donne accès à des informations détaillées sur les erreurs liées aux enregistrements couplés. En règle générale, ces types d’erreur sont provoqués par des actions de l’utilisateur, par exemple lorsque :  

* Deux personnes ont modifié les mêmes données dans les deux applications professionnelles.
* Une personne a supprimé les données dans l’une des applications, mais pas les deux.

> [!Note]
> La page **Erreurs de synchronisation de données couplées** affiche des informations sur les projets liés aux enregistrements couplés. Si vous résolvez toutes les erreurs mais que les enregistrements ne sont toujours pas synchronisés, cela peut avoir quelque chose à voir avec un paramètre d’intégration. En règle générale, votre administrateur devra résoudre ces types d’erreurs.   

## <a name="example"></a>Exemple :
Cette vidéo montre un exemple de dépannage des erreurs survenues lors de la synchronisation avec [!INCLUDE[prod_short](includes/cds_long_md.md)]. Le processus sera le même pour toutes les intégrations. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Pour afficher et résoudre les erreurs de synchronisation des enregistrements couplés
1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Erreurs de synchronisation des données couplées**, puis choisissez le lien associé.
2. La page **Erreurs de synchronisation des données couplées** affiche les problèmes qui se produisent lorsque vous avez synchronisé des enregistrements couplés. Le tableau suivant répertorie les actions que vous pouvez utiliser pour résoudre les problèmes un par un :

|Action|Description|
|----|----|
|**Supprimer le couplage**|Découple les enregistrements et ils ne seront plus synchronisés. Pour redémarrer la synchronisation, vous devez les coupler à nouveau. |
|**Réessayer** et **Réessayer tout**|Pour chaque enregistrement dans lequel une erreur est détectée, la synchronisation est ignorée sauf si vous corrigez le problème. Réessayer inclut l’enregistrement sélectionné dans la prochaine synchronisation, et **Réessayer tout** comprend tous les enregistrements.|
|**Synchroniser**|L’application tentera de résoudre un conflit lorsque les données ont été modifiées dans les deux applications professionnelles. Vous pouvez choisir les données à utiliser.|
|**Restaurer des enregistrements** et **Supprimer des enregistrements**|Celles-ci sont utiles lorsqu’un enregistrement a été supprimé dans l’une des applications métier. Supprimer les enregistrements supprime l’enregistrement ou la ligne dans l’application où il existe toujours. La restauration des enregistrement recrée l’enregistrement ou la ligne dans l’application métier où elle a été supprimée.|

> [!NOTE]
> Pour réduire le nombre de conflits à résoudre, vous pouvez configurer vos mappages de table d’intégration pour appliquer ces actions automatiquement. Pour plus d’informations, voir [Gestion des tables d’intégration](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Pour afficher le journal de synchronisation pour un enregistrement spécifique (synchronisé manuellement)
1. Ouvrez, par exemple, un client, un article ou tout autre enregistrement qui synchronise des données entre [!INCLUDE[prod_short](includes/prod_short.md)] et Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)].
2. Choisissez l’action **Journal de synchronisation** pour afficher le journal de synchronisation pour un enregistrement sélectionné. Par exemple, un client spécifique que vous avez synchronisé manuellement.

## <a name="remove-couplings-between-records"></a>Supprimer les couplages entre les enregistrements
Lorsque quelque chose ne va pas dans votre intégration et que vous devez découpler des enregistrements pour arrêter de les synchroniser, vous pouvez le faire pour un ou plusieurs enregistrements à la fois. Vous pouvez découpler un ou plusieurs enregistrements des pages de liste ou sur la page **Erreurs de synchronisation de données couplées** en choisissant une ou plusieurs lignes et en choisissant **Supprimer le couplage**. Vous pouvez également supprimer tous les couplages pour un ou plusieurs mappages de table sur la page **Mappages de table d’intégration**. 

Si une entité avec un couplage unidirectionnel est supprimée dans [!INCLUDE[prod_short](includes/prod_short.md)], vous devez supprimer manuellement le couplage rompu. Pour ce faire, sur la page **Erreurs de synchronisation de données couplées**, choisissez l′action **Rechercher des suppressions**, puis supprimez les couplages.

## <a name="see-also"></a>Voir aussi
[Configuration des comptes d’utilisateur pour l’intégration à Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Utiliser Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
