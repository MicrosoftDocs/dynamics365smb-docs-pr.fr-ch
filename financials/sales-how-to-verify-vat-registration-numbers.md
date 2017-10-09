---
title: "Procédure : Vérifier les numéros d'identification intracomm. | Microsoft Docs"
description: "Vous pouvez utiliser un service Web UE pour vérifier que les numéros d'identification intracomm. saisis sur les fiches client, fournisseur ou contact sont valides."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Procédure : Vérifier les numéros d'identification intracomm.
Vous pouvez utiliser un service Web UE pour vérifier que les numéros d'identification intracomm. saisis sur les fiches client, fournisseur ou contact sont valides.  

 Lorsque vous modifiez le champ **N° identif. intracomm.**d'une fiche pour laquelle la valeur du champ **Code pays/région** est un pays ou une région de l'UE, le nouveau numéro d'identification intra-communautaire et votre code utilisateur sont consignés dans la fenêtre **Journal identif. intracomm.**. Vous vérifiez un numéro d'identification intracomm. en choisissant le bouton **Vérifier n° d'identification** de la fenêtre **Journal identif. intracomm.**. Une nouvelle ligne est créée chaque fois que vous utilisez la fonction de vérification. Si le numéro a pu être vérifié, le champ **Statut** indique **Valide**. Si le numéro n'a pu être vérifié, le champ **Statut** indique **Non valide**, et vous devez modifier le numéro dans le champ **N° identif. intracomm.** de la fiche et lancer une nouvelle fois la fonction de vérification.  

 L'URL du service Web par défaut est définie dans le champ **URL de validation de n° id. intracomm.** dans la fenêtre **Paramètres comptabilité**.  

 Dans le tableau **Format n° identif. intracomm.**, vous pouvez modifier pour chaque pays/région les différents formats du numéro d'identification intracomm. que les utilisateurs sont autorisés à saisir dans le champ **N° identif. intracomm.**  

> [!WARNING]  
>  Ce service Web utilise le protocole http, ce qui signifie que les données transférées à travers le service ne sont pas cryptées.  

> [!NOTE]  
>  Vous pouvez rencontrer des temps d'arrêt pour ce service dont Microsoft n'est pas responsable, étant donné que le service fait partie d'un vaste réseau de l'UE de registres de TVA nationaux.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>Pour vérifier un numéro d'identification intracomm. à partir d'une fiche client  
Les informations ci-dessous décrivent comment vérifier le numéro d'identification intracommunautaire d'un client. La procédure est identique pour un fournisseur ou un contact.   
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.  

2.  Ouvrez la fiche d'un client sur laquelle vous souhaitez vérifier le numéro d'identification intracomm.  

    > [!NOTE]  
    >  Le champ **Code pays/région** de la fiche client doit contenir un pays/une région de l'UE.  
3.  Dans le raccourci **Facturation**, cliquez sur le bouton de zoom en regard du champ **N° identif. intracomm.**  

    La fenêtre **Journal identif. intracomm.** s'ouvre en affichant une ligne sur laquelle le champ **Statut** indique **Non vérifié**.  
4.  Choisissez l'action **Vérifier n° d'identification**.  

     Une nouvelle ligne est créée si le champ **Statut** indique **Valide** ou **Non valide**.  
5.  Si le champ **Statut** indique **Non valide**, modifiez le numéro dans le champ **N° identif. intracomm.** sur la fiche, puis répétez les étapes 3 à 4.  

## <a name="see-also"></a>Voir aussi  
[Finances](finance.md)  
[Procédure : enregistrer de nouveaux clients](sales-how-register-new-customers.md)  
[Procédure : enregistrer de nouveaux fournisseurs](purchasing-how-register-new-vendors.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

