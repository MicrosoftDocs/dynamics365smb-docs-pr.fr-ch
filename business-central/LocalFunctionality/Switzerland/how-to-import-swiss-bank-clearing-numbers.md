---
title: "Procédure : Importer des numéros de compensation d'une banque suisse"
description: Les numéros de compensation bancaire sont les numéros uniques utilisés pour identifier chaque agence ou succursale bancaire dans l'annuaire bancaire. Ces informations sont nécessaires pour le paiement électronique. Ce fichier peut être téléchargé à partir du site Web SIX Interbank Clearing.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fac98b748ef7adfbad06ddeb659dabecca4eed50
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779836"
---
# <a name="import-swiss-bank-clearing-numbers"></a>Importer des numéros de compensation d'une banque suisse
Les numéros de compensation bancaire sont les numéros uniques utilisés pour identifier chaque agence ou succursale bancaire dans l'annuaire bancaire. Ces informations sont nécessaires pour le paiement électronique. Ce fichier peut être téléchargé à partir du site Web [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121).  

Vous pouvez importer le fichier BC Bank Master - le fichier officiel des numéros de compensation bancaires suisses - pour mettre à jour les informations relatives au numéro de compensation bancaire dans l'annuaire bancaire. Lorsque vous importez le fichier de numéros de compensation bancaire, les données sont importées dans la table **Annuaire bancaire**, et les données existantes sont remplacées. Après avoir importé le fichier de numéros de compensation bancaire, vous pouvez définir le code établissement mis à jour pour les clients et les fournisseurs. Pour plus d'informations, voir la table Compte bancaire client et la table Compte bancaire fournisseur.  

## <a name="to-import-swiss-bank-clearing-numbers"></a>Pour importer des numéros de compensation d'une banque suisse  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Annuaire bancaire**, puis sélectionnez le lien associé.  
2.  Choisissez l'action **Importer l'annuaire bancaire**.  
3.  Dans la page **Importer l'annuaire bancaire**, dans le raccourci **Options**, sélectionnez le champ **Mettre à jour automatiquement les numéros de compensation** pour mettre à jour les numéros de compensation bancaire automatiquement.  
4.  Choisissez le bouton **Imprimer** ou le bouton **Aperçu** pour importer les numéros de compensation bancaire, puis, dans la page **Ouvrir**, localisez le fichier que vous avez téléchargé depuis le site Web SIX Interbank Clearing.
5. Cliquez sur le bouton **Ouvrir**.  

    Si vous choisissez le bouton **Imprimer**, le contenu du fichier est imprimé. Si vous choisissez le bouton **Aperçu**, la table **Annuaire bancaire** sera mise à jour et un rapport dont les numéros de compensation auront été modifiés s'affichera.  

La procédure suivante décrit comment définir des numéros d'établissement pour les comptes bancaires clients, mais les mêmes étapes s'appliquent également pour définir des numéros d'établissement pour les comptes bancaires fournisseur.  

## <a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a>Pour définir des numéros d'établissement pour les comptes bancaires clients  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients**, puis sélectionnez le lien associé.  
2.  Sélectionnez le client pour lequel vous souhaitez créer les informations d'un compte bancaire, puis sélectionnez l'action **Comptes bancaires**.  
3.  Dans la page **Liste comptes bancaires client**, sélectionnez le compte bancaire requis, puis cliquez sur l'action **Modifier**.  
4.  Sur le raccourci **Général**, renseignez le champ **Code établissement**. sélectionnez le numéro de l'agence ou de la succursale bancaire.  
5.  Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques, Suisse](swiss-electronic-payments.md)   
 [Configuration des comptes bancaires](../../bank-how-setup-bank-accounts.md)
