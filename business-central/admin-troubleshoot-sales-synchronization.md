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
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 82b5f3ec52be27c4fbe60a6a63a0cfc5f6f1bd7c
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196558"
---
# <a name="troubleshooting-synchronization-errors"></a>Résolution des erreurs de synchronisation
Il y a beaucoup de pièces mobiles impliquées dans l'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] avec Common Data Service, et parfois les choses ne se passent pas bien. Cette rubrique répertorie certaines des erreurs types qui se produisent et donne des indications sur la manière de les résoudre.

Les erreurs se produisent souvent à cause de quelque chose qu'un utilisateur a fait pour coupler des enregistrements ou parce que la configuration de l'intégration est fausse. Pour les erreurs liées aux enregistrements couplés, les utilisateurs peuvent les résoudre eux-mêmes. Ces erreurs sont causées par des actions telles que la suppression d'un enregistrement dans l'une des applications métier mais pas les deux, puis la synchronisation. Pour plus d'informations, voir [Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Exemple :
Cette vidéo montre un exemple de dépannage des erreurs survenues lors de la synchronisation avec Sales. Le processus sera le même pour toutes les intégrations. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Les erreurs liées à la configuration de l'intégration nécessitent généralement l'attention de l'administrateur. Vous pouvez voir ces erreurs sur la page **Erreurs de synchronisation d'intégration**. Voici des exemples de problèmes classiques :  
  
* Les autorisations et les rôles attribués aux utilisateurs ne sont pas corrects.  
* Le compte administrateur a été spécifié en tant qu'utilisateur d'intégration.  
* Le mot de passe de l'utilisateur d'intégration est défini pour nécessiter une modification lorsque l'utilisateur se connecte.  
* Les taux de change pour les devises ne sont pas spécifiés dans l'une ou l'autre application.  
  
Vous devez résoudre manuellement les erreurs, mais la page vous aide de plusieurs manières. Par exemple :  

* Les champs **Source** et **Destination** peuvent contenir des liens vers l'enregistrement où l'erreur a été trouvée. Cliquez sur le lien pour ouvrir l'enregistrement et recherchez l'erreur.  
* Les actions **Supprimer les écritures ultérieures à 7 jours** et **Supprimer toutes les écritures** vont nettoyer la liste. En règle générale, vous utilisez ces actions après avoir résolu la cause d'une erreur affectant de nombreux enregistrements. Faites attention, cependant. Ces actions peuvent supprimer des erreurs toujours pertinentes.

Parfois, les horodatages sur les enregistrements peuvent provoquer des conflits. La table « Enregistrement intégration CDS » conserve les horodatages « Dernière synch. modifiée le » et « Dernière synch. CDS modifiée le » pour la dernière intégration effectuée dans les deux directions pour un enregistrement. Ces horodatages sont comparés aux horodatages sur les enregistrements Business Central et Sales. Dans Business Central, l'horodatage se trouve dans la table Enregistrement intégration.

Vous pouvez filtrer les enregistrements à synchroniser en comparant les horodatages des enregistrements dans les champs « Filtre synch. modifiée le » et « Fltr. synch. table int. mod. le » de la table « Mappage de table d'intégration ».

Le message d'erreur de conflit « Impossible de mettre à jour l'enregistrement client, car sa date de dernière modification est postérieure à celle de l'enregistrement de compte » ou « Impossible de mettre à jour l'enregistrement de compte, car sa date de dernière modification est postérieure à celle de l'enregistrement client » peut apparaître si un enregistrement a un horodatage supérieur au champ « Filtre synch. modifiée le » du Mappage de table d'intégration, mais s'il n'est pas plus récent que l'horodatage de l’enregistrement de l’intégration de Sales. Cela signifie que l'enregistrement source a été synchronisé manuellement, et non par l'entrée de la file d'attente des tâches. 

Le conflit se produit, car l'enregistrement de destination a également été modifié : l'horodatage de l'enregistrement est plus récent que l'horodatage de l'enregistrement de l'intégration de Sales. La vérification de la destination ne se produit que pour les tables bidirectionnelles. 

Ces enregistrements sont maintenant déplacés vers la page « Enregistrements de synchronisation ignorés », que vous ouvrez à partir de la page Configuration de la connexion Microsoft Dynamics dans Business Central. Vous pouvez y spécifier les modifications à conserver, puis synchroniser à nouveau les enregistrements.

## <a name="see-also"></a>Voir aussi
[Intégration à Common Data Service](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuration des comptes d'utilisateur pour intégration à Common Data Service](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)  
[Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md)  
