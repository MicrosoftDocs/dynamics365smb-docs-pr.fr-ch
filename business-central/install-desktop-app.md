---
title: Installer Business Central sur votre bureau
description: Cet article explique comment obtenir l’application Business Central sur un bureau Windows ou MACiOS.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'phone, tablet'
ms.date: 01/11/2022
ms.author: jswymer
---
# <a name="get-business-central-desktop-app"></a>Installer l’application Business Central sur votre bureau

Si vous disposez d’un ordinateur Windows (PC) ou macOS, vous pouvez installer une application Business Central sur votre bureau. L’application fonctionne avec Business Central Online et On-premises.

## <a name="why-use-the-app"></a>Pourquoi utiliser l’application ?

L’application Business Central ressemble au client web, mais elle offre quelques avantages, tels que les suivants :

- L’application est facilement accessible depuis le menu **Démarrer** ; vous pouvez facilement l’épingler à la barre des tâches ou la faire lancer par défaut lorsque vous démarrez votre ordinateur.
- En général, l’application offre également un affichage plus rapide et plus fluide à l’écran, sans différence de performances par rapport à l’exécution de [!INCLUDE[prod_short](includes/prod_short.md)] dans le navigateur.
- L’application s’ouvre dans sa propre fenêtre, indépendamment des fenêtres du navigateur. Cette fonctionnalité facilite la recherche lors de l’exécution d’un grand nombre d’applications ou d’onglets de navigateur.
- Si vous disposez de plusieurs environnements Business Central (Online uniquement), vous pouvez installer l’application séparément pour chaque environnement.

     Lorsque vous ouvrez l’application pour un environnement spécifique, le nom de l’environnement est inclus dans le titre de la fenêtre. Lorsque vous travaillez sur plusieurs environnements [!INCLUDE[prod_short](includes/prod_short.md)], chaque fenêtre d’application est affichée séparément. Le nom vous permet de voir plus facilement quelle fenêtre est associée à chaque environnement.

## <a name="install-the-app-for-business-central-online"></a>Installer l’application pour Business Central Online

Il existe deux façons d’installer l’application pour Business Central Online. Vous pouvez l’installer directement depuis le navigateur ou depuis Microsoft Store. Quelle que soit l’approche que vous utilisez, c’est la même application. La différence est que l’installation à partir du navigateur vous permet d’installer l’application pour chaque environnement lorsqu’il y en a plusieurs.

### <a name="from-microsoft-store"></a>Sur Microsoft Store

1. Accédez à [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=2182870).
2. Choisissez **Obtenir** > **Installer**. 
3. Une fois l’application installée, choisissez **Ouvrir**, puis connectez-vous à Business Central.

La prochaine fois que vous voudrez ouvrir l’application, recherchez-la dans le menu **Démarrer**.

### <a name="from-the-browser"></a>Depuis le navigateur

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

## <a name="install-the-app-for-business-central-on-premises"></a>Installer l’application pour Business Central On-premises

L’installation de l’application de bureau lorsque vous utilisez Business Central On-premises s’effectue directement à partir du navigateur [comme décrit ci-dessus](#from-the-browser). Si vous n’avez qu’un seul locataire, ouvrez simplement Business Central dans votre navigateur, puis sélectionnez soit ![l’icône pour installer une application dans Edge.](media/ui-edge-install-app-icon.png) **Application disponible. Installer Business Central** ou ![l’icône pour installer une application dans Chrome.](media/ui-chrome-install-app-icon.png) **Installer Business Central** comme illustré ci-dessus.

La différence est lorsque vous avez plusieurs locataires. Contrairement à [!INCLUDE[prod_short](includes/prod_short.md)] Online, où vous pouvez installer l’application pour différents environnements, avec la version On-premises, vous ne pouvez installer l’application que pour un seul locataire. Ainsi, avant d’installer l’application lorsque vous avez plusieurs locataires, assurez-vous de basculer vers le bon locataire. Une fois installée, lorsque vous ouvrez l’application, elle ouvrira directement le locataire.

> [!IMPORTANT]
> Si vous utilisez la 1re vague de lancement 2021 Business Central (version 18) ou une version antérieure, vous ne pouvez pas installer l’application comme décrit dans cet article. Au lieu de cela, installez l’application à partir de [Microsoft Store](https://go.microsoft.com/fwlink/?LinkId=734848). Pour plus d’informations et de l’aide sur l’installation de cette application héritée, voir [Préparation et installation de l’application Business Central](/dynamics365/business-central/dev-itpro/deployment/install-business-central-app).

## <a name="see-also"></a>Voir aussi

[FAQ sur les applications mobiles](ui-mobile-faq.yml)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
