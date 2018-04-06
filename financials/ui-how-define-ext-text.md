---
title: "Ajouter des lignes supplémentaires pour définir le texte étendu d'une description d'article | Microsoft Docs"
description: "Vous pouvez ajouter des lignes supplémentaires pour étendre le texte standard qui décrit un article."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7f83b9fa8803e3b6611e0167a972c0e54f5eff79
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="adding-extended-item-text"></a>Ajout de texte d'article étendu
Vous pouvez étendre un texte standard pour les articles en ajoutant des lignes supplémentaires et vous pouvez définir des conditions d'utilisation concernant ces lignes supplémentaires. Vous devez effectuer cette opération à partir des fiches article.

## <a name="to-define-extended-text-for-an-item-description"></a>Pour définir le texte étendu pour une description de l'article
1. Ouvrez la fiche correspondant à l'article auquel vous voulez ajouter du texte étendu, puis sélectionnez **Texte étendu**.
2. Dans le champ **Code**, entrez le premier code, puis, dans le champ **Désignation**, entrez le texte souhaité.
3. Choisissez **Textes étendus**.
4. Renseignez les lignes de la fenêtre **Texte étendu** avec du texte supplémentaire.
5. Renseignez le champ **Code langue** ou le champ **Commun toutes langues** si vous utilisez des codes langue.
6. Renseignez les champs **Date début** et **Date fin** si vous souhaitez limiter les dates d'utilisation du texte étendu.
7. Cochez les cases appropriées pour les types de documents où vous souhaitez imprimer le texte étendu.
8. Fermez la fenêtre.

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Pour ajouter un texte d'article étendu à une ligne commande vente
1. Ouvrez une commande vente avec une ligne vente pour un article qui a étendu le texte défini. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
2. Sélectionnez la ligne en question, puis sélectionnez l'action **Insérer textes étendus**.

## <a name="see-also"></a>Voir aussi
[Configuration de stock](inventory-setup-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

