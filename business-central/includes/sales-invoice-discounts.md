---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470302"
---
<span data-ttu-id="7bd58-101">Lorsque tous les articles ont été entrés sur les lignes vente, vous pouvez calculer la remise sur facture pour l’ensemble du document vente en choisissant l’action **Calculer remise facture**.</span><span class="sxs-lookup"><span data-stu-id="7bd58-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="7bd58-102">La remise est calculée en fonction de toutes les lignes du document vente pour les articles et les ressources pour lesquels le champ **Remise facture autorisée** de la ligne commande vente indique **Oui**.</span><span class="sxs-lookup"><span data-stu-id="7bd58-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="7bd58-103">C’est la configuration par défaut pour les articles.</span><span class="sxs-lookup"><span data-stu-id="7bd58-103">This is the default setting for items.</span></span> <span data-ttu-id="7bd58-104">Les lignes avec des frais annexes, par exemple, ne sont pas incluses dans le calcul de la remise facture.</span><span class="sxs-lookup"><span data-stu-id="7bd58-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="7bd58-105">Si vous souhaitez appliquer une remise à ces lignes, vous devez définir le champ **% remise ligne** sur les lignes appropriées.</span><span class="sxs-lookup"><span data-stu-id="7bd58-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="7bd58-106">Si le champ **Calculer remise facture** est sélectionné dans la page **Paramètres ventes**, la remise facture est calculée automatiquement lorsque vous effectuez l’une des actions suivantes sur un document vente :</span><span class="sxs-lookup"><span data-stu-id="7bd58-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="7bd58-107">Afficher les statistiques</span><span class="sxs-lookup"><span data-stu-id="7bd58-107">View statistics</span></span>
> * <span data-ttu-id="7bd58-108">Afficher une impression test</span><span class="sxs-lookup"><span data-stu-id="7bd58-108">View a test report</span></span>
> * <span data-ttu-id="7bd58-109">Imprimer</span><span class="sxs-lookup"><span data-stu-id="7bd58-109">Print</span></span>
> * <span data-ttu-id="7bd58-110">Comptabilisation</span><span class="sxs-lookup"><span data-stu-id="7bd58-110">Post</span></span>

<span data-ttu-id="7bd58-111">Les conditions de remise facture pour un client sont définies sur la page **Remise facture client** pour le client.</span><span class="sxs-lookup"><span data-stu-id="7bd58-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="7bd58-112">Le code devise du document vente est utilisé pour trouver les conditions remise facture de la devise.</span><span class="sxs-lookup"><span data-stu-id="7bd58-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="7bd58-113">Si vous n’avez pas défini de remise facture pour les devises, les conditions de remise facture définies sur la page **Remises facture client** avec des montants dans votre devise locale et le taux de change à la date de comptabilisation du document vente sont utilisés pour calculer la remise facture en devise.</span><span class="sxs-lookup"><span data-stu-id="7bd58-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
