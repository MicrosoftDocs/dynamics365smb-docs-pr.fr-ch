---
title: Familiarisation avec les écritures comptables et les COA
description: Décrit les écritures comptables, le plan comptable, et les catégories de compte. Utilisez la page Paramètres comptabilité pour préciser la gestion des problèmes comptables dans votre société.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 8590571283ae810d442d514e6968c1feb9865cd8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/30/2021
ms.locfileid: "6321129"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Familiarisation avec les écritures comptables et les COA

Les écritures comptables stockent vos données financières, et le plan comptable affiche les comptes sur lesquels toutes les écritures comptables sont validées. [!INCLUDE[prod_short](includes/prod_short.md)] inclut un plan comptable standard prêt à prendre en charge votre société.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Configuration des écritures comptable et configuration de la comptabilisation

La configuration des écritures comptables est le composant principal des processus financiers car elle définit comment vous validez les données.  

Sur la page **Paramètres comptabilité**, vous spécifiez comment gérer certains problèmes comptables dans votre société, par exemple :  

* Les détails arrondi facture  
* Les formats d’adresse  
* Les états financiers  

De même, sur la page **Paramètres comptabilisation**, vous spécifiez comment vous souhaitez configurer les combinaisons de groupes généraux comptabilisation marché et de groupes généraux comptabilisation produit. Les groupes comptabilisation mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux. Saisissez une ligne pour chaque combinaison de groupes comptabilisation marché et de groupes comptabilisation produit. Pour plus d’informations, voir [Paramètres du groupe comptabilisation](finance-posting-groups.md).  

> [!TIP]
> La page **Paramètres comptabilité** comprend des champs génériques et des champs spécifiques à votre pays ou région. Si vous n’êtes pas sûr de la signification d’un champ, nous vous suggérons de travailler avec votre comptable pour déterminer s’il est pertinent pour votre organisation.  

## <a name="the-chart-of-accounts"></a>Le plan comptable

Le plan comptable affiche tous les comptes généraux. Vous pouvez effectuer les opérations suivantes à partir du plan comptable :  

* Afficher les états qui affichent les écritures comptables et les soldes.  
* Clôturer votre exercice comptable.  
* Ouvrir la fiche compte général pour ajouter ou modifier des paramètres.  
* Consulter la liste des groupes comptabilisation qui effectuent les validations vers ce compte.
* Afficher les soldes débit et crédit d’un seul compte  

Vous pouvez ajouter, modifier ou supprimer des comptes généraux. Toutefois, pour éviter les différences, vous ne pouvez pas supprimer un compte général si ses données sont utilisées dans le plan comptable.  

## <a name="account-categories"></a>Catégories de compte

Vous pouvez personnaliser la structure de vos états financiers en mappant les comptes généraux aux catégories de comptes.  

La page **Catégories de compte général** affiche vos catégories et sous-catégories et les comptes généraux que leurs sont affectés. Vous pouvez créer des sous-catégories et affecter ces catégories à des comptes existants.  

Vous créez un groupe des catégories en effectuant une indentation d’autres sous-catégories sous une ligne de la page **Catégories de compte général**. Cela vous facilite l’obtention d’une vue d’ensemble, car chaque groupement affiche un solde final. Par exemple, vous pouvez créer des sous-catégories pour différents types d’actifs puis créer des groupes des catégories pour différencier les immobilisations des actifs à court terme, par exemple.  

Vous pouvez spécifier si les comptes de chaque sous-catégorie doivent être inclus dans des types spécifiques d’états. Les catégories de compte vous aident à définir la présentation de vos états financiers.  

### <a name="example"></a>Exemple :

Par exemple, le solde relevé par défaut solde est doté d’une sous-catégorie pour la *trésorerie* dans *Actifs à court terme*. Vous souhaitez que le solde relevé tienne compte du fonds de caisse et du compte chèque, vous pouvez donc procéder comme suit :  

1. Ajouter deux nouvelles sous-catégories. :

    * Une pour le fonds de caisse  
    * Une pour votre compte courant  
2. Spécifier la définition d’état supplémentaire **Comptes de trésorerie** pour ces sous-catégories.  
3. Effectuer une indentation sous la sous-catégorie **Trésorerie**.  

À la prochaine génération des tableaux d’analyse, votre relevé solde suivant affichera un solde final pour la trésorerie et deux lignes avec les soldes pour le fonds de caisse et le compte chèque.  

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Accès pour créer et modifier des comptes et des catégories de comptes

Dans une petite organisation, comme la société de démonstration CRONUS, la plupart des utilisateurs peuvent modifier le plan comptable, à l’exception des utilisateurs disposant d’une licence MEMBRE D’ÉQUIPE. Cependant, dans les grandes organisations, l’accès pour modifier le plan comptable est limité selon les rôles et les autorisations. Si vous êtes administrateur ou si vous avez le rôle de *Chef d’entreprise* ou de *Comptable*, vous pouvez vérifier les autorisations de tous les utilisateurs pour vous assurer que les bonnes personnes ont accès aux tables pertinentes. Pour plus d’informations, voir [Pour afficher ou modifier les autorisations d’un utilisateur](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Configuration ou modification du plan comptable](finance-setup-chart-accounts.md)  
[Veille économique](bi.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]