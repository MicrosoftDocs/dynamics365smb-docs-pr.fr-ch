---
title: Configurer les processus financiers| Microsoft Docs
description: En savoir plus sur les tâches pour paramétrer les finances de votre société afin de les adapter à votre comptabilité ou vos audits.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 400506fe0b39944e683fd5e65e6b710ffdb9089b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182747"
---
# <a name="setting-up-finance"></a>Configuration de Finance
Avant de commencer à gérer votre activité, vous devez spécifier des règles et des valeurs par défaut concernant le mode de gestion souhaité des processus financiers de cette société. Pour commencer, vous devez configurer l'élément essentiel des enregistrements comptables de la société, à savoir le plan comptable. Configurez ensuite des groupes comptabilisation afin d'accroître l'efficacité du processus d'affectation des comptes imputables de comptabilité par défaut aux clients, fournisseurs et articles.

Certaines configurations financières peuvent être effectuées automatiquement avec des guides de configuration assistée, d'autres doivent être effectuées manuellement. Pour plus d'informations, voir [Préparation aux activités commerciales](ui-get-ready-business.md).

Vous pouvez utiliser des axes analytiques pour ajouter différents types d'informations à chaque transaction. Vous pouvez configurer les axes analytiques de base de votre société, tels que les projets et les départements. Vous pouvez ensuite ajouter, le cas échéant, des axes analytiques supplémentaires, et configurer des axes analytiques temporaires à utiliser pendant une période limitée, par exemple, dans le cadre d'une campagne de vente. Pour plus d'informations, reportez-vous à [Utilisation des axes](finance-dimensions.md).

De nombreuses tâches de configuration doivent être effectuées avant l'enregistrement des transactions financières, mais vous pouvez modifier la plupart des paramètres ultérieurement. Certaines tâches de configuration sont facultatives, par exemple, vous ne configurez des consolidations et des validations intersociétés que si vous utilisez plusieurs sociétés. D'autres tâches de configuration, telles que la spécification de la période durant laquelle la validation est autorisée, devront probablement être répétées régulièrement.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
| Choisissez la méthode pour payer vos fournisseurs. |[Définition des modes de règlement](finance-payment-methods.md) |
| Spécifiez les groupes comptabilisation qui mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux. |[Configuration de groupes comptabilisation](finance-posting-groups.md)|
|Créer des tableaux d'analyse et définir des catégories de compte pour définir le contenu des graphiques et états financiers, tels que les états Bilan et Comptes de gestion.|[Préparer la génération d'états financiers avec des tableaux d'analyse et des catégories de compte](bi-how-work-account-schedule.md)|
|Configurer une valeur de tolérance selon laquelle le système clôt une facture même si le règlement, tenant compte d'éventuelles remises, ne couvre pas intégralement le montant de la facture.|[Utilisation des écarts de règlement et des écarts d'escompte](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Définir les périodes fiscales. |[Utiliser des périodes et exercices comptables](finance-accounting-periods-and-fiscal-years.md) |
| Définissez comment déclarer les montants de taxe sur la valeur ajoutée que vous avez recueillis sur les ventes aux autorités fiscales. |[Configuration de la TVA](finance-setup-vat.md)|
|Se préparer à gérer la TVA sur encaissement en association avec des méthodes comptables basées sur la trésorerie.|[Configurer la TVA sur encaissement pour la comptabilité basée sur la trésorerie](finance-setup-unrealized-vat.md)|
| Définissez vos fonctionnalités Ventes et Achats pour gérer les paiements dans des devises étrangères.|[Activer le lettrage d'écritures comptables client en devises différentes](finance-how-enable-application-ledger-entries-different-currencies.md)
|Définissez une ou plusieurs devises supplémentaires afin que les montants soient automatiquement reportés sur des états en devise société et en devise report supplémentaires sur toutes les écritures comptables et d'autres écritures.|[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)|
|Ajustez régulièrement les équivalents en devise supplémentaire pour compenser la fluctuation des taux de change.|[Mettre à jour des taux de change devise](finance-how-update-currencies.md)|
|Définir plusieurs taux d'intérêt à utiliser pour différentes périodes pour les paiements retardés dans les transactions commerciales.|[Paramétrer plusieurs taux d'intérêt](finance-how-to-set-up-multiple-interest-rates.md)|
|Préparer à arrondir les montants des factures automatiquement lors de la création de celles-ci.|[Configuration de la fonction arrondi facture](finance-set-up-invoice-rounding.md)|
| Ajouter de nouveaux comptes au plan comptable existant. |[Configuration du plan comptable](finance-setup-chart-accounts.md) |
| Configurez les graphiques de veille économique pour analyser la trésorerie. |[Configuration d'une analyse de trésorerie](finance-setup-cash-flow-analyses.md) |
|Activer la facturation d'un client qui n'est pas configuré dans le système.|[Configurer des clients effectuant un achat au comptoir](finance-how-to-set-up-cash-customers.md)|
| Configurer l'état intracommunautaire et envoyer-le à une administration | [Configurer et enregistrer un état intracommunautaire](finance-how-setup-report-intrastat.md)|
|Vérifiez qu'une écriture dans une feuille comptabilité est affectée à plusieurs comptes lors de la validation de la feuille, soit par quantité, pourcentage ou montant.|[Utiliser les clés de ventilation dans les feuilles de comptabilité](ui-how-use-allocation-keys-general-journals.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
