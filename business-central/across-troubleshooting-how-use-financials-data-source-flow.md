---
title: "Résolution des problèmes : Intégration à Microsoft Flow | Microsoft Docs"
description: "Vous pouvez modifier la façon de rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0818550021bf17e5a269d3e11f8db54b9ff80dfa
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Résolution des problèmes : Intégration à Microsoft Flow - URL de demande trop longue
Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.  

> [!NOTE]  
>   Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.  

Si vous créez un Microsoft Flow à l'aide du connecteur [!INCLUDE[d365fin](includes/d365fin_md.md)], vous risquez de recevoir un message d'erreur indiquant que l'URL demandée est trop longue après avoir créé le flux, comme par exemple : **RequestUriTooLong**.

## <a name="cause"></a>Motif
Pour déclencher un flux, les modifications apportées à vos données font l'objet d'une recherche. Quand les connecteurs déterminent si vos données ont été modifiées, ils comparent les données mises en cache aux données aux nouvelles données demandées à partir du document origine.  

Si la demande de données crée une URL qui est trop longue, elle échouera. Parmi les causes courantes on trouve :
- En général, toutes les tables source contenant plus de 250 lignes
- Les tables source contenant plusieurs milliers d'enregistrements

## <a name="workaround"></a>Solution de contournement
Suivez ces étapes pour résoudre le problème.
1. Modifiez le flux qui échoue.
2. Développez **Afficher les options avancées** dans le déclencheur de flux.
3. Dans le champ **Ignorer le nombre**, indiquez le nombre d'enregistrements à ignorer.  
Par exemple, si la table que vous utilisez comme source de données contient 4 000 enregistrements, saisissez 4 000 comme nombre d'enregistrements à ignorer.
4. Mettez votre flux à jour.

> [!NOTE]  
> Le connecteur est actuellement en version Bêta. Des mises à jour sur la façon dont les modifications sont apportées aux données sont prévues dans une prochaine version.


## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé](across-how-use-financials-data-source-flow.md)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)    
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  

