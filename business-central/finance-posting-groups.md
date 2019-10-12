---
title: Paramètre du groupe comptabilisation| Microsoft Docs
description: Aperçu des groupes comptabilisation que vous pouvez utiliser pour gagner du temps et éviter les erreurs lorsque vous validez des transactions.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: c10fb70d10370ec105876eada6bcad010eb8b4b3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301891"
---
# <a name="setting-up-posting-groups"></a>Configuration de groupes comptabilisation
Les groupes comptabilisation mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux. Ils vous font gagner du temps et permettent d'éviter des erreurs lorsque vous validez des transactions. Les valeurs de transaction vont dans les comptes spécifiés dans le groupe comptabilisation pour cette entité particulière. Il vous suffit seulement d'avoir un plan comptable. Pour plus d'informations, reportez-vous à [Configuration du plan comptable](finance-setup-chart-accounts.md).  

Les groupes comptabilisation sont traités dans trois catégories :  

* Général - définit à qui vous vendez et à qui vous achetez, et ce que vous vendez et ce que vous achetez. Vous pouvez aussi combiner des groupes pour spécifier des éléments comme les comptes résultats dans lesquels valider ou utiliser des groupes pour filtrer les états.  
* Spécifique - permet d'utiliser des documents vente au lieu de valider directement dans le module Comptabilité. Lors de la création d'écritures comptables client, les écritures correspondantes sont passées en comptabilité.  
* Taxe - définit les pourcentages de taxes et les types de calcul qui s'appliquent à l'acheteur et au vendeur, et à ce que vous vendez et ce que vous achetez.

Les tables suivantes décrivent les groupes comptabilisation dans chaque catégorie.  

| Groupes comptabilisation généraux | Désignation |
| --- | --- |
| Groupes comptabilisation marché |Affectez ce groupe aux clients et aux fournisseurs pour spécifier à qui vous vendez, et à qui vous achetez. Définissez cela sur la page **Groupes compta. marché**. Lorsque vous effectuez cette opération, vous devez prendre en compte le nombre de groupes nécessaires pour répartir les ventes et les achats. Par exemple, les groupes clients et fournisseurs peuvent être répartis par zone géographique ou par type d'activité. |
| Groupes comptabilisation produit |Affectez ce groupe à des articles et des ressources pour spécifier les éléments que vous vendez, et que vous achetez. Définissez cela sur la page **Groupes compta. produit**. Lorsque vous effectuez cette opération, vous devez considérer le nombre de groupes nécessaires pour répartir les ventes par article et ressource, et pour répartir les achats par article. Par exemple, divisez ces groupes par Matières premières, Vte détail, Ressources, Capacités, etc. |
| Paramètres comptabilisation |Combinez les groupes comptabilisation marché et produit, puis choisissez les comptes à valider. Pour chaque combinaison de groupes comptabilisation marché et produit, vous pouvez affecter un ensemble de comptes généraux. Par exemple, vous pouvez valider la vente d'un même article dans différents comptes ventes de la comptabilité car différents groupes comptabilisation marché sont affectés aux clients. Définissez cela sur la page **Paramètres comptabilisation**. |

