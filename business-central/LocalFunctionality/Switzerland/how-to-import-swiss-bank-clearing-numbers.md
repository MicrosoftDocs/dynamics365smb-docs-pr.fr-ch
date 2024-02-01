---
title: 'Importer des numéros de compensation d''une banque suisse [CH]'
description: Cet article vous indique la procédure d'importation de numéros de compensation d'une banque suisse à l'aide de la version suisse de Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 11501
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="import-swiss-bank-clearing-numbers-in-the-swiss-version"></a>Importer des numéros de compensation d'une banque suisse dans la version suisse

Les numéros de compensation bancaire sont les numéros uniques utilisés pour identifier chaque agence ou succursale bancaire dans l'annuaire bancaire. Ces informations sont nécessaires pour le paiement électronique. Ce fichier peut être téléchargé à partir du site Web [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121).  

Vous pouvez importer le fichier .txt BC Bank Master - le fichier officiel des numéros de compensation bancaires suisses - pour mettre à jour les informations relatives au numéro de compensation bancaire dans l'annuaire bancaire. Lorsque vous importez le fichier de numéros de compensation bancaire, les données sont importées dans la table **Annuaire bancaire**, et les données existantes sont remplacées. Après avoir importé le fichier de numéros de compensation bancaire, vous pouvez définir le code établissement mis à jour pour les clients et les fournisseurs. Pour plus d'informations, voir la table Compte bancaire client et la table Compte bancaire fournisseur.  

## <a name="to-import-swiss-bank-clearing-numbers"></a>Pour importer des numéros de compensation d'une banque suisse

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Annuaire bancaire**, puis sélectionnez le lien associé.  
2. Choisissez l'action **Importer l'annuaire bancaire**.  
3. Cliquez sur le bouton **...** pour ouvrir le fichier des numéros de compensation bancaires .txt.
4. Dans la page **Importer l'annuaire bancaire**, dans le raccourci **Options**, sélectionnez le champ **Mettre à jour automatiquement les numéros de compensation** pour mettre à jour les numéros de compensation bancaire automatiquement.  
5. Choisissez le bouton **Imprimer** ou le bouton **Aperçu** pour importer les numéros de compensation bancaire, puis, dans la page **Ouvrir**, localisez le fichier que vous avez téléchargé depuis le site Web SIX Interbank Clearing.
6. Cliquez sur le bouton **Ouvrir**.  

   Si vous choisissez le bouton **Imprimer**, le contenu du fichier est imprimé. Si vous choisissez le bouton **Aperçu**, la table **Annuaire bancaire** sera mise à jour et un rapport dont les numéros de compensation auront été modifiés s'affichera.  

La procédure suivante explique comment définir des numéros d'établissement pour les comptes bancaires clients. La même procédure s'applique également pour définir des numéros d'établissement pour les comptes bancaires fournisseur.  

## <a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a>Pour définir des numéros d'établissement pour les comptes bancaires clients

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Clients**, puis sélectionnez le lien associé.  
2. Sélectionnez le client pour lequel vous souhaitez créer les informations d'un compte bancaire, puis sélectionnez l'action **Comptes bancaires**.  
3. Dans la page **Liste comptes bancaires client**, sélectionnez le compte bancaire requis, puis cliquez sur l'action **Modifier**.  
4. Sur le raccourci **Général**, renseignez le champ **Code établissement**. sélectionnez le numéro de l'agence ou de la succursale bancaire.  
5. Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi

[Paiements électroniques, Suisse](swiss-electronic-payments.md)  
[Configuration des comptes bancaires](../../bank-how-setup-bank-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
