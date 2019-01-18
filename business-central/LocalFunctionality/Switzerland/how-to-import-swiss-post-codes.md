---
title: "Procédure : Importer les codes postaux suisses"
description: "Vous pouvez réimporter le dernier fichier des codes postaux et l'utiliser pour mettre la table **Code postal** à jour. Le fichier Code postal peut être téléchargé du site Web de la Poste suisse. Après avoir importé le dernier code postal, vous pouvez définir des codes postaux pour des clients ou des fournisseurs."
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
ms.openlocfilehash: 9b3bdba62eae9a95152da2dada7ed5b70ce974e8
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="import-swiss-post-codes"></a>Importer les codes postaux suisses
Vous pouvez réimporter le dernier fichier des codes postaux et l'utiliser pour mettre la table **Code postal** à jour. Le fichier Code postal peut être téléchargé du site Web de la [Poste suisse](https://go.microsoft.com/fwlink/?LinkId=150292). Après avoir importé le dernier code postal, vous pouvez définir des codes postaux pour des clients ou des fournisseurs. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux fournisseurs](../../purchasing-how-register-new-vendors.md).  

## <a name="to-import-post-codes"></a>Pour importer des codes postaux  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Codes postaux**, puis sélectionnez le lien connexe.  
2.  Sélectionnez l'action **Importer codes postaux**.  
3.  Dans la page **Importer codes postaux**, dans le champ **Nom fichier**, entrez le nom du fichier Code postal que vous souhaitez importer avec la table **Code postal**.  
4.  Cliquez sur le bouton **OK**.  

    Les dernières informations de code postal sont importées.  

La procédure suivante décrit comment définir les codes postaux pour les clients, mais les mêmes étapes s'appliquent également pour définir les codes postaux pour les fournisseurs.  

## <a name="to-define-post-codes-for-customers"></a>Pour définir des codes postaux pour les clients  

1.  Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.  
2.  Sélectionnez le client pour lequel vous souhaitez définir un code postal, puis sélectionnez l'action **Modifier**.  
3.  Dans la page **Fiche client**, dans le raccourci **Général**, dans le champ **Code postal**, sélectionnez le code postal pour l'adresse du client.  

    > [!NOTE]  
    >  Lorsque vous sélectionnez le code postal, les champs **Ville** et **Code pays/région** fournissent automatiquement des informations dans la table **Code postal**. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](../../sales-how-register-new-customers.md).  

4.  Cliquez sur le bouton **OK**.  

## <a name="see-also"></a>Voir aussi   
 [Documents vente et Documents achat, Suisse](swiss-purchase-documents-and-sales-documents.md)   
 [Imprimer la liste des prélèvements de stock d'une commande vente](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [Imprimer les commandes achat et vente lors d'une validation par lots](how-to-print-sales-and-purchase-orders-during-batch-posting.md)   
 [Enregistrer un nouveau fournisseur](../../purchasing-how-register-new-vendors.md)  

