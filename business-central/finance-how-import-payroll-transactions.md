---
title: Importer les transactions de paie| Microsoft Docs
description: Pour gérer les paies, vous importez et validez des transactions financières de votre fournisseur de paie dans la comptabilité, en utilisant une extension de paie telle que Ceridian ou Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: a99cbfec41bc4bf1e2cd5971d4cf5806bf42ab2b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183656"
---
# <a name="import-payroll-transactions"></a>Importer les transactions de paie
Pour tenir compte des paiements des salaires et des transactions associées, vous devez importer et valider des transactions financières effectuées par votre fournisseur de paie dans la comptabilité. Pour cela, vous devez commencer par importer un fichier que vous recevez du fournisseur de paie sur la page **Feuille comptabilité**. Vous devez ensuite mapper les comptes externes du fichier de paie aux comptes généraux appropriés. Enfin, vous devez valider les transactions de paie en fonction du mappage de compte.

> [!NOTE]  
>   Pour utiliser cette fonctionnalité, une extension pour l'importation de la paie doit être installée et activée. Les extensions Salaire de Ceridian et Importer le fichier de paie de Quickbooks sont préinstallées dans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour plus d'informations, voir [Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Pour importer un fichier de paie
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité**, puis sélectionnez le lien associé.
2. Dans le nom feuille comptabilité pertinent, sélectionnez l'action **Importer les transactions de paie**. Un guide d'installation assisté s'ouvre.
3. Suivez les étapes de la page **Importer les transactions de paie**.

    > [!TIP]  
    >   Dans l'étape à propos du mappage des enregistrements de paie externes dans les comptes généraux, les mappages que vous effectuez seront reconnus la prochaine fois que les mêmes enregistrements seront importés. Cela vous permettra d'économiser du temps car vous n'avez pas à remplir manuellement le champ **N° compte** dans la feuille comptabilité à chaque importation de transactions de paie récurrentes.   

    Lorsque vous cliquez sur le bouton **OK** dans le guide de configuration assistée, la page **Feuille comptabilité** est complétée par des lignes représentant les transactions contenues dans le fichier de paie et par les comptes appropriés des champs **Compte général** en fonction des mappages effectués dans le guide.
4. Modifiez ou validez les lignes feuille comme pour toute autre transaction comptable générale. Pour plus d'informations, reportez-vous à [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
