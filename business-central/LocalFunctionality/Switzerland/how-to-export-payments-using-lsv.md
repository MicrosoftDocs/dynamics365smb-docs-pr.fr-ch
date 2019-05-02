---
title: 'Procédure : Exporter des paiements en mode LSV'
description: Vous pouvez exporter ou écrire des fichiers Lastschrift Verfahren (LSV +) contenant des informations sur les paiements après la fermeture du prélèvement LSV. Vous pouvez envoyer les fichiers générés à la banque sur un disque, ou utiliser un transfert de fichiers électronique tel que votre logiciel de banque en ligne ou un portail Internet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 753b1fb7dcade062228e1d14d5bb9a19ffd0703a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "827283"
---
# <a name="export-payments-using-lsv"></a><span data-ttu-id="14d88-104">Exporter des paiements en mode LSV</span><span class="sxs-lookup"><span data-stu-id="14d88-104">Export Payments Using LSV</span></span>
<span data-ttu-id="14d88-105">Vous pouvez exporter ou écrire des fichiers Lastschrift Verfahren (LSV +) contenant des informations sur les paiements après la fermeture du prélèvement LSV.</span><span class="sxs-lookup"><span data-stu-id="14d88-105">You can export or write Lastschrift Verfahren (LSV+) files that contain payments information after closing the LSV collection.</span></span> <span data-ttu-id="14d88-106">Vous pouvez envoyer les fichiers générés à la banque sur un disque, ou utiliser un transfert de fichiers électronique tel que votre logiciel de banque en ligne ou un portail Internet.</span><span class="sxs-lookup"><span data-stu-id="14d88-106">You can send the generated files to the bank on a disk, or use an electronic file transfer such as your online banking software or an Internet portal.</span></span>  

## <a name="to-export-payments-using-lsv"></a><span data-ttu-id="14d88-107">Pour exporter des paiements en mode LSV</span><span class="sxs-lookup"><span data-stu-id="14d88-107">To export payments using LSV</span></span>  

1.  <span data-ttu-id="14d88-108">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Liste feuilles LSV**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="14d88-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="14d88-109">Dans la page **Liste feuilles LSV**, sélectionnez la feuille LSV nécessaire.</span><span class="sxs-lookup"><span data-stu-id="14d88-109">On the **LSV Journal List** page, select the required LSV journal.</span></span>  
3.  <span data-ttu-id="14d88-110">Choisissez l'action **Écrire le fichier LSV**.</span><span class="sxs-lookup"><span data-stu-id="14d88-110">Choose the **Write LSV File** action.</span></span>  
4.  <span data-ttu-id="14d88-111">Dans la page **Écrire le fichier LSV**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="14d88-111">On the **Write LSV File** page, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="14d88-112">Champ</span><span class="sxs-lookup"><span data-stu-id="14d88-112">Field</span></span>|<span data-ttu-id="14d88-113">Désignation</span><span class="sxs-lookup"><span data-stu-id="14d88-113">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="14d88-114">**N°**</span><span class="sxs-lookup"><span data-stu-id="14d88-114">**No.**</span></span>|<span data-ttu-id="14d88-115">Indiquez le numéro de feuille LSV que vous souhaitez exporter.</span><span class="sxs-lookup"><span data-stu-id="14d88-115">Specify the LSV journal number that you want to export.</span></span>|  
    |<span data-ttu-id="14d88-116">**Test**</span><span class="sxs-lookup"><span data-stu-id="14d88-116">**Test**</span></span>|<span data-ttu-id="14d88-117">Spécifiez si vous envoyez les livraisons test à votre banque.</span><span class="sxs-lookup"><span data-stu-id="14d88-117">Specify if you are sending test deliveries to your bank.</span></span> <span data-ttu-id="14d88-118">La banque ne traite pas de fichier de test.</span><span class="sxs-lookup"><span data-stu-id="14d88-118">The bank does not process test files.</span></span>|  

5.  <span data-ttu-id="14d88-119">Toutes les lignes sont été transférées à la feuille LSV.</span><span class="sxs-lookup"><span data-stu-id="14d88-119">All related lines are transferred to the LSV journal.</span></span> <span data-ttu-id="14d88-120">Le fichier LSV est généré dans le dossier prédéterminé.</span><span class="sxs-lookup"><span data-stu-id="14d88-120">The LSV file is generated in the predetermined folder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="14d88-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14d88-121">See Also</span></span>  
 <span data-ttu-id="14d88-122">[Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="14d88-122">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="14d88-123">[Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="14d88-123">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="14d88-124">[Fermer prélèvement LSV](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="14d88-124">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 [<span data-ttu-id="14d88-125">Valider les paiements LSV+</span><span class="sxs-lookup"><span data-stu-id="14d88-125">Post LSV+ Payments</span></span>](how-to-post-lsv-payments.md)