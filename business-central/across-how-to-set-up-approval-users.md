---
title: Configurer des utilisateurs d’approbation
description: Avant de pouvoir créer des workflows qui impliquent des étapes d’approbation, vous devez configurer les utilisateurs du workflow qui sont impliqués dans les processus d’approbation avec les paramètres utilisateur d’approbation.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7602481a357a9b9e362a7b6fc0d605de04f44537
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129222"
---
# <a name="set-up-approval-users"></a>Configurer des utilisateurs d’approbation

Avant de pouvoir créer des workflows qui impliquent des étapes d’approbation, vous devez configurer les utilisateurs du workflow qui sont impliqués dans les processus d’approbation. Sur la page **Paramètres utilisateur d’approbation**, vous pouvez également définir les limites pour des types spécifiques de demandes et définir des approbateurs remplaçants à qui des demandes d’approbation sont déléguées lorsque l’approbateur initial est absent.  

> [!NOTE]  
> Les utilisateurs d’approbation, à la fois demandeurs d’approbation et approbateurs, doivent d’abord être définis comme utilisateurs du flux de travail sur la page **Groupe d’utilisateurs du flux de travail**. Pour plus d’informations, reportez-vous à [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md).  

 Lorsque vous configurez des utilisateurs approbation, vous pouvez utiliser le paramétrage de création de réponses du workflow pour des workflow d’approbation. Pour plus d’informations, reportez-vous à l’étape 9 dans [Créer des workflows](across-how-to-create-workflows.md).  

> [!NOTE]  
> Pour indiquer qu’une demande d’approbation n’est pas approuvée tant que plusieurs approbateurs dans une chaîne d’approbation ne l’ont pas approuvée, configurez les approbateurs selon une hiérarchie. Pour le type d’approbateur **Approbateur**, configurez les approbateurs sur la page **Paramètres utilisateur d’approbation**. Pour le type d’approbateur **Groupe d’utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d’utilisateurs du flux de travail** et définissez la hiérarchie en affectant des numéros incrémentiels à chaque approbateur dans le champ **N° séquence** . Pour plus d’informations, reportez-vous à cette rubrique et à [Configurer des utilisateurs de workflow](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Configurer un utilisateur approbation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres utilisateur approbation**, puis choisissez le lien associé.  
2. Créez une ligne sur la page **Paramètres utilisateur d’approbation**, puis renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code utilisateur**|Sélectionnez le code de l’utilisateur impliqué dans le processus d’approbation.|  
    |**Code vendeur/acheteur**|Spécifiez le code vendeur ou acheteur qui s’applique à l’utilisateur dans le champ **Code vendeur/acheteur**.<br /><br /> En général, vous remplissez le champ **Code vendeur/acheteur** si le vendeur ou l’acheteur responsable pour le client ou le fournisseur, est aussi la personne qui doit approuver la demande vente ou achat en question.|  
    |**ID approbateur**|Sélectionnez le code d’utilisateur qui doit approuver des demandes effectuées par l’utilisateur dans le champ **ID utilisateur**.|  
    |**Montant maximal vente autorisé**|Spécifiez le montant de vente maximal en DS qui peut être approuvé par l’utilisateur dans le champ **ID utilisateur**.|  
    |**Montant illimité de vente autorisé**|Spécifiez que l’utilisateur dans le champ **ID utilisateur** peut approuver toutes les demandes vente quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal vente autorisé**.|  
    |**Montant maximal achat autorisé**|Spécifiez le montant d’achat maximal en DS qui peut être approuvé par l’utilisateur dans le champ **ID utilisateur**.|  
    |**Montant illimité d’achat autorisé**|Spécifiez que l’utilisateur dans le champ **ID utilisateur** peut approuver toutes les demandes achat quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal vente autorisé**.|  
    |**Montant maximal demande achat autorisé**|Spécifiez le montant maximal en DS qui peut être approuvé par l’utilisateur pour les devis d’achat dans le champ **ID utilisateur**.<br /><br /> Pour utiliser ce champ, vous devez sélectionner l’option **Chaîne d’approbateurs** dans le champ **Type limite approbateur** sur la page **Réponse de flux de travail**.|  
    |**Montant illimité de demande d’achat autorisé**|Spécifiez que l’utilisateur dans le champ **ID utilisateur** peut approuver tous les devis d’achat quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal demande achat autorisé**.|  
    |**Remplaçant**|Sélectionnez le code d’utilisateur qui doit approuver des demandes effectuées par l’utilisateur dans le champ **ID utilisateur** si l’utilisateur dans le champ **ID approbateur** n’est pas disponible. <br /><br />**Note :** le remplaçant peut être soit l’utilisateur dans le champ **Remplaçant**, l’approbateur direct, soit l’administrateur d’approbation, dans cet ordre de priorité. Pour plus d’informations, reportez-vous à [Utilisation des flux d’approbation](across-how-use-approval-workflows.md).|  
    |**Adresse de messagerie**|Spécifiez l’adresse de messagerie de l’utilisateur dans le champ **ID utilisateur**.|  
    |**Administrateur approbation**|Spécifiez l’utilisateur qui a des autorisations de débloquer des workflows d’approbation, par exemple, en déléguant les demandes d’approbation à de nouveaux approbateurs remplaçants et en supprimant des demandes d’approbation échues.|

    > [!Note]
    > Une seule personne peut être l’administrateur d’approbation.

3. Pour test le paramétrage utilisateur approbation, choisissez l’action **Tester paramètres utilisateur approbation**.  
4. Répétez les étapes 2 et 3 pour chaque utilisateur que vous souhaitez configurer en tant qu’utilisateur approbation.  

## <a name="see-also"></a>Voir aussi

[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)   
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)   
[Créer des workflows](across-how-to-create-workflows.md)   
[Paramétrage des workflows](across-set-up-workflows.md)   
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Flux de travail](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]