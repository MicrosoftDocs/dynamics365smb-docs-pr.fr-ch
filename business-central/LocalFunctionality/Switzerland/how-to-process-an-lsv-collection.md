---
title: "Procédure : Traiter un prélèvement LSV"
description: "Vous pouvez utiliser **Feuilles LSV** pour créer et traiter les paiements des clients Lastschrift Verfahren (LSV+). Vous pouvez enregistrer les paiements dans la feuille règlement, créer un fichier LSV, puis imprimer l'ordre de prélèvement."
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
ms.openlocfilehash: f447e0c20081cf64709e14cbe524d80fd8075b1c
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="process-an-lsv-collection"></a>Traiter un prélèvement LSV
Vous pouvez utiliser **Feuilles LSV** pour créer et traiter les paiements des clients Lastschrift Verfahren (LSV+). Vous pouvez enregistrer les paiements dans la feuille règlement, créer un fichier LSV, puis imprimer l'ordre de prélèvement. Pour plus d'informations, voir la page Feuille règlement et [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md).  

Lorsque vous lancez le traitement par lots **Proposition de prélèvement LSV**, chaque prélèvement proposé est enregistrée sur une ligne feuille LSV, et les factures ouvertes sont transférées aux feuilles LSV. Pour plus d'informations, voir la table Feuille LSV.  

Vous pouvez afficher, modifier ou supprimer les lignes paiement proposées. Si vous corrigez le montant proposé, la différence est marquée sous la forme d'une remise. Vous pouvez exécuter le traitement par lots plusieurs fois pour différents groupes de clients. Les lignes de suggestion peuvent être placées sur la même feuille.  

## <a name="to-create-an-lsv-collection"></a>Pour créer un prélèvement LSV  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Liste feuilles LSV**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Nouveau**.  
3.  Dans la page **Liste feuilles LSV**, renseignez les champs requis comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Code banque LSV**|Sélectionnez le code banque LSV pour la banque qui procèdera au prélèvement.|  
    |**Description de la feuille LSV**|Permet de saisir une description pour l'écriture.|

4.  Sélectionnez l'écriture feuille LSV requise, puis sélectionnez l'action **Proposition de prélèvement LSV** pour créer les paiements de prélèvement automatique par LSV+.  
5.  Dans la page **Proposition de prélèvement LSV**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N°**|Entrez le numéro de feuille LSV.|  
    |**Date d'échéance début**|Spécifiez la date d'échéance début des écritures ouvertes à proposer pour le prélèvement.|  
    |**Date d'échéance fin**|Spécifiez la date d'échéance fin des écritures ouvertes à proposer pour le prélèvement.|  
    |**Date de prélèvement**|Spécifiez la date à laquelle le prélèvement est clôturé. L'ordre LSV+ doit être envoyé au moins trois jours bancaires avant la date de prélèvement.|  

6.  Cliquez sur le bouton **OK**.  

Toutes les lignes sont été transférées à la feuille LSV. Après avoir effectué le prélèvement LSV, vous pouvez visualiser, vérifier ou modifier les paiements proposés dans la page **Feuille LSV**. Pour plus d'informations, voir la table Ligne feuille LSV.  

## <a name="to-manage-suggested-payments"></a>Pour gérer les paiements proposés  

1.  Dans la page **Liste feuilles LSV**, sélectionnez l'écriture feuille requise, puis sélectionnez l'action **Ligne feuille LSV**.  

    Vous pouvez visualiser et modifier les paiements proposés dans cette page. Vous pouvez saisir les paiements requis manuellement. Pour les nouvelles lignes feuille, le champ **Statut LSV** est défini sur **Ouvrir** pour indiquer que la facture est impayée.  

3.  Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Fermer prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Valider des paiements LSV+](how-to-post-lsv-payments.md)   
 [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md)

