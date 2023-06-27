---
title: Familiarisation avec les écritures comptables et les COA
description: 'Décrit la comptabilité, le plan comptable, et les catégories de compte. Utilisez la page Paramètres comptabilité pour préciser la gestion des problèmes comptables dans votre société.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts" />Comprendre la comptabilité et le plan comptable

La comptabilité (comptes généraux) stocke vos données financières, et le plan comptable (COA) affiche les comptes sur lesquels toutes les écritures comptables sont validées. [!INCLUDE[prod_short](includes/prod_short.md)] inclut un plan comptable standard prêt à prendre en charge votre société.

## <a name="general-ledger-setup-and-general-posting-setup" />Paramètres comptabilité et paramètres comptabilisation

La configuration des écritures comptables est le composant principal des processus financiers car elle définit comment vous validez les données. Deux pages jouent un rôle particulièrement important dans la configuration de vos processus financiers :  

* La page **Paramètres comptabilité**

  Sur la page **Paramètres comptabilité**, vous spécifiez comment gérer certains problèmes comptables dans votre société, par exemple :  

  * Les détails arrondi facture  
  * Les formats d’adresse  
  * Les états financiers

  > [!TIP]
  > La page **Paramètres comptabilité** comprend des champs génériques et des champs spécifiques à votre pays ou région. Si vous n’êtes pas sûr de la signification d’un champ, nous vous suggérons de travailler avec votre comptable pour déterminer s’il est pertinent pour votre organisation. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Ouvrez la page [ici](https://businesscentral.dynamics.com/?page=118).
  
* La page **Paramètres comptabilisation**

  De même, sur la page **Paramètres comptabilisation**, vous spécifiez comment vous souhaitez configurer les combinaisons de groupes généraux comptabilisation marché et de groupes généraux comptabilisation produit. Les groupes comptabilisation mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux. Saisissez une ligne pour chaque combinaison de groupes comptabilisation marché et de groupes comptabilisation produit. Mais vous pouvez également ouvrir chaque ligne dans sa propre fiche paramètres comptabilisation. Pour plus d’informations, consultez [Configurer les groupes comptabilisation](finance-posting-groups.md).  

  > [!TIP]
  > Si vous ne pouvez pas voir les champs que vous recherchez sur la page **Paramètres comptabilisation**, utilisez la barre de défilement horizontale au bas de la page pour faire défiler l’affichage vers la droite.  

  Ouvrez la page [ici](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts" />Le plan comptable

Le plan comptable affiche tous les comptes généraux. Vous pouvez effectuer les opérations suivantes à partir du plan comptable :  

* Afficher les états qui affichent les écritures comptables et les soldes.  
* Clôturer votre exercice comptable.  
* Ouvrir la fiche compte général pour ajouter ou modifier des paramètres.  
* Consulter la liste des groupes comptabilisation pour ce compte.
* Afficher les soldes débit et crédit d’un seul compte.

Vous pouvez ajouter, modifier ou supprimer des comptes généraux. Toutefois, pour éviter les différences, vous ne pouvez pas supprimer un compte général si ses données sont utilisées dans le plan comptable. De plus, à partir de la 2e vague de lancement 2022, vous pouvez également bloquer la suppression accidentelle de comptes pendant les périodes sensibles. Pour plus d’informations, consultez la section [Supprimer des comptes](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories" />Catégories de compte

Vous pouvez personnaliser la structure de vos états financiers en mappant les comptes généraux aux catégories de comptes.  

La page **Catégories de compte général** affiche vos catégories et sous-catégories et les comptes généraux qui leurs sont affectés. Vous pouvez créer des sous-catégories et affecter ces catégories à des comptes existants.  

Vous pouvez créer un groupe des catégories en effectuant une indentation d’autres sous-catégories sous une ligne de la page **Catégories de compte général**. Les groupes de catégorie facilitent l’obtention d’une vue d’ensemble, car chaque groupement affiche un solde final. Par exemple, vous pouvez créer des sous-catégories pour différents types d’actifs, puis créer des groupes des catégories pour différencier les immobilisations des actifs à court terme, par exemple.  

Vous pouvez définir si des types d’états spécifiques doivent inclure les comptes de chaque sous-catégorie. Les catégories de compte vous aident à définir la présentation de vos états financiers.  

### <a name="example" />Exemple :

Par exemple, le solde relevé par défaut solde est doté d’une sous-catégorie pour la *trésorerie* dans *Actifs à court terme*. Si vous souhaitez que le solde relevé tienne compte du fonds de caisse et du compte chèque, vous devez procéder comme suit :

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Catégories de compte général**, puis choisissez le lien associé.
   1. Sinon, ouvrez la page [ici](https://businesscentral.dynamics.com/?page=790).
2. Choisissez l’action **Modifier la liste**.
3. Ajoutez deux nouvelles sous-catégories : une pour le fonds de caisse, et l’autre pour le compte chèque.
   1. Sélectionnez la catégorie **Actifs à court terme**.
   2. Sélectionnez l’action **Nouveau**.
   3. Entrez le nom de la sous-catégorie dans le champ **Description**.
   4. Dans le champ **Comptes généraux dans une catégorie**, sélectionnez le compte général approprié.
   5. Dans le champ **Définition d’état supplémentaire**, sélectionnez l’option **Comptes de trésorerie**.
4. Effectuer une indentation sous la sous-catégorie **Trésorerie**.
   1. Sélectionnez la sous-catégorie créée à l’étape 3.
   2. Sélectionnez l’action **Indenter**.
   3. Choisissez l’action **Déplacer vers le bas**.
   4. Sélectionnez l’action **Indenter** pour définir une indentation sous la sous-catégorie **Trésorerie**.

Lorsque vous sélectionnez l’action **Générer des états financiers** (ou la prochaine fois que le rapport sera généré), votre relevé de solde affichera les lignes suivantes :

* Solde total en espèces.
* Lignes avec soldes pour le fonds de caisse et le compte courant.  

> [!NOTE]
> Si vous créez un compte général sans affecter de catégorie de compte, lorsque vous affectez le compte à un groupe comptabilisation [!INCLUDE[prod_short](includes/prod_short.md)] attribue automatiquement la catégorie de compte du compte général immédiatement au-dessus du compte dans votre plan comptable. Cependant, pour inclure le nouveau compte dans vos états financiers, vous devez choisir l’action **Générer des états financiers** sur la page **Catégories de compte général**. Vous pouvez également ouvrir la page Fiche de compte G/L, spécifier la catégorie de compte, puis régénérer votre état financier.

## <a name="get-a-quick-overview" />Obtenir un aperçu rapide

La page **Plan comptable** affiche les comptes dans une liste hiérarchique qui offre un accès rapide aux informations clés pour chaque compte. Cependant, la liste est statique et si vous avez un grand nombre de comptes, vous devrez peut-être défiler pour afficher les différents comptes. Si vous souhaitez simplement un aperçu rapide des éléments de base, tels que les variations nettes et les soldes, la page **Vue d’ensemble du plan comptable** est une alternative utile. La disposition des colonnes sur la page est maintenant la même que celle que vous trouverez sur la page **Plan comptable** (mais avec moins de colonnes), vous n’aurez donc pas à vous réorienter. Vous pouvez développer ou réduire les niveaux hiérarchiques pour condenser la vue. Pour faciliter le passage d’une page à l’autre, la page **Vue d’ensemble du plan comptable** est disponible à partir de la page **Plan comptable**.

## <a name="access-to-create-and-edit-accounts-and-account-categories" />Accès pour créer et modifier des comptes et des catégories de comptes

Dans une petite organisation, comme la société de démonstration CRONUS, la plupart des utilisateurs peuvent modifier le plan comptable, à l’exception des utilisateurs disposant d’une licence MEMBRE D’ÉQUIPE. Cependant, les grandes organisations utilisent généralement des rôles et des autorisations d’utilisation pour limiter l’accès pour modifier le plan comptable. Si vous êtes administrateur ou si vous avez le rôle de *Gestionnaire d’activité* ou de *Comptable*, vous pouvez contrôler les autorisations utilisateur pour vous assurer que les bonnes personnes ont accès aux tables pertinentes. Pour plus d’informations, consultez la section [Pour afficher ou modifier les autorisations d’un utilisateur](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-microsoft-training" />Voir la [formation Microsoft](/training/modules/business-central-configure-general-ledger-setup/) associée

## <a name="see-also" />Voir aussi

[Configurer ou modifier le plan comptable](finance-setup-chart-accounts.md)  
[Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md)  
[Veille économique](bi.md)  
[Finances](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
