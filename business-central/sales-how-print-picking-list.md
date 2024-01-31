---
title: Imprimer la liste des prélèvements à partir d’une commande vente
description: 'Vous pouvez imprimer une liste des prélèvements des stocks directement à partir d’une commande client, des ventes, de la facture et d’autres documents de vente sortants.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Imprimer la liste des prélèvements

Vous pouvez imprimer une liste des prélèvements de stock directement à partir d’une commande client ou d’autres documents qui déclenchent l’expédition des articles.

Cet état est généralement utilisé dans les entreprises sans fonctionnalité dédiée à la gestion des entrepôts, de sorte qu’un magasinier peut afficher ou imprimer la liste des prélèvements à partir du document de vente associé. Dans les entreprises avec un volume plus élevé ou des processus plus complexes, l’expédition et le prélèvement sont planifiés et effectués dans des documents d’entrepôt dédiés. Learn more at [Flux de désenlogement](design-details-outbound-warehouse-flow.md).

## Pour imprimer la liste des prélèvements à partir d’une commande vente

La procédure suivante se base sur une commande vente. Les étapes sont similaires pour tous les autres documents pouvant être utilisés pour lancer l’expédition d’articles, par exemple un ordre transfert.

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Rechercher une page ou un état") entrez **Commandes vente**, puis sélectionnez le lien associé.  
2. Ouvrez une commande vente pour laquelle vous souhaitez sélectionner des articles.  
3. Choisir l’action **Rapport**, puis choisissez l’action **Liste de prélèvement par ordre**.  
4. Sélectionnez le bouton **Imprimer** pour imprimer la liste de prélèvements, ou le bouton **Aperçu** pour l’afficher à l’écran.

Vous pouvez également enregistrer la liste des prélèvements en tant que document, par exemple, pour l’envoyer à quelqu’un ou pour l’ajouter en tant que pièce jointe à la commande client. Learn more at [Gérer les pièces jointes, les liens et les notes sur les fiches et les documents](ui-how-add-link-to-record.md).

> [!NOTE]
> Si vous avez utilisé la fonction **Éclater nomenclature** sur la commande client, seuls les composants de l’élément d’assemblage associé sont affichés dans le rapport. Learn more at [Utiliser les nomenclatures](inventory-how-work-BOMs.md).

## Voir aussi

[Stock](inventory-manage-inventory.md)  
[Flux de désenlogement](design-details-outbound-warehouse-flow.md)
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
