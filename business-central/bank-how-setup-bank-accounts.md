---
title: Configurer des comptes bancaires (contient une vidéo)
description: "Découvrez comment les comptes bancaires sont utilisés dans Business\_Central et comment vous pouvez rapprocher les montants avec votre banque."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 08/03/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-bank-accounts"></a>Configuration des comptes bancaires

[!INCLUDE[prod_short](includes/prod_short.md)] vous permet de gérer vos transactions bancaires à l’aide des comptes bancaires. Les comptes peuvent être en devise société ou en devise étrangère. Après avoir configuré des comptes bancaires, vous pouvez aussi utiliser l’option d’impression de chèque. Les comptes bancaires incluent des fonctionnalités supplémentaires pour le [rapprochement des paiements](receivables-apply-payments-auto-reconcile-bank-accounts.md), le [rapprochement bancaire](bank-how-reconcile-bank-accounts-separately.md) et l’import et l’export de fichiers bancaires. Les comptes bancaires peuvent également être inclus dans les transactions en comptabilité. Chaque compte bancaire est lié à un compte du plan comptable via le groupe de comptabilisation du compte bancaire affecté. L’utilisation d’un compte bancaire dans une opération de paiement créera automatiquement une entrée à la fois sur le compte bancaire et sur le compte général connecté.  

Les comptes bancaires fonctionnent différemment selon qu’un code de devise est spécifié :

- Si le code de la devise est vide

  Toutes les transactions sur le compte bancaire seront en devise locale (DS) de l’entreprise actuelle. Si une transaction est effectuée sur le compte dans une autre devise, les montants sont comptabilisés sur le compte en DS sur la base du taux de change de la devise concernée. Tous les chèques émis à partir de ce compte doivent être émis en DS. Si le compte bancaire est utilisé dans un journal, la ligne de journal héritera automatiquement du code devise vide.  
  
- Le code devise est spécifié

  Toutes les transactions effectuées sur ce compte et les chèques émis de ce compte doivent être dans la même devise que celle spécifiée sur le compte.

Vous pouvez gagner du temps lors de la saisie des données en définissant un compte bancaire comme compte par défaut à utiliser pour la devise spécifiée pour le compte. Dans ce cas, le compte sera affecté aux documents vente et service qui utilisent la devise. Pour définir le compte le compte par défaut pour les documents vente et service, sur la page **Fiche compte bancaire**, activez le bouton bascule **Utiliser par défaut pour la devise**. Si nécessaire, vous pouvez choisir un autre compte lorsque vous travaillez sur un document.

Un compte bancaire fait partie intégrante de [!INCLUDE[prod_short](includes/prod_short.md)] et joue un rôle dans de nombreuses autres fonctionnalités. L’illustration suivante montre les relations les plus importantes :

![Illustration des relations de compte bancaire.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Vous pouvez voir que la création d’un compte bancaire le rend disponible dans tous les endroits indiqués ci-dessus et l’indique pour le compte général concerné et sur la page **Informations société**.

Un compte bancaire est généralement surveillé quotidiennement pour s’assurer que tout nouveau paiement des clients est enregistré le plus rapidement possible. Cela permet de s’assurer que le statut réel d’un client est reflété dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cela permet aux commerciaux, comptables et autres employés d’accéder aux informations les plus pertinentes et les plus à jour afin d’éviter d’appeler inutilement le client concernant des factures en souffrance ou des retards d’expédition.  

![Illustration du paiement bancaire.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Une autre tâche consiste à importer les paiements en devise du fournisseur avec les taux de change réalisés pour s’assurer que le statut réel des fournisseurs est à jour. L’utilisation de la fonctionnalité [rapprochement des paiements](receivables-apply-payments-auto-reconcile-bank-accounts.md) est le moyen le plus simple de le faire. Dans la **Feuille rapprochement bancaire**, vous pouvez importer des opérations bancaires directement depuis une application bancaire en ligne et les faire valider plus ou moins automatiquement. Le journal identifie et publie automatiquement les éléments suivants :  

- Paiements par prélèvement automatique des clients  
- Paiements clients de factures uniques  
- Paiements forfaitaires des clients  
- Paiements client en devises étrangères  
- Paiements fournisseur  
- Paiements fournisseur en devise étrangère  
- Paiements et abonnements récurrents des fournisseurs  
- Frais bancaires et intérêts  

Le rapprochement des paiements génère un gain de temps considérable lors de la comptabilisation des paiements entrants et sortants. Cependant, les opérations sur le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] ne sont pas considérées comme correctes à 100 % tant que vous n’avez pas effectué de rapprochement bancaire.  

Le rapprochement bancaire consiste à s’assurer que le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] correspond au compte externe à la banque.  

 ![Illustration du rapprochement bancaire.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Dans l’illustration ci-dessus, le côté gauche représente le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)], et le côté droit représente les transactions importées de la banque via l’application bancaire en ligne. Le diagramme du milieu montre les transactions des deux côtés, c’est-à-dire le rapprochement bancaire.

