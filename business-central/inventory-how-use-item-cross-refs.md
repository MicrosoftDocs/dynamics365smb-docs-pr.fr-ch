---
title: Utiliser références article
description: 'Configurez des références entre les descriptions, les unités et les variantes que vous et votre fournisseur ou client utilisez pour un article.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/02/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Utiliser références article

Si vous achetez ou vendez des articles pour lesquels vous et votre fournisseur ou client utilisez des termes différents, vous pouvez définir une référence entre vos termes pour les articles et les termes que le client ou le fournisseur de cet article utilise. De cette façon, la description de l’article du fournisseur ou du client, l’unité ou le code variante est automatiquement inséré sur les documents pertinents lorsque vous remplissez le **Numéro de référence de l’article** .  

## Pour configurer une référence article

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Articles**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un article pour lequel vous voulez créer une référence.
3. Sélectionnez l’action **Références article**.

     Si vous ne trouvez pas l’action **Références article**, choisissez d’afficher plus d’options, puis recherchez-la sous **Association** > **Article**.
  
4. Sur une nouvelle ligne de la page **Écritures de référence article**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

La procédure suivante décrit comment spécifier la référence article sur une Commande achat. Les mêmes étapes s’appliquent aux documents vente et autres documents achat.  

## Pour saisir une description de l’article d’un fournisseur sur un document

1. Choisissez l’icône :::image type="icon" source="media/ui-search/search_small.png" border="false":::, entrez **Commandes achat**, puis choisissez le lien associé.
2. Créez une commande achat pour le fournisseur pour lequel vous avez créé une référence article dans la procédure précédente.
3. Créez une ligne achat pour l’article pour lequel vous avez créé une référence article dans la procédure précédente.
4. Dans le champ **N° référence article**, sélectionnez la référence article pertinente, puis choisissez le bouton **OK**.

Le champ **Description** de la ligne est remplacé par la description d’article du fournisseur, telle que configurée dans l’écriture référence article. Si la référence article comprend un code variante ou une unité, ces valeurs sont également copiées dans le document.  

## Scanner les codes-barres avec l’application mobile Business Central

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Le tableau suivant répertorie les pages qui prennent en charge la numérisation des codes-barres des références d’articles de l’application mobile [!INCLUDE [prod_short](includes/prod_short.md)].

|Page  |Valeur du champ que vous pouvez scanner  |
|---------|---------|
|Référence d’article     | N° référence        |
|Ligne feuille article     | N° référence article        |
|Ligne commande de stock physique     |N° référence article         |
|Ligne achat     |   N° référence article      |
|Ligne vente     | N° référence article        |

## Voir aussi

[Enregistrement des nouveaux articles](inventory-how-register-new-items.md)  
[Stock](inventory-manage-inventory.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
