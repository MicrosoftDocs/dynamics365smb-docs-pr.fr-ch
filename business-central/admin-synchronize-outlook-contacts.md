---
title: Partager des contacts entre Business Central et Outlook| Microsoft Docs
description: Ce service a une intégration étroite avec Office 365, ce qui vous permet de partager des contacts entre Outlook et Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f7cf42a003e68d68bf29a3623e9573f6e33eed4b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186635"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synchroniser les contacts de Business Central avec les contacts de Microsoft Outlook
Vous pouvez voir les mêmes contacts dans [!INCLUDE[d365fin](includes/d365fin_md.md)] que dans Outlook si vous configurez la synchronisation des contacts. Par exemple, si vous êtes un vendeur, vous pouvez effectuer une partie de votre travail dans Outlook et l'autre partie dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si les contacts sont les mêmes dans les deux emplacements, votre travail est plus simple.  

Un dossier dédié dans Outlook facilite la recherche des contacts, et vous pouvez définir un filtre pour synchroniser uniquement les contacts de [!INCLUDE[d365fin](includes/d365fin_md.md)] que vous souhaitez voir dans Outlook. Une fois que la synchronisation des contacts est configurée, vous pouvez démarrer manuellement la synchronisation ou configurer la synchronisation automatique des contacts à des intervalles planifiés.  

## <a name="set-up-synchronization"></a>Configurer la synchronisation
Vous configurez le mode de synchronisation des contacts avec Outlook sur la page **Configuration de la synchronisation Exchange** de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Au préalable, votre profil utilisateur dans [!INCLUDE[d365fin](includes/d365fin_md.md)] doit spécifier votre compte de messagerie Office 365. Vous pouvez le vérifier dans la section **Office 365 Authentification** de votre profil utilisateur dans la liste **Utilisateurs**.  

Ensuite, sur la page **Configuration de la synchronisation Exchange**, vous pouvez valider que la connexion à Exchange fonctionne avant de configurer la synchronisation des contacts. Ouvrez la page **Paramètres synch. contacts** et démarrez la synchronisation. Appliquez éventuellement un filtre pour définir les contacts à synchroniser entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Outlook. Par exemple, vous pouvez définir un filtre par nom, type, société ou autre. Vous pouvez également modifier le nom par défaut du dossier avec lequel les contacts seront synchronisés dans Outlook. Le nom par défaut est *Business Central*.  

Une fois que cette synchronisation a été configurée, les modifications apportées au contact dans Outlook ou dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sont synchronisées avec l'autre.  

Chacun de vos collègues peut également configurer sa propre synchronisation Exchange et définir son propre filtre de synchronisation des contacts.  

## <a name="synchronize-contacts"></a>Synchroniser les contacts
Si vous avez l'habitude d'utiliser les contacts dans [!INCLUDE[d365fin](includes/d365fin_md.md)], il vous sera facile de démarrer manuellement la synchronisation au moment qui vous convient à partir de la liste **Contacts**. Choisissez simplement l'action **Synchronisation avec Office 365** et décidez si vous souhaitez modifier le filtre que vous avez défini. Lorsque vous cliquez sur le bouton OK, la synchronisation démarre immédiatement, et les dernières modifications sont appliquées à vos contacts dans Outlook.  

Dans la liste **Contacts**, vous pouvez synchroniser les contacts de deux manières :

* **Synchronisation avec Office 365**

  Cette action synchronise toutes les modifications de Office 365 vers [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis la précédente synchronisation, en fonction de la dernière date de modification. Les nouveaux contacts dans Office 365 sont également synchronisés dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Cette procédure est généralement plus rapide qu'une synchronisation complète.  

* **Synchronisation complète avec Office 365**

  Cette action synchronise tous les contacts dans les deux directions, indépendamment de la dernière date de synchronisation et de la dernière date de modification.  

Dans les deux cas, les contacts sont uniquement synchronisés à partir d'Outlook si les champs obligatoires sont renseignés. Les champs obligatoires à synchroniser avec Office 365 sont **Nom**, **Adresse e-mail** et leur type doit être Personne. [!INCLUDE[d365fin](includes/d365fin_md.md)] est le maître des informations de contact, les informations de contact [!INCLUDE[d365fin](includes/d365fin_md.md)] seront donc enregistrées en cas de doublons.  

Dans Outlook, les contacts de [!INCLUDE[d365fin](includes/d365fin_md.md)] sont affichés dans un dossier sous **Autre contacts** dans la vue **Personnes**. Si vous n'êtes pas familiarisé avec la vue Personne dans Outlook, vous pouvez y accéder à partir des options de navigation dans le coin inférieur gauche d'Outlook.  

## <a name="see-also"></a>Voir aussi
[Mise en route](product-get-started.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation des contacts (personnes) dans Outlook sur le Web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
