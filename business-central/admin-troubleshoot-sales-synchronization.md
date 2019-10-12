---
title: Dépannage des erreurs de synchronisation | Microsoft Docs
description: Fournit des indications pour identifier et résoudre les erreurs de synchronisation.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304299"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="77ae0-103">Résolution des erreurs de synchronisation</span><span class="sxs-lookup"><span data-stu-id="77ae0-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="77ae0-104">Il y a beaucoup de pièces mobiles impliquées dans l'intégration [!INCLUDE[d365fin](includes/d365fin_md.md)] avec [!INCLUDE[crm_md](includes/crm_md.md)], et parfois les choses ne se passent pas bien.</span><span class="sxs-lookup"><span data-stu-id="77ae0-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="77ae0-105">Cette rubrique répertorie certaines des erreurs types qui se produisent et donne des indications sur la manière de les résoudre.</span><span class="sxs-lookup"><span data-stu-id="77ae0-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="77ae0-106">Les erreurs se produisent souvent à cause de quelque chose qu'un utilisateur a fait pour coupler des enregistrements ou parce que la configuration de l'intégration est fausse.</span><span class="sxs-lookup"><span data-stu-id="77ae0-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="77ae0-107">Pour les erreurs liées aux enregistrements couplés, les utilisateurs peuvent les résoudre eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="77ae0-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="77ae0-108">Ces erreurs sont causées par des actions telles que la suppression d'un enregistrement dans l'une des applications métier mais pas les deux, puis la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="77ae0-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="77ae0-109">Pour plus d'informations, voir [Afficher le statut d'une synchronisation](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="77ae0-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="77ae0-110">Les erreurs liées à la configuration de l'intégration nécessitent généralement l'attention de l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="77ae0-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="77ae0-111">Vous pouvez voir ces erreurs sur la page **Erreurs de synchronisation d'intégration**.</span><span class="sxs-lookup"><span data-stu-id="77ae0-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="77ae0-112">Voici des exemples de problèmes classiques :</span><span class="sxs-lookup"><span data-stu-id="77ae0-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="77ae0-113">Les autorisations et les rôles attribués aux utilisateurs ne sont pas corrects.</span><span class="sxs-lookup"><span data-stu-id="77ae0-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="77ae0-114">Le compte administrateur a été spécifié en tant qu'utilisateur d'intégration.</span><span class="sxs-lookup"><span data-stu-id="77ae0-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="77ae0-115">Le mot de passe de l'utilisateur d'intégration est défini pour nécessiter une modification lorsque l'utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="77ae0-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="77ae0-116">Les taux de change pour les devises ne sont pas spécifiés dans l'une ou l'autre application.</span><span class="sxs-lookup"><span data-stu-id="77ae0-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="77ae0-117">Vous devez résoudre manuellement les erreurs, mais la page vous aide de plusieurs manières.</span><span class="sxs-lookup"><span data-stu-id="77ae0-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="77ae0-118">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="77ae0-118">For example:</span></span>  

* <span data-ttu-id="77ae0-119">Les champs **Source** et **Destination** peuvent contenir des liens vers l'enregistrement où l'erreur a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="77ae0-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="77ae0-120">Cliquez sur le lien pour ouvrir l'enregistrement et recherchez l'erreur.</span><span class="sxs-lookup"><span data-stu-id="77ae0-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="77ae0-121">Les actions **Supprimer les écritures ultérieures à 7 jours** et **Supprimer toutes les écritures** vont nettoyer la liste.</span><span class="sxs-lookup"><span data-stu-id="77ae0-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="77ae0-122">En règle générale, vous utilisez ces actions après avoir résolu la cause d'une erreur affectant de nombreux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="77ae0-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="77ae0-123">Faites attention, cependant.</span><span class="sxs-lookup"><span data-stu-id="77ae0-123">Use caution, however.</span></span> <span data-ttu-id="77ae0-124">Ces actions peuvent supprimer des erreurs toujours pertinentes.</span><span class="sxs-lookup"><span data-stu-id="77ae0-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="77ae0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77ae0-125">See Also</span></span>
<span data-ttu-id="77ae0-126">[Intégration à [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="77ae0-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="77ae0-127">[Configuration des comptes d'utilisateur pour intégration à [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="77ae0-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="77ae0-128">[Configurer une connexion vers [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="77ae0-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="77ae0-129">Coupler et synchroniser des enregistrements manuellement</span><span class="sxs-lookup"><span data-stu-id="77ae0-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="77ae0-130">Afficher le statut d'une synchronisation</span><span class="sxs-lookup"><span data-stu-id="77ae0-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  