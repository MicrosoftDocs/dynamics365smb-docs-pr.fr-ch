---
title: "Procédure : créer une présentation de rapport ou de document personnalisée | Microsoft Docs"
description: "Apprenez à concevoir la présentation d&quot;un état."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 79c1e5c1ea01077e2e5012ba07618760ccf2a4af
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Procédure : créer une présentation de rapport ou de document personnalisée
Par défaut, un rapport aura une présentation de rapport intégrée, qui peut être soit une présentation de rapport RDLC ou une présentation de rapport Word, ou les deux. Vous ne pouvez pas modifier les présentations intégrées. Cependant, vous pouvez créer vos propres présentations personnalisées qui vous permettent de modifier l'apparence d'un rapport lorsqu'il est consulté, imprimé ou enregistré. Vous pouvez créer plusieurs présentations de rapport personnalisées pour le même rapport, puis faire basculer la présentation utilisée par un rapport selon vos besoins.

**Remarque** : dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le terme « état » couvre également les documents externes, tels que les factures vente et les confirmations de commande que vous envoyez à des clients comme fichiers PDF.

Pour créer une présentation personnalisée, vous pouvez effectuer une copie d'une présentation personnalisée existante ou ajouter une nouvelle présentation personnalisée, qui est le plus souvent basée sur une présentation intégrée. Lorsque vous ajoutez une nouvelle présentation personnalisée, vous pouvez choisir d'ajouter un type de présentation de rapport RDLC, un type de présentation de rapport Word, ou les deux. La nouvelle présentation personnalisée est automatiquement basée sur la présentation intégrée pour le rapport s'il y en a une disponible. S'il n'y a pas de présentation intégrée pour le type, alors une nouvelle présentation vide est créée, que vous devrez modifier et concevoir entièrement. Pour plus d'informations sur les présentations de rapport RDLC et Word, les présentations intégrées et personnalisées, et plus encore, reportez-vous à [Gérer la présentation des états](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Pour créer une présentation personnalisée
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Search for Page or Report icon"), entrez **Sélection présentation état**, puis sélectionnez le lien connexe.  
   La fenêtre **Sélection présentation état** répertorie tous les états disponibles dans la société spécifiée dans le champ Société en haut de la fenêtre.
2. Définissez le champ **Société** sur la société pour laquelle vous souhaitez créer la présentation de rapport.
3. Sélectionnez la ligne de l'état pour lequel vous souhaitez créer la présentation, puis sélectionnez **Présentations personnalisées**.  
   La fenêtre **Présentations état personnalisées** s'affiche et répertorie toutes les présentations personnalisées disponibles pour l'état sélectionné.
4. Si vous souhaitez créer une copie d'une présentation personnalisée existante, sélectionnez cette dernière, puis sélectionnez **Copier**.  
   La copie de la présentation personnalisée s'affiche dans la fenêtre **Présentations état personnalisées**. Le terme Copie figure dans le champ Description.
5. Si vous voulez ajouter une nouvelle présentation personnalisée basée sur une présentation intégrée, procédez comme suit :  
   1. Choisissez **Nouveau**. La fenêtre **Insérer présentation intégrée pour un état** s'affiche. Les champs **ID** et **Nom** sont automatiquement renseignés.
   2. Pour ajouter un type de présentation de rapport Word, cochez la case **Insérer présentation Word**.
   3. Pour ajouter un type de présentation de rapport RDLC, cochez la case **Insérer présentation RDLC**.
   4. Cliquez sur le bouton **OK**.  
      Les nouvelles présentations personnalisées s'affichent dans la fenêtre **Présentations état personnalisées**. Si une nouvelle présentation est basée sur une présentation intégrée, les termes **Copie d'une présentation intégrée** figurent dans le champ **Description**. S'il n'y avait aucune présentation intégrée pour l'état, les termes **Nouvelle présentation** figurent dans le champ **Description** de la nouvelle présentation, ce qui indique que la présentation personnalisée est vide.
6. Par défaut, le champ **Nom de la société** est vide, ce qui signifie que la présentation personnalisée est disponible pour l'état dans toutes les sociétés. Afin que la présentation personnalisée soit disponible pour une société spécifique uniquement, sélectionnez **Modifier**, puis définissez le champ **Nom de la société** sur la société que vous souhaitez.

## <a name="see-also"></a>Voir aussi
[Gestion des présentations de rapport](ui-manage-report-layouts.md)  
[Procédure : Modification de la présentation actuellement utilisée sur un rapport](ui-how-change-layout-currently-used-report.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

