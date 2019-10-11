---
title: 'Procédure : Exporter des paiements en mode LSV'
description: Vous pouvez exporter ou écrire des fichiers Lastschrift Verfahren (LSV +) contenant des informations sur les paiements après la fermeture du prélèvement LSV. Vous pouvez envoyer les fichiers générés à la banque sur un disque, ou utiliser un transfert de fichiers électronique tel que votre logiciel de banque en ligne ou un portail Internet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8bf948ec9440e22a30b2cc549b81d404d5e303e8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301059"
---
# <a name="export-payments-using-lsv"></a>Exporter des paiements en mode LSV
Vous pouvez exporter ou écrire des fichiers Lastschrift Verfahren (LSV +) contenant des informations sur les paiements après la fermeture du prélèvement LSV. Vous pouvez envoyer les fichiers générés à la banque sur un disque, ou utiliser un transfert de fichiers électronique tel que votre logiciel de banque en ligne ou un portail Internet.  

## <a name="to-export-payments-using-lsv"></a>Pour exporter des paiements en mode LSV  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Liste feuilles LSV**, puis sélectionnez le lien connexe.  
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
 [Fermer prélèvement LSV](how-to-close-an-lsv-collection.md)   
 [Valider les paiements LSV+](how-to-post-lsv-payments.md)
