---
title: Audit des modifications| Microsoft Docs
description: Vous pouvez activer un journal utilisateur de sorte que vous avez un historique de toutes les modifications apportées aux données dans les tables suivies. Vous pouvez également suivre les activités avec certains types de journaux d'activité.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cffa7d23b7c09561914cc00a8a4b9820ed743c29
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775370"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="bad26-104">Audit des modifications dans Business Central</span><span class="sxs-lookup"><span data-stu-id="bad26-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="bad26-105">Vous pouvez activer le journal des modifications dans [!INCLUDE[d365fin](includes/d365fin_md.md)] afin d'avoir un historique des activités.</span><span class="sxs-lookup"><span data-stu-id="bad26-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="bad26-106">Le journal est basé sur les modifications apportées aux données dans les tableaux que vous suivez. Sur la page **Écritures du journal des modifications**, les entrées sont chronologiquement ordonnées et montrent les modifications apportées aux champs des tables spécifiées.</span><span class="sxs-lookup"><span data-stu-id="bad26-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="bad26-107">Le journal modification regroupe tous les changements apportés à la table.</span><span class="sxs-lookup"><span data-stu-id="bad26-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="bad26-108">Les modifications d'un utilisateur ne sont pas visibles dans les **Écritures du journal des modifications** jusqu'à ce que la session utilisateur soit redémarrée, ce qui se produit dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="bad26-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="bad26-109">La session a expiré et a été actualisée.</span><span class="sxs-lookup"><span data-stu-id="bad26-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="bad26-110">L'utilisateur a sélectionné une autre société ou un autre Tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="bad26-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="bad26-111">L'utilisateur s'est déconnecté et reconnecté.</span><span class="sxs-lookup"><span data-stu-id="bad26-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="bad26-112">Utilisation du journal des modifications</span><span class="sxs-lookup"><span data-stu-id="bad26-112">Working with the Change Log</span></span>

<span data-ttu-id="bad26-113">Dans de nombreux systèmes financiers, il est souvent difficile de trouver l'origine des erreurs ou des modifications de données.</span><span class="sxs-lookup"><span data-stu-id="bad26-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="bad26-114">Il peut s'agir d'une simple erreur de numéro de téléphone client comme d'une écriture comptable erronée.</span><span class="sxs-lookup"><span data-stu-id="bad26-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="bad26-115">Le journal des modifications vous permet de suivre toutes les modifications directes apportées par un utilisateur aux données dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="bad26-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="bad26-116">Vous devez spécifier les opérations que le système doit journaliser, pour chaque table et chaque champ, puis activer le journal modification.</span><span class="sxs-lookup"><span data-stu-id="bad26-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="bad26-117">Vous devez activer et désactiver le journal des modifications sur la page **Paramètres journal modification**.</span><span class="sxs-lookup"><span data-stu-id="bad26-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="bad26-118">Lorsqu'un utilisateur active ou désactive le journal des modifications, cette activité est enregistrée, ainsi vous pouvez toujours savoir quel utilisateur est à l'origine de la modification.</span><span class="sxs-lookup"><span data-stu-id="bad26-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="bad26-119">Sur la page **Paramètres journal modification**, si vous choisissez l'option **Tables**, vous pouvez spécifier les tables dont vous souhaitez suivre les modifications, et quelles modifications suivre. [!INCLUDE[d365fin](includes/d365fin_md.md)] suit également un nombre de tables système.</span><span class="sxs-lookup"><span data-stu-id="bad26-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="bad26-120">Une fois que vous avez configuré et activé le journal des modifications et modifié des données, vous pouvez afficher et filtrer les modifications sur la page **Écritures journal modification**.</span><span class="sxs-lookup"><span data-stu-id="bad26-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="bad26-121">Vous pouvez supprimer des données à partir de la page **Suppr écritures journal modif**, dans laquelle vous pouvez définir des filtres basés sur la date et l'heure.</span><span class="sxs-lookup"><span data-stu-id="bad26-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="bad26-122">Utilisation des journaux d'activité</span><span class="sxs-lookup"><span data-stu-id="bad26-122">Working with Activity Logs</span></span>

<span data-ttu-id="bad26-123">À partir des pages [!INCLUDE [prodshort](includes/prodshort.md)], vous pouvez afficher un journal d’activités indiquant l’état et les erreurs éventuelles des fichiers que vous exportez ou importez dans [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="bad26-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="bad26-124">Les informations sont affichées dans la page **Journal des activités** en fonction du contexte d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="bad26-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="bad26-125">Vous pouvez ouvrir la fenêtre depuis les pages **Paramètres du service d'échange de documents**, **Document entrant**, **Facture vente validée** et **Avoir vente enregistré**, par exemple.</span><span class="sxs-lookup"><span data-stu-id="bad26-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="bad26-126">Vous pouvez vider la liste des entrées du journal ou simplement effacer la liste des entrées de plus de 7 jours.</span><span class="sxs-lookup"><span data-stu-id="bad26-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bad26-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bad26-127">See Also</span></span>
[<span data-ttu-id="bad26-128">Modifier les paramètres de base</span><span class="sxs-lookup"><span data-stu-id="bad26-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="bad26-129">Tri</span><span class="sxs-lookup"><span data-stu-id="bad26-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="bad26-130">Recherche de pages et d'informations avec la fonction de recherche</span><span class="sxs-lookup"><span data-stu-id="bad26-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="bad26-131">[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="bad26-131">[Assign Permissions to Users and Groups](ui-define-granular-permissions.md)  </span></span>  
<span data-ttu-id="bad26-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bad26-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
