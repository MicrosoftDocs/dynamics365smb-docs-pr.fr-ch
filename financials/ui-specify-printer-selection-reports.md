---
title: "Paramétrage d'états à imprimer sur des imprimantes spécifiques | Microsoft Docs"
description: "En savoir plus sur la configuration d'une imprimante pour un état et l'utilisation de la fenêtre Sélections d'imprimantes."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9612d1b0859639bf25713dd8bcfbebdaacd3517e
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="1faa1-103">Spécifier la sélection de l'imprimante pour les états</span><span class="sxs-lookup"><span data-stu-id="1faa1-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="1faa1-104">Cette page est vide car vous ne pouvez pas encore configurer d'imprimantes spécifiques pour des états spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1faa1-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="1faa1-105">Nous essayons de résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="1faa1-105">We are working on solving this.</span></span>

<span data-ttu-id="1faa1-106">En attendant, si vous souhaitez imprimer un état, vous devez d'abord le télécharger en tant document PDF en choisissant le bouton **Envoyer à**.</span><span class="sxs-lookup"><span data-stu-id="1faa1-106">In the meantime, when you want to print a report, you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="1faa1-107">Puis, vous devez sélectionner le type d'état pour télécharger le fichier et choisir **Document PDF**.</span><span class="sxs-lookup"><span data-stu-id="1faa1-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="1faa1-108">À présent, vous pouvez soit ouvrir le document directement en PDF et l'imprimer, ou l'enregistrer et l'imprimer plus tard.</span><span class="sxs-lookup"><span data-stu-id="1faa1-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="1faa1-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1faa1-109">See Also</span></span>
<span data-ttu-id="1faa1-110">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1faa1-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1faa1-111">Exécuter des traitements par lots</span><span class="sxs-lookup"><span data-stu-id="1faa1-111">Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="1faa1-112">Envoyer des documents par e-mail</span><span class="sxs-lookup"><span data-stu-id="1faa1-112">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  

