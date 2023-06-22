---
title: Configuration de groupe comptabilisation
description: Aperçu des groupes comptabilisation que vous pouvez utiliser pour gagner du temps et éviter les erreurs lorsque vous validez des transactions.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 08/26/2022
ms.author: bholtorf
---
# <a name="set-up-posting-groups" />Configuration des groupes comptabilisation

Les groupes comptabilisation mappent des entités à des comptes généraux. Les clients, les fournisseurs, les articles, les ressources et les documents vente et achat sont des exemples d’entités. Les groupes comptabilisation vous font gagner du temps et permettent d’éviter des erreurs lorsque vous validez des transactions. Les valeurs de transaction vont dans les comptes spécifiés dans le groupe comptabilisation pour cette entité particulière. Il vous suffit seulement d’avoir un plan comptable. Pour plus d’informations, reportez-vous à [Configuration du plan comptable](finance-setup-chart-accounts.md).  

Les groupes comptabilisation sont traités dans trois catégories :  

* Général

  Définit à qui vous vendez et à qui vous achetez, et ce que vous vendez et ce que vous achetez. Vous pouvez aussi combiner des groupes pour spécifier des éléments comme les comptes résultats dans lesquels valider ou utiliser des groupes pour filtrer les états.  
* Spécifique

  Permet d’utiliser des documents vente au lieu de valider directement dans le module Comptabilité. Lors de la création d’écritures comptables client, les écritures correspondantes sont passées en comptabilité.  
* Taxes

  Définit les pourcentages de taxes et les types de calcul qui s’appliquent à l’acheteur et au vendeur, et à ce que vous vendez et ce que vous achetez.

Les sections suivantes décrivent les groupes comptabilisation dans chaque catégorie.  

## <a name="general-posting-groups" />Groupes comptabilisation généraux

Le tableau suivant décrit les groupes comptabilisation généraux.

| Type | Description |
| --- | --- |
| Groupes comptabilisation marché |Affectez ce groupe aux clients et aux fournisseurs pour spécifier à qui vous vendez, et à qui vous achetez. Définissez ces groupes comptabilisation sur la page **Groupes compta. marché**. Lorsque vous effectuez cette opération, vous devez prendre en compte le nombre de groupes nécessaires pour répartir les ventes et les achats. Par exemple, les groupes clients et fournisseurs peuvent être répartis par zone géographique ou par type d’activité. |
| Groupes comptabilisation produit |Affectez ce groupe à des articles et des ressources pour spécifier les éléments que vous vendez, et que vous achetez. Définissez ces groupes comptabilisation sur la page **Groupes compta. produit**. Lorsque vous effectuez cette opération, vous devez considérer le nombre de groupes nécessaires pour répartir les ventes par article et ressource, et pour répartir les achats par article. Par exemple, divisez ces groupes par Matières premières, Vte détail, Ressources, Capacités, etc. |
| Paramètres comptabilisation |Combinez les groupes comptabilisation marché et produit, puis choisissez les comptes à valider. Pour chaque combinaison de groupes comptabilisation marché et produit, vous pouvez affecter un ensemble de comptes généraux. Par exemple, vous pouvez valider la vente d’un même article dans différents comptes généraux car les clients sont affectés à différents groupes comptabilisation marché. Définissez ces configurations sur la page **Paramètres comptabilisation**. |

## <a name="specific-posting-groups" />Groupes comptabilisation spécifiques

Le tableau suivant décrit les groupes comptabilisation spécifiques aux types de données.

