---
title: Utiliser des profils pour classer les contacts
description: Configurer des questionnaires profil pour classer vos contacts professionnels
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2019
ms.openlocfilehash: fe02153a89ad5f63855cff5eec5344d601c8663a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "934457"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="ccdcd-103">Utiliser des questionnaires profil pour classer les contacts professionnels</span><span class="sxs-lookup"><span data-stu-id="ccdcd-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="ccdcd-104">Vous pouvez configurer des questionnaires profil à utiliser au moment d'entrer des informations sur les profils de vos contacts.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="ccdcd-105">Dans chaque questionnaire, vous pouvez configurer les questions à poser à vos contacts.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="ccdcd-106">Vous pouvez également exécuter le questionnaire pour répondre automatiquement à certaines de ces questions en fonction des données contact, client ou fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="ccdcd-107">Pour ajouter un questionnaire profil</span><span class="sxs-lookup"><span data-stu-id="ccdcd-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="ccdcd-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres questionnaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ccdcd-109">Sous l'onglet **Accueil**, dans le groupe **Nouveau**, choisissez **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="ccdcd-110">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="ccdcd-111">Pour ajouter des questions à un questionnaire profil</span><span class="sxs-lookup"><span data-stu-id="ccdcd-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="ccdcd-112">Choisissez le questionnaire profil approprié, puis sous l'onglet **Accueil**, dans le groupe **Processus**, choisissez **Modifier paramètres questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="ccdcd-113">Sur la première ligne vide, dans le champ **Type**, choisissez **Question**, puis tapez la question dans le champ **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="ccdcd-114">Renseignez les autres champs sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="ccdcd-115">Sur la ligne vide suivante, dans le champ **Type**, choisissez **Réponse**, puis tapez la réponse dans le champ **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="ccdcd-116">Dans le champ **Priorité**, sélectionnez la priorité.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="ccdcd-117">Dans les champs **Valeur début** et **Valeur fin**, définissez une plage de points.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="ccdcd-118">Les contacts obtenant un nombre de points compris dans la plage définie recevront la réponse.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="ccdcd-119">Répétez ces étapes pour entrer toutes les questions et réponses du questionnaire profil.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="ccdcd-120">Après avoir créé un questionnaire, vous devez créer des évaluations contact pour classer vos contacts.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="ccdcd-121">Vous pouvez également définir des questions qui sont évaluées automatiquement en fonction des informations de la fiche contact.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="ccdcd-122">Si vous entrez une question dont la réponse est automatique, choisissez <STRONG>Ligne</STRONG>, puis <STRONG>Questionnaire</STRONG> pour entrer les critères de réponse automatique.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="ccdcd-123">Classification automatique des contacts</span><span class="sxs-lookup"><span data-stu-id="ccdcd-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="ccdcd-124">Vous pouvez configurer le programme pour qu'il classe automatiquement les contacts en fonction des données client, fournisseur et contact. Pour cela, configurez des questions profil à réponse automatique sur la page **Paramètres questionnaires profil**.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="ccdcd-125">Vous ne pouvez affecter une classification basée sur les données contact qu'aux contacts enregistrés en tant que clients. De même, seuls les contacts enregistrés en tant que fournisseurs peuvent se voir affecter une classification basée sur les données fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="ccdcd-126">La classification automatique n'est pas mise à jour automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="ccdcd-127">Par conséquent, vous pouvez être amené à mettre à jour les questionnaires profil après avoir mis à jour les données client, fournisseur ou contact dont ils dépendent.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="ccdcd-128">Une fois que vous avez configuré les questions profil à réponse automatique, affectez à un contact le questionnaire profil qui les contient. [!INCLUDE[d365fin](includes/d365fin_md.md)] répond ensuite automatiquement aux questions.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="ccdcd-129">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ccdcd-129">Example</span></span>
<span data-ttu-id="ccdcd-130">Vous pouvez classer vos contacts en fonction du montant de leurs achats :</span><span class="sxs-lookup"><span data-stu-id="ccdcd-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccdcd-131"><strong>Réponse</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="ccdcd-132"><strong>Doc. lettrage</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccdcd-133">A</span><span class="sxs-lookup"><span data-stu-id="ccdcd-133">A</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-134">contacts ayant effectué des achats pour une somme supérieure ou égale à 500 000 DS</span><span class="sxs-lookup"><span data-stu-id="ccdcd-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccdcd-135">B</span><span class="sxs-lookup"><span data-stu-id="ccdcd-135">B</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-136">contacts ayant effectué des achats pour une somme comprise entre 100 000 et 499 999 DS</span><span class="sxs-lookup"><span data-stu-id="ccdcd-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccdcd-137">C</span><span class="sxs-lookup"><span data-stu-id="ccdcd-137">C</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-138">contacts ayant effectué des achats pour une somme inférieure ou égale à 99 999 DS</span><span class="sxs-lookup"><span data-stu-id="ccdcd-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccdcd-139">Pour cela, renseignez la page **Paramètres questionnaires profil** comme suit :</span><span class="sxs-lookup"><span data-stu-id="ccdcd-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccdcd-140"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="ccdcd-141"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="ccdcd-142"><strong>Classification automatique</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="ccdcd-143"><strong>Valeur début</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="ccdcd-144"><strong>Valeur fin</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccdcd-145">Question</span><span class="sxs-lookup"><span data-stu-id="ccdcd-145">Question</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-146">Classification ABC</span><span class="sxs-lookup"><span data-stu-id="ccdcd-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-147">Cochez la ligne appropriée.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccdcd-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="ccdcd-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-149">A</span><span class="sxs-lookup"><span data-stu-id="ccdcd-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ccdcd-150">500,000</span><span class="sxs-lookup"><span data-stu-id="ccdcd-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccdcd-151">Réponse</span><span class="sxs-lookup"><span data-stu-id="ccdcd-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-152">B</span><span class="sxs-lookup"><span data-stu-id="ccdcd-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ccdcd-153">100,000</span><span class="sxs-lookup"><span data-stu-id="ccdcd-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-154">499,999</span><span class="sxs-lookup"><span data-stu-id="ccdcd-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccdcd-155">Réponse</span><span class="sxs-lookup"><span data-stu-id="ccdcd-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="ccdcd-156">C</span><span class="sxs-lookup"><span data-stu-id="ccdcd-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="ccdcd-157">99,999</span><span class="sxs-lookup"><span data-stu-id="ccdcd-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccdcd-158">Renseignez ensuite la page **Questionnaire profil** comme suit :</span><span class="sxs-lookup"><span data-stu-id="ccdcd-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccdcd-159"><strong>Champ</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="ccdcd-160"><strong>Valeur</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ccdcd-161"><strong>Champ de classification des clients</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="ccdcd-162"><emphasis>Ventes DS</emphasis></span><span class="sxs-lookup"><span data-stu-id="ccdcd-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ccdcd-163"><strong>Méthode classification</strong></span><span class="sxs-lookup"><span data-stu-id="ccdcd-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="ccdcd-164"><emphasis>Valeur définie</emphasis></span><span class="sxs-lookup"><span data-stu-id="ccdcd-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ccdcd-165">Lorsque vous affectez le questionnaire profil contenant cette question à un contact, le programme insère automatiquement la réponse correspondante dans les lignes profil de la fiche contact.</span><span class="sxs-lookup"><span data-stu-id="ccdcd-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccdcd-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccdcd-166">See Also</span></span>
[<span data-ttu-id="ccdcd-167">Création de contacts</span><span class="sxs-lookup"><span data-stu-id="ccdcd-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
