---
title: Comment émettre des relances livraison dans la version suisse
description: Après avoir créé des relances livraison, vous devez les émettre et les imprimer afin de pouvoir envoyer des relances aux fournisseurs. Avant d'émettre les relances livraison, vous pouvez imprimer un rapport de test.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2020
ms.author: edupont
ms.openlocfilehash: f71107b8b7ca5b259baf17276ab66b0583521a19
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778231"
---
# <a name="issue-delivery-reminders-in-the-swiss-version"></a>Émettre des relances livraison dans la version suisse

Après avoir créé des relances livraison, vous devez les émettre et les imprimer afin de pouvoir les envoyer aux fournisseurs. Avant d'émettre les relances livraison, vous pouvez imprimer un rapport de test. Pour plus d'informations, voir [Imprimer des rapports de test pour les relances livraison](how-to-print-test-reports-for-delivery-reminders.md).  

Lorsque vous émettez les relances livraison, des écritures comptables de relance livraison sont créées. Vous pouvez afficher les écritures comptables créées dans la page **Écritures comptables relance livraison**.  

## <a name="to-issue-delivery-reminders"></a>Pour émettre des relances livraison  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Relance livraison**, puis sélectionnez le lien associé.  
2.  Dans la page **Relance livraison**, sélectionnez la relance livraison que vous souhaitez émettre, puis choisissez l'action **Modifier**.  
3.  Sélectionnez l'action **Émettre**.  
4.  Dans la page **Émettre relance livraison**, sur le raccourci **Options**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Imprimer**|Sélectionnez cette option pour imprimer les relances livraison lorsqu'elles sont émises.|  
    |**Remplacer date comptabilisation**|Sélectionnez cette option pour remplacer la date de comptabilisation existante pour la relance livraison.|  
    |**Date de validation**|Date de validation de la relance livraison.<br /><br /> Cette date de comptabilisation est utilisée pour toutes les relances livraison si vous avez sélectionné la case à cocher **Remplacer date comptabilisation**. Si la case à cocher **Remplacer date comptabilisation** est effacée, cette date ne sera utilisée que pour les relances livraison pour lesquelles une date de comptabilisation n'est pas disponible.|  

5.  Éventuellement, dans le raccourci **En-tête de relance livraison**, sélectionnez les filtres appropriés.  

    > [!NOTE]  
    >  Vous pouvez supprimer les filtres et émettre à nouveau les relances livraison en même temps.  

6.  Choisissez le bouton **OK**.  

Vous pouvez afficher les relances émises dans la page **Relances livraison émises**. En option, vous pouvez maintenant imprimer une relance livraison.  

## <a name="to-view-delivery-reminder-ledger-entries"></a>Pour afficher des écritures comptables de relance livraison  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat**, puis sélectionnez le lien associé.  
2.  Sélectionnez la commande achat pour laquelle vous souhaitez afficher le statut de relance, puis choisissez l'action **Modifier**.  
3.  Sélectionnez l'action **Écritures comptables de relance livraison**.  

Dans la page Écritures comptables de relance livraison, vous pouvez afficher les écritures comptables de relance livraison pour la commande achat sélectionnée.  

## <a name="see-also"></a>Voir aussi  
 [relances livraison](delivery-reminders.md)   
 [Générer des relances livraison](how-to-generate-delivery-reminders.md)   
 [Créer manuellement des relances livraison](how-to-create-delivery-reminders-manually.md)
