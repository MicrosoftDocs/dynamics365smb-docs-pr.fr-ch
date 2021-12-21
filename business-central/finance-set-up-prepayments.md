---
title: Configuration des acomptes
description: Découvrez comment configurer Business Central afin de pouvoir utiliser les acomptes pour facturer et collecter les acomptes requis des clients ou régler des acomptes aux fournisseurs.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keyword: prepayment
ms.date: 10/27/2021
ms.author: edupont
ms.openlocfilehash: a09f0cd35c62b65bf690fd785c0fc9a4b4b178d7
ms.sourcegitcommit: 4223484b0eeceb0258dae5abfd04e1a9a4a0990d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2021
ms.locfileid: "7889858"
---
# <a name="set-up-prepayments"></a>Configuration des acomptes

Si vous voulez que vos clients fassent des paiements avant de leur expédier une commande ou si votre fournisseur exige que vous fassiez un paiement avant de vous expédier une commande, vous pouvez utiliser la fonctionnalité Acompte. La fonctionnalité Acomptes vous permet de facturer et de collecter les acomptes requis des clients ou de régler des acomptes aux fournisseurs, et pour s’assurer que tous les paiements partiels sont validés sur une facture. Pour plus d’informations, consultez [Créer des factures d’acompte](finance-how-to-create-prepayment-invoices.md).

Avant de valider des factures acompte, vous devez configurer les comptes de validation dans le module Comptabilité et configurer des souches de numéros pour les documents acompte. Vous devez spécifier un compte pour les paiements anticipés liés aux ventes et un compte pour les paiements anticipés liés aux achats. Vous pouvez spécifier les mêmes comptes imputables à utiliser pour tous les paiements anticipés liés à tous les groupes de comptabilisation commerciaux ou généraux du produit, ou vous pouvez spécifier des comptes spécifiques pour des groupes de comptabilisation spécifiques pour les ventes et les achats, respectivement. Cela dépend des exigences de votre entreprise en matière de suivi des paiements anticipés.  

Vous pouvez définir le pourcentage du montant ligne qui sera facturé pour acompte, pour un client ou un fournisseur, pour tous les articles ou pour une sélection d’articles. Une fois la configuration terminée, vous pouvez générer des factures acompte à partir des commandes vente et achat. Vous pouvez utiliser les pourcentages par défaut pour chaque ligne vente ou achat, ou, au besoin, modifier les montants de la facture. Par exemple, vous pouvez spécifier un montant total pour la commande entière.  

> [!NOTE]
> Nous vous recommandons de ne pas utiliser un pourcentage de prépaiement de 100 % dans les cas suivants :
>
> * Si vous résidez en Amérique du Nord. En raison du mode de calcul des taxes, un pourcentage de paiement anticipé de 100 % peut entraîner des problèmes avec les factures de paiement anticipé.
> * Dans toutes les régions, si vous déduisez manuellement un escompte de la facture. Un pourcentage de prépaiement de 100 % ne laissera pas automatiquement un montant sur lequel déduire la remise. 

Puisque le montant payé par anticipation appartient à l’acheteur jusqu’à ce qu’il ait reçu les biens ou les services, vous devez configurer des comptes généraux pour recevoir les montants d’acompte jusqu’à la validation de la facture finale. Les acomptes vente doivent être enregistrés dans un compte passif jusqu’à l’expédition des articles. Les acomptes achat doivent être enregistrés dans un compte immobilisations jusqu’à la réception des articles. En outre, vous devez configurer un compte général séparé pour chaque identifiant TVA.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Ajouter des comptes acompte aux paramètres comptabilisation  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilisation**, puis choisissez le lien associé.
2. Sur la page **Paramètres comptabilisation**, renseignez les champs suivants pour les lignes appropriées :  

    * **Compte acomptes vente**  
    * **Compte acomptes achat**  

> [!TIP]
> Si vous ne pouvez pas voir les champs de la page **Paramètres comptabilisation**, utilisez la barre de défilement horizontale au bas de la page pour faire défiler l’affichage vers la droite.  

