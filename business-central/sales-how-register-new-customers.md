---
title: Enregistrer de nouveaux clients en créant une fiche client (contient une vidéo)
description: Décrit comment créer une fiche client pour enregistrer des informations sur chaque nouveau client ou client auquel vous vendez.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="register-new-customers" />Enregistrer de nouveaux clients

Les clients sont l’origine de vos revenus. Chaque client auquel vous vendez un élément doit être enregistré en tant que fiche client. Les fiches client contiennent les informations nécessaires à la vente de biens au client. Pour plus d’informations, voir [Facturer des ventes](sales-how-invoice-sales.md) et [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

Avant de pouvoir enregistrer de nouveaux clients, vous devez configurer divers codes vente que vous pouvez sélectionner lorsque vous renseignez les fiches client. En savoir plus sur [Configurer les ventes](sales-setup-sales.md).


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers" />Ajout de nouveaux clients

Vous pouvez ajouter de nouveaux clients manuellement, en remplissant les champs sur la page **Fiche client**, ou vous pouvez utiliser des modèles contenant des informations prédéfinies. Par exemple, vous pouvez créer un modèle pour différents types de profils de client. L’utilisation de modèles permet de gagner du temps lors de l’ajout de nouveaux clients et permet de garantir que les informations sont correctes à chaque fois. 

Si vous créez :
* Si vous créez des modèles pour plusieurs types de client, vous pouvez choisir le modèle approprié à utiliser lorsque vous ajoutez un client.
* Si vous ne créez qu’un seul modèle, il sera utilisé pour tous les nouveaux clients. 

Après avoir créé un modèle, vous pouvez utiliser l’action **Appliquer le modèle** pour l’appliquer à un ou plusieurs client sélectionnés. Pour créer un modèle, vous remplissez les informations que vous souhaitez réutiliser sur la page **Fiche client**, puis l’enregistrez en tant que modèle. Pour plus d’informations, consultez [Pour enregistrer la fiche client en tant que modèle](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Il peut être utile de personnaliser la page **Modèle de client** lorsque vous créez un modèle. Par exemple, vous pouvez ajouter le champ **Limite autorisé** à un modèle. Pour plus d’informations, voir la section [Personnaliser votre espace de travail](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Vous pouvez également créer un client à partir d’un contact. Pour plus d’informations, reportez-vous à la section [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card" />Pour créer une fiche client

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

**Prix et remises** fournit des options pour gérer des prix spéciaux ou des remises pour le client lorsqu’une commande répond à certains critères. Par exemple, les critères peuvent être lorsqu’ils achètent un certain article, commandent une quantité minimale ou achètent avant une date, comme la fin d’une campagne. En savoir plus, [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

Le client est désormais enregistré, et la fiche client est prête à être utilisée sur les documents vente.  

### <a name="to-save-the-customer-card-as-a-template" />Pour enregistrer la fiche client en tant que modèle

Si vous souhaitez utiliser cette fiche client comme modèle lorsque vous créez de nouvelles fiches client, enregistrez-la comme modèle.

1. Sur la page **Fiche client**, sélectionnez l’action **Sauvegarder comme modèle**. La page **Modèle client** s’ouvre et affiche la fiche client comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles, sélectionnez l’action **Axes analytiques**. La page **Modèles axe** s’ouvre et affiche tous les codes axe qui sont définis pour le client.
4. Modifiez ou entrez les codes axe s’appliquant aux nouvelles fiches client créées à l’aide du modèle.  
5. Lorsque vous avez terminé le nouveau modèle client, cliquez sur le bouton **OK**.

Le modèle client est ajouté à la liste des modèles client. Vous pouvez ainsi l’utiliser pour créer des fiches client.

## <a name="deleting-customer-cards" />Suppression de fiches client

Si vous avez enregistré une transaction pour un client, vous ne pouvez pas supprimer la fiche client, car les écritures comptables peuvent être nécessaires pour l’audit. Pour supprimer des fiches client avec des écritures comptables, contactez votre partenaire Microsoft pour le faire via le code.  

## <a name="managing-credit-limits" />Gestion des limites de crédit

Les crédits autorisés, les soldes échus et les conditions de paiement permettent à [!INCLUDE [prod_short](includes/prod_short.md)] d’émettre une alerte crédit autorisé ou solde échu lorsque vous entrez une commande vente. De plus, les options conditions de relance et conditions intérêts de retard vous permettent de facturer des intérêts et des frais supplémentaires.  

Le champ **Crédit autorisé** sur une fiche client spécifie le montant maximal de dépassement du solde de paiement que vous autorisez le client à dépasser avant que des alertes ne soient émises. Ensuite, lorsque vous saisissez des informations dans des journaux, des devis, des commandes et des factures, [!INCLUDE [prod_short](includes/prod_short.md)] teste l’en-tête vente et les lignes vente individuelles pour voir si le crédit autorisé a été dépassé.

Vous pouvez valider même si le crédit autorisé a été dépassé. Si vous laissez le champ blanc, il n’y a pas de limite de crédit pour ce client.  

Vous pouvez choisir de ne pas afficher les alertes vous indiquant que le crédit autorisé du client a été dépassé et vous pouvez spécifier les types d’avertissement que vous souhaitez voir.

### <a name="to-specify-credit-limit-warnings" />Pour spécifier les alertes crédit autorisé

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.

2. Sur le raccourci **Général**, dans le champ **Alertes crédit**, choisissez l’option appropriée comme décrit dans le tableau suivant :

    |Option| Description|
    |------|------------|
    |**Toutes les alertes**| Le programme contrôle à la fois les champs **Crédit autorisé** et **Solde dû** de la fiche client, et affiche une alerte si le client a dépassé son crédit autorisé ou si le client a un solde échu.|
    |**Crédit autorisé**|Le programme compare la valeur du champ **Crédit autorisé** de la fiche client et le solde du client, et affiche une alerte si le solde du client dépasse ce montant.|
    |**Solde échu**|Le champ **Solde dû** de la fiche client est contrôlé et une alerte s’affiche si le client a un solde échu.|
    |**Aucune alerte**|Aucune alerte n’est affichée sur le statut du client.|

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics--business-central" />Voir la [formation Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) associée.

## <a name="see-also" />Voir aussi

[Définition des modes de règlement](finance-payment-methods.md)  
[Fusionner l’enregistrement des doublons](sales-how-merge-duplicate-records.md)  
[Création des souches de numéros](ui-create-number-series.md)  
[Activer les livraisons partielles avec avis d’expédition](sales-how-send-partial-shipments.md)  
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Utilisez des cartes en ligne pour trouver des emplacements et des directions](across-online-maps.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
