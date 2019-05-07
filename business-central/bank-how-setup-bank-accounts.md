---
title: Configurer des comptes bancaires| Microsoft Docs
description: Vous pouvez rapprocher des comptes bancaires avec les relevés de la banque.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e3ccc70405b286929c9d267e76c3ba76fd2e7e4a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "931500"
---
# <a name="set-up-bank-accounts"></a>Configuration des comptes bancaires
[!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet de gérer vos transactions bancaires à l'aide des comptes bancaires. Les comptes peuvent être en devise société ou en devise étrangère. Après avoir configuré des comptes bancaires, vous pouvez aussi utiliser l'option d'impression de chèque.

## <a name="to-set-up-bank-accounts"></a>Pour configurer des comptes bancaires
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sur la page **Comptes bancaires**, sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Pour renseigner le champ **Solde** avec un solde ouvert, vous devez valider une écriture comptable compte bancaire avec le montant en question. Vous pouvez effectuer cette opération en effectuant un rapprochement bancaire. Pour plus d'informations, reportez vous à [Rapprocher des comptes bancaires séparément](bank-how-reconcile-bank-accounts-separately.md). Sinon, vous pouvez appliquer le solde ouvert dans le cadre de la création des données générales de nouvelles sociétés à l'aide du guide de configuration assistée **Effectuer migration données métier**. Pour plus d'informations, reportez-vous à [Mise en route](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pour configurer votre compte bancaire pour importer ou exporter des fichiers bancaires
Les champs du raccourci **Transfert** de la page **Fiche compte bancaire archivé** sont associés à l'importation/exportation des flux et des fichiers bancaires. Pour plus d'informations, reportez-vous à [Configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md) et [Configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Ouvrez la fiche d'un compte bancaire pour lequel vous exporterez ou importerez des fichiers bancaires.
3. Sur le raccourci **Transfert**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Différents services d'exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes sur la page **Fiche compte bancaire**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses alors que vous essayez d'exporter le fichier. Lisez bien les courtes descriptions des champs ou reportez-vous aux rubriques de procédure associées. Par exemple, pour exporter un fichier de paiement pour un transfert électronique de fonds, les champs **Dernier n° avis de remise** et **N° interne** sont remplis. Pour plus d'informations, reportez-vous à [Exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Pour configurer des comptes bancaires fournisseur pour exporter des fichiers bancaires
Les champs du raccourci **Transfert** de la page **Fiche compte bancaire fourn.** sont associés à l'exportation des flux et des fichiers bancaires. Pour plus d'informations, reportez-vous à [Configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md) et [Exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md).

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Fournisseurs**, puis sélectionnez le lien associé.
2. Ouvrez la fiche d'un fournisseur pour le compte bancaire duquel vous exporterez des fichiers bancaires.
3. Choisissez l'option **Comptes bancaires**.
3. Renseignez les champs selon vos besoins sur la page **Fiche compte bancaire fourn.** du raccourci **Transfert**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Configuration de groupes comptabilisation](finance-posting-groups.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
