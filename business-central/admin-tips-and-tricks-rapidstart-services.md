---
title: Conseils - RapidStart Services | Microsoft Docs
description: Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.
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
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821555"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="39d12-103">Conseils : RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="39d12-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="39d12-104">Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="39d12-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="39d12-105">Optimisation des modèles de société</span><span class="sxs-lookup"><span data-stu-id="39d12-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="39d12-106">Les modèles de configuration peuvent vous aider à rationaliser votre processus d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="39d12-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="39d12-107">Ces modèles vous permettent d'inclure des clients similaires dans des segments, puis de développer un protocole d'implémentation qui traite tous les clients d'un segment de la même façon.</span><span class="sxs-lookup"><span data-stu-id="39d12-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="39d12-108">Vous pouvez ainsi appliquer un niveau de préconfiguration à chaque segment et procéder rapidement à une implémentation.</span><span class="sxs-lookup"><span data-stu-id="39d12-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="39d12-109">Questionnaires de configuration</span><span class="sxs-lookup"><span data-stu-id="39d12-109">Configuration questionnaires</span></span>  
<span data-ttu-id="39d12-110">Pour faciliter le remplissage d’un questionnaire de configuration, envisagez de définir des réponses par défaut pour indiquer des recommandations.</span><span class="sxs-lookup"><span data-stu-id="39d12-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="39d12-111">Création de lignes feuille par lots</span><span class="sxs-lookup"><span data-stu-id="39d12-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="39d12-112">Il est recommandé d'utiliser les outils de migration de données fournis pour migrer des écritures feuille.</span><span class="sxs-lookup"><span data-stu-id="39d12-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="39d12-113">Sinon, si vous utilisez le traitement par lots pour créer des lignes feuille, celui-ci a une portée limitée et ne génère que des champs par défaut dans une feuille.</span><span class="sxs-lookup"><span data-stu-id="39d12-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="39d12-114">Le reste de la feuille doit ensuite être renseigné manuellement.</span><span class="sxs-lookup"><span data-stu-id="39d12-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="39d12-115">Migration des transactions</span><span class="sxs-lookup"><span data-stu-id="39d12-115">Migrating transactions</span></span>  
<span data-ttu-id="39d12-116">Il est recommandé de migrer des soldes ouverts dans l'ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="39d12-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="39d12-117">Migrez les soldes ouverts de la comptabilité sans utiliser la comptabilité auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="39d12-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="39d12-118">Utilisez des comptes de compensation propres aux soldes ouverts, avec une configuration pour chaque comptabilité auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="39d12-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="39d12-119">Configurez les comptes de compensation de manière à activer les imputations directes.</span><span class="sxs-lookup"><span data-stu-id="39d12-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="39d12-120">Migration des écritures comptables client ouvertes.</span><span class="sxs-lookup"><span data-stu-id="39d12-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="39d12-121">Migrez les écritures comptables article ouvertes.</span><span class="sxs-lookup"><span data-stu-id="39d12-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="39d12-122">Migrez les écritures comptables immobilisation ouvertes.</span><span class="sxs-lookup"><span data-stu-id="39d12-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="39d12-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39d12-123">See Also</span></span>  
[<span data-ttu-id="39d12-124">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="39d12-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="39d12-125">Administration</span><span class="sxs-lookup"><span data-stu-id="39d12-125">Administration</span></span>](admin-setup-and-administration.md)
