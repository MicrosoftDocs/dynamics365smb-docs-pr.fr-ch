---
title: Gestion financière (contient une vidéo)
description: "Découvrez comment Business\_Central répond à vos besoins en matière de gestion financière, de comptabilité, d’audit ou de tenue des registres."
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '1151, 1166, 9027, 9004'
ms.date: 02/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="financial-management"></a>Gestion financière

[!INCLUDE[prod_short](includes/prod_short.md)] comprend une configuration standard de la plupart des processus financiers, mais vous pouvez modifier la configuration pour l’adapter à vos besoins d’activité. En savoir plus sur [Configurer Finance](finance-setup-finance.md).

La configuration par défaut inclut un plan comptable et des groupes comptabilisation standard qui permettent d’accroître l’efficacité du processus d’affectation des comptes de validation de comptabilité par défaut aux clients, fournisseurs et articles.  

Les sections suivantes décrivent une séquence de tâches, avec des liens vers les rubriques qui les décrivent.  

## <a name="take-a-video-tour"></a>Faire une visite vidéo

Cette vidéo suivante présente certaines des fonctionnalités clés de la gestion des finances. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

## <a name="get-started-with-finance-capabilities"></a>Démarrer avec les capacités financières

Avant de commencer à gérer votre activité, vous devez spécifier comment vous souhaitez gérer les processus financiers de votre société.

|Pour...| Voir |
|---|---|
| Modifiez la configuration standard de [!INCLUDE[prod_short](includes/prod_short.md)] pour la plupart des processus financiers afin de l’adapter aux besoins de votre entreprise. | [Configuration de Finance](finance-setup-finance.md) | 
| En savoir plus sur la comptabilité et le plan comptable. |[Familiarisation avec les écritures comptables et les COA](finance-general-ledger.md) |

## <a name="accounting"></a>Comptabilité

Cette section décrit certains des outils comptables que vous utilisez pour enregistrer les transactions financières afin qu’elles répondent à vos besoins en matière d’enregistrement, de reporting et de gestion financière.

| Pour... | Voir |
| --- | --- |
| Ajouter des axes analytiques pour un veille économique enrichie. |[Utilisation des axes analytiques](finance-dimensions.md) |
|En savoir plus sur l’utilisation de devises supplémentaires et mettre à jour les taux de change devise automatiquement. |[Mise à jour des taux de change devise](finance-how-update-currencies.md)|
| Identifier les revenus et les dépenses dans des périodes autres que celles de la validation des transactions. |[Échelonnement des recettes et des dépenses](finance-how-defer-revenue-expenses.md)|
|Ventiler une écriture d’une feuille comptabilité dans différents comptes lorsque vous validez la feuille. |[Ventiler des coûts et des bénéfices](year-allocate-costs-income.md) |
| Affecter les surcoûts, tels que le fret et la manutention que vous encourez lors de la transaction, jusqu’aux articles impliqués. De cette façon, le coût est reflété dans l’évaluation du stock. |[Utilisation des frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md) |
| Découvrez les options disponibles pour automatiser l’envoi de factures d’abonnement à vos clients et enregistrer des revenus récurrents. |[Utilisation des revenus périodiques](finance-recurring-invoicing.md)|
|Afficher les dépenses des employés pour les activités liées au travail et effectuer les remboursements directement sur les comptes bancaires des employés.|[Enregistrement et remboursement des frais des employés](finance-how-record-reimburse-employee-expenses.md)|

## <a name="vat-and-taxes"></a>TVA et taxes

Travailler avec la TVA dans [!INCLUDE[prod_short](includes/prod_short.md)] est facile, et vous pouvez utiliser une configuration manuelle ou automatique. Ces articles fournissent des informations sur la manière de respecter les réglementations spécifiques à votre pays/région.

| Pour... | Voir |
| --- | --- |
|Calculer la taxe sur la valeur ajoutée (TVA) sur les transactions de vente et d’achat afin de pouvoir déclarer les montants aux autorités fiscales.|[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)|
|Préparer une déclaration qui répertorie la TVA des ventes, et envoyer la déclaration à l’administration fiscale de l’UE. | [Déclarer la TVA aux autorités fiscales](finance-how-report-vat.md)|
|Convertir manuellement les contrats de service pour modifier leur taux de TVA.|[Conversion des contrats de service, y compris des montants TVA](service-how-to-convert-service-contracts.md)|

## <a name="manage-receivables-and-payables"></a>Gérer les créances et les dettes

Le cœur de la finance est centré sur la gestion des créances et des dettes, l’enregistrement des transactions, le rapprochement des comptes bancaires, le paiement des fournisseurs, la réception des paiements des clients, le remboursement des dépenses des employés, etc. Cette section fournit des liens vers les concepts de base.