Si vous n’avez pas encore configuré de comptes généraux pour les acomptes, vous pouvez ouvrir la page **Liste des comptes généraux** à partir du champ du compte correspondant.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Configurer des souches de numéros pour des documents acompte  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres ventes**, puis choisissez le lien associé.
2. Sur la page **Paramètres ventes**, sur le raccourci **Souches de numéros**, remplissez les champs suivants :  

   * **N° fact. acompte enreg.**
   * **N° avoir acompte enreg.**

3. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres achat**, puis choisissez le lien associé.
4. Sur la page **Paramètres achats**, sur le raccourci **Souches de numéros**, remplissez les champs suivants :

    * **N° fact. acompte enreg.**
    * **N° avoir acompte enreg.**

> [!NOTE]  
> Vous pouvez utiliser les mêmes souches de numéros pour des factures acompte et des factures normales, ou utiliser des souches de numéros différentes. Si vous utilisez des souches différentes, elles ne doivent pas se chevaucher car vous ne pouvez pas avoir des numéros identiques dans les deux souches.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Pour configurer des pourcentages d’acompte pour des articles, des clients et des fournisseurs

Pour un article, vous pouvez configurer un pourcentage d’acompte par défaut pour tous les clients, pour un client spécifique ou pour un groupe prix client. Si vous ne souhaitez pas appliquer le même pourcentage d’acompte à tous les clients, vous devez spécifier à quels clients ou à quels groupes de prix client s’applique le pourcentage d’acompte.

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez un article, puis cliquez sur l’action **Pourcentages acompte**.  
3. Sur la page **Pourcentages acompte vente**, renseignez autant de champs que nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Pour un client ou un fournisseur, vous pouvez configurer un pourcentage d’acompte par défaut pour tous les articles et tous les types de lignes vente. Vous entrez cette valeur dans la fiche client ou fournisseur. La procédure suivante montre comment spécifier un pourcentage de prépaiement pour un client, mais des étapes similaires s’appliquent aux fournisseurs.  

1. Sélectionnez l’icône ![en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un client.
3. Remplissez le champ **Acompte**.
4. Répétez les étapes pour d’autres clients ou fournisseurs.  

> [!TIP]
> Vous pouvez également accéder à la page **Pourcentages acompte vente** à partir de la carte client ou fournisseur.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Pour déterminer quel pourcentage d’acompte a la priorité  

Une commande peut avoir un pourcentage d’acompte dans l’en-tête vente et un autre pourcentage pour les articles figurant dans les lignes. Pour déterminer quel pourcentage d’acompte s’applique à chaque ligne vente, le système recherche le pourcentage d’acompte dans l’ordre suivant et applique la première valeur par défaut qu’il trouve :  

1. un pourcentage d’acompte pour l’article figurant dans la ligne et le client auquel la commande est destinée ;  
2. un pourcentage d’acompte pour l’article figurant dans la ligne et le groupe prix client auquel le client appartient ;  
3. un pourcentage d’acompte pour l’article figurant dans la ligne pour tous les clients ;  
4. le pourcentage d’acompte figurant dans l’en-tête vente ou achat.  

Autrement dit, le pourcentage d’acompte figurant dans la fiche client ne s’applique que si aucun pourcentage d’acompte n’est configuré pour l’article. Toutefois, si vous modifiez le contenu du champ **% acompte** dans l’en\-tête vente ou achat après avoir créé les lignes, le pourcentage d’acompte figurant dans toutes les lignes est mis à jour. Cela facilite la création d’une commande avec un pourcentage d’acompte fixe, quel que soit le pourcentage configuré pour les articles.

## <a name="see-also"></a>Voir aussi  

[Facturation d’acomptes](finance-invoice-prepayments.md)  
[Procédure pas à pas : configuration et facturation d’acomptes](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Calculer la taxe sur les biens et services pour les acomptes en Australie](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Calculer la taxe sur les biens et services pour les acomptes en Nouvelle-Zélande](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Familiarisation avec les écritures comptables et les COA](finance-general-ledger.md)  
[Finances](finance.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]