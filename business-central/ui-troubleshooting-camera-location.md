---
title: "Dépannage\_: accès à la caméra et à l’emplacement"
description: Cet article décrit comment résoudre les problèmes d’accès à la caméra et aux informations de localisation dans Business Central.
author: brentholtorf
ms.author: bholtorf
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
---

# <a name="troubleshooting-accessing-camera-and-location"></a>Dépannage : accès à la caméra et à l’emplacement

Vous pouvez rencontrer des problèmes lorsque vous essayez d’accéder à la caméra et aux informations de localisation d’un appareil à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez trouver les causes possibles de ces problèmes et comment les contourner ci-dessous.

## <a name="device-must-have-camera-and-location-capabilities"></a>L’appareil doit avoir des capacités de caméra et de localisation

Afin d’accéder à la caméra ou à l’emplacement d’un utilisateur à partir d’un appareil, l’appareil doit avoir une caméra physique ou la capacité de récupérer les informations d’emplacement, respectivement.

Si votre appareil possède des capacités de caméra et de localisation, mais que vous rencontrez toujours des problèmes, il est possible que certains pilotes nécessitent une mise à jour ou une réinstallation. Même si vous n’êtes pas sûr, nous vous recommandons toujours de mettre à jour le système d’exploitation, les pilotes et le navigateur de votre appareil vers la dernière version pour une expérience optimale.

## <a name="access-permissions-not-enabled"></a>Autorisations d’accès non activées

Vous devez autoriser l’accès général à la caméra et à l’emplacement depuis les paramètres de confidentialité de votre appareil et donner explicitement l’autorisation de [!INCLUDE[prod_short](includes/prod_short.md)] pour y accéder. Par exemple, pour voir ou modifier les autorisations pour un appareil fonctionnant sous Windows, accédez à **Paramètres**, choisissez **Confidentialité**, puis **Autorisations d’application**. 

Pour les appareils mobiles, vous devez accorder des autorisations d’accès à la caméra et à l’emplacement à l’application mobile [!INCLUDE[prod_short](includes/prod_short.md)]. Pour ce faire pour un appareil iOS, accédez à **Paramètres**, choisissez **Confidentialité**, puis **Caméra** ou **Emplacement**. Pour les appareils Android, accédez à **Paramètres**, choisissez **Applications et notifications**, **Avancée**, **Gestionnaire des autorisations**, puis **Caméra** ou **Emplacement**.

De plus, si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] dans un navigateur, vous devez également accorder l’autorisation du site [!INCLUDE[prod_short](includes/prod_short.md)] pour accéder à la caméra ou aux informations de localisation. Pour voir ou modifier les autorisations d’un site dans le navigateur Microsoft Edge, allez à **Paramètres**, choisissez **Autorisations de site**, puis **Caméra** ou **Emplacement**. Notez que cela peut être différent pour d’autres navigateurs.

Par défaut, l’appareil ou le navigateur affichera une demande d’accès à ces fonctionnalités lorsque l’utilisateur les activera pour la première fois.

> [!NOTE]  
> Certains anciens navigateurs n’accordent pas l’accès à la caméra et à l’emplacement. Par exemple, l’appareil photo n’est pas disponible dans le navigateur Internet Explorer ou Edge hérité.

## <a name="web-client-connection-not-secure"></a>Connexion client Web non sécurisée

Les fonctionnalités de caméra et de localisation ne sont disponibles que lors de l’accès au client Web via des connexions HTTP sécurisées SSL, à l’aide du Schéma d’URI `https://`. 

La seule exception est la connexion à `http://localhost`, utilisé à des fins de développement et de test.


## <a name="work-with-virtualization-technologies"></a>Utiliser des technologies de virtualisation

Lors de la connexion à [!INCLUDE[prod_short](includes/prod_short.md)] via Remote Desktop ou une autre virtualisation, l’accès à la caméra ou à l’emplacement peut ne pas être disponible. Si tel est le cas, utilisez plutôt le système physique.

## <a name="antivirus-software"></a>Logiciel antivirus
Certains logiciels antivirus bloquent l’accès à la caméra et à l’emplacement par défaut. N’oubliez pas de vérifier les paramètres de votre logiciel antivirus.

## <a name="see-also"></a>Voir aussi
[Implémentation de la caméra dans AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implémentation de l’emplacement dans AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]
