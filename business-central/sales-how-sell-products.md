---
title: Créer une commande vente et vendre des produits | Microsoft Docs
description: Décrit comment créer une commande vente pour enregistrer votre contrat avec un client pour vendre ou commercialiser des produits dans des conditions spécifiques.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 19b32e8faa6b9e56505379d1f06fd5ad79466614
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115530"
---
# <a name="sell-products"></a>Vendre des produits

Vous créez une commande vente ou une facture vente pour enregistrer votre accord avec un client pour vendre certains produits selon certaines conditions de livraison et de paiement.

> [!NOTE]  
> Utilisez des commandes vente si votre processus de vente requiert que vous expédiiez des parties d’une quantité de commande, par exemple, si la quantité totale est pas disponible d’un coup. Si vous utilisez des factures vente, alors [!INCLUDE [prod_short](includes/prod_short.md)] suppose que vous expédiez la quantité complète lorsque vous validez la facture. Si vous commercialisez des articles en les livrant directement du fournisseur au client, vous devez également utiliser les commandes vente. Pour plus d’informations, voir [Effectuer des livraisons directes](sales-how-drop-shipment.md). Pour tous les autres aspects, les commandes vente fonctionnent de la même manière que les factures vente. Pour plus d’informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).

Vous pouvez négocier avec le client en créant d’abord un devis, que vous pouvez convertir en commande vente lorsque vous êtes d’accord sur la vente. Pour plus d’informations, voir [Créer des devis](sales-how-make-offers.md).

Une fois que le client a confirmé l’accord, par exemple après une procédure de devis, vous pouvez envoyer une confirmation de commande pour enregistrer votre obligation de fournir les produits comme convenu.

Lorsque vous fournissez les produits, entièrement ou partiellement, vous validez la commande vente comme étant expédiée ou expédiée et facturée pour créer l’article et les écritures comptables client associés dans votre système. Lorsque vous validez la commande vente, vous pouvez également envoyer par e-mail le document en pièce jointe au format PDF. Vous pouvez faire en sorte que le corps du message soit prérempli avec un résumé des informations de commande et de paiement, par exemple un lien vers Paypal. Pour plus d’informations, voir [Envoyer des documents par e-mail](ui-how-send-documents-email.md).

Dans les environnements d’entreprise où le client paie un certain temps après la livraison, conformément aux conditions de paiement, une facture vente validée reste ouverte (impayée) jusqu’à ce que le département Comptabilité client vérifie la réception du paiement et lettre le paiement à la facture vente validée. Pour plus d’informations, voir [Rapprocher les paiements à l’aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).

Dans les environnements d’entreprise où le client paie immédiatement, par exemple par PayPal ou en espèces, le paiement est enregistré immédiatement lorsque vous validez la commande vente comme facturée, c’est-à-dire la facture vente validée est clôturée comme entièrement lettrée. Vous sélectionnez la méthode appropriée dans le champ **Code mode de règlement** de la commande vente. Voir l’étape 8. Pour les paiements électroniques, tels que PayPal, vous devez également renseigner le champ **Service de paiement**. Pour plus d’informations, voir [Activer les paiements client via les services de paiement](sales-how-enable-payment-service-extensions.md).

Vous pouvez même créer des commandes à paiement direct pour les clients non enregistrés en configurant une fiche « client en espèces », vers laquelle vous pointez sur la commande vente. Pour plus d’informations, reportez-vous à [Configurer des clients effectuant un achat au comptoir](finance-how-to-set-up-cash-customers.md).

Vous pouvez facilement corriger ou annuler une facture vente validée qui résulte d’une commande vente avant qu’elle soit payée. Cela est utile si vous souhaitez corriger une erreur de saisie, ou si le client demande une modification tôt dans le processus de commande. Pour plus d’informations, voir [Corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md). Si la facture vente validée est payée, vous devez créer un avoir vente pour contrepasser la vente. Pour plus d’informations, reportez-vous à [Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).

La fiche article peut être de type **Stock**, **Service** et **Hors stock** pour spécifier si l’article est une unité de stock physique, une unité de temps de travail ou une unité physique qui n’est pas conservée dans le stock. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md). Le processus de commande vente est identique pour les trois types d’article.

Vous pouvez remplir les champs relatifs au client sur la commande vente de deux façons selon que le client est déjà enregistré ou non. Reportez-vous à l’étape 2 de la procédure ci-dessous.

## <a name="to-create-a-sales-order"></a>Pour créer une commande vente

1. Choisissez l’icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.
2. Dans le champ **Client**, entrez le nom d’un client existant.

    D’autres champs de la page **Commande vente** sont désormais renseignés avec les informations standard sur le client sélectionné.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]  

    Plusieurs champs de la commande vente sont désormais renseignés avec les informations que vous avez spécifiées sur la nouvelle fiche client.
