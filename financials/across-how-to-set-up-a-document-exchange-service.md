---
title: "Procédure de configuration d'un service d'échange de document | Microsoft Docs"
description: "Utilisez un fournisseur de services externe pour échanger des documents électroniques avec vos partenaires commerciaux."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1191313565e813a92c13fa07b6278e7263eeaf19
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-a-document-exchange-service"></a>Procédure : configurer un service d'échange de document
Utilisez un fournisseur de services externe pour échanger des documents électroniques avec vos partenaires commerciaux. Pour plus d'informations, voir [Échange de données en tant que documents électroniques](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Pour configurer un service d'échange de documents  
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Paramètres service Doc. Exch.**, puis sélectionnez le lien connexe.  
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
>  Il est recommandé de protéger les informations de connexion que vous saisissez dans la fenêtre **Paramètres service VAN**. Vous pouvez chiffrer des données sur le serveur en générant de nouvelles clés de chiffrement ou en important des clés existantes que vous activez sur l'instance de serveur qui est connectée à la base de données. Ceci est décrit dans la procédure suivante.  

## <a name="to-encrypt-your-logon-information"></a>Pour chiffrer les informations de connexion  
1. Dans la fenêtre **Paramètres service VAN**, sélectionnez l'action **Gestion du chiffrement**.  
2. Dans la fenêtre **Gestion du chiffrement des données**, activez le chiffrement de vos données. <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a>Voir aussi  
[Configurer un échange de données](across-set-up-data-exchange.md)  
[Échange de données en tant que documents électroniques](across-data-exchange.md)

