---
title: Champs obligatoires pour exécuter les processus | Microsoft Docs
description: En savoir plus sur les champs marqués avec un astérisque rouge, ce qui indique qu’ils sont requis et doivent être renseignés pour exécuter les processus.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: cf2a64ef102dec16ad0df83e8c911e2b6c3bd88e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912136"
---
# <a name="detecting-mandatory-fields"></a><span data-ttu-id="04b94-103">Détection de champs obligatoires</span><span class="sxs-lookup"><span data-stu-id="04b94-103">Detecting Mandatory Fields</span></span>
<span data-ttu-id="04b94-104">Lorsque vous entrez des données sur les pages dans [!INCLUDE[d365fin](includes/d365fin_md.md)], certains champs sont marqués par un astérisque rouge.</span><span class="sxs-lookup"><span data-stu-id="04b94-104">When you enter data on pages in [!INCLUDE[d365fin](includes/d365fin_md.md)], certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="04b94-105">L’astérisque rouge signifie que le champ doit être renseigné pour terminer un processus qui utilise ce champ, par exemple, valider une transaction qui utilise la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="04b94-105">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>

<span data-ttu-id="04b94-106">Même si le champ contient un astérisque rouge, vous n’êtes pas forcé de remplir le champ avant de poursuivre avec les autres champs ou fermer la page.</span><span class="sxs-lookup"><span data-stu-id="04b94-106">Even though the field contains a red asterisk, you are not forced to fill in the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="04b94-107">L’astérisque rouge sert uniquement à rappeler que la fin d’un certain processus restera bloquée.</span><span class="sxs-lookup"><span data-stu-id="04b94-107">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>

## <a name="examples"></a><span data-ttu-id="04b94-108">Exemples</span><span class="sxs-lookup"><span data-stu-id="04b94-108">Examples</span></span>
<span data-ttu-id="04b94-109">Sur la page **Fiche client** , l’astérisque rouge figure dans le champ **Nom** , dans le champ **Code zone recouvrement** et dans les champs de groupe comptabilisation pour indiquer que vous ne pouvez pas valider une transaction de vente pour le client à moins que les champs soient renseignés.</span><span class="sxs-lookup"><span data-stu-id="04b94-109">On the **Customer Card** page, the red asterisk appears in the **Name** field, in the **Tax Area Code** field, and in the posting group fields to indicate that you cannot post a sales transaction for the customer unless the fields are filled.</span></span>

<span data-ttu-id="04b94-110">Sur la page **Fiche article** , l’astérisque rouge figure dans le champ **Description** pour indiquer que vous ne pouvez pas entrer l’article dans une ligne document, par exemple une commande vente, à moins que ce champ soient renseigné.</span><span class="sxs-lookup"><span data-stu-id="04b94-110">On the **Item Card** page, the red asterisk appears in the **Description** field to indicate that you cannot enter the item on a document line, such as a sales order, unless this field is filled.</span></span>

## <a name="see-also"></a><span data-ttu-id="04b94-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04b94-111">See Also</span></span>
<span data-ttu-id="04b94-112">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04b94-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
