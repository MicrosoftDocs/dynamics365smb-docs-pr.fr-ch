---
title: Partager des contacts entre Business Central et Outlook
description: Ce service a une intégration étroite avec Microsoft 365, ce qui vous permet de partager des contacts entre Outlook et Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.search.form: 6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 12ce99a79f465543ecc314b5042e70b6802f86ec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142434"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synchroniser les contacts de Business Central avec les contacts de Microsoft Outlook

Vous pouvez voir les mêmes contacts dans [!INCLUDE[prod_short](includes/prod_short.md)] que dans Outlook si vous configurez la synchronisation des contacts. Par exemple, si vous êtes un vendeur, vous pouvez effectuer une partie de votre travail dans Outlook et l’autre partie dans [!INCLUDE[prod_short](includes/prod_short.md)]. Si les contacts sont les mêmes dans les deux emplacements, votre travail est plus simple.  

Un dossier dédié dans Outlook facilite la recherche des contacts, et vous pouvez définir un filtre pour synchroniser uniquement les contacts de [!INCLUDE[prod_short](includes/prod_short.md)] que vous souhaitez voir dans Outlook. Une fois que la synchronisation des contacts est configurée, vous pouvez démarrer manuellement la synchronisation ou configurer la synchronisation automatique des contacts à des intervalles planifiés.  

## <a name="set-up-synchronization"></a>Configurer la synchronisation
Vous configurez le mode de synchronisation des contacts avec Outlook sur la page **Configuration de la synchronisation Exchange** de [!INCLUDE[prod_short](includes/prod_short.md)]. Au préalable, votre profil utilisateur dans [!INCLUDE[prod_short](includes/prod_short.md)] doit spécifier votre compte de messagerie Microsoft 365. Vous pouvez vérifier cela dans la section **Authentification Microsoft 365** de votre profil utilisateur dans la liste **Utilisateurs**.  

Ensuite, sur la page **Configuration de la synchronisation Exchange**, vous pouvez valider que la connexion à Exchange fonctionne avant de configurer la synchronisation des contacts. Ouvrez la page **Paramètres synch. contacts** et démarrez la synchronisation. Appliquez éventuellement un filtre pour définir les contacts à synchroniser entre [!INCLUDE[prod_short](includes/prod_short.md)] et Outlook. Par exemple, vous pouvez définir un filtre par nom, type, société ou autre. Vous pouvez également modifier le nom par défaut du dossier avec lequel les contacts seront synchronisés dans Outlook. Le nom par défaut est *Business Central*.  

Une fois que cette synchronisation a été configurée, les modifications apportées au contact dans Outlook ou dans [!INCLUDE[prod_short](includes/prod_short.md)] sont synchronisées avec l’autre.  

Chacun de vos collègues peut également configurer sa propre synchronisation Exchange et définir son propre filtre de synchronisation des contacts.  

## <a name="synchronize-contacts"></a>Synchroniser les contacts
Si vous avez l’habitude d’utiliser les contacts dans [!INCLUDE[prod_short](includes/prod_short.md)], il vous sera facile de démarrer manuellement la synchronisation au moment qui vous convient à partir de la liste **Contacts**. Choisissez simplement l’action **Synchronisation avec Microsoft 365** et décidez si vous souhaitez modifier le filtre que vous avez défini. Lorsque vous cliquez sur le bouton OK, la synchronisation démarre immédiatement, et les dernières modifications sont appliquées à vos contacts dans Outlook.  

Dans la liste **Contacts**, vous pouvez synchroniser les contacts de deux manières :

* **Synchronisation avec Microsoft 365**

  Cette action synchronise toutes les modifications de Microsoft 365 vers [!INCLUDE[prod_short](includes/prod_short.md)] depuis la précédente synchronisation, en fonction de la dernière date de modification. Les nouveaux contacts dans Microsoft 365 sont également synchronisés dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cette procédure est généralement plus rapide qu'une synchronisation complète.  

* **Synchronisation complète avec Microsoft 365**

  Cette action synchronise tous les contacts dans les deux directions, indépendamment de la dernière date de synchronisation et de la dernière date de modification.  

Dans les deux cas, les contacts sont uniquement synchronisés à partir d'Outlook si les champs obligatoires sont renseignés. Les champs obligatoires à synchroniser avec Microsoft 365 sont **Nom**, **Adresse e-mail** et leur type doit être Personne. [!INCLUDE[prod_short](includes/prod_short.md)] est le maître des informations de contact, les informations de contact [!INCLUDE[prod_short](includes/prod_short.md)] seront donc enregistrées en cas de doublons.  

Dans Outlook, les contacts de [!INCLUDE[prod_short](includes/prod_short.md)] sont affichés dans un dossier sous **Autre contacts** dans la vue **Personnes**. Si vous n’êtes pas familiarisé avec la vue Personne dans Outlook, vous pouvez y accéder à partir des options de navigation dans le coin inférieur gauche d’Outlook.  

## <a name="see-also"></a>Voir aussi
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utilisation des contacts (personnes) dans Outlook sur le Web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]