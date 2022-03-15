---
title: Configurer des comptes bancaires (contient une vidéo)
description: Découvrez comment les comptes bancaires sont utilisés dans Business Central et comment vous pouvez rapprocher les montants avec votre banque.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: 4c305d4ba1f4208eb7a3c5845d4b32bb40f930e6
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382326"
---
# <a name="set-up-bank-accounts"></a>Configuration des comptes bancaires

[!INCLUDE[prod_short](includes/prod_short.md)] vous permet de gérer vos transactions bancaires à l’aide des comptes bancaires. Les comptes peuvent être en devise société ou en devise étrangère. Après avoir configuré des comptes bancaires, vous pouvez aussi utiliser l’option d’impression de chèque. Les comptes bancaires incluent des fonctionnalités supplémentaires pour le [rapprochement des paiements](receivables-apply-payments-auto-reconcile-bank-accounts.md), le [rapprochement bancaire](bank-how-reconcile-bank-accounts-separately.md) et l’import et l’export de fichiers bancaires. Les comptes bancaires peuvent également être inclus dans les transactions en comptabilité. Chaque compte bancaire est lié à un compte du plan comptable via le groupe de comptabilisation du compte bancaire affecté. L’utilisation d’un compte bancaire dans une opération de paiement créera automatiquement une entrée à la fois sur le compte bancaire et sur le compte général connecté.  

Les comptes bancaires fonctionnent différemment selon qu’un code de devise est spécifié :

- Le code de la devise est vide

  Toutes les transactions sur le compte bancaire seront en devise locale (DS) de l’entreprise actuelle. Si une transaction est effectuée sur le compte dans une autre devise, les montants sont comptabilisés sur le compte en DS sur la base du taux de change de la devise concernée. Tous les chèques émis à partir de ce compte doivent être émis en DS. Si le compte bancaire est utilisé dans un journal, la ligne de journal héritera automatiquement du code devise vide.  
- Le code devise est spécifié

  Toutes les transactions effectuées sur ce compte doivent être dans la même devise que celle spécifiée sur le compte. Tous les chèques émis à partir de ce compte doivent également avoir cette devise.  

Un compte bancaire fait partie intégrante de [!INCLUDE[prod_short](includes/prod_short.md)] et joue un rôle dans de nombreuses autres fonctionnalités. L’illustration suivante montre les relations les plus importantes :

![Illustration des relations de compte bancaire.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Cela signifie que la création d’un compte bancaire le rend disponible dans tous les endroits indiqués ci-dessus et l’indique pour le compte général concerné et sur la page **Informations société**.

Un compte bancaire est généralement surveillé quotidiennement pour s’assurer que tout nouveau paiement des clients est enregistré le plus rapidement possible. Cela permet de s’assurer que le statut réel des clients est reflété dans [!INCLUDE[prod_short](includes/prod_short.md)] afin que les vendeurs, comptables et autres employés aient accès à des informations pertinentes et à jour. De cette façon, ils évitent les appels inutiles au client concernant des factures en retard ou des retards d’expédition.  

![Illustration du paiement bancaire.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Une autre tâche consiste à importer les paiements en devise du fournisseur avec les taux de change réalisés pour s’assurer que le statut réel des fournisseurs est à jour. Le moyen le plus simple de s’assurer que le compte bancaire est mis à jour consiste à utiliser la fonctionnalité de [rapprochement des paiements](receivables-apply-payments-auto-reconcile-bank-accounts.md). Dans la **Feuille rapprochement bancaire**, vous pouvez importer des opérations bancaires directement depuis une application bancaire en ligne et les faire valider plus ou moins automatiquement. Le journal identifie et publie automatiquement les éléments suivants :  

- Paiements par prélèvement automatique des clients  
- Paiements clients de factures uniques  
- Paiements forfaitaires des clients  
- Paiements client en devises étrangères  
- Paiements fournisseur  
- Paiements fournisseur en devise étrangère  
- Paiements et abonnements récurrents des fournisseurs  
- Frais bancaires et intérêts  

Le rapprochement des paiements génère un gain de temps considérable lors de la comptabilisation des paiements entrants et sortants. Cependant, les opérations sur le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] n’est pas considéré comme correct à 100 % tant que vous n’avez pas effectué de rapprochement bancaire.  

Le rapprochement bancaire consiste à s’assurer que le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] correspond au compte externe à la banque.  

 ![Illustration du rapprochement bancaire.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Dans l’illustration ci-dessus, le côté gauche représente le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)], et le côté droit représente les transactions importées de la banque via l’application bancaire en ligne. Le diagramme du milieu montre les transactions des deux côtés, c’est-à-dire le rapprochement bancaire.

Depuis le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)], la plupart des transactions doivent être connues de la banque physique. Les seules exceptions incluent les cas suivants :  

