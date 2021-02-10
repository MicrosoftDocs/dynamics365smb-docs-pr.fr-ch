---
title: Enregistrer les frais ou des revenus directement dans la comptabilité| Microsoft Docs
description: Pour les activités économiques qui ne sont pas représentés par un document, comme de plus petits frais ou règlements, vous pouvez créer les transactions associées en validant des lignes de feuille sur la page Feuille comptabilité.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72e2851ee60d6cb79f722d12e16ddcb30e95fdbe
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746956"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="bc798-103">Valider les transactions directement vers la comptabilité</span><span class="sxs-lookup"><span data-stu-id="bc798-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="bc798-104">Les feuilles comptabilité vous permettent de valider des transactions financières directement dans les comptes généraux et dans d’autres comptes tels que les comptes bancaires, client, fournisseur et salarié.</span><span class="sxs-lookup"><span data-stu-id="bc798-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="bc798-105">Une utilisation classique de la feuille comptabilité est de valider les dépenses des salariés avec leurs fonds propres au cours des activités commerciales, pour un remboursement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="bc798-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="bc798-106">Pour plus d’informations, voir [Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="bc798-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="bc798-107">Les feuilles comptabilité valident les transactions financières dans les comptes généraux et d’autres comptes tels que les comptes bancaires, clients, fournisseurs et employés.</span><span class="sxs-lookup"><span data-stu-id="bc798-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="bc798-108">La validation avec une feuille comptabilité crée toujours des écritures dans les comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="bc798-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="bc798-109">C’est le cas même lorsque, par exemple, vous validez une ligne feuille dans un compte client, parce qu’une écriture est validée dans un compte client de la comptabilité via un groupe comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="bc798-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="bc798-110">Vous pouvez personnaliser votre version d’une feuille comptabilité en configurant un nom de feuille ou un modèle feuille.</span><span class="sxs-lookup"><span data-stu-id="bc798-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="bc798-111">Pour plus d’informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="bc798-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="bc798-112">Contrairement aux écritures qui sont validées avec des documents qui nécessitent un processus d’avoir, vous pouvez correctement contrepasser les écritures validées avec la feuille comptabilité.</span><span class="sxs-lookup"><span data-stu-id="bc798-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="bc798-113">Pour plus d’informations, voir [Inversion d’une validation feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="bc798-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="bc798-114">Pour valider une transaction directement vers la comptabilité</span><span class="sxs-lookup"><span data-stu-id="bc798-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="bc798-115">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="bc798-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc798-116">Ouvrez la feuille comptabilité appropriée.</span><span class="sxs-lookup"><span data-stu-id="bc798-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="bc798-117">Pour plus d’informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="bc798-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="bc798-118">Sur une nouvelle ligne feuille, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="bc798-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="bc798-119">Répétez l’étape 3 pour toutes les transactions distinctes que vous souhaitez valider.</span><span class="sxs-lookup"><span data-stu-id="bc798-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="bc798-120">Si vous souhaitez saisir les lignes de transaction au-dessus d’une ligne compte contrepartie, par exemple, pour un compte bancaire, activez la case à cocher **Suggérer le montant contrepartie** de la ligne pour votre lot sur la page **Noms feuilles comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="bc798-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="bc798-121">Puis le champ **Montant** de la ligne compte contrepartie est automatiquement prérempli avec la valeur requise pour équilibrer les transactions.</span><span class="sxs-lookup"><span data-stu-id="bc798-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="bc798-122">Choisissez l’action **Valider** pour enregistrer les transactions sur les comptes généraux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bc798-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc798-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc798-123">See Also</span></span>

[<span data-ttu-id="bc798-124">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="bc798-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="bc798-125">Enregistrer et rembourser les frais des employés</span><span class="sxs-lookup"><span data-stu-id="bc798-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="bc798-126">Inversion d’une validation feuille et annuler les réceptions/envois</span><span class="sxs-lookup"><span data-stu-id="bc798-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="bc798-127">Finances</span><span class="sxs-lookup"><span data-stu-id="bc798-127">Finance</span></span>](finance.md)  
<span data-ttu-id="bc798-128">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc798-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
