---
title: Installer Business Central sur votre bureau
description: Cet article explique comment obtenir l’application Business Central sur un bureau Windows ou MACiOS.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: phone, tablet
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: babf20be3c22a3d4b7dd710e2486c59bc11351fe
ms.sourcegitcommit: 795f0298e32b4c0174aeeb9a7da64f1e5c8457d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/04/2021
ms.locfileid: "7596662"
---
# <a name="get-business-central-desktop-app"></a>Installer l’application Business Central sur votre bureau

Si vous disposez d’un ordinateur Windows (PC) ou macOS, vous pouvez installer une application Business Central sur votre bureau. 
> [!NOTE]
> Si vous utilisez Business Central de la 1e vague de lancement 2021 ou une version antérieure, téléchargez l’application à partir du [Windows Store](https://go.microsoft.com/fwlink/?LinkId=734848).

## <a name="why-use-the-app"></a>Pourquoi utiliser l’application ?

L’application Business Central ressemble au client web, mais elle offre quelques avantages, tels que les suivants :

- L’application est facilement accessible depuis le menu **Démarrer** ; vous pouvez facilement l’épingler à la barre des tâches ou la faire lancer par défaut lorsque vous démarrez votre ordinateur.
- En général, l’application offre également un affichage plus rapide et plus fluide à l’écran, sans différence de performances par rapport à l’exécution de [!INCLUDE[prod_short](includes/prod_short.md)] dans le navigateur.
- L’application s’ouvre dans sa propre fenêtre, indépendamment des fenêtres du navigateur. Cette fonctionnalité facilite la recherche lors de l’exécution d’un grand nombre d’applications ou d’onglets de navigateur.
- Si vous disposez de plusieurs environnements Business Central (en ligne uniquement), vous pouvez installer l’application séparément pour chaque environnement.

     Lorsque vous ouvrez l’application pour un environnement spécifique, le nom de l’environnement est inclus dans le titre de la fenêtre. Lorsque vous travaillez sur plusieurs environnements [!INCLUDE[prod_short](includes/prod_short.md)], chaque fenêtre d’application est affichée séparément. Le nom vous permet de voir plus facilement quelle fenêtre est associée à chaque environnement.

## <a name="install-the-app"></a>Installer l’application

1. Ouvrez le client web [!INCLUDE[prod_short](includes/prod_short.md)] dans un navigateur Microsoft Edge ou Google Chrome.

2. Si la page de sélection de l’environnement apparaît, vous pouvez effectuer l’une des deux actions suivantes :

   - Sélectionnez l’environnement et passez à l’étape suivante pour installer l’application. Dans ce cas, l’application installée ouvrira l’environnement que vous sélectionnez.
   - Ne sélectionnez pas d’environnement et passez à l’étape suivante pour installer l’application. Dans ce cas, l’application installée ouvrira la page de sélection d’environnement, au lieu d’un environnement spécifique.

3. Pour installer l’application, selon votre navigateur, sélectionnez ![l’icône pour installer une application dans Edge.](media/ui-edge-install-app-icon.png) **Application disponible. Installer Business Central** ou ![l’icône pour installer une application dans Chrome.](media/ui-chrome-install-app-icon.png) **Installer Business Central**, puis **Installer**.

   | Microsoft Edge | Google Chrome |
   |--|--|
   | :::image type="content" source="media/ui-edge-install-app-v2.png" alt-text="illustration d’un bouton pour installer une application dans Edge."::: | :::image type="content" source="media/ui-chrome-install-app-v2.png" alt-text="illustration d’un bouton pour installer une application dans Chrome."::: |

  > [!TIP]
  > Avec Edge, vous pouvez également installer l’application en accédant au menu **Paramètres et plus** dans le navigateur, puis en sélectionnant **Applications** > **Installer ce site en tant qu’application** > **Installer**.

Une fois installée, l’application apparaît dans le menu **Démarrer**. Si vous avez sélectionné un environnement spécifique pour l’application, le nom de l’environnement est ajouté au nom de l’application dans le menu **Démarrer**.

### <a name="for-business-central-on-premises"></a>Pour Business Central local

L’installation de l’application lorsque vous utilisez Business Central sur site est fondamentalement la même que celle décrite ci-dessus. Si vous n’avez qu’un seul locataire, ouvrez simplement Business Central dans votre navigateur, puis sélectionnez soit ![l’icône pour installer une application dans Edge.](media/ui-edge-install-app-icon.png) **Application disponible. Installer Business Central** ou ![l’icône pour installer une application dans Chrome.](media/ui-chrome-install-app-icon.png) **Installer Business Central** comme illustré ci-dessus. 

La différence est lorsque vous avez plusieurs locataires. Contrairement à [!INCLUDE[prod_short](includes/prod_short.md)] en ligne, où vous pouvez installer l’application séparément pour différents environnements, avec la version sur site vous ne pouvez installer l’application que pour un seul locataire. Ainsi, avant d’installer l’application lorsque vous avez plusieurs locataires, assurez-vous de basculer vers le bon locataire. Une fois installée, lorsque vous ouvrez l’application, elle ouvrira directement le locataire.

<!-- for FAQ or troubleshooting
> [!NOTE]
> To install the app, [!INCLUDE[prod_short](includes/prod_short.md)] must be configured for HTTPS. If it isn't, you won't see ![Icon for installing an app in Edge.](media/ui-edge-install-app-icon.png) **App available. Install Business Central** or ![Icon for installing an app in Chrome.](media/ui-chrome-install-app-icon.png) **Install Business Central** in the browser. If you're having problems, contact your administrator or see [Configuring SSL to Secure the Business Central Web Client Connection](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection) about how to configure HTTPS.
-->

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[FAQ relative aux applications mobiles](ui-mobile-faq.yml)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]