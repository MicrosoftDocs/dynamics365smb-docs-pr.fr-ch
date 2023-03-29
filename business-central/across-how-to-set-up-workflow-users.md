---
title: "Procédure\_: configurer des utilisateurs de flux de travail"
description: 'Avant de pouvoir créer des flux de travail, vous devez configurer des utilisateurs qui y participent sur la page Groupe d’utilisateurs du flux de travail.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
---
# Configurer des utilisateurs de flux de travail

Avant de pouvoir créer des flux de travail approbation, vous devez configurer des utilisateurs qui participent aux flux de travail. Cela est nécessaire, par exemple, pour spécifier qui doit recevoir une notification pour agir sur une étape du flux de travail.  

Sur la page **Groupes d’utilisateurs du flux de travail**, configurez des utilisateurs sous des groupes d’utilisateurs de flux de travail, et spécifiez le numéro des utilisateurs dans une séquence de processus, comme une chaîne d’approbateurs. 

Les utilisateurs de flux de travail dont la fonction est utilisateurs approbation, à la fois demandeurs d’approbation et approbateurs, doivent également être définis sur la page **Paramètres utilisateur approbation**. En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Pour indiquer qu’une demande d’approbation n’est pas approuvée tant que plusieurs utilisateurs dans une chaîne d’approbation ne l’ont pas approuvée, configurez les approbateurs selon une hiérarchie. Pour le type d’approbateur **Approbateur**, configurez les approbateurs sur la page **Paramètres utilisateur d’approbation**. Pour le type d’approbateur **Groupe d’utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d’utilisateurs du flux de travail** et définissez la hiérarchie en affectant des numéros incrémentiels à chaque approbateur dans le champ **N° séquence** . En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md). 

## Configurer un utilisateur de flux de travail

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes utilisateur flux de travail**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Groupe d’utilisateurs du flux de travail** s’ouvre.  
3. Dans le champ **Code**, entrez 20 caractères maximum pour identifier le flux de travail.  
4. Dans le champ **Description**, décrivez le flux de travail.  
5. Dans le raccourci **Membres de groupe d’utilisateurs du flux de travail**, renseignez la première ligne des champs comme indiqué dans le tableau ci-dessous.  

   |Champ|Désignation|
   |-----|-----------|
   |**Nom d’utilisateur**|Spécifiez l’utilisateur qui participera aux flux de travail.<br /><br /> L’utilisateur doit exister sur la page **Paramètres utilisateur**. En savoir plus sur [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).|
   |**N° séquence**|Spécifiez l’ordre dans lequel l’utilisateur du flux de travail s’engage dans un flux par rapport à d’autres utilisateurs. Ce champ peut être utilisé, par exemple, pour indiquer à quel moment l’utilisateur approuve, par rapport à d’autres approbateurs, lorsque vous utilisez l’option **Groupe d’utilisateurs de flux de travail** dans le champ **Type approbateur** de la réponse de flux de travail lié.| 

   > [!TIP]
   > CONSEIL : pour indiquer qu’une demande d’approbation nécessite l’approbation de plusieurs utilisateurs de même niveau, quelle que soit la hiérarchie, configurez un groupe d’utilisateurs horizontal en affectant le même numéro de séquence aux approbateurs appropriés.

6. Répétez l’étape 5 pour ajouter des utilisateurs de flux de travail dans le groupe d’utilisateurs de flux de travail.  
7. Répétez l’étape 2 à 6 pour ajouter des groupes d’utilisateurs de flux de travail.  

## Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## Voir aussi

[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Utilisation des flux d’approbation](across-use-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flux de travail](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
