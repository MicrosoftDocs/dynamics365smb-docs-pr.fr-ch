---
title: "Personnaliser les signaux visuels à propos de l'activité d'une pile | Microsoft Docs"
description: "Configurez un indicateur en couleur sur une vignette de la pile pour fournir un signal visuel personnalisé de l'activité de la pile."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e4ceaeae1a37a521d2d5bd22ab711757283e6321
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="82091-103">Configurer un indicateur coloré sur des piles</span><span class="sxs-lookup"><span data-stu-id="82091-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="82091-104">Vous pouvez configurer des piles qui apparaissent sur le Tableau de bord pour inclure un indicateur qui modifie la couleur en fonction des valeurs de données dans les piles.</span><span class="sxs-lookup"><span data-stu-id="82091-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="82091-105">L'indicateur apparait sous forme d'une barre de couleur le long de la bordure supérieure de la mosaïque Pile.</span><span class="sxs-lookup"><span data-stu-id="82091-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="82091-106">Il offre un signal visuel du statut de l'activité de la pile, ce qui peut indiquer des conditions favorables ou défavorables pour inviter l'utilisateur à prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="82091-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="82091-107">Par exemple, si une pile affiche les factures vente en cours, vous pouvez définir l'indicateur pour qu'il apparaisse vert (favorable) lorsque le nombre total des factures vente en cours est inférieur à 10, et apparaisse rouge (défavorable) lorsque le total est supérieur à 20.</span><span class="sxs-lookup"><span data-stu-id="82091-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="82091-108">Dans la fenêtre **Paramètres pile**, vous configurez des indicateurs pour toutes les piles disponibles dans la base de données de la société.</span><span class="sxs-lookup"><span data-stu-id="82091-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="82091-109">Pour configurer l'indicateur, vous pouvez spécifier jusqu'à deux valeurs de seuil qui définissent trois plages de valeurs de données (basse, moyenne et haute) à laquelle vous pouvez appliquer une couleur différente (ou un style différent).</span><span class="sxs-lookup"><span data-stu-id="82091-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="82091-110">Pour paramétrer des indicateurs colorés sur des piles</span><span class="sxs-lookup"><span data-stu-id="82091-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="82091-111">Sous **Activités** sur votre page Tableau de bord, sélectionnez **Paramétrer piles**.</span><span class="sxs-lookup"><span data-stu-id="82091-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="82091-112">La fenêtre **Paramètres pile** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="82091-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="82091-113">La fenêtre répertorie les indicateurs actuellement paramétrés sur des piles.</span><span class="sxs-lookup"><span data-stu-id="82091-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="82091-114">Pour modifier un indicateur, modifiez les champs et modifiez, par exemple, les valeurs pour des seuils différents.</span><span class="sxs-lookup"><span data-stu-id="82091-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="82091-115">Le tableau suivant répertorie les couleurs correspondant aux options des champs **Style bas de gamme**, **Style milieu de gamme** et **Style haut de gamme**.</span><span class="sxs-lookup"><span data-stu-id="82091-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="82091-116">Option</span><span class="sxs-lookup"><span data-stu-id="82091-116">Option</span></span> | <span data-ttu-id="82091-117">Couleur</span><span class="sxs-lookup"><span data-stu-id="82091-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="82091-118">**Aucun**</span><span class="sxs-lookup"><span data-stu-id="82091-118">**None**</span></span> |<span data-ttu-id="82091-119">Aucune couleur (même couleur que la mosaïque Pile)</span><span class="sxs-lookup"><span data-stu-id="82091-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="82091-120">**Favorable**</span><span class="sxs-lookup"><span data-stu-id="82091-120">**Favorable**</span></span> |<span data-ttu-id="82091-121">Vert</span><span class="sxs-lookup"><span data-stu-id="82091-121">Green</span></span> |
| <span data-ttu-id="82091-122">**Défavorable**</span><span class="sxs-lookup"><span data-stu-id="82091-122">**Unfavorable**</span></span> |<span data-ttu-id="82091-123">Rouge</span><span class="sxs-lookup"><span data-stu-id="82091-123">Red</span></span> |
| <span data-ttu-id="82091-124">**Ambigu**</span><span class="sxs-lookup"><span data-stu-id="82091-124">**Ambiguous**</span></span> |<span data-ttu-id="82091-125">Jaune</span><span class="sxs-lookup"><span data-stu-id="82091-125">Yellow</span></span> |
| <span data-ttu-id="82091-126">**Subordonné**</span><span class="sxs-lookup"><span data-stu-id="82091-126">**Subordinate**</span></span> |<span data-ttu-id="82091-127">Gris</span><span class="sxs-lookup"><span data-stu-id="82091-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="82091-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82091-128">See Also</span></span>
<span data-ttu-id="82091-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82091-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

