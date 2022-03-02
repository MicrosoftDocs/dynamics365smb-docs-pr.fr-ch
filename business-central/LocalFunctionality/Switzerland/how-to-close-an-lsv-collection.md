---
title: Fermer un prélèvement LSV [CH]
description: Vous devez fermer les collections Lastschrift Verfahren (LSV+) pour écrire les fichiers LSV qui peuvent être envoyés à la banque pour le prélèvement des paiements.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 3010830, 3010831, 3010832,3010834, 3010835
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: 5e6d78d3c38866e877acfc5cd87e8827027ae480
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146003"
---
# <a name="close-an-lsv-collection-in-the-swiss-version"></a>Fermer un prélèvement LSV dans la version suisse
Vous devez fermer les collections Lastschrift Verfahren (LSV+) pour écrire les fichiers LSV qui peuvent être envoyés à la banque pour le prélèvement des paiements. Lorsque vous fermez un prélèvement, le prélèvement est terminé et les validations dans la feuille LSV sont combinées.  

Lorsque le prélèvement est terminé, le numéro de prélèvement actuel est affecté dans la feuille LSV, en fonction du dernier prélèvement. Ce numéro LSV est transféré vers les écritures client pour toutes les factures ouvertes. Le fichier de prélèvement peut être reconstruit à tout moment en utilisant le numéro LSV. Le champ **En attente** est également renseigné avec **LSV** dans les écritures client pour éviter de dupliquer des écritures ouvertes. Pour plus d'informations, voir la table **Feuille LSV** et la table **Écriture comptable client**. Vous pouvez également rouvrir un prélèvement clôturé.  

## <a name="to-close-an-lsv-collection"></a>Pour fermer un prélèvement LSV  

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Liste feuilles LSV**, puis sélectionnez le lien associé.  
2.  Sélectionnez la ligne feuille requise, puis sélectionnez l'action **Modifier la date comptabilisation**. La valeur du champ **Date de crédit** à l'aide de la valeur suggérée lors du prélèvement LSV.  
3.  Dans le champ **Nouvelle date**, saisissez la nouvelle date.  
4.  Choisissez *l'action *Clôturer le prélèvement**.  

    > [!NOTE]  
    >  Les champs du raccourci **Options** pour le traitement par lots **Prélèvement de fin LSV** ne peuvent pas être modifiés, et correspondent à la ligne feuille sélectionnée.  

5.  Choisissez le bouton **OK**.  

    Dans la page **Liste feuilles LSV**, la valeur du champ **Statut LSV** passe de **Modifier** à **Lancé**. Les lignes feuille ne peuvent plus être modifiées.  

## <a name="to-reopen-an-lsv-collection"></a>Pour rouvrir un prélèvement LSV  

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Liste feuilles LSV**, puis sélectionnez le lien associé.  
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