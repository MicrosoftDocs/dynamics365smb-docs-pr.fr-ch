---
title: "Procédure\_: configurer des utilisateurs de flux de travail"
description: 'Avant de pouvoir créer des flux de travail, vous devez configurer des utilisateurs qui y participent sur la page Paramètres utilisateur des approbations.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# Configurer une séquence d’utilisateurs de flux de travail

Avant de pouvoir créer des flux de travail approbation, vous devez configurer des utilisateurs qui enverront des requêtes et leurs approbateurs. Par exemple, vous pouvez spécifier qui doit recevoir une notification pour agir sur une étape du flux de travail. Vous configurez les participants du flux de travail approbation sur la page **Paramètres utilisateur des approbations**. En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).

Sur la page  **Groupes d’utilisateurs du flux de travail**, vous pouvez spécifier où un participant s’engage dans un flux de travail approbation en saisissant un numéro dans le champ **N° de séquence** . Par exemple, vous pouvez spécifier que les utilisateurs s’engagent dans un ordre séquentiel, comme une chaîne d’approbateurs. Vous pouvez également spécifier une liste plate d’approbateurs en saisissant le même numéro. Dans ce dernier cas, un seul des approbateurs doit approuver une demande.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## Configurer un groupe d’utilisateurs de flux de travail

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  saisissez **Groupes utilisateur flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Groupe d’utilisateurs du flux de travail** s’ouvre.  
3. Dans le champ **Code**, entrez 20 caractères maximum pour identifier le flux de travail.  
4. Dans le champ **Description**, décrivez le flux de travail.  
5. Dans le raccourci **Membres de groupe d’utilisateurs du flux de travail**, renseignez la première ligne des champs comme indiqué dans le tableau ci-dessous.  

   |Champ|Désignation|
   |-----|-----------|
   |**Nom de l'utilisateur**|Spécifiez l’utilisateur qui participera à un flux de travail.<br /><br /> L’utilisateur doit exister sur la page **Paramètres utilisateur**. En savoir plus sur [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).|
   |**N° séquence**|Spécifiez l’ordre dans lequel l’utilisateur du flux de travail s’engage dans un flux par rapport à d’autres utilisateurs. Ce champ peut être utilisé, par exemple, pour indiquer à quel moment l’utilisateur approuve, par rapport à d’autres approbateurs, lorsque vous utilisez l’option **Groupe d’utilisateurs de flux de travail** dans le champ **Type approbateur** de la réponse de flux de travail lié.| 

6. Répétez l’étape 5 pour ajouter des utilisateurs de flux de travail dans le groupe d’utilisateurs de flux de travail.  

## Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## Voir aussi

[Configuration des utilisateurs des approbations](across-how-to-set-up-approval-users.md)  
[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Utilisation des flux d’approbation](across-use-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flux de travail](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
