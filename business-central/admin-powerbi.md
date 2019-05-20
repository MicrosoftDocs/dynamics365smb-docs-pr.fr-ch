---
title: Packs de contenu Business Central et Power BI | Microsoft Docs
description: Il est facile d'obtenir des informations exploitables, de la veille économique et des KPI de vos données Business Central grâce à Power BI et aux packs de contenu Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/26/2019
ms.author: edupont
ms.openlocfilehash: a999a9533aa2dd4e8dcadea04e7838305b34ba5b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247527"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Activation de vos données commerciales pour Power BI
Il est facile d'obtenir des informations exploitables de vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] grâce à Power BI et aux packs de contenu [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI extrait vos données, puis génère un tableau de bord prêt à l'emploi et des états basés sur ces données.  

Vous devez disposer d'un compte valide avec Dynamics 365 et avec Power BI. En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) si vous souhaitez créer vos propres états Power BI. Les packs de contenu Power BI nécessitent des autorisations vers les tables d'où sont extraites les données. Vous trouverez plus d'informations sur les besoins ci-dessous.  

> [!IMPORTANT]
> Les packs de contenu décrits dans cet article sont conçus pour utiliser Azure Active Directory comme mécanisme d'authentification. Si vous utilisez [!INCLUDE [prodshort](includes/prodshort.md)] local et utilisez un autre mécanisme d'authentification, Power BI ne peut pas se connecter à vos données.  

Microsoft a publié les packs de contenu suivants :

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Liste des clients  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finances  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Liste des articles  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Projets  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Liste des projets  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Factures achat  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Ventes  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Liste des commandes vente  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Liste des fournisseurs  

## <a name="using-the-dashboards"></a>Utilisation des tableaux de bord
Chaque pack de contenu contient des états que vous pouvez afficher :

