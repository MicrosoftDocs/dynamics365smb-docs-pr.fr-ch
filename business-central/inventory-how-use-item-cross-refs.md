---
title: Utiliser la table Référence externe article | Microsoft Docs
description: Si vous configurez une référence externe entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l'article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence externe**. .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/12/2019
ms.author: sgroespe
ms.openlocfilehash: 09fb7c17e2fccbd3b2ad3195cffa37493ad40f61
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/19/2019
ms.locfileid: "852278"
---
# <a name="use-item-cross-references"></a>Utiliser les références externes article
Si vous configurez une référence externe entre la désignation article que vous utilisez pour un article et la désignation que le fournisseur de cet article utilise, la désignation de l'article du fournisseur est automatiquement insérée sur les documents achat du fournisseur lorsque vous renseignez le **N° référence externe**. . La même fonctionnalité s'applique pour les numéros d'article client sur les documents vente.

Les procédures suivantes décrivent comment utiliser les références externes article côté achat. La procédure est identique côté achat.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Pour configurer une référence externe article à la description d'un article fournisseur
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.
2. Ouvrez la fiche correspondant à l'article pour lequel vous souhaitez créer une référence externe à la description de l'article que le fournisseur utilise pour cet article.
3. Choisissez l'action **Références externes**.
4. Sur une nouvelle ligne de la page **Écritures de référence externe article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Pour saisir une description de l'article d'un fournisseur sur une commande achat
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat**, puis sélectionnez le lien associé.
2. Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence externe article dans la procédure précédente.
3. Créez une ligne achat pour l'article pour lequel vous avez créé une référence externe article dans la procédure précédente.
4. Dans le champ **N° type référence externe**, sélectionnez la référence externe article que vous avez créée, puis choisissez le bouton **OK**.

Le champ **Description** de la ligne est remplacé par la description d'article du fournisseur, tel que configuré dans l'écriture référence externe article.

## <a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Inventaire](inventory-manage-inventory.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
