---
title: "Procédure : configurer des utilisateurs d'approbation | Microsoft Docs"
description: Avant de pouvoir créer des workflows qui impliquent des étapes d'approbation, vous devez configurer les utilisateurs du workflow qui sont impliqués dans les processus d'approbation. Sur la page Paramètres utilisateur d'approbation, vous pouvez également définir les limites pour des types spécifiques de demandes et définir des approbateurs remplaçants à qui des demandes d'approbation sont déléguées lorsque l'approbateur initial est absent.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4775af4afa3d1e97ad15aa24a710ec4e27ef554e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "912647"
---
# <a name="set-up-approval-users"></a>Configurer des utilisateurs d'approbation
Avant de pouvoir créer des flux de travail qui impliquent des étapes d'approbation, vous devez configurer les utilisateurs du flux de travail qui sont impliqués dans les processus d'approbation. Sur la page **Paramètres utilisateur d'approbation**, vous pouvez également définir les limites pour des types spécifiques de demandes et définir des approbateurs remplaçants à qui des demandes d'approbation sont déléguées lorsque l'approbateur initial est absent.  

> [!NOTE]  
>  Les utilisateurs d'approbation, à la fois demandeurs d'approbation et approbateurs, doivent d'abord être définis comme utilisateurs du flux de travail sur la page **Groupe d'utilisateurs du flux de travail**. Pour plus d'informations, reportez-vous à [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md).  

 Lorsque vous configurez des utilisateurs approbation, vous pouvez utiliser le paramétrage de création de réponses du workflow pour des workflow d'approbation. Pour plus d'informations, reportez-vous à l'étape 9 dans [Créer des workflows](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Pour indiquer qu'une demande d'approbation n'est pas approuvée tant que plusieurs approbateurs dans une chaîne d'approbation ne l'ont pas approuvée, configurez les approbateurs selon une hiérarchie. Pour le type d'approbateur **Approbateur**, configurez les approbateurs sur la page **Paramètres utilisateur d'approbation**. Pour le type d'approbateur **Groupe d'utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d'utilisateurs du flux de travail** et définissez la hiérarchie en affectant des numéros incrémentiels à chaque approbateur dans le champ **N° séquence** . Pour plus d'informations, reportez-vous à cette rubrique et à [Configurer des utilisateurs de workflow](across-how-to-set-up-workflow-users.md).  
>   
>  Pour indiquer qu'une demande d'approbation n'est pas approuvée tant que plusieurs approbateurs de même niveau ne l'ont pas approuvée, indépendamment d'une hiérarchie, configurez un groupe d'utilisateurs de flux de travail horizontal. Pour le type d'approbateur **Groupe d'utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d'utilisateurs du flux de travail** et affectez le même numéro à chaque approbateur dans le champ **N° séquence** . Pour plus d'informations, reportez-vous à [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Configurer un utilisateur approbation  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres utilisateur approbation**, puis sélectionnez le lien associé.  
2. Créez une ligne sur la page **Paramètres utilisateur d'approbation**, puis renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code utilisateur**|Sélectionnez le code de l'utilisateur impliqué dans le processus d'approbation.|  
    |**Code vendeur/acheteur**|Spécifiez le code vendeur ou acheteur qui s'applique à l'utilisateur dans le champ **Code vendeur/acheteur**.<br /><br /> En général, vous remplissez le champ **Code vendeur/acheteur** si le vendeur ou l'acheteur responsable pour le client ou le fournisseur, est aussi la personne qui doit approuver la demande vente ou achat en question.|  
    |**ID approbateur**|Sélectionnez le code d'utilisateur qui doit approuver des demandes effectuées par l'utilisateur dans le champ **ID utilisateur**.|  
    |**Montant maximal vente autorisé**|Spécifiez le montant de vente maximal en DS qui peut être approuvé par l'utilisateur dans le champ**ID utilisateur**.|  
    |**Montant illimité de vente autorisé**|Spécifiez que l'utilisateur dans le champ**ID utilisateur** peut approuver toutes les demandes vente quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal vente autorisé**.|  
    |**Montant maximal achat autorisé**|Spécifiez le montant d'achat maximal en DS qui peut être approuvé par l'utilisateur dans le champ**ID utilisateur**.|  
    |**Montant illimité d'achat autorisé**|Spécifiez que l'utilisateur dans le champ**ID utilisateur** peut approuver toutes les demandes achat quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal vente autorisé**.|  
    |**Montant maximal demande achat autorisé**|Spécifiez le montant maximal en DS qui peut être approuvé par l'utilisateur pour les devis d'achat dans le champ **ID utilisateur**.<br /><br /> Pour utiliser ce champ, vous devez sélectionner l'option **Chaîne d'approbateurs** dans le champ **Type limite approbateur** sur la page **Réponse de flux de travail**.|  
    |**Montant illimité de demande d'achat autorisé**|Spécifiez que l'utilisateur dans le champ**ID utilisateur** peut approuver tous les devis d'achat quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal demande achat autorisé**.|  
    |**Remplaçant**|Sélectionnez le code d'utilisateur qui doit approuver des demandes effectuées par l'utilisateur dans le champ **ID utilisateur** si l'utilisateur dans le champ **ID approbateur** n'est pas disponible. **Note :** le remplaçant peut être soit l'utilisateur dans le champ **Remplaçant**, l'approbateur direct, soit l'administrateur d'approbation, dans cet ordre de priorité. Pour plus d'informations, reportez-vous à [Utilisation des flux d'approbation](across-how-use-approval-workflows.md).|  
    |**Adresse de messagerie**|Spécifiez l'adresse de messagerie de l'utilisateur dans le champ **ID utilisateur**.|  
    |**Administrateur approbation**|Spécifiez l'utilisateur qui a des autorisations de débloquer des workflows d'approbation, par exemple, en déléguant les demandes d'approbation à de nouveaux approbateurs remplaçants et en supprimant des demandes d'approbation échues.|  

    > [!NOTE]  
    >  Le comportement du champ **Type limite approbateur** s'applique uniquement aux modules où les limites peuvent être définies, à savoir les approbations de vente et d'achat. Tous les autres types d'approbation où les limites ne s'appliquent pas ont toujours le comportement décrit pour l'option **Approbateur direct**.  

3. Pour test le paramétrage utilisateur approbation, choisissez l'action **Tester paramètres utilisateur approbation**.  
4. Répétez les étapes 2 et 3 pour chaque utilisateur que vous souhaitez configurer en tant qu'utilisateur approbation.  

## <a name="see-also"></a>Voir aussi  
[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)   
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)   
[Créer des workflows](across-how-to-create-workflows.md)   
[Paramétrage des workflows](across-set-up-workflows.md)   
[Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Flux de travail](across-workflow.md)   
