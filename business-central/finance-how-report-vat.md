---
title: Envoyer les déclarations de TVA destinées à l'administration fiscale | Microsoft Docs
description: Apprendre à préparer les déclarations qui répertorient la TVA des ventes au cours d'une période, ou à partir des ventes et achats, et envoyer la déclaration à l'administration fiscale.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 729524ce2145b4e167fb49671045b298affb862b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820976"
---
# <a name="how-to-report-vat-to-a-tax-authority"></a><span data-ttu-id="4d017-103">Procédure : Déclarer la TVA à l’administration fiscale</span><span class="sxs-lookup"><span data-stu-id="4d017-103">How To: Report VAT to a Tax Authority</span></span>
<span data-ttu-id="4d017-104">Cette rubrique décrit les états dans [!INCLUDE[d365fin](includes/d365fin_md.md)] que vous pouvez utiliser pour envoyer des informations sur les montants de la taxe sur la valeur ajoutée (TVA) relatifs aux ventes et achats à l'administration fiscale de votre région.</span><span class="sxs-lookup"><span data-stu-id="4d017-104">This topic describes the reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] that you can use to submit information about value-added tax (VAT) amounts for sales and purchases to tax authorities in your region.</span></span>

<span data-ttu-id="4d017-105">Vous pouvez utiliser les états suivants :</span><span class="sxs-lookup"><span data-stu-id="4d017-105">You can use the following reports :</span></span>

* <span data-ttu-id="4d017-106">La déclaration de liste de vente de l'Union européenne (EU) **Liste des ventes UE** répertorie les montants de la taxe sur la valeur ajoutée (TVA) que vous avez collectés pour les ventes aux clients enregistrés dans les pays de l'Union européenne (UE).</span><span class="sxs-lookup"><span data-stu-id="4d017-106">The **EC Sales List** European Community (EC) Sales List report lists the value added tax (VAT) amounts that you have collected for sales to VAT-registered customers in the European Union (EU) countries.</span></span>  
* <span data-ttu-id="4d017-107">L'état **Retour TVA** inclut la TVA pour les ventes et les achats aux clients dans tous les pays utilisant la TVA.</span><span class="sxs-lookup"><span data-stu-id="4d017-107">The **VAT Return** report includes VAT for sales and purchases to customers in all countries that use VAT.</span></span>

<span data-ttu-id="4d017-108">Si vous souhaitez afficher un historique complet des écritures TVA, chaque validation impliquant la TVA crée une écriture dans la page **Écritures TVA**.</span><span class="sxs-lookup"><span data-stu-id="4d017-108">If you want to view a complete history of VAT entries, every posting that involves VAT creates an entry on the **VAT Entries** page.</span></span> <span data-ttu-id="4d017-109">Ces écritures sont utilisées pour calculer le montant de votre déclaration TVA, tel que paiement et remboursement, pour une période donnée.</span><span class="sxs-lookup"><span data-stu-id="4d017-109">These entries are used to calculate your VAT settlement amount, such as your payment and refund, for a specific period.</span></span> <span data-ttu-id="4d017-110">Pour afficher les écritures TVA, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Écritures TVA**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4d017-110">To view VAT entries, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Entries**, and then choose the related link.</span></span>

## <a name="about-the-ec-sales-list-report"></a><span data-ttu-id="4d017-111">À propos de l'état Liste des ventes UE</span><span class="sxs-lookup"><span data-stu-id="4d017-111">About the EC Sales List report</span></span>
<span data-ttu-id="4d017-112">Au Royaume-Uni, toutes les sociétés qui vendent des biens et des services aux clients enregistrés pour la TVA, y compris les clients dans d'autres pays de l'Union européenne (UE), doivent envoyer une version électronique de l'état Liste des ventes de la Communauté européenne (CE) au format XML sur le site Web du service de la fiscalité et des douanes du Royaume-Uni.</span><span class="sxs-lookup"><span data-stu-id="4d017-112">In the UK, all companies that sell goods and services to VAT-registered customers, including customers in other European Union (EU) countries, must submit an electronic version of the European Community (EC) Sales List report in XML format through Her Majesty's Revenue and Customs (HMRC) website.</span></span> <span data-ttu-id="4d017-113">La liste des ventes de l'Union européenne ne fonctionne que pour les pays de l'UE.</span><span class="sxs-lookup"><span data-stu-id="4d017-113">The EC Sales List report works only for countries in the EU.</span></span>

