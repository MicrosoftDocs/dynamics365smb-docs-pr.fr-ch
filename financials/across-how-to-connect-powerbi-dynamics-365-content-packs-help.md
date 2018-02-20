---
title: "Comment connecter Power BI à Finance and Operations, Business edition | Microsoft Docs"
description: "Il est facile d'obtenir des informations exploitables, de la veille économique et des KPI de vos données Finance and Operations, Business edition grâce à Power BI et aux packs de contenu Finance and Operations, Business edition"
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 01/29/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4a1498e634046e54bdb9a5793731e44808c2f1eb
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a>Connexion de Power BI aux packs de contenu Finance and Operations, Business edition
Il est facile d'obtenir des informations exploitables de vos données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft grâce à Power BI et aux packs de contenu [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft. Power BI extrait vos données, puis génère un tableau de bord prêt à l'emploi et des états basés sur ces données.

> [!NOTE]  
>  Remarque : vous devez disposer d'un compte valide avec Dynamics 365 et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  Les packs de contenu Power BI nécessitent des autorisations vers les tables d'où sont extraites les données. Vous trouverez plus d'informations sur les besoins ci-dessous.  

## <a name="how-to-connect"></a>Pour vous connecter
1. Sélectionnez **Extraire les données** en bas du volet de navigation gauche.  
![Naviguer pour obtenir des données](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. Dans la zone **Services**, sélectionnez **Extraire**. Une fenêtre s'ouvre alors, elle contient **AppSource** et **Applications pour applications Power BI**.  
![Choisir des packs de contenu à partir des services en ligne](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Sélectionnez **Applications** dans l'onglet **Applications pour applications Power BI** et choisissez le pack de contenu **Microsoft Dynamics 365 for Finance and Operations** à utiliser, puis cliquez sur **Obtenir maintenant**.  
![Sélectionner Dynamics 365 for Finance and Operations, Business edition et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Quand on vous le demande, indiquez le nom de *votre société* dans [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Il ne s'agit pas du nom complet.  
![Sélectionner Dynamics 365 for Finance and Operations, Business edition et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Une fois connecté, un tableau de bord, un état et un ensemble de données sont automatiquement chargés dans votre espace de travail Power BI. Une fois terminé, les mosaïques sont mises à jour avec les données de votre compte.
![Sélectionner Dynamics 365 for Finance and Operations, Business edition et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Et ensuite ?

- Cliquez sur [poser une question dans la zone Q&R](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) en haut du tableau de bord.  
- [Modifiez les mosaïques](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) du tableau de bord.  
- [Sélectionnez une mosaïque](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) pour ouvrir l'état sous-jacent.  
- Il est prévu que votre ensemble de données soit actualisé quotidiennement, vous pouvez toutefois modifier la planification de l'actualisation ou essayer de l'actualiser à la demande en sélectionnant **Actualiser maintenant**.

## <a name="system-requirements"></a>Configuration système requise
Pour importer les données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] dans Power BI, vous devez disposer des autorisations sur les services Web utilisés pour récupérer les données. Les services Web obligatoires pour chaque pack de contenu incluent :

**Microsoft Dynamics 365 for Finance and Operations – CRM**
- SalesOpportunities

**Microsoft Dynamics 365 for Finance and Operations – Sales**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard

**Microsoft Dynamics 365 for Finance and Operations – Finance**
- PowerBIFinance

**Microsoft Dynamics 365 for Finance and Operations – Jobs**
- Liste des projets
- Lignes planning projet
- Lignes tâche projet

## <a name="web-services"></a>Services web
Pour trouver facilement les services Web, il suffit de les chercher dans [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Dans la liste, assurez-vous que la case Publier est cochée pour les services Web répertoriés ci-dessus.

## <a name="troubleshooting"></a>Incident
Le tableau de bord Power BI s'appuie sur les services Web publiés qui sont répertoriés ci-dessus. Il affichera les données de la société de démonstration ou de votre propre société si vous importez les données de votre solution financière actuelle. Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.

### <a name="incorrect-company-name"></a>Nom de société incorrect  
Une erreur commune consiste à entrer le nom complet de la société au lieu du nom de la société. Pour trouver le nom de la société, cherchez dans **Sociétés**. Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre société.

### <a name="incorrect-user-name-and-password"></a>Nom d'utilisateur et mot de passe incorrects  
Le nom d'utilisateur et le mot de passe utilisés pour la connexion sont identiques à ceux utilisés pour la connexion à votre compte Microsoft Office 365.  

Les packs de contenu nécessitent également que vous ayez un compte [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft.  Une fois les informations d'identification saisies, tous les abonnés [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft accessibles seront détectés automatiquement.  Si vous n'avez pas de compte [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft sous licence ou d'essai, vous recevrez un message d'erreur.

## <a name="see-also"></a>Voir aussi
[Mise en route de Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Concepts de base](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Veille économique](bi.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importation des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
[Configuration de la génération d'états [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI](across-how-use-financials-data-source-powerbi.md)  

