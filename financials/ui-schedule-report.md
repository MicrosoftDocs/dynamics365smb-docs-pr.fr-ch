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
ms.lasthandoff: 07/07/2017


---
# <a name="schedule-a-report-to-run"></a>Planifier un état à exécuter
Vous pouvez planifier un état à exécuter à une date et une heure spécifiques. Les états prévus sont entrés dans la file projets et traités au moment prévu, comme les autres projets. Vous pouvez choisir de sauvegarder l'état traité dans un fichier, par exemple, Excel, Word ou PDF, de l'imprimer sur une imprimante sélectionnée ou de traiter l'état uniquement. Si vous choisissez d'enregistrer l'état dans un fichier, alors l'état traité est envoyé à la **Boîte de réception état** de votre page d'accueil, dans laquelle vous pouvez l'afficher.

Vous pouvez planifier un état lorsque vous l'ouvrez. Vous devez sélectionner **Planifier** et entrer des informations telles que l'imprimante, ainsi que la date et l'heure. L'état est alors ajouté à la file d'attente des travaux et sera exécuté au moment spécifié. Lorsque l'état a été traité, l'article est supprimé de la file projets. Si vous avez enregistré l'état traité dans un fichier, il est disponible dans la **Boîte de réception état**.

## <a name="see-also"></a>Voir aussi
[Spécifier la sélection de l'imprimante pour les états](ui-specify-printer-selection-reports.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

