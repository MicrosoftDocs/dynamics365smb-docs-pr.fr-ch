---
title: Utilisation de l'extension Paiements et rapprochements (DK) | Microsoft Docs
description: "Cette extension facilite l'exportation de fichiers préformatés pour répondre aux exigences bancaires pour les soumissions électroniques."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 09/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 0718012c9278b337409805d95870d22dac4675ad
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---

# <a name="the-payments-and-reconciliations-dk-extension-for-microsoft-dynamics-for-finance-and-operations-business-edition"></a>L'extension Paiements et rapprochements (DK) pour Microsoft Dynamics for Finance and Operations, Business edition
Réalise des paiements rapides et sans erreur en exportant des fichiers formatés spécifiquement pour les échanges avec votre fournisseur ou votre banque. Ces fichiers accélèrent les processus de paiement et de réconciliation, et éliminent les erreurs qui apparaissent lorsque vous saisissez manuellement des informations sur le site Web d'une banque.  
  
Cette extension prend en charge les formats de fichier de plusieurs banques danoises. Lorsque vous exportez des informations paiement vers un fichier, l'extension emballe les données dans le format demandé par votre banque. Par exemple, les formats sont notamment Bankdata-vl, V3, BEC, SDC et FIK, utilisés par de nombreuses banques ; certains sont aussi plus spécialisés pour certaines banques, par exemple, Danske Bank et Nordea. L'extension inclut également des formats d'importation et de rapprochement de relevés bancaires.  
  
> [!Note]
> Pour utiliser l'extension, vous devez connaître le format demandé par votre banque ou votre fournisseur. Certaines banques ou fournisseurs indiquent cette information sur leurs sites Web ; toutefois, vous pouvez être amené à contacter leur service client pour obtenir l'information.  
  
## <a name="supported-bank-formats"></a>Formats bancaires pris en charge
Cette extension peut appliquer les formats de fichier suivants pour les fichiers paiement :  
  
* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Pour configurer l'extension
Voici quelques étapes pour commencer.  
  
* Autoriser les exportations de données de règlement. Pour vous aider à protéger vos données, cette option n'est pas facilement disponible.  
* Configurer des achats et des fournisseurs pour ne pas avoir besoin des numéros de document externe sur les factures. Si nécessaire, vous pouvez utiliser le numéro de référence pour vous référer à une facture spécifique.  
* Spécifier le mode de règlement de chaque fournisseur. Les modes de règlement définissent la manière dont vous payez des factures du fournisseur. Par exemple, Banque, Caisse, Chèque, ou Compte.  
* Spécifier le type de format à utiliser pour chacun de vos comptes bancaires. Par exemple, NORDEA, DANSKEBANK, SDC, etc.  
  
En outre, vous devez affecter les fournisseurs à un **Groupe compta. marché** et à un **Groupe compta. fournisseur** nationaux. Le paramètre de pays/région du fournisseur doit être le Danemark (DK). Pour plus d'informations, voir [Configuration de groupes comptabilisation](finance-posting-groups.md).  
  
### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a>Pour autoriser [!INCLUDE[d365fin](includes/d365fin_md.md)] à exporter des données de règlement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille paiement**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Modifier feuille paiement**, choisissez le lot **Banque**.  
3. Sélectionnez la case à cocher **Autoriser exportation paiement**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Pour spécifier un mode de règlement pour un fournisseur
Le tableau suivant affiche les combinaisons des modes de règlement FIK et virement GIRO pris en charge par [!INCLUDE[d365fin](includes/d365fin_md.md)].

||Type 01 | Type 04 | Type 71 | Type 73 |
|----|---|---|---|---|
|N° de compte Giro ou N° créditeur FIK ? | N° de compte Giro | N° de compte Giro | N° créditeur FIK | N° créditeur FIK|
|Autorise les messages au destinataire ? | Oui |Non |Non | Oui |
|Contient le numéro de référence du paiement ? | Non | Oui, 16 chiffres. | Oui, 15 chiffres. | Non|

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.  
2. Ouvrez la fiche, développez l'onglet **Paiements**, dans le champ **Mode de règlement** sélectionnez le mode de règlement.  
3. Selon votre sélection, vous devez renseigner d'autres champs. Voir la table ci-dessus pour une description des combinaisons.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Pour spécifier le format à utiliser pour un compte bancaire
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.  
2. Ouvrez la fiche pour le compte bancaire.  
3. Dans le champ **Format exportation paiement**, choisissez le format de votre fichier d'exportation.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Choisir les informations de paiement FIK ou Giro pour les factures fournisseur
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures achat**, puis sélectionnez le lien connexe.
2. Sélectionnez le fournisseur Rappelez-vous, il doit s'agir d'un fournisseur danois avec une adresse au Danemark.
3. Créez une facture. Les champs **Mode de règlement** et **Numéro fournisseur** sont renseignés selon les paramètres de la fiche fournisseur. Vous pouvez les modifier.
4. Dans le champ **Référence paiement**, saisissez le numéro à 15 chiffres de la facture fournisseur.  
  
    > [!Tip]
    > Il vous suffit d'ajouter les 11 derniers chiffres du numéro. [!INCLUDE[d365fin](includes/d365fin_md.md)] ajoutera quatre zéros au début du numéro.  
  
5. Validez la facture.

## <a name="to-use-the-extension-to-export-payment-data"></a>Pour utiliser l'extension d'exportation des données de paiement
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles paiement**, puis sélectionnez le lien connexe.  
2. Choisissez l'action **Proposer des feuilles de paiement fournisseur**.  
  
    > [!Tip]
    > Si vous souhaitez n'exporter que des paiements spécifiques, utilisez les options de filtrage des données.  
  
3. Si nécessaire, vous pouvez ajouter des filtres pour n'exporter que des paiements spécifiques.  
4. Dans le champ **Mode émission paiement**, sélectionnez **Paiement électronique**.  
5. Sélectionnez l'option **Exporter**.  

## <a name="see-also"></a>Voir aussi .
[Personnalisation de Dynamics 365 for [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)  
[Procédure : créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[Procédure : configurer un prélèvement SEPA](finance-how-to-set-up-sepa-direct-debit.md)  
[Procédure : valider des réceptions règlement de prélèvement SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  




