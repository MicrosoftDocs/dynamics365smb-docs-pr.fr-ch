---
title: Réaliser des paiements avec l’extension AMC Banking (États-Unis) ou le virement SEPA (UE)
description: Traitez les paiements à vos fournisseurs en exportant un fichier avec les informations de paiement provenant des lignes feuille.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/06/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Effectuer des paiements avec l’extension AMC Banking 365 Fundamentals ou virement SEPA

Sur la page **Feuille paiement**, vous pouvez traiter les paiements à vos fournisseurs en exportant un fichier avec les informations de paiement provenant des lignes feuille. Vous pouvez ensuite télécharger le fichier vers votre banque électronique, où sont traités les transferts d’argent associés. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge le format de virement SEPA, mais dans votre pays/région, d’autres formats de paiements électroniques peuvent être disponibles.

> [!NOTE]
> Dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)], un fournisseur global de services pour convertir les données bancaires dans n’importe quel format de fichier que votre banque requiert est paramétré et connecté. Dans les versions nord-américaines, le même service peut être utilisé pour envoyer des fichiers de paiement sous forme de transfert de fonds électronique (EFT), par exemple le réseau ACH (Automated Clearing House), mais avec un processus légèrement différent. Voir l’étape 6 de [Pour exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Pour activer les virements SEPA, vous devez d’abord créer un compte bancaire, un fournisseur, et le lot de feuille général sur laquelle la feuille de paiements est basée. Vous préparez ensuite les paiements aux fournisseurs en renseignant automatiquement la page **Feuille paiement** avec les paiements dus aux dates comptabilisation spécifiées.  

> [!NOTE]  
> Lorsque vous avez vérifié que les paiements sont traités avec succès par la banque, vous pouvez passer aux lignes feuille paiement.  

## Configuration de l’extension AMC Banking 365 Fundamentals

Activez l’extension AMC Banking 365 Fundamentals pour convertir les fichiers de relevé bancaire dans un format que vous pouvez importer, ou pour convertir les fichiers de paiement exportés au format imposé par votre banque. Pour plus d’informations, voir [Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

## Configuration des virements SEPA

Sur la page **Feuille paiement**, vous pouvez exporter des paiements vers un fichier pour le charger sur votre banque électronique afin de traiter les transferts d’argent liés. [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge le format de virement SEPA, mais dans votre pays/région, d’autres formats de paiements électroniques peuvent être disponibles.  

Pour activer l’exportation de formats de fichiers bancaires qui ne sont pas pris en charge en natif dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez configurer une définition d’échange de données à l’aide de l’infrastructure d’échange de données. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).  

Avant de pouvoir traiter le paiement par voie électronique lorsque vous exportez des fichiers paiement au format de virement SEPA, vous devez exécuter les étapes de configuration suivantes :  

* Paramétrer le compte bancaire concerné pour traiter le format de virement SEPA  
* Configurer des fiches fournisseur pour traiter les paiements en exportant les fichiers au format de virement SEPA  
* Configurer la feuille comptabilité associée pour activer l’export de paiement à partir de la page **Feuille paiement**  
* Lier la définition d’échange de données pour un ou plusieurs types de règlement au(x) mode(s) de règlement approprié(s)  

> [!TIP]
> Cet article s’applique à la version générique de [!INCLUDE [prod_short](includes/prod_short.md)]. Dans votre pays ou région, des champs obligatoires supplémentaires peuvent avoir été ajoutés aux différentes pages. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Pour configurer un compte bancaire pour SEPA Credit Transfer

1. Dans la zone **Rechercher**, saisissez **Comptes bancaires**, puis sélectionnez le lien associé.  
2. Ouvrez la fiche du compte bancaire à partir duquel vous exporterez des fichiers paiement au format de virement SEPA.  
3. Sur le raccourci **Transfert**, dans le champ **Format exportation paiement**, choisissez **SEPACT**.  
4. Sur le raccourci **Général**, dans le champ **N° msg. virement**, sélectionnez une série de numéros à partir de laquelle des numéros sont attribués aux entrées de virement SEPA.  
5. Assurez-vous que le champ **IBAN** est renseigné.  

    > [!NOTE]  
    > Le champ **Code devise** doit avoir la valeur **EUR**, car les virements SEPA ne peuvent être effectués que dans la devise EURO.  

### Pour configurer une fiche fournisseur pour SEPA Credit Transfer

1. Dans la zone **Rechercher**, entrez **Fournisseurs**, puis sélectionnez le lien associé.  
2. Ouvrez la fiche du fournisseur que vous allez payer par voie électronique en exportant des fichiers paiement au format de virement SEPA.  
3. Sur le raccourci **Paiement**, dans le champ **Code mode de règlement**, sélectionnez **BANQUE**.  
4. Dans le champ **Compte bancaire préféré**, cliquez sur la banque sur laquelle l’argent est transféré lorsqu’il est traité par votre banque électronique.  

    Si vous n’avez pas encore créé de banque pour ce fournisseur, vous pouvez le faire maintenant. Pour plus d’informations, consultez [Configurer les comptes bancaires des fournisseurs pour l’exportation des fichiers bancaires](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). La valeur du champ **Compte bancaire préféré** est copiée dans le champ **Cpte bancaire destinataire** de la page **Feuille paiement**.  

### Pour définir la feuille de paiement jusqu’aux fichiers de paiement d’exportation

1. Dans la zone **Rechercher**, entrez **Feuilles paiement**, puis choisissez le lien associé.  
2. Dans le champ **Nom de la feuille**, choisissez le bouton déroulant.  
3. Dans la page **Noms feuilles comptabilité**, sélectionnez l’action **Modifier la liste**.  
4. Sur la ligne de la feuille paiement que vous allez utiliser pour exporter des paiements, activez la case à cocher **Autoriser exportation paiement**.  

### Pour lier la définition d’échange de données pour un ou plusieurs types de règlement au(x) mode(s) de règlement approprié(s)

1. Dans la zone **Rechercher**, entrez **Modes de règlement**, puis choisissez le lien associé.  
2. Sur la page **Modes de règlement**, sélectionnez le mode de paiement qui est utilisé pour exporter des paiements, puis cliquez sur le champ **Définition ligne exportation paiem.**  
3. Sur la page **Définitions ligne exportation paiem.**, sélectionnez le code spécifié dans le champ **Code** du raccourci **Définitions ligne** à l’étape 4 de la section « Pour décrire le formatage des lignes et des colonnes dans le fichier » dans [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).  

## Préparation de la feuille paiement

Renseignez la feuille paiement avec des lignes pour les paiements dus aux fournisseurs, avec la possibilité d’insérer des dates comptabilisation sur la base de la date d’échéance des documents achat associés. Pour plus d’informations, reportez-vous à [Gestion des comptes fournisseur](payables-manage-payables.md).

## Exportation des paiements vers un fichier bancaire

Lorsque vous êtes prêt à effectuer des paiements à vos fournisseurs ou rembourser vos salariés, vous pouvez exporter un fichier contenant les informations de paiement sur les lignes sur la page **Feuille paiement**. Vous pouvez ensuite transférer le fichier à votre banque afin qu’elle traite les transferts d’argent concernés.

Dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)], l’extension AMC Banking 365 Fundamentals est disponible. Dans les versions nord-américaines, la même extension peut être utilisée pour envoyer des fichiers de paiement comme transfert de fonds électronique (EFT), toutefois avec un processus légèrement différent. Voir l’étape 6 de [Pour exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Pour pouvoir exporter des fichiers de paiement à partir de la feuille paiement, vous devez spécifier le format électronique du compte bancaire concerné, et vous devez activer l’extension AMC Banking 365 Fundamentals. Pour plus d’informations, voir [Configurer des comptes bancaires](bank-how-setup-bank-accounts.md) et [Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md). Vous devez aussi cocher la case **Autoriser exportation paiement** sur la page **Noms feuilles comptabilité**. Pour en savoir plus, consultez [Utiliser des feuilles comptabilité](ui-work-general-journals.md).  

La page **Registres virement** vous permet d’afficher les fichiers paiement qui ont été exportés de la feuille paiement. À partir de cette page, vous pouvez également réexporter des fichiers paiement en cas d’erreurs techniques ou de modifications des fichiers. Notez toutefois que les fichiers EFT exportés ne sont pas affichés sur la page et ne peuvent pas être réexportés.  

### Pour exporter des paiements vers un fichier bancaire

La section suivante décrit comment payer un fournisseur par chèque. La procédure est la même pour rembourser un client par chèque.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuilles paiement**, puis choisissez le lien associé.
2. Renseignez les lignes feuille paiement. Pour plus d’informations, voir [Enregistrer des paiements et des remboursements](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Si vous utilisez EFT, vous devez sélectionner **Paiement électronique** ou **Paiement électronique-IAT** dans le champ **Mode émission paiement**. Différents services d’exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes sur les pages **Fiche compte bancaire archivé** et **Fiche compte bancaire fourn.**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses alors que vous essayez d’exporter le fichier.
    >
    > La fonction EFT ne peut être utilisée que pour les comptes bancaires dans la devise locale. Elle ne peut pas être utilisée avec une devise étrangère, indiquée par une valeur dans le champ **Code de devise**. (La valeur du champ vide signifie la devise locale.)

3. Lorsque vous avez renseigné toutes les lignes feuille paiement, sélectionnez **Exporter**.
4. Sur la page **Exporter paiements électroniques**, renseignez les champs selon vos besoins.

    Chaque message d’erreur est affiché dans le récapitulatif **Erreurs fichier de paiement** dans lequel vous pouvez également choisir un message d’erreur pour afficher les informations détaillées. Vous devez résoudre toutes les erreurs avant que le fichier de paiement ne puisse être exporté.

    > [!TIP]  
    > Lorsque vous utilisez l’extension AMC Banking 365 Fundamentals, un message d’erreur courant stipule que le numéro de compte bancaire n’a pas la longueur requise par votre banque. Pour éviter ou résoudre l’erreur, vous devez supprimer la valeur du champ **IBAN** sur la page **Fiche compte bancaire** puis, dans le champ **N° compte bancaire**, saisissez le numéro du compte bancaire dans le format requis par votre banque.

5. Sur la page **Enregistrer sous**, spécifiez l’emplacement où le fichier est exporté, puis choisissez **Enregistrer**.

    > [!NOTE]  
    > Si vous utilisez EFT, enregistrez le formulaire de remise fournisseur qui en résulte en tant que document Word ou sélectionnez d’envoyer un message e-mail directement au fournisseur. Les paiements sont à présent ajoutés sur la page **Générer fichier EFT** d’où vous pouvez générer plusieurs ordres de paiement ensemble pour économiser le coût de transmission. Pour plus d’informations, reportez-vous aux étapes suivantes.
6. Sur la page **Feuille paiement**, sélectionnez **Générer fichier EFT**.

    Sur la page **Générer fichier EFT**, tous les paiements définis pour EFT que vous avez exportés à partir de la feuille paiement pour un compte bancaire spécifique, mais qui ne sont pas encore générés, sont répertoriés dans le raccourci **Lignes**.
7. Choisissez **Générer fichier EFT** pour exporter un fichier pour tous les paiements EFT.
8. Sur la page **Enregistrer sous**, spécifiez l’emplacement où le fichier est exporté, puis choisissez **Enregistrer**.

Le fichier de paiement bancaire est exporté à l’emplacement que vous spécifiez et vous pouvez passer à son téléchargement sur votre compte bancaire électronique et effectuer les paiements. Vous pouvez ensuite valider les lignes feuille paiement exportées.

### Pour planifier la validation des paiements exportés

Si vous ne souhaitez pas valider une ligne feuille paiement pour un paiement exporté, par exemple parce que vous attendez la confirmation que la transaction a été traitée par la banque, vous pouvez simplement supprimer la ligne feuille. Lorsque vous créez ensuite une ligne feuille paiement pour payer le montant ouvert de la facture, le champ **Montant total exporté** affiche la quantité du montant ayant déjà été exportée. En outre, vous pouvez rechercher des informations détaillées concernant le total exporté en cliquant sur le bouton **Écritures reg. virement** pour visualiser des détails sur les fichiers de paiement exportés.

Si vous appliquez un processus selon lequel vous ne validez pas les paiements tant que vous n’avez pas la confirmation qu’ils ont été traités par la banque, vous pouvez contrôler ceci de deux façons.

* Dans une feuille paiement avec les lignes paiement proposées, vous pouvez trier soit la colonne **Exporté dans fichier paiement** soit la colonne **Montant total exporté**, puis supprimer les propositions de paiement pour les factures ouvertes pour lesquelles les paiements ont déjà été effectués et pour lesquelles vous ne souhaitez pas effectuer de paiements.
* Sur la page **Proposer paiements fournisseur**, où vous spécifiez les paiements à insérer dans la feuille de paiement, vous pouvez cochez la case **Ignorer les paiements exportés** si vous ne souhaitez pas insérer des lignes feuille pour les paiements qui ont déjà été exportés.

Pour afficher des informations sur les paiements exportés, sélectionnez l’action **Historique d’exportation des paiements**.

### Pour réexporter des paiements vers un fichier bancaire

Vous pouvez réexporter des fichiers paiement à partir de la page **Registres virement**. Avant de supprimer ou de valider les lignes feuille paiement, vous pouvez également réexporter le fichier de paiement à partir de la page **Feuille paiement** en l’exportant simplement à nouveau. Si vous avez supprimé ou validé les lignes feuille paiement après les avoir exportées, vous pouvez réexporter le même fichier de paiement à partir de la page **Registres virement**. Sélectionnez la ligne correspondant au lot de virements que vous souhaitez réexporter, puis, sélectionnez l’action **Réexporter les paiements dans un fichier**.

> [!NOTE]  
> Les fichiers EFT exportés ne sont pas affichés sur la page **Registres virement** et ne peuvent pas être réexportés.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Registres de virements**, puis sélectionnez le lien associé.
2. Sélectionnez une exportation de règlement que vous souhaitez réexporter, puis sélectionnez **Réexporter les paiements dans un fichier**.

## Comptabilisation des règlements

Lorsque le paiement électronique est traité avec succès par la banque, validez les paiements. Pour plus d’informations, reportez-vous à [Effectuer des paiements](payables-make-payments.md).

## Voir aussi

[Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Gestion des comptes fournisseur](payables-manage-payables.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]