<span data-ttu-id="4d017-114">La déclaration comprend une ligne pour chaque type de transaction avec le client, et affiche le montant total pour chaque type de transaction.</span><span class="sxs-lookup"><span data-stu-id="4d017-114">The report includes one line for each type of transaction with the customer, and displays the total amount for each type of transactions.</span></span> <span data-ttu-id="4d017-115">La déclaration peut inclure trois types de transactions :</span><span class="sxs-lookup"><span data-stu-id="4d017-115">There are three types of transactions that the report can include:</span></span>  

* <span data-ttu-id="4d017-116">Marchandises B2B</span><span class="sxs-lookup"><span data-stu-id="4d017-116">B2B Goods</span></span>  
* <span data-ttu-id="4d017-117">Services B2B</span><span class="sxs-lookup"><span data-stu-id="4d017-117">B2B Services</span></span>  
* <span data-ttu-id="4d017-118">Marchandises triangulées B2B</span><span class="sxs-lookup"><span data-stu-id="4d017-118">B2B Triangulated Goods</span></span>  

<span data-ttu-id="4d017-119">Les biens et des services B2B indiquent si vous avez vendu un bien ou un service, et sont contrôlés par le paramètre **Service UE** des paramètres validation TVA.</span><span class="sxs-lookup"><span data-stu-id="4d017-119">B2B goods and services specify whether you sold a good or a service, and are controlled by the **EU Service** setting in the VAT posting setup.</span></span> <span data-ttu-id="4d017-120">Les marchandises triangulées B2B indiquent si vous vous êtes engagé dans des transactions avec un tiers, et sont contrôlées par le paramètre **Trans. tripartite UE** sur les documents vente, comme des commandes vente, des factures, des avoirs, etc.</span><span class="sxs-lookup"><span data-stu-id="4d017-120">B2B Triangulated Goods indicate whether you engaged in trade with a 3rd party, and are controlled by the **EU 3-Party Trade** setting on sales documents, such as sales orders, invoices, credit memos, and so on.</span></span>  

<span data-ttu-id="4d017-121">Une fois que l'administration fiscale aura examiné votre état, elle devra envoyer un e-mail au contact de votre société.</span><span class="sxs-lookup"><span data-stu-id="4d017-121">After the tax authority reviews your report, they will send an email to the contact person for your company.</span></span> <span data-ttu-id="4d017-122">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], le contact est spécifié sur la page **Informations société**.</span><span class="sxs-lookup"><span data-stu-id="4d017-122">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the contact person is specified on the **Company Information** page.</span></span> <span data-ttu-id="4d017-123">Avant de soumettre l'état, assurez-vous qu'un contact est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4d017-123">Before you submit the report, make sure that a contact person is chosen.</span></span>

## <a name="about-the-vat-return-report"></a><span data-ttu-id="4d017-124">À propos de l'état Retour TVA</span><span class="sxs-lookup"><span data-stu-id="4d017-124">About the VAT Return report</span></span>
<span data-ttu-id="4d017-125">Utilisez cet état pour envoyer les documents relatifs à la TVA sur les ventes et les achats, tels que les commandes d'achat et de vente, les factures et les avoirs.</span><span class="sxs-lookup"><span data-stu-id="4d017-125">Use this report to submit VAT for sales and purchase documents, such as purchase and sales orders, invoices, and credit memos.</span></span> <span data-ttu-id="4d017-126">Les informations contenues dans l'état sont au même format que dans la déclaration de l'administration fiscale et douanière.</span><span class="sxs-lookup"><span data-stu-id="4d017-126">The information in the report is in the same format as on the declaration form from the customs and tax authorities.</span></span>  

<span data-ttu-id="4d017-127">La TVA est calculée sur la base des paramètres validation TVA et des groupes comptabilisation TVA que vous avez définis.</span><span class="sxs-lookup"><span data-stu-id="4d017-127">VAT is calculated based on the VAT posting setup and the VAT posting groups that you have set up.</span></span>

<span data-ttu-id="4d017-128">Pour le retour TVA, vous pouvez spécifier les écritures pour :</span><span class="sxs-lookup"><span data-stu-id="4d017-128">For the VAT return, you can specify the entries to include:</span></span>

