---
title: Configurer et publier les services Web KPI pour les tableaux d’analyse | Microsoft Docs
description: Cette rubrique décrit comment afficher les données KPI basées sur des tableaux d’analyse spécifiques.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 54b0abc6b4c4834fd57cdc71d3d3ece024e3395c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913853"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Configuration et publication des services Web KPI sur la base de tableaux d’analyse
La page **Tableau d’analyse - Paramètres du service web KPI** vous permet de configurer la manière dont les informations KPI du tableau d’analyse sont affichées et sur quels tableaux d’analyse spécifiques baser les KPI. Lorsque vous sélectionnez le bouton **Publier le service Web** , les informations KPI du tableau d’analyse spécifiées sont ajoutées à la liste des services Web publiés sur la page **Services web** .  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Configuration et de publication d’un service Web KPI sur la base de tableaux d’analyse  
1.  Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Tableau d’analyse - Paramètres du service web KPI** , puis sélectionnez le lien associé.  
2.  Sous le raccourci **Général** , renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Début valeurs prévues**|Spécifiez la date à laquelle les valeurs prévues sont affichées sur le graphique KPI du tableau d’analyse.<br /><br /> Les valeurs prévues sont récupérées à partir du budget en comptabilité que vous sélectionnez dans le champ **Nom budget comptable** . **Note ::** pour obtenir des KPI qui affichent les chiffres prévus après une certaine date et les chiffres réels avant cette date, vous pouvez modifier le champ **Début période validation** sur la page **Paramètres comptabilité** . Pour plus d’informations, voir Début période validation.|  
    |**Nom budget comptable**|Spécifiez le nom du budget en comptabilité qui fournit les valeurs prévues au service Web KPI du tableau d’analyse.|  
    |**Période**|Indiquez la période sur laquelle le service Web KPI du tableau d’analyse se base.|  
    |**Afficher par**|Indiquez l’intervalle de temps dans lequel le KPI du tableau d’analyse est affiché.|  
    |**Nom du service web**|Indiquez le nom du service Web KPI du tableau d’analyse.<br /><br /> Ce nom est affiché dans le champ **Nom de service** sur la page **Services web** .|  

    Spécifiez un ou plusieurs tableaux d’analyse que vous souhaitez publier en tant que service Web KPI en fonction du paramétrage que vous avez fait dans la table précédente.  

3.  Sous le raccourci **Tableaux d’analyse** , renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Nom tableau d’analyse**|Permet d’indiquer le tableau d’analyse sur lequel le service Web KPI se base.|  
    |**Description tableau analyse**|Permet d’indiquer la désignation du tableau d’analyse sur lequel le service Web KPI se base.|  

4.  Répétez l’étape 3 pour tous les tableaux d’analyse sur lesquels vous souhaitez baser le service Web KPI du tableau d’analyse.  
5.  Pour visualiser ou modifier le tableau d’analyse sélectionné, sur le raccourci **Tableau d’analyse** , choisissez l’action **Modifier tableau d’analyse** .  
6.  Pour afficher les informations KPI du tableau d’analyse que vous avez définies, choisissez l’action **Tableau d’analyse - Paramètres du service web KPI** .  
7.  Pour publier le service Web KPI du tableau d’analyse, choisissez l’action **Publier le service web** . Le service Web est ajouté à la liste des services Web publiés sur la page **Web Services** .  

> [!NOTE]  
>  V-us pouvez également publier le service Web KPI en pointant vers l’objet de page **Tableau d’analyse-Paramètres du service web KPI** à partir de la page **Services web** . Pour plus d’informations, voir [Publication d’un service Web](across-how-publish-web-service.md).  

## <a name="see-also"></a>Voir aussi  
[Veille économique](bi.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
