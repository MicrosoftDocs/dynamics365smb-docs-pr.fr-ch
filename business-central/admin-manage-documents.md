---
title: "Gérer, supprimer ou compresser des documents | Microsoft Docs"
description: "Conservez vos données historiques ou supprimez-les."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5cc49d8b17a56c8f19926cf33e63467005d4788c
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="manage-documents"></a>Gérer les documents
Un rôle central, par exemple un administrateur d'application, doit régulièrement gérer les documents accumulés au fil du temps en les supprimant ou en les compressant.  

## <a name="delete-documents"></a>Supprimer documents
Dans certains cas, vous pouvez souhaiter supprimer des commandes achat facturées qui n'ont pas été supprimées. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie que vous avez entièrement facturé les commandes achat supprimées. Vous ne pouvez pas supprimer de commandes qui n'ont pas été entièrement facturées et reçues.  

Les retours sont généralement supprimés après leur facturation. Lorsque vous validez une facture, elle est transférée vers la page **Avoir achat enregistré**. Si vous avez activé la case à cocher **Expédition retour sur avoir** sur la page **Paramètres achats**, la facture est transférée vers la page **Expédition retour enregistrée**. Vous pouvez supprimer les documents à l'aide du traitement par lots **Supprimer les retours achat facturés**. Avant de procéder à la suppression, le traitement par lots vérifie que les retours achat ont été entièrement livrés et facturés.  

Les commandes ouvertes achat ne sont pas supprimées une fois que toutes les commandes achat associées ont été traitées et facturées. Vous pouvez supprimer les commandes ouvertes à l'aide du traitement par lots **Supprimer commandes ouvertes achat facturées**.  

Les commandes service facturées sont habituellement supprimées automatiquement après avoir été entièrement facturées. Lors de la validation d'une facture, une écriture correspondante est générée sur la page **Factures service enreg.**. Vous pouvez afficher le document validé sur la page **Facture service enreg.**.  

Le programme ne supprime pas la commande service automatiquement cependant, si la quantité totale sur la commande a été validée, non pas à partir de la commande service proprement dite, mais à partir de la page **Facture service**. Ensuite, il se peut que vous deviez supprimer des commandes facturées qui n'ont pas été supprimées. Pour ce faire, exécutez le traitement par lots **Supprimer commandes service facturées**.  

## <a name="see-also"></a>Voir aussi  
[Administration](admin-setup-and-administration.md)  