* <span data-ttu-id="4d017-129">Envoyer les transactions ouvertes uniquement, ou ouvertes et clôturées.</span><span class="sxs-lookup"><span data-stu-id="4d017-129">Submit open transactions only, or open and closed.</span></span> <span data-ttu-id="4d017-130">Par exemple, cela est utile lorsque vous préparez votre retour TVA annuel final.</span><span class="sxs-lookup"><span data-stu-id="4d017-130">For example, this is useful when you prepare your final annual VAT return.</span></span>
* <span data-ttu-id="4d017-131">Envoyer uniquement les écritures des périodes définies, ou inclure également les écritures des périodes précédentes.</span><span class="sxs-lookup"><span data-stu-id="4d017-131">Submit only entries from the specified periods, or also include entries from previous periods.</span></span> <span data-ttu-id="4d017-132">Cette fonction est utile pour mettre à jour un retour TVA déjà envoyé, par exemple, si un fournisseur vous envoie une facture échue.</span><span class="sxs-lookup"><span data-stu-id="4d017-132">This is useful for updating a VAT return that you have already submitted, for example, if a vendor sends you a late invoice.</span></span>    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a><span data-ttu-id="4d017-133">Pour vous connecter au service Web de votre administration fiscale</span><span class="sxs-lookup"><span data-stu-id="4d017-133">To connect to your tax authority's web service</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="4d017-134">fournit des connexions de service à des sites Web d'administrations fiscales.</span><span class="sxs-lookup"><span data-stu-id="4d017-134">provides service connections to tax authority websites.</span></span> <span data-ttu-id="4d017-135">Par exemple, si vous vous trouvez au Royaume-uni, vous pouvez activer la connexion de service **GovTalk** pour envoyer la liste des ventes UE et les états de retour TVA par voie électronique.</span><span class="sxs-lookup"><span data-stu-id="4d017-135">For example, if you are in the UK, you can enable the **GovTalk** service connection to submit the EC Sales List and VAT Return reports electronically.</span></span> <span data-ttu-id="4d017-136">Si vous souhaitez envoyer l'état manuellement, par exemple en saisissant vos données sur le site Web de l'administration fiscale, cela n'est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4d017-136">If you want to submit the report manually, for example by entering your data on the tax authority's website, this is not required.</span></span>   

