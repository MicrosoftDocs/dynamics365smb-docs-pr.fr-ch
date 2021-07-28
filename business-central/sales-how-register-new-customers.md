---
title: Enregistrer de nouveaux clients en créant une fiche client
description: Décrit comment créer une fiche client pour enregistrer des informations sur chaque nouveau client ou client auquel vous vendez.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bb323a5cceb4988035d442d6bc8347125f927bf4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436766"
---
# <a name="register-new-customers"></a>Enregistrer de nouveaux clients

Les clients sont l’origine de vos revenus. Chaque client auquel vous vendez un élément doit être enregistré en tant que fiche client. Les fiches client contiennent les informations nécessaires à la vente de biens au client. Pour plus d’informations, voir [Facturer des ventes](sales-how-invoice-sales.md) et [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

Avant de pouvoir enregistrer de nouveaux clients, vous devez configurer divers codes vente que vous pouvez sélectionner lorsque vous renseignez les fiches client. Pour plus d’informations, reportez-vous à [Définition des ventes](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Ajout de nouveaux clients

Pour enregistrer un nouveau client, vous devez remplir une fiche client. Vous pouvez créer des modèles pour différents profils de clients ou ajouter des clients sans modèles. Vous pouvez également créer un client à partir d’un contact. Pour plus d’informations, reportez-vous à [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Si des modèles client existent pour différents types de clients, une page s’affiche lorsque vous créez une nouvelle fiche client à partir de laquelle vous pouvez sélectionner un modèle client approprié. Si un seul modèle client existe, les nouvelles fiches client utiliseront toujours ce modèle.  

### <a name="to-create-a-new-customer-card"></a>Pour créer une fiche client

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.  
2. Sur la page **Clients**, sélectionnez l’action **Nouveau**.

    Si un seul modèle client existe, une nouvelle fiche client avec certains champs renseignés à l’aide des informations provenant du modèle s’ouvre.

    Si plusieurs modèles client existent, une page s’affiche et vous permet de sélectionner un modèle client. Dans ce cas, suivez les deux étapes suivantes.
3. Sur la page **Sélectionnez un modèle pour un nouveau client**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche client.
4. Cliquez sur le bouton **OK**. Une fiche client avec certains champs contenant les informations provenant de ce modèle s’ouvre.  
5. Renseignez ou modifiez les champs de la fiche client selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sur le raccourci **Prix vente**, vous pouvez afficher les prix spéciaux ou les remises accordées au client si certains critères sont réunis, par exemple l’article, la quantité minimum commande ou la date de fin. Chaque ligne représente un prix spécial ou une remise ligne. Chaque colonne représente un critère qui doit s’appliquer pour garantir le prix spécial que vous saisissez dans le champ **Prix** ou la remise ligne que vous saisissez dans le champ **% remise ligne**. Pour plus d’informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

Le client est désormais enregistré, et la fiche client est prête à être utilisée sur les documents vente.

Si vous souhaitez utiliser cette fiche client comme modèle lorsque vous créez de nouvelles fiches client, enregistrez-la comme modèle. Pour plus d’informations, reportez-vous à la section suivante.  

### <a name="to-save-the-customer-card-as-a-template"></a>Pour enregistrer la fiche client en tant que modèle

1. Sur la page **Fiche client**, sélectionnez l’action **Sauvegarder comme modèle**. La page **Modèle client** s’ouvre et affiche la fiche client comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles, sélectionnez l’action **Axes analytiques**. La page **Modèles axe** s’ouvre et affiche tous les codes axe qui sont définis pour le client.
4. Modifiez ou entrez les codes axe s’appliquant aux nouvelles fiches client créées à l’aide du modèle.  
5. Lorsque vous avez terminé le nouveau modèle client, cliquez sur le bouton **OK**.

Le modèle client est ajouté à la liste des modèles client. Vous pouvez ainsi l’utiliser pour créer des fiches client.

## <a name="deleting-customer-cards"></a>Suppression de fiches client

Si vous avez enregistré une transaction pour un client, vous ne pouvez pas supprimer la carte car les écritures comptables peuvent être nécessaires pour l’audit. Pour supprimer des fiches client avec des écritures comptables, contactez votre partenaire Microsoft pour le faire via le code.  

## <a name="managing-credit-limits"></a>Gestion des limites de crédit

Les crédits autorisés, les soldes échus et les conditions de paiement permettent à [!INCLUDE [prod_short](includes/prod_short.md)] d’émettre une alerte crédit autorisé ou solde échu lorsque vous entrez une commande vente.  De plus, les options conditions de relance et conditions intérêts de retard vous permettent de facturer des intérêts et des frais supplémentaires.  

Le champ **Crédit autorisé** sur une fiche client spécifie le montant maximal de dépassement du solde de paiement que vous autorisez le client à dépasser avant que des alertes ne soient émises. Ensuite, lorsque vous saisissez des informations dans des journaux, des devis, des commandes et des factures, [!INCLUDE [prod_short](includes/prod_short.md)] teste l’en-tête vente et les lignes vente individuelles pour voir si le crédit autorisé a été dépassé.

Vous pouvez valider même si le crédit autorisé a été dépassé. Si vous laissez le champ blanc, il n’y a pas de crédit autorisé pour ce client.  

Vous pouvez choisir de ne pas afficher les alertes vous indiquant que le crédit autorisé du client a été dépassé et vous pouvez spécifier les types d’avertissement que vous souhaitez voir.

### <a name="to-specify-credit-limit-warnings"></a>Pour spécifier les alertes crédit autorisé

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.

2. Sur le raccourci **Général**, dans le champ **Alertes crédit**, choisissez l’option appropriée comme décrit dans le tableau suivant :

    |Option| Description|
    |------|------------|
    |**Toutes les alertes**| Le programme contrôle à la fois les champs **Crédit autorisé** et **Solde dû** de la fiche client, et affiche une alerte si le client a dépassé son crédit autorisé ou si le client a un solde échu.|
    |**Crédit autorisé**|Le programme compare la valeur du champ **Crédit autorisé** de la fiche client et le solde du client, et affiche une alerte si le solde du client dépasse ce montant.|
    |**Solde échu**|Le champ **Solde dû** de la fiche client est contrôlé et une alerte s’affiche si le client a un solde échu.|
    |**Aucune alerte**|Aucune alerte n’est affichée sur le statut du client.|

## <a name="see-also"></a>Voir aussi

[Définition des modes de règlement](finance-payment-methods.md)  
[Fusionner l’enregistrement des doublons](sales-how-merge-duplicate-records.md)  
[Création des souches de numéros](ui-create-number-series.md)  
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
