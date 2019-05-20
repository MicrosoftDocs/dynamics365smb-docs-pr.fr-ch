---
title: Exporter des paiements vers un fichier de paiement électronique| Microsoft Docs
description: Pour traiter les paiements fournisseur, vous autorisez un service de conversion de données bancaires, exportez un fichier bancaire et téléchargez le fichier sur votre banque électronique pour transférer les fonds.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 539aac89d2da6b2eb81da7f6df729cdb5bc15cb1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253820"
---
# <a name="export-payments-to-a-bank-file"></a>Exporter des paiements vers un fichier bancaire
Lorsque vous êtes prêt à effectuer des paiements à vos fournisseurs ou rembourser vos salariés, vous pouvez exporter un fichier contenant les informations de paiement sur les lignes sur la page **Feuille paiement**. Vous pouvez ensuite transférer le fichier à votre banque afin qu'elle traite les transferts d'argent concernés.

Dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)], un fournisseur global de services pour convertir les données bancaires dans n'importe quel format de fichier que votre banque requiert est paramétré et connecté. Dans les versions nord-américaines, le même service peut être utilisé pour envoyer des fichiers de paiement comme transfert de fonds électronique (EFT), toutefois avec un processus légèrement différent. Voir l'étape 6 de [Pour exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).    

> [!NOTE]  
>   Pour pouvoir exporter des fichiers de paiement à partir de la feuille paiement, vous devez spécifier le format électronique du compte bancaire concerné, et vous devez activer le service de conversion des données bancaires. Pour plus d'informations, voir [Configuration de comptes bancaires](bank-how-setup-bank-accounts.md) et [Configurer le service de conversion de données bancaires](bank-how-setup-bank-data-conversion-service.md). Vous devez aussi cocher la case **Autoriser exportation paiement** sur la page **Noms feuilles comptabilité**. Pour plus d'informations, voir [Utilisation des feuilles comptabilité](ui-work-general-journals.md).  

La page **Registres virement** vous permet d'afficher les fichiers paiement qui ont été exportés de la feuille paiement. À partir de cette page, vous pouvez également réexporter des fichiers paiement en cas d'erreurs techniques ou de modifications des fichiers. Notez toutefois que les fichiers EFT exportés ne sont pas affichés sur la page et ne peuvent pas être réexportés.  

## <a name="to-export-payments-to-a-bank-file"></a>Pour exporter des paiements vers un fichier bancaire
La section suivante décrit comment payer un fournisseur par chèque. La procédure est la même pour rembourser un client par chèque.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles paiement**, puis sélectionnez le lien associé.
2. Renseignez les lignes feuille paiement. Pour plus d'informations, voir [Enregistrer des paiements et des remboursements](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Si vous utilisez EFT, vous devez sélectionner **Paiement électronique** ou **Paiement électronique-IAT** dans le champ **Mode émission paiement**. Différents services d'exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes sur les pages **Fiche compte bancaire archivé** et **Fiche compte bancaire fourn.**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses alors que vous essayez d'exporter le fichier.

3. Lorsque vous avez renseigné toutes les lignes feuille paiement, sélectionnez **Exporter**.
4. Sur la page **Exporter paiements électroniques**, renseignez les champs selon vos besoins.

    Chaque message d'erreur est affiché dans le récapitulatif **Erreurs fichier de paiement** dans lequel vous pouvez également choisir un message d'erreur pour afficher les informations détaillées. Vous devez résoudre toutes les erreurs avant que le fichier de paiement ne puisse être exporté.

    > [!TIP]  
    >   Lorsque vous utilisez le service conversion données bancaires, un message d'erreur courant stipule que le numéro de compte bancaire n'a pas la longueur requise par votre banque. Pour éviter ou résoudre l'erreur, vous devez supprimer la valeur du champ **IBAN** sur la page **Fiche compte bancaire** puis, dans le champ **N° compte bancaire**, saisissez le numéro du compte bancaire dans le format requis par votre banque.

