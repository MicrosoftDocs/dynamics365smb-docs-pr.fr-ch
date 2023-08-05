---
title: Ajuster les coûts article manuellement
description: 'Vous pouvez ajuster manuellement l’évaluation du stock d’un article à l’aide des méthodes FIFO ou d’évaluation stock moyen, lorsque les coûts de produits changent.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 06/16/2021
ms.author: edupont
---
# Ajuster coûts et prix article
Le coût d’un article (valeur du stock) que vous achetez et vendez ultérieurement peut changer au cours de sa durée de vie, par exemple parce que des frais de transport sont ajoutés à son coût d’achat après que vous ayez vendu l’article. L’ajustement des coûts est particulièrement utile dans les situations où vous vendez des biens avant de facturer leur achat. Pour toujours connaître la valeur du stock correcte, les coûts article doivent donc être ajustés régulièrement. Cela garantit que les statistiques vente et profit sont à jour et que les indicateurs clés financiers sont corrects. Pour plus d’informations, voir [Détails de conception : modes évaluation stock](design-details-cost-adjustment.md).

En règle générale, la valeur du champ **Coût unitaire** sur la fiche article repose sur le coût standard des articles utilisant le mode évaluation stock standard. Pour les articles utilisant d’autres modes évaluation stock, la valeur repose sur le calcul du stock disponible (coûts facturés et prévus) divisé par la quantité disponible. Pour plus d’informations, voir [Comprendre le calcul du coût unitaire](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

Dans [!INCLUDE[prod_short](includes/prod_short.md)], les coûts article sont automatiquement ajustés chaque fois qu’un mouvement de stock se produit, par exemple lors de la validation d’une facture achat pour un article.

Vous pouvez également utiliser une fonction pour ajuster manuellement les coûts d’un ou de plusieurs articles. Cela est utile, par exemple, si vous savez que les coûts article ont changé pour d’autres raisons que des mouvements de stock.

Les coûts article sont ajustés selon la méthode FIFO ou d’évaluation stock moyen, selon la sélection effectuée dans le guide de configuration assistée **Configurer ma société** ou dans le champ **Mode évaluation stock** sur la fiche article. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

Si vous utilisez la méthode de coût FIFO, le coût unitaire d’un article est la valeur réelle de toute réception de l’article. Le stock est évalué avec la supposition que les premiers articles stockés sont ceux vendus en premier.

Si vous utilisez la méthode de l’évaluation stock moyen, le coût unitaire d’un article est calculé comme le coût unitaire moyen à chaque moment après un achat. Le stock est évalué avec la supposition que tous les stocks sont vendus simultanément. Pour les articles utilisant ce mode d’évaluation stock, vous pouvez choisir le champ **Coût unitaire** de la fiche article pour afficher l’historique des transactions à partir duquel est calculé le coût moyen

La fonction d’ajustement des coûts traite uniquement les écritures valeur non encore ajustées. Si la fonction est confrontée à une situation où des coûts entrants modifiés doivent être transférés à des écritures sortantes associées, de nouvelles écritures valeur ajustées sont créées, sur la base des informations des écritures valeur d’origine, mais contenant le montant de l’ajustement. La fonction d’ajustement des coûts utilise la date comptabilisation de l’écriture valeur d’origine dans l’écriture ajustée, sauf si la date est comprise dans une période inventaire clôturée. Dans ce cas, l’application utilise la date début de la période d’inventaire ouverte suivante. Si aucune période inventaire n’est utilisée, la date du champ **Début période validation** de la page **Paramètres comptabilité** définira la date de comptabilisation de l’écriture ajustée.

## Pour ajuster les coûts article manuellement
1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Ajuster coûts : Écr. article**, puis sélectionnez le lien associé.
2. Sur la page **Ajuster coûts - Écr. article**, spécifiez les articles pour lesquels ajuster les coûts.
3. Choisissez le bouton **OK**.

## Pour apporter des modifications générales au coût unitaire direct
Si vous devez modifier le coût unitaire direct de plusieurs articles, vous pouvez utiliser le traitement par lots **Ajuster coûts/prix article**.  

 Le traitement par lots modifie la valeur du champ **Prix unitaire** sur la fiche article. Le traitement par lots modifie la valeur du champ de la même manière pour tous les articles (ou pour les articles sélectionnés). Le traitement par lots multiplie la valeur du champ par un facteur appliqué que vous devez indiquer.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Ajuster coûts/prix article**, puis sélectionnez le lien associé.  
2. Dans le champ **Champ à modifier**, indiquez le champ de l’article ou de la fiche point de stock à modifier.  
3. Dans le champ **Facteur appliqué**, indiquez le facteur d’ajustement de la valeur. Par exemple, entrez **1,5** pour augmenter la valeur de 50 %.  
4. Sous le raccourci **Article**, définissez des filtres pour indiquer, par exemple, les articles à traiter avec le traitement par lots.  
5. Cliquez sur le bouton **OK**.  

## Comprendre le calcul du coût unitaire
En règle générale, la valeur du champ **Coût unitaire** sur la fiche article repose sur le coût standard des articles utilisant le mode évaluation stock standard. Pour les articles utilisant d’autres modes évaluation stock, la valeur repose sur le calcul du stock disponible (coûts facturés et prévus) divisé par la quantité disponible.  

 Pour en savoir plus sur les incidences de la valeur du champ **Mode évaluation stock** sur le calcul du coût unitaire pour les achats et les ventes, consultez les chapitres suivants.  

## Calcul du coût unitaire pour les achats  
 Lorsque vous achetez des articles, le programme copie toujours la valeur du champ **Dernier coût direct** de la fiche article vers le champ **Coût unitaire direct** d’une ligne achat ou vers la ligne Montant unitaire sur une ligne feuille article.  

 L’élément sélectionné dans le champ **Mode d’évaluation du stock** détermine la façon dont [!INCLUDE[prod_short](includes/prod_short.md)] calcule le contenu du champ **Coût unitaire** sur les lignes.  

### Modes d’évaluation du stock FIFO, LIFO, spécifique ou moyen  
 [!INCLUDE[prod_short](includes/prod_short.md)] calcule la valeur du champ **Coût unitaire DS** sur la ligne achat, ou la valeur du champ **Coût unitaire** sur la ligne feuille article sur la base de cette formule :  

 Coût unitaire DS = (Coût unitaire direct - (Montant de la remise/Quantité)) x (1 + % du coût indirect/100) + Frais généraux  

### Mode évaluation stock Standard  
 Le champ **Coût unitaire DS** sur la ligne achat, ou le champ **Coût unitaire** est renseigné sur la ligne feuille article en copiant la valeur du champ **Coût unitaire** de la fiche article. En utilisant le mode évaluation stock Standard, il repose toujours sur le coût standard.  

 Lorsque vous validez l’achat, le coût unitaire de la ligne achat ou de la ligne feuille article est copié vers l’écriture facture article d’achat, et vous pouvez la visualiser dans la liste des écritures de l’article.  

### Tous les modes évaluation stock  
 Le programme utilise toujours le coût unitaire de la ligne document origine pour calculer la valeur du champ **Coût total (réel)**, ou éventuellement du champ **Coût total (prévu)** concernant cette écriture article, quel que soit le mode évaluation stock de l’article.  

## Calcul du coût unitaire pour les ventes  
 Lorsque vous vendez des articles, le coût unitaire est copié du champ Coût unitaire de la fiche article vers la ligne vente ou la ligne feuille article.  

 Lorsque vous validez, le programme copie le coût unitaire vers l’écriture article facture vente, et il peut être vu dans la liste d’écritures de l’article. [!INCLUDE[prod_short](includes/prod_short.md)] utilise le coût unitaire de la ligne document origine pour calculer la valeur du champ **Coût total (réel)**, ou éventuellement du champ **Coût total (prévu)** dans l’écriture valeur concernant cette écriture article.  

## Voir aussi
[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Stock](inventory-manage-inventory.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]