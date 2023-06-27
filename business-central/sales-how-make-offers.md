---
title: Créer des devis
description: Consultez comment créer une offre vente offrent ou un document de demande de proposition pour enregistrer votre offre à un client ou prospecter pour vendre des produits dans certaines conditions.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: edupont
---
# <a name="make-sales-quotes" />Créer des devis

Vous créez un devis pour enregistrer votre proposition à un client ou un prospect pour vendre certains biens selon certaines conditions de livraison et de paiement. Vous pouvez envoyer un devis au client pour communiquer la proposition. Vous pouvez envoyer par e-mail le document en pièce jointe au format PDF. Vous pouvez faire en sorte que le corps du message soit prérempli avec un résumé du devis. Pour plus d’informations, voir [Envoyer des documents par e-mail](ui-how-send-documents-email.md).

Lorsque vous négociez avec le client ou le prospect, vous pouvez modifier et renvoyer autant de devis que nécessaire. Lorsque le client accepte le devis, vous convertissez le devis en facture vente ou en commande vente dans laquelle vous traitez la vente. Pour plus d’informations, voir [Facturer des ventes](sales-how-invoice-sales.md) ou [Vendre des produits](sales-how-sell-products.md).

Dans la plupart des cas, vous envoyez des devis aux clients potentiels. Vous avez souvent un interlocuteur avec qui vous négociez. S’il accepte ensuite votre offre, vous transformez le devis en commande et enregistrez le prospect en tant que client dans [!INCLUDE [prod_short](includes/prod_short.md)]. Dans la procédure suivante, nous nous concentrons sur les contacts, mais vous pouvez également envoyer des devis aux clients existants.  

## <a name="to-create-a-sales-quote" />Pour créer un devis

1. Sélectionnez l’icône ![en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devis**, puis sélectionnez le lien associé.
2. Spécifiez le contact ou le client auquel vous souhaitez envoyer le devis.

    - Si le devis concerne un contact existant, indiquez le nom dans le champ **N° de contact** .  

        Si le devis concerne un client existant, indiquez le client dans le champ **Client**.
    - Si le contact n’est pas enregistré, procédez comme suit :

        1. Dans le champ **N° contact** choisissez le bouton de modification :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Dans la boîte de dialogue de sélection du contact, choisissez l’action **Nouveau**, puis remplissez les champs correspondants. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Pour plus d’informations, reportez-vous à [Créer des contacts](marketing-create-contact-companies.md).  
        3. Lorsque vous avez rempli la fiche de contact, sélectionnez le contact récemment créé dans la liste des contacts, puis cliquez sur le bouton OK pour revenir au devis.

        Plusieurs champs du devis sont désormais renseignés avec les informations que vous avez spécifiées sur la nouvelle fiche de contact.

        > [!NOTE]
        > Pour calculer correctement les taxes et les prix d’un devis, vous devez choisir le modèle client correspondant dans le champ **Code modèle client**. Le modèle est utilisé pour convertir le contact en client une fois le devis converti en commande vente ou en facture.
    -  Si le devis est destiné à un nouveau client, vous devez ajouter le client. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).  

3. Renseignez les champs restants de la page **Devis**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Vous êtes maintenant prêt à renseigner les lignes commande vente pour les produits que vous vendez au client pour toute transaction avec le client ou le prospect que vous souhaitez enregistrer dans un compte général.  

    Si vous avez défini des lignes vente récurrentes pour le client, tel qu’un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la commande par l’intermédiaire de l’action **Extraire les lignes vente récurrentes**.  

4. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.
5. Dans le champ **N°**, sélectionnez un enregistrement à valider en fonction de la valeur du champ **Type**.

    Laissez le champ **N°** vide dans les cas suivants :
    - Si la ligne est destinée à un commentaire. Saisissez le commentaire dans le champ **Description**.
    - Si la ligne est destinée à un article de catalogue. Sélectionnez l’action **Sélectionner articles de catalogue**. Pour en savoir plus, voir [Utiliser des articles de catalogue](inventory-how-work-nonstock-items.md).

6. Dans le champ **Quantité**, entrez le nombre d’unités du produit, de frais ou de la transaction que la ligne enregistre pour le client.

    > [!NOTE]  
    >  Si l’article est de type **Service** ou si le champ **Type** contient **Ressource**, la quantité est alors une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité** de la ligne. Pour plus d’informations, reportez-vous à [Configuration d’unités article](inventory-how-setup-units-of-measure.md)

    La valeur du champ **Montant ligne** est calculée comme suit : *Prix unitaire* x *Quantité*.  

    Le prix et les montants ligne sont affichés avec ou sans la taxe de vente en fonction de la valeur que vous avez sélectionnée dans le champ **Prix incluant les taxes** de la fiche client.  
7. Si vous souhaitez accorder une remise, saisissez un pourcentage dans le champ **% remise ligne**. La valeur du champ **Montant ligne** est mise à jour en conséquence.  

    Si des prix article spéciaux sont définis sur le raccourci **Prix vente et remises ligne vente** dans la fiche client ou article, le prix et le montant de la ligne vente sont automatiquement mis à jour si les critères de prix convenus sont réunis. Pour plus d’informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Répétez les étapes 4 à 7 pour chaque produit que vous souhaitez proposer au contact.

    Les totaux sous les lignes sont calculés automatiquement au fur et à mesure que vous créez ou modifiez des lignes.  
9. Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC**.

    Si vous avez défini des remises facture pour le client, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture** si les critères sont réunis, et le montant associé est inséré dans le champ **Montant remise facture sans TVA**. Pour plus d’informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Pour que **Devis valide jusqu’à** soit renseigné automatiquement avec un certain nombre de jours après la création du devis, vous pouvez renseigner le champ **Calcul de validité du devis** sur la page **Ventes**.

10. Lorsque les lignes devis sont renseignées, sélectionnez l’action **Envoyer par e-mail**.
11. Sur la page **Envoyer e-mail**, renseignez les champs restants et examinez le devis intégré. Pour plus d’informations, voir [Envoyer des documents par e-mail](ui-how-send-documents-email.md).
12. Si le contact accepte le devis, choisissez l’action **Créer commande**.  

    Sinon, si votre organisation préfère ce processus, choisissez l’action **Créer une facture**.  
    > [!NOTE]
    > Si vous avez ajouté un client à l’étape 2, il vous sera demandé de confirmer la conversion du devis en commande.  
    >
    > Si vous avez ajouté un contact d’un client potentiel à l’étape 2, vous serez invité à suivre les étapes suivantes :
    >
    >  - Convertissez le contact ou le prospect en client en choisissant l’un des modèles de conversion de contact. Pour plus d’informations, reportez-vous à [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Confirmez la conversion du devis en commande.

La conversion supprime le devis de la base de données. Une facture vente ou une commande vente basée sur les informations du devis et dans laquelle vous pouvez traiter la vente est créée. Dans le champ **N° devis** de la facture vente ou de la commande vente, vous pouvez visualiser le numéro du devis à partir duquel elle a été réalisée. Pour plus d’informations, voir [Facturer des ventes](sales-how-invoice-sales.md) ou [Vendre des produits](sales-how-sell-products.md).  

## <a name="external-document-number" />Numéro de document externe

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Archiver des documents](across-how-to-archive-documents.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
