---
title: Transactions entre sociétés de la même organisation | Microsoft Docs
description: Avec la fonctionnalité intersociétés, vous pouvez simplifier les processus et les transactions entre sociétés appartenant à la même organisation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 44f6fa0f4f5b957a3164fb8cda68c0397f639bc1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750120"
---
# <a name="managing-intercompany-transactions"></a>Gestion des transactions intersociétés
Votre organisation peut comprendre plusieurs sociétés mais pourrait ne pas disposer du nombre équivalent d’équipes comptables et administratives. La fonctionnalité Intersociétés vous permet de commercer avec vos filiales et vos organisations partenaires internes de la même manière qu’avec vos fournisseurs et vos clients externes. Vous n’entrez les informations de transaction intersociétés qu’une seule fois dans les documents appropriés. Vous pouvez continuer à utiliser les fonctionnalités que vous connaissez bien, telles que la gestion des clients et des fournisseurs. Les fonctionnalités de mappage pour le plan comptable et les dimensions permettent de veiller à ce que les informations apparaissent aux bons endroits.  

La fonctionnalité Intersociétés offre quatre grands avantages :  

- Productivité accrue résultant du gain de temps et de la simplification des transactions  
- Possibilité d’erreur réduite grâce à une saisie unique d’informations et de mises à jour automatisées à l’échelle du système  
- Piste d’audit et visibilité complètes des activités commerciales et des historiques de transactions  
- Transactions efficaces, rentables avec des filiales ou des succursales  

Vous contrôlez totalement tous les documents de transaction. Par exemple, vous pouvez rejeter un document qui vous a été envoyé et, de cette manière, inverser des validations feuille et annuler les réceptions/envois incorrects. Ou bien, lorsque vous faites un achat à une société partenaire ou une filiale, vous pouvez mettre à jour la commande achat tant que la société vendeuse n’a pas expédié de biens.  

Lorsque vous entrez une transaction, vous ne devez pas spécifier les comptes pour un ensemble de lois particulier, mais simplement fournir l’identification de la société concernée. La fonctionnalité Intersociétés crée des lignes feuilles comptabilité qui entraînent un équilibrage des lois des deux sociétés impliquées dans une transaction. Dans Clients et fournisseurs, vous affectez un code partenaire intersociétés à tout client ou fournisseur. À partir de ce moment, l’ensemble des commandes et des factures générées en relation avec des transactions avec ces sociétés produisent des documents correspondants dans la société partenaire, ce qui aboutit à un équilibrage correct des comptes.  

 Après avoir paramétré vos partenaires commerciaux comme clients et fournisseurs dans le système et leur avoir affecté des codes partenaire intersociété, vous pouvez échanger des documents achat et vente intersociété, notamment des articles et des frais annexes. La fonctionnalité Intersociétés permet l’exécution de transactions intersociétés entre plusieurs bases de données ; par exemple, dans différents pays/régions, ainsi que l’utilisation de plusieurs devises, plans comptables, dimensions et numérotations d’articles.  

La consolidation des données financières peut être particulièrement appropriée en association avec des processus intersociétés. Pour plus d’informations, voir [Consolidation des données financières de plusieurs sociétés](finance-consolidated-company-reporting.md).

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

|À |Voir|
|---|---|
|Créez vos fournisseurs et vos clients intersociétés en tant que partenaires intersociétés, et configurez un plan comptable intersociétés.|[Configuration des fonctionnalités intersociétés](intercompany-how-setup.md)|
|Utilisez les documents ou les feuilles intersociétés pour valider les transactions effectuées avec vos partenaires intersociétés.|[Utiliser les documents et les feuilles intersociétés](intercompany-how-work-documents-journals.md)|
|Organisez et traitez les transactions entrantes et sortantes que vous échangez avec vos partenaires intersociétés.|[Gérer la boîte de réception et la boîte d’envoi intersociétés](intercompany-how-manage-intercompany-inbox.md)|
|Utilisez les écritures intersociétés pour répartir les coûts entre les sociétés partenaires.|[Allouer les coûts aux partenaires intersociétés](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]