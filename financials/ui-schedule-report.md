---
title: "Planification d'un état à exécuter à une date et une heure spécifiques | Microsoft Docs"
description: "En savoir plus sur l'entrée d'un état dans une file d'attente de projets et la planification de son traitement à une date et à une heure spécifiques."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, job queue
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0b97a5e48c4b339375ca9ad8cbe8388c5d47bb44
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="schedule-a-report-to-run"></a><span data-ttu-id="a1b7c-103">Planifier un état à exécuter</span><span class="sxs-lookup"><span data-stu-id="a1b7c-103">Schedule a Report to Run</span></span>
<span data-ttu-id="a1b7c-104">Vous pouvez planifier un état à exécuter à une date et une heure spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-104">You can schedule a report to run at a specific date and time.</span></span> <span data-ttu-id="a1b7c-105">Les états prévus sont entrés dans la file projets et traités au moment prévu, comme les autres projets.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-105">Scheduled reports are entered in the job queue and processed at the scheduled time, similar to other jobs.</span></span> <span data-ttu-id="a1b7c-106">Vous pouvez choisir de sauvegarder l'état traité dans un fichier, par exemple, Excel, Word ou PDF, de l'imprimer sur une imprimante sélectionnée ou de traiter l'état uniquement.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-106">You can choose to save the processed report to a file, such as an Excel, Word, or PDF, print it to a selected printer, or process the report only.</span></span> <span data-ttu-id="a1b7c-107">Si vous choisissez d'enregistrer l'état dans un fichier, alors l'état traité est envoyé à la **Boîte de réception état** de votre page d'accueil, dans laquelle vous pouvez l'afficher.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-107">If you choose to save the report to a file, then the processed report is sent to the **Report Inbox** area on your Home page, where you can view it.</span></span>

<span data-ttu-id="a1b7c-108">Vous pouvez planifier un état lorsque vous l'ouvrez.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-108">You can schedule a report when you open a report.</span></span> <span data-ttu-id="a1b7c-109">Vous devez sélectionner **Planifier** et entrer des informations telles que l'imprimante, ainsi que la date et l'heure.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-109">You choose the **Schedule** action and then you enter information such as printer, and time and date.</span></span> <span data-ttu-id="a1b7c-110">L'état est alors ajouté à la file d'attente des travaux et sera exécuté au moment spécifié.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-110">The report is then added to the job queue and will be run at the specified time.</span></span> <span data-ttu-id="a1b7c-111">Lorsque l'état a été traité, l'article est supprimé de la file projets.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-111">When the report is processed, the item will be removed from the job queue.</span></span> <span data-ttu-id="a1b7c-112">Si vous avez enregistré l'état traité dans un fichier, il est disponible dans la **Boîte de réception état**.</span><span class="sxs-lookup"><span data-stu-id="a1b7c-112">If you saved the processed report to a file, it will be available in the **Report Inbox** area.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1b7c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1b7c-113">See Also</span></span>
[<span data-ttu-id="a1b7c-114">Spécifier la sélection de l'imprimante pour les états</span><span class="sxs-lookup"><span data-stu-id="a1b7c-114">Specify Printer Selection for Reports</span></span>](ui-specify-printer-selection-reports.md)  
<span data-ttu-id="a1b7c-115">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1b7c-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

