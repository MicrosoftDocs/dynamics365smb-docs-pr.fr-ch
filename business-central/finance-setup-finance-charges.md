---
title: Configurer les conditions intérêts de retard
description: Découvrez comment configurer Business Central afin de pouvoir informer les clients des frais supplémentaires en envoyant des factures d’intérêts.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: aba5ca8eb9425c11c7f8a55a08a153ee18821632
ms.sourcegitcommit: 06bfb3aa59de50d983175e68e681b9d206423242
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672033"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="99198-103">Configurer les conditions intérêts de retard</span><span class="sxs-lookup"><span data-stu-id="99198-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="99198-104">Lorsqu’un client n’effectue pas son paiement à la date d’échéance, des intérêts de retard peuvent être calculés automatiquement et ajoutés aux montants échus sur le compte du client.</span><span class="sxs-lookup"><span data-stu-id="99198-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="99198-105">Vous pouvez informer le client des frais ajoutés en lui envoyant une facture d’intérêts.</span><span class="sxs-lookup"><span data-stu-id="99198-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="99198-106">Mais tout d’abord, vous devez créer un code qui représente un calcul d’intérêts de retard.</span><span class="sxs-lookup"><span data-stu-id="99198-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="99198-107">Vous pouvez ensuite entrer ce code dans le champ Code condition intérêts des fiches client.</span><span class="sxs-lookup"><span data-stu-id="99198-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="99198-108">Conditions intérêts de retard</span><span class="sxs-lookup"><span data-stu-id="99198-108">Finance charge terms</span></span>

