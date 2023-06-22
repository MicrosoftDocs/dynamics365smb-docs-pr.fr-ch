---
title: Comptabilité et tenue de livres
description: Cet article fournit des informations qui vous aideront à utiliser Microsoft Dynamics 365 Business Central pour effectuer correctement la comptabilité et la tenue de livres de votre entreprise.
author: altotovi
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, bookkeeping'
ms.search.form: '16, 39, 108'
ms.date: 03/14/2023
ms.author: altotovi
---

# <a name="accounting-and-bookkeeping" />Comptabilité et tenue de livres

La comptabilité est une fonction essentielle de toute solution de planification des ressources d’entreprise (ERP), ainsi que de la plupart des entreprises. La comptabilité représente le processus d’enregistrement et de catalogage des transactions financières d’une entreprise, puis de récupération, de mesure, de synthèse et de présentation des résultats sous la forme de différents états souvent requis par la législation locale. L’objectif principal de ce processus est d’aider la direction de l’entreprise à comprendre les finances de l’entreprise et à mesurer les résultats des activités économiques de l’entreprise.

La tenue de livres fait partie du processus comptable et consiste à enregistrer régulièrement toutes les transactions financières d’une entreprise. [!INCLUDE[prod_short](includes/prod_short.md)] est un système ERP qui comprend des outils intégrés pour faciliter la tenue des livres dans le système. De nombreuses actions peuvent être effectuées automatiquement.

Cet article fournit un aperçu des processus de tenue de livres, y compris les règles, les procédures et d’autres directives incluses dans [!INCLUDE[prod_short](includes/prod_short.md)]. Le contenu de cet article est destiné à aider les comptables et les aides-comptables à accomplir leur travail quotidien dans ce système ERP. Pour une aide supplémentaire, un assistant contextuel est intégré à [!INCLUDE[prod_short](includes/prod_short.md)]. Cet assistant contient des liens vers des informations liées à la page en cours et des instructions de travail avec le processus concerné. Pour y accéder, sélectionnez le bouton [**Aide**](product-help-and-support.md) dans le coin supérieur droit pour ouvrir le volet **Aide**. Utilisez ensuite les liens des sections **À propos de cette tâche ou de cette page** et **Ressources connexes de Microsoft Learn**.

La vidéo suivante présente certaines des fonctionnalités clés de la comptabilité et de la tenue de livres.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

Le tableau suivant décrit une série de tâches et fournit des liens vers les articles qui les décrivent.

