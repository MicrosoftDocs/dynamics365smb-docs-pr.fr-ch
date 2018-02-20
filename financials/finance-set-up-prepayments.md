---
title: Configurer des acomptes | Microsoft Docs
description: "Les acomptes sont des paiements qui sont facturés et validés dans une commande acompte vente ou achat avant la facturation finale. Vous pouvez demander un acompte avant de fabriquer les produits commandés ou demander à ce que le paiement soit effectué avant d'envoyer les articles à un client. La fonctionnalité d'acomptes vous permet de facturer et de collecter les acomptes requis des clients ou de régler des acomptes aux fournisseurs. Vous pouvez ainsi vous assurer que tous les paiements sont validés sur une facture."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 15/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 66c5d81fd7c3517b42930f53b81e06a3583aeb3d
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-prepayments"></a>Configuration des acomptes
Si vous voulez que vos clients fassent des paiements avant de leur expédier une commande ou si votre fournisseur exige que vous fassiez un paiement avant de vous expédier une commande, vous pouvez utiliser la fonctionnalité Acompte. La fonctionnalité vous permet de facturer et de collecter les acomptes requis des clients ou de régler des acomptes aux fournisseurs, et pour s'assurer que tous les paiements partiels sont validés sur une facture. Pour plus d'informations, consultez [Créer des factures d'acompte](finance-how-to-create-prepayment-invoices.md).

Avant de valider des factures acompte, vous devez configurer les comptes de validation dans le module Comptabilité et configurer des souches de numéros pour les documents acompte.  

Vous pouvez définir le pourcentage du montant ligne qui sera facturé pour acompte, pour un client ou un fournisseur, pour tous les articles ou pour une sélection d'articles. Une fois la configuration terminée, vous pouvez générer des factures acompte à partir des commandes vente et achat. Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou, au besoin, modifier les montants de la facture. Par exemple, vous pouvez spécifier un montant total pour la facture entière.  

Puisque le montant payé par anticipation appartient à l'acheteur jusqu'à ce qu'il ait reçu les biens ou les services, vous devez configurer des comptes généraux pour recevoir les montants d'acompte jusqu'à la validation de la facture finale. Les acomptes vente doivent être enregistrés dans un compte passif jusqu'à l'expédition des articles. Les acomptes achat doivent être enregistrés dans un compte immobilisations jusqu'à la réception des articles. En outre, vous devez configurer un compte général séparé pour chaque identifiant TVA.

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Ajouter des comptes acompte aux paramètres comptabilisation  

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres comptabilisation**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Paramètres comptabilisation**, vous devez renseigner les champs suivants :  

    - **Compte acomptes vente**  
    - **Compte acomptes achat**  

Si vous n'avez pas encore configuré de comptes généraux pour les acomptes, vous pouvez le faire dans la fenêtre **Liste des comptes généraux**.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Configurer des souches de numéros pour des documents acompte  

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône"), entrez **Paramètres ventes**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Paramètres ventes**, renseignez les champs suivants :  

   - **N° fact. acompte enreg.**
   - **N° avoir acompte enreg.**

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Paramètres achats**, renseignez les champs suivants :

    - **N° fact. acompte enreg.**
    - **N° avoir acompte enreg.**

> [!NOTE]  
>  Vous pouvez utiliser les mêmes souches de numéros pour des factures acompte et des factures normales, ou utiliser des souches de numéros différentes. Si vous utilisez des souches différentes, elles ne doivent pas se chevaucher car vous ne pouvez pas avoir des numéros identiques dans les deux souches.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Pour configurer des pourcentages d'acompte pour des articles, des clients et des fournisseurs  
Pour un article, vous pouvez configurer un pourcentage d'acompte par défaut pour tous les clients, pour un client spécifique ou pour un groupe prix client.  

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Articles**, puis sélectionnez le lien connexe.
2. Sélectionnez un article, puis cliquez sur l'action **Pourcentages acompte**.  
3. Dans la fenêtre **Pourcentages acompte vente**, renseignez autant de champs que nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Pour un client ou un fournisseur, vous pouvez configurer un pourcentage d'acompte par défaut pour tous les articles et tous les types de lignes vente. Vous entrez cette valeur dans la fiche client ou fournisseur.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un client.
3. Remplissez le champ **Acompte**.
4. Répétez les étapes pour d'autres clients ou fournisseurs.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Pour déterminer quel pourcentage d'acompte a la priorité  
Une commande peut avoir un pourcentage d'acompte dans l'en-tête vente et un autre pourcentage pour les articles figurant dans les lignes. Pour déterminer quel pourcentage d'acompte s'applique à chaque ligne vente, le système recherche le pourcentage d'acompte dans l'ordre suivant et applique la première valeur par défaut qu'il trouve :  
1. un pourcentage d'acompte pour l'article figurant dans la ligne et le client auquel la commande est destinée ;  
2. un pourcentage d'acompte pour l'article figurant dans la ligne et le groupe prix client auquel le client appartient ;  
3. un pourcentage d'acompte pour l'article figurant dans la ligne pour tous les clients ;  
4. le pourcentage d'acompte figurant dans l'en-tête vente ou achat.  

Autrement dit, le pourcentage d'acompte figurant dans la fiche client ne s'applique que si aucun pourcentage d'acompte n'est configuré pour l'article. Toutefois, si vous modifiez le contenu du champ **% acompte** dans l'en\-tête vente ou achat après avoir créé les lignes, le pourcentage d'acompte figurant dans toutes les lignes est mis à jour. Cela facilite la création d'une commande avec un pourcentage d'acompte fixe, quel que soit le pourcentage configuré pour les articles.

## <a name="see-also"></a>Voir aussi  
[Facturation d'acomptes](finance-invoice-prepayments.md)  
[Procédure pas à pas : configuration et facturation d'acomptes](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Familiarisation avec les écritures comptables et les COA](finance-general-ledger.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

