---
title: Créer une commande vente client et vendre des produits
description: Décrit comment créer une commande vente pour enregistrer votre contrat avec un client pour vendre ou commercialiser des produits dans des conditions spécifiques.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 11/03/2023
ms.author: bholtorf
---
# Vente de produits avec une commande vente client

Cet article fournit des conseils aux utilisateurs sur le moment d’utiliser une commande vente plutôt qu’une simple facture. Si votre processus de vente exige que vous ne livriez que partiellement une commande, par exemple si la quantité totale n’est pas disponible d’un coup, vous devez traiter cette vente en créer une commande vente.

Vous devez également utiliser les commandes vente si vous commercialisez des articles en les livrant directement du fournisseur au client, dans ce qui est appelé une livraison directe. En savoir plus sur [Créer des livraisons directes](sales-how-drop-shipment.md). Pour tous les autres aspects, les commandes vente fonctionnent de la même manière que les factures vente. En savoir plus sur [Facturer des ventes](sales-how-invoice-sales.md).

Lorsque vous fournissez les produits, entièrement ou partiellement, vous validez la commande vente comme étant expédiée ou expédiée et facturée pour créer l’article et les écritures comptables client associés dans votre système. Lorsque vous validez la commande vente, vous pouvez également envoyer par e-mail le document en pièce jointe au format PDF. Vous pouvez faire en sorte que le corps du message soit prérempli avec un résumé des informations de commande et de paiement, par exemple un lien vers Paypal. En savoir plus sur [Expédier des articles](warehouse-how-ship-items.md) et [Envoyer des documents par e-mail](ui-how-send-documents-email.md).

Dans les environnements d’entreprise où le client paie immédiatement, comme par PayPal ou en espèces, le paiement est enregistré immédiatement lorsque vous validez la facture vente, c’est-à-dire la facture vente validée est clôturée comme entièrement lettrée. Vous sélectionnez la méthode appropriée dans le champ **Code mode de règlement** de la commande vente. Reportez-vous à l’étape 5 ci-dessous. Pour les paiements électroniques, tels que PayPal, vous devez également renseigner le champ **Service de paiement**. En savoir plus, [Activer les paiements client via les services de paiement](sales-how-enable-payment-service-extensions.md).

Vous pouvez même créer des commandes à paiement direct pour les clients non enregistrés en configurant une fiche « client en espèces », vers laquelle vous pointez sur la commande vente. En savoir plus sur [Configurer les clients effectuant un achat au comptoir](finance-how-to-set-up-cash-customers.md).

## Créer une commande vente

