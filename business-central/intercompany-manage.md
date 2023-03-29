---
title: Gestion des transactions intersociétés
description: 'Avec la fonctionnalité intersociétés, vous pouvez simplifier les processus et les transactions entre sociétés appartenant à la même organisation.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: 605
ms.date: 08/11/2021
ms.author: edupont
---
# Gestion des transactions intersociétés

Les fonctionnalités de transactions intersociétés sont conçues pour les utilisateurs qui contrôlent plusieurs entités juridiques et ont mis en place plusieurs sociétés afin de séparer les fonctions comptables de chacune d’elles. Cette description large s’applique à de nombreux utilisateurs, en particulier ceux qui opèrent sur des marchés internationaux ou dans des zones incluant des cultures commerciales et des environnements environnementaux très disparates.

Votre organisation peut comprendre plusieurs sociétés mais pourrait ne pas disposer du nombre équivalent d’équipes comptables et administratives. Les transactions intersociétés vous permettent de simplifier et de rationaliser les processus et les transactions commerciaux entre toutes ces entités.

Après avoir commencé à utiliser les transactions intersociétés, le fait de commercer avec vos filiales partenaires internes devient aussi simple que de traiter avec des fournisseurs et des clients externes. Vous n’entrez les informations de transaction intersociétés qu’une seule fois dans les documents appropriés. Vous pouvez continuer à utiliser les fonctionnalités que vous connaissez bien, telles que la gestion des clients et des fournisseurs. Les fonctionnalités de mappage pour le plan comptable et les dimensions permettent de veiller à ce que les informations apparaissent aux bons endroits.  

La fonctionnalité Intersociétés offre quatre grands avantages :  

- Productivité accrue résultant du gain de temps et de la simplification des transactions  
- Possibilité d’erreur réduite grâce à une saisie unique d’informations et de mises à jour automatisées à l’échelle du système  
- Piste d’audit et visibilité complètes des activités commerciales et des historiques de transactions  
- Transactions efficaces, rentables avec des filiales ou des succursales  

## Rationalisation du flux des activités commerciales  

Les transactions intersociétés vous permettent de distribuer des documents vente et achat, ainsi que des écritures comptables à l’ensemble de vos bureaux satellites, représentations commerciales ou succursales depuis le programme. Cela vous permet de bénéficier d’un gain de temps et d’une efficacité accrue dans l’ensemble de votre organisation, dans la mesure où vous éliminez les activités redondantes liées à la saisie de données, ainsi qu’à l’envoi, la réception, l’impression et l’archivage des documents vente et achat sur papier.  

Vous contrôlez totalement tous les documents de transaction. Par exemple, vous pouvez rejeter un document qui vous a été envoyé et, de cette manière, inverser des validations feuille et annuler les réceptions/envois incorrects. Ou bien, lorsque vous faites un achat à une société partenaire ou une filiale, vous pouvez mettre à jour la commande achat tant que la société vendeuse n’a pas expédié de biens.  

Lorsque vous entrez une transaction, vous ne devez pas spécifier les comptes pour un ensemble de lois particulier, mais simplement fournir l’identification de la société concernée. La fonctionnalité intersociétés crée des lignes feuilles comptabilité qui entraînent un équilibrage des lois des deux sociétés impliquées dans une transaction. Dans Clients et fournisseurs, vous affectez un code partenaire intersociétés à tout client ou fournisseur. À partir de ce moment, l’ensemble des commandes et des factures générées en relation avec des transactions avec ces sociétés produisent des documents correspondants dans la société partenaire, ce qui aboutit à un équilibrage correct des comptes.  

La fonctionnalité de transactions intersociétés est concentrée sur la prise en charge de transactions intersociétés impliquant des documents vente et achat et des lignes feuille comptabilité. Dans ce domaine, la fonctionnalité de transactions intersociétés permet l’exécution de transactions intersociétés entre plusieurs bases de données [!INCLUDE [prod_short](includes/prod_short.md)], par exemple, dans différents pays/régions, ainsi que l’utilisation de plusieurs devises, plans comptables, dimensions et numérotations d’articles.  

La fonctionnalité de transactions intersociétés utilise plusieurs écritures et documents pour les transactions intersociétés :  

- Écritures comptables
- Commandes achat et vente
- Factures achat et vente
- Avoirs
- Retours

Lorsque vous configurez les transactions intersociétés, vous créez une liste de partenaires intersociétés, appelés partenaires IC, ainsi qu’un plan comptable intersociété. En procédant de cette manière, vous pouvez effectuer des transactions feuille comptabilité intersociété. Vous configurez des dimensions (si nécessaire) séparément.  

> [!NOTE]
> La feuille comptabilité proprement dite n’inclut pas de fonctionnalité de devise mais convertit tous les montants conformément au taux applicable à la devise locale.

Après avoir paramétré vos partenaires commerciaux comme clients et fournisseurs dans le système et leur avoir affecté des codes partenaire intersociété, vous pouvez échanger des documents achat et vente intersociété, notamment des articles et des frais annexes. [!INCLUDE [prod_short](includes/prod_short.md)] permet l’exécution de transactions intersociétés entre plusieurs bases de données ; par exemple, dans différents pays/régions, ainsi que l’utilisation de plusieurs devises, plans comptables, dimensions et numérotations d’articles.  

> [!NOTE]
> Tous les types de données ne peuvent pas être échangés entre les entreprises de cette manière. Les factures achat ne sont pas soumises aux partenaires commerciaux via des processus intersociétés. Mais les factures vente soumises via des processus intersociétés seront créées en tant que factures achat dans la société destinataire.

La consolidation des données financières peut être particulièrement appropriée pour les processus intersociétés. Pour plus d’informations, voir [Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les articles qui les décrivent.

|À |Voir|
|---|---|
|Créez vos fournisseurs et vos clients intersociétés en tant que partenaires intersociétés, et configurez un plan comptable intersociétés.|[Configuration des fonctionnalités intersociétés](intercompany-how-setup.md)|
|Utilisez les documents ou les feuilles intersociétés pour valider les transactions effectuées avec vos partenaires intersociétés.|[Utiliser les documents et les feuilles intersociétés](intercompany-how-work-documents-journals.md)|
|Organisez et traitez les transactions entrantes et sortantes que vous échangez avec vos partenaires intersociétés.|[Gérer la boîte de réception et la boîte d’envoi intersociétés](intercompany-how-manage-intercompany-inbox.md)|
|Utilisez les transactions intersociétés pour répartir les coûts entre les sociétés partenaires.|[Allouer les coûts aux partenaires intersociétés](intercompany-allocate-costs.md)|

## Voir aussi

[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
