---
title: Dépannage et correction des axes analytiques
description: Découvrez comment dépanner les erreurs d′axes analytiques classiques et comment corriger les axes analytiques après leur utilisation sur des transactions validées.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 09/27/2021
ms.author: bholtorf
---

# Dépannage et correction des axes analytiques

Les rapports financiers et les vues d′analyse reposent souvent sur les données des axes analytiques. Malgré les garanties disponibles, il se produit parfois une erreur pouvant entraîner des imprécisions. Cette rubrique décrit certaines erreurs classiques et explique comment corriger les affectations d′axes analytiques sur les transactions validées afin que les rapports financiers soient précis.

## Résolution des erreurs liées aux axes analytiques

Lorsque vous validez des documents ou des lignes feuille qui contiennent des axes analytiques, différentes erreurs peuvent survenir qui sont toutefois généralement liées à une configuration ou à une affectation incorrectes des axes.

> [!NOTE]
> Dans la liste suivante des messages d’erreur potentielle, les codes *%X* sont des espaces réservés pour les variables de données qui le message réel contient dans l’interface utilisateur selon le contexte. Par exemple, *%1 %2 est bloqué.* pourrait s’afficher dans l’interface utilisateur comme « La ZONE du code axe est bloquée ».  

|Problème|Message d’erreur|Solution possible|
|-----|-------------|-----------------|
|Axe bloqué|%1 %2 est bloqué.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec l’axe bloqué et débloquez-le.<br />- Supprimez la ligne ensemble de dimensions pour l’axe bloqué.|
|Axe supprimé|%1 %2 est introuvable.|- Restaurez l’axe manquant.<br />- Recherchez les documents non validés contenant l’ensemble de dimensions avec l’axe manquant et ajoutez-le.<br />- Supprimez la ligne ensemble de dimensions pour l’axe manquant.|
|Valeur de l’axe bloqué|%1 %2 - %3 est bloqué.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec la valeur de l’axe bloqué et débloquez-le.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l’axe bloqué.|
|Valeur de l’axe supprimé|    %1 pour %2 est manquant.|- Restaurez la valeur de l’axe manquant.<br />- Recherchez les documents non validés contenant l’ensemble d’axes avec la valeur de l’axe manquant et ajoutez-le.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l’axe manquant.|
|Valeur de l’axe rejeté|Le type de valeur de l’axe pour %1 %2 - %3 ne doit pas être %4.|- Modifiez le champ **Type de valeur de l’axe** sur la page **Valeurs de l’axe** avec **Standard** ou **Début total**.<br />- Supprimez la ligne ensemble de dimensions pour la valeur de l’axe bloqué.|
|Croisement analytique bloqué|Les axes analytiques %1 et %2 ne peuvent pas être utilisés ensemble.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec la valeur du croisement analytique bloqué et débloquez-le.<br />- Modifiez une des lignes d’ensembles d’autorisation en conflit pour le croisement analytique.|
|Croisement valeur analytique bloquée|Les croisements analytiques %1 - %2 et %3 - %4 ne peuvent pas être utilisés ensemble.|- Recherchez les documents non validés contenant l’ensemble de dimensions avec la valeur du croisement analytique bloqué et débloquez-le.<br />- Modifiez une des lignes d’ensembles d’autorisation en conflit pour le croisement de la valeur analytique.|
|Code de valeur analytique vierge pour l’axe par défaut où le champ **Contrôle validation** contient **Code obligatoire**|- Sélectionnez un %1 pour le %2 %3.<br />- Sélectionnez un %1 pour le %2 %3 pour %4 %5.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez une valeur analytique non vierge pour l’axe analytique en conflit dans l’ensemble d’axes.|
|Code de valeur analytique erroné pour l’axe par défaut où le champ **Contrôle validation** contient **Code identique**|- Sélectionnez %1 %2 pour le %3 %4.<br />- Sélectionnez %1 %2 pour le %3 %4 pour %5 %6.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez la valeur analytique requise pour l’axe analytique en conflit dans l’ensemble de dimensions.|
|Code de valeur analytique non vierge pour l’axe par défaut vierge où le champ **Contrôle validation** contient **Code identique**|-%1 %2 doit être vierge.<br />-%1 %2 doit être vierge pour %3 %4.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Saisissez un code de valeur analytique vierge pour l’axe analytique en conflit dans l’ensemble d’axes.|
|Valeur analytique inattendue pour l’axe par défaut où le champ **Contrôle validation** contient **Aucun code**|-%1 %2 ne doit pas être mentionné.<br />-%1 %2 ne doit pas être mentionné pour %3 %4.|- Modifiez le champ **Contrôle validation** sur la page **Axe analytique par défaut**.<br />- Supprimez la ligne en conflit depuis l’ensemble de dimensions.|
|Une correction d’axe analytique ne se termine pas correctement.||-Choisissez **Réinitialiser** pour rétablir la correction à un état brouillon. Cela réinitialise les modifications et vous pouvez réexécuter la correction.|

