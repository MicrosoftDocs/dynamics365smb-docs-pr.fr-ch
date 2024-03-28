---
title: Mettre à jour les taux de change (contient une vidéo)
description: Découvrez comment utiliser Business Central pour ajuster les taux de change pour les montants dans différentes devises.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 11/13/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="update-currency-exchange-rates"></a>Mise à jour des taux de change devise

Si vous négociez dans différentes devises, vous devez suivre les variations des taux de change. [!INCLUDE [prod_short](includes/prod_short.md)] vous aide à gérer et mettre à jour les taux de change manuellement ou automatiquement et configurer un service de taux de change de devise.

## <a name="currencies"></a>Devises

> [!TIP]  
> Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous trouverez des informations en temps réel sur les taux de devise étrangère (FX) ou les taux historiques, sous le terme Devise. Pour plus d’informations, voir [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Spécifiez les codes devise dans la liste **Devises**, y compris les informations supplémentaires et les paramètres nécessaires pour chaque code devise. Pour plus d’informations, voir [Devises](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Exemple de transaction en devise comptabilité

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Taux de change

Les taux de change permettent de calculer la valeur en devise société (DS) de chaque transaction en devise. La page **Taux d’échange** comprend les champs suivants :

|Champ|Désignation|  
|---------------------------------|---------------------------------------|  
|**Date début**|Date à laquelle le taux de change a été effectué.|  
|**Code devise**|Code devise lié à ce taux de change.|  
|**Code devise liée**|Si cette devise fait partie d’un calcul de devise triangulaire, configurez le code devise associé ici.|  
|**Montant taux de change**|Le montant du taux de change est le taux pour le code devise sélectionné sur la ligne. Il s’agit normalement de 1 ou 100.|  
|**Montant taux de change lié**|Le montant du taux de change lié concerne le taux à utiliser pour le code devise liée.|  
|**Montant taux de change ajust.**|Le taux pour le code devise sélectionné sur la ligne à utiliser pour le traitement par lots **Ajuster taux de change**.|  
|**Montant taux change lié ajust.**|Le taux pour le code devise sélectionné sur la ligne à utiliser pour le traitement par lots **Ajuster taux de change**.|  
|**Fixer montant taux de change**|Spécifie si le taux de change peut être modifié sur les factures et les lignes feuille.|  

En général, les valeurs des champs **Montant taux de change** et **Montant taux de change lié** sont utilisées comme taux de change par défaut sur tous les nouveaux documents client et fournisseur créés à l’avenir. Le taux de change est affecté au document en fonction de la date de travail actuelle.  

> [!Note]
> Le taux de change réel est calculé à l’aide de cette formule :
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Le montant du taux de change de l’ajustement ou le montant du taux de change de l’ajustement relationnel est utilisé pour mettre à jour toutes les transactions banque, client ou fournisseur ouvertes.  

> [!Note]
> Le taux de change réel est calculé à l’aide de cette formule :
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjust-exchange-rates"></a>Ajustement des taux de change

Comme les taux de change ne cessent de fluctuer, ajustez régulièrement d’autres équivalents de devise. Si vous ne le faites pas, les montants que vous avez convertis à partir de devises étrangères (ou autres) et validés dans la comptabilité en devise locale peuvent être incorrects. De plus, mettez à jour les écritures quotidiennes validées avant de saisir un taux de change quotidien.

Vous pouvez utiliser le traitement par lots **Ajuster taux de change** pour ajuster manuellement les taux de change pour les écritures client, fournisseur et compte bancaire validées. Le traitement par lots peut également mettre à jour d’autres montants en devise de déclaration dans les écritures comptables.  

> [!TIP]
> Vous pouvez utiliser un service pour mettre à jour automatiquement les taux de change dans le système. Pour plus d’informations, reportez vous à [Configurer un service de taux de change des devises](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service). Cependant, cela n’ajuste pas les taux de change sur les transactions déjà enregistrées. Pour mettre à jour les taux de change sur les écritures validées, utilisez la tâche de traitement par lots **Ajuster les taux de change**.

Vous pouvez également spécifier comment l’ajustement traite les axes analytiques des écritures de pertes et profits non réalisés en choisissant l’une des options suivantes dans le champ **Validation d’axe analytique** :  

* **Axes analytiques source** : transférez les sections analytiques des écritures comptables pour les pertes et profits non réalisés à partir de l’écriture que vous ajustez.  
* **Pas d’axes analytiques** : ne transférez pas les sections analytiques pour les pertes et profits non réalisés vers les écritures comptables. [!INCLUDE [prod_short](includes/prod_short.md)] utilise toujours les paramètres d’axe analytique par défaut, par exemple, **Code obligatoire**, **Même code** ou **Pas de code**. Si les écritures de transaction source ont des sections analytiques, l’ajustement crée des écritures sans sections analytiques.  
* **Axes analytiques compte général** : transférez les sections analytiques de l’écriture source des paramètres d’axe analytique du compte général de pertes et profits non réalisés vers les écritures comptables.

> [!NOTE]
> Pour utiliser la fonctionnalité en version préliminaire, activez la fonction **Mise à jour des fonctionnalités : activer l’utilisation du nouvel ajustement du taux de change extensible, y compris la révision de la validation** sur la page **[Gestion des fonctionnalités](https://businesscentral.dynamics.com/?page=2610)**.

> [!IMPORTANT]
> En raison des exigences locales en Suisse, nous vous déconseillons d’activer la fonction **Mise à jour des fonctionnalités : activer l’utilisation du nouvel ajustement du taux de change extensible, y compris la révision de la validation** dans la version Suisse (CH).

## <a name="preview-the-effect-of-an-adjustment"></a>Prévisualiser l’effet d’un ajustement

Vous pouvez prévisualiser l’effet d’un ajustement du taux de change sur la validation avant la validation réelle en choisissant l’action **Aperçu validation** sur la page de demande du rapport **Ajustement des taux de change** (rapport 596). Sur la page de demande, vous pouvez spécifier ce qu’il faut inclure dans l’aperçu :

* Obtenir une validation détaillée dans la comptabilité par écriture.
* Obtenir une validation récapitulative par devise. Sélectionnez simplement le champ **Ajuster par écriture** dans le rapport **Ajustement des taux de change**.

### <a name="effect-on-customers-and-vendors"></a>Effet sur les clients et les fournisseurs

Pour les comptes client et fournisseur, le traitement par lots utilise le taux de change valide à la date de validation spécifiée pour le traitement par lots pour ajuster la device. Le traitement par lots calcule les différences pour chaque solde en devise et valide les montants dans le compte général spécifié dans le champ **Compte gains prévus** ou **Compte pertes prévues** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur le compte client/fournisseur en comptabilité.

Ce traitement par lots traite toutes les écritures comptables client et toutes les écritures comptables fournisseur ouvertes. S’il y a une différence de taux de change pour une écriture, le traitement par lots crée une écriture comptable client ou fournisseur détaillée. La nouvelle écriture reflète le montant ajusté dans l’écriture comptable client ou fournisseur.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Axes analytiques des écritures comptables client et fournisseur

[!INCLUDE [prod_short](includes/prod_short.md)] attribue les axes analytiques des écritures comptables client ou fournisseur aux écritures ajustement et valide les ajustements pour chaque combinaison de sections analytiques.

### <a name="effect-on-bank-accounts"></a>Effet sur les comptes bancaires

Pour les comptes bancaires, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque compte bancaire possédant un code devise et valide les montants dans le compte général spécifié dans le champ **Compte gains constatés** ou **Compte pertes constatées** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur les comptes bancaires spécifiés dans les groupes comptabilisation banque. Le traitement par lots calcule une écriture par devise et par groupe comptabilisation.

#### <a name="dimensions-on-bank-account-entries"></a>Axes analytiques des écritures compte bancaire

Les axes analytiques par défaut du compte bancaire sont affectés aux écritures ajustement pour le compte général du compte bancaire et pour le compte gain/perte.

### <a name="effect-on-gl-accounts"></a>Effet sur les comptes généraux

Si vous validez dans une autre devise de déclaration, le traitement par lots peut créer de nouvelles écritures comptables pour les ajustements de devise entre la devise locale et l’autre devise de déclaration. Le travail par lots calcule les différences pour chaque écriture comptable. Il ajuste l’écriture comptable en fonction de la valeur du champ **Ajustement taux de change** de chaque compte général.

#### <a name="dimensions-on-gl-account-entries"></a>Axes analytiques des écritures compte général

Les axes analytiques par défaut des comptes dans lesquels ils sont validés sont affectés aux écritures ajustement.

> [!Important]
> Avant de pouvoir utiliser le traitement par lots, entrez le taux de change ajustement qui est utilisé pour ajuster les soldes en devises. Pour ce faire sur la page **Taux de change devise**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="set-up-a-currency-exchange-rate-service"></a>Configuration d’un service de taux de change des devises

Vous pouvez utiliser un service externe pour tenir vos taux de change des devises à jour, par exemple FloatRates. 

> [!NOTE]
> La plupart des services de taux de change fournissent des données compatibles avec le processus d’importation dans [!INCLUDE[prod_short](includes/prod_short.md)]. Cependant, les données sont parfois formatées différemment et vous devez personnaliser votre processus d’importation. Pour cela, vous pouvez utiliser l’infrastructure d’échange de données en ajoutant votre propre codeunit. Vous aurez probablement besoin de l’aide d’un développeur. Pour plus d’informations, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Services de taux de change des devises**, puis sélectionnez le lien associé.
2. Sélectionnez l’action **Nouveau**.
3. Sur la page **Service de taux de change devise**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Activez le bouton bascule **Activé** pour activer le service.

> [!NOTE]
> La vidéo suivante montre comment vous connecter à un service de taux de change des devises, en prenant l’exemple de la Banque Centrale Européenne. Dans le segment qui décrit comment configurer les mappages de champs, le paramètre de la colonne **Source** pour **Nœud parent pour code devise** ne renvoie que la première devise trouvée. Le paramètre doit être `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="update-currency-exchange-rates-through-a-service"></a>Mettre à jour les taux de change des devises à partir d’un service

Suivez les étapes indiquées pour mettre à jour les taux de change via un service :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Devises**, puis sélectionnez le lien associé.
2. Sélectionner l’option **Mettre à jour les taux de change**.

## <a name="correct-mistakes"></a>Corriger les erreurs

De temps en temps, vous devrez peut-être corriger une erreur dans une opération de paiement associée à des ajustements des gains et des pertes de change. Vous pouvez utiliser l’action **Contrepasser transaction** sur les **Écritures comptables bancaires**, **Écritures comptables client** et **Ecritures comptables fournisseur** pour délettrer les écritures comptables et annuler la transaction de paiement.

> [!NOTE]
> Lorsque vous délettrez les écritures comptables et contrepassez un paiement pour une écriture à laquelle sont associés des ajustements de taux de change, l’annulation comptabilise les écritures de contrepassation pour les ajustements. Vous devrez peut-être réexécuter l’ajustement du taux de change pour obtenir le solde actuel correct.

## <a name="see-also"></a>Voir aussi

## <a name="see-also-1"></a>Voir aussi

[Devises dans Business Central](finance-currencies.md)  
[Configurer des devises](finance-set-up-currencies.md)  
[Configuration d’une devise report supplémentaire](finance-how-setup-additional-currencies.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
