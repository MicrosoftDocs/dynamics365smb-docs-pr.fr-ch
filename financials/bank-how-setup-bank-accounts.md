---
title: "Procédure : configuration de comptes bancaires| Microsoft Docs"
description: "Procédure : configuration de comptes bancaires"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 665c07a7242796718cfb01a1eb901d4df04ef8c9
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-bank-accounts"></a>Procédure : configuration de comptes bancaires
[!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet de gérer vos transactions bancaires à l'aide des comptes bancaires. Les comptes peuvent être en devise société ou en devise étrangère. Après avoir configuré des comptes bancaires, vous pouvez aussi utiliser l'option d'impression de chèque.

## <a name="to-set-up-bank-accounts"></a>Pour configurer des comptes bancaires
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Comptes bancaires**, sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pour configurer votre compte bancaire pour importer ou exporter des fichiers bancaires
Les champs du raccourci **Transfert** de la fenêtre **Fiche compte bancaire archivé** sont associés à l'importation/exportation des flux et des fichiers bancaires. Pour plus d'informations, reportez-vous à [Procédure : configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md) et [Procédure: configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md).

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Ouvrez la fiche d'un compte bancaire pour lequel vous exporterez ou importerez des fichiers bancaires.
3. Sur le raccourci **Transfert**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Remarque** : différents services d'exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes dans la fenêtre **Fiche compte bancaire**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses alors que vous essayez d'exporter le fichier. Lisez bien les courtes descriptions des champs ou reportez-vous aux rubriques de procédure associées. Par exemple, pour exporter un fichier de paiement pour un transfert électronique de fonds, le champ **Dernier n° avis de remise** et le champ **N° interne** doivent être renseignés. Pour plus d'informations, reportez-vous à [Procédure : exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Pour configurer des comptes bancaires fournisseur pour exporter des fichiers bancaires
Les champs du raccourci **Transfert** de la fenêtre **Fiche compte bancaire fourn.** sont associés à l'exportation des flux et des fichiers bancaires. Pour plus d'informations, reportez-vous à [Procédure : configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md) et [Procédure : exportation de paiements vers un fichier bancaire](payables-how-export-payments-bank-file.md).

1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Fournisseurs**, puis sélectionnez le lien associé.
2. Ouvrez la fiche d'un fournisseur pour le compte bancaire duquel vous exporterez des fichiers bancaires.
3. Choisissez l'option **Comptes bancaires**.
3. Renseignez les champs selon vos besoins dans la fenêtre **Fiche compte bancaire fourn.** du raccourci **Transfert**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Voir aussi
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

