---
title: Configurer les processus financiers| Microsoft Docs
description: En savoir plus sur les tâches pour paramétrer les finances de votre société afin de les adapter à votre comptabilité ou vos audits.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: fc8f52e5ef9fdeb8a2add9cf030a348012f25366
ms.sourcegitcommit: 02f1633213793bfc040ad0d2a96fe76572215aa5
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 11/12/2019
ms.locfileid: "2798514"
---
# <a name="setting-up-finance"></a>Configuration de Finance
Pour vous aider à démarrer rapidement, [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut des configurations standard pour la plupart des processus financiers. Si vous devez modifier les configurations en fonction de votre activité, n'hésitez pas. Par exemple, à partir du tableau de bord, vous pouvez utiliser un guide de configuration assistée pour configurer la taxe sur les ventes en fonction de votre situation géographique.  

Toutefois, il existe quelques éléments que vous devez configurer vous-même. Par exemple, si vous souhaitez utiliser les axes analytiques comme base pour la veille économique.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| Pour | Voir |
| --- | --- |
| Choisissez la méthode pour payer vos fournisseurs. |[Définition des modes de règlement](finance-payment-methods.md) |
| Spécifiez les groupes comptabilisation qui mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux. |[Configuration de groupes comptabilisation](finance-posting-groups.md)|
|Créer des tableaux d'analyse et définir des catégories de compte pour définir le contenu des graphiques et états financiers, tels que les états Bilan et Comptes de gestion.|[Préparer la génération d'états financiers avec des tableaux d'analyse et des catégories de compte](bi-how-work-account-schedule.md)|
|Configurer une valeur de tolérance selon laquelle le système clôt une facture même si le règlement, tenant compte d'éventuelles remises, ne couvre pas intégralement le montant de la facture.|[Utilisation des écarts de règlement et des écarts d'escompte](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Définir les périodes fiscales. |[Ouvrir un nouvel exercice comptable](finance-how-open-new-fiscal-year.md) |
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

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Gestion des comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