| Pour... | Voir |
| --- | --- |
| Lettrer des paiements entrants, rapprocher des comptes bancaires pendant le lettrage de paiement et collecter des soldes échus. |[Gestion des comptes client](receivables-manage-receivables.md) |
| Effectuer des paiements, lettrer les paiements sortants et traiter les chèques. |[Gestion des comptes fournisseur](payables-manage-payables.md) |
|Faire en sorte que vos clients envoient leur règlement avant la livraison ou envoyer le paiement à vos fournisseurs avant qu’ils n’effectuent la livraison.|[Facturation d’acomptes](finance-invoice-prepayments.md)|
| Rapprocher et transférer des fonds entre comptes bancaires. |[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md) |

## <a name="manage-multiple-companies"></a>Gérer plusieurs entreprises

[!INCLUDE [prod_short](includes/prod_short.md)] offre aux petites et moyennes entreprises une solution de gestion d′entreprise facile à utiliser et à entretenir à un faible coût de possession.

| Pour... | Voir |
| --- | --- |
|Configurer les partenaires intersociétés et traiter les transactions, manuellement ou automatiquement, entre les personnes morales dans la même société.|[Gestion des transactions intersociétés](intercompany-manage.md)|
|Combiner des écritures comptables de plusieurs sociétés dans une société consolidée virtuelle pour l’analyse financière.|[Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md)|
| Travaillez plus étroitement avec les entreprises apparentées auxquelles vous avez accès et obtenez des informations sur les données relatives aux points d’intérêt clés (KPI). | [Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md)|

## <a name="period-end-reporting-and-related-tasks"></a>Rapports de fin de période et tâches connexes

À la fin de chaque période comptable ou à la fin de l’année fiscale, il y a un certain nombre de tâches administratives à effectuer. Par exemple, vous voudrez probablement vous assurer que tous les documents et journaux sont comptabilisés, que les données monétaires sont à jour, que les comptes sont clôturés, etc. Les tâches réelles dépendent de votre société.

| Pour... | Voir |
| --- | --- |
|Gérer les coûts ajustés et de fabrication, générer des états sur les coûts et rapprocher les coûts avec la comptabilité.|[Gestion des coûts ajustés](finance-manage-inventory-costs.md)|
| Importez des transactions de paie de votre fournisseur de paie dans les écritures comptables. |[Importation des transactions de paie](finance-how-import-payroll-transactions.md)|
|Apprendre à utiliser le tableau de bord Comptable, à inviter un comptable externe et à utiliser le Hub Entreprise pour gérer les comptes de plusieurs clients.|[Expériences des comptables dans Business Central](finance-accounting.md)| 

## <a name="managerial-accounting"></a>Comptabilité de gestion

En tant que chef d’entreprise ou contrôleur de gestion, il est important que vous puissiez préparer et analyser les données commerciales dont vous avez besoin pour prendre des décisions éclairées. Les articles du tableau suivant vous aident à préparer les données. Pour en savoir plus sur l’analyse, consultez [Vue d’ensemble de Business Intelligence et Reporting](reports-bi-reporting.md).

| Pour... | Voir |
| --- | --- |
|Analyser les coûts de fonctionnement de votre activité en affectant les coûts réels et budgétés des opérations, des départements, des produits et des projets relatifs aux centres de coûts.|[Comptabilité pour les coûts](finance-manage-cost-accounting.md)|
| Contrôlez le flux de trésorerie entrant et sortant de votre entreprise. |[Analyse des trésoreries dans votre société](finance-analyze-cash-flow.md) |
|Procédure de suivi et de bout en bout sur l’utilisation des états financiers pour effectuer des prévisions de trésorerie.|[Procédure pas-à-pas : créer des prévisions de trésorerie à l’aide d’états financiers](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md)|
| Utiliser des états financiers et des aperçus dans Microsoft Excel. |[Analyse des états financiers dans Excel](finance-analyze-excel.md) |

## <a name="free-e-learning-modules"></a>Modules d’apprentissage en ligne gratuits

Vous souhaitez en savoir plus sur [!INCLUDE[prod_short](includes/prod_short.md)] à votre rythme ? 

[!INCLUDE[footer-include](includes/footer-banner.md)]

## <a name="see-also"></a>Voir aussi

[Configuration de Finance](finance-setup-finance.md)  
[Utiliser le module Ventes](sales-manage-sales.md)  
[Utiliser le module Achats](purchasing-manage-purchasing.md)  
[Clôture des périodes fiscales](year-close-years-periods.md)  
[Gestion des projets](projects-manage-projects.md)  
[Importation des données à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]
