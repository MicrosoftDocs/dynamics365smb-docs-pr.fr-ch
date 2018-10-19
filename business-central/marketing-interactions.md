---
title: "Gérer les interactions avec vos contacts| Microsoft Docs"
description: "Vous pouvez gérer tous les types de communication ou d'interactions entre votre société et vos contacts. Par exemple, une communication par lettre, par téléphone, lors de réunions, etc."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6fb3c1a19626c4cfa078f030a387e314ae2e0480
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="managing-interactions-with-contacts"></a>Gestion des interactions avec les contacts
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les interactions désignent tous les types de communication entre votre société et vos contacts. Par exemple, les communications peuvent s'effectuer par lettre, par e-mail, par télécopie,par téléphone, et ainsi de suite.

Le module de gestion des relations vous permet d'enregistrer toutes les interactions vente et marketing avec vos contacts afin d'effectuer le suivi des efforts mis en œuvre, et d'améliorer vos futures relations commerciales. La configuration de votre application pour enregistrer les interactions est constituée des tâches suivantes :

* Configuration de modèles interaction  
* Création d'interactions sur les contacts ou les segments  
* Affichage et gestion des interactions enregistrées  

##  <a name="setting-up-interaction-templates"></a>Configuration de modèles interaction
Pour pouvoir créer et enregistrer des interactions, vous devez configurer des modèles interaction. Lorsque vous créez des interactions, vous devez spécifier les modèles sur lesquels elles sont basées. Un modèle interaction est un prototype qui définit les caractéristiques de base d'une interaction.
Vous pouvez configurer un modèle interaction dans la fenêtre **Modèles interaction**.

Une fois les données relatives au modèle interaction saisies, vous pouvez créer un document joint, par exemple un document Microsoft Word. Répétez les étapes pour chaque modèle interaction à configurer.  

## <a name="creating-interactions"></a>Création d'interactions
Il existe deux méthodes d'enregistrement des interactions :

* Créez manuellement des interactions liées à un contact unique ou à un segment. Pour plus d'informations, reportez-vous à [Créer des interactions sur les contacts et les segments](marketing-how-create-interactions.md).  
* Vous pouvez enregistrer automatiquement les interactions lorsque vous effectuez des opérations dans l'application, telles que l'impression d'une facture ou d'un devis. Pour plus d'informations, reportez-vous à [Enregistrer automatiquement les interactions avec les contacts](marketing-auto-record-interactions.md).

## <a name="viewing-and-managing-recorded-interactions"></a>Affichage et gestion des interactions enregistrées
Dans la fenêtre **Écritures journal interaction**, vous pouvez afficher toutes les interactions enregistrées qui n'ont pas été supprimées. Vous pouvez ouvrir cette fenêtre de plusieurs façons :

* À l'aide de l'icône **Page ou état pour la recherche** pour effectuer des recherches sur **Écritures journal interaction**.
* En sélectionnant l'action **Écritures journal interaction** sur un contact ou un segment.
  La fenêtre **Écriture journal interaction** répertorie les interactions que vous créez manuellement et celles que l'application enregistre automatiquement.

Cette fenêtre vous permet d'effectuer les opérations suivantes :

* Afficher le statut des interactions.
* Marquer les interactions comme annulées.

Vous pouvez supprimer les écritures journal interaction ayant été annulées. Pour supprimer des écritures journal interaction, sélectionnez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer les écritures journal interaction annulées**, puis sélectionnez le lien connexes et renseignez les informations.

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Gestion des opportunités de ventes](marketing-manage-sales-opportunities.md)  
[Utilisation de Business Central](ui-work-product.md)  