| Groupes comptabilisation spécifiques | Désignation |
| --- | --- |
| Groupes compta. client |Définissez les comptes à utiliser lorsque vous validez des transactions Comptabilité client. Si vous utilisez un stock conjointement avec des clients, le groupe comptabilisation marché affecté au client et le groupe comptabilisation produit affecté à l'article en stock déterminent les comptes dans lesquels les écritures lignes commande vente valident. Voir « Groupe comptabilisation marché » et « Groupe comptabilisation produit » sous **Groupes comptabilisation généraux** ci-dessus. Définissez cela sur la page **Groupes compta. client**. |
| Groupes compta. fournisseur |Définissez où valider les transactions des comptes fournisseur, des comptes frais forfaitaires, et des comptes d'escompte. Cela est similaire aux groupes comptabilisation client. Définissez cela sur la page **Groupes compta. fournisseur**. |
| Groupes compta. stock |Définissez des groupes comptabilisation stock que vous devez ensuite affecter aux comptes articles appropriés sur la page **Paramètres compta. stock**. Ainsi, lorsque vous validez des écritures article, le système effectue la validation sur le compte général qui est configuré pour la combinaison groupe comptabilisation stock/magasin liée à l'article. Des groupes comptabilisation stock offrent également un moyen idéal d'organiser vos stocks. Ainsi, vous pouvez séparer des articles par groupe comptabilisation lors de la génération d'états. Définissez cela sur la page **Groupes compta. stock**. |
| Groupes compta. banque |Définissez des comptes bancaires. Par exemple, cela peut simplifier les processus de traçabilité des transactions et des rapprochements bancaires. Définissez cela sur la page **Groupes compta. banque**. |
| Groupes comptabilisation immobilisations |Définissez des comptes pour les différents types de dépenses et frais, tels que les coûts d'acquisition, les montants d'amortissement cumulés, les coûts d'acquisition sur cession, l'amortissement cumulé sur cession, les gains sur cession, les pertes sur cession, les frais de maintenance et les frais d'amortissement. Définissez cela sur la page **Groupes compta. immo.** |

| Groupe compta. TVA | Désignation |
| --- | --- |
| Groupes compta. marché TVA |Déterminez la manière de calculer et de valider la taxe de vente pour les clients et les fournisseurs. Définissez cela sur la page **Groupes compta. marché TVA**. Lorsque vous le faites, pensez au nombre de groupes dont vous avez besoin. De nombreux facteurs peuvent entrer en jeu, notamment la législation locale, et le fait de travailler sur le marché national et international. |
| Groupes compta. produit TVA |Indiquez les calculs TVA nécessaires pour les types d'articles ou de ressources que vous achetez ou vendez. |
| Paramètres compta. TVA |Combinez des groupes compta. marché et des groupes compta. produit TVA. Lorsque vous renseignez une ligne dans une feuille comptabilité, une ligne achat, ou une ligne vente, nous allons consulter la combinaison pour identifier les comptes à utiliser. |

## <a name="example-of-linking-posting-groups"></a>Exemple de liaison de groupes comptabilisation
Voici un scénario.  

Ces groupes comptabilisation sont choisis dans la fiche client :  

* Groupe comptabilisation marché
* Groupe compta. client  

Ces groupes comptabilisation sont choisis dans la fiche article :  

* Groupe comptabilisation produit  
* Groupe comptabilisation stock  

Lors de la création d'un document vente, l'en-tête vente utilise les informations de la fiche client et les lignes ventes utilisent les informations de la fiche article.  

* La validation revenus (résultats) est déterminée par la combinaison du groupe comptabilisation marché et du groupe comptabilisation produit.  
* La validation comptabilisation client (bilan) est déterminée par le groupe comptabilisation client.  
* La validation stock (bilan) est déterminée par le groupe comptabilisation stock.  
* La validation coût des biens vendus (comptes résultats) est déterminée par la combinaison du groupe comptabilisation marché et du groupe comptabilisation produit.  

Votre paramétrage détermine quand la validation a lieu. Par exemple, la synchronisation est affectée au moment où vous exécutez des activités périodiques, par exemple : valider coûts ajustés et ajuster coût écritures article.

## <a name="copying-posting-setup-lines"></a>Copie de lignes paramètres validation
Plus il y a de groupes comptabilisation produit et marché, plus la page Paramètres comptabilisation contient de lignes. Cela peut entraîner la nécessité d'entrer un grand nombre de données pour configurer les paramètres comptabilisation pour la société. S'il peut y avoir un grand nombre de combinaisons différentes de groupes comptabilisation marché et produit, différentes combinaisons peuvent encore valider dans les mêmes comptes généraux. Pour limiter le nombre de saisies manuelles, copiez les comptes généraux à partir d'une ligne existante sur la page **Paramètres comptabilisation**.

## <a name="see-also"></a>Voir aussi .
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
