---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035815"
---
<span data-ttu-id="f749c-101">Lorsque tous les articles ont été entrés sur les lignes commande vente, vous pouvez calculer la remise sur facture pour l’ensemble du document vente en choisissant l’action **Calculer remise facture**.</span><span class="sxs-lookup"><span data-stu-id="f749c-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="f749c-102">Si le champ **Calculer remise facture** est sélectionné dans la fenêtre **Paramètres ventes**, la remise facture est calculée automatiquement lorsque vous effectuez l’une des actions suivantes sur un document vente :</span><span class="sxs-lookup"><span data-stu-id="f749c-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="f749c-103">Afficher les statistiques</span><span class="sxs-lookup"><span data-stu-id="f749c-103">View statistics</span></span>
* <span data-ttu-id="f749c-104">Afficher une impression test</span><span class="sxs-lookup"><span data-stu-id="f749c-104">View a test report</span></span>
* <span data-ttu-id="f749c-105">Imprimer</span><span class="sxs-lookup"><span data-stu-id="f749c-105">Print</span></span>
* <span data-ttu-id="f749c-106">Comptabilisation</span><span class="sxs-lookup"><span data-stu-id="f749c-106">Post</span></span>

<span data-ttu-id="f749c-107">La remise est répartie sur toutes les lignes du document vente pour les articles et les ressources pour lesquels le champ **Remise facture autorisée** de la ligne commande vente indique **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f749c-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="f749c-108">C’est la configuration par défaut pour les articles.</span><span class="sxs-lookup"><span data-stu-id="f749c-108">This is the default setting for items.</span></span>

<span data-ttu-id="f749c-109">Les conditions de remise facture sont définies sur la page **Remise facture client** pour calculer la remise facture.</span><span class="sxs-lookup"><span data-stu-id="f749c-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="f749c-110">Le code devise du document vente est utilisé pour trouver les conditions remise facture de la devise.</span><span class="sxs-lookup"><span data-stu-id="f749c-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="f749c-111">Si vous n’avez pas défini de remise facture pour les devises, les conditions de remise facture définies sur la page **Remises facture client** avec des montants dans votre devise locale et le taux de change à la date de comptabilisation du document vente sont utilisés pour calculer la remise facture en devise.</span><span class="sxs-lookup"><span data-stu-id="f749c-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
