---
title: Faites bénéficier à vos clients de l'expérience de comptable Dynamics 365 | Microsoft Docs
description: Découvrez comment ajouter les clients existants à l'Accountant Hub pour Dynamics 365.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 95a4153c56693d8bdd28980f1acff14b917a9488
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300082"
---
# <a name="add-clients-to-your-dashboard-in-include-d365acc_longincludesd365acc_long_mdmd"></a>Ajouter des clients à votre tableau de bord dans [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Vous pouvez ajouter un client à l'aide de la page **Clients**, que vous pouvez ouvrir en cliquant sur l'action **Gérer les clients** dans le ruban. Il suffit de sélectionner **Nouveau**, puis de renseigner les champs.  

> [!div class="mx-imgBorder"]
> ![Ajouter un client](./media/accountant-add-client/manage-client.png)

Les données de la fiche de chaque client sont spécifiées par vous, et vous pouvez les modifier selon vos besoins. Toutefois, le champ **URL client** est indispensable, car il vous permet d'accéder au [!INCLUDE [d365fin](includes/d365fin_md.md)] de chaque client. Utilisez l'action **Valider l'URL client** dans le ruban pour vérifier que vous avez saisi le bon lien. L'URL que vous devez saisir pointe vers l'instance [!INCLUDE [d365fin](includes/d365fin_md.md)] du client et inclut son adresse de domaine. Par exemple, s'il a spécifié un domaine tel que MyBusiness.com, le lien vers son instance [!INCLUDE [d365fin](includes/d365fin_md.md)] est *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Avant la mise à jour de mai 2018, l'URL spécifiée avait un format différent avec le nom de la société du client au début. Dans la version actuelle de [!INCLUDE [d365fin](includes/d365fin_md.md)], le format est ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, où ```clientdomain``` représente le domaine de votre client.  

L'URL du client est ensuite utilisée lorsque vous choisissez l'option de menu **Atteindre société** dans le tableau de bord [!INCLUDE [d365acc](includes/d365acc_md.md)].  

### <a name="get-invited-to-a-clients-include-d365fin_longincludesd365fin_long_mdmd"></a>Être invité dans l'instance [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] d'un client
Une société qui utilise [!INCLUDE [d365fin](includes/d365fin_md.md)] peut vous inviter dans [!INCLUDE [d365fin](includes/d365fin_md.md)] comme comptable externe. Pour être invité, vous devez lui communiquer l'adresse électronique que vous utilisez avec [!INCLUDE [d365acc](includes/d365acc_md.md)], par exemple <em>moi@accountant.com</em>. L'administrateur de votre client peut ensuite vous ajouter à son système en exécutant l'Assistant **Inviter un comptable externe**.  

Vous recevrez ensuite un e-mail du client avec des liens vers [!INCLUDE [d365fin](includes/d365fin_md.md)]. Le premier lien est une invitation pour obtenir l'accès à la société. Ouvrez le lien et acceptez les étapes qui vous ajoutent au [!INCLUDE [d365fin](includes/d365fin_md.md)] de votre client. Le second lien vous permet d'ajouter ce client à votre tableau de bord dans [!INCLUDE [d365acc](includes/d365acc_md.md)] comme décrit ci-dessus.  

Lorsque vous avez accepté l'invitation, vous êtes connecté et vous pouvez accéder aux données financières du client sur le tableau de bord **Comptable**. Pour plus d'informations, voir [Expériences de comptable dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Voir aussi
[Mise en route avec [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Dépannage de [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  
