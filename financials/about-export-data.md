---
title: "Exportation de données vers Excel à partir de Dynamics 365 for Financials | Microsoft Docs"
description: "En savoir plus sur l&quot;exportation des données de Dynamics 365 for Financials vers Excel."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 02/22/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 94b2bbcd3db4b5071221b6f24e0f960355db3af1
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="exporting-your-data-to-excel-from-dynamics-365-for-financials"></a>Exportation de vos données de Dynamics 365 for Financials vers Excel
Si vous souhaitez travailler avec vos données à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Excel, vous pouvez ouvrir toutes les listes et les utiliser dans Excel. De même, si vous souhaitez annuler votre abonnement à [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], vous pouvez exporter vos données vers Excel afin de pouvoir les transférer par la suite.

## <a name="opening-lists-in-excel"></a>Ouverture de listes dans Excel
Vous pouvez ouvrir des données dans Excel à partir de n'importe quelle feuille ou liste. Il vous suffit d'ouvrir la page que vous souhaitez, puis de cliquer sur **Ouvrir dans Excel**. Par exemple, ouvrez la liste des clients (recherchez **Clients**), puis sélectionnez **Ouvrir dans Excel**. Votre navigateur vous invite alors à ouvrir ou à enregistrer le classeur Excel généré.  

Chaque liste inclut un certain nombre de colonnes, et l'exportation vers Excel inclut toutes les colonnes qui sont dans votre vue actuelle. Si vous souhaitez ajouter ou supprimer des colonnes avant d'ouvrir la liste dans Excel, il vous suffit simplement d'ouvrir le menu contextuel de n'importe quelle colonne et d'indiquer ensuite les colonnes que vous souhaitez visualiser. Cette liste de colonnes est différente de la plupart des listes, et elle reflète la structure de la base de données où vos données sont enregistrées. Si vous ne connaissez pas le type de données d'une certaine colonne, vous pouvez l'ajouter à votre affichage, puis décider de la supprimer à nouveau.  

## <a name="exporting-data-to-other-finance-systems"></a>Exportation de données vers d'autres systèmes financiers
Si vous décidez d'annuler votre abonnement à [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exporter vos données vers Excel et les transférer ensuite dans votre système financier suivant.  

Bien entendu, vous pouvez exporter toutes les pages, mais il peut y en avoir trop. Vous devez donc exporter les principales pages suivantes, et penser à ajouter toutes les colonnes comme décrit précédemment :  

* Plan comptable  
* Clients  
* Fournisseurs  
* Banques  
* Articles  

Si vous souhaitez exporter toutes vos transactions financières également, le volume de données est alors très important et l'exportation prend alors souvent plusieurs minutes. Les transactions financières sont affichées dans la page **Écritures comptables**.  

Nous recommandons également d'exporter des données à partir des pages suivantes :  

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

**Remarque** : Si vous avez défini plusieurs sociétés dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], vous devez exporter les données appropriées de chaque société.

## <a name="see-also"></a>Voir aussi
[Annulation de votre abonnement à [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](madeira-cancel.md)  
[Importation de données métier à partir d'autres systèmes financiers](upload-data.md)  
[Finance](finance.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

