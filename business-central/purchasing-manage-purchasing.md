---
title: Aperçu des tâches permettant de gérer vos achats
description: 'Décrit les tâches permettant de gérer vos processus d’achat ou d’approvisionnement, y compris le fonctionnement des factures achat et des commandes achat.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Procédure d’achat

Vous créez une facture achat ou une commande achat pour enregistrer le coût d’achats et suivre les créances. Si vous devez contrôler un stock, les factures achat sont également utilisées pour mettre à jour de manière dynamique les niveaux de stock afin que vous puissiez réduire vos coûts et fournir un meilleur service client. Le prix d’achat, notamment les frais de service, et les valeurs d’inventaire qui résultent de la validation des factures achat contribuent aux chiffres du profit et à d’autres KPI financiers sur votre Tableau de bord.

Vous devez utiliser les commandes achat si votre processus de vente exige que vous enregistriez des réceptions partielles d’une quantité de commande, par exemple, si la quantité totale n’était pas disponible auprès du fournisseur. Si vous commercialisez des articles en les livrant directement depuis votre fournisseur auprès de votre client, vous devez également utiliser les commandes achat. Pour plus d’informations, voir [Effectuer des livraisons directes](sales-how-drop-shipment.md). Pour tous les autres aspects, les commandes achat fonctionnent de la même manière que les factures achat.

Les factures achat peuvent être créées automatiquement en utilisant le service de reconnaissance optique de caractères (OCR) pour convertir les factures PDF de vos fournisseurs en documents électroniques qui sont ensuite convertis en factures achat par un flux de travail. Pour utiliser cette fonctionnalité, vous devez d’abord vous inscrire au service OCR, puis effectuer diverses configurations. Pour plus d’informations, voir [Documents entrants](across-income-documents.md).

Les produits peuvent être des articles en stock et des services. Pour plus d’informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

Pour tous les processus d’achat, vous pouvez incorporer un flux de travail d’approbation, par exemple, pour exiger que les achats en grande quantité soient approuvés par le responsable de la comptabilité. Pour plus d’informations, reportez-vous à [Utilisation des flux d’approbation](across-how-use-approval-workflows.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| À | Voir |
| --- | --- |
| Créer une facture achat pour enregistrer votre accord avec un fournisseur pour acheter des biens selon certaines conditions de livraison et de paiement. |[Enregistrer des achats](purchasing-how-record-purchases.md) |
|Créez une demande de prix pour refléter une demande de devis auprès de votre fournisseur, que vous pourrez ultérieurement convertir en commande achat.|[Demander des devis](purchasing-how-request-quotes.md)|
| Créer une facture achat pour toutes les lignes ou pour les lignes sélectionnées sur une facture vente. |[Acheter des articles pour une vente](purchasing-how-purchase-products-sale.md) |
|Comprenez ce qui se passe lorsque vous publiez des documents achat.|[Validation des achats](ui-post-purchases.md)|
| Effectuer une action sur une facture achat enregistrée impayée pour créer automatiquement un avoir et soit annuler la facture achat, soit la recréer pour que vous puissiez y apporter des corrections. |[Corriger ou annuler des factures vente impayées](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Créer un avoir achat pour rembourser une facture achat validée spécifique pour indiquer les produits que vous retournez au fournisseur et le montant règlement que vous récupérez. |[Traiter les retours ou annulations d’achats](purchasing-how-register-new-vendors.md) |
|Préparez la facturation de plusieurs réceptions provenant du même fournisseur en une seule fois en regroupant les réceptions sur une facture.|[Regroupement de bons de réception sur une seule facture](purchasing-how-to-combine-receipts.md)|
|Conversion, par exemple, de factures électroniques de vos fournisseurs en factures achat dans Business Central.|[Recevoir et convertir des documents électroniques](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Découvrez comment [!INCLUDE[prod_short](includes/prod_short.md)] calcule le moment où vous devez commander un article pour le recevoir à une certaine date.|[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md)|
|Résolvez la confusion lorsque deux enregistrements ou plus existent pour le même fournisseur.|[Fusionner l’enregistrement des doublons](sales-how-merge-duplicate-records.md)|
|Gérez votre engagement envers un fournisseur à acheter de grandes quantités livrées en plusieurs expéditions sur une certaine période.|[Utilisation des commandes cadres achat](sales-how-to-create-blanket-sales-orders.md)|

## Numéros de document externe

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Voir aussi

[Définition des achats](purchasing-setup-purchasing.md)  
[Enregistrement des nouveaux fournisseurs](purchasing-how-register-new-vendors.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fonctionnalités marché](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
