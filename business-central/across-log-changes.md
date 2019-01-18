---
title: "Effectuer le suivi de l'activité utilisateur dans un journal modification| Microsoft Docs"
description: "Vous pouvez activer un journal utilisateur de sorte que vous avez un historique de toutes les modifications apportées aux données dans les tables suivies."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 3f158d7ed56445d6d2acf2ef8e5e9ab8e7487531
ms.openlocfilehash: bd0751ad5a4c0c7d9c3f7d5621bb7e6a62c3be2a
ms.contentlocale: fr-ch
ms.lasthandoff: 12/04/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="3ea8e-103">Journalisation des modifications dans Business Central</span><span class="sxs-lookup"><span data-stu-id="3ea8e-103">Logging Changes in Business Central</span></span>

<span data-ttu-id="3ea8e-104">Vous pouvez activer le journal des modifications dans [!INCLUDE[d365fin](includes/d365fin_md.md)] afin d'avoir un historique des activités.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="3ea8e-105">Le journal est basé sur les modifications apportées aux données dans les tableaux que vous suivez. Sur la page **Écritures du journal des modifications**, les entrées sont chronologiquement ordonnées et montrent les modifications apportées aux champs des tables spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="3ea8e-106">Le journal modification regroupe tous les changements apportés à la table.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="3ea8e-107">Les modifications d'un utilisateur ne sont pas visibles dans les **Écritures du journal des modifications** jusqu'à ce que la session utilisateur soit redémarrée, ce qui se produit dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="3ea8e-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="3ea8e-108">La session a expiré et a été actualisée.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="3ea8e-109">L'utilisateur a sélectionné une autre société ou un autre Tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="3ea8e-110">L'utilisateur s'est déconnecté et reconnecté.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="3ea8e-111">Utilisation du journal des modifications</span><span class="sxs-lookup"><span data-stu-id="3ea8e-111">Working with the Change Log</span></span>

<span data-ttu-id="3ea8e-112">Dans de nombreux systèmes financiers, il est souvent difficile de trouver l'origine des erreurs ou des modifications de données.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="3ea8e-113">Il peut s'agir d'une simple erreur de numéro de téléphone client comme d'une écriture comptable erronée.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="3ea8e-114">Le journal des modifications vous permet de suivre toutes les modifications directes apportées par un utilisateur aux données dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="3ea8e-115">Vous devez spécifier les opérations que le système doit journaliser, pour chaque table et chaque champ, puis activer le journal modification.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="3ea8e-116">Vous devez activer et désactiver le journal des modifications sur la page **Paramètres journal modification**.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="3ea8e-117">Lorsqu'un utilisateur active ou désactive le journal des modifications, cette activité est enregistrée, ainsi vous pouvez toujours savoir quel utilisateur est à l'origine de la modification.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="3ea8e-118">Sur la page **Paramètres journal modification**, si vous choisissez l'option **Tables**, vous pouvez spécifier les tables dont vous souhaitez suivre les modifications, et quelles modifications suivre. [!INCLUDE[d365fin](includes/d365fin_md.md)] suit également un nombre de tables système.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="3ea8e-119">Une fois que vous avez configuré et activé le journal des modifications et modifié des données, vous pouvez afficher et filtrer les modifications sur la page **Écritures journal modification**.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="3ea8e-120">Vous pouvez supprimer des données à partir de la page **Suppr écritures journal modif**, dans laquelle vous pouvez définir des filtres basés sur la date et l'heure.</span><span class="sxs-lookup"><span data-stu-id="3ea8e-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3ea8e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ea8e-121">See Also</span></span>
[<span data-ttu-id="3ea8e-122">Modification des paramètres de base</span><span class="sxs-lookup"><span data-stu-id="3ea8e-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="3ea8e-123">Tri</span><span class="sxs-lookup"><span data-stu-id="3ea8e-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="3ea8e-124">Utilisation de l'icône Page ou état pour la recherche </span><span class="sxs-lookup"><span data-stu-id="3ea8e-124">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="3ea8e-125">[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="3ea8e-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="3ea8e-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3ea8e-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

