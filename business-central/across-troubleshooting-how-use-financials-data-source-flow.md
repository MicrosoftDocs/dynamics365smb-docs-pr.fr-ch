---
title: Résolution des problèmes liés à l'intégration de Microsoft Flow | Microsoft Docs
description: Vous pouvez modifier la façon de rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 8a43df89261867f80ba16782cde92b040ce180c8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "925939"
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
