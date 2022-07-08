---
title: 'Procédure : configurer des utilisateurs de flux de travail'
description: Avant de pouvoir créer des workflows, vous devez configurer des utilisateurs qui y participent sur la page Groupe d’utilisateurs du workflow.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 57d106918230007484f37979b416d44277c86035
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075149"
---
# <a name="set-up-workflow-users"></a>Configurer des utilisateurs de flux de travail

Avant de pouvoir créer des flux de travail, vous devez configurer des utilisateurs qui participent aux flux de travail. Cela est nécessaire, par exemple, pour spécifier qui doit recevoir une notification pour agir sur une étape du flux de travail.  

Sur la page **Groupe d’utilisateurs du flux de travail**, configurez des utilisateurs sous des groupes d’utilisateurs de flux de travail, et spécifiez le numéro des utilisateurs dans une séquence de processus, comme une chaîne d’approbateurs.  

Les utilisateurs de flux de travail dont la fonction est utilisateurs approbation, à la fois demandeurs d’approbation et approbateurs, doivent également être définis sur la page **Paramètres utilisateur approbation**. Pour plus d’informations, voir [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Pour indiquer qu’une demande d’approbation n’est pas approuvée tant que plusieurs approbateurs dans une chaîne d’approbation ne l’ont pas approuvée, configurez les approbateurs selon une hiérarchie. Pour le type d’approbateur **Approbateur**, configurez les approbateurs sur la page **Paramètres utilisateur d’approbation**. Pour le type d’approbateur **Groupe d’utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d’utilisateurs du flux de travail** et définissez la hiérarchie en affectant des numéros incrémentiels à chaque approbateur dans le champ **N° séquence** . Pour plus d’informations, reportez-vous à [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md) et à la section suivante.  
>
> Pour indiquer qu’une demande d’approbation n’est pas approuvée tant que plusieurs approbateurs de même niveau ne l’ont pas approuvée, indépendamment d’une hiérarchie, configurez un groupe d’utilisateurs de flux de travail horizontal. Pour le type d’approbateur **Groupe d’utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d’utilisateurs du flux de travail** et affectez le même numéro à chaque approbateur dans le champ **N° séquence** . Pour plus d’informations, reportez-vous à la section suivante.  

## <a name="to-set-up-a-workflow-user"></a>Configurer un utilisateur de workflow

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes utilisateur workflow**, puis choisissez le lien associé.  
2. Sélectionnez l’action **Nouveau**. La page **Groupe d’utilisateurs du flux de travail** s’ouvre.  
3. Dans le champ **Code**, entrez 20 caractères maximum pour identifier le flux de travail.  
4. Dans le champ **Description**, décrivez le workflow.  
5. Dans le raccourci **Membres de groupe d’utilisateurs du workflow**, renseignez la première ligne des champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Nom d’utilisateur**|Spécifiez l’utilisateur qui participera aux workflows.<br /><br /> L’utilisateur doit exister sur la page **Paramètres utilisateur**. Pour en savoir plus, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).|  
    |**N° séquence**|Spécifiez l’ordre dans lequel l’utilisateur du flux de travail s’engage dans un flux par rapport à d’autres utilisateurs. Ce champ peut être utilisé, par exemple, pour indiquer à quel moment l’utilisateur approuve, par rapport à d’autres approbateurs, lorsque vous utilisez l’option **Groupe d’utilisateurs de flux de travail** dans le champ **Type approbateur** de la réponse de flux de travail lié. **CONSEIL :**  pour indiquer qu’une demande d’approbation n’est pas approuvée tant que plusieurs approbateurs de même niveau ne l’ont pas approuvée, quelle que soit la hiérarchie, configurez un groupe d’utilisateurs horizontal en affectant le même numéro de séquence aux approbateurs appropriés.|  
6. Répétez l’étape 5 pour ajouter des utilisateurs de workflow dans le groupe d’utilisateurs.  
7. Répétez l’étape 2 à 6 pour ajouter des groupes d’utilisateurs de workflow.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Voir aussi

[Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md)  
[Paramétrage des workflows](across-set-up-workflows.md)  
[Utiliser des workflows](across-use-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flux de travail](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]