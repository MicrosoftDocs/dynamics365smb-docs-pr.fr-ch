---
title: "Procédure : Configurer l'extension GetAddress.io UK Postcodes | Microsoft Docs"
description: "Décrit la fonctionnalité générale que vous utilisez pour interagir avec des données dans Financials, par exemple entrer les valeurs, trier les données, et modifier les vues."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a>Procédure : Configurer l'extension GetAddress.io UK Postcodes
Cette extension facilite la saisie des adresses au Royaume-Uni pour les entités comme les clients, les contacts, les salariés, les fournisseurs, les comptes bancaires, etc. 

L'extension GetAddress.io UK Postcodes utilise l'API getAddress pour rechercher des adresses dans les codes postaux au Royaume-Uni. Pour utiliser l'extension, vous devez obtenir un plan et une clé API pour l'API getAddress. C'est facile, et nous pouvons vous aider à le faire lorsque vous configurez l'extension GetAddress.io UK Postcodes. Les plans sont basés sur l'utilisation ou sur ce qui est parfois désigné sous le nom d'appels. Un appel, dans ce cas, a lieu lorsque [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche la liste des adresses dans un code postal. Selon la fréquence à laquelle vous ajoutez des adresses, choisissez le plan qui vous convient le mieux. Si vous choisissez **Obtenir clé API** dans la page, vous allez utiliser le plan **Libre**, qui vous permet d'ajouter 20 adresses par jour, et qui est valable 30 jours. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Pour configurer l'extension GetAddress.io UK Postcodes 
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Connexions au service**, puis sélectionnez le lien connexe.  
2. Dans la fenêtre **Connexions au service**, choisissez **Service code postal R-U**.
3. Dans la page **Configuration fournisseur code postal**, choisissez **Désactivé**.
4. Dans la fenêtre **Sélection du service de code postal**, choisissez **GetAddress.io**.
5. Dans la fenêtre **GetAddress.io Config**, choisissez **Obtenir clé API** pour ouvrir la page **Plans** sur le site Web pour obtenir l'API getAddress.  

    > [!NOTE]  
>   Vous pouvez être amené à autoriser les messages contextuels dans votre navigateur.
6. Vous pouvez acheter un plan ou simplement choisir **Obtenir clé API**, et fournir ensuite votre adresse e-mail.
7. Ouvrez l'e-mail à partir de getAddress.io, et copiez la clé d'API. La clé se trouve sous l'en-tête **Votre clé API**.
8. Dans la fenêtre **GetAddress.io Config**, collez la clé API dans le champ **Clé API** et choisissez **OK**.
9. Dans la page **Connexions au service**, vérifiez que le champ **Fournisseur adresse** contient bien **GetAddress.io**. Si c'est le cas, le service est activé.

## <a name="see-also"></a>Voir aussi
[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Personnalisatoin de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
