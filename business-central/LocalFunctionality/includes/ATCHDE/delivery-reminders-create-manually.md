---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df06e45136e3ab948fb6ca090c84d10609b76f45
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747545"
---
Dans [!INCLUDE[prod_short](../../../includes/prod_short.md)], vous pouvez créer des relances livraison lorsqu'un achat n'a pas été livré comme prévu. Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues.  

> [!NOTE]
> Pour créer des relances livraison, vous devez avoir configuré les conditions, les niveaux et les textes des relances livraison.

## <a name="to-create-a-delivery-reminder-manually"></a>Pour créer une relance livraison manuellement  

1. Choisissez l'icône ![Icône Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Relance livraison**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3. Sur la page **Relance livraison**, renseignez les champs comme décrit dans le tableau ci-dessous.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N°**|Numéro d'identification unique de la relance livraison.|  
    |**N° fournisseur**|Numéro du fournisseur pour lequel vous souhaitez publier la relance livraison.<br /><br /> Lorsque vous sélectionnez le numéro de fournisseur, les champs **Nom**, **Adresse**, **CP/Ville** et **Contact** sont renseignés automatiquement.|  
    |**Date de validation**|Date de validation de la relance livraison. Cette date est copiée dans toutes les écritures comptables de la relance livraison.|  
    |**Date document**|Date du document de la relance livraison. Cette date est également utilisée pour calculer la date d'échéance pour la relance livraison. Vous pouvez modifier la date de validation, le cas échéant.|  
    |**Niveau relance**|Niveau de relance livraison. Cette valeur est basée sur le nombre de relances livraison déjà envoyées.|  
    |**Code condition relance**|Spécifiez le code condition relance livraison qui est paramétré pour le fournisseur.|  
    |**Date d'échéance**|Date d'échéance de la relance livraison.|  

4. Choisissez l'action **Proposer lignes relance**.  

    S'il existe des livraisons échues du fournisseur spécifié, ces dernières sont ajoutées à la relance livraison.  

5. Cliquez sur le bouton **OK**.  

    La relance livraison est créée. Vous pouvez alors émettre et imprimer la relance livraison.  
