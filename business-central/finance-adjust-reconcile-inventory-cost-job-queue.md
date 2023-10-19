---
title: Planifier des tâches pour ajuster et rapprocher les coûts de stock
description: 'Découvrez comment vous pouvez utiliser la file d’attente des travaux pour déplacer les tâches d’ajustement du coût stocks ou de rapprochement avec la comptabilité en arrière-plan. Par exemple, si votre société exécute de nombreuses tâches ou traite de nombreuses transactions.'
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 09/19/2023
ms.author: bholtorf
---
# Planifier des tâches pour ajuster et rapprocher les coûts de stock

La planification de tâches pour l’ajustement automatique des coûts avec la comptabilité et la validation dans la comptabilité est activée par défaut.
Cependant, à mesure que les données s’accumulent au fil du temps, cela peut affecter les performances. Pour réduire la charge de l’application, il est souvent utile d’utiliser les écritures file d’attente des travaux pour déplacer les tâches à exécuter en arrière-plan.

## Déplacez la tâche d’ajustement des coûts article en arrière-plan à l’aide de la configuration assistée

La création des écritures file d’attente des travaux peut être compliquée, même pour un consultant expérimenté ; par conséquent, nous avons un guide de configuration assistée pour faciliter le processus d’ajustement des coûts article.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Paramètres stock**, puis sélectionnez le lien associé.  
2. Dans la page **Paramètres stock**, activez le champ **Compta. coûts automatique** ou spécifiez **Jamais** dans le champ **Ajustement automatique des coûts**.  
3. Dans la notification qui s’affiche maintenant en haut de la page, choisissez le lien **Planifier écriture file d’attente des travaux**. Cela ouvre le guide de configuration assistée **Planifier l’ajustement et la validation des coûts**.  
4. Spécifiez la tâche que vous souhaitez planifier.  

  > [!NOTE]
  > Vous ne pouvez pas créer une nouvelle écriture file d’attente des travaux si une écriture file d’attente des travaux pour la tâche spécifiée existe déjà.

5. Sélectionnez le champ **Afficher les écritures file d’attente des travaux quand vous avez terminé** pour réviser et ajuster les paramètres. Pour plus d’informations, voir [Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md).  

## Pour créer une écriture file d’attente des travaux pour ajuster et rapprocher manuellement le coût stocks

Vous pouvez également créer des écritures file d’attente des travaux manuellement. La procédure suivante montre comment définir le traitement par lots **Ajuster coût écritures article** pour s’exécuter automatiquement chaque jour, mais les mêmes étapes s’appliquent au traitement par lots **Valider coûts ajustés**.  

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Écritures file d’attente des travaux**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**.  
3. Dans le champ **Type objet à exécuter**, choisissez *Rapport*.  
4. Dans le champ **ID objet à exécuter**, choisissez *795*, **Ajuster coût écritures article**.  
5. Dans le champ **Formule de la date de la prochaine exécution**, entrez *1D*.
6. Dans le champ **Heure début**, entrez *14h00*.
7. Choisissez l’action **Attribuer le statut Prêt**.

Maintenant, le coût stocks sera mis à jour toutes les nuits.  

Pour planifier une tâche de rapprochement du stock avec la comptabilité, choisissez Codeunit 2846 **Valider coûts ajustés**.

> [!TIP]
> Pour éviter le verrouillage, ne planifiez pas de tâches pour le traitement par lots **Ajuster coûts : Écr. article**, le codeunit **Valider coûts ajustés** et les tâches de validation des transactions de vente ou d’achat en même temps. Assurez-vous également qu’ils utilisent la même catégorie de file d’attente des travaux.

## Voir aussi

[Ajustement coûts article](inventory-how-adjust-item-costs.md)  
[Rapprochement des coûts et de la comptabilité](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Utiliser des files d’attente des travaux pour planifier des tâches](admin-job-queues-schedule-tasks.md)  
[Recherche de pages et d’informations avec Tell Me](ui-search.md)  
[Utiliser [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
