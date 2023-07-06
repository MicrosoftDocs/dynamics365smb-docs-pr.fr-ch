---
title: Utilisation des flux de travail approbation
description: Vous pouvez configurer et utiliser des flux de travail qui relient les tâches de processus métier telles que la publication automatique ou la demande et l’approbation de nouveaux enregistrements.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="use-approval-workflows"></a><a name="use-approval-workflows"></a><a name="use-approval-workflows"></a>Utilisation des flux d’approbation

Un flux de travail est une séquence de tâches déclenchées par une action, une condition ou une règle. Les flux de travail sont généralement mis en œuvre pour intégrer la logique métier à une organisation, telle que la séparation des tâches, l’unification des processus ou pour appliquer les bonnes pratiques.

Les flux de travail sont conçus pour créer des demandes pour approbation d’une modification du champ d’enregistrement tout en conservant l’ancienne valeur au cas où la demande ne serait pas approuvée. La nouvelle valeur ne sera pas mise en œuvre tant que la dernière demande n’aura pas été approuvée.

La logique métier pourrait être l’approbation de :

- Nouvelles données de base telles que les comptes généraux, les clients, les fournisseurs ou les articles.
- Modifications apportées aux champs dans les enregistrements existants contenant des informations sensibles, telles que **N° compte bancaire fournisseur** ou **Crédit autorisé du client**.
- Modifications apportées aux champs des enregistrements existants contenant des informations critiques pour l’entreprise, telles que **Prix de vente des articles**.
- Nouveaux utilisateurs ou modifications des autorisations des utilisateurs.
- Documents achat.
- Documents vente.
- Documents entrants.
- Feuilles financières avant publication.

L’illustration suivante montre un exemple de flux de travail avec approbation séquentielle déclenchée par un utilisateur. En déclenchant le flux de travail, une demande d’approbation est créée pour le premier approbateur.  

![Illustration d’un flux de travail avec approbation séquentielle.](media/Workflows/approval-flow.png)

Ci-dessus, vous voyez une illustration de la façon dont la demande doit être approuvée par le premier approbateur avant que la demande ne soit envoyée au prochain approbateur. Si la demande n’est pas approuvée par le premier approbateur, elle ne sera jamais transmise au prochain approbateur.

Le chemin emprunté depuis le déclenchement initial du workflow peut varier en fonction de la nature de l’approbation.  

L’illustration suivante montre une approbation parallèle déclenchée par l’utilisateur. En déclenchant le flux d’utilisateur, une demande d’approbation est envoyée à tous les approbateurs simultanément.  

![Illustration d’un flux de travail avec approbation parallèle.](media/Workflows/approval-flow-2.png)

Cependant, le flux de travail n’est pas approuvé tant que toutes les demandes n’ont pas été approuvées par les approbateurs, comme le montre l’illustration suivante :  

![Illustration d’un flux de travail rejeté avec approbation parallèle.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Pour un flux de travail avec plusieurs approbateurs, tous les approbateurs doivent approuver chaque étape avant que le flux de travail puisse passer à l’événement suivant. L’approbation d’un seul approbateur ne fera pas avancer le flux de travail.

Vous pouvez configurer et utiliser des flux de travail qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Il est également possible de créer plusieurs fois le même flux de travail. Chaque flux de travail peut-être déclenché par un événement utilisant des filtres différents. Ceci est utile si une demande d’approbation dans un service doit être approuvée par un approbateur, alors que les demandes d’approbation dans d’autres services doivent être approuvées par un autre approbateur. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du flux de travail, précédées ou suivies des tâches de l’utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du flux de travail.  

Avant de pouvoir commencer à utiliser des flux de travail, vous devez configurer des utilisateurs de flux de travail, créer les flux de travail, potentiellement précédés d’une personnalisation de code et spécifier la manière dont les utilisateurs reçoivent les notifications. En savoir plus sur [Configurer les flux de travail](across-set-up-workflows.md).

> [!NOTE]  
> Les étapes d’un flux de travail traitent en général des utilisateurs qui demandent l’approbation des tâches et des approbateurs qui acceptent ou rejettent les demandes d’approbations. C’est pourquoi la plupart des rubriques sur l’utilisation des flux de travail concernent les approbations.  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les articles qui les décrivent.  

| **Pour** | **Voir** |
|--|--|
| Configurez un flux de travail approbation pour démarrer lorsque le premier événement de point d’entrée se produit. | [Activation des flux d’approbation](across-how-to-enable-workflows.md) |
| Demander l’approbation d’une tâche, en tant qu’approbateur, accepter, décliner ou déléguer des approbations, et envoyer ou afficher des notifications d’approbation. | [Procédure : utilisation des flux d’approbation](across-how-use-approval-workflows.md) |
| Créez des étapes de flux de travail qui limitent l’utilisation d’un certain type d’enregistrement avant qu’un certain événement ne se produise, par exemple que l’enregistrement est approuvé. | [Restreindre et autoriser l’utilisation d’un enregistrement](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Affichez les instances d’étape de flux de travail dont le statut est **Terminé**. | [Afficher des instances d’étape de flux de travail archivées](across-how-to-view-archived-workflow-step-instances.md) |
| Supprimez un flux de travail approbation que vous êtes sûr de ne plus utiliser. | [Suppression des flux d’approbation](across-how-to-delete-workflows.md) |

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Voir aussi

[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Flux de travail](across-workflow.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
