---
title: Démarrage rapide de Informations financières
description: Préparez votre entreprise en configurant les informations financières dans Business Central.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a>Démarrage rapide de Informations financières

Après avoir saisi les informations de base sur l’entreprise dans [!INCLUDE[prod_short](includes/prod_short.md)], l’une des prochaines étapes consiste à remplir la section financière. Vous faites cela non seulement pour recevoir ou effectuer des paiements, mais également pour gérer et déclarer correctement les numéros de votre entreprise.

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Le plan comptable

Le plan comptable (COA) offre un aperçu des finances de l’entreprise, répertoriant les comptes dans des groupes structurés tels que les actifs, les passifs, les revenus, le coût des marchandises vendues et les dépenses. [!INCLUDE[prod_short](includes/prod_short.md)] inclut un plan comptable standard que vous pouvez personnaliser selon les pratiques comptables de votre société.

## <a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a>Configurer le plan comptable

La vidéo suivante vous montre comment configurer le plan comptable dans [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a>Ajouter un compte au plan comptable

Pour ajouter un compte non inclus par défaut dans [!INCLUDE[prod_short](includes/prod_short.md)] —par exemple, les services de jardinage—suivez simplement ces étapes :

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.
2. Sélectionnez l’option **Nouveau** pour ouvrir la page **Fiche compte général**.
3. Dans le raccourci **Général**, renseignez les champs comme indiqué dans le tableau ci-dessous. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Champ | Données |
   | --- | --- |
   | **N°** | 61250 |
   | **Nom** | Services de jardinage |
   | **Gestion/Bilan** | Compte de gestion |
   | **Catégorie de compte** | Frais |
   | **Sous-catégorie du compte** | Dépenses de réparation et d’entretien |
   | **Débit/Crédit** | Les deux |
   | **Type compte** | Valider |

4. Sur le raccourci **Validation**, entrez les données suivantes :

   | Champ | Données |
   | --- | --- |
   | **Type compta. TVA** | Achats |
   | **Groupe comptabilisation marché** | National |
   | **Groupe compta. produit** | Services |

5. Sur la page **Fiche compte général**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a>Obtenir un aperçu du plan comptable

Si vous avez besoin d’une vue plus compacte du plan comptable, sans colonnes pour les groupes de comptabilisation, le type de comptabilisation ou le type de coût, par exemple, la **Vue d’ensemble du plan comptable** répertorie les principales informations pour chaque compte dans un tableau plus petit. De plus, vous pouvez réduire ou développer des groupes pour masquer les comptes qu’ils contiennent.

Pour afficher l’aperçu, choisissez l’option **Vue d’ensemble du plan comptable** sur la page **Plan comptable** ou recherchez la fonctionnalité à l’aide de ![Ampoule qui ouvre la fonction Tell Me 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire").

En savoir plus sur le plan comptable et le grand livre général sur [Comprendre le grand livre et le plan comptable](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a>Configuration des comptes bancaires

Les comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] enregistrent les opérations bancaires et sont associés aux écritures du plan comptable. La vidéo suivante vous montre comment configurer les comptes bancaires.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Sélectionnez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sur la page **Comptes bancaires**, sélectionnez l’action **Nouveau**.
3. Dans le champ **N°**, un identifiant tel que *B010* sera saisi automatiquement s’il existe une liste de séries numérotées pour les comptes bancaires. Sinon, entrez une combinaison unique.

   Le champ est différent du champ **Numéro de compte bancaire** également disponible dans le raccourci **Général**.
4. Sur la page **Fiche compte bancaire**, renseignez les champs comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Configurer le plan comptable](finance-setup-chart-accounts.md)  
[Configurer des comptes bancaires](bank-how-setup-bank-accounts.md)  
[Exécuter et imprimer des états](ui-work-report.md)  
[Démarrage rapide de Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
