---
title: Exporter vos données Business Central vers Excel| Microsoft Docs
description: Vous pouvez exporter vos états financiers et vos données de veille économique de Business Central vers Excel, ou ouvrir vos données dans Excel.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4a6bfb8d20c13019807b2308737380c4fd31dcc6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776512"
---
# <a name="exporting-your-business-data-to-excel"></a>Exportation de vos données métier vers Excel
Si vous souhaitez travailler avec vos données à partir de [!INCLUDE[prod_short](includes/prod_short.md)] dans Excel, vous pouvez ouvrir toutes les listes et les utiliser dans Excel. De même, si vous souhaitez annuler votre abonnement à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez exporter vos données vers Excel afin de pouvoir les transférer par la suite.

## <a name="opening-lists-in-excel"></a>Ouverture de listes dans Excel
Vous pouvez ouvrir des données dans Excel à partir de n’importe quelle feuille ou liste. Il vous suffit d’ouvrir la page que vous souhaitez, puis de cliquer sur **Ouvrir dans Excel**. Par exemple, ouvrez la liste des clients (recherchez **Clients**), puis sélectionnez **Ouvrir dans Excel**. Votre navigateur vous invite alors à ouvrir ou à enregistrer le classeur Excel généré.  

> [!NOTE]
> Utilisez cette option si vous ne souhaitez pas effectuer et publier des modifications à nouveau dans [!INCLUDE[prod_short](includes/prod_short.md)].  

Chaque liste inclut un certain nombre de colonnes, et l’exportation vers Excel inclut toutes les colonnes qui sont dans votre vue actuelle. Si vous souhaitez ajouter ou supprimer des colonnes avant d’ouvrir la liste dans Excel, il vous suffit simplement d’ouvrir le menu contextuel de n’importe quelle colonne et d’indiquer ensuite les colonnes que vous souhaitez visualiser. Cette liste de colonnes est différente de la plupart des listes, et elle reflète la structure de la base de données où vos données sont enregistrées. Si vous ne connaissez pas le type de données d’une certaine colonne, vous pouvez l’ajouter à votre affichage, puis décider de la supprimer à nouveau.  

### <a name="edit-data-in-excel"></a>Modifier des données dans Excel
Votre expérience [!INCLUDE[prod_short](includes/prod_short.md)] inclut un complément pour Excel vous permettant de modifier des données dans Excel. Pour plus d’informations, voir [Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Exportation de données vers d’autres systèmes financiers
Si vous décidez d’annuler votre abonnement à [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez exporter vos données vers Excel et les transférer ensuite dans votre système financier suivant.  

Bien entendu, vous pouvez exporter toutes les pages, mais il peut y en avoir trop. Vous devez donc exporter les principales pages suivantes, et penser à ajouter toutes les colonnes comme décrit précédemment :  

* Plan comptable  
* Clients  
* Fournisseurs  
* Banques  
* Articles  

Si vous souhaitez exporter toutes vos transactions financières également, le volume de données est alors très important et l’exportation prend alors souvent plusieurs minutes. Les transactions financières sont affichées sur la page **Écritures comptables**.  

Nous recommandons également d’exporter des données à partir des pages suivantes :  

* Écritures comptables client  
* Écritures comptables fournisseur  
* Écritures comptables compte bancaire  
* Écritures comptables article  
* Paramètres comptabilisation  
* Groupes compta. client  
* Groupes compta. fournisseur  
* Groupes comptabilisation stock  
* Groupe comptabilisation banque  
* Budgets  
* Écritures budget  
* Devis  
* Factures vente  
* Factures achat  
* Contacts  
* Vendeurs  

> [!NOTE]  
> Si vous avez défini plusieurs sociétés dans [!INCLUDE[prod_short](includes/prod_short.md)], vous devez exporter les données appropriées de chaque société.

> [!NOTE]
> Vous devez disposer d’au moins l’une des autorisations suivantes pour ouvrir ou modifier des données dans Excel :
>    - Ensemble d’autorisations *Action Exportation Excel D365*  
>    - Autorisation système 6110 *Autoriser l’action Exporter vers Excel*.  

Pour plus d’informations, voir [Pour afficher ou modifier les autorisations d’un utilisateur](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi
[Annuler pour votre abonnement [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Analyse des états financiers dans Microsoft Excel](finance-analyze-excel.md)  
[Finances](finance.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]