---
title: "Gérer, supprimer ou compresser des documents | Microsoft Docs"
description: "Conservez vos données historiques ou supprimez-les."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 60438f0b6f0d5da60925b5b9c309cc359a8422e3
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="manage-documents"></a>Gérer les documents
Un rôle central, par exemple un administrateur d'application, doit régulièrement gérer les documents accumulés au fil du temps en les supprimant ou en les compressant.  

## <a name="delete-documents"></a>Supprimer documents
Dans certains cas, vous pouvez souhaiter supprimer des commandes achat facturées qui n'ont pas été supprimées. [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie que vous avez entièrement facturé les commandes achat supprimées. Vous ne pouvez pas supprimer de commandes qui n'ont pas été entièrement facturées et reçues.  

Les retours sont généralement supprimés après leur facturation. Lorsque vous validez une facture, elle est transférée vers la fenêtre **Avoir achat enregistré**. Si vous avez activé la case à cocher **Expédition retour sur avoir** dans la fenêtre **Paramètres achats**, la facture est transférée vers la fenêtre **Expédition retour enregistrée**. Vous pouvez supprimer les documents à l'aide du traitement par lots **Supprimer les retours achat facturés**. Avant de procéder à la suppression, le traitement par lots vérifie que les retours achat ont été entièrement livrés et facturés.  

Les commandes ouvertes achat ne sont pas supprimées une fois que toutes les commandes achat associées ont été traitées et facturées. Vous pouvez supprimer les commandes ouvertes à l'aide du traitement par lots **Supprimer commandes ouvertes achat facturées**.  

Les commandes service facturées sont habituellement supprimées automatiquement après avoir été entièrement facturées. Lors de la validation d'une facture, une écriture correspondante est générée dans la fenêtre **Factures service enreg.**. Vous pouvez afficher le document validé dans la fenêtre **Facture service enreg.**.  

Le programme ne supprime pas la commande service automatiquement cependant, si la quantité totale sur la commande a été validée, non pas à partir de la commande service proprement dite, mais à partir de la fenêtre **Facture service**. Ensuite, il se peut que vous deviez supprimer des commandes facturées qui n'ont pas été supprimées. Pour ce faire, exécutez le traitement par lots **Supprimer commandes service facturées**.  

## <a name="see-also"></a>Voir aussi  
[Configuration et administration dans Finance and Operations, Business edition](admin-setup-and-administration.md)  