<span data-ttu-id="99198-109">Vous devez configurer des conditions intérêts de retard pour chaque calcul de frais financiers, puis affecter les conditions au client dans le champ **Code condition intérêts** sur la page **Client**.</span><span class="sxs-lookup"><span data-stu-id="99198-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="99198-110">Les intérêts de retard peuvent être calculés en utilisant les méthodes du solde journalier moyen ou celles du solde échu.</span><span class="sxs-lookup"><span data-stu-id="99198-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="99198-111">Solde journalier moyen</span><span class="sxs-lookup"><span data-stu-id="99198-111">Average daily balance</span></span>  
  
  <span data-ttu-id="99198-112">Le nombre de jours pendant lequel le paiement est en retard est pris en compte :</span><span class="sxs-lookup"><span data-stu-id="99198-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="99198-113">*Méthode Solde journalier moyen* - *Frais financiers* = *Montant échu* x *(Jours échus/ Période d’intérêts)* x *(Taux d’intérêt/100)*</span><span class="sxs-lookup"><span data-stu-id="99198-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="99198-114">Solde dû</span><span class="sxs-lookup"><span data-stu-id="99198-114">Balance due</span></span>  
  
  <span data-ttu-id="99198-115">La facture d’intérêts représente un pourcentage du montant échu :</span><span class="sxs-lookup"><span data-stu-id="99198-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="99198-116">*Méthode du solde échu* - *Frais financiers* = *Montant échu* x *(Taux d’intérêt / 100)*</span><span class="sxs-lookup"><span data-stu-id="99198-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="99198-117">En outre, chaque condition de la table Conditions intérêts de retard est lié à une autre table, la table Texte intérêts de retard.</span><span class="sxs-lookup"><span data-stu-id="99198-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="99198-118">Pour chaque ensemble de conditions, vous pouvez définir un texte début et un texte fin à inclure dans la facture d’intérêts.</span><span class="sxs-lookup"><span data-stu-id="99198-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="99198-119">Pour configurer des conditions intérêts de retard</span><span class="sxs-lookup"><span data-stu-id="99198-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="99198-120">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Conditions intérêts de retard**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="99198-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="99198-121">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="99198-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="99198-122">Pour utiliser plusieurs combinaisons de conditions intérêts de retard, créez un code pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="99198-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="99198-123">Pour chaque condition intérêts de retard, vous pouvez spécifier des conditions particulières, qui peuvent inclure des frais supplémentaires en devise société (DS) et en devise étrangère.</span><span class="sxs-lookup"><span data-stu-id="99198-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="99198-124">Vous pouvez définir des frais supplémentaires en devise pour chaque condition sur la page **Conditions intérêts de retard**.</span><span class="sxs-lookup"><span data-stu-id="99198-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="99198-125">Sélectionnez l’action **Devises**.</span><span class="sxs-lookup"><span data-stu-id="99198-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="99198-126">Sur la page **Devises condition intérêts**, définissez pour chaque condition un code devise et des frais supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="99198-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="99198-127">Lorsque vous créez des intérêts de retard en devise, les conditions intérêts devise définies ici serviront à créer des factures d’intérêts.</span><span class="sxs-lookup"><span data-stu-id="99198-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="99198-128">Si aucune condition intérêts de retard en devise n’est définie, les conditions intérêts de retard en devise société définies sur la page **Conditions intérêts de retard** seront utilisées, puis converties dans la devise souhaitée.</span><span class="sxs-lookup"><span data-stu-id="99198-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="99198-129">Pour chaque condition intérêts, vous pouvez spécifier le texte à imprimer avant (**Texte début**) ou après (**Texte fin**) les écritures de la facture d’intérêts.</span><span class="sxs-lookup"><span data-stu-id="99198-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="99198-130">Choisissez les actions **Texte de début** ou **Texte de fin** respectivement, puis renseignez la page **Texte intérêts de retard**.</span><span class="sxs-lookup"><span data-stu-id="99198-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="99198-131">Pour insérer automatiquement des valeurs correspondantes dans le texte facture d’intérêts résultant, entrez les espaces réservés suivants dans le champ **Texte**.</span><span class="sxs-lookup"><span data-stu-id="99198-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="99198-132">Paramètre substituable</span><span class="sxs-lookup"><span data-stu-id="99198-132">Placeholder</span></span>|<span data-ttu-id="99198-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="99198-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="99198-134">%1</span><span class="sxs-lookup"><span data-stu-id="99198-134">%1</span></span>|<span data-ttu-id="99198-135">Contenu du champ **Date du document** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99198-136">%2</span><span class="sxs-lookup"><span data-stu-id="99198-136">%2</span></span>|<span data-ttu-id="99198-137">Contenu du champ **Date d’échéance** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99198-138">%3</span><span class="sxs-lookup"><span data-stu-id="99198-138">%3</span></span>|<span data-ttu-id="99198-139">Contenu du champ **Taux d’intérêt** dans les conditions d’intérêts de retard associées</span><span class="sxs-lookup"><span data-stu-id="99198-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="99198-140">%4</span><span class="sxs-lookup"><span data-stu-id="99198-140">%4</span></span>|<span data-ttu-id="99198-141">Contenu du champ **Montant ouvert** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99198-142">%5</span><span class="sxs-lookup"><span data-stu-id="99198-142">%5</span></span>|<span data-ttu-id="99198-143">Contenu du champ **Montant intérêts** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99198-144">%6</span><span class="sxs-lookup"><span data-stu-id="99198-144">%6</span></span>|<span data-ttu-id="99198-145">Contenu du champ **Frais supplémentaires** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99198-146">%7</span><span class="sxs-lookup"><span data-stu-id="99198-146">%7</span></span>|<span data-ttu-id="99198-147">Montant total de la relance</span><span class="sxs-lookup"><span data-stu-id="99198-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="99198-148">%8</span><span class="sxs-lookup"><span data-stu-id="99198-148">%8</span></span>|<span data-ttu-id="99198-149">Contenu du champ **Code devise** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99198-150">%9</span><span class="sxs-lookup"><span data-stu-id="99198-150">%9</span></span>|<span data-ttu-id="99198-151">Contenu du champ **Date comptabilisation** de l’en-tête de facture d’intérêts</span><span class="sxs-lookup"><span data-stu-id="99198-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="99198-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99198-152">See also</span></span>

[<span data-ttu-id="99198-153">Collecte des soldes restants</span><span class="sxs-lookup"><span data-stu-id="99198-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="99198-154">Configurer les conditions et niveaux de relance</span><span class="sxs-lookup"><span data-stu-id="99198-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="99198-155">Configuration de Finance</span><span class="sxs-lookup"><span data-stu-id="99198-155">Setting Up Finance</span></span>](finance-setup-finance.md)  
