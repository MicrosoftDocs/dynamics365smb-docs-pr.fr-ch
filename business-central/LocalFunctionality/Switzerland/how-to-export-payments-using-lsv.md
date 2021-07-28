---
title: 'Procédure : Exporter des paiements en mode LSV [CH]'
description: Vous pouvez exporter ou écrire des fichiers Lastschrift Verfahren (LSV +) contenant des informations sur les paiements après la fermeture du prélèvement LSV.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: 1b38b864adb6c045018d1bd07852320dbdc2c22c
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437172"
---
# <a name="export-payments-using-lsv-in-the-swiss-version"></a>Exporter des paiements en mode LSV dans la version suisse
Vous pouvez exporter ou écrire des fichiers Lastschrift Verfahren (LSV +) contenant des informations sur les paiements après la fermeture du prélèvement LSV. Vous pouvez envoyer les fichiers générés à la banque sur un disque, ou utiliser un transfert de fichiers électronique tel que votre logiciel de banque en ligne ou un portail Internet.  

## <a name="to-export-payments-using-lsv"></a>Pour exporter des paiements en mode LSV  

1.  Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Liste feuilles LSV**, puis sélectionnez le lien associé.  
2.  Dans la page **Liste feuilles LSV**, sélectionnez la feuille LSV nécessaire.  
3.  Choisissez l'action **Écrire le fichier LSV**.  
4.  Dans la page **Écrire le fichier LSV**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N°**|Indiquez le numéro de feuille LSV que vous souhaitez exporter.|  
    |**Test**|Spécifiez si vous envoyez les livraisons test à votre banque. La banque ne traite pas de fichier de test.|  

5.  Toutes les lignes sont été transférées à la feuille LSV. Le fichier LSV est généré dans le dossier prédéterminé.  

## <a name="see-also"></a>Voir aussi  
 [Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md)   
 [Traiter un prélèvement LSV](how-to-process-an-lsv-collection.md)   
 [Fermer un prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Valider les paiements LSV+](how-to-post-lsv-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]