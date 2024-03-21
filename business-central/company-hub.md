---
title: Gérer le travail entre plusieurs entreprises dans le Hub Entreprise
description: En savoir plus sur le Hub Entreprise Dynamics 365 Business Central que vous utilisez pour gérer votre travail dans plusieurs entreprises.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '1151, 1154, 1165, 1166'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Gérer le travail entre plusieurs entreprises dans le Hub Entreprise

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Certaines personnes travaillent dans plusieurs entreprises [!INCLUDE [prod_short](includes/prod_short.md)], et certains travaillent également dans plus d’une organisation, comme des comptables externes, ou des employés et des gestionnaires de sociétés ayant plusieurs filiales. Pour ces utilisateurs, et bien d’autres, le Hub Entreprise sert de page de destination qui donne une vue d’ensemble financière des entreprises et des environnements. Il offre aux utilisateurs un outil pour gérer le travail dans les différents environnements dans lesquels ils travaillent, entre les entreprises, les environnements et les régions.  

Vous pouvez accéder au hub de l’entreprise en passant au rôle **Hub Entreprise** dans Mes paramètres, ou en ouvrant la page **Hub Entreprise**. Vous pouvez faire le même travail aux deux endroits, mais les actions sont placées légèrement différemment dans les menus.  

[![Affiche la page Hub Entreprise qui répertorie toutes les entreprises.](media/company-hub.png)](media/company-hub.png#lightbox)  

> [!NOTE]
> Vous pouvez connecter le Hub Entreprise à autant d’entreprises que vous le souhaitez. Cependant, vous ne pouvez connecter le Hub Entreprise qu’aux entreprises hébergées dans [!INCLUDE [prod_short](includes/prod_short.md)] en ligne.

## Page d’accueil du Hub Entreprise

Si vous utilisez le rôle de **Hub Entreprise**, votre page d’accueil affiche une liste des entreprises auxquelles vous avez accès, y compris des informations sur les données des points clés d’intérêt et des liens pour ouvrir chaque entreprise. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Choisissez l’action **Hub Entreprise** pour ouvrir le Hub Entreprise, où vous pouvez travailler plus étroitement avec chaque entreprise.  

> [!TIP]
> Pour accéder à une entreprise spécifique dans [!INCLUDE [prod_short](includes/prod_short.md)], choisissez le nom de l’entreprise ou choisissez l’élément de menu **Accéder à la société**, vous êtes connecté automatiquement dans un nouvel onglet de navigateur.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Actions pour une entreprise répertoriée dans le Hub Entreprise.":::

Vous pouvez ajouter de nouvelles sociétés, par exemple lorsque vous obtenez un nouveau client ou lorsque votre société ajoute une nouvelle filiale. Pour plus d’informations, voir [Ajouter des entreprises à votre Hub Entreprise](company-hub-add-company.md).  

> [!TIP]
> Afin d’actualiser les données dans le Hub Entreprise, vous devez avoir accès aux données des entreprises dont les données proviennent.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## Tâches affectées

Dans le [!INCLUDE [prod_short](includes/prod_short.md)], vous pouvez affecter des tâches à vous-même et à d’autres utilisateurs, et d’autres utilisateurs peuvent vous affecter des tâches. Le Hub Entreprise vous fournit un aperçu des tâches affectées à chaque client, et vous pouvez également accéder à une liste de toutes les tâches affectées en choisissant **Mes tâches utilisateur** sur la page **Accueil**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### Mes tâches utilisateur

La liste **Mes tâches utilisateur** vous permet de planifier votre journée en affichant plus d’informations sur les tâches qui vous sont affectées chez tous vos sociétés.  

Vous pouvez effectuer un tri par date d’échéance, par exemple, ou tout autre type de données vous permettant de planifier votre journée. Par défaut, la liste affiche toutes les tâches qui vous sont affectées, mais vous pouvez définir des filtres pour afficher uniquement les tâches qui sont marquées comme ayant une priorité élevée, par exemple.  

Pour sélectionner une tâche, cliquez dessus dans la liste des tâches utilisateur en attente. Dans le ruban, le lien **Atteindre l’élément de tâche** ouvre la page sur laquelle vous pouvez effectuer le travail.  

Lorsque vous avez terminé une tâche, marquez-la comme terminée.  

Pour plus d’informations sur les entreprises et les environnements, voir [Liens d’environnements](company-hub-add-company.md#environment-links).  

## Accéder au Hub Entreprise

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Pour accéder au Hub Entreprise, vous devez avoir accès via le groupe d’utilisateurs *HUB ENTREPRISE D365* ou via l’ensemble d’autorisations *HUB ENTREPRISE D365*. Vous devez également avoir accès aux sociétés répertoriées dans votre Hub Entreprise, ce qui signifie que vous devez être un utilisateur de ces sociétés. Pour plus d’informations, voir [Créer des utilisateurs conformément aux licences](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Le Hub Entreprise est une liste à l’échelle de l’entreprise, de sorte que tout utilisateur qui a accès au Hub Entreprise pourra voir toutes les entreprises de leur propre chef. Le client [!INCLUDE [prod_short](includes/prod_short.md)] et tous les indicateurs de performance clés des entreprises auxquelles ils ont accès.

Si vous ne parvenez pas à trouver le Hub Entreprise et que vous savez que vous y avez obtenu l’accès, vérifiez auprès de votre administrateur si le Hub Entreprise est répertorié dans la page **Gestion des extensions**. Pour plus d’informations, voir [Personnalisation de Business Central à l’aide d’extensions](ui-extensions.md).  

## Configurer le Hub Entreprise

Pour commencer à utiliser le Hub Entreprise, vous devez ajouter une ou plusieurs entreprises à votre tableau de bord. Pour plus d’informations, voir [Ajouter des entreprises à votre Hub Entreprise](company-hub-add-company.md).  

Mais pour ajouter une entreprise, vous devez avoir accès à une ou plusieurs instances de [!INCLUDE [prod_short](includes/prod_short.md)] en plus de l’entreprise dans laquelle vous utilisez le Hub Entreprise.  

Par exemple, si vous êtes comptable, vos clients peuvent vous inviter à leur [!INCLUDE [prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Inviter votre comptable externe dans votre Business Central](finance-accounting.md#inviteaccountant).  

Les administrateurs peuvent utiliser le même guide de configuration assistée pour vous ajouter à leur [!INCLUDE [prod_short](includes/prod_short.md)], ou ils peuvent vous ajouter au compte Microsoft Entra approprié dans le centre d’administration Microsoft 365. Pour en savoir plus, voir [Gérer les utilisateurs et les groupes](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## Voir aussi

[Ajouter des entreprises à votre Hub Entreprise](company-hub-add-company.md)  
[Expériences de comptables dans Business Central](finance-accounting.md)  
[Hub Entreprise pour l’extension Business Central](ui-extensions-company-hub.md)  
[Modifier les paramètres de base](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]