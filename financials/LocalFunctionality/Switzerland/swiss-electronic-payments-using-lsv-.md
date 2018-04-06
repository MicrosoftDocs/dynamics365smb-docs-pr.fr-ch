---
title: "Paiements électroniques à l'aide de LSV+, Suisse"
description: "La méthode de paiement électronique Lastschrift Verfahren (LSV+) (ou par prélèvement), version améliorée de LSV, permet aux entreprises de récupérer les paiements directement à partir des comptes bancaires de leurs clients. Pour récupérer les paiements clients, vous devez envoyer un fichier LSV à la banque afin que celle-ci prenne en compte les paiements requis dans le fichier."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6dd44e11baa7a834081e215f21a53db089f47c4b
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="swiss-electronic-payments-using-lsv"></a>Paiements électroniques à l'aide de LSV+, Suisse
La méthode de paiement électronique Lastschrift Verfahren (LSV+) (ou par prélèvement), version améliorée de LSV, permet aux entreprises de récupérer les paiements directement à partir des comptes bancaires de leurs clients. Pour récupérer les paiements clients, vous devez envoyer un fichier LSV à la banque afin que celle-ci prenne en compte les paiements requis dans le fichier.  

La méthode LSV+ est un principe de prélèvement avec un droit d'opposition. Business Direct Debit (BDD) est un système de prélèvement sans droit d'opposition. Le format de fichier à envoyer à la banque est le même pour LSV+ et BDD.  

Avant d'utiliser le module LSV, vous devez définir des paramètres dans la fenêtre **Configuration de LSV**.

## <a name="automatic-esr-processing"></a>Traitement ESR automatique  
Vous pouvez télécharger des transactions de crédit de paiement au format de fichier ESR (Einzahlungsschein mit Referenznummer) de la banque. Vous pouvez recevoir des paiements LSV traités dans le fichier ESR si le numéro de référence ESR est intégré au système LSV+. Si des paiements LSV+ sont inclus dans vos fichiers LSV importés, les lignes de journal LSV associées sont automatiquement fermées. Le traitement ESR automatique est uniquement effectué pour les paiements utilisant des francs suisses (CHF) et nécessite que vous procédiez comme suit :  

- Après avoir envoyé le fichier LSV+ à la banque, soumettez un rapport de paiement dans les trois jours ouvrables suivant la date de traitement LSV demandée.  

- Importez les fichiers ESR et validez les feuilles ESR. Si une transaction ESR importée est liée à une ligne règlement ouverte LSV+, la ligne feuille LSV appropriée est automatiquement fermée par ESR.  

    > [!NOTE]  
    >  En important un fichier ESR, la ligne feuille LSV est clôturée par ESR si la feuille LSV appropriée est disponible, quelle que soit la nature de la transaction ESR.  

- Après la date de traitement LSV, vous pouvez vérifier les lignes feuille LSV. Si toutes les lignes feuille LSV sont fermées, le statut du champ **Statut LSV** passe à **Terminé**.  

## <a name="see-also"></a>Voir aussi  
 [Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md)   
 [Fermer prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Valider des paiements LSV+](how-to-post-lsv-payments.md)   
 [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md)   
 [Paiements électroniques, Suisse](swiss-electronic-payments.md)   
 [Paiements électroniques à l'aide de ESR+, Suisse](swiss-electronic-payments-using-esr.md)   
 [Effectuer des paiements](../../payables-make-payments.md)