5. Sur la page **Enregistrer sous**, spécifiez l'emplacement où le fichier est exporté, puis choisissez **Enregistrer**.

    > [!NOTE]  
    >   Si vous utilisez EFT, enregistrez le formulaire de remise fournisseur qui en résulte en tant que document Word ou sélectionnez d'envoyer un message e-mail directement au fournisseur. Les paiements sont à présent ajoutés sur la page **Générer fichier EFT** d'où vous pouvez générer plusieurs ordres de paiement ensemble pour économiser le coût de transmission. Pour plus d'informations, reportez-vous aux étapes suivantes.
6. Sur la page **Feuille paiement**, sélectionnez **Générer fichier EFT**.

    Sur la page **Générer fichier EFT**, tous les paiements définis pour EFT que vous avez exportés à partir de la feuille paiement pour un compte bancaire spécifique, mais qui ne sont pas encore générés, sont répertoriés dans le raccourci **Lignes**.
7. Choisissez **Générer fichier EFT** pour exporter un fichier pour tous les paiements EFT.
8. Sur la page **Enregistrer sous**, spécifiez l'emplacement où le fichier est exporté, puis choisissez **Enregistrer**.

Le fichier de paiement bancaire est exporté à l'emplacement que vous spécifiez et vous pouvez passer à son téléchargement sur votre compte bancaire électronique et effectuer les paiements. Vous pouvez ensuite valider les lignes feuille paiement exportées.

## <a name="to-plan-when-to-post-exported-payments"></a>Pour planifier la validation des paiements exportés
Si vous ne souhaitez pas valider une ligne feuille paiement pour un paiement exporté, par exemple parce que vous attendez la confirmation que la transaction a été traitée par la banque, vous pouvez simplement supprimer la ligne feuille. Lorsque vous créez ensuite une ligne feuille paiement pour payer le montant ouvert de la facture, le champ **Montant total exporté** affiche la quantité du montant ayant déjà été exportée. En outre, vous pouvez rechercher des informations détaillées concernant le total exporté en cliquant sur le bouton **Écritures reg. virement** pour visualiser des détails sur les fichiers de paiement exportés.

Si vous appliquez un processus selon lequel vous ne validez pas les paiements tant que vous n'avez pas la confirmation qu'ils ont été traités par la banque, vous pouvez contrôler ceci de deux façons.

* Dans une feuille paiement avec les lignes paiement proposées, vous pouvez trier soit la colonne **Exporté dans fichier paiement** soit la colonne **Montant total exporté**, puis supprimer les propositions de paiement pour les factures ouvertes pour lesquelles les paiements ont déjà été effectués et pour lesquelles vous ne souhaitez pas effectuer de paiements.
* Sur la page **Proposer paiements fournisseur**, où vous spécifiez les paiements à insérer dans la feuille de paiement, vous pouvez cochez la case **Ignorer les paiements exportés** si vous ne souhaitez pas insérer des lignes feuille pour les paiements qui ont déjà été exportés.

Pour afficher des informations sur les paiements exportés, sélectionnez l'action **Historique d'exportation des paiements**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Pour réexporter des paiements vers un fichier bancaire
Vous pouvez réexporter des fichiers paiement à partir de la page **Registres virement**. Avant de supprimer ou de valider les lignes feuille paiement, vous pouvez également réexporter le fichier de paiement à partir de la page **Feuille paiement** en l'exportant simplement à nouveau. Si vous avez supprimé ou validé les lignes feuille paiement après les avoir exportées, vous pouvez réexporter le même fichier de paiement à partir de la page **Registres virement**. Sélectionnez la ligne correspondant au lot de virements que vous souhaitez réexporter, puis, sélectionnez l'action **Réexporter les paiements dans un fichier**.

> [!NOTE]  
>   Les fichiers EFT exportés ne sont pas affichés sur la page **Registres virement** et ne peuvent pas être réexportés.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Registres virement**, puis sélectionnez le lien associé.
2. Sélectionnez une exportation de règlement que vous souhaitez réexporter, puis sélectionnez **Réexporter les paiements dans un fichier**.

## <a name="see-also"></a>Voir aussi
[Effectuer des paiements](payables-make-payments.md)  
[Fournisseurs](payables-manage-payables.md)  
[Définition des achats](purchasing-setup-purchasing.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
