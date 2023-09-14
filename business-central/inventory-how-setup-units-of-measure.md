---
title: Comment configurer des unités article | Microsoft Docs
description: Vous pouvez définir plusieurs unités pour un article afin de pouvoir affecter des unités à l’article.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2021
ms.author: bholtorf
---
# Configuration d’unités

Dans le cadre de la configuration de votre [!INCLUDE [prod_short](includes/prod_short.md)], vous définissez des unités générales sur la page **Unités**. Ensuite, lorsque vous enregistrez de nouveaux articles, vous spécifiez l’unité de base sur la **Fiche article**. Mais vous pouvez également ajouter des unités ultérieurement.  

Vous pouvez définir plusieurs unités pour un article afin que vous puissiez affecter des unités à l’article aux fins suivantes :

- Affectez une unité de base sur la fiche article de l’article pour définir la manière dont elle est stockée dans le stock et pour servir de base de conversion aux autres unités.
- Affectez d’autres unités pour les documents d’achat, de production, ou de vente pour spécifier le nombre d’unités de base que vous gérez dans ces processus. Par exemple, vous pouvez acheter l’article en palettes et n’utiliser que des pièces individuelles en production.

Si un article est stocké dans une unité mais produit dans une autre, un ordre de fabrication utilisant une unité de lot de fabrication est créé pour calculer la quantité correcte des composants durant le traitement par lots **Actualiser O.F.**. Une situation dans laquelle un article fabriqué est stocké en pièces mais produit en tonnes est un exemple d’un calcul d’unité de lot de fabrication. Pour plus d’informations, voir [Utiliser les unités de lot de fabrication](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

Un autre outil qui facilite l’utilisation de plusieurs unités de mesure pour les articles est la possibilité de spécifier une précision d’arrondi pour les unités de mesure de base. La spécification d’une précision d’arrondi fournit des indications sur ce qu’une personne doit saisir pour un processus métier donné et aide à atténuer les problèmes d’arrondi. Lorsque vous utilisez d’autres unités de mesure, la valeur dans le champ **Qté. par unité** permet de calculer la quantité dans l’unité de mesure de base, ce qui peut entraîner des problèmes d’arrondi. Par exemple, imaginez que vous recevez une boîte contenant six articles. Lorsque la boîte arrive à votre entrepôt, vous découvrez qu’il manque l’un des six articles. Vous décidez de ne pas valider la réception d’une boîte, mais de modifier à la place la quantité reçue à cinq des six pièces. Cela conduirait à une réception de 4,99998 pièces au lieu de cinq. Sur la page **Unités article**, le champ **Précision arrondi quantité** vous permet de spécifier une valeur qui convertira la quantité en un nombre plus facile à comprendre. En continuant avec l’exemple, nous entrons **1** dans le champ pour arrondir la valeur à cinq pièces.

## Pour configurer des unités

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Unités de mesure**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. Une nouvelle ligne vide est insérée.  
3. Remplissez les champs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Si vous savez que votre organisation vendra des articles avec cette unité à des clients dans d’autres pays/régions, vous pouvez ajouter des traductions.  
    1. Sélectionnez le code pour lequel vous souhaitez définir des traductions, puis cliquez sur **Traductions**.
    2. Dans le champ **Code langue**, sélectionnez la flèche déroulante pour visualiser la liste des codes langue disponibles. Sélectionnez le code langue pour lequel vous souhaitez entrer une traduction, puis choisissez le bouton OK pour copier le code dans le champ.
    3. Dans le champ **Désignation**, saisissez le texte approprié.
5. Répétez les étapes précédentes pour toutes les unités supplémentaires que vous souhaitez ajouter.  

Lorsque vous enregistrez un nouvel article, vous pouvez choisir l’unité de base dans la liste des unités que vous avez maintenant configurée. Vous pouvez également configurer plusieurs unités pour un article.  

## Pour configurer plusieurs unités article

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche article pour laquelle vous souhaitez configurer des unités de remplacement.
3. Choisissez l’action **Unités de mesure**. La page **Unités article** s’ouvre.
4. Si le champ **Unité de base** de la fiche article est renseigné, cette unité est déjà installée.
5. Sélectionnez l’action **Nouveau**. Une nouvelle ligne vide est insérée.
6. Dans le champ **Code**, entrez le nom de l’unité. Sinon, sélectionnez le champ pour choisir parmi les codes unité figurant dans la base de données.
7. Dans le champ **Quantité par unité** entrez le nombre d’unités de l’unité de base que la nouvelle unité contient.
8. Éventuellement, dans les champs **Hauteur**, **Largeur**, **Longueur** et **Poids**, spécifiez des informations précises sur la taille des unités de manière à ce que [!INCLUDE [prod_short](includes/prod_short.md)] puisse calculer le nombre d’unités article pouvant être placées dans un emplacement donné. Le champ **Cubage** est calculé automatiquement en fonction de la **Hauteur**, **Largeur** et **Longueur**.

    Si l’un de ces champs contient une valeur autre que 0, cette mesure est utilisée pendant tous les processus qui impliquent le placement d’articles dans un emplacement : rangement, mouvements, réceptions, expéditions, prélèvements et ajustements. [!INCLUDE [prod_short](includes/prod_short.md)] compare la somme de chaque mesure physique des articles rangés ajoutés à ceux qui se trouvent déjà dans l’emplacement à la taille maximum ou à l’autre mesure qui peut être logée dans un emplacement, en fonction de la capacité de l’emplacement sur la fiche magasin pour cet article. En d’autres termes, vous devez utiliser la même mesure unitaire pour chaque dimension dans toutes les unités article ; utilisez des kilogrammes ou des livres pour le poids, par exemple, mais soyez cohérent.
9. Répétez les étapes 5 à 7 pour définir toutes les autres unités que vous souhaitez utiliser dans les différents processus de cet article.

    Dans le champ **Unité de base** situé au bas de la fenêtre, vous pouvez visualiser ou modifier l’unité de base de l’article. Vous pouvez également modifier l’unité de base dans le champ **Unité de base** de la fiche article. Sur la page **Unités article**, l’unité de base doit avoir la valeur **1** dans le champ **Qté par unité**.

Vous pouvez maintenant utiliser les unités de remplacement sur les documents achat, production, et vente. Pour plus d’informations, consultez [Pour entrer un code unité par défaut pour des transactions de ventes et d’achat](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## Pour configurer des traductions d’unités

Lorsque vous vendez des articles à des clients étrangers, vous pouvez être amené à indiquer l’unité dans leur langue. Vous pouvez le faire en spécifiant des traductions pour les unités de mesure.

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Unités de mesure**, puis choisissez le lien associé.
2. Sélectionnez le code pour lequel vous souhaitez définir des traductions, puis cliquez sur **Traductions**.
3. Dans le champ **Code langue**, sélectionnez la flèche déroulante pour visualiser la liste des codes langue disponibles. Sélectionnez le code langue pour lequel vous souhaitez entrer une traduction, puis choisissez le bouton OK pour copier le code dans le champ.
4. Dans le champ **Désignation**, saisissez le texte approprié.
5. Répétez les étapes 2 à 4 pour les codes unité et les langues pour lesquels vous souhaitez indiquer des traductions.

## Pour entrer un code unité par défaut pour des transactions de ventes et d’achat

Si vous utilisez habituellement d’autres unités que l’unité de base pour vos achats et vos ventes, vous pouvez indiquer des unités distinctes. Pour cela, vous devez configurer les unités sur la page **Unités article**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche article appropriée pour laquelle vous souhaitez indiquer un code unité par défaut pour les achats et les ventes.
3. Pour les ventes, sur le raccourci **Facturation**, dans le champ **Unité de vente**, ouvrez la page **Unités article**.
4. Pour les achats, sur le raccourci **Réapprovisionnement**, dans le champ **Unité d’achat**, ouvrez la page **Unités article**.
5. Sélectionnez le code que vous souhaitez configurer comme unité par défaut pour les ventes ou les achats respectivement, puis cliquez sur le bouton **OK**.

## Voir la [formation Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) associée

## Voir aussi

[Utiliser les unités de lot de fabrication](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Gestion du stock](inventory-manage-inventory.md)  
[Gestion des achats](purchasing-manage-purchasing.md)  
[Gestion des ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
