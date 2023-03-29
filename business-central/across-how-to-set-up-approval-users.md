---
title: Configurer des utilisateurs d’approbation
description: 'Avant de pouvoir créer des flux de travail qui impliquent des étapes d’approbation, vous devez configurer les utilisateurs du flux de travail qui sont impliqués dans les processus d’approbation sur la page Paramètres utilisateur approbation.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
---
# Configurer des utilisateurs d’approbation

Avant de pouvoir créer des flux de travail qui impliquent des étapes d’approbation, vous devez configurer les utilisateurs du flux de travail qui sont impliqués dans les processus d’approbation. Sur la page **Paramètres utilisateur d’approbation**, vous pouvez également définir les limites pour des types spécifiques de demandes et définir des approbateurs remplaçants à qui des demandes d’approbation sont déléguées lorsque l’approbateur initial est absent.  

> [!NOTE]  
> Les utilisateurs d’approbation, à la fois demandeurs d’approbation et approbateurs, doivent d’abord être définis comme utilisateurs du flux de travail sur la page **Groupe d’utilisateurs du flux de travail**. En savoir plus sur [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md).  

Lorsque vous configurez des utilisateurs approbation, vous pouvez créer de réponses du flux de travail pour des flux de travail approbation. En savoir plus à partir de l’étape 9 sur [Créer des flux de travail approbation](across-how-to-create-workflows.md).  

> [!NOTE]  
> Pour indiquer qu’une demande d’approbation n’est pas approuvée tant que plusieurs utilisateurs dans une chaîne d’approbation ne l’ont pas approuvée, configurez les approbateurs selon une hiérarchie. Pour le type d’approbateur **Approbateur**, configurez les approbateurs sur la page **Paramètres utilisateur d’approbation**. Pour le type d’approbateur **Groupe d’utilisateurs de flux de travail**, configurez les approbateurs sur la page **Groupe d’utilisateurs du flux de travail** et définissez la hiérarchie en affectant des numéros incrémentiels à chaque approbateur dans le champ **N° séquence** . En savoir plus sur [Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md).  

## Configurer un utilisateur approbation

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres utilisateur approbation**, puis choisissez le lien associé.  
2. Créez une ligne sur la page **Paramètres utilisateur d’approbation**, puis renseignez les champs comme indiqué dans le tableau suivant.  

   |Champ|Désignation|
   |-----|-----------|
   |**Code utilisateur**|Sélectionnez le code de l’utilisateur impliqué dans le processus d’approbation.|
   |**Code vendeur/acheteur**|Spécifiez le code vendeur ou acheteur qui s’applique à l’utilisateur.<br /><br /> En général, vous remplissez le champ **Code vendeur/acheteur** si le vendeur ou l’acheteur responsable pour le client ou le fournisseur, est aussi la personne qui doit approuver la demande vente ou achat en question.|
   |**ID approbateur**|Sélectionnez le code d’utilisateur qui doit approuver des demandes effectuées par l’utilisateur dans le champ **ID utilisateur**.|
   |**Montant maximal vente autorisé**|Spécifiez le montant de vente maximal en devise locale (DS) qui peut être approuvé par l’utilisateur dans le champ **ID utilisateur**.|
   |**Montant illimité de vente autorisé**|Spécifiez que l’utilisateur dans le champ **ID utilisateur** peut approuver toutes les demandes vente quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal vente autorisé**.|
   |**Montant maximal achat autorisé**|Spécifiez le montant d’achat maximal en DS qui peut être approuvé par l’utilisateur pour les devis d’achat dans le champ **ID utilisateur**.|
   |**Montant illimité d’achat autorisé**|Spécifiez que l’utilisateur dans le champ **ID utilisateur** peut approuver toutes les demandes achat quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal achat autorisé**.|
   |**Montant maximal demande achat autorisé**|Spécifiez le montant maximal en DS qui peut être approuvé par l’utilisateur pour les devis d’achat dans le champ **ID utilisateur**.<br /><br /> Pour utiliser ce champ, vous devez sélectionner l’option **Chaîne d’approbateurs** dans le champ **Type limite approbateur** sur la page **Réponse de flux de travail**.|
   |**Montant illimité de demande d’achat autorisé**|Spécifiez que l’utilisateur dans le champ **ID utilisateur** peut approuver tous les devis achat quel que soit leur montant.<br /><br /> Si vous cochez cette case, vous ne pouvez pas renseigner le champ **Montant maximal demande achat autorisé**.|
   |**Remplaçant**|Sélectionnez le code d’utilisateur qui doit approuver des demandes effectuées par l’utilisateur dans le champ **ID utilisateur** si l’utilisateur dans le champ **ID approbateur** n’est pas disponible. <br /><br />**Note :** le remplaçant peut être soit l’utilisateur dans le champ **Remplaçant**, l’approbateur direct, soit l’administrateur d’approbation, dans cet ordre de priorité. En savoir plus sur [Utiliser des flux de travail approbation](across-how-use-approval-workflows.md).|
   |**Adresse de messagerie**|Spécifiez l’adresse de messagerie de l’utilisateur dans le champ **ID utilisateur**.|
   |**Administrateur approbation**|Spécifiez l’utilisateur qui a des autorisations de débloquer des flux de travail approbation, par exemple, en déléguant les demandes d’approbation à de nouveaux approbateurs remplaçants et en supprimant des demandes d’approbation échues.|

   > [!NOTE]
   > Une seule personne peut être l’administrateur d’approbation.

3. Pour test le paramétrage utilisateur approbation, choisissez l’action **Tester paramètres utilisateur approbation**.  
4. Répétez les étapes 2 et 3 pour chaque utilisateur que vous souhaitez configurer en tant qu’utilisateur approbation.  

## Voir la [formation Microsoft](/training/modules/create-workflows/) associée

## Voir aussi

[Configurer des utilisateurs de flux de travail](across-how-to-set-up-workflow-users.md)  
[Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md)  
[Créer des flux de travail approbation](across-how-to-create-workflows.md)  
[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Procédure pas à pas : Configuration et utilisation d’un flux d’approbation d’achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Flux de travail](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
