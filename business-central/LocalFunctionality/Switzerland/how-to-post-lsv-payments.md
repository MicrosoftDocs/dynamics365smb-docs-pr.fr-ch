---
title: "Procédure : Valider les paiements LSV+"
description: "Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 26fa934e00b380b7416417f2a1d37e7bde4a5098
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-lsv-payments"></a>Valider les paiements LSV+
Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.  

## <a name="to-post-lsv-payments"></a>Pour valider les paiements LSV+  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles règlement**, puis sélectionnez le lien connexe.  
2.  Sélectionnez la feuille requise, puis cliquez sur l'action **Modifier journal**.  

    > [!NOTE]  
    >  Vous pouvez sélectionner le nom de feuille pour LSV dans laquelle le compte contrepartie concerné est défini. Vous ne pouvez pas importer plusieurs fichiers lignes feuille LSV dans la même feuille règlement. Pour plus d'informations, reportez-vous à la fenêtre Feuille règlement.  

3.  Sélectionnez l'action **Obtenir à partir de la feuille LSV**.  
4.  Dans la fenêtre **Liste feuilles LSV**, sélectionnez la ligne feuille LSV que vous souhaitez importer avec la feuille règlement.  

    > [!NOTE]  
    >  Vous pouvez importer uniquement des lignes feuille où le champ **Statut LSV** est défini sur **Fichier créé**.  

5.  Cliquez sur le bouton **OK**.  

    La ligne feuille LSV est importée dans la feuille règlement. La valeur du champ **Statut LSV** dans la fenêtre **Liste feuilles LSV** passe de **Fichier créé** à **Terminé**.  

    Vous pouvez vérifier les paiements importés et les comparer à votre option de paiement bancaire dans la fenêtre **Feuille règlement**. Vous pouvez également supprimer les lignes paiement qui ne peuvent pas être traitées par la banque, et pour lesquelles vous devez continuer avec le client manuellement.  

6.  Sélectionnez l'action **Valider**.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md)   
 [Fermer prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md) 

