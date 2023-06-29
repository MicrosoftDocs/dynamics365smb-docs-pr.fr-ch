---
title: Paramétrage de votre navigateur
description: "Décrit comment configurer les navigateurs pour qu’ils fonctionnent avec Business\_Central et les produits qui y sont intégrés."
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Configuration et dépannage de votre navigateur pour qu’il fonctionne avec le client Web Business Central

Cet article explique comment configurer votre navigateur pour que le [!INCLUDE[web_client](includes/web_client.md)] et toutes ses fonctionnalités fonctionnent correctement. Lisez cet article si vous rencontrez des problèmes pour ouvrir le [!INCLUDE[web_client](includes/web_client.md)], car certains problèmes peuvent être causés par les paramètres de votre navigateur.

L’article fournit des détails sur la configuration Microsoft Edge, mais les exigences pour JavaScript, les cookies et les fenêtres contextuelles sont les mêmes pour tous les navigateurs pris en charge. Pour les autres navigateurs, reportez-vous aux instructions fournies par le fabricant.  

## <a name="use-a-supported-browser"></a><a name="use-a-supported-browser"></a>Utiliser un navigateur compatible

Assurez-vous d’utiliser l’un des navigateurs pris en charge. Voir [Configuration minimale requise pour l’utilisation de Business Central](product-requirements.md#browsers).  

## <a name="allow-javascript-from-business-central"></a><a name="allow-javascript-from-business-central"></a>Autoriser JavaScript depuis Business Central

*Problème :*

Si le navigateur n’autorise pas JavaScript, vous verrez **NotSupported/DisabledJavaScript** dans la barre d’adresse et un message **HTTP 404.0 - Not Found** lorsque vous essayez d’ouvrir [!INCLUDE[prod_short](includes/prod_short.md)], et le 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Correctif :*

1. Dans Microsoft Edge, accédez à **Paramètres** > **Cookies et autorisations du site** > **JavaScript**.
2. Exécutez l’une des étapes suivantes. Choisissez l’étape recommandée par votre organisation :

    - Déplacez le bouton bascule **Autorisé** vers la gauche (désactivé). Puis, sélectionnez **Ajouter** et saisissez l’adresse (URL) pour [!INCLUDE[prod_short](includes/prod_short.md)] dans la zone **Site**. Sélectionnez **Ajouter** lorsque vous avez terminé.
    - Déplacez le bouton bascule **Autorisé** vers la droite (activé).

## <a name="allow-cookies-from-business-central"></a><a name="allow-cookies-from-business-central"></a>Autoriser les cookies depuis Business Central

*Problème :*

Si le navigateur n’autorise pas les cookies, vous obtiendrez l’erreur suivante :

**Désolé, la page est introuvable. Veuillez vérifier l’adresse et réessayer.** 

*Correctif :*

1. Dans Microsoft Edge, accédez à **Réglages** > **Cookies et autorisations du site** > **Cookies et données de site**.
2. Déplacez le bouton bascule **Autoriser les sites à enregistrer et lire les données des cookies** vers la droite (activé).  

## <a name="allow-pop-ups-from-business-central"></a><a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Autoriser les fenêtres contextuelles depuis Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] s’intègre à plusieurs produits. Dans certains cas, comme avec Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] s’ouvre, ou « ouvre une fenêtre contextuelle » dans le produit. Cette fonctionnalité nécessite que votre navigateur autorise les fenêtres contextuelles de [!INCLUDE[prod_short](includes/prod_short.md)].

*Problème :*

Si des fenêtres contextuelles pour [!INCLUDE[prod_short](includes/prod_short.md)] sont bloquées, vous recevez un message similaire au message suivant :

**Un problème est survenu. Votre navigateur bloque peut-être les fenêtres contextuelles nécessaires à Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Correctif :*

1. Dans Microsoft Edge, accédez à **Paramètres** > **Cookies et autorisations du site** > **Fenêtres contextuelles et redirections**.
2. Déplacez le bouton bascule **Bloqué** vers la droite (activé).
3. Sélectionnez **Ajouter**. Dans la zone **Site**, saisissez `https://businesscentral.dynamics.com`, puis sélectionnez **Ajouter**.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Résolution des incidents dans Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
