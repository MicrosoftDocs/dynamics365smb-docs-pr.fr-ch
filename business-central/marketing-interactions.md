---
title: Gérer les interactions avec vos contacts| Microsoft Docs
description: Vous pouvez gérer tous les types de communication ou d’interactions entre votre société et vos contacts. Par exemple, une communication par lettre, par téléphone, lors de réunions, etc.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 854970fc2d47110375cf905236df19c90db27e33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914054"
---
# <a name="record-interactions-with-contacts"></a>Enregistrer les interactions avec les contacts
La configuration de votre application pour enregistrer les interactions est constituée des tâches suivantes :

* Configuration de modèles interaction  
* Création d’interactions sur les contacts ou les segments  
* Affichage et gestion des interactions enregistrées  

##  <a name="setting-up-interaction-templates"></a>Configuration de modèles interaction
Pour pouvoir créer et enregistrer des interactions, vous devez configurer des modèles interaction. Lorsque vous créez des interactions, vous devez spécifier les modèles sur lesquels elles sont basées. Un modèle interaction est un prototype qui définit les caractéristiques de base d’une interaction.
Vous pouvez configurer un modèle interaction sur la page **Modèles interaction** .

Une fois les données relatives au modèle interaction saisies, vous pouvez créer un document joint, par exemple, un document Microsoft Word. Répétez les étapes pour chaque modèle interaction à configurer.  

## <a name="creating-interactions"></a>Création d’interactions
Il existe deux méthodes d’enregistrement des interactions :

* Créez manuellement des interactions liées à un contact unique ou à un segment. Pour plus d’informations, reportez-vous à [Créer des interactions sur les contacts et les segments](marketing-how-create-interactions.md).  
* Vous pouvez enregistrer automatiquement les interactions lorsque vous effectuez des opérations dans l’application, telles que l’impression d’une facture ou d’un devis. Pour plus d’informations, reportez-vous à [Enregistrer automatiquement les interactions avec les contacts](marketing-auto-record-interactions.md).

## <a name="viewing-and-managing-recorded-interactions"></a>Affichage et gestion des interactions enregistrées
Sur la page **Écritures journal interaction** , vous pouvez afficher toutes les interactions enregistrées qui n’ont pas été supprimées. Vous pouvez ouvrir cette page de plusieurs façons :

* À l’aide de l’icône **Page ou état pour la recherche** pour effectuer des recherches sur **Écritures journal interaction** .
* En sélectionnant l’action **Écritures journal interaction** sur un contact ou un segment.
  La page **Écriture journal interaction** répertorie les interactions que vous créez manuellement et celles que l’application enregistre automatiquement.

Vous pouvez effectuer les actions suivantes sur cette page :

* Afficher le statut des interactions.
* Marquer les interactions comme annulées.

Vous pouvez supprimer les écritures journal interaction ayant été annulées. Pour supprimer des écritures journal interaction, sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les écritures journal interaction annulées** , puis sélectionnez le lien associé et renseignez les informations.

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Utilisation de Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]