* Sélectionnez un visuel du tableau de bord pour afficher l'un des états sous-jacents.  
* Filtrez l'état ou ajoutez les champs que vous souhaitez contrôler.  
* Épinglez cette vue personnalisée au tableau de bord pour continuer à effectuer le suivi.  
  Vous pouvez actualiser les données manuellement, et vous pouvez configurer un programme d'actualisation. Pour plus d'informations, voir [Configuration d'une actualisation planifiée](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Les packs de contenu sont pré-configurés pour fonctionner avec les données provenant de la société de démonstration que vous obtenez lorsque vous vous connectez à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lorsque vous installez les applications dans Power BI et que vous vous connectez à vos propres données, certains états peuvent ne pas fonctionner, car ils reposent sur des données dont votre société ne dispose pas. Dans ces cas, vous pouvez simplement supprimer ces états de votre tableau de bord.  

> [!NOTE]  
>   Vous pouvez également générer vos propres états et tableaux de bord dans Power BI selon vos données [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Connexion de vos données métier à Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>Pour vous connecter
1. Sélectionnez **Extraire les données** en bas du volet de navigation gauche.  
![Naviguer pour obtenir des données](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Vous pouvez également démarrer depuis [!INCLUDE [prodshort](includes/prodshort.md)]. Dans le Tableau de bord, accédez à **Sélection des états** dans le composant du Tableau de bord Power BI. Sélectionnez **Service** ou **Mon organisation** dans le ruban. Lorsque l'une de ces actions est sélectionnée, vous arrivez dans la galerie Organisation de Power BI ou dans la bibliothèque des services de Power BI, qui sera également filtrée pour afficher uniquement les packs de contenu associés à [!INCLUDE[prodshort](includes/prodshort.md)].

2. Dans la zone **Services**, sélectionnez **Extraire**. Une page s'ouvre alors, elle contient **AppSource** et **Applications pour applications Power BI**.  
![Choisir des packs de contenu à partir des services en ligne](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Sélectionnez **Applications** dans l'onglet **Applications pour applications Power BI** et choisissez le pack de contenu **Microsoft Dynamics 365 Business Central** à utiliser, puis cliquez sur **Obtenir maintenant**.  
![Sélectionnez Dynamics 365 Business Central et sélectionnez Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Quand on vous le demande, indiquez le nom de *votre société* dans [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Il ne s'agit pas du nom complet. Le nom de la société se trouve dans la page Sociétés de votre instance [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].  
![Sélectionnez Dynamics 365 Business Central et sélectionnez Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-business-central-finance.png)
5. Une fois connecté, un tableau de bord, un état et un ensemble de données sont automatiquement chargés dans votre espace de travail Power BI. Une fois terminé, les mosaïques sont mises à jour avec les données de votre société [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].
![Sélectionnez Dynamics 365 Business Central et sélectionnez Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Et ensuite ?

- Cliquez sur [poser une question dans la zone Q&R](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) en haut du tableau de bord.
- [Modifiez les mosaïques](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) du tableau de bord.  
- [Sélectionnez une mosaïque](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) pour ouvrir l'état sous-jacent.  
- Il est prévu que votre ensemble de données soit actualisé quotidiennement, vous pouvez toutefois modifier la planification de l'actualisation ou essayer de l'actualiser à la demande en sélectionnant **Actualiser maintenant**.

## <a name="system-requirements"></a>Configuration système requise
Pour importer les données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] dans Power BI, vous devez disposer des autorisations sur les services Web utilisés pour récupérer les données. Les services Web obligatoires pour chaque pack de contenu incluent :

### <a name="role-center-reports"></a>États du Tableau de bord

**Microsoft Dynamics 365 Business Central – CRM**
- Opportunités ventes
- Modèle Excel Afficher Société
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Modèle Excel Afficher Société
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central – Jobs**
- Liste des projets
- Lignes planning projet
- Lignes tâche projet
- Étiquettes d'état Power BI
- Modèle Excel Afficher Société

**Microsoft Dynamics 365 Business Central - Sales**
- Tableau de bord ventes
- Modèle Excel Afficher Société
- Étiquettes d'état Power BI

### <a name="list-page-reports"></a>États Page de liste

**Microsoft Dynamics 365 Business Central – Customers List**
- Ventes d'articles par client
- Liste des achats d'articles Power BI
- Liste des ventes d'articles Power BI
- Tableau de bord ventes
- Liste des clients Power BI
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Liste des montants Power BI GL
- Montant budgété Power BI GL
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central – Items List**
- Ventes d'articles par client
- Liste des achats d'articles Power BI
- Liste des ventes d'articles Power BI
- Tableau de bord ventes
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central – Jobs List**
- Liste des projets Power BI
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Liste des achats Power BI
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Liste des ventes Power BI
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI


**Microsoft Dynamics 365 Business Central – Vendors List**
- Liste des achats d'articles Power BI
- Liste des ventes d'articles Power BI
- Liste des fournisseurs Power BI
- ExcelTemplateViewCompany
- Étiquettes d'état Power BI

## <a name="web-services"></a>Services web
Pour trouver facilement les services Web, il suffit de les chercher dans [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Dans la liste, assurez-vous que la case Publier est cochée pour les services Web répertoriés ci-dessus.

## <a name="troubleshooting"></a>Incident
Le tableau de bord Power BI s'appuie sur les services Web publiés qui sont répertoriés ci-dessus. Il affichera les données de la société de démonstration ou de votre propre société si vous importez les données de votre solution financière actuelle. Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.

### <a name="incorrect-company-name"></a>Nom de société incorrect  
Une erreur commune consiste à entrer le nom complet de la société au lieu du nom de la société. Pour trouver le nom de la société, cherchez dans **Sociétés**. Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre société.

### <a name="incorrect-user-name-and-password"></a>Nom d'utilisateur et mot de passe incorrects  
Le nom d'utilisateur et le mot de passe utilisés pour la connexion sont identiques à ceux utilisés pour la connexion à votre compte Microsoft Office 365.  

Les packs de contenu nécessitent également que vous ayez un compte [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft. Une fois les informations d'identification saisies, tous les abonnés [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft accessibles seront détectés automatiquement. Si vous n'avez pas de compte Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sous licence ou d'essai, vous recevrez un message d'erreur.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>La clé ne correspond à aucune ligne de la table
Si vous entrez un nom de société non valide pendant le processus de connexion, le message d'erreur suivant « La clé ne correspond à aucune ligne de la table » peut s'afficher. Indiquez le nom de société correct, puis reconnectez-vous.

## <a name="see-also"></a>Voir aussi
[Mise en route avec Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Concepts de base](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Veille économique](bi.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
