---
title: Facturer des ventes
description: 'Décrit comment créer une facture vente ou une commande vente, enregistrer votre contrat avec un client pour vendre des produits dans des conditions spécifiques.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="invoice-sales"></a>Facturer des ventes

Vous pouvez généralement créer une commande vente ou une facture vente pour enregistrer votre accord avec un client pour vendre certains produits selon certaines conditions de livraison et de paiement.  

Cependant, vous devez utiliser une commande vente au lieu d’une facture vente si vous :  

* Vous devez expédier uniquement une partie d’une quantité de commande, par exemple, si la quantité totale n’est pas disponible.  
* Expédiez des produits après avoir validé les factures vente correspondantes.
* Vendez des articles que votre fournisseur fournit directement à votre client (une livraison directe). En savoir plus sur [Créer des livraisons directes](sales-how-drop-shipment.md).  

Pour toutes les autres situations, les commandes vente et les factures vente fonctionnent de la même manière. Pour plus d’informations sur l’utilisation des commandes vente, reportez-vous à [Vendre des produits](sales-how-sell-products.md).

Vous pouvez négocier avec le client en créant d’abord un devis, que vous pouvez convertir en facture vente ou en commande vente lorsque vous êtes d’accord sur la vente. En savoir plus, [Créer des devis](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Créer des factures vente

Si le client décide d’acheter, vous validez la facture vente pour créer les écritures quantité et valeur associées. Lorsque vous validez la facture vente, vous pouvez également envoyer par e-mail le document en pièce jointe au format PDF. Vous pouvez faire en sorte que le corps du message soit prérempli avec un résumé des informations de facturation et de paiement, par exemple un lien vers Paypal. En savoir plus sur [Envoyer des documents par e-mail](ui-how-send-documents-email.md). Lorsque le client paie la facture, vous pouvez enregistrer ce paiement de différentes manières, selon la taille et les flux de travail favoris de votre organisation. En savoir plus sur la section [Enregistrement des paiements](#registering-payments).  

Les fiches article peuvent être de type **Stock**, **Service** et **Hors stock** pour spécifier si l’article est une unité de stock physique, une unité de temps de travail ou une unité physique qui n’est pas conservée dans le stock. En savoir plus sur [Enregistrer de nouveaux articles](inventory-how-register-new-items.md). Le processus de facture vente est identique pour les trois types d’article.

Vous pouvez remplir les champs relatifs au client sur la facture vente de deux façons selon que le client est déjà enregistré ou non. Reportez-vous à l’étape 2 de la procédure ci-dessous.

### <a name="to-create-a-sales-invoice"></a>Pour créer une facture vente :

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente**, puis sélectionnez le lien associé.  
2. Dans le champ **Client**, entrez le nom d’un client existant. Si, toutefois, le client est nouveau et n’est donc pas enregistré, suivez ces étapes pour remplir les informations client standard sur la page **Facture vente** :

    1. Dans le champ **Nom du client**, entrez le nom du nouveau client.
    2. Dans la boîte de dialogue d’enregistrement du nouveau client, cliquez sur le bouton **Oui**.
    3. Sur la page **Sélectionnez un modèle pour un nouveau client**, sélectionnez un modèle sur lequel baser la nouvelle fiche client, puis cliquez sur **OK**.
    4. Une nouvelle fiche client affiche des informations sur le modèle client sélectionné. Renseignez les champs restants. En savoir plus sur [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).  
    5. Lorsque vous avez terminé la fiche client, choisissez **Fermer** pour revenir à la page **Facture vente**.

   Plusieurs champs de la facture vente sont désormais renseignés avec les informations que vous avez spécifiées sur la nouvelle fiche client.  
3. Renseignez les champs restants de la page **Facture vente**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si vous autorisez le client à payer immédiatement, par exemple, en liquide ou par PayPal, renseignez le champ **Code mode de règlement**. Le paiement est ensuite enregistré dès que vous validez la facture vente. Si vous sélectionnez *Espèces*, le paiement est enregistré dans un compte contrepartie spécifié.

    Vous êtes maintenant prêt à renseigner le raccourci **Lignes** pour les produits que vous vendez au client ou pour toute transaction avec le client que vous souhaitez enregistrer dans un compte général.

4. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.
   * Si vous avez défini des lignes vente récurrentes pour le client, tel qu’un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la commande par l’intermédiaire de l’action **Extraire les lignes vente récurrentes**.
5. Dans le champ **N°**, sélectionnez un enregistrement à valider en fonction de la valeur du champ **Type**.

    Laissez le champ **N°** vide dans les cas suivants :

    * Si la ligne est destinée à un commentaire. Saisissez le commentaire dans le champ **Description**.
    * Si la ligne est destinée à un article de catalogue. Sélectionnez l’action **Sélectionner articles de catalogue**. En savoir plus sur [Utiliser des éléments de catalogue](inventory-how-work-nonstock-items.md).

6. Dans le champ **Quantité**, entrez le nombre d’unités du produit, de frais ou de la transaction que la ligne enregistre pour le client.  

    > [!NOTE]  
    > Si l’article est de type **Service** ou si le champ **Type** contient **Ressource**, la quantité est alors une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité** de la ligne. Pour plus d’informations, reportez-vous à [Configuration d’unités article](inventory-how-setup-units-of-measure.md)

    La valeur du champ **Montant ligne** est calculée comme suit : *Prix unitaire* x *Quantité*.  

    Le prix et les montants ligne sont affichés avec ou sans la taxe de vente en fonction de la valeur que vous avez sélectionnée dans le champ **Prix incluant les taxes** de la fiche client.  
7. Si vous souhaitez accorder une remise, saisissez un pourcentage dans le champ **% remise ligne**. La valeur du champ **Montant ligne** est mise à jour en conséquence.  

    Si des prix article spéciaux sont définis sur le raccourci **Prix vente et remises ligne vente** dans la fiche client ou article, le prix et le montant de la ligne vente sont automatiquement mis à jour si les critères de prix convenus sont réunis. En savoir plus, [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Répétez les étapes 4 à 7 pour chaque produit ou frais que vous souhaitez facturer au client.

    Les champs totaux sous les lignes sont automatiquement mises à jour comme vous créez ou modifiez des lignes pour afficher les montants qui seront validés en comptabilité.

    > [!NOTE]
    > Dans de très rares cas, les montants validés peuvent différer de ce qui est affiché dans les champs des totaux. Cela est généralement dû aux calculs d’arrondi par rapport à la TVA ou à la taxe sur les ventes.<br /><br />Pour vérifier les montants qui seront réellement validés, vous pouvez utiliser la page **Statistiques**, qui tient compte des calculs d’arrondi. Aussi, si vous choisissez l’action **Lancer**, les champs de totaux seront mis à jour pour inclure les calculs d’arrondi.
9. Dans le champ **Montant remise facture sans TVA**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC**.

    Si vous avez défini des remises facture pour le client, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture** si les critères de remise sont réunis, et le montant associé est inséré dans le champ **Montant remise facture sans TVA**. En savoir plus, [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

10. Lorsque les lignes facture vente sont renseignées, sélectionnez l’action **Valider et envoyer**.  

La boîte de dialogue **Valider et envoyer la confirmation** s’ouvre et indique le mode de réception de documents par défaut du client. Vous pouvez modifier le mode d’envoi en cliquant sur le bouton de recherche pour le champ **Envoyer le document à**. En savoir plus, [Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md).

Les écritures comptables article et client associés sont à présent créés dans votre système, et la facture vente est sortie en tant que document au format PDF. La facture vente est supprimée de la liste des factures vente et remplacée par un nouveau document dans la liste des factures vente validées.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcul de remises facture pour des ventes

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Factures enregistrées

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Vous pouvez facilement corriger ou annuler une facture vente validée avant qu’elle ne soit payée. Cela est utile si vous souhaitez corriger une erreur de saisie, ou si le client demande une modification tôt dans le processus de commande. En savoir plus, [Corriger ou annuler des factures vente impayées](sales-how-correct-cancel-sales-invoice.md) Si la facture vente validée est payée, vous devez créer un avoir vente pour contrepasser la vente. En savoir plus, [Traiter les retours ou annulations des ventes](sales-how-process-sales-returns-cancellations.md)  

[Ouvrir la liste des **factures vente validées**](https://businesscentral.dynamics.com/?page=143) dans [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments"></a>Enregistrement des paiements

Selon les besoins de votre entreprise, vous pouvez être payé et enregistrer ce paiement de diverses manières : manuellement, automatiquement, et via des services de paiement.  

Vous pouvez traiter les paiements directement depuis la fiche client. Utilisez l’action **Enregistrer les paiements client** pour obtenir un aperçu des factures impayées de ce client. Ensuite, marquez la facture comme payée entièrement ou partiellement. Ce rapprochement des paiements traite les paiements de vos clients en faisant correspondre les montants perçus sur votre compte bancaire avec les factures vente impayées associées, puis valide les paiements. Pour plus d’informations, reportez-vous à la section [Pour rapprocher les paiements individuellement](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

Dans les environnements d’entreprise où le client paie un certain temps après la livraison, conformément aux conditions de paiement, une facture vente validée reste ouverte (impayée) jusqu’à ce que le département Comptabilité client vérifie la réception du paiement et lettre le paiement à la facture vente validée. Cela peut être effectué manuellement ou automatiquement. Pour plus d’informations, consultez [Rapprocher des paiements clients avec la Feuille règlement ou les Écritures comptables client](receivables-how-apply-sales-transactions-manually.md) et [Rapprocher les paiements à l’aide de l’application automatique](receivables-how-reconcile-payments-auto-application.md).  

Dans les environnements d’entreprise où le client paie immédiatement, par exemple par PayPal ou en espèces, le paiement est enregistré immédiatement lorsque vous validez la facture vente, c’est-à-dire la facture vente validée est clôturée comme entièrement lettrée. Vous sélectionnez la méthode appropriée dans le champ **Code mode de règlement** de la commande vente. Pour les paiements électroniques, tels que PayPal, vous devez également renseigner le champ **Service de paiement**. En savoir plus, [Activer les paiements client via les services de paiement](sales-how-enable-payment-service-extensions.md).

Vous pouvez même créer des factures à paiement direct pour les clients non enregistrés en configurant une fiche « client en espèces », vers laquelle vous pointez sur la facture vente. En savoir plus sur [Configurer les clients effectuant un achat au comptoir](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Si vous souhaitez envoyer à vos clients des rappels de paiements en retard, vous devez configurer des niveaux et des conditions de rappel. En savoir plus, [Configurer les conditions et niveaux et textes de relance](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Numéros de document externe

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/invoicing-customers-dynamics-365-business-central/index) associée.

## <a name="see-also"></a>Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Imprimer la liste des prélèvements](sales-how-print-picking-list.md)  
[Stock](inventory-manage-inventory.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Collecte des soldes restants](receivables-collect-outstanding-balances.md)  
[Facturation en vrac à partir de Microsoft Bookings dans Business Central](finance-bookings.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