> [!NOTE]  
> La procédure suivante suppose que le client est déjà configuré. Pour obtenir des instructions sur la façon de procéder, voir [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez **Nouveau** pour créer une écriture.
3. Dans le champ **Client**, entrez le nom d’un client existant.

    D’autres champs de la page **Commande vente** sont désormais renseignés avec les informations standard sur le client sélectionné.  

4. Renseignez les champs restants de la page **Commande vente**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si vous autorisez le client à payer immédiatement, par exemple, par carte de crédit ou par PayPal, renseignez le champ **Code mode de règlement**. Le paiement est ensuite enregistré dès que vous validez la commande vente comme facturée. Si vous sélectionnez *Espèces*, le paiement est enregistré dans un compte contrepartie spécifié.

    Vous êtes maintenant prêt à renseigner les lignes commande vente avec les articles en stock ou les services que vous voulez vendre au client.

    Si vous avez défini des lignes vente récurrentes pour le client, tel qu’un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la commande par l’intermédiaire de l’action **Extraire les lignes vente récurrentes**.
5. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.

6. Dans le champ **N°**, saisissez le numéro d’un article de stock ou d’un service.

    Laissez le champ **N°** vide si la ligne est destinée à un :

    * Commentaire. Saisissez le commentaire dans le champ **Description**.
    * Article de catalogue. Sélectionnez l’action **Sélectionner articles de catalogue**. En savoir plus sur [Utiliser des éléments de catalogue](inventory-how-work-nonstock-items.md).
7. Dans le champ **Quantité**, saisissez le nombre d’articles à vendre.

    > [!NOTE]  
    > Pour les articles de type *Ressource* ou *Service*, la quantité est une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité** de la ligne. Pour plus d’informations, reportez-vous à [Configuration d’unités article](inventory-how-setup-units-of-measure.md).

    Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Prix unitaire** multipliée par le nombre du champ **Quantité**.

    Le prix et les montants ligne sont affichés avec ou sans la Sales Tax en fonction de la valeur que vous avez sélectionné dans le champ **Prix incluant les taxes** de la fiche client.
8. Dans le champ **% remise ligne**, saisissez un pourcentage si vous souhaitez accorder au client une remise sur le produit. La valeur du champ **Montant ligne** est mise à jour en conséquence.

    Si vous avez configuré des prix article spéciaux sont définis sur le raccourci **Prix vente et remises ligne vente** dans la fiche client ou article, et après avoir satisfait aux critères de prix, le prix et le montant de la ligne vente est automatiquement mise à jour. En savoir plus, [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).
9. Pour ajouter un commentaire sur la ligne commande que le client peut afficher dans la commande vente imprimée, saisissez un commentaire sur une ligne vierge, dans le champ **Description**.  
10. Répétez les étapes 5 à 9 pour chaque article que vous souhaitez vendre au client.

    Les champs totaux sous les lignes sont automatiquement mises à jour comme vous créez ou modifiez des lignes pour afficher les montants qui seront validés en comptabilité.

    > [!NOTE]
    > Dans de très rares cas, les montants validés peuvent différer de ce qui est affiché dans les champs des totaux. Cela est généralement dû aux calculs d’arrondi par rapport à la TVA ou à la taxe sur les ventes.
    >
    > Pour vérifier les montants qui seront réellement validés, utilisez la page **Statistiques**, qui tient compte des calculs d’arrondi. Aussi, si vous choisissez l’action **Lancer**, les champs de totaux seront mis à jour pour inclure les calculs d’arrondi.  

11. Dans le champ **Montant remise facture**, vous pouvez entrer un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC**.

    Si vous définissez des remises facture pour le client et en respectant les critères de prix, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture**. Et le montant remise calculé est alors inséré dans le champ **Montant remise facture sans TVA**. En savoir plus, [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).
12. Pour expédier seulement une partie de la quantité commandée, entrez la quantité dans le champ **Qté à expédier**. La valeur est copiée automatiquement dans le champ **Qté à facturer**.

    > [!NOTE]
    > Si le champ **Avis d’expédition** est défini comme **Terminé** dans le raccourci **Expédition et facturation**, vous ne pouvez pas valider de livraisons partielles. En savoir plus sur [Traiter les livraisons partielles](sales-how-send-partial-shipments.md).
13. Pour facturer seulement une partie de la quantité expédiée, entrez la quantité dans le champ **Qté à facturer**. La quantité doit être inférieure à la valeur du champ **Qté à expédier**.  
14. Lorsque les lignes commande vente sont renseignées, sélectionnez l’action **Valider et envoyer**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

La boîte de dialogue **Valider et envoyer la confirmation** s’ouvre et indique le mode de réception de documents par défaut du client. Vous pouvez modifier le mode d’envoi en cliquant sur le bouton de recherche pour le champ **Envoyer le document à**. En savoir plus, [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).

Les écritures comptables article et client associés sont à présent créés dans votre système, et la commande vente est sortie en tant que document au format PDF. Une fois la commande vente est entièrement validée, elle est supprimée de la liste des commandes vente et remplacée par de nouveaux documents dans la liste des factures vente validées et des expéditions vente enregistrées.  

## Numéro de document externe

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## Voir aussi

[Facturation des ventes](sales-how-invoice-sales.md)  
[Validation des ventes](ui-post-sales.md)  
[Expédition des articles](warehouse-how-ship-items.md)  
[Réalisation de livraisons directes](sales-how-drop-shipment.md)  
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Imprimer la liste des prélèvements](sales-how-print-picking-list.md)  
[Traiter les livraisons partielles](sales-how-send-partial-shipments.md)  
[Stock](inventory-manage-inventory.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
