---
title: Ajouter des lignes supplémentaires pour définir les descriptions étendues
description: Vous pouvez ajouter des lignes supplémentaires pour étendre le texte standard qui décrit un article, un compte général et d'autres données.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782333"
---
# <a name="add-extended-text"></a>Ajouter du texte étendu

Vous pouvez étendre la description des articles, des unités de stockage, des comptes généraux et des ressources en ajoutant des lignes supplémentaires en tant que texte étendu. Vous pouvez également définir des conditions d'utilisation des lignes supplémentaires.  

La section suivante décrit comment ajouter du texte étendu à une description d'un élément. Mais les mêmes étapes s'appliquent aux unités de stockage, aux comptes généraux et aux ressources.  

## <a name="to-define-extended-text-for-an-description"></a>Pour définir le texte étendu pour une description

1. Ouvrez la fiche correspondant à l'article auquel vous voulez ajouter du texte étendu, puis sélectionnez **Texte étendu**.
2. Renseignez les champs **Code** et **Désignation**.
3. Choisissez **Nouveau**.
4. Renseignez le champ **Code langue** ou activez la case à cocher **Commun toutes langues** si vous utilisez des codes langue.
5. Renseignez les champs **Date début** et **Date fin** si vous souhaitez limiter les dates d'utilisation du texte étendu.
6. Dans le champ **Texte**, entrez le texte étendu.
7. Cochez les cases appropriées pour les types de documents où vous souhaitez imprimer le texte étendu.
8. Fermez la page.

Vous pouvez maintenant ajouter ce texte étendu aux documents. La procédure suivante explique comment ajouter du texte étendu à une commande vente, mais les mêmes étapes s'appliquent à tout autre document que vous avez spécifié pour le texte étendu.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Pour ajouter un texte d'article étendu à une ligne commande vente

1. Ouvrez une commande vente avec une ligne vente pour un article qui a étendu le texte défini. Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).
2. Sélectionnez la ligne en question, puis sélectionnez l'action **Insérer textes étendus**.

## <a name="see-also"></a>Voir aussi

[Configuration de stock](inventory-setup-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
