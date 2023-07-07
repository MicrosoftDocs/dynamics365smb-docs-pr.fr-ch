---
title: Mettre à jour les taux de change (contient une vidéo)
description: 'Si vous suivez des montants dans différentes devises, vous pouvez laisser Business Central ajuster les taux de devise étrangère des écritures validées avec un service externe.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates"></a>Mettre à jour des taux de change devise

Vous pouvez définir différentes devises dans [!INCLUDE [prod_short](includes/prod_short.md)], par exemple si vous achetez ou vendez dans des devises autres que votre devise locale. Ensuite, pour vous aider à suivre l’évolution des taux de change, vous pouvez gérer les devises manuellement ou configurer un service de taux de change.

## <a name="currencies"></a>Devises

> [!TIP]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], si vous recherchez des informations en temps réel sur les taux de devise étrangère (FX) ou les taux historiques, vous les trouverez sous la désignation de devise. En plus de cet article, voir aussi [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Vous spécifiez les codes devise dans la liste **Devises**, y compris les informations supplémentaires et les paramètres nécessaires pour chaque code devise. Pour plus d’informations, voir [Devises](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Exemple de transaction en devise comptabilité

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Taux de change

Les taux de change permettent de calculer la valeur en devise société (DS) de chaque transaction en devise. La page **Taux d’échange** comprend les champs suivants :

|Champ|Description|  
|---------------------------------|---------------------------------------|  
|**Date début**|Date à laquelle le taux de change a été effectué|  
|**Code devise**|Code devise lié à ce taux de change|  
|**Code devise liée**|Si cette devise fait partie d’un calcul de devise triangulaire, le code devise associé peut être configuré ici|  
|**Montant taux de change**|Le montant du taux de change est le taux à utiliser pour le code devise sélectionné sur la ligne. Il s’agit normalement de 1 ou 100|  
|**Montant taux de change lié**|Le montant du taux de change lié concerne le taux à utiliser pour le code devise liée.|  
|**Montant taux de change ajust.**|Le montant du taux de change d’ajustement est le taux à utiliser pour le code devise sélectionné sur la ligne à utiliser pour le traitement par lots **Ajuster taux de change**.|  
|**Montant taux change lié ajust.**|Le montant du taux de change d’ajustement lié est le taux à utiliser pour le code devise sélectionné sur la ligne à utiliser pour le traitement par lots **Ajuster taux de change**.|  
|**Fixer montant taux de change**|Spécifie si le taux de change de la devise peut être modifié sur les factures et les lignes feuille.|  

En général, les valeurs des champs **Montant taux de change** et **Montant taux de change lié** sont utilisées comme taux de change par défaut sur tous les nouveaux documents client et fournisseur créés à l’avenir. Le taux de change est affecté au document en fonction de la date de travail actuelle.  

> [!Note]
> Le taux de change réel sera calculé à l’aide de cette formule :
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Le montant du taux de change d’ajustement ou le montant du taux de change d’ajustement lié sera utilisé pour mettre à jour toutes les transactions banque, client ou fournisseur.  

> [!Note]
> Le taux de change réel sera calculé à l’aide de cette formule :
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Ajustement des taux de change

Comme les taux de change ne cessent de fluctuer, il convient d’ajuster périodiquement les équivalents devise supplémentaires de votre système. À défaut d’effectuer ces ajustements, les montants convertis à partir de devises étrangères (ou supplémentaires) et publiés dans la comptabilité en DS risquent d’être erronés. En outre, les écritures quotidiennes validées avant la saisie d’un taux de change quotidien dans l’application doivent être mises à jour après la saisie des informations de taux de change quotidienne.

Le traitement par lots **Ajuster taux de change** permet d’ajuster manuellement les taux de change d’écritures client, fournisseur et compte bancaire validées. Il peut également mettre à jour d’autres montants en devise report dans des écritures comptables.  

> [!TIP]
> Vous pouvez utiliser un service pour mettre à jour automatiquement les taux de change dans le système. Pour plus d’informations, reportez vous à [Configurer un service de taux de change des devises](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Cependant, cela n’ajuste pas les taux de change sur les transactions déjà enregistrées. Pour mettre à jour les taux de change sur les écritures validées, utilisez la tâche de traitement par lots **Ajuster les taux de change**.

Vous pouvez consulter un aperçu de l’effet d’un ajustement sur la comptabilisation avant de valider réellement en choisissant **Aperçu** sur la page **Ajuster les taux de change**. De plus, vous pouvez sélectionner si la validation comptable sera détaillée (par écriture) ou résumée (par devise) en sélectionnant **Résumer les écritures**. Vous pouvez également spécifier comment traiter les axes analytiques des écritures de pertes et profits non réalisés en choisissant l’une des options suivantes dans le champ **Transférer les sections analytiques** :  

- **Écriture d’origine** : Les sections analytiques des écritures comptables pour les pertes et profits non réalisées seront transférées à partir de l’écriture ajustée.
- **Par compte général** : Les écritures comptables pour les pertes et profits non réalisés auront des sections analytiques transférées à partir de l’écriture source des paramètres des axes analytiques du compte général de pertes et profits non réalisés.
- **Pas de transfert** : Les écritures comptables pour les pertes et profits non réalisés n’auront pas de sections analytiques.

### <a name="effect-on-customers-and-vendors"></a>Effet sur les clients et fournisseurs

Pour les comptes client et fournisseur, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque solde en devise et valide les montants dans le compte général spécifié dans le champ **Compte gains prévus** ou **Compte pertes prévues** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur le compte client/fournisseur en comptabilité.

Ce traitement par lots traite toutes les écritures comptables client et toutes les écritures comptables fournisseur ouvertes. En cas de différence du taux de change d’une écriture, le traitement par lots crée une écriture comptable détaillée client ou fournisseur reflétant le montant ajusté dans l’écriture comptable client ou fournisseur.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Axes analytiques sur des écritures comptables client et fournisseur

Les axes analytiques des écritures comptables client/fournisseur sont affectés aux écritures ajustement et les ajustements sont validés par combinaison de sections analytiques.

### <a name="effect-on-bank-accounts"></a>Effet sur les comptes bancaires

Pour les comptes bancaires, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque compte bancaire possédant un code devise et valide les montants dans le compte général spécifié dans le champ **Compte gains constatés** ou **Compte pertes constatées** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur les comptes bancaires spécifiés dans les groupes comptabilisation banque. Le traitement par lots calcule une écriture par devise et par groupe comptabilisation.

#### <a name="dimensions-on-bank-account-entries"></a>Axes analytiques sur des écritures compte bancaire

Les axes analytiques par défaut du compte bancaire sont affectés aux écritures ajustement pour le compte général du compte bancaire et pour le compte gain/perte.

### <a name="effect-on-gl-accounts"></a>Effet sur les comptes généraux
Si vous validez en devise report, vous pouvez demander au traitement par lots de créer de nouvelles écritures comptables pour les ajustements de devise entre devise société et devise report. Le traitement par lots calcule les différences pour chaque écriture comptable et ajuste l’écriture comptable en fonction de la valeur du champ **Ajustement taux de change** de chaque compte général.

##### <a name="dimensions-on-gl-account-entries"></a>Axes analytiques sur des écritures compte général
Les axes analytiques par défaut des comptes dans lesquels ils sont validés sont affectés aux écritures ajustement.

> [!Important]
> Avant de pouvoir utiliser le traitement par lots, vous devez entrer le taux de change ajustement qui est utilisé pour ajuster les soldes en devises. Pour ce faire sur la page **Taux de change devise**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Configurer un service de taux de change des devises
Vous pouvez utiliser un service externe pour tenir vos taux de change des devises à jour, par exemple FloatRates. 

> [!NOTE]
> La plupart des services de taux de change fournissent des données compatibles avec le processus d’importation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cependant, les données sont parfois formatées différemment et vous devrez personnaliser votre processus d’importation. Pour cela, vous pouvez utiliser l’infrastructure d’échange de données en ajoutant votre propre codeunit. Vous aurez probablement besoin de l’aide d’un développeur. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services de taux de change des devises**, puis choisissez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Service de taux de change devise**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Activez le bouton bascule **Activé** pour activer le service.

> [!NOTE]
> La vidéo suivante montre un exemple de connexion à un service de taux de change des devises, en prenant l’exemple de la Banque Centrale Européenne. Dans le segment qui décrit comment configurer les mappages de champs, le paramètre de la colonne **Source** pour **Nœud parent pour code devise** ne renverra que la première devise trouvée. Le paramètre doit être `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Pour mettre à jour les taux de change des devises à partir d’un service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devises**, puis choisissez le lien associé.
2. Choisissez l’option **Mettre à jour les taux de change**.

La valeur dans le champ **Taux de change** de la page **Devises** est mise à jour avec le dernier taux de change des devises.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/paths/use-multiple-currencies-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Devises dans Business Central](finance-currencies.md)  
[Configurer des devises](finance-set-up-currencies.md)  
[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
