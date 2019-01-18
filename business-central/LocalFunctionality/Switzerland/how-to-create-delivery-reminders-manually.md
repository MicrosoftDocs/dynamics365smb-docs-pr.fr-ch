---
title: "Procédure : créer manuellement des relances livraison"
description: "Dans Business Central, vous pouvez créer des relances livraison lorsqu'un achat n'a pas été envoyé comme prévu. Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 47f646f21495951f1eb7382fb91e4b69e9dd6129
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="create-delivery-reminders-manually"></a>Créer manuellement des relances livraison
Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez créer des relances livraison lorsqu'un achat n'a pas été envoyé comme prévu. Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues. Pour plus d'informations, voir [Générer des relances livraison](how-to-generate-delivery-reminders.md).

> [!NOTE]
> Pour créer des relances livraison, vous devez configurer les propriétés de relance livraison. Pour plus d'informations, voir [Configurer des relances livraison](how-to-set-up-delivery-reminders.md).

## <a name="to-create-a-delivery-reminder-manually"></a>Pour créer une relance livraison manuellement  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Relance livraison**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Dans la page **Relance livraison**, sur le raccourci **Général**, renseignez les champs comme indiqué dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N°**|Numéro d'identification unique de la relance livraison.|  
    |**N° fournisseur**|Numéro du fournisseur pour lequel vous souhaitez publier la relance livraison.<br /><br /> Lorsque vous sélectionnez le numéro de fournisseur, les champs **Nom**, **Adresse**, **CP/Ville** et **Contact** sont renseignés automatiquement.|  
    |**Date de validation**|Date de validation de la relance livraison. Cette date est copiée dans toutes les écritures comptables de la relance livraison.|  
    |**Date document**|Date du document de la relance livraison. Cette date est également utilisée pour calculer la date d'échéance pour la relance livraison. Vous pouvez modifier la date de validation, le cas échéant.|  
    |**Niveau relance**|Niveau de relance livraison. Cette valeur est basée sur le nombre de relances livraison déjà envoyées. Pour plus d'informations, voir [Configurer les conditions, niveaux et textes de relance livraison](how-to-set-up-delivery-reminder-terms-levels-and-text.md).|  
    |**Code condition relance**|Spécifiez le code condition relance livraison qui est paramétré pour le fournisseur.|  
    |**Date d'échéance**|Date d'échéance de la relance livraison.|  

4.  Choisissez l'action **Proposer lignes relance**  

    S'il existe des livraisons échues du fournisseur spécifié, ces dernières sont ajoutées à la relance livraison.  

5.  Cliquez sur le bouton **OK**.  

    La relance livraison est créée. Vous pouvez alors émettre et imprimer la relance livraison.  

## <a name="see-also"></a>Voir aussi  
 [relances livraison](delivery-reminders.md)   
 [Générer des relances livraison](how-to-generate-delivery-reminders.md)   
 [Configurer des relances livraison](how-to-set-up-delivery-reminders.md)   
 [Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Émettre des relances livraison](how-to-issue-delivery-reminders.md)   
 [Imprimer des rapports de test pour les relances livraison](how-to-print-test-reports-for-delivery-reminders.md)