## Modification des attributions d’axe analytique après la publication

Si vous découvrez qu’une dimension incorrecte a été utilisée sur les écritures comptables comptabilisées, vous pouvez corriger les valeurs d’axe analytique et mettre à jour vos vues d’analyse. Cela vous aide à garder vos rapports et analyses financiers exacts.

> [!IMPORTANT]
> Les fonctionnalités de correction des axes analytiques visent uniquement à rendre les rapports financiers précis. Les corrections d′axes analytiques s′appliquent uniquement aux entrées comptables. Ils ne modifient pas les axes analytiques affectés aux autres écritures comptables pour la même transaction. Un problème de correspondance existe entre les axes analytiques affectés dans les écritures comptables et dans les grands livres auxiliaires.

### Paramétrage des corrections des axes analytiques

Il y a deux choses à prendre en compte lors de la configuration des corrections d’axe analytique :

* Y a-t-il des axes analytiques que vous ne souhaitez pas permettre aux gens de changer ? Sur la page **Paramètres de correction d’axes analytiques**, spécifiez les axes analytiques que vous souhaitez bloquer pour les modifications.
* À qui souhaitez-vous autoriser le changement d’axes analytiques ? Pour autoriser les utilisateurs à apporter des modifications, attribuez l’autorisation **CORRECTION AXE D365** aux utilisateurs. Les autorisations leur permettent de créer des corrections d’axes analytiques, de les exécuter et de les annuler si nécessaire. Ils pourront également spécifier des axes analytiques bloqués. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md). 

### Correction d’un axe analytique

Vous pouvez sélectionner manuellement une ou plusieurs écritures comptables ou utiliser des filtres pour sélectionner des séries d’entrées. Si nécessaire, vous pouvez également ajouter ou supprimer des axes analytiques. 

1. Pour démarrer une correction d’axes analytiques, utilisez l’une des pages suivantes :

    * Sur la page **Comptabilité/Registre**, en sélectionnant un registre, puis en choisissant l’action **Corriger les axes analytiques**. Ceci lance une correction pour les entrées dans le registre sélectionné.
    * Sur la page **Écritures comptables**, en choisissant l’action **Correction d’axes analytiques**. 

2. Dans le champ **Description**, entrez les informations sur la modification. D’autres personnes pourraient utiliser ces informations plus tard pour comprendre ce qui a été fait.
3. Sur le Raccourci **Écritures comptables sélectionnées**, choisissez les entrées appropriées.

    > [!IMPORTANT]
    > Lorsque vous modifiez une sélection, les valeurs du Raccourci **Modifications de correction d’axes analytiques** sont réinitialisées. Par conséquent, sélectionnez toujours les entrées avant de spécifier les changements de valeur d’axes analytiques.

   Le tableau suivant décrit les options.

   |Option  |Description  |
   |---------|---------|
   |Ajouter les écritures associées     |Ajoutez les écritures comptables qui sont dans le même registre comptable.|   
   |Ajouter par filtre     |Utilisez des critères de filtre lors de l’ajout d’écritures comptables.|
   |Sélection manuelle     |Sélectionnez des écritures comptables spécifiques.         |
   |Ajouter par axe analytique     |Filtrez les écritures comptables par axes analytiques.         |
   |Supprimer des écritures     |Désélectionnez des écritures comptables.         |
   |Gérer les critères de sélection     |Suivez le processus de sélection et annulez les sélections si nécessaire.         |

