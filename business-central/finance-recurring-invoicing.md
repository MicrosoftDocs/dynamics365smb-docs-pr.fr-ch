---
title: Utiliser des revenus récurrents
description: Découvrez les options disponibles pour automatiser l’envoi de factures d’abonnement à vos clients et enregistrer des revenus récurrents.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: bholtorf
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Utiliser des revenus récurrents dans [!INCLUDE[prod_short](includes/prod_short.md)]

De nombreuses sociétés passent d’un modèle de revenus d’entreprise où les revenus proviennent des achats ponctuels d’un client à un modèle d’abonnement où les revenus sont générés de manière récurrente en échange d’un accès cohérent à la fourniture d’un bien ou d’un service.
[!INCLUDE[prod_short](includes/prod_short.md)] propose les options suivantes pour automatiser l’envoi de factures d’abonnement à vos clients et enregistrer des revenus récurrents. 

## Enregistrer les revenus avec une feuille comptabilité récurrente

Une feuille récurrente est une feuille comptabilité contenant des champs spécifiques pour la gestion des transactions que vous validez souvent avec peu ou pas de modifications comme le loyer, les abonnements, l’électricité ou le chauffage. Utilisez ces champs dans le cadre des transactions récurrentes pour valider les montants fixes et variables. Avec une feuille abonnement, les écritures qui sont régulièrement validées ne sont saisies qu’une fois. Les comptes, axes, sections analytiques, etc., que vous saisissez restent ainsi dans la feuille après validation. Si des ajustements sont nécessaires, vous pouvez les faire à chaque validation.

### Pourquoi utiliser cette option

