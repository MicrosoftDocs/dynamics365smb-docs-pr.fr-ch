---
title: Annuler la validation d’assemblage
description: Découvrez comment corriger les erreurs dans un ordre d’assemblage validé.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# Annuler la validation d’assemblage

Annulez la validation d’un ordre d’assemblage pour corriger une erreur ou supprimer une validation indésirable.

Lorsque vous annulez un ordre d’assemblage validé, des écritures comptables article de correction sont créées pour contrepasser les écritures d’origine. Chaque écriture production positive pour l’élément d’assemblage est contrepassée par une écriture production négative. Chaque écriture production négative pour un composant d’assemblage est contrepassée par une écriture production positive. Le lettrage des coûts fixes est créé automatiquement entre les écritures de correction et les écritures d’origine afin de garantir une inversion de même coût.  

Lorsque vous annulez un ordre d’assemblage entièrement validé, vous pouvez recréer l’ordre d’origine. Par exemple, pour apporter des corrections avant de le valider à nouveau.  

Lorsque vous annulez un ordre d’assemblage partiellement validé, tous les champs de quantité concernés, notamment les champs **Quantité assemblée**, **Quantité consommée** et **Quantité restante** sont restaurés avec leur valeur précédant la validation.  

Pour recréer ou restaurer des ordres d’assemblage, l’article de la validation d’origine doit respecter les conditions suivantes :  

* Il est toujours en stock. Autrement dit, il n’a pas été vendu ni autrement consommé par des transactions sortantes.  
* Il n’est pas réservé.  
* Il doit exister dans l’emplacement dans lequel il a été produit.  

Les ordres d’assemblage ne peuvent être restaurés que si le numéro et la séquence des lignes de l’ordre d’assemblage n’ont pas été modifiés.  

> [!TIP]  
> Pour résoudre les conflits dus à des modifications des lignes, vous pouvez rétablir manuellement les modifications sur les lignes en question avant d’annuler l’ordre d’assemblage validé. Vous pouvez valider l’ordre d’assemblage, puis le recréer lorsque vous annulez la validation.  

La procédure suivante décrit comment annuler les ordres d’assemblage validés qui contiennent des articles assemblés pour stock. Pour annuler des ordres d’assemblage validés avec des articles qui ont été assemblés pour commande, utilisez l’action **Annuler l’expédition** sur l’expédition validée associée. Pour en savoir plus sur l’annulation des expéditions, consultez [Inverser des validations feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md). L’annulation de l’ordre d’assemblage validé se déroule de la même manière que celle décrite dans cet article.  

## Pour annuler la validation d’un ordre d’assemblage

Vous pouvez annuler des ordres d’assemblage entièrement ou partiellement validés.

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Ordres d’assemblage validés**, puis sélectionnez le lien associé.  

   Chaque validation partielle crée un ordre d’assemblage validé distinct.  
2. Ouvrez l’ordre d’assemblage validé que vous souhaitez annuler, puis choisissez **Annuler l’assemblage**.  

    Si l’ordre d’assemblage validé est lié à un ordre d’assemblage entièrement validé qui a été supprimé, vous pouvez recréer l’ordre supprimé. Par exemple, vous pouvez recréer l’ordre parce que vous souhaitez le retraiter.  
3. Pour recréer l’ordre d’assemblage, choisissez **Oui**. Pour annuler la validation sans recréer l’ordre d’assemblage associée, choisissez **Non**.  

Le champ **Contrepassé** de l’ordre d’assemblage prend la valeur **Oui**. La validation de l’ordre d’assemblage est maintenant annulée. Vous pouvez traiter l’intégralité de l’ordre d’assemblage si vous avez choisi de le recréer, ou l’ordre d’assemblage ouvert que vous avez restauré à son état d’origine.  

> [!NOTE]  
> Pour restaurer les quantités de plusieurs validations partielles dans un ordre d’assemblage, vous devez annuler tous les ordres d’assemblage validés en suivant les étapes 1 à 3.  

## Voir aussi

[Gestion des assemblages](assembly-assemble-items.md)  
[Inverser des validations feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md)  
[Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md)  
[Utilisation des nomenclatures d’assemblage](assembly-how-work-assembly-boms.md)  
[Stock](inventory-manage-inventory.md)  
[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]