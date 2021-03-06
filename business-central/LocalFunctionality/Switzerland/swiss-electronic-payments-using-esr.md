---
title: Paiements électroniques à l'aide de ESR+, Suisse
description: La méthode de paiement électronique Einzahlungsschein mit Referenznummer (ESR) est un service de prélèvement électronique qui permet au client de facturer les factures ouvertes en francs suisses (CHF) et en euros (EUR), et de comptabiliser efficacement les paiements entrants.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9e3faf54e5c54dce99dd6bc33b6dc85e7d1ad184
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774707"
---
# <a name="swiss-electronic-payments-using-esr"></a>Paiements électroniques à l'aide de ESR+, Suisse
La méthode de paiement électronique Einzahlungsschein mit Referenznummer (ESR) est un service de prélèvement électronique qui permet au client de facturer les factures ouvertes en francs suisses (CHF) et en euros (EUR), et de comptabiliser efficacement les paiements entrants. Le numéro de référence, ou la ligne de code, contient toutes les données de comptabilité pertinentes.  

Avec les paiements électroniques ESR, vous pouvez effectuer les opérations suivantes :  

- Envoyez les bordereaux de paiement ESR avec des numéros de référence uniques sur les factures. En raison des numéros de référence ESR uniques, les paiements pour règlement sont automatiquement appliqués aux factures correspondantes. Pour plus d'informations, reportez-vous à [Imprimer des factures ESR](how-to-print-esr-invoices.md).  

- Téléchargez quotidiennement les fichiers ESR de la banque. Les fichiers contiennent des informations sur toutes les factures payées.  

- Importez les fichiers ESR et créez des lignes de paiement automatiquement pour chaque paiement. Pour plus d'informations, reportez-vous à [Importer des paiements ESR](how-to-import-esr-payments.md).  

> [!NOTE]  
>  Avant de pouvoir utiliser le module ESR, vous devez configurer la banque, le compte bancaire et le nom de fichier. Vous devez également spécifier si ESR ou ESR+ doit être utilisé.

Lorsque vous avez évalué les informations de configuration, vous pouvez ajuster le formulaire de facture et créer une série de tests que vous pouvez demander à votre banque ou à votre service postal de valider.  

Lorsque vous configurez des souches de numéros pour les factures, vous devez suivre les instructions suivantes :  

- Utilisez un maximum de huit chiffres.  
- Utilisez uniquement des caractères numériques.  
- Ne précédez pas les nombres de zéros.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques, Suisse](swiss-electronic-payments.md)   
 [Imprimer des factures ESR](how-to-print-esr-invoices.md)   
 [Importation de paiements ESR](how-to-import-esr-payments.md)   
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Effectuer des paiements](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]