Avec cette option, vous définissez des périodes de facturation flexibles avec des [Formules de date](ui-enter-date-ranges.md#use-date-formulas).

Cependant, avec cette option, vous ne pouvez pas imprimer ni envoyer de factures dans la version par défaut de [!INCLUDE[prod_short](includes/prod_short.md)].  

Pour plus d’informations, voir [Utiliser des feuilles abonnement](ui-work-general-journals.md#work-with-recurring-journals).  

## Créer plusieurs factures à partir d’une feuille projet récurrente

La feuille projet récurrente est une alternative plus avancée à la feuille comptabilité. Vous définissez les articles, les ressources et les comptes généraux qui doivent être répétés pour chaque projet, et vous spécifiez la fréquence de récurrence.  

Après avoir validé une feuille projet récurrente, vous pouvez créer plusieurs factures avec la tâche **Créer une facture vente projet**. Vous pouvez examiner et valider les factures créées dans la page **Factures vente**.

### Pourquoi utiliser cette option

Avec cette option, vous suivez la procédure de facturation standard avec tous les avantages y afférents, notamment les dispositions standard et client pour les préférences de communication. Vous pouvez également définir des prix pour chaque projet individuellement.

Cependant, pour chaque nouveau client, vous devez créer un nouveau projet et ajouter des lignes à la feuille récurrente. 

Pour plus d’informations, voir [Créer des lignes feuille projet](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) et [Créer plusieurs factures vente projet](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## Créer plusieurs factures à partir de lignes vente récurrentes

Si vous devez souvent créer des lignes vente et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes vente récurrentes que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes. Utilisez le traitement par lots **Créer des factures vente récurrentes** pour créer des factures vente en fonction des lignes vente récurrentes qui sont affectées aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans les lignes vente récurrentes.  

### Pourquoi utiliser cette option

Avec cette option, vous pouvez attribuer les mêmes lignes récurrentes à plusieurs clients. Vous pouvez définir la période de validité des lignes vente récurrentes pour un client spécifique. Vous pouvez attribuer plusieurs lignes récurrentes au même client et toutes seront incluses dans la facture.

Cependant, il n’y a aucun moyen de définir des prix fixes pour les articles, car [!INCLUDE[prod_short](includes/prod_short.md)] utilisera les prix réels et la remise en vigueur à la date du document pour essayer de trouver la meilleure combinaison qui donne le prix le plus bas.  

Pour plus d’informations, voir [Créer des lignes vente et achat récurrentes](sales-how-work-standard-lines.md).

## Factures récurrentes avec contrat de service

Un contrat de service contient les accords relatifs aux contrats de service passés entre vos clients et votre société. Un contrat de service inclut des accords niveau service et des articles de service dont vous effectuez la maintenance dans le cadre du contrat.  

Vous pouvez définir la date de début du contrat, la période de facturation, spécifier si le contrat est prépayé ou non, ainsi que les détails de révision des tarifs si vous prévoyez de modifier les tarifs pendant que le contrat est actif. Vous pouvez utiliser à la fois des articles de service ou des articles des lignes contrat de service.
Vous pouvez créer des modèles contrat pour définir le mode de création de certains types de contrat.  

### Pourquoi utiliser cette option

Avec cette option, vous utilisez une partie de la fonctionnalité de gestion des services avancée qui ne se limite pas à l’émission de factures récurrentes mais prend également en charge les opérations des ateliers de réparation et sur le terrain.

Cependant, cette option nécessite la licence Premium. La configuration de la gestion des services et sa maintenance peuvent ne pas offrir d’énormes avantages dans des scénarios d’abonnement plus simples.  

Pour plus d’informations, voir [Utiliser des contrats de service et des devis contrat de service](service-how-to-create-service-contracts-and-service-contract-quotes.md) et [Facturer plusieurs contrats de service](service-how-create-invoices.md#to-invoice-several-service-contracts).

## Fonctionnalités associées
Il existe plusieurs fonctionnalités associées dans [!INCLUDE[prod_short](includes/prod_short.md)].

### Commandes cadres vente

Une commande cadre vente représente le cadre d’un accord à long terme entre votre société et votre client.
Une commande ouverte est généralement établie quand un client s’est engagé à acheter de grandes quantités à livrer en plusieurs expéditions de plus petite taille au cours d’une période déterminée. Souvent, les commandes ouvertes ne portent que sur un seul article avec des dates de livraison prédéterminées. La principale raison d’utiliser une commande cadre plutôt qu’une commande vente est que les quantités entrées dans une commande cadre n’affectent pas la disponibilité de l’article ; toutefois, elle peut être utilisée à des fins de planification.

#### Pourquoi utiliser cette option

Avec cette option, vous utilisez la demande anticipée, les informations soient donc prises en compte lors des routines de planification normales. Pour plus d’informations, voir [Prévisions de la demande et commandes cadres](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Cependant, la version par défaut n’offre pas la possibilité prédéfinie de traiter plusieurs commandes cadres en bloc.

Pour plus de détails, voir [Utiliser des commandes cadres vente](sales-how-to-create-blanket-sales-orders.md).

### Commandes récurrentes (Norvège)

Vous pouvez utiliser des commandes récurrentes pour créer des modèles de commande cadre afin que les commandes client puissent être créées en fonction d’intervalles de date que vous définissez. Par exemple, si vous livrez la même commande vente toutes les deux semaines, vous pouvez utiliser une commande cadre vente et créer des commandes récurrentes.
Vous pouvez utiliser des groupes récurrents pour définir une plage de paramètres qui montrent comment vous passez les commandes. Ces groupes sont affectés à des commandes cadres qui doivent être créées régulièrement. Pour créer les commandes récurrentes, vous devrez exécuter régulièrement le processus de création de commandes récurrentes. 

#### Pourquoi utiliser cette option

Avec cette option, vous pouvez choisir entre les prix fixes et les « meilleurs » prix.

Toutefois, cette option n’est disponible qu’en Norvège. La période de validité peut être définie au niveau du groupe récurrent.

Pour en savoir plus, voir [Commandes récurrentes](LocalFunctionality/Norway/recurring-orders.md).

### Revenus récurrents et facturation d’abonnement par d’autres fournisseurs

Vous pouvez obtenir des extensions pour Business Central sur le site [AppSource.microsoft.com](https://appsource.microsoft.com/). Certaines extensions sont fournies par Microsoft, et d’autres sont fournies par d’autres sociétés. La liste des extensions par d’autres sociétés évolue chaque mois. Tenez-vous informé sur le site [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) et obtenez des applications pour vous aider à faire votre travail dans Business Central.  

## Voir aussi

[Formules de date](ui-enter-date-ranges.md#use-date-formulas)  
[Utiliser des feuilles abonnement](ui-work-general-journals.md#work-with-recurring-journals)  
[Créer des lignes feuille projet](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Créer plusieurs factures vente projet](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Créer des lignes ventes et achat récurrentes](sales-how-work-standard-lines.md)  
[Utiliser des contrats de service et des devis contrat de service](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Facturer plusieurs contrats de service](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Prévisions de demande et commandes ouvertes](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Utiliser des commandes ouvertes vente](sales-how-to-create-blanket-sales-orders.md)  
[Commandes récurrentes (Norvège)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]