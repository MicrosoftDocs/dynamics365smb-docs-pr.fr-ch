---
title: "Expérience de comptable avec Dynamics 365 | Microsoft Docs"
description: "En savoir plus sur Accountant Hub pour Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/10/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 591ca492802166610f00ad5be09badd719fdb64a
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="get-started-with-included365acclongincludesd365acclongmdmd"></a>Mise en route avec [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

Chaque entreprise doit tenir ses comptes et valider sa comptabilité. Certaines sociétés utilisent un comptable externe, et d'autres ont un comptable dans le personnel. Si vous êtes un comptable avec plusieurs clients, vous pouvez utiliser [!INCLUDE[d365acc](includes/d365acc_md.md)] comme tableau de bord pour un meilleur aperçu de vos clients.  

Vous pouvez accéder à [!INCLUDE[d365acc](includes/d365acc_md.md)] en vous connectant à partir de [Dynamics 365 — Accountant Hub sur Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]  
>  Lorsque vous vous connectez à [!INCLUDE[d365acc](includes/d365acc_md.md)], vous devez indiquer votre adresse e-mail professionnelle, par exemple *me@accountant.com*. Il est recommandé d'utiliser la même adresse e-mail lorsque vous travaillez dans les versions clients de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], de sorte que vous puissiez facilement basculer entre les clients. L'adresse électronique du comptable doit être une adresse professionnelle basée sur Active Directory.

## <a name="working-with-individual-clients"></a>Utilisation de clients individuels
Le tableau de bord affiche les informations les plus importantes sur chaque client.  
![Accountant Hub](./media/accountant-get-started/accountant-dashboard-tasks.png)

La colonne **Nom client** affiche les noms des clients, et la colonne **Nom de la société** répertorie toutes les sociétés si le client a plusieurs sociétés dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. Il existe aussi des champs permettant d'afficher les tâches qui vous sont affectées dans la société de votre client, y compris les tâches échues.  

Vous pouvez personnaliser le tableau de bord pour afficher les points de données que vous souhaitez voir en ajoutant ou supprimant des colonnes. Par exemple, vous souhaitez peut-être visualiser les taxes dues, le nombre de documents vente ouvertes chaque client a, ou le nombre de factures achat dues la semaine suivante. Vous pouvez configurer la vue à votre convenance. Si vous avez de nombreux clients, vous pouvez utiliser des filtres pour trier votre affichage.  

À côté du nom du client, les points de suspension (...) font apparaître un menu court :

-   Actualiser la société actuelle et obtenir des données récentes pour le client  
-   Accédez au [!INCLUDE[d365fin](includes/d365fin_md.md)] du client  
-   Sélectionner d'autres clients  

De même, vous pouvez utiliser le menu déroulant **Résumé client** pour actualiser toutes les sociétés, par exemple.  

> [!TIP]  
>  Pour accéder au [!INCLUDE[d365fin](includes/d365fin_md.md)] d'un client, choisissez l'élément de menu **Accéder au client**. Vous êtes connecté automatiquement.

## <a name="company-details"></a>Aperçu société
Vous pouvez afficher plus d'informations sur les données de vos clients en sélectionnant le nom de la société qui vous intéresse. Ceci ouvre le volet **Aperçu société**, où vous pouvez visualiser des informations complémentaires, telles que les éléments suivants :  

* Soldes des comptes de trésorerie  
* Prévision de trésorerie  
* Factures achat échues  
* Factures vente en retard  

![Détails de la société du client dans le tableau de bord du comptable](./media/accountant-get-started/accountant-company-details.png)

Techniquement, vous êtes maintenant connecté au serveur [!INCLUDE[d365fin](includes/d365fin_md.md)] de votre client, et les données affichées sont des données en temps réel. Si vous souhaitez examiner plus en détail les données, par exemple une facture achat échue, sélectionnez le lien pour être redirigé vers la société du client.  

> [!TIP]  
>  Vous pouvez lancer les classeurs Excel prédéfinis dans l'onglet **États** du ruban. Ces classeurs Excel sont conçus comme des états et rapports financiers prêts à être imprimés, mais vous pouvez également les modifier selon vos besoins. Pour plus d'informations, voir [Analyse des états financiers dans Microsoft Excel](/dynamics365/financials/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) dans l'Aide de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Sinon, fermez le volet des détails et passez au client suivant.  

## <a name="assigned-tasks"></a>Tâches affectées
Dans le [!INCLUDE[d365fin](includes/d365fin_md.md)] de votre client, vous pouvez affecter des tâches à vous-même et à d'autres utilisateurs, et d'autres utilisateurs peuvent vous affecter des tâches. Votre tableau de bord dans [!INCLUDE[d365acc](includes/d365acc_md.md)] vous fournit un aperçu des tâches affectées à chaque client, et vous pouvez également accéder à une liste de toutes les tâches affectées en choisissant **Mes tâches utilisateur** dans la navigation de gauche.  

Dans la société du client, vous disposez également de piles qui appellent les tâches qui vous sont affectées dans ce client spécifique.

![Tâches affectées au comptable à la société du client](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Mes tâches utilisateur
La liste **Mes tâches utilisateur** dans [!INCLUDE[d365acc](includes/d365acc_md.md)] vous permet de planifier votre journée en affichant plus d'informations sur les tâches qui vous sont affectées chez tous vos clients.  

![Liste des tâches qui m'ont été affectées en tant que comptable externe](./media/accountant-get-started/accountant-tasklist.png)

Vous pouvez effectuer un tri par date d'échéance, par exemple, ou tout autre type de données vous permettant de planifier votre journée. Par défaut, la liste affiche toutes les tâches qui vous sont affectées, mais vous pouvez définir des filtres pour afficher uniquement les tâches qui sont marquées comme ayant une priorité élevée, par exemple.

Pour sélectionner une tâche, il suffit de cliquer dessus dans la liste des tâches utilisateur en attente. Dans le ruban, le lien **Atteindre l'élément de tâche** ouvre la fenêtre dans laquelle vous pouvez effectuer le travail.  

Lorsque vous avez terminé une tâche, marquez-la simplement comme terminée.  

## <a name="see-also"></a>Voir aussi
[Ajouter des clients à votre tableau de bord dans [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
[Bienvenue dans [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Analyse des états financiers dans Microsoft Excel](/dynamics365/financials/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)   
[Expériences de comptable dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/financials/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365 — Accountant Hub sur Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