4. Sur le Raccourci **Modifications de correction d’axes analytiques**, choisissez l’axes analytiques que vous souhaitez modifier dans le champ **Code d’axes analytiques** et la nouvelle valeur dans le champ **Nouveau code de valeur d’axes analytiques**.
5. Pour valider que la correction, choisissez **Valider les changements d’axes analytiques**. Pour plus d′informations, voir [Validation des corrections d′axes analytiques](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Choisir **Exécuter**.

### Validation des corrections d’axes analytiques

Avant d’exécuter une correction, il est conseillé de la valider d’abord. La validation vérifie les restrictions sur la comptabilisation des valeurs pour les comptes généraux, les restrictions pour les axes analytiques et si les valeurs des axes analytiques sont bloquées. Lors de la validation, le statut de la correction est défini sur **Validation en cours**. Après avoir validé une correction, le résultat s’affiche dans le champ **Statut de validation**. Si des erreurs ont été trouvées, vous pouvez utiliser l’action **Afficher les erreurs** pour les enquêter. Après avoir corrigé une erreur, vous devez utiliser l’action **Rouvrir** pour exécuter la correction ou une nouvelle validation.

Vous pouvez soit exécuter une correction immédiatement, soit la planifier pour une exécution ultérieure. Si vous exécutez des corrections sur un jeu de données volumineux, nous vous recommandons de le planifier pour qu’il s’exécute en dehors des heures ouvrables. Pour plus d′informations, voir [Corrections d′axes analytiques sur des jeux de données volumineux](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### Annuler une correction

Après avoir corrigé un axe analytique, si vous n’aimez pas ce que vous voyez, vous pouvez utiliser l’action **Annuler** pour réinitialiser la valeur précédente. Cependant, vous ne pouvez annuler que la correction la plus récente. Avant d’annuler une correction, vous pouvez valider les modifications que l’annulation apportera. Par exemple, cela est utile si les restrictions d’axes analytiques ont changé après la correction.

Si l’action Annuler n’est pas disponible, par exemple parce que vous avez effectué de nombreuses corrections, vous pouvez utiliser l’action **Copier dans le brouillon** pour démarrer une nouvelle correction pour les mêmes entrées.

### Corrections d’axes analytiques sur des jeux de données volumineux

Soyez prudent lorsque vous corrigez de grands ensembles d’entrées, par exemple, des ensembles comprenant plus de 10 000 entrées. Si vous le pouvez, nous vous recommandons d’utiliser les filtres pour exécuter les corrections sur des jeux de données plus petits. Il est également judicieux d’exécuter des corrections en dehors des heures normales de bureau. 

### Utiliser des vues d’analyse avec des corrections d’axes analytiques

Si **Mise à jour sur la publication** est activé pour une vue d’analyse, [!INCLUDE[prod_short](includes/prod_short.md)] peut afficher la vue lorsque les documents et les journaux sont publiés. Vous pouvez également mettre à jour les vues avec ce paramètre activé avec les résultats des corrections d’axes analytiques. Pour ce faire, activez le bouton de basculement **Mettre à jour les vues d’analyse**. La mise à jour des vues d’analyse peut avoir un impact sur les performances, en particulier pour les grands jeux de données, c’est pourquoi nous vous recommandons de mettre à jour les vues d’analyse uniquement pour les petits jeux de données.  

### Affichage des corrections de axes analytiques historiques

Si une écriture comptable a été corrigée, vous pouvez étudier la modification en utilisant l’action **Historique des corrections d’axes analytiques**.

### Traitement des corrections incomplètes

Si une correction ne se termine pas, un avertissement s’affiche sur la carte de correction. Si cela se produit, vous pouvez utiliser l’action **Réinitialiser** pour rétablir la correction à un statut de brouillon et annuler les modifications. Vous pouvez ensuite exécuter à nouveau la correction.

> [!NOTE]
> La réinitialisation d’une correction incomplète n’affectera pas les mises à jour des vues d’analyse, car celles-ci se produisent à la fin du processus de correction.

### Utiliser la comptabilité analytique avec les écritures comptables corrigées

Une fois les axes analytiques corrigés, vos données pour la comptabilité analytique seront désynchronisées. La comptabilité analytique utilise des axes analytiques pour agréger les montants des centres de coûts et des coûts associés, et pour exécuter les répartitions de coûts. La modification des axes analytiques des écritures comptables signifiera probablement que vous réexécuterez vos modèles de comptabilité analytique. Que vous deviez simplement supprimer quelques registres de coûts et réexécuter les allocations, ou que vous deviez tout supprimer et réexécuter tous vos modèles, cela dépend des données qui ont été mises à jour et de la configuration de vos capacités de comptabilité analytique. Vous devez manuellement identifier où les corrections d’axes analytiques auront un impact sur la comptabilité analytique et où des mises à jour sont nécessaires. [!INCLUDE[prod_short](includes/prod_short.md)] ne propose pas actuellement de moyen automatisé de le faire.

## Voir la [formation Microsoft](/training/modules/dimensions-dynamics-365-business-central/) associée

## Voir aussi

[Utiliser les axes analytiques](finance-dimensions.md)  
[Analyse des données par axe analytique](bi-how-analyze-data-dimension.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