3. Renseignez les champs restants de la page **Commande vente**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si vous autorisez le client à payer immédiatement, par exemple, par carte de crédit ou par PayPal, renseignez le champ **Code mode de règlement**. Le paiement est ensuite enregistré dès que vous validez la commande vente comme facturée. Si vous sélectionnez ESPÈCES, le paiement est enregistré dans un compte contrepartie spécifié.

    Vous êtes maintenant prêt à renseigner les lignes commande vente avec les articles en stock ou les services que vous voulez vendre au client.

    Si vous avez défini des lignes vente récurrentes pour le client, tel qu’un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la commande par l’intermédiaire de l’action **Extraire les lignes vente récurrentes**.
4. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.

5. Dans le champ **N°**, saisissez le numéro d’un article de stock ou d’un service.

    Laissez le champ **N°** vide dans les cas suivants :

    * Si la ligne est destinée à un commentaire. Saisissez le commentaire dans le champ **Description**.
    * Si la ligne est destinée à un article de catalogue. Sélectionnez l’action **Sélectionner articles de catalogue**. Pour en savoir plus, voir [Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md).
6. Dans le champ **Quantité**, saisissez le nombre d’articles à vendre.

    > [!NOTE]  
    > Pour les articles de type *Ressource* ou *Service*, la quantité est une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité** de la ligne. Pour plus d’informations, reportez-vous à [Configuration d’unités article](inventory-how-setup-units-of-measure.md).

    Le champ **Montant ligne** est mis à jour pour indiquer la valeur du champ **Prix unitaire** multipliée par la valeur du champ **Quantité**.

    Le prix et les montants ligne sont affichés avec ou sans la Sales Tax en fonction de la valeur que vous avez sélectionné dans le champ **Prix incluant les taxes** de la fiche client.
7. Dans le champ **% remise ligne**, saisissez un pourcentage si vous souhaitez accorder au client une remise sur le produit. La valeur du champ **Montant ligne** est mise à jour en conséquence.

    Si vous avez défini des prix article spéciaux sur le raccourci **Prix vente et remises ligne vente** dans la fiche client ou article, le prix et le montant de la ligne devis sont automatiquement mis à jour si les critères de prix convenus sont réunis. Pour plus d’informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).
8. Pour ajouter un commentaire sur la ligne devis que le client peut afficher dans le devis vente imprimé, saisissez un texte dans le champ **Description** sur une ligne vierge.  
9. Répétez les étapes 4 à 8 pour chaque article que vous souhaitez à vendre au client.

    Les champs totaux sous les lignes sont automatiquement mises à jour comme vous créez ou modifiez des lignes pour afficher les montants qui seront validés en comptabilité.

    > [!NOTE]
    > Dans de très rares cas, les montants validés peuvent différer de ce qui est affiché dans les champs des totaux. Cela est généralement dû aux calculs d’arrondi par rapport à la TVA ou à la taxe sur les ventes.
    >
    > Pour vérifier les montants qui seront réellement validés, utilisez la page **Statistiques**, qui tient compte des calculs d’arrondi. Aussi, si vous choisissez l’action **Lancer**, les champs de totaux seront mis à jour pour inclure les calculs d’arrondi.  

10. Dans le champ **Montant remise facture**, vous pouvez entrer un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC**.

    Si vous avez défini des remises facture pour le client, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture** si les critères sont réunis, et le montant associé est inséré dans le champ **Montant remise facture sans TVA**. Pour plus d’informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).
11. Pour expédier seulement une partie de la quantité commandée, entrez la quantité dans le champ **Qté à expédier**. La valeur est copiée dans le champ **Qté à facturer**.
12. Pour facturer seulement une partie de la quantité expédiée, entrez la quantité dans le champ **Qté à facturer**. La quantité doit être inférieure à la valeur du champ **Qté à expédier**.  
13. Lorsque les lignes commande vente sont renseignées, sélectionnez l’action **Valider et envoyer**.

La boîte de dialogue **Valider et envoyer la confirmation** s’ouvre et indique le mode de réception de documents par défaut du client. Vous pouvez modifier le mode d’envoi en cliquant sur le bouton de recherche pour le champ **Envoyer le document à**. Pour plus d’informations, reportez vous à [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).

Les écritures comptables article et client associés sont à présent créés dans votre système, et la commande vente est sortie en tant que document au format PDF. Lorsque la commande vente est entièrement validée, elle est supprimée de la liste des commandes vente et remplacée par de nouveaux documents dans la liste des factures vente validées et la liste des expéditions vente enregistrées.  

## <a name="external-document-number"></a>Numéro de document externe

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Imprimer la liste des prélèvements](sales-how-print-picking-list.md)  
[Stock](inventory-manage-inventory.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]