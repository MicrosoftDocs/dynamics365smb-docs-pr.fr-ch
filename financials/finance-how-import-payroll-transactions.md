---
title: "Procédure : Importer les transactions de paie| Microsoft Docs"
description: "Décrit comment importer les paiements des salaires et les transactions associées à partir de votre fournisseur de paie dans les écritures comptables."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Procédure d'importation de transactions de paie 
Pour tenir compte des paiements des salaires et des transactions associées, vous devez importer et valider des transactions financières effectuées par votre fournisseur de paie dans la comptabilité. Pour cela, vous devez commencer par importer un fichier que vous recevez du fournisseur de paie dans la fenêtre **Feuille comptabilité**. Vous devez ensuite mapper les comptes externes du fichier de paie aux comptes généraux appropriés. Enfin, vous devez valider les transactions de paie en fonction du mappage de compte.

**Remarque** : Pour utiliser cette fonctionnalité, une extension pour l'importation de la paie doit être installée et activée. Les extensions Salaire de Ceridian et Importer le fichier de paie de Quickbooks sont préinstallées dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, reportez-vous à [Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Pour importer un fichier de paie
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Feuilles comptabilité**, puis sélectionnez le lien associé.
2. Dans le nom feuille comptabilité pertinent, sélectionnez l'action **Importer les transactions de paie**. Un guide d'installation assisté s'ouvre.
3. Suivez les étapes de la fenêtre **Importer les transactions de paie**.

    **Astuce** : Dans l'étape à propos du mappage des enregistrements de paie externes dans les comptes généraux, les mappages que vous effectuez seront reconnus la prochaine fois que les mêmes enregistrements seront importés. Cela vous permettra de gagner du temps car vous n'avez pas à renseigner manuellement le champ **N° compte.** de la feuille comptabilité chaque fois que vous importez des transactions de paie récurrentes.   

    Lorsque vous cliquez sur le bouton **OK** dans le guide de configuration assistée, la fenêtre **Feuille comptabilité** est complétée par des lignes représentant les transactions contenues dans le fichier de paie et par les comptes appropriés des champs **Compte général** en fonction des mappages effectués dans le guide.
4. Modifiez ou validez les lignes feuille comme pour toute autre transaction comptable générale. Pour plus d'informations, reportez-vous à [Procédure : utilisation des feuilles comptabilité](ui-work-general-journals.md).   

## <a name="see-also"></a>Voir aussi
[Finance](finance.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)  
[Procédure : travailler avec les feuilles comptabilité](ui-work-general-journals.md)  