|Type | Description |
| --- | --- |
| Groupes compta. client |Définissez les comptes à utiliser lorsque vous validez des transactions Comptabilité client. Si vous utilisez un stock conjointement avec des clients, les comptes dans lesquels les écritures lignes commande vente sont validées sont déterminés par le groupe comptabilisation marché affecté au client et le groupe comptabilisation produit affecté à l’article en stock. Voir *Groupes comptabilisation marché* et *Groupes comptabilisation produit* dans la section [Groupes comptabilisation généraux](#general-posting-groups) . Définissez ces groupes comptabilisation sur la page **Groupes compta. client**. |
| Groupes compta. fournisseur |Définissez où valider les transactions des comptes fournisseur, des comptes frais forfaitaires, et des comptes d’escompte. Cela est similaire aux groupes comptabilisation client. Définissez ces groupes comptabilisation sur la page **Groupes compta. fournisseur**. |
| Groupes compta. stock |Définissez des groupes comptabilisation stock que vous devez ensuite affecter aux comptes articles appropriés sur la page **Paramètres compta. stock**. Ainsi, lorsque vous validez des écritures article, le système effectue la validation sur le compte général qui est configuré pour la combinaison groupe comptabilisation stock/magasin liée à l’article. Des groupes comptabilisation stock offrent également un moyen idéal d’organiser vos stocks. Ainsi, vous pouvez séparer des articles par groupe comptabilisation lors de la génération d’états. Définissez ces groupes comptabilisation sur la page **Groupes compta. stock**. |
| Groupes compta. banque |Définissez les comptes généraux dans lesquels les écritures compte bancaire sont validées. Par exemple, cela peut simplifier les processus de traçabilité des transactions et des rapprochements bancaires. Définissez ces groupes comptabilisation sur la page **Groupes compta. banque**. Nous recommandons que le champ **Imputation directe** de ces comptes généraux soient définis sur *Non*. |
| Groupes comptabilisation immobilisations |Définissez des comptes pour les différents types de dépenses et frais, tels que les coûts d’acquisition, les montants d’amortissement cumulés, les coûts d’acquisition sur cession, l’amortissement cumulé sur cession, les gains sur cession, les pertes sur cession, les frais de maintenance et les frais d’amortissement. Définissez ces groupes comptabilisation sur la page **Groupes compta. immo.**. |

### <a name="allowing-substitute-customer-or-vendor-posting-groups-on-documents" />Autorisation de groupes comptabilisation client ou fournisseur de remplacement sur les documents

[!INCLUDE [preview](includes/preview.md)]

Vous pouvez permettre aux utilisateurs de choisir des groupes de validation client et fournisseur différents de ceux par défaut lorsqu’ils utilisent des documents et des feuilles vente ou achat.

Pour autoriser les modifications des groupes comptabilisation client, choisissez **Autoriser plusieurs groupes comptabilisation** sur les pages **Paramètres ventes** et **Paramètres Gestion des services**, et sur la page **Paramètres achats** page pour les modifications des groupes comptabilisation fournisseur.

Sur les pages **Groupes compta. client** ou **Groupes compta. fournisseur**, vous pouvez spécifier les groupes de validation à autoriser comme substituts en choisissant **Articles de substitution**. Les groupes de comptabilisation de substitution peuvent remplacer les groupes comptabilisation client ou fournisseur par défaut spécifié pour un client ou un fournisseur.

Après avoir configuré cela, vous pouvez choisir parmi les groupes de comptabilisation de substitution autorisés et modifier le groupe de comptabilisation client ou fournisseur lors de la validation des documents et des feuilles vente ou achat. Les groupes de comptabilisation client ou fournisseur de substitution sont copiés dans les documents et feuilles validés, et les écritures comptables à recevoir ou à payer sont validées dans les comptes généraux spécifiés pour les substituts.

Lors de l’application, par exemple, d’une facture et d’un paiement qui sont validés avec différents groupes de validation client ou fournisseur (différents comptes généraux), [!INCLUDE[prod_short](includes/prod_short.md)] transfère les montants entre les comptes généraux pour les équilibrer.

## <a name="tax-posting-groups" />Groupes comptabilisation TVA

Le tableau suivant décrit les groupes comptabilisation associés aux taxes.

| Type | Description |
| --- | --- |
| Groupes compta. marché TVA |Déterminez la manière de calculer et de valider la taxe de vente pour les clients et les fournisseurs. Définissez ces groupes comptabilisation sur la page **Groupes compta. marché TVA**. Lorsque vous le faites, pensez au nombre de groupes dont vous avez besoin. De nombreux facteurs peuvent entrer en jeu, notamment la législation locale, et le fait de travailler sur le marché national et international. |
| Groupes compta. produit TVA |Indiquez les calculs TVA nécessaires pour les types d’articles ou de ressources que vous achetez ou vendez. |
| Paramètres compta. TVA |Combinez des groupes compta. marché et des groupes compta. produit TVA. Lorsque vous renseignez une ligne dans une feuille comptabilité, une ligne achat, ou une ligne vente, nous allons consulter la combinaison pour identifier les comptes à utiliser. |

Si votre pays utilise la taxe sur la valeur ajoutée (TVA), voir [Configurer des méthodes de calcul et de validation de la taxe sur la valeur ajoutée](finance-setup-vat.md).  

## <a name="example-of-linking-posting-groups" />Exemple de liaison de groupes comptabilisation

Voici un scénario.  

Ces groupes comptabilisation sont choisis dans la fiche client :  

* Groupe comptabilisation marché
* Groupe compta. client  

Ces groupes comptabilisation sont choisis dans la fiche article :  

* Groupe comptabilisation produit  
* Groupe comptabilisation stock  

Lors de la création d’un document vente, l’en-tête vente utilise les informations de la fiche client et les lignes ventes utilisent les informations de la fiche article.  

* La validation revenus (résultats) est déterminée par la combinaison du groupe comptabilisation marché et du groupe comptabilisation produit.  
* La validation comptabilisation client (bilan) est déterminée par le groupe comptabilisation client.  
* La validation stock (bilan) est déterminée par le groupe comptabilisation stock.  
* La validation coût des biens vendus (comptes résultats) est déterminée par la combinaison du groupe comptabilisation marché et du groupe comptabilisation produit.  

Votre paramétrage détermine quand la validation a lieu. Par exemple, la synchronisation est affectée au moment où vous exécutez des activités périodiques, par exemple : valider coûts ajustés et ajuster coût écritures article.

## <a name="copying-posting-setup-lines" />Copie de lignes paramètres validation

Plus il y a de groupes comptabilisation produit et marché, plus la page **Paramètres comptabilisation** contient de lignes. Cela peut entraîner la nécessité d’entrer un grand nombre de données pour configurer les paramètres comptabilisation pour la société. S’il peut y avoir un grand nombre de combinaisons différentes de groupes comptabilisation marché et produit, différentes combinaisons peuvent encore valider dans les mêmes comptes généraux. Pour limiter le nombre de saisies manuelles, copiez les comptes généraux à partir d’une ligne existante sur la page **Paramètres comptabilisation**.

## <a name="set-up-posting-groups-on-the-go" />Configurer des groupes de comptabilisation en déplacement

Pour que les utilisateurs démarrent plus rapidement, [!INCLUDE[prod_short](includes/prod_short.md)] peut afficher des notifications de comptes généraux manquants dans diverses configurations de groupe de comptabilisation. Pour recevoir ces notifications, assurez-vous que la notification **Compte général manquant dans le groupe comptabilisation ou la configuration** est sélectionnée dans la page **Mes notifications**, à laquelle vous pouvez accéder à partir du champ **Modifier lorsque je reçois des notifications** dans la page **Mes paramètres**.  

De cette façon, lorsque vous travaillez sur un document qui utilise un groupe de comptabilisation ou une configuration pour laquelle il manque un compte général requis, vous recevez une notification. Choisissez le lien dans la notification pour ouvrir une page où vous pouvez apporter les modifications appropriées, à condition que vous y soyez autorisé.  

> [!NOTE]
> Afin de vous diriger directement vers le groupe de comptabilisation ou le paramétrage auquel il manque un compte général, [!INCLUDE[prod_short](includes/prod_short.md)] crée un espace réservé pour une configuration ou un groupe de comptabilisation. Les configurations et les groupes de comptabilisation constituent, pour le comptable, un moyen de contrôler la manière dont les écritures sont validées dans la comptabilité. Ainsi, la création juste à temps de configurations et de groupes de comptabilisation peut ne pas être autorisée dans votre organisation.  
>
> Dans ce cas, désactivez la notification *Compte général manquant dans le groupe comptabilisation ou la configuration*, puis collaborez avec votre comptable pour apporter les modifications appropriées au groupe de comptabilisation, à la configuration ou à votre document. Il s’agit d’une étape importante, car une fois les documents validés, les paramètres ou les groupes de comptabilisation utilisés de manière incorrecte ne peuvent pas être supprimés car des écritures comptables sont créées pour eux.

À partir de la 1re vague de lancement 2022, vous pouvez utiliser le champ **Bloqué** sur la page **Paramètres comptabilisation** pour empêcher les utilisateurs d’utiliser par erreur une configuration qui n’est plus pertinente pour les nouvelles publications.  

## <a name="troubleshooting-posting-group-errors" />Résolution des erreurs de groupe comptabilisation

Les groupes comptabilisation sont l’un des concepts les plus avancés à configurer dans [!INCLUDE[prod_short](includes/prod_short.md)]. S’ils ne sont pas configurés correctement, des erreurs peuvent se produire lors de la validation de documents ou de lignes feuille. Par exemple, ces erreurs sont généralement causées par une erreur d’affectation des comptes de la comptabilité ou de combinaison des groupes comptabilisation.

Quand quelque chose ne va pas, [!INCLUDE[prod_short](includes/prod_short.md)] affiche la page **Messages d’erreur**. La page **Messages d’erreur** peut faciliter l’identification et la résolution du problème. Cette page propose une description de l’erreur qui signale la configuration du groupe comptabilisation qui nécessite une attention particulière. Par exemple, le message peut indiquer « Il manque des Paramètres comptabilisation au compte Acompte vente ». Il existe également un lien pour ouvrir la page qui est à l’origine du problème, afin que vous puissiez le résoudre rapidement.  

> [!NOTE]
> La gestion des erreurs décrite ci-dessus n’est pas disponible sur les feuilles article, ressource, employé et immobilisation, ni pour les comptes de la comptabilité ajoutés dans des versions locales des groupes comptabilisation.

## <a name="see-related-microsoft-trainingtrainingmodulesposting-groups-dynamics--business-central" />Voir la [formation Microsoft](/training/modules/posting-groups-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Comptabilité et plan comptable](finance-general-ledger.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
