---
title: Mise à jour des taux de change des devises| Microsoft Docs
description: Pour utiliser plusieurs devises dans votre société, vous pouvez définir un code pour chaque devise et utiliser un service externe de taux de change.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a9fa636fb68a428da3c587e59be1bf76cf976207
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "926953"
---
# <a name="update-currency-exchange-rates"></a>Mettre à jour des taux de change devise
Les sociétés opérant dans un nombre croissant de pays/régions, il est de plus en plus important qu'elles puissent échanger ou générer des états financiers dans plusieurs devises. Vous devez définir un code pour chaque devise utilisée si vous achetez ou vendez dans des devises différentes de votre devise locale, si vous disposez de comptes client ou fournisseur dans d'autres devises, ou si vous enregistrez des transactions comptables dans des devises différentes.

Votre comptabilité est configurée pour utiliser votre devise société (DS), mais vous pouvez la configurer pour utiliser une autre devise avec un taux de change courant. Si vous désignez une deuxième devise comme « devise report supplémentaire », [!INCLUDE[d365fin](includes/d365fin_md.md)] enregistre automatiquement les montants d'état en DS et dans cette devise report supplémentaire pour chaque écriture comptable, ainsi que pour d'autres écritures, telles que les écritures TVA. Pour plus d'informations, voir [Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Ajustement des taux de change
Comme les taux de change ne cessent de fluctuer, il convient d'ajuster périodiquement les équivalents devise supplémentaires de votre système. À défaut d'effectuer ces ajustements, les montants convertis à partir de devises étrangères (ou supplémentaires) et publiés dans la comptabilité en DS risquent d'être erronés. En outre, les écritures quotidiennes validées avant la saisie d'un taux de change quotidien dans le programme doivent être mises à jour après la saisie des informations de taux de change quotidienne.

Le traitement par lots **Ajuster taux de change** permet d'ajuster manuellement les taux de change d'écritures client, fournisseur et compte bancaire validées. Il peut également mettre à jour d'autres montants en devise report dans des écritures comptables. Vous pouvez aussi faire ajuster les taux de change automatiquement à l'aide d'un service. Pour plus d'informations, reportez vous à [Configurer un service de taux de change des devises](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Effet sur les clients et fournisseurs
Pour les comptes client et fournisseur, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque solde en devise et valide les montants dans le compte général spécifié dans le champ **Compte gains prévus** ou **Compte pertes prévues** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur le compte client/fournisseur en comptabilité.

Ce traitement par lots traite toutes les écritures comptables client et toutes les écritures comptables fournisseur ouvertes. En cas de différence du taux de change d'une écriture, le traitement par lots crée une écriture comptable détaillée client ou fournisseur reflétant le montant ajusté dans l'écriture comptable client ou fournisseur.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Axes analytiques sur des écritures comptables client et fournisseur
Les axes analytiques des écritures comptables client/fournisseur sont affectés aux écritures ajustement et les ajustements sont validés par combinaison de sections analytiques.

### <a name="effect-on-bank-accounts"></a>Effet sur les comptes bancaires
Pour les comptes bancaires, le traitement par lots ajuste la devise en utilisant le taux de change valide à la date de comptabilisation spécifiée dans le traitement par lots. Le traitement par lots calcule les différences pour chaque compte bancaire possédant un code devise et valide les montants dans le compte général spécifié dans le champ **Compte gains constatés** ou **Compte pertes constatées** de la page **Devises**. Les écritures de contrepartie sont automatiquement validées sur les comptes bancaires spécifiés dans les groupes comptabilisation banque. Le traitement par lots calcule une écriture par devise et par groupe comptabilisation.

#### <a name="dimensions-on-bank-account-entries"></a>Axes analytiques sur des écritures compte bancaire
Les axes analytiques par défaut du compte bancaire sont affectés aux écritures ajustement pour le compte général du compte bancaire et pour le compte gain/perte.

### <a name="effect-on-gl-accounts"></a>Effet sur les comptes généraux
Si vous validez en devise report, vous pouvez demander au traitement par lots de créer de nouvelles écritures comptables pour les ajustements de devise entre devise société et devise report. Le traitement par lots calcule les différences pour chaque écriture comptable et ajuste l'écriture comptable en fonction de la valeur du champ **Ajustement taux de change** de chaque compte général.

##### <a name="dimensions-on-gl-account-entries"></a>Axes analytiques sur des écritures compte général
Les axes analytiques par défaut des comptes dans lesquels ils sont validés sont affectés aux écritures ajustement.

> [!Important]
> Avant de pouvoir utiliser le traitement par lots, vous devez entrer le taux de change ajustement qui est utilisé pour ajuster les soldes en devises. Pour ce faire sur la page **Taux de change devise**.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Configurer un service de taux de change des devises
Vous pouvez utiliser un service externe pour tenir vos taux de change des devises à jour, par exemple FloatRates.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Services de taux de change devise**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Sur la page **Service de taux de change devise**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Activez la case à cocher **Activé** pour activer le service.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Pour mettre à jour les taux de change des devises à partir d'un service
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Devises**, puis choisissez le lien associé.
2. Choisissez l'option **Mettre à jour les taux de change**.

La valeur dans le champ **Taux de change** de la page **Devises** est mise à jour avec le dernier taux de change des devises.

## <a name="see-also"></a>Voir aussi
[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
