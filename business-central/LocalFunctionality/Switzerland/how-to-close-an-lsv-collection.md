---
title: 'Procédure : Fermer un prélèvement LSV'
description: Vous devez fermer les collections Lastschrift Verfahren (LSV+) pour écrire les fichiers LSV qui peuvent être envoyés à la banque pour le prélèvement des paiements. Lorsque vous fermez un prélèvement, le prélèvement est terminé et les validations dans la feuille LSV sont combinées.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c850eca99de389f9750e3bc2f7fc0d8a72c4a1cf
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775704"
---
# <a name="close-an-lsv-collection"></a>Fermer prélèvement LSV
Vous devez fermer les collections Lastschrift Verfahren (LSV+) pour écrire les fichiers LSV qui peuvent être envoyés à la banque pour le prélèvement des paiements. Lorsque vous fermez un prélèvement, le prélèvement est terminé et les validations dans la feuille LSV sont combinées.  

Lorsque le prélèvement est terminé, le numéro de prélèvement actuel est affecté dans la feuille LSV, en fonction du dernier prélèvement. Ce numéro LSV est transféré vers les écritures client pour toutes les factures ouvertes. Le fichier de prélèvement peut être reconstruit à tout moment en utilisant le numéro LSV. Le champ **En attente** est également renseigné avec **LSV** dans les écritures client pour éviter de dupliquer des écritures ouvertes. Pour plus d'informations, voir la table **Feuille LSV** et la table **Écriture comptable client**. Vous pouvez également rouvrir un prélèvement clôturé.  

## <a name="to-close-an-lsv-collection"></a>Pour fermer un prélèvement LSV  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste feuilles LSV**, puis sélectionnez le lien associé.  
2.  Sélectionnez la ligne feuille requise, puis sélectionnez l'action **Modifier la date comptabilisation**. La valeur du champ **Date de crédit** à l'aide de la valeur suggérée lors du prélèvement LSV.  
3.  Dans le champ **Nouvelle date**, saisissez la nouvelle date.  
4.  Choisissez *l'action *Clôturer le prélèvement**.  

    > [!NOTE]  
    >  Les champs du raccourci **Options** pour le traitement par lots **Prélèvement de fin LSV** ne peuvent pas être modifiés, et correspondent à la ligne feuille sélectionnée.  

5.  Choisissez le bouton **OK**.  

    Dans la page **Liste feuilles LSV**, la valeur du champ **Statut LSV** passe de **Modifier** à **Lancé**. Les lignes feuille ne peuvent plus être modifiées.  

## <a name="to-reopen-an-lsv-collection"></a>Pour rouvrir un prélèvement LSV  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste feuilles LSV**, puis sélectionnez le lien associé.  
2.  Sélectionnez la ligne feuille appropriée pour laquelle vous voulez rouvrir le prélèvement, choisissez l'action **Rouvrir le prélèvement**.  

    > [!NOTE]  
    >  Vous ne pouvez rouvrir le prélèvement que si vous n'avez pas encore envoyé le fichier LSV+ à la banque.  

3.  Choisissez le bouton **Oui** pour confirmer la réouverture du prélèvement.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md)   
 [Valider des paiements LSV+](how-to-post-lsv-payments.md)   
 [Exporter des paiements en mode LSV](how-to-export-payments-using-lsv.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]