- Corrections publiées dans [!INCLUDE[prod_short](includes/prod_short.md)]  
- Chèques émis pas encore encaissés  
- Paiements fournisseurs qui n’ont pas été approuvés par la banque  

Depuis le compte physique en banque, des transactions inconnues qui n’ont pas été identifiées dans le journal de rapprochement des paiements arrivent tout le temps, telles que les suivantes :  

- Nouveaux abonnements fournisseurs  
- Paiements client sans description
- Intérêts bancaires
- Frais bancaires
- Frais de carte de crédit qui n’ont pas encore été signalés

Plus les informations de mappage que vous faites dans le journal de rapprochement des paiements sont optimales, plus les transactions sont enregistrées automatiquement et plus le rapprochement bancaire périodique devient facile.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Certains champs peuvent contenir des données sensibles, comme les champs **Code établissement**,**N° de compte bancaire**, **Code BIC** et **Code IBAN**. Pour plus d’informations, voir [Surveillance des champs sensibles](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Pour configurer des comptes bancaires

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sur la page **Comptes bancaires**, sélectionnez l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Par exemple, le champ **Groupe compta. banque** connecte le compte bancaire au compte général sous-jacent dans le bilan. Pour plus d’informations, voir [Configuration des groupes comptabilisation](finance-posting-groups.md).

> [!TIP]
> Certains champs sont masqués jusqu’à ce que vous choisissiez l’action **Afficher plus**, généralement parce qu’ils sont rarement utilisés. D’autres doivent être ajoutés par personnalisation. Pour plus d’informations, voir [Personnaliser votre espace de travail](ui-personalization-user.md).

Vous pouvez créer autant de comptes bancaires que nécessaire pour votre entreprise. Pour chaque compte bancaire, vous devez spécifier des informations qui rendent le compte bancaire identifiable de manière unique. Ces informations comprennent l’adresse géographique de la banque, les séries de numéros pour différents types de transactions, telles que les prélèvements automatiques et les virements, la devise dans laquelle les montants sont spécifiés et les informations utilisées pour l’importation des relevés bancaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->
> [!NOTE]
> Pour renseigner le champ **Solde** avec un solde ouvert, vous devez valider une écriture comptable compte bancaire avec le montant en question. Vous pouvez effectuer cette opération en effectuant un rapprochement bancaire. Pour plus d’informations, voir [Rapprocher des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md).  
>
> Sinon, vous pouvez appliquer le solde ouvert dans le cadre de la création des données générales de nouvelles sociétés à l’aide du guide de configuration assistée **Effectuer migration données métier**. Pour plus d’informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).  

> [!IMPORTANT]
> Il est important que vous ne comptabilisiez pas le solde d’ouverture directement dans la comptabilité. Le fait d’avoir des écritures dans le compte général qui sont comptabilisées directement sur le compte général vous empêchera généralement de rapprocher le compte bancaire ou, dans le cas de comptes bancaires en devise étrangère, entraînera l’accumulation de différences au fur et à mesure que vous postez plus de rapprochements bancaires. Souvent, vous comptabilisez le solde bancaire d’ouverture directement sur le compte bancaire, et le montant se retrouve ensuite dans le compte général. Sinon, contrepassez-le plus tard sur un compte général désigné que vous avez utilisé pour équilibrer le solde d’ouverture des écritures comptables. Dans les deux cas, vous devez équilibrer toute écriture directe sur le compte général avant de commencer votre premier rapprochement bancaire, et surtout si le compte bancaire est en devise étrangère.  

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pour configurer votre compte bancaire pour importer ou exporter des fichiers bancaires

