---
title: Configurer des comptes bancaires| Microsoft Docs
description: "Vous pouvez rapprocher des comptes bancaires dans Financials des relevés de la banque."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7c626c96e3dc4d445a463a050af5c6663cb4ade1
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-bank-accounts"></a>Configuration des comptes bancaires
[!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet de gérer vos transactions bancaires à l'aide des comptes bancaires. Les comptes peuvent être en devise société ou en devise étrangère. Après avoir configuré des comptes bancaires, vous pouvez aussi utiliser l'option d'impression de chèque.

## <a name="to-set-up-bank-accounts"></a>Pour configurer des comptes bancaires
1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Comptes bancaires**, sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Pour renseigner le champ **Solde** avec un solde ouvert, vous devez valider une écriture comptable compte bancaire avec le montant en question. Vous pouvez effectuer cette opération en effectuant un rapprochement bancaire. Pour plus d'informations, reportez vous à [Rapprocher des comptes bancaires séparément](bank-how-reconcile-bank-accounts-separately.md). Sinon, vous pouvez appliquer le solde ouvert dans le cadre de la création des données générales de nouvelles sociétés à l'aide de la configuration assistée **Effectuer migration données métier**. Pour en savoir plus, voir [Bienvenue dans [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pour configurer votre compte bancaire pour importer ou exporter des fichiers bancaires
Les champs du raccourci **Transfert** de la fenêtre **Fiche compte bancaire archivé** sont associés à l'importation/exportation des flux et des fichiers bancaires. Pour plus d'informations, reportez-vous à [Configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md) et [Configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md).

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un compte bancaire pour lequel vous exporterez ou importerez des fichiers bancaires.
3. Sur le raccourci **Transfert**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Différents services d'exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes dans la fenêtre **Fiche compte bancaire**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses alors que vous essayez d'exporter le fichier. Lisez bien les courtes descriptions des champs ou reportez-vous aux rubriques de procédure associées. Par exemple, pour exporter un fichier de paiement pour un transfert électronique de fonds, les champs **Dernier n° avis de remise** et **N° interne** sont remplis. Pour plus d'informations, reportez-vous à [Exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Pour configurer des comptes bancaires fournisseur pour exporter des fichiers bancaires
Les champs du raccourci **Transfert** de la fenêtre **Fiche compte bancaire fourn.** sont associés à l'exportation des flux et des fichiers bancaires. Pour plus d'informations, reportez-vous à [Configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md) et [Exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md).

1. Choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche d'un fournisseur pour le compte bancaire duquel vous exporterez des fichiers bancaires.
3. Choisissez l'option **Comptes bancaires**.
3. Renseignez les champs selon vos besoins dans la fenêtre **Fiche compte bancaire fourn.** du raccourci **Transfert**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

