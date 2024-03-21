---
title: Configurer les processus financiers
description: En savoir plus sur les tâches pour paramétrer les finances de votre société afin de les adapter à votre comptabilité ou vos audits.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-finance"></a>Configuration de Finance

Avant de commencer à gérer votre activité, vous devez spécifier comment vous souhaitez gérer les processus financiers de cette société. Pour commencer, vous devez configurer l’élément essentiel des enregistrements comptables de la société, à savoir le plan comptable. Configurez ensuite des groupes comptabilisation afin d’accroître l’efficacité du processus d’affectation des comptes imputables de comptabilité par défaut aux clients, fournisseurs et articles.

Certaines configurations financières peuvent être effectuées automatiquement avec des guides de configuration assistée, d’autres doivent être effectuées manuellement. En savoir plus, [Préparation aux activités commerciales](ui-get-ready-business.md). La page **Paramètres comptabilité** spécifie comment gérer les différents processus comptables dans votre société. Par exemple, vous utilisez cette page pour spécifier les détails arrondi facture, le code devise de votre devise société, les formats adresse et si vous souhaitez utiliser une devise report. En savoir plus [Comprendre la comptabilité et le plan comptable](finance-general-ledger.md).  

Vous pouvez utiliser des axes analytiques pour ajouter différents types d’informations à chaque transaction. Vous pouvez configurer les axes analytiques de base de votre société, tels que *Projets* et *Départements*. Ultérieurement, ajoutez d’autres dimensions lorsque vous en avez besoin. Par exemple, vous pouvez configurer des dimensions temporaires à utiliser pendant une période de temps limitée, comme pendant une campagne de vente. En savoir plus sur [Utiliser les dimensions](finance-dimensions.md).

De nombreuses tâches de configuration doivent être effectuées avant l’enregistrement des transactions financières, mais vous pouvez ajuster la plupart des paramètres selon les besoins. Cela dit, il existe également des tâches de configuration facultatives. Par exemple, vous devez configurer uniquement les comptabilisations et les consolidations intersociétés si vous utilisez plusieurs sociétés. D’autres tâches de configuration, telles que la spécification de la période durant laquelle la validation est autorisée, devront probablement être répétées régulièrement.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

| À | Voir |
| --- | --- |
|Afficher ou modifier les comptes généraux pour lesquels toutes les écritures comptables sont validées|[Configurer ou modifier le plan comptable](finance-setup-chart-accounts.md)|
| Indiquez comment vous souhaitez être payé par les clients et comment vous souhaitez payer vos fournisseurs. |[Paramétrer les modes de paiement](finance-payment-methods.md) |
| Spécifier les conditions de paiement pour gérer les dates d’échéance et calculer les escomptes possibles.|[Configurer les conditions de paiement](finance-payment-terms.md) |
| Spécifiez les groupes comptabilisation qui mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux. |[Configurer les groupes comptabilisation](finance-posting-groups.md)|
|Créer des états financiers et définir des catégories de compte pour définir le contenu des graphiques et états financiers, tels que les états Bilan et Comptes de gestion.|[Préparer Financial Reporting avec des données financières et des catégories de compte](bi-how-work-account-schedule.md)|
|Configurer une valeur de tolérance selon laquelle le système clôt une facture même si le règlement, tenant compte d’éventuelles remises, ne couvre pas intégralement le montant de la facture.|[Utilisation des écarts de règlement et des écarts d’escompte](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Définir les périodes fiscales. |[Utiliser des périodes et exercices comptables](finance-accounting-periods-and-fiscal-years.md) |
|Configurer des conditions de facturation qui rappellent à vos clients d’effectuer le paiement.|[Configurer les conditions et niveaux de relance](finance-setup-reminders.md)|
| Définir comment déclarer les montants de taxe sur la valeur ajoutée (TVA) que vous avez recueillis sur les ventes aux autorités fiscales. |[Configuration de la TVA](finance-setup-vat.md)|
|Se préparer à gérer la TVA sur encaissement en association avec des méthodes comptables basées sur la trésorerie.|[Configurer la TVA sur encaissement pour la comptabilité basée sur la trésorerie](finance-setup-unrealized-vat.md)|
|Définir les devises étrangères dans lesquelles vous achetez, vendez ou faites état des transactions.|[Configurer des devises](finance-set-up-currencies.md)|
| Définir vos fonctionnalités Ventes et Achats pour gérer les paiements dans des devises étrangères.|[Activer le lettrage d’écritures comptables client en devises différentes](finance-how-enable-application-ledger-entries-different-currencies.md)
|Définir une ou plusieurs devises supplémentaires afin que les montants soient automatiquement reportés sur des états en devise société et en devise report supplémentaires sur toutes les écritures comptables et d’autres écritures.|[Configurer une devise report supplémentaire](finance-how-setup-additional-currencies.md)|
|Ajustez régulièrement les équivalents en devise supplémentaire pour compenser la fluctuation des taux de change.|[Mettre à jour des taux de change devise](finance-how-update-currencies.md)|
|Définir plusieurs taux d’intérêt à utiliser pour différentes périodes pour les paiements retardés dans les transactions commerciales.|[Paramétrer plusieurs taux d’intérêt](finance-how-to-set-up-multiple-interest-rates.md)|
|Faire en sorte que les montants soient automatiquement arrondis au fur et à mesure que les factures sont créées.|[Configuration de la fonction arrondi facture](finance-set-up-invoice-rounding.md)|
| Ajouter de nouveaux comptes au plan comptable existant. |[Configuration du plan comptable](finance-setup-chart-accounts.md) |
| Configurez les graphiques de veille économique pour analyser la trésorerie. |[Configuration d’une analyse de trésorerie](finance-setup-cash-flow-analyses.md) |
|Activer la facturation d’un client qui n’est pas configuré dans le système.|[Configurer des clients effectuant un achat au comptoir](finance-how-to-set-up-cash-customers.md)|
| Configurer l’état intracommunautaire et envoyer-le à une administration. | [Configurer et enregistrer un état intracommunautaire](finance-how-setup-report-intrastat.md)|
|Vérifier qu’une écriture dans une feuille comptabilité est affectée à plusieurs comptes lors de la validation de la feuille, soit par quantité, pourcentage ou montant.|[Utiliser les clés de ventilation dans les feuilles de comptabilité](ui-how-use-allocation-keys-general-journals.md)|
|Configurer des codes journaux et des codes motif que vous pouvez utiliser pour suivre les pistes d’audit.|[Configuration des codes source et des codes de motif pour les pistes d’audit](finance-setup-trail-codes.md)|
|Spécifier les états par défaut à utiliser pour différents types de documents.|[Sélection des états dans Business Central](across-report-selections.md)|

> [!TIP]
> En fonction de votre emplacement géographique, certaines pages Business Central peuvent contenir des champs qui ne sont pas décrits dans les articles répertoriés ci-dessus, car ils s’appliquent à des fonctionnalités locales ou à des personnalisations. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Analyse de la trésorerie dans votre société](finance-analyze-cash-flow.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