| Tâche | Article |
|------|---------|
| Afficher ou modifier les comptes généraux pour lesquels toutes les écritures comptables sont validées. | [Configurer ou modifier le plan comptable](finance-setup-chart-accounts.md) |
| Indiquer comment vos clients vous paieront et comment vous paierez vos fournisseurs. | [Configuration des modes de règlement](finance-payment-methods.md) |
| Spécifier les conditions de paiement pour gérer les dates d’échéance et calculer les escomptes possibles. | [Configuration des conditions de paiement](finance-payment-terms.md) |
| Spécifier les groupes comptabilisation qui mappent des entités (telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat) dans des comptes généraux. | [Configuration des groupes comptabilisation](finance-posting-groups.md)|
| Créer des états financiers et définir des catégories de compte pour définir le contenu des graphiques et états financiers, tels que les états **Bilan** et **Compte de gestion**. | [Préparation de Financial Reporting avec des données financières et des catégories de compte](bi-how-work-account-schedule.md)|
| Configurer la valeur de tolérance que le système utilise pour clore une facture même si le règlement, tenant compte d’éventuelles remises, ne couvre pas intégralement le montant de la facture. | [Utilisation des écarts de règlement et des écarts d’escompte](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Définir les périodes fiscales. | [Utiliser des périodes et exercices comptables](finance-accounting-periods-and-fiscal-years.md) |
| Configurer des conditions de facturation qui rappellent à vos clients d’effectuer les paiements. | [Configuration des conditions et niveaux](finance-setup-reminders.md)|
| Définir comment déclarer les montants de taxe sur la valeur ajoutée (TVA) que vous avez recueillis sur les ventes aux autorités fiscales. | [Configuration de la TVA (taxe sur la valeur ajoutée)](finance-setup-vat.md) |
| Déterminer comment vous allez gérer la TVA sur encaissement en association avec des méthodes comptables basées sur la trésorerie. | [Configuration de la TVA sur encaissement pour la comptabilité basée sur la trésorerie](finance-setup-unrealized-vat.md) |
| Définir les devises étrangères dans lesquelles vous achetez, vendez ou faites état des transactions. | [Configurer des devises](finance-set-up-currencies.md) |
| Définir vos fonctionnalités de vente et d’achat pour gérer les paiements dans des devises étrangères. | [Activation du lettrage d’écritures comptables en devises différentes](finance-how-enable-application-ledger-entries-different-currencies.md) |
| Définir une ou plusieurs devises supplémentaires afin que les montants soient automatiquement reportés dans la devise société et dans une devise report supplémentaires sur toutes les écritures comptables et d’autres écritures. | [Configuration d’une devise report supplémentaire](finance-how-setup-additional-currencies.md) |
| Ajuster régulièrement les équivalents en devise supplémentaire pour compenser la fluctuation des taux de change. | [Mise à jour des taux de change devise](finance-how-update-currencies.md)|
| Définir plusieurs taux d’intérêt pour différentes périodes associées aux paiements en retard dans les transactions commerciales. | [Configuration de plusieurs taux d’intérêt](finance-how-to-set-up-multiple-interest-rates.md) |
| Faire en sorte que les montants soient automatiquement arrondis au fur et à mesure que les factures sont créées. | [Configuration de l’arrondi facture](finance-set-up-invoice-rounding.md) |
| Ajouter de nouveaux comptes au plan comptable (COA) existant. | [Configuration du plan comptable](finance-setup-chart-accounts.md) |
| Configurez les graphiques de veille économique pour analyser la trésorerie. | [Configuration d’une analyse de trésorerie](finance-setup-cash-flow-analyses.md) |
| Permettre aux clients qui ne sont pas configurés dans le système d’être facturés. | [Configuration des clients effectuant un achat en espèces](finance-how-to-set-up-cash-customers.md) |
| Configurer l’état intracommunautaire et envoyer-le à une administration. | [Configurer et enregistrer un état intracommunautaire](finance-how-setup-report-intrastat.md) |
| Vérifier qu’une écriture feuille est affectée à plusieurs comptes lors de la validation de la feuille, soit par quantité, pourcentage ou montant. | [Utilisation des clés de ventilation dans les feuilles comptabilité](ui-how-use-allocation-keys-general-journals.md) |
| Configurer des codes journaux et des codes motif à utiliser pour suivre les pistes d’audit. | [Configuration des codes source et des codes de motif pour les pistes d’audit](finance-setup-trail-codes.md) |
| Spécifier les états par défaut utilisés pour différents types de documents. | [Sélection des états dans Business Central](across-report-selections.md) |
| Lettrer des paiements entrants, rapprocher des comptes bancaires pendant le lettrage de paiement et collecter des soldes échus. | [Gestion des comptes client](receivables-manage-receivables.md) |
| Effectuer des paiements, lettrer les paiements sortants et traiter les chèques. | [Gestion des comptes fournisseur](payables-manage-payables.md) |
| Faire en sorte que vos clients envoient leur règlement avant la livraison ou envoyer le paiement à vos fournisseurs avant qu’ils n’effectuent la livraison. | [Facturation d’acomptes](finance-invoice-prepayments.md) |
| Rapprocher et transférer des fonds entre comptes bancaires. | [Rapprochement de comptes bancaires](bank-manage-bank-accounts.md) |
| Configurer les partenaires intersociétés et traiter manuellement ou automatiquement les transactions entre les personnes morales dans la même société. | [Gestion des transactions intersociétés](intercompany-manage.md) |
| Analyser les coûts de fonctionnement de votre activité en affectant les coûts réels et budgétés des opérations, des départements, des produits et des projets relatifs aux centres de coûts. | [Comptabilité pour les coûts](finance-manage-cost-accounting.md) |
| Gérer les coûts ajustés et de fabrication, générer des états sur les coûts et rapprocher les coûts avec la comptabilité. | [Gestion des coûts ajustés](finance-manage-inventory-costs.md) |
| Gérer et déclarer les encaissements et les décaissements. | [Vue d’ensemble de la trésorerie]( finance-cash-flow-overview.md) |
| Contrôler le flux de trésorerie entrant et sortant de votre entreprise. | [Analyse des trésoreries dans votre société](finance-analyze-cash-flow.md) |
| Suivre un processus de bout en bout qui utilise les états financiers pour effectuer des prévisions de trésorerie. | [Créer des prévisions de trésorerie à l’aide d’états financiers](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| En savoir plus sur les écritures comptables et le COA. | [Familiarisation avec les écritures comptables et les COA](finance-general-ledger.md) |
| Combiner des écritures comptables de plusieurs sociétés dans une société consolidée virtuelle pour l’analyse financière. | [Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md)|
| Ajouter des axes analytiques pour une BI plus riche. | [Utilisation des axes analytiques](finance-dimensions.md) |
| Créer des budgets comptabilité pour prévoir différentes activités financières et affecter des axes analytiques aux fins de BI. | [Création de budgets comptables](finance-how-create-budgets.md) |
| Enregistrer les revenus et les frais directement dans la comptabilité sans valider les documents commerciaux appropriés. | [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md) |
| Contrepasser les écritures contrepassées pour annuler les validations de valeur dans la feuille comptabilité ou les validations de quantité sur des documents achat et vente. | [Inversion d’une validation feuille et annuler les réceptions/envois](finance-how-reverse-journal-posting.md) |
| Ventiler une écriture d’une feuille comptabilité dans différents comptes lorsque vous validez la feuille. | [Ventiler des coûts et des bénéfices](year-allocate-costs-income.md) |
| Affecter les surcoûts, tels que le fret et la manutention que vous encourez lors de la transaction, jusqu’aux articles qui sont impliqués. Le coût est alors reflété dans l’évaluation du stock. | [Utilisation des frais annexes pour comptabiliser les coûts commerciaux supplémentaires](payables-how-assign-item-charges.md) |
| Valider les dépenses des employés pour les activités liées au travail et effectuer les remboursements directement sur les comptes bancaires des employés. | [Enregistrement et remboursement des frais des employés](finance-how-record-reimburse-employee-expenses.md) |
| Affecter les revenus et les dépenses à des périodes qui diffèrent des périodes au cours desquelles les transactions ont été réellement comptabilisées. | [Échelonnement des recettes et des dépenses](finance-how-defer-revenue-expenses.md) |
| Découvrez les options disponibles pour envoyer automatiquement les factures d’abonnement à vos clients et enregistrer les revenus récurrents. | [Utilisation des revenus périodiques](finance-recurring-invoicing.md) |
| Utiliser des devises supplémentaires et mettre à jour automatiquement les taux de change devise. | [Mise à jour des taux de change devise](finance-how-update-currencies.md) |
| Importez des transactions de paie de votre fournisseur de paie dans les écritures comptables. | [Importation des transactions de paie](finance-how-import-payroll-transactions.md) |
| Calculer la TVA sur les transactions de vente et d’achat afin de pouvoir déclarer les montants aux autorités fiscales. | [Utilisation de la TVA sur les ventes et les achats](finance-work-with-vat.md) |
| Préparer une déclaration qui répertorie la TVA des ventes, et envoyer la déclaration à l’administration fiscale de l’UE. | [Déclarer la TVA aux autorités fiscales](finance-how-report-vat.md) |
| Convertir manuellement les contrats de service pour modifier leur taux de TVA. | [Conversion des contrats de service, y compris des montants TVA](service-how-to-convert-service-contracts.md) |
| Utiliser des états financiers et des aperçus dans Microsoft Excel. | [Analyse des états financiers dans Excel](finance-analyze-excel.md) |
| Utiliser le tableau de bord Comptable, inviter un comptable externe et utiliser le Hub Entreprise pour gérer les comptes de plusieurs clients. | [Expériences des comptables dans Business Central](finance-accounting.md) |
| Configurez les états intracommunautaires pour assurer le commerce avec les autres membres de l’UE conformément à la législation locale. | [Configuration de la déclaration d’échanges de biens]( finance-how-setup-report-intrastat.md) |
| Remplir, valider et soumettre un état intracommunautaire. | [Utilisation les états de déclaration d’échanges de biens]( finance-how-report-intrastat.md) |
| Configurer, remplir, valider et soumettre l’état de déclaration de services pour les échanges de services dans toute l’UE. | [Configurer et utiliser la déclaration de services]( finance-how-setup-use-service-declaration.md) |
| Créer des immobilisations, affecter des méthodes d’amortissement, valider des acquisitions et des valeurs résiduelles et imprimer les listes d’immobilisations. | [Acquérir des immobilisations](fa-how-acquire.md) |
| Enregistrer les visites de service, valider les coûts de maintenance et surveiller les coûts de maintenance. | [Mettre à jour des immobilisations](fa-how-maintain.md) |
| Mettre à jour les informations d’assurance, valider les coûts d’acquisition vers les polices d’assurance, modifier la couverture assurance, visualiser les statistiques assurance et répertorier les polices d’assurance. | [Assurer les immobilisations](fa-how-insure.md) |
| Reclasser les immobilisations, les transférer vers d’autres emplacements, et les diviser ou les combiner. | [Transfert, fractionnement ou regroupement des immobilisations](fa-how-trans-split-combine.md) |
| Ajuster la valeur des immobilisations, valider les réévaluations et les transactions de dépréciation. | [Réévaluation des immobilisations](fa-how-revalue.md) |
| Calculer et valider l’amortissement, et analyser l’amortissement dans les états sur les immobilisations. | [Amortissement des immobilisations](fa-how-depreciate-amortize.md) |
| Valider les transactions de cession, visualiser les écritures comptables cession et valider les cessions partielles. | [Céder ou annuler des immobilisations](fa-how-dispose-retire.md) |
| Gérer les budgets d’immobilisations, budgéter les coûts d’acquisition, les cessions d’immobilisations et l’amortissement. | [Gestion des budgets pour les immobilisations](fa-how-manage-budgets.md) |
| Configurer des utilisateurs du flux de travail approbation, spécifier comment les utilisateurs sont notifiés et créer des flux de travail. Pour de nouveaux flux de travail pour des scénarios non pris en charge, implémentez les éléments requis du flux de travail en personnalisant le code d’application. | [Configuration des flux de travail d’approbation](across-set-up-workflows.md) |
| Activer les flux de travail approbation, agir sur les notifications de flux de travail (par exemple, en demandant et en approuvant une étape de flux de travail), et archiver et supprimer des flux de travail. | [Utilisation des flux de travail approbation](across-use-workflows.md) |
| Afficher les montants réels comparés aux montants budgétés pour tous les comptes et pour plusieurs périodes. | [Analyser les montants réalisés et les montants budgétés](bi-how-analyze-actual-versus-budget.md) |
| Créer de nouveaux états financiers pour définir les déclarations financières aux fins de reporting ou pour les afficher comme graphiques. | [Préparer des états financiers avec des données financières et des catégories de compte](bi-how-work-account-schedule.md) |
| Analyser vos performances financières en définissant des KPI (Indicateurs de performances clés) basés sur les états financiers, et publier les KPI en tant que services Web. Les KPI des états financiers publiés peuvent être affichés sur un site Web ou être importés dans Excel à l’aide des services Web OData. | [Configuration et publication des services web d’indicateur de performance clé sur la base d’états financiers](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Configurer des vues pour analyser des données à l’aide d’axes. | [Analyse des données par axe analytique](bi-how-analyze-data-dimension.md) |
| Créer de nouveaux rapports d’analyse pour les ventes, les achats et le stock, et configurer des modèles d’analyse. | [Créer des rapports d’analyse](bi-how-create-analysis-views-reports.md) |
| Activer la génération d’états financiers généraux par des organisations comptables internationales à l’aide de la norme eXtensible Business Reporting Language (XBRL). | [Création d’états avec XBRL](bi-create-reports-with-xbrl.md) |
| Modifier l’accès intentionnel à la base de données sur les états, les pages du type API et les requêtes pour réduire la charge et améliorer les performances. | [Gestion de l’intention d’accès à la base de données](admin-data-access-intent.md) |

## <a name="see-also" />Voir aussi

[Configuration de Finance](finance-setup-finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Clôture des périodes fiscales](year-close-years-periods.md)  
[Gestion des projets](projects-manage-projects.md)  
[Importation des données à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
