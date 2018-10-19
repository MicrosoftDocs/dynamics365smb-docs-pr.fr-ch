---
title: "Comment configurer des unités article | Microsoft Docs"
description: "Vous pouvez définir plusieurs unités pour un article afin de pouvoir affecter des unités à l'article."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b920a3edfab41409cd8d7cf3f5e463f66268e953
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-item-units-of-measure"></a>Configuration d'unités article
Vous pouvez définir plusieurs unités pour un article afin que vous puissiez affecter des unités à l'article aux fins suivantes :

- Affectez une unité de base sur la fiche article de l'article pour définir la manière dont elle est stockée dans le stock et pour servir de base de conversion aux autres unités.
- Affectez d'autres unités pour les documents d'achat, de production, ou de vente pour spécifier le nombre d'unités de base que vous gérez dans ces processus. Par exemple, vous pouvez acheter l'article en palettes et n'utiliser que des pièces individuelles en production.

Si un article est stocké dans une unité mais produit dans une autre, un ordre de fabrication utilisant une unité de lot de fabrication est créé pour calculer la quantité correcte des composants durant le traitement par lots **Actualiser O.F.**. Une situation dans laquelle un article fabriqué est stocké en pièces mais produit en tonnes est un exemple d'un calcul d'unité de lot de fabrication. Pour plus d'informations, voir [Utiliser les unités de lot de fabrication](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Pour configurer une unité
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.
2. Ouvrez la fiche article pour laquelle vous souhaitez configurer des unités de remplacement.
3. Choisissez l'action **Unités de mesure**. La fenêtre **Unités article** s'ouvre.
4. Si le champ **Unité de base** de la fiche article est renseigné, cette unité est déjà installée.
5. Sélectionnez l'action **Nouveau**. Une nouvelle ligne vide est insérée.
6. Dans le champ **Code**, entrez le nom de l'unité. Sinon, sélectionnez le champ pour choisir parmi les codes unité figurant dans la base de données.
7. Dans le champ **Quantité par unité** entrez le nombre d'unités de l'unité de base que la nouvelle unité contient.
8. Répétez les étapes 5 à 7 pour définir toutes les autres unités que vous souhaitez utiliser dans les différents processus de cet article.

Vous pouvez maintenant utiliser les unités de remplacement sur les documents achat, production, et vente. Pour plus d'informations, voir Saisir des codes unité par défaut pour des transactions d'achat et de vente ou Utiliser l'unité de lot de fabrication.

## <a name="to-set-up-unit-of-measure-translations"></a>Pour configurer des traductions d'unités
Lorsque vous vendez des articles à des clients étrangers, vous pouvez être amené à indiquer l'unité dans leur langue. Pour cela, vous devez d'abord configurer les traductions d'unités nécessaires.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Unités de mesure**, puis sélectionnez le lien associé.
2. Sélectionnez le code pour lequel vous souhaitez définir des traductions, puis cliquez sur **Traductions**.
3. Dans le champ **Code langue**, sélectionnez la flèche déroulante pour visualiser la liste des codes langue disponibles. Sélectionnez le code langue pour lequel vous souhaitez entrer une traduction, puis choisissez le bouton OK pour copier le code dans le champ.
4. Dans le champ **Désignation**, saisissez le texte approprié.
5. Répétez les étapes 2 à 4 pour les codes unité et les langues pour lesquels vous souhaitez indiquer des traductions.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Pour entrer un code unité par défaut pour des transactions de ventes et d'achat
Si vous utilisez habituellement d'autres unités que l'unité de base pour vos achats et vos ventes, vous pouvez indiquer des unités distinctes. Pour cela, vous devez configurer les unités de mesure dans la fenêtre **Unités article**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.
2. Ouvrez la fiche article appropriée pour laquelle vous souhaitez indiquer un code unité par défaut pour les achats et les ventes.
3. Pour les ventes, sur le raccourci **Facturation**, dans le champ **Unité de vente**, ouvrez la fenêtre **Unités article**.
4. Pour les achats, sur le raccourci **Réapprovisionnement**, dans le champ **Unité d'achat**, ouvrez la fenêtre **Unités article**.
5. Sélectionnez le code que vous souhaitez configurer comme unité par défaut pour les ventes ou les achats respectivement, puis cliquez sur le bouton **OK**.

## <a name="see-also"></a>Voir aussi
[Utiliser les unités de lot de fabrication](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Gestion du stock](inventory-manage-inventory.md)  
[Gestion des achats](purchasing-manage-purchasing.md)  
[Gestion des ventes](sales-manage-sales.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

