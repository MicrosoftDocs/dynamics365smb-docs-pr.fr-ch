---
title: Paiements électroniques à l'aide de LSV+, Suisse
description: La méthode de paiement électronique Lastschrift Verfahren (LSV+) (ou par prélèvement), version améliorée de LSV, permet aux entreprises de récupérer les paiements directement à partir des comptes bancaires de leurs clients. Pour récupérer les paiements clients, vous devez envoyer un fichier LSV à la banque afin que celle-ci prenne en compte les paiements requis dans le fichier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e24ecdcaf32662f38bd2e192f29c23e5f01cb28d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382002"
---
# <a name="swiss-electronic-payments-using-lsv"></a><span data-ttu-id="a966f-104">Paiements électroniques à l'aide de LSV+, Suisse</span><span class="sxs-lookup"><span data-stu-id="a966f-104">Swiss Electronic Payments Using LSV+</span></span>
<span data-ttu-id="a966f-105">La méthode de paiement électronique Lastschrift Verfahren (LSV+) (ou par prélèvement), version améliorée de LSV, permet aux entreprises de récupérer les paiements directement à partir des comptes bancaires de leurs clients.</span><span class="sxs-lookup"><span data-stu-id="a966f-105">The Lastschrift Verfahren (LSV+)—or direct debit—electronic payment method, an improved version of LSV, allows companies to retrieve payments directly from its customers’ bank accounts.</span></span> <span data-ttu-id="a966f-106">Pour récupérer les paiements clients, vous devez envoyer un fichier LSV à la banque afin que celle-ci prenne en compte les paiements requis dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="a966f-106">To retrieve customer payments, you must send an LSV file to the bank, and the bank will collect the payments requested in the file.</span></span>  

<span data-ttu-id="a966f-107">La méthode LSV+ est un principe de prélèvement avec un droit d'opposition.</span><span class="sxs-lookup"><span data-stu-id="a966f-107">The LSV+ method is a direct debit principle with right of objection.</span></span> <span data-ttu-id="a966f-108">Business Direct Debit (BDD) est un système de prélèvement sans droit d'opposition.</span><span class="sxs-lookup"><span data-stu-id="a966f-108">Business Direct Debit (BDD) is a direct debit system without right of objection.</span></span> <span data-ttu-id="a966f-109">Le format de fichier à envoyer à la banque est le même pour LSV+ et BDD.</span><span class="sxs-lookup"><span data-stu-id="a966f-109">The file format to be sent to the bank is the same for LSV+ and BDD.</span></span>  

<span data-ttu-id="a966f-110">Avant d'utiliser le module LSV, vous devez définir des paramètres dans la page **Configuration de LSV**.</span><span class="sxs-lookup"><span data-stu-id="a966f-110">Before using the LSV module, you must define the settings on the **LSV Setup** page.</span></span>

## <a name="automatic-esr-processing"></a><span data-ttu-id="a966f-111">Traitement ESR automatique</span><span class="sxs-lookup"><span data-stu-id="a966f-111">Automatic ESR Processing</span></span>  
<span data-ttu-id="a966f-112">Vous pouvez télécharger des transactions de crédit de paiement au format de fichier ESR (Einzahlungsschein mit Referenznummer) de la banque.</span><span class="sxs-lookup"><span data-stu-id="a966f-112">You can download payment credit transactions in Einzahlungsschein mit Referenznummer (ESR) file format from the bank.</span></span> <span data-ttu-id="a966f-113">Vous pouvez recevoir des paiements LSV traités dans le fichier ESR si le numéro de référence ESR est intégré au système LSV+.</span><span class="sxs-lookup"><span data-stu-id="a966f-113">You can receive processed LSV payments in the ESR file if the ESR reference number is integrated with the LSV+ system.</span></span> <span data-ttu-id="a966f-114">Si des paiements LSV+ sont inclus dans vos fichiers LSV importés, les lignes de journal LSV associées sont automatiquement fermées.</span><span class="sxs-lookup"><span data-stu-id="a966f-114">If LSV+ payments are included in your imported LSV files, the related LSV journal lines are closed automatically.</span></span> <span data-ttu-id="a966f-115">Le traitement ESR automatique est uniquement effectué pour les paiements utilisant des francs suisses (CHF) et nécessite que vous procédiez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a966f-115">Automatic ESR processing is performed only for payments that use Swiss Francs (CHF), and requires that you do the following:</span></span>  

- <span data-ttu-id="a966f-116">Après avoir envoyé le fichier LSV+ à la banque, soumettez un rapport de paiement dans les trois jours ouvrables suivant la date de traitement LSV demandée.</span><span class="sxs-lookup"><span data-stu-id="a966f-116">After you have sent the LSV+ file to the bank, submit a payments report within three business days following the requested LSV processing date.</span></span>  

- <span data-ttu-id="a966f-117">Importez les fichiers ESR et validez les feuilles ESR.</span><span class="sxs-lookup"><span data-stu-id="a966f-117">Import the ESR files, and post the ESR journals.</span></span> <span data-ttu-id="a966f-118">Si une transaction ESR importée est liée à une ligne règlement ouverte LSV+, la ligne feuille LSV appropriée est automatiquement fermée par ESR.</span><span class="sxs-lookup"><span data-stu-id="a966f-118">If an imported ESR transaction is related to an open LSV+ payment line, then the appropriate LSV journal line is automatically closed by ESR.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a966f-119">En important un fichier ESR, la ligne feuille LSV est clôturée par ESR si la feuille LSV appropriée est disponible, quelle que soit la nature de la transaction ESR.</span><span class="sxs-lookup"><span data-stu-id="a966f-119">When importing an ESR file, the LSV journal line is closed by ESR if the appropriate LSV journal is found, regardless of the ESR transaction type.</span></span>  

- <span data-ttu-id="a966f-120">Après la date de traitement LSV, vous pouvez vérifier les lignes feuille LSV.</span><span class="sxs-lookup"><span data-stu-id="a966f-120">After the LSV processing date, you can check the LSV journal lines.</span></span> <span data-ttu-id="a966f-121">Si toutes les lignes feuille LSV sont fermées, le statut du champ **Statut LSV** passe à **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="a966f-121">If all of the LSV journal lines are closed, then the status of the **LSV Status** field is updated to  **Finished**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a966f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a966f-122">See Also</span></span>  
 <span data-ttu-id="a966f-123">[Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="a966f-123">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="a966f-124">[Fermer prélèvement LSV](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="a966f-124">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="a966f-125">[Valider des paiements LSV+](how-to-post-lsv-payments.md) </span><span class="sxs-lookup"><span data-stu-id="a966f-125">[Post LSV+ Payments](how-to-post-lsv-payments.md) </span></span>  
 <span data-ttu-id="a966f-126">[Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md) </span><span class="sxs-lookup"><span data-stu-id="a966f-126">[Export Payments Using LSV](how-to-export-payments-using-lsv.md) </span></span>  
 <span data-ttu-id="a966f-127">[Paiements électroniques, Suisse](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="a966f-127">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 <span data-ttu-id="a966f-128">[Paiements électroniques à l'aide de ESR+, Suisse](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="a966f-128">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 [<span data-ttu-id="a966f-129">Effectuer des paiements</span><span class="sxs-lookup"><span data-stu-id="a966f-129">Making Payments</span></span>](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]