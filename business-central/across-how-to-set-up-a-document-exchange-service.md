---
title: Procédure de configuration d'un service d'échange de document | Microsoft Docs
description: Utilisez un fournisseur de services externe pour échanger des documents électroniques avec vos partenaires commerciaux.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a9bba4d097ca24de094f153c91d7888811cdfd4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241207"
---
# <a name="set-up-a-document-exchange-service"></a>Configurer un service d'échange de document
Utilisez un fournisseur de services externe pour échanger des documents électroniques avec vos partenaires commerciaux. Pour plus d'informations, voir [Échanger des données par voir électronique](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Pour configurer un service d'échange de documents  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres service Doc. Exch.**, puis sélectionnez le lien associé.  
2. Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Agent utilisateur**|Entrez tout texte que vous pouvez utiliser pour identifier votre société dans les processus d'échange de documents.|  
    |**ID abonné Doc. Exch.**|Entrez l'abonné dans le service d'échange de documents qui représente votre société. Elle est fournie par le fournisseur de services d'échange de documents.|  
    |**Activé**|Spécifiez si le service est activé. **Note :** dès que vous activez le service, au moins deux écritures file projet sont créées pour traiter le trafic de documents électroniques dans et hors de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lorsque vous désactivez le service, les écritures de file projets sont supprimées.|  
    |**URL inscription**|Spécifiez la page Web sur laquelle vous vous êtes connecté au service d'échange de documents.|  
    |**URL service**|Spécifiez l'adresse du service d'échange de documents qui sera appelé lorsque vous envoyez ou recevez des documents électroniques.|  
    |**URL connexion**|Spécifiez la page de connexion au service d'échange de documents, c'est-à-dire l'emplacement où vous saisissez le nom de l'utilisateur et le mot de passe de votre société pour vous connecter au service.|  
    |**Clé consommateur**|Entrez la clé OAuth à 3 branches pour la clé consommateur. Elle est fournie par le fournisseur de services d'échange de documents.|  
    |**Clé secrète du consommateur**|Entrez la clé secrète qui protège la clé consommateur. Elle est fournie par le fournisseur de services d'échange de documents.|  
    |**Jeton**|Entrez la clé OAuth à 3 branches pour le token. Elle est fournie par le fournisseur de services d'échange de documents.|  
    |**Clé secrète du jeton**|Entrez le secret qui protège le token. Elle est fournie par le fournisseur de services d'échange de documents.|  

    > [!NOTE]  
    > Vos données de connexion sont automatiquement chiffrées.

## <a name="see-also"></a>Voir aussi  
[Configuration de l'échange de données](across-set-up-data-exchange.md)  
[Échanger des données par voir électronique](across-data-exchange.md)
