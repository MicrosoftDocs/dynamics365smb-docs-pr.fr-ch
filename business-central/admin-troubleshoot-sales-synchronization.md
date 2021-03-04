---
title: Dépannage des erreurs de synchronisation | Microsoft Docs
description: Fournit des indications pour identifier et résoudre les erreurs de synchronisation.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 1c2181ee381425a168a9b6b6ce321e595a01ed8e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755007"
---
# <a name="troubleshooting-synchronization-errors"></a>Résolution des erreurs de synchronisation
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Il y a beaucoup de pièces mobiles impliquées dans l’intégration [!INCLUDE[prod_short](includes/prod_short.md)] avec [!INCLUDE[prod_short](includes/cds_long_md.md)], et parfois les choses ne se passent pas bien. Cette rubrique répertorie certaines des erreurs types qui se produisent et donne des indications sur la manière de les résoudre.

Les erreurs se produisent souvent à cause de quelque chose qu’un utilisateur a fait pour coupler des enregistrements ou parce que la configuration de l’intégration est fausse. Pour les erreurs liées aux enregistrements couplés, les utilisateurs peuvent les résoudre eux-mêmes. Ces erreurs sont causées par des actions telles que la suppression de données dans l’une des applications métier mais pas les deux, puis la synchronisation. Pour plus d’informations, voir [Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Exemple :
Cette vidéo montre un exemple de dépannage des erreurs survenues lors de la synchronisation avec Sales. Le processus sera le même pour toutes les intégrations. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Les erreurs liées à la configuration de l’intégration nécessitent généralement l’attention de l’administrateur. Vous pouvez voir ces erreurs sur la page **Erreurs de synchronisation d’intégration**. Voici des exemples de problèmes classiques :  
  
* Les autorisations et les rôles attribués aux utilisateurs ne sont pas corrects.  
* Le compte administrateur a été spécifié en tant qu’utilisateur d’intégration.  
* Le mot de passe de l’utilisateur d’intégration est défini pour nécessiter une modification lorsque l’utilisateur se connecte.  
* Les taux de change pour les devises ne sont pas spécifiés dans l’une ou l’autre application.  
  
Vous devez résoudre manuellement les erreurs, mais la page vous aide de plusieurs manières. Par exemple :  

* Les champs **Source** et **Destination** peuvent contenir des liens vers la ligne où l’erreur a été trouvée. Cliquez sur le lien pour rechercher l’erreur.  
* Les actions **Supprimer les écritures ultérieures à 7 jours** et **Supprimer toutes les écritures** vont nettoyer la liste. En règle générale, vous utilisez ces actions après avoir résolu la cause d’une erreur affectant de nombreux enregistrements. Faites attention, cependant. Ces actions peuvent supprimer des erreurs toujours pertinentes.

Parfois, les horodatages sur les enregistrements peuvent provoquer des conflits. La table « Enregistrement intégration CDS » conserve les horodatages « Dernière synch. modifiée le » et « Dernière synch. CDS modifiée le » pour la dernière intégration effectuée dans les deux directions pour une ligne. Ces horodatages sont comparés aux horodatages sur les enregistrements Business Central et Sales. Dans Business Central, l’horodatage se trouve dans la table Enregistrement intégration.

Vous pouvez filtrer les enregistrements à synchroniser en comparant les horodatages des lignes dans les champs « Filtre synch. modifiée le » et « Fltr. synch. table int. mod. le » de la table « Mappage de table d’intégration ».

Le message d’erreur de conflit « Impossible de mettre à jour l’enregistrement client, car sa date de dernière modification est postérieure à celle de l’enregistrement de compte » ou « Impossible de mettre à jour l’enregistrement de compte, car sa date de dernière modification est postérieure à celle de l’enregistrement client » peut apparaître si une ligne a un horodatage supérieur au champ « Filtre synch. modifiée le » du Mappage de table d’intégration, mais s’il n’est pas plus récent que l’horodatage de l’enregistrement de l’intégration de Sales. Cela signifie que la ligne source a été synchronisée manuellement, et non par l’entrée de la file d’attente des tâches. 

Le conflit se produit, car la ligne de destination a également été modifiée : l’horodatage de ligne est plus récent que l’horodatage de l’enregistrement de l’intégration de Sales. La vérification de la destination ne se produit que pour les tables bidirectionnelles. 

Ces enregistrements sont maintenant déplacés vers la page « Enregistrements de synchronisation ignorés », que vous ouvrez à partir de la page Configuration de la connexion Microsoft Dynamics dans Business Central. Vous pouvez y spécifier les modifications à conserver, puis synchroniser à nouveau les enregistrements.

## <a name="remove-couplings-between-records"></a>Supprimer les couplages entre les enregistrements
Lorsque quelque chose ne va pas dans votre intégration et que vous devez découpler des enregistrements pour arrêter de les synchroniser, vous pouvez le faire pour un ou plusieurs enregistrements à la fois. Vous pouvez découpler un ou plusieurs enregistrements des pages de liste ou sur la page **Erreurs de synchronisation de données couplées** en choisissant une ou plusieurs lignes et en choisissant **Supprimer le couplage**. Vous pouvez également supprimer tous les couplages pour un ou plusieurs mappages de table sur la page **Mappages de table d’intégration**. 

## <a name="see-also"></a>Voir aussi
[Intégration à Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuration des comptes d’utilisateur pour intégration à Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)  
[Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]