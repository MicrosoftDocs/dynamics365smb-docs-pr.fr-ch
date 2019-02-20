---
title: "Mise à jour des taux de change des devises| Microsoft Docs"
description: "Pour utiliser plusieurs devises dans votre société, vous pouvez définir un code pour chaque devise et utiliser un service externe de taux de change."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: fr-ch
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a>Mettre à jour des taux de change devise
Les sociétés opérant dans un nombre croissant de pays/régions, il est de plus en plus important qu'elles puissent échanger ou générer des états financiers dans plusieurs devises. Vous devez définir un code pour chaque devise utilisée si vous achetez ou vendez dans des devises différentes de votre devise locale, si vous disposez de comptes client ou fournisseur dans d'autres devises, ou si vous enregistrez des transactions comptables dans des devises différentes.

Votre comptabilité est configurée pour utiliser votre devise société (DS), mais vous pouvez la configurer pour utiliser une autre devise avec un taux de change courant. Si vous désignez une deuxième devise comme « devise report supplémentaire », [!INCLUDE[d365fin](includes/d365fin_md.md)] enregistre automatiquement les montants d'état en DS et dans cette devise report supplémentaire pour chaque écriture comptable, ainsi que pour d'autres écritures, telles que les écritures TVA. Pour plus d'informations, voir [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Ajustement des taux de change
Comme les taux de change ne cessent de fluctuer, il convient d'ajuster périodiquement les équivalents devise supplémentaires de votre système. À défaut d'effectuer ces ajustements, les montants convertis à partir de devises étrangères (ou supplémentaires) et publiés dans la comptabilité en DS risquent d'être erronés. En outre, les écritures quotidiennes validées avant la saisie d'un taux de change quotidien dans le programme doivent être mises à jour après la saisie des informations de taux de change quotidienne. Le traitement par lots Ajuster taux de change permet d'ajuster les taux de change d'écritures client, fournisseur et compte bancaire validées. Il peut également mettre à jour d'autres montants en devise report dans des écritures comptables.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Configurer un service de taux de change des devises
Vous pouvez utiliser un service externe pour tenir vos taux de change des devises à jour, par exemple FloatRates.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Services de taux de change devise**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Sur la page **Service de taux de change devise**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Activez la case à cocher **Activé** pour activer le service.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Pour mettre à jour les taux de change des devises à partir d'un service
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Devises**, puis choisissez le lien associé.
2. Choisissez l'option **Mettre à jour les taux de change**.

La valeur dans le champ **Taux de change** de la page **Devises** est mise à jour avec le dernier taux de change des devises.

## <a name="see-also"></a>Voir aussi
[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

