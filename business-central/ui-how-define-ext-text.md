---
title: Ajouter des lignes supplémentaires pour définir les descriptions d'article étendues | Microsoft Docs
description: Vous pouvez ajouter des lignes supplémentaires pour étendre le texte standard qui décrit un article.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a43cca28bb24c5723d81ca28a3d1f86a38f5ad7c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248431"
---
# <a name="add-extended-item-text"></a>Ajouter un texte d'article étendu
Vous pouvez étendre un texte standard pour les articles en ajoutant des lignes supplémentaires et vous pouvez définir des conditions d'utilisation concernant ces lignes supplémentaires. Vous devez effectuer cette opération à partir des fiches article.

## <a name="to-define-extended-text-for-an-item-description"></a>Pour définir le texte étendu pour une description de l'article
1. Ouvrez la fiche correspondant à l'article auquel vous voulez ajouter du texte étendu, puis sélectionnez **Texte étendu**.
2. Renseignez les champs **Code** et **Désignation**.
3. Choisissez **Nouveau**.
4. Renseignez le champ **Code langue** ou activez la case à cocher **Commun toutes langues** si vous utilisez des codes langue.
5. Renseignez les champs **Date début** et **Date fin** si vous souhaitez limiter les dates d'utilisation du texte étendu.
6. Dans le champ **Texte**, entrez le texte étendu.
7. Cochez les cases appropriées pour les types de documents où vous souhaitez imprimer le texte étendu.
8. Fermez la page.

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Pour ajouter un texte d'article étendu à une ligne commande vente
1. Ouvrez une commande vente avec une ligne vente pour un article qui a étendu le texte défini. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
2. Sélectionnez la ligne en question, puis sélectionnez l'action **Insérer textes étendus**.

## <a name="see-also"></a>Voir aussi
[Configuration de stock](inventory-setup-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
