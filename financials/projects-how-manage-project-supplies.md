---
title: "Procédure : gérer les fournitures pour un projet| Microsoft Docs"
description: "Décrit comment fournir du matériel et des services aux projets."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f52fa9545b50038c1d28daa164add07915ef2656
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-supplies"></a>Procédure : Gérer les fournitures pour un projet
La gestion des fournitures des projets relatifs à des articles, services et dépenses est l'un des aspects essentiels de l'exécution d'un projet. Vous pouvez utiliser les quantités de stock ou effectuer des achats spécifiques au projet en utilisant des commandes achat ou des factures achat. Par exemple, un projet de service sur un ordinateur requiert un nouveau disque. Vous devez donc créer une facture achat pour l'acheter et pour enregistrer le projet pour lequel il sera utilisé.

Si le processus d'achat ne requiert pas d'enregistrement séparé de la transaction physique, un achat peut être traité dans la fenêtre **Feuille compta. projet**. Pour plus d'informations, reportez-vous à [Procédure : Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Pour acheter des articles ou des services pour un projet
La procédure suivante indique comment utiliser une facture achat pour acheter des produits pour un projet. Les mêmes étapes s'appliquent lors de l'utilisation d'une commande achat.  

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Factures achat**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**, puis renseignez les champs selon vos besoins. Pour plus d'informations, reportez-vous à [Procédure : enregistrer des achats](purchasing-how-record-purchases.md).
3. Dans les champs **N° projet ** et **N° tâche projet**, sélectionnez les informations du projet pour lequel vous souhaitez acheter des articles ou des services. Utilisez la fonction **Choisir les colonnes** si le champ n'est pas visible. Pour plus d'informations, voir [Personnalisation utilisateur](ui-user-personalization.md).

    La valeur que vous sélectionnez dans le champ **Type ligne projet** définit si une ligne planning est créée lorsque vous validez l'activité de l'article. Si le champ indique **Facturable**, les lignes planning projet prêtes pour facturation sont créées. Pour plus d'informations, reportez-vous à [Procédure : Facturer des projets](projects-how-invoice-jobs.md).
4. Sélectionnez l'action **Valider**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Pour afficher la valeur des achats pour un projet
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Projets**, puis sélectionnez le lien associé.
2. Ouvrez la fiche projet appropriée.

    Dans le raccourci **Tâches**, le champ **Commandes ouvertes** affiche le montant total en commande, en devise société, des articles en stock et des services sur les documents achat pour la tâche projet ligne.  

    Le champ **Montant reçu non facturé** affiche la valeur des articles livrés sur les documents achat mais non facturés.  
3. Choisissez l'un des champs pour ouvrir la fenêtre **Lignes achat** dans laquelle vous pouvez consulter des informations sur les lignes de document achat associées, incluant les articles ou les services qui ont été réceptionnés.

## <a name="to-post-a-job-related-expense"></a>Pour valider des frais liés à un projet
Si vous supportez les dépenses extraordinaires ou exceptionnelles du projet, vous pouvez utiliser la fenêtre **Feuille compta. projet** pour les valider directement dans le compte projet approprié.

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuilles compta. projet**, puis sélectionnez le lien associé.  
2. Créez une ligne et renseignez les informations concernant les frais, notamment les informations des champs **N° projet** et **N° tâche projet**.  
3. Lorsque la feuille est renseignée, cliquez sur **Valider**.

## <a name="see-also"></a>Voir aussi
[Gestion de projets](projects-manage-projects.md)  
[Finance](finance.md)  
[Achats](purchasing-manage-purchasing.md)         
[Ventes](sales-manage-sales.md)      
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

