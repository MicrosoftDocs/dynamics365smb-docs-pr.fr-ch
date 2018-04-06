---
title: "Affichage et modification des paramètres de base dans Financials| Microsoft Docs"
description: "Découvrez comment modifier certains des paramètres de base de Financials, par exemple, le Tableau de bord, la société, ou la date de travail."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ee0615cd475d412f7380d6577bfa2965bb0cee9f
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="changing-basic-settings"></a>Modification des paramètres de base
Dans la fenêtre **Mes paramètres**, vous pouvez afficher et modifier les paramètres de base de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="role-center"></a>Tableau de bord
Le Tableau de bord représente la page d'accueil, une page de démarrage conçue pour les exigences du rôle. Le Tableau de bord vous donne un aperçu de l'entreprise, reflétant les informations, les tâches, et les priorités de votre rôle. 

Avec la partie supérieure du Tableau de bord, vous voyez une barre de navigation qui vous donne un accès facile aux entités courantes du rôle, telles que ses clients, fournisseurs, articles, etc.

Ce qui s'affiche dans la zone de contenu principale dépend du Tableau de bord spécifique. Par exemple, dans la plupart des tableaux de bord, vous pouvez trouver des vignettes Activités qui affichent des données actuelles et sur lesquelles vous pouvez cliquer pour un accès facile au document sélectionné. Les indicateurs de performance clés peuvent être configurés de sorte à afficher un graphique sélectionné pour une représentation visuelle, par exemple, de la trésorerie ou des revenus et des dépenses. Certains tableaux de bord permettent de créer une liste d'entités préférées, comme les clients et les fournisseurs, ou afficher la Boîte de réception état.

### <a name="to-change-role-center"></a>Pour modifier le tableau de bord
Le Tableau de bord par défaut est **Gestionnaire d'activité**, mais vous pouvez sélectionner un autre Tableau de bord qui correspond mieux à vos besoins mieux.
1. Dans le coin supérieur droit, sélectionnez l'icône **Paramètres** ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez **Mes paramètres**.
2. Dans la fenêtre **Mes paramètres**, dans le champ **Tableau de bord** , sélectionnez le Tableau de bord que vous souhaitez définir comme standard. Par exemple, sélectionnez **Comptable**.
3. Cliquez sur le bouton **OK**.

## <a name="company"></a>Société
Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], une société fonctionne comme un conteneur de données. Il peut y avoir plusieurs sociétés dans une seule base de données, mais une seule peut être sélectionnée à la fois.

La société par défaut est appelée CRONUS et contient uniquement des données de démonstration.

> [!TIP]  
>   Pour afficher un nom différent pour votre société dans l'application (par exemple sur la page d'accueil Tableau de bord), définissez le champ **Nom** sur la page **Informations société** ou le champ **Nom d'affichage** sur la page **Sociétés**.  

## <a name="work-date"></a>Date de travail
La date de travail par défaut est généralement la date du jour. Vous pouvez être amené à modifier temporairement la date de travail pour effectuer des tâches telles que l'exécution de transactions à une date différente de la date actuelle, .

> [!TIP]  
>   Pour entrer rapidement la date de travail dans un champ de date, tapez **w**. Pour entrer la date actuelle dans le champ de date, tapez **t**.

> [!IMPORTANT]  
>   La date de travail est seulement modifiée jusqu'à ce que vous fermiez la société ou que la date change. Si vous ouvrez une autre société, ou si vous ouvrez la même société le lendemain, et si vous souhaitez toujours utiliser une date qui n'est pas la date programme, il faut à nouveau établir la date de travail.

## <a name="region"></a>Région
Le paramètre **Région** détermine la manière dont les dates, heures, nombres et devises sont affichés ou mis en forme.   

## <a name="changing-when-i-receive-notifications"></a>Modification lorsque je reçois des notifications
Sélectionnez ce lien pour afficher ou modifier les notifications que vous recevez au sujet de certains événements ou modification de statut, lorsque vous êtes sur le point de facturer un client avec des écritures échues, ou lorsque le stock disponible est inférieur à la quantité que vous êtes sur le point de vendre. Pour plus d'informations, voir [Notifications intelligentes](ui-smart-notifications.md).

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  

