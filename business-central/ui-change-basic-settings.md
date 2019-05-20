---
title: Affichage et modification des paramètres de base | Microsoft Docs
description: Découvrez comment modifier certains paramètres de base, par exemple, le tableau de bord, la société ou la date de travail.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: d95d2f609129e4bdba35deda726323dbed2ba67a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250998"
---
# <a name="changing-basic-settings"></a>Modification des paramètres de base
Sur la page [**Mes paramètres**](https://businesscentral.dynamics.com?page=9176 "Accédez directement à votre page Paramètres utilisateurs dans Business Central"), vous pouvez visualiser et modifier les paramètres de base pour [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vos modifications affectent uniquement votre espace de travail, et non les espaces de travail des autres utilisateurs.  

## <a name="role-center"></a> Tableau de bord
Le tableau de bord représente la page d'accueil, un écran de démarrage conçu pour les exigences d'un rôle spécifique dans une organisation. Selon votre rôle, le tableau de bord donne une vue d'ensemble de l'entreprise, de votre département ou de vos tâches personnelles. Il vous permet également d'accéder à vos tâches quotidiennes et de rechercher les tâches qui vous sont affectées.

-   En haut, la navigation vous permet de permuter entre les clients, les fournisseurs, les articles et d'autres listes d'informations importantes. De même, les actions vous permettent de lancer des tâches, comme la création d'une facture vente, directement à partir du tableau de bord.

-   Au centre, vous trouverez les **Activités**. Les activités affichent les données actuelles et vous pouvez cliquer ou appuyer dessus pour afficher des informations plus détaillées. Les indicateurs de performance clés peuvent être configurés de sorte à afficher un graphique sélectionné pour une représentation visuelle, par exemple, de la trésorerie ou des revenus et des dépenses. Vous pouvez également générer la liste des clients favoris sur la page d'accueil pour les comptes avec lesquels vous travaillez souvent ou auxquels vous devez accorder une attention particulière.

### <a name="to-change-role-center"></a>Pour modifier le tableau de bord
Le Tableau de bord par défaut est **Gestionnaire d'activité**, mais vous pouvez sélectionner un autre Tableau de bord qui correspond mieux à vos besoins mieux.
1. Dans le coin supérieur droit, sélectionnez l'icône **Paramètres** ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez **Mes paramètres**.
2. Sur la page **Mes paramètres**, dans le champ **Tableau de bord** , sélectionnez le Tableau de bord que vous souhaitez définir comme standard. Par exemple, sélectionnez **Comptable**.
3. Cliquez sur le bouton **OK**.

## <a name="company"></a>Société
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une société fonctionne comme un conteneur de données. Il peut y avoir plusieurs sociétés dans une seule base de données, mais une seule peut être sélectionnée à la fois.

La société par défaut est appelée CRONUS et contient uniquement des données de démonstration.

> [!TIP]  
>   Pour afficher un nom différent pour votre société dans l'application (par exemple sur le Tableau de bord), définissez le champ **Nom** sur la page **Informations société** ou le champ **Nom d'affichage** sur la page **Sociétés**.  

## <a name="work-date"></a>Date de travail
La date de travail par défaut est généralement la date du jour. Vous pouvez être amené à modifier temporairement la date de travail pour effectuer des tâches telles que l'exécution de transactions à une date différente de la date actuelle, .

> [!TIP]  
>   Pour entrer rapidement la date de travail dans un champ de date, tapez **t**. Pour entrer la date actuelle dans le champ de date, tapez **a**.

> [!IMPORTANT]  
>   Une fois la date de travail modifiée, si vous vous déconnectez ou si vous changez de société, les données de travail reviennent par défaut à la date de travail. Ainsi, la prochaine fois que vous vous connecterez ou lorsque vous reviendrez à la société d'origine, vous devrez peut-être redéfinir la date de travail. 

### <a name="work-date-indication"></a>Indication de la date de travail
<!--
Whenever the work date is not set to the current day (today), there are two indicators on pages that you open for editing:

- A reminder appears at the top of the page that tells you what the work date is set to. The reminder provides a direct link to the work date setting on the **My Settings** page so you change the date if you want. From the reminder, you can also choose to dismiss the reminder for the rest of your session. Unless you change the work date to "today", the reminder will appear the next time you sign in. 

- If you dismiss the reminder, the work date will appear in the title of the page.  
-->
Si la date de travail n'est pas définie sur la date actuelle (aujourd'hui), sur toutes les pages sur lesquelles vous pouvez modifier les données, la date de travail actuelle s'affiche dans l'angle supérieur gauche de la page.
  
## <a name="region"></a> Région

Le paramètre **Région** détermine la manière dont les dates, heures, nombres et devises sont affichés ou mis en forme.


## <a name="language"></a> Langue
Modifie la langue d'affichage. Ce champ s'affiche uniquement lorsque vous avez le choix entre plusieurs langues. 

La langue initiale est déterminée par l'administrateur ou par les paramètres de votre navigateur lorsque vous vous inscrivez à [!INCLUDE[d365fin](includes/d365fin_md.md)]. La langue définie est utilisée sur tous les appareils à partir desquels vous vous connectez, par exemple un téléphone ou une tablette.

## <a name="changing-when-i-receive-notifications"></a>Modification lorsque je reçois des notifications
Sélectionnez ce lien pour afficher ou modifier les notifications que vous recevez au sujet de certains événements ou modification de statut, lorsque vous êtes sur le point de facturer un client avec des écritures échues, ou lorsque le stock disponible est inférieur à la quantité que vous êtes sur le point de vendre. Pour plus d'informations, voir [Notifications intelligentes](ui-smart-notifications.md).

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Modification des fonctionnalités affichées](ui-experiences.md)  
