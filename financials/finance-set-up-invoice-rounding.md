---
title: Configurer la fonction arrondi facture | Microsoft Docs
description: "Vous pouvez arrondir les montants des factures lors de la création de celles-ci. De plus, les réglementations ou la douane locale peuvent exiger des factures arrondies d'une certaine manière, par exemple, divisibles par 0,05."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-invoice-rounding"></a>Configuration de la fonction arrondi facture
Si vous devez arrondir des montants de factures lorsque vous créez des factures, vous pouvez utiliser la fonction d'arrondi automatique. Lorsqu'une facture est arrondie, une ligne supplémentaire contenant le montant arrondi est ajoutée et validée avec les autres lignes facture.

> [!NOTE]  
>  Les réglementations ou la douane locale peuvent exiger des factures arrondies d'une certaine manière, par exemple, divisibles par 0,05.  
  
Pour utiliser l'arrondi facture automatique, vous devez :  
  
* spécifier les comptes généraux dans lesquels les différences d'arrondi seront validées ;  
* configurer les règles d'arrondi des factures dans les devises société et étrangère ;  
* activer la fonction.  
  
> [!NOTE]  
>  Outre les fonctions d'arrondi facture, vous pouvez arrondir les montants des factures à l'aide des fonctions arrondi montant unité et arrondi montant.  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Configurer des comptes généraux afin d'autoriser les différences d'arrondi dans les factures
Pour utiliser la fonction d'arrondi automatique de facture, vous devez configurer les comptes généraux dans lesquels des différences d'arrondi seront utilisées. Pour cela, vous devez toutefois configurer des groupes comptabilisation produit TVA. Pour plus d'informations, reportez-vous à [Configuration TVA](finance-setup-vat.md).  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Pour configurer des comptes généraux afin d'autoriser les différences d'arrondi dans les factures  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Plan comptable**, puis sélectionnez le lien connexe.  
2. Sur la page **Plan comptable**, configurez le compte et nommez-le, par exemple **Arrondi facture**. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilise le nom de ce compte comme texte pour les factures arrondies.  
3. Selon que vous utilisez la TVA ou la taxe de vente, dans les champs **Groupe compta. produit TVA** ou **Groupe compta. produit TVA**, choisissez un groupe comptabilisation pour les montants arrondis. Vous pouvez aussi paramétrer un nouveau code groupe à utiliser pour les arrondis facture.
4. Laissez les champs **Type compta. TVA** et **Groupe compta. marché TVA** ou **Groupe compta. marché TVA** vides. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
À présent, vous pouvez affecter le compte arrondi facture aux groupes comptabilisation sur la page **Groupes compta. fournisseur**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Configuration de règles d'arrondi pour les devises étrangères et société
Avant d'utiliser la fonction d'arrondi automatique, vous devez configurer les règles d'arrondi pour les devises étrangères et société.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Pour configurer les règles d'arrondi pour les devises étrangères  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Devises**, puis sélectionnez le lien connexe.  
2. Sur la page **Devises**, choisissez la devise étrangère pour ouvrir la **Fiche devise**, puis renseignez les champs **Précision arrondi montant**, **Précis. arrondi montant unité**, **Précision arrondi facture** et **Type arrondi facture**.
  
### <a name="to-set-up-rounding-for-your-local-currency"></a>Pour configurer les règles d'arrondi pour les devises société
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres comptabilité**, puis sélectionnez le lien connexe.  
2. Sur la page **Paramètres comptabilité**, sous le raccourci **Général**, renseignez les champs **Précis. arrondi fact.** et **Type arrondi facture**.  

## <a name="activate-the-invoice-rounding-function"></a>Activer la fonction arrondi facture  
Vous devez activer la fonction arrondi facture pour que les factures vente et achat soient automatiquement arrondies. Activez séparément la fonction arrondi facture pour les factures vente et les factures achat.

1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Paramètres ventes** ou **Paramètres achats**, puis sélectionnez le lien connexe.  
2. Sur le raccourci **Général**, sélectionnez la case **Arrondi facture**.  
  
## <a name="see-also"></a>Voir aussi  
[Facturer des ventes](sales-how-invoice-sales.md)  
[Enregistrer des achats](purchasing-how-record-purchases.md)
