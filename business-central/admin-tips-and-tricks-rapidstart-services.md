---
title: Conseils - RapidStart Services | Microsoft Docs
description: Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e301d788fdedacf0fc2ac3ce29946df965bed711
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777081"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="c314f-103">Conseils : RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c314f-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="c314f-104">Lorsque vous configurez des sociétés avec RapidStart Services, il est recommandé de suivre certains conseils pour faciliter votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="c314f-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="c314f-105">Optimisation des modèles de société</span><span class="sxs-lookup"><span data-stu-id="c314f-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="c314f-106">Les modèles de configuration peuvent vous aider à rationaliser votre processus d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c314f-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="c314f-107">Ces modèles vous permettent d’inclure des clients similaires dans des segments, puis de développer un protocole d’implémentation qui traite tous les clients d’un segment de la même façon.</span><span class="sxs-lookup"><span data-stu-id="c314f-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="c314f-108">Vous pouvez ainsi appliquer un niveau de préconfiguration à chaque segment et procéder rapidement à une implémentation.</span><span class="sxs-lookup"><span data-stu-id="c314f-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="c314f-109">Questionnaires de configuration</span><span class="sxs-lookup"><span data-stu-id="c314f-109">Configuration questionnaires</span></span>

<span data-ttu-id="c314f-110">Pour faciliter le remplissage d’un questionnaire de configuration, envisagez de définir des réponses par défaut pour indiquer des recommandations.</span><span class="sxs-lookup"><span data-stu-id="c314f-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="c314f-111">Création de lignes feuille par lots</span><span class="sxs-lookup"><span data-stu-id="c314f-111">Batch creation of journal lines</span></span>

<span data-ttu-id="c314f-112">Il est recommandé d’utiliser les outils de migration de données fournis pour migrer des écritures feuille.</span><span class="sxs-lookup"><span data-stu-id="c314f-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="c314f-113">Sinon, si vous utilisez le traitement par lots pour créer des lignes feuille, celui-ci a une portée limitée et ne génère que des champs par défaut dans une feuille.</span><span class="sxs-lookup"><span data-stu-id="c314f-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="c314f-114">Le reste de la feuille doit ensuite être renseigné manuellement.</span><span class="sxs-lookup"><span data-stu-id="c314f-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="c314f-115">Migration des transactions</span><span class="sxs-lookup"><span data-stu-id="c314f-115">Migrating transactions</span></span>

<span data-ttu-id="c314f-116">Il est recommandé de migrer des soldes ouverts dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="c314f-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="c314f-117">Migrez les soldes ouverts de la comptabilité sans utiliser la comptabilité auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="c314f-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="c314f-118">Utilisez des comptes de compensation propres aux soldes ouverts, avec une configuration pour chaque comptabilité auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="c314f-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="c314f-119">Configurez les comptes de compensation de manière à activer les imputations directes.</span><span class="sxs-lookup"><span data-stu-id="c314f-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="c314f-120">Migration des écritures comptables client ouvertes.</span><span class="sxs-lookup"><span data-stu-id="c314f-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="c314f-121">Migrez les écritures comptables article ouvertes.</span><span class="sxs-lookup"><span data-stu-id="c314f-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="c314f-122">Migrez les écritures comptables immobilisation ouvertes.</span><span class="sxs-lookup"><span data-stu-id="c314f-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="c314f-123">Rendre chaque paquet gérable</span><span class="sxs-lookup"><span data-stu-id="c314f-123">Make each package manageable</span></span>

<span data-ttu-id="c314f-124">Lorsque vous utilisez des packages de configuration pour migrer des données, séparez les données en packages séparés pour une portabilité plus facile.</span><span class="sxs-lookup"><span data-stu-id="c314f-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="c314f-125">Par exemple, si vous souhaitez migrer 20 ans d’écritures comptables, l’importation peut prendre plusieurs heures et jours.</span><span class="sxs-lookup"><span data-stu-id="c314f-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="c314f-126">Au lieu de cela, divisez les données afin que chaque package devienne plus gérable.</span><span class="sxs-lookup"><span data-stu-id="c314f-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="c314f-127">Actuellement, il n’y a pas de règles fermes pour rendre un package performant, mais si vous rencontrez des problèmes lors de l’importation ou de l’exportation d’un package, essayez de le réduire et voyez si cela aide.</span><span class="sxs-lookup"><span data-stu-id="c314f-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c314f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c314f-128">See Also</span></span>

[<span data-ttu-id="c314f-129">Configuration d’une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c314f-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c314f-130">Administration</span><span class="sxs-lookup"><span data-stu-id="c314f-130">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]