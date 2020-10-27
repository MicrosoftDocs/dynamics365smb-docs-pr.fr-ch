---
title: Config. identifiant messagerie | Microsoft Docs
description: Apprenez à transformer les interactions de messagerie entre les vendeurs et les clients en véritables opportunités de vente.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923635"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="db2cf-103">Suivre les échanges de messages électroniques entre les vendeurs et les contacts</span><span class="sxs-lookup"><span data-stu-id="db2cf-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="db2cf-104">Tirez le meilleur parti des communications entre les vendeurs et vos clients existants ou potentiels en suivant les échanges de courriers électroniques, puis en les transformant en opportunités exploitables.</span><span class="sxs-lookup"><span data-stu-id="db2cf-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="db2cf-105">peut utiliser Exchange Online pour conserver un journal des messages entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="db2cf-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="db2cf-106">Vous pouvez afficher et analyser le contenu de chaque message sur la page **Écritures journal interaction** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="db2cf-107">Configurer les dossiers publics et les règles de connexion à la messagerie dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="db2cf-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="db2cf-108">Ensuite, vous connectez [!INCLUDE[prodshort](includes/prodshort.md)] à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="db2cf-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="db2cf-109">Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour enregistrer les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="db2cf-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="db2cf-110">Commencez avec la connexion à la messagerie en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="db2cf-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="db2cf-111">Connectez [!INCLUDE[d365fin](includes/d365fin_md.md)] à Exchange Online pour votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db2cf-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Microsoft 365 subscription.</span></span> <span data-ttu-id="db2cf-112">Exchange Online gère vos e-mails.</span><span class="sxs-lookup"><span data-stu-id="db2cf-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="db2cf-113">Nous avons facilité cette étape en fournissant un guide de configuration assisté.</span><span class="sxs-lookup"><span data-stu-id="db2cf-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="db2cf-114">Vous avez juste besoin de vos identifiants d’administrateur pour votre compte d’administrateur dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db2cf-114">You just need your administrator credentials for your administrator account in Microsoft 365.</span></span> <span data-ttu-id="db2cf-115">Pour commencer le guide, accédez à **Configuration assistée** , puis choisissez **Configurer la journalisation des emails** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-115">To start the guide, go to **Assisted Setup** , and then choose **Set up email logging** .</span></span>  

2. <span data-ttu-id="db2cf-116">Assurez-vous que des adresses électroniques valides ont été entrées dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour vos commerciaux et vos contacts, selon qu’ils sont des clients potentiels ou existants.</span><span class="sxs-lookup"><span data-stu-id="db2cf-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="db2cf-117">Pour ce faire, pour chaque client ou vendeur, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** et regardez le champ **E-mail** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="db2cf-118">Une fois les étapes du guide terminées, vous pouvez vérifier si la connexion a réussi.</span><span class="sxs-lookup"><span data-stu-id="db2cf-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="db2cf-119">Recherchez **Paramètres marketing** , choisissez **Traiter** , puis **Fonctions** et **Valider la configuration de la connexion à la messagerie** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-119">Search for **Marketing Setup** , choose **Process** , then **Functions** , and then **Validate Email Logging Setup** .</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="db2cf-120">Affichage des échanges de messages électroniques dans le journal des interactions</span><span class="sxs-lookup"><span data-stu-id="db2cf-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="db2cf-121">crée une entrée sur la page **Journal des interactions** chaque fois qu’un vendeur et un contact échangent un message par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="db2cf-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="db2cf-122">Pour afficher le journal des interactions, ouvrez la fiche **Contact** ou **Vendeur/Acheteur** pour la personne, puis choisissez **Historique** , et **Écritures journal interaction** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-122">To view the interaction log, open the **Contact** or **Salesperson Purchaser** card for the person, and then choose **History** , and then choose **Interaction Log Entries** .</span></span> <span data-ttu-id="db2cf-123">Nous pouvons faire certaines choses avec chaque entrée du journal, par exemple :</span><span class="sxs-lookup"><span data-stu-id="db2cf-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="db2cf-124">Affichez le contenu du message électronique échangé en cliquant sur l’action **Afficher les pièces jointes** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="db2cf-125">Transformez un échange de courrier électronique en opportunité de vente. Si une entrée semble prometteuse, vous pouvez la transformer en opportunité, puis gérer son évolution vers une vente.</span><span class="sxs-lookup"><span data-stu-id="db2cf-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="db2cf-126">Pour cela, sélectionnez l’entrée, puis cliquez sur l’action **Créer une opportunité** .</span><span class="sxs-lookup"><span data-stu-id="db2cf-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="db2cf-127">Pour plus d’informations, voir [Gérer des opportunités de vente](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="db2cf-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="db2cf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db2cf-128">See Also</span></span>
[<span data-ttu-id="db2cf-129">Gestion des relations</span><span class="sxs-lookup"><span data-stu-id="db2cf-129">Managing Relationships</span></span>](marketing-relationship-management.md)