Les champs du raccourci **Transfert** de la page **Fiche compte bancaire archivé** sont associés à l’importation/exportation des flux et des fichiers bancaires. Pour plus d’informations, voir [Utilisation de l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) et [Configuration du service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Ouvrez la fiche d’un compte bancaire pour lequel vous exporterez ou importerez des fichiers bancaires.
3. Sur le raccourci **Transfert**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Différents services d’exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes sur la page **Fiche compte bancaire**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses alors que vous essayez d’exporter le fichier. Lisez bien les courtes descriptions des champs ou reportez-vous aux rubriques de procédure associées. Par exemple, pour exporter un fichier de paiement pour un transfert électronique de fonds, les champs **Dernier n° avis de remise** et **N° interne** sont remplis. Pour plus d’informations, reportez-vous à [Exportation de paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Les champs sur le raccourci **Transit** sur le compte bancaire servent à des fins différentes, selon que le paiement est entrant ou sortant.

L’illustration montre l’itinéraire des paiements entrants :

:::row:::
    :::column:::
        1. Les transactions sont exportées depuis le compte bancaire dans un format .csv lisible par l’homme ou dans le propre format de la banque.
        <br><br>
2. La *définition d’échange de données* fait correspondre les informations du fichier aux champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configurer un échange de données](across-set-up-data-exchange.md)
<br><br>
3. La *configuration d’exportation/d’importation de données* définit l’exportation ou l’importation et est liée à la définition de l’échange de données.
<br><br>
4. Le *format d’importation des relevés bancaires* lie les paramètres de l’importation au compte bancaire.
<br><br>
5. Les paiements sont importés via la page **Feuille rapprochement bancaire** ou la page **Rapprochement des comptes bancaires**.
    :::column-end:::
    :::column:::
        ![Illustration des paiements reçus de la banque sur des comptes bancaires.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Les paiements entrants sont toujours importés via la page **Feuille rapprochement bancaire** ou directement dans la page **Rapprochement des comptes bancaires**. En revanche, les paiements sortants peuvent provenir de n’importe quelle feuille de paiements. La seule condition préalable est que le champ **Autoriser exportation paiement** dans la feuille paiement concerné doit être sélectionné.

L’illustration montre l’itinéraire des paiements sortants :

:::row:::
    :::column:::
        6. Les transactions renseignées dans un journal des paiements qui a été préparé pour l’exportation des paiements vers un fichier.
        <br><br>
        7. Le *format d’importation des relevés bancaires* lie les paramètres de l’importation au compte bancaire.
        <br><br>
        8. La *configuration d’exportation/d’importation de données* définit l’exportation ou l’importation et est liée à la définition de l’échange de données.
        <br><br>
        9. La *définition d’échange de données* fait correspondre les informations du fichier aux champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, voir [Configurer un échange de données](across-set-up-data-exchange.md)
        <br><br>
        10. Les paiements sont exportés du journal des paiements et importés dans le compte bancaire.
    :::column-end:::
    :::column:::
        ![Illustration des paiements reçus de la banque sur des comptes bancaires.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Pour configurer des comptes bancaires fournisseur pour exporter des fichiers bancaires

Les champs du raccourci **Transfert** de la page **Fiche compte bancaire fourn.** sont associés à l’exportation des flux et des fichiers bancaires. Pour plus d’informations, voir [Utilisation de l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) et [Exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche d’un fournisseur pour le compte bancaire duquel vous exporterez des fichiers bancaires.
3. Choisissez l’option **Comptes bancaires**.
4. Dans la **Liste des comptes bancaires des fournisseurs**, choisissez le compte bancaire approprié ou ajoutez un nouveau compte bancaire.  
5. Renseignez les champs selon vos besoins sur la page **Fiche compte bancaire fourn.** du raccourci **Transfert**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Certains champs du compte bancaire fournisseur peuvent contenir des données sensibles, comme les champs **Code établissement**, **N° de compte bancaire**, **Code BIC** et **Code IBAN**. Pour plus d’informations, voir [Surveillance des champs sensibles](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Changer votre compte bancaire

Si vous souhaitez utiliser un autre compte bancaire pour votre entreprise, vous devez créer le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)]. Nous vous recommandons de ne pas simplement remplacer les informations sur le compte que vous utilisez actuellement, car cela peut entraîner des données incorrectes. Par exemple, votre solde d’ouverture peut être incorrect ou votre flux bancaire peut cesser de fonctionner correctement. Il est important que vous fassiez la distinction entres comptes actuels et nouveaux comptes.

Après avoir créé le compte bancaire, vous devez également créer un groupe d’écritures bancaires et l’affecter à un nouveau compte général. Vous pouvez réutiliser un groupe comptabilisation bancaire existant et les transactions bancaires seront comptabilisées sur les mêmes comptes généraux que les autres comptes bancaires qui partagent le groupe comptabilisation bancaire. Cependant, nous vous recommandons de créer un groupe d’écriture bancaire et un nouveau compte général afin que les rapprochements soient plus faciles à faire.

> [!NOTE]
> N’oubliez pas que les informations de compte bancaire sur les factures de vente ouvertes mentionnent toujours le compte bancaire d’origine. En conséquence, les paiements sont susceptibles d’être toujours enregistrés sur ce compte. Nous vous recommandons de garder les deux comptes actifs pendant un certain temps après le changement.

Pour obtenir une vue plus condensée de vos comptes de trésorerie dans les rapports financiers, utilisez les comptes **Début total** et **Total final** dans votre plan comptable, les lignes **Totalisation** dans les tableaux de comptes ou les catégories de comptes généraux. Pour plus d’informations, consultez la section [Vue d’ensemble de Business Intelligence et Financial Reporting](bi.md).

## <a name="see-also"></a>Voir aussi

[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Configuration de groupes comptabilisation](finance-posting-groups.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Prélèvement SEPA dans Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Pour configurer votre compte bancaire pour les prélèvements automatiques SEPA](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Pour configurer un compte bancaire pour les virements SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Effectuer des paiements avec l’extension AMC Banking 365 Fundamentals ou les virements SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Rapprochement paiement](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Familiarisation avec les écritures comptables et les COA](finance-general-ledger.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
