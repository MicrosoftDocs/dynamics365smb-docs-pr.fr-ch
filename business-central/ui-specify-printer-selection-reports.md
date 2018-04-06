---
title: "Paramétrage d'états à imprimer sur des imprimantes spécifiques | Microsoft Docs"
description: "En savoir plus sur la configuration d'une imprimante pour un état et l'utilisation de la fenêtre Sélections d'imprimantes."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a07caec88ece9b9e940777976d6d5555839ae581
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="specify-printer-selection-for-reports"></a>Spécifier la sélection de l'imprimante pour les états
Cette page est vide car vous ne pouvez pas encore configurer d'imprimantes spécifiques pour des états spécifiques. Nous essayons de résoudre ce problème.

En attendant, si vous souhaitez imprimer un état, vous devez d'abord le télécharger en tant document PDF en choisissant le bouton **Envoyer à**. Puis, vous devez sélectionner le type d'état pour télécharger le fichier et choisir **Document PDF**. À présent, vous pouvez soit ouvrir le document directement en PDF et l'imprimer, ou l'enregistrer et l'imprimer plus tard.

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Exécuter des traitements par lots](ui-how-run-batch-jobs.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  