Depuis le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)], la plupart des transactions doivent être connues de la banque physique. Les quelques exceptions incluent les cas suivants :  

- Corrections publiées dans [!INCLUDE[prod_short](includes/prod_short.md)]  
- Chèques émis pas encore encaissés 
- Paiements fournisseurs qui n’ont pas été approuvés par la banque  

Depuis le compte physique en banque, des transactions qui n’ont pas été identifiées dans la feuille rapprochement bancaire arrivent tout le temps, telles que les suivantes :  

- Nouveaux abonnements fournisseurs  
- Paiements client sans description
- Intérêts bancaires
- Frais bancaires
- Frais de carte de crédit non encore rapportés

Plus les informations de mappage dans la feuille rapprochement bancaire sont optimales, plus les transactions sont enregistrées automatiquement et plus le rapprochement bancaire périodique devient facile.

Regardez dans la vidéo ci-dessous les étapes de base pour créer un compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Certains champs peuvent contenir des données sensibles, comme les champs **Code établissement**,**N° de compte bancaire**, **Code BIC** et **Code IBAN**. Pour plus d’informations, consultez [Surveiller des champs sensibles](across-log-changes.md#monitor-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Pour configurer des comptes bancaires

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sur la page **Comptes bancaires**, sélectionnez l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Par exemple, le champ **Groupe compta. banque** qui connecte le compte bancaire au compte général sous-jacent dans le bilan. Pour plus d’informations, consultez [Configurer les groupes comptabilisation](finance-posting-groups.md).

> [!TIP]
> Certains champs sont masqués jusqu’à ce que vous choisissiez l’action **Afficher plus**, généralement parce qu’ils sont rarement utilisés. D’autres doivent être ajoutés par personnalisation. Pour plus d’informations, consultez [Personnaliser votre espace de travail](ui-personalization-user.md).

Vous pouvez créer autant de comptes bancaires que nécessaire pour votre entreprise. Pour chaque compte bancaire, vous devez spécifier des informations qui rendent le compte bancaire identifiable de manière unique. Ces informations comprennent l’adresse géographique de la banque, les souches de numéros pour différents types de transactions, telles que les prélèvements automatiques et les virements, la devise dans laquelle les montants sont spécifiés et les informations utilisées pour l’importation des relevés bancaires. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance"></a>Pour entrer un solde d’ouverture

Pour renseigner le champ **Solde** avec un solde ouvert, vous devez valider une écriture comptable compte bancaire avec le montant en question. Vous pouvez effectuer cette opération en effectuant un rapprochement bancaire. Pour plus d’informations, consultez [Rapprochement des comptes bancaires](bank-how-reconcile-bank-accounts-separately.md).  
>
> Sinon, vous pouvez appliquer le solde ouvert dans le cadre de la création des données générales de nouvelles sociétés à l’aide du guide de configuration assistée **Effectuer migration données métier**. En savoir plus, [Préparation aux activités commerciales](ui-get-ready-business.md).  

> [!IMPORTANT]
> Ne validez pas le solde d’ouverture directement dans la comptabilité. Le fait d’avoir des écritures dans le compte général qui y ont été comptabilisées directement vous empêche généralement de rapprocher le compte bancaire. Avec les comptes bancaires en devise étrangère, une telle pratique entraîne l’accumulation de différences à mesure que vous validez davantage de rapprochements bancaires. En règle générale, vous comptabilisez le solde bancaire d’ouverture directement sur le compte bancaire, et le montant se retrouve ensuite dans le compte général. Sinon, vous pourrez le contrepasser plus tard en dehors du compte général que vous utilisez pour équilibrer le solde d’ouverture des écritures comptables. Dans les deux cas, vous devez équilibrer toute écriture directe sur le compte général avant de commencer votre premier rapprochement bancaire (surtout si le compte bancaire est en devise étrangère).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Pour configurer votre compte bancaire pour importer ou exporter des fichiers bancaires

Les champs associés à l’importation et à l’exportation des flux et des fichiers bancaires se trouvent sur le raccourci **Transfert** de la page **Fiche compte bancaire**. Pour plus d’informations, consultez [Utilisation de l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) et [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Ouvrez la fiche d’un compte bancaire pour lequel vous allez exporter ou importer des fichiers bancaires.
3. Sur le raccourci **Transfert**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Différents services d’exportation de fichiers et leurs formats nécessitent des valeurs de configuration différentes sur la page **Fiche compte bancaire**. Vous serez informé si des valeurs de configuration sont manquantes ou fausses lorsque vous exportez le fichier. Lisez les courtes descriptions des champs ou reportez-vous aux rubriques de procédure associées. Par exemple, pour exporter un fichier de paiement pour un transfert électronique de fonds, les champs **Dernier n° avis de remise** et **N° interne** doivent être remplis. Pour plus d’informations, consultez [Exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Les champs sur le raccourci **Transit** sur le compte bancaire servent à des fins différentes, selon que le paiement est entrant ou sortant.

L’illustration ci-dessous montre l’itinéraire des paiements entrants (les numéros dans la description correspondent à ceux de l’illustration) :

:::row:::
    :::column:::

1. Les transactions sont exportées depuis le compte bancaire dans un format .csv lisible par l’homme ou dans le propre format de la banque.
2. La *définition d’échange de données* fait correspondre les informations du fichier aux champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez [Configurer l’échange de données](across-set-up-data-exchange.md)
3. La *configuration d’exportation/d’importation de données* définit l’exportation ou l’importation et est liée à la définition de l’échange de données.
4. Le *format d’importation des relevés bancaires* lie les paramètres de l’importation au compte bancaire.
5. Les paiements sont importés via la page **Feuille rapprochement bancaire** ou la page **Rapprochement des comptes bancaires**.

  :::column-end:::
  :::column:::

        ![Illustration des paiements reçus de la banque sur des comptes bancaires.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Les paiements entrants sont toujours importés via la page **Feuille rapprochement bancaire** ou directement dans la page **Rapprochement des comptes bancaires**. En revanche, les paiements sortants peuvent provenir de n’importe quelle feuille de paiements. La seule condition préalable est que le champ **Autoriser exportation paiement** dans la feuille paiement concerné doit être sélectionné.

L’illustration ci-dessous montre l’itinéraire des paiements sortants (les numéros dans la description correspondent à ceux de l’illustration) :

:::row:::
    :::column:::

6. Les transactions sont renseignées dans un journal des paiements qui a été préparé pour l’exportation des paiements vers un fichier.
7. Le *format d’importation des relevés bancaires* lie les paramètres de l’importation au compte bancaire.
8. La *configuration d’exportation/d’importation de données* définit l’exportation ou l’importation et est liée à la définition de l’échange de données.
9. La *définition d’échange de données* fait correspondre les informations du fichier aux champs dans [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d’informations, consultez [Configurer les définitions d’échange de données](across-set-up-data-exchange.md)
10. Les paiements sont exportés du journal des paiements et importés dans le compte bancaire.

  :::column-end:::
  :::column:::

        ![Illustration des paiements reçus de la banque sur des comptes bancaires.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Pour configurer des comptes bancaires fournisseur pour exporter des fichiers bancaires

Les champs du raccourci **Transfert** de la page **Fiche compte bancaire fourn.** sont associés à l’exportation des flux et des fichiers bancaires. Pour plus d’informations, consultez [Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) et [Exporter des paiements vers un fichier bancaire](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Changer votre compte bancaire

Pour utiliser un autre compte bancaire pour votre entreprise, vous devez créer le compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)]. Nous vous recommandons de ne pas simplement remplacer les informations sur le compte que vous utilisez actuellement, car cela peut entraîner des données incorrectes. Par exemple, votre solde d’ouverture peut être incorrect ou votre flux bancaire peut cesser de fonctionner correctement. Il est important que vous fassiez la distinction entre comptes actuels et nouveaux comptes.

Après avoir créé le compte bancaire, vous devez également créer un groupe d’écritures bancaires et l’affecter à un nouveau compte général. Vous pouvez réutiliser un groupe comptabilisation bancaire existant et les transactions bancaires seront comptabilisées sur les mêmes comptes généraux que les autres comptes bancaires qui partagent ce groupe comptabilisation bancaire. Cependant, nous vous recommandons de créer un groupe d’écriture bancaire et un nouveau compte général afin que les rapprochements soient plus faciles à faire.

> [!NOTE]
> N’oubliez pas que les informations de compte bancaire sur les factures de vente ouvertes mentionnent toujours le compte bancaire d’origine. En conséquence, les paiements sont susceptibles d’être toujours enregistrés sur ce compte. Nous vous recommandons de garder les deux comptes actifs pendant un certain temps après le changement.

Pour obtenir une vue plus condensée de vos comptes de trésorerie dans les rapports financiers, utilisez les comptes **Début total** et **Total final** dans votre plan comptable, les lignes **Totalisation** dans les états financiers ou les catégories de comptes généraux. Pour plus d’informations, consultez la section [Vue d’ensemble de Business Intelligence et Financial Reporting](bi.md).

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
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
