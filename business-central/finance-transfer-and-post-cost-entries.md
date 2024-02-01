---
title: Transfert et validation des écritures de coûts
description: 'Avant de définir des affectations de coûts, vous devez comprendre les différentes sources d’où proviennent les écritures de coûts.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Transfert et validation des écritures de coûts

Avant de définir des affectations de coûts, vous devez comprendre comment les écritures de coûts proviennent des sources suivantes :  

- Transfert automatique des écritures comptables.  
- Validation manuelle de coûts pour les écritures de coûts, les frais internes et les affectations manuelles.  
- Validation automatique de l’affectation de coûts réels.  
- Transfert des écritures budgétées vers les écritures réelles.

## Critères de transfert des écritures comptables vers les écritures de coûts

Il est important de comprendre les critères pour le transfert des écritures comptables aux écritures de coûts. Lors du transfert, le traitement par lots pour **Transférer les écritures comptables vers CA** applique les critères suivants pour déterminer si les écritures comptables sont transférées et comment.  

Les écritures comptables sont transférées si :  

- Les écritures ont des sections analytiques correspondant à un centre de coûts ou à un coût associé.  
- Les écritures ont des sections analytiques correspondant à un centre de coûts et à un coût associé. Pour ces écritures, le centre de coûts est prioritaire. Vous pouvez ainsi éviter qu’un type de coût apparaisse à la fois dans un coût associé et dans un centre de coûts, ce qui le comptabiliserait deux fois dans les statistiques.  
- Le numéro de document dans les écritures est vide. C’est pourquoi, il s’affichera avec le numéro de document 0000 dans les écritures de coûts.  
- Les écritures sont transférées vers un type de coût qui autorise les écritures combinées. Ces écritures sont transférées ainsi sur une base mensuelle ou journalière.  

Les écritures comptables ne sont pas transférées si :  

- Les écritures ont des sections analytiques ne correspondant ni à un centre de coûts ni à un coût associé.  
- Les écritures sont égales à zéro.  
- Les écritures ont un compte général qui a été supprimé.  
- Les écritures ont un compte général qui n’est pas du type **Comptes de gestion**.  
- Les écritures ont un compte général sans type de coût affecté.  
- La date de validation des écritures est antérieure à **Date début pour transfert comptabilité**.  
- Les écritures ont été validées avec une date de clôture. Il s’agit généralement des écritures qui redéfinissent le solde des comptes de gestion sur la fin de l’exercice.

## Transfert des écritures comptables vers les écritures de coûts

Vous pouvez transférer les écritures comptables aux écritures de coûts.  

Avant d’exécuter le transfert des écritures comptables vers des écritures de coûts, vous devez vous y préparer pour éviter toute validation manuelle de correction.  

### Pour préparer le transfert  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité analytique**, puis choisissez le lien associé.  
2.  Sur la page **Paramètres comptabilité analytique**, vérifiez que le champ **Date début pour transfert comptabilité** est défini sur la valeur appropriée.  
3.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable des types de coûts**, puis choisissez le lien associé.  
4.  Sur la page **Fiche type de coût**, vérifiez que le champ **Plage compte général** est lié correctement de sorte que chaque type de coût récupère les écritures de la comptabilité.  
5.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
6.  Pour chaque compte général approprié, sur la page **Fiche compte général**, dans le raccourci Comptabilité analytique, vérifiez que le champ **N° type coût** est lié correctement à un type de coût. Pour plus d’informations, voir [Configuration du contrôle de gestion](finance-set-up-cost-accounting.md).  
7.  Vérifiez que toutes les écritures comptables appropriées comprennent des sections analytiques correspondant à un centre de coûts et à un coût associé.  

### Pour transférer les écritures comptables vers les écritures de coûts

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transférer les écritures comptables vers CA**, puis sélectionnez le lien associé.  
2.  Cliquez sur le bouton **Oui** pour démarrer le transfert. Le processus transfère toutes les écritures comptables qui n’ont pas déjà été transférées.  

Lors du transfert, le processus crée des connexions dans les écritures des tables **Écriture de coûts** et **Registre de coûts**. Cela permet d’identifier l’origine des écritures de coûts.

## Transfert automatique et écritures combinées

En comptabilité analytique, vous pouvez transférer les écritures comptables vers un type de coût à l’aide d’une validation combinée. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options.  

|Combiner écritures|Désignation|  
|---------------------|-----------------|  
|Aucun|Chaque écriture comptable est transférée individuellement vers le type de coût correspondant.|  
|Jour|Les écritures comptables, dont la date de validation est identique, sont transférées en une seul écriture vers le type de coût correspondant.|  
|Mois|Toutes les écritures comptables du même mois calendaire sont transférées en une seul écriture vers le type de coût correspondant.|  

> [!IMPORTANT]  
>  Si vous avez coché la case **Transférer automatiquement à partir de la compta** sur la page **Paramètres comptabilité analytique**, [!INCLUDE[prod_short](includes/prod_short.md)] met à jour la comptabilité analytique après chaque validation comptable. Les écritures combinées ne sont pas possibles.

## Résultats du transfert des écritures comptables vers les écritures de coûts

Lors du transfert des écritures comptables vers les écritures de coûts, [!INCLUDE[prod_short](includes/prod_short.md)] crée des connexions dans les écritures dans les tables **Écriture comptable**, **Écriture de coûts** et **Registre de coûts** pour assurer le suivi des connexions entre les écritures de coûts et les écritures comptables.  

### Écritures comptables

Pour chaque écriture comptable transférée vers la comptabilité analytique, [!INCLUDE[prod_short](includes/prod_short.md)] renseigne le champ **N° écriture**  

### Écritures de coûts

Pour chaque écriture de coûts, [!INCLUDE[prod_short](includes/prod_short.md)] garde le numéro de l’écriture comptable correspondante dans le champ **N° séquence compta.** de la table **Écriture de coûts**.  

Pour les écritures de coûts combinées, [!INCLUDE[prod_short](includes/prod_short.md)] garde le numéro de la dernière écriture comptable, à savoir l’écriture avec le numéro le plus élevé.  

Le champ **Compte général** de la table **Écriture de coûts** contient le numéro du compte général, d’où provient l’écriture de coûts.  

Pour les écritures de coûts uniques, [!INCLUDE[prod_short](includes/prod_short.md)] transfère le texte de validation depuis l’écriture comptable vers le champ de texte **Description**. Pour les écritures combinées, le champ de texte indique que ces écritures sont transférées en tant qu’écritures combinées. Par exemple, pour une écriture combinée pour octobre 2013, le texte peut être **Écritures combinées, octobre 2013**.  

### Registre de coûts

Dans la table **Registre de coûts**, [!INCLUDE[prod_short](includes/prod_short.md)] crée une écriture à l’aide du transfert source depuis la comptabilité. L’écriture enregistre le premier et le dernier numéros des écritures comptables transférées, outre le premier et le dernier numéros des écritures de coûts créées.

## Voir aussi

 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
 [Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)  
 [Définition et répartition des coûts](finance-define-and-allocate-costs.md)  
 [Comptabilité pour les coûts](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
