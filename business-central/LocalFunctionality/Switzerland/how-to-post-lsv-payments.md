---
title: 'Procédure : Valider les paiements LSV+'
description: Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.
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
ms.openlocfilehash: f8dc03d4b11a14f442901ed40375467e9b8bf210
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "934063"
---
# <a name="post-lsv-payments"></a>Valider les paiements LSV+
Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.  

## <a name="to-post-lsv-payments"></a>Pour valider les paiements LSV+  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuilles règlement**, puis sélectionnez le lien connexe.  
2.  Sélectionnez la feuille requise, puis cliquez sur l'action **Modifier journal**.  

    > [!NOTE]  
    >  Vous pouvez sélectionner le nom de feuille pour LSV dans laquelle le compte contrepartie concerné est défini. Vous ne pouvez pas importer plusieurs fichiers lignes feuille LSV dans la même feuille règlement. Pour plus d'informations, reportez-vous à la page Feuille règlement.  

3.  Sélectionnez l'action **Obtenir à partir de la feuille LSV**.  
4.  Dans la page **Liste feuilles LSV**, sélectionnez la ligne feuille LSV que vous souhaitez importer avec la feuille règlement.  

    > [!NOTE]  
    >  Vous pouvez importer uniquement des lignes feuille où le champ **Statut LSV** est défini sur **Fichier créé**.  

5.  Cliquez sur le bouton **OK**.  

    La ligne feuille LSV est importée dans la feuille règlement. La valeur du champ **Statut LSV** dans la page **Liste feuilles LSV** passe de **Fichier créé** à **Terminé**.  

    Vous pouvez vérifier les paiements importés et les comparer à votre option de paiement bancaire dans la page **Feuille règlement**. Vous pouvez également supprimer les lignes paiement qui ne peuvent pas être traitées par la banque, et pour lesquelles vous devez continuer avec le client manuellement.  

6.  Sélectionnez l'action **Valider**.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md)   
 [Fermer prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md) 
