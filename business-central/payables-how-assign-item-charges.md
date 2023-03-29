---
title: Affecter les frais annexes aux ventes et aux achats (contient une vidéo)
description: 'Affectez les frais annexes lorsque vous avez besoin que les articles de stock comptabilisent les coûts ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez lorsque vous achetez ou vendez des articles.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 06/22/2021
ms.author: edupont
---
# Utiliser Frais annexes pour comptabiliser les coûts commerciaux supplémentaires
Pour une évaluation correcte, vos articles de stock doivent comptabiliser tous les coûts ajoutés, tels que le fret, la manutention, les assurances, et transport, que vous encourez lorsque vous achetez ou vendez des articles. Pour les achats, le coût en magasin d’un article acheté est constitué du prix d’achat au fournisseur et de tous les frais annexes directs pouvant être affectés à chacune des réceptions ou expéditions retour. Pour les ventes, il peut s’avérer aussi fondamental pour votre société de connaître le coût de l’expédition des articles vendus que le coût en magasin des articles achetés.

En plus d’enregistrer les coûts supplémentaires dans votre valeur de stock, vous pouvez utiliser la fonction Frais annexes pour qui suit :

- Identifier le coût en magasin d’un article et optimiser le réseau de distribution
- Détailler le coût ou prix unitaire d’un article à des fins d’analyse
- Inclure des rabais à partir du coût unitaire et des rabais sur ventes à partir du prix unitaire

Avant d’affecter des item Frais annexes, vous devez configurer des numéros de frais annexes pour les différents types de frais annexes, y compris dans quels comptes généraux les frais liés aux ajustements de ventes, d’achats et de stock ils sont validés. Un numéro de frais annexes contient une combinaison de groupe comptabilisation produit, de code groupe taxes, de groupe comptabilisation produit TVA et de frais annexes. Lorsque vous saisissez le numéro frais annexes dans un document achat ou vente, le compte général correspondant est récupéré sur la base du paramétrage du numéro frais annexes et des informations sur le document.

Pour les documents achat et vente, vous pouvez affecter des frais annexes de deux manières :
- Sur le document répertoriant les articles touchés par les frais annexes. En général, vous procédez ainsi pour des documents qui n’ont pas encore été entièrement validés.
- Dans une facture distincte dans laquelle vous liez les frais annexes aux expéditions ou aux réceptions validées dans lesquelles les articles liés aux frais annexes sont répertoriés.

> [!NOTE]  
>   Vous pouvez affecter des frais annexes aux commandes, aux factures, et aux avoirs, pour les deux ventes et achats. Les procédures suivantes décrivent comment utiliser les frais annexes pour une facture achat. Les étapes sont similaires pour tous les autres documents achat et vente.

## Exemple :
Cette vidéo montre comment gérer un coût d’expédition supplémentaire dans le cadre de l’évalution des coûts de stock.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## Pour configurer des numéros de frais annexes
Utilisez les numéros de frais annexes pour distinguer les différents types de frais annexes utilisés dans votre société.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Frais article**, puis choisissez le lien associé.
2. Sur la page **Frais annexes**, sélectionnez l’action **Nouveau** pour créer ligne.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Pour affecter des frais annexes directement à la facture achat pour l’article
Si vous connaissez les frais annexes au moment de valider une facture achat pour l’article, procédez comme suit.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.
2. Créez une facture achat. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).
3. Assurez-vous que la facture achat a une ou plusieurs lignes de type Article.
4. Sur une nouvelle ligne, dans le champ **Type**, sélectionnez **Frais annexes**.
5. Dans le champ **Quantité**, saisissez les unités de ces frais annexes qui vous ont été facturées.
6. Dans le champ **Coût unitaire direct**, saisissez le montant des frais annexes.
7. Renseignez les champs restants selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Dans les étapes suivantes, vous créez l’affectation réelle. Jusqu’à ce que les frais annexes soient entièrement affectés, la valeur dans le champ **Qté à affecter** est en rouge.
8. Sur le raccourci **Lignes**, cliquez sur l’action **Affectation frais annexes**.

    La page **Affectation frais annexes** s’ouvre affichant une ligne pour chaque ligne de type Article de la facture achat. Pour affecter des frais annexes à une ou plusieurs lignes facture, vous pouvez utiliser une fonction qui les affecte et les distribue pour vous ou vous pouvez renseigner manuellement le champ **Qté à affecter**. Les étapes suivantes décrivent comment utiliser la fonction Suggérer affectation frais annexes.

9. Sur la page **Affectation frais annexes**, choisissez l’action **Suggérer affectation frais annexes**.
10. S’il existe plusieurs lignes facture de type Article, choisissez l’une des quatre options de distribution.  

Si les frais annexes sont entièrement affectés, la valeur dans le champ **Qté à affecter** de la facture achat est zéro.

Les frais annexes sont maintenant affectés à la facture achat. Lorsque vous validez la réception de la facture achat, les valeurs de stock des articles sont mises à jour avec le coût des frais annexes.  

## Pour affecter des frais annexes depuis une facture distincte à la facture achat pour l’article
Si vous avez reçu une facture des frais annexes après avoir validé la réception achat d’origine, procédez comme suit.
1. Répétez les étapes 1 à 8 de [Pour affecter des frais annexes directement à la facture achat pour l’article](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Sur la page **Affectation frais annexes**, cliquez sur l’action **Extraire lignes réception**.
3. Sur la page **Lignes réception achat**, sélectionnez la réception achat validée de l’article auquel vous souhaitez affecter les frais annexes, puis choisissez le bouton **OK**.
4. Choisissez l’action **Suggérer affectation frais annexes**.

Les frais annexes de la facture achat distincte sont maintenant affectés à l’article sur la réception achat enregistrée, mettant ainsi à jour la valeur de stock de l’article avec le coût des frais annexes.

## Voir la [formation Microsoft](/training/modules/post-purchase-item-charges-dynamics-365-business-central/) associée

## Voir aussi

[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Enregistrer des achats](purchasing-how-record-purchases.md)  
[Facturer des ventes](sales-how-invoice-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
