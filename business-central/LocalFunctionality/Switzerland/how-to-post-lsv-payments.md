---
title: "Procédure\_: Valider les paiements LSV+"
description: Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '3010830, 3010831, 3010832,3010834, 3010835'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="post-lsv-payments" />Valider les paiements LSV+
Vous pouvez valider les paiements après avoir reçu l'avis de paiement Lastschrift Verfahren (LSV+) de la banque.  

## <a name="to-post-lsv-payments" />Pour valider les paiements LSV+

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Feuilles règlement**, puis sélectionnez le lien associé.  
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

## <a name="see-also" />Voir aussi
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md)   
 [Fermer un prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