<span data-ttu-id="4d017-137">Pour déclarer la TVA à une administration par voie électronique, vous devez connecter [!INCLUDE[d365fin](includes/d365fin_md.md)] au service Web de l'administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-137">To report VAT to a tax authority electronically, you need to connect [!INCLUDE[d365fin](includes/d365fin_md.md)] to the tax authority's web service.</span></span> <span data-ttu-id="4d017-138">Cela suppose que vous configuriez un compte avec votre administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-138">This requires that you set up an account with your tax authority.</span></span> <span data-ttu-id="4d017-139">Lorsque vous avez un compte, vous pouvez activer une connexion de service que nous fournissons dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4d017-139">When you have an account, you can enable a service connection that we provide in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="4d017-140">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Connexions au service**, puis sélectionnez le lien approprié.</span><span class="sxs-lookup"><span data-stu-id="4d017-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Connections**, and then choose appropriate link.</span></span>
2. <span data-ttu-id="4d017-141">Renseignez les champs requis.</span><span class="sxs-lookup"><span data-stu-id="4d017-141">Fill in the required fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   <span data-ttu-id="4d017-142">Il est judicieux de tester votre connexion.</span><span class="sxs-lookup"><span data-stu-id="4d017-142">It's a good idea to test your connection.</span></span> <span data-ttu-id="4d017-143">Pour cela, choisissez la case à cocher **Mode test**, puis préparez et envoyez votre état TVA comme décrit dans la section _Préparer et envoyer un état TVA_.</span><span class="sxs-lookup"><span data-stu-id="4d017-143">To do this, choose the **Test Mode** check box, then prepare and submit your VAT report as described in the _To prepare and submit a VAT report_ section.</span></span> <span data-ttu-id="4d017-144">En mode Test, le service vérifie si l'administration fiscale peut recevoir votre état, et le statut de l'état indiquera si l'envoi du test a réussi.</span><span class="sxs-lookup"><span data-stu-id="4d017-144">While in Test Mode, the service tests whether the tax authority can receive your report, and the status of the report will indicate whether the test submission was successful.</span></span> <span data-ttu-id="4d017-145">Il est important de retenir que ce n'est pas un envoi réel.</span><span class="sxs-lookup"><span data-stu-id="4d017-145">It's important to remember that this is not an actual submission.</span></span> <span data-ttu-id="4d017-146">Pour réellement envoyer l'état, vous devez désactiver la case à cocher **Mode test**, puis répéter le processus d'envoi.</span><span class="sxs-lookup"><span data-stu-id="4d017-146">To submit the report for real, you must clear the **Test Mode** check box, and then repeat the submission process.</span></span>

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a><span data-ttu-id="4d017-147">Pour configurer les états TVA dans [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="4d017-147">To set up VAT reports in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="4d017-148">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramétrage déclaration TVA**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4d017-148">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Report Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4d017-149">Pour laisser des utilisateurs modifier et retourner cet état, sélectionnez la case à cocher **Modifier les états soumis**.</span><span class="sxs-lookup"><span data-stu-id="4d017-149">To let users change and resubmit this report, choose the **Modify Submitted Reports** check box.</span></span>  
3. <span data-ttu-id="4d017-150">Choisissez la souche de numéros à utiliser pour chaque état.</span><span class="sxs-lookup"><span data-stu-id="4d017-150">Choose the number series to use for each report.</span></span>  

## <a name="to-prepare-and-submit-a-vat-report"></a><span data-ttu-id="4d017-151">Pour préparer et soumettre un état TVA</span><span class="sxs-lookup"><span data-stu-id="4d017-151">To prepare and submit a VAT report</span></span>
1. <span data-ttu-id="4d017-152">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste des ventes UE** ou **Retour TVA**, et sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4d017-152">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **EC Sales List** or **VAT Return**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4d017-153">Sélectionnez **Nouveau**, puis renseignez les champs requis.</span><span class="sxs-lookup"><span data-stu-id="4d017-153">Choose **New**, and then fill in the required fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4d017-154">Pour générer le contenu de l'état, sélectionnez l'action **Proposer lignes**.</span><span class="sxs-lookup"><span data-stu-id="4d017-154">To generate the content of the report, choose the **Suggest Lines** action.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="4d017-155">Pour l'état Liste des ventes UE, vous pouvez consulter les transactions incluses dans les lignes de l'état avant d'envoyer l'état.</span><span class="sxs-lookup"><span data-stu-id="4d017-155">For the EC Sales List report, you can review the transactions included in the report lines before you submit the report.</span></span> <span data-ttu-id="4d017-156">Pour cela, sélectionnez la ligne, puis cliquez sur l'action **Afficher écritures TVA**.</span><span class="sxs-lookup"><span data-stu-id="4d017-156">To do that, choose the line, and then choose the **Show VAT Entries** action.</span></span>  
4. <span data-ttu-id="4d017-157">Pour valider et préparer l'état pour l'envoi, choisissez l'action **Emettre**.</span><span class="sxs-lookup"><span data-stu-id="4d017-157">To validate and prepare the report for submission, choose the **Release** action.</span></span>  

    > [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="4d017-158">confirme que l'état est configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="4d017-158">validates whether the report is set up correctly.</span></span> <span data-ttu-id="4d017-159">Si la validation échoue, les erreurs sont affichées sous **Erreurs et avertissements**, de sorte que vous sachiez quoi corriger.</span><span class="sxs-lookup"><span data-stu-id="4d017-159">If the validation fails, the errors display under **Errors and Warnings** so that you know what to fix.</span></span> <span data-ttu-id="4d017-160">Généralement, si le message concerne un paramètre manquant dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez cliquer sur le message pour ouvrir la page contenant les informations à corriger.</span><span class="sxs-lookup"><span data-stu-id="4d017-160">Typically, if the message is about a missing setting in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can click the message to open the page that contains the information to correct.</span></span>  
5. <span data-ttu-id="4d017-161">Pour envoyer l'état, sélectionnez l'action **Soumettre**.</span><span class="sxs-lookup"><span data-stu-id="4d017-161">To submit the report, choose the **Submit** action.</span></span>  

<span data-ttu-id="4d017-162">Une fois que vous envoyez la déclaration, [!INCLUDE[d365fin](includes/d365fin_md.md)] surveille le service et conserve un enregistrement de vos communications.</span><span class="sxs-lookup"><span data-stu-id="4d017-162">After you submit the report, [!INCLUDE[d365fin](includes/d365fin_md.md)] monitors the service and keeps a record of your communications.</span></span> <span data-ttu-id="4d017-163">Le champ **Statut** indique l'état de la déclaration en cours.</span><span class="sxs-lookup"><span data-stu-id="4d017-163">The **Status** field indicates where the report is in the process.</span></span> <span data-ttu-id="4d017-164">Par exemple, lorsque l'administration traite votre déclaration, le statut de celle-ci passe à **Réussie**.</span><span class="sxs-lookup"><span data-stu-id="4d017-164">For example, when the authorities process your report, the status of the report changes to **Succeeded**.</span></span> <span data-ttu-id="4d017-165">Si l'administration fiscale trouve des erreurs dans la déclaration que vous avez envoyée, le statut de celle-ci est **Échec**.</span><span class="sxs-lookup"><span data-stu-id="4d017-165">If the tax authority found mistakes in the report you submitted, the status of the report will be **Failed**.</span></span> <span data-ttu-id="4d017-166">Vous pouvez afficher les erreurs sous **Erreurs et avertissements**, corrigez-les, puis envoyez la déclaration.</span><span class="sxs-lookup"><span data-stu-id="4d017-166">You can view the errors under **Errors and Warnings**, correct them, and then submit the report again.</span></span> <span data-ttu-id="4d017-167">Pour visualiser une liste de toutes vos déclarations de liste des ventes UE, consultez la page **États de liste des ventes UE**.</span><span class="sxs-lookup"><span data-stu-id="4d017-167">To view a list of all your EC Sales List reports, go to the **EC Sales List Reports** page.</span></span>  

## <a name="viewing-communications-with-your-tax-authority"></a><span data-ttu-id="4d017-168">Affichage de l’historique des communications avec votre administration fiscale</span><span class="sxs-lookup"><span data-stu-id="4d017-168">Viewing communications with your tax authority</span></span>
<span data-ttu-id="4d017-169">Dans certains pays, vous échangez des messages avec l'administration fiscale lorsque vous envoyez des états.</span><span class="sxs-lookup"><span data-stu-id="4d017-169">In some countries, you exchange messages with the tax authority when you submit reports.</span></span> <span data-ttu-id="4d017-170">Vous pouvez afficher le premier et le dernier message que vous avez envoyés ou reçus en choisissant **Télécharger le message d’envoi** et les actions **Télécharger le message de réponse**.</span><span class="sxs-lookup"><span data-stu-id="4d017-170">You can view the first and the last message you sent or received by choosing the **Download Submission Message** and **Download Response Message** actions.</span></span>  

## <a name="submitting-vat-reports-manually"></a><span data-ttu-id="4d017-171">Envoi manuel des états TVA</span><span class="sxs-lookup"><span data-stu-id="4d017-171">Submitting VAT reports manually</span></span>
<span data-ttu-id="4d017-172">Si vous utilisez une autre méthode pour envoyer l'état, par exemple en exportant le XML et en le téléchargeant sur le site Web d'une administration fiscale, vous pouvez ensuite choisir **Marquer comme Soumis** pour clôturer la période de référence.</span><span class="sxs-lookup"><span data-stu-id="4d017-172">If you use another method to submit the report, for example by exporting the XML and uploading it to a tax authority website, afterward you can choose **Mark as Submitted** to close the reporting period.</span></span> <span data-ttu-id="4d017-173">Lorsque vous signalez un état comme lancé, vous ne pouvez plus le modifier.</span><span class="sxs-lookup"><span data-stu-id="4d017-173">When you mark the report as released, it becomes non-editable.</span></span> <span data-ttu-id="4d017-174">Si vous devez modifier l'état après l'avoir signalé comme lancé, vous devez le rouvrir.</span><span class="sxs-lookup"><span data-stu-id="4d017-174">If you must change the report after you mark it as released, you must reopen it.</span></span>

## <a name="vat-settlement"></a><span data-ttu-id="4d017-175">Déclaration de TVA</span><span class="sxs-lookup"><span data-stu-id="4d017-175">VAT settlement</span></span>
<span data-ttu-id="4d017-176">Périodiquement, vous devez régler la TVA nette aux autorités fiscales.</span><span class="sxs-lookup"><span data-stu-id="4d017-176">Periodically, you must remit the net VAT to the tax authorities.</span></span> <span data-ttu-id="4d017-177">Si vous devez effectuer des déclarations de TVA fréquemment, vous pouvez exécuter le traitement par lots **Calculer et valider décl. TVA** pour clôturer les écritures TVA ouvertes et transférer les montants TVA achat et vente dans le compte de déclaration TVA.</span><span class="sxs-lookup"><span data-stu-id="4d017-177">If you need to settle VAT frequently, you can run the **Calc. and Post VAT Settlement** batch job to close the open VAT entries and transfer purchase and sales VAT amounts to the VAT settlement account.</span></span>

<span data-ttu-id="4d017-178">Lors du transfert des montants TVA vers le compte de déclaration, le compte TVA achat est crédité et le compte TVA vente est débité sur la base des montants calculés pour la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4d017-178">When you transfer VAT amounts to the settlement account, the purchase VAT account is credited, and the sales VAT account is debited with the amounts calculated for the specified period.</span></span> <span data-ttu-id="4d017-179">Le montant net est crédité ou débité, si le montant achat TVA est supérieur, sur le compte de déclaration TVA.</span><span class="sxs-lookup"><span data-stu-id="4d017-179">The net amount is credited or debited, if the purchase VAT amount is larger, to the VAT settlement account.</span></span> <span data-ttu-id="4d017-180">Vous pouvez valider la déclaration immédiatement ou imprimer d'abord une impression test.</span><span class="sxs-lookup"><span data-stu-id="4d017-180">You can post the settlement immediately or print a test report first.</span></span>  

> [!Note]
> <span data-ttu-id="4d017-181">Lorsque vous utilisez le traitement par lots **Calculer et valider décl. TVA**, si vous ne spécifiez pas **Groupe compta. marché TVA** ni **Groupe compta. produit TVA**, les écritures contenant les codes des groupes comptabilisation marché et des groupes comptabilisation produit sont incluses.</span><span class="sxs-lookup"><span data-stu-id="4d017-181">When you use the **Calc. and Post VAT Settlement** batch job, if you don't specify a **VAT Bus. Posting Group** and a **VAT Prod. Posting group**, entries with all business posting groups and product posting group codes are included.</span></span>

## <a name="configuring-your-own-vat-reports"></a><span data-ttu-id="4d017-182">Configuration de vos propres états de TVA</span><span class="sxs-lookup"><span data-stu-id="4d017-182">Configuring your own VAT reports</span></span>
<span data-ttu-id="4d017-183">Vous pouvez utiliser l'état Liste des ventes UE prédéfini, cependant, vous pouvez également créer vos propres états.</span><span class="sxs-lookup"><span data-stu-id="4d017-183">You can use the EC Sales List report out-of-the-box, however, you can also create your own reports.</span></span> <span data-ttu-id="4d017-184">Cela nécessite de créer des codeunits.</span><span class="sxs-lookup"><span data-stu-id="4d017-184">This requires that you create a few codeunits.</span></span> <span data-ttu-id="4d017-185">Si vous avez besoin de l'aide à cette fin, contactez un partenaire certifié Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d017-185">If you need help with that, contact a Microsoft Partner.</span></span>  

<span data-ttu-id="4d017-186">Le tableau suivant décrit les codeunits que vous devez créer pour votre état.</span><span class="sxs-lookup"><span data-stu-id="4d017-186">The following table describes the codeunits that you must create for your report.</span></span>

| <span data-ttu-id="4d017-187">Codeunit</span><span class="sxs-lookup"><span data-stu-id="4d017-187">Codeunit</span></span> | <span data-ttu-id="4d017-188">Ce qu'il doit effectuer</span><span class="sxs-lookup"><span data-stu-id="4d017-188">What it must do</span></span> |
|----|-----|
|<span data-ttu-id="4d017-189">Proposer lignes</span><span class="sxs-lookup"><span data-stu-id="4d017-189">Suggest Lines</span></span>| <span data-ttu-id="4d017-190">Extraire les informations de la table Ecritures TVA, et les afficher sur les lignes de l'état TVA.</span><span class="sxs-lookup"><span data-stu-id="4d017-190">Fetch information from the VAT Entries table, and display it in lines on the VAT report.</span></span>|
|<span data-ttu-id="4d017-191">Contenu</span><span class="sxs-lookup"><span data-stu-id="4d017-191">Content</span></span> | <span data-ttu-id="4d017-192">Contrôler le format de l'état.</span><span class="sxs-lookup"><span data-stu-id="4d017-192">Control the format of the report.</span></span> <span data-ttu-id="4d017-193">Par exemple, si c'est un fichier XML ou JSON.</span><span class="sxs-lookup"><span data-stu-id="4d017-193">For example, whether it is XML or JSON.</span></span> <span data-ttu-id="4d017-194">Le format à utiliser dépend des besoins du service Web de votre administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-194">The format to use depends on the requirements of your tax authority's web service.</span></span> |
|<span data-ttu-id="4d017-195">Soumission</span><span class="sxs-lookup"><span data-stu-id="4d017-195">Submission</span></span> | <span data-ttu-id="4d017-196">Contrôler comment et quand vous envoyez l'état selon les besoins de votre administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-196">Control how, and when, you submit the report based on the requirements of your tax authority.</span></span> |
|<span data-ttu-id="4d017-197">Gestionnaire de réponse</span><span class="sxs-lookup"><span data-stu-id="4d017-197">Response Handler</span></span> | <span data-ttu-id="4d017-198">Gérer le retour de l'administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-198">Handle the return from the tax authority.</span></span> <span data-ttu-id="4d017-199">Par exemple, elle peut envoyer un message e-mail au contact de votre société.</span><span class="sxs-lookup"><span data-stu-id="4d017-199">For example, it might send an email message to your company's contact person.</span></span> |
|<span data-ttu-id="4d017-200">Annuler</span><span class="sxs-lookup"><span data-stu-id="4d017-200">Cancel</span></span> | <span data-ttu-id="4d017-201">Envoyer une annulation d'un état de TVA qui a été envoyé précédemment à votre administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-201">Send a cancellation of a VAT report that was submitted earlier to your tax authority.</span></span> |  

> [!Note]
> <span data-ttu-id="4d017-202">Lorsque vous créez des codeunits pour l'état, faites attention à la valeur du champ **Version de la déclaration TVA**.</span><span class="sxs-lookup"><span data-stu-id="4d017-202">When create codeunits for the report, pay attention to the value in the **VAT Report Version** field.</span></span> <span data-ttu-id="4d017-203">Ce champ doit refléter la version de l'état qui est ou a été requis par l'administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-203">This field must reflect the version of the report that is, or was, required by the tax authority.</span></span> <span data-ttu-id="4d017-204">Par exemple, vous pouvez saisir **2017** dans le champ pour indiquer que l'état remplit les conditions qui étaient en place cette année.</span><span class="sxs-lookup"><span data-stu-id="4d017-204">For example, you might enter **2017** in the field to indicate that the report conforms to the requirements that were in place that year.</span></span> <span data-ttu-id="4d017-205">Pour trouver la version en cours, contactez votre administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="4d017-205">To find the current version, contact your tax authority.</span></span>
 
## <a name="see-also"></a><span data-ttu-id="4d017-206">Voir aussi .</span><span class="sxs-lookup"><span data-stu-id="4d017-206">See also</span></span>
[<span data-ttu-id="4d017-207">Configuration des méthodes de calcul et de validation de la taxe sur la valeur ajoutée</span><span class="sxs-lookup"><span data-stu-id="4d017-207">Setting Up to Calculations and Posting Methods for Value-Added Tax</span></span>](finance-setup-vat.md)  
[<span data-ttu-id="4d017-208">Utiliser la TVA sur les ventes et les achats</span><span class="sxs-lookup"><span data-stu-id="4d017-208">Work with VAT on Sales and Purchases</span></span>](finance-work-with-vat.md)  
[<span data-ttu-id="4d017-209">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="4d017-209">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="4d017-210">Facturer des ventes</span><span class="sxs-lookup"><span data-stu-id="4d017-210">Invoice Sales</span></span>](sales-how-invoice-sales.md)  