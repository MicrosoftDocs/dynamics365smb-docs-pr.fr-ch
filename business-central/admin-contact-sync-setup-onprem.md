---
title: "Configurer la synchronisation du contact avec Outlook pour Business\_Central en local"
description: "Découvrez comment configurer un environnement local Business\_Central pour synchroniser les contacts dans Business\_Central et Outlook."
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
---

# Configurer la synchronisation du contact avec Outlook pour Business Central en local

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Dans cet article, vous apprendrez à configurer [!INCLUDE[prod_short](includes/prod_short.md)] sur site pour synchroniser les contacts dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les contacts dans Outlook. Pour plus d’informations sur la fonctionnalité, accédez à [Synchroniser les contacts dans Business Central avec les contacts dans Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Introduction

La synchronisation des contacts nécessite l’utilisation du protocole OAuth 2.0 pour l’authentification avec Exchange Online. Auparavant, l’authentification de base était également prise en charge, mais elle est obsolète et n’est plus prise en charge avec Exchange Online. Vous pouvez en savoir plus sur l’obsolescence sur [Abandon de l’authentification de base dans Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Cette modification signifie que la synchronisation des contacts dans Business Central peut avoir cessé de fonctionner sur votre environnement local. Cet article vous expliquera comment le faire fonctionner à nouveau.

## Conditions préalables

- Exchange Online, en version autonome ou via Microsoft 365 plan  
- Accès au locataire Microsoft Entra utilisé par Exchange Online
- Les utilisateurs [!INCLUDE[prod_short](includes/prod_short.md)] disposent d’un Microsoft 365 ou Exchange Online compte de messagerie, qui est attribué à leurs comptes dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez vérifier ce paramètre dans la section **Authentification Microsoft 365** du profil utilisateur dans la liste **Utilisateurs**. 

## Configurer la synchronisation des contacts

Effectuez les étapes suivantes pour configurer la synchronisation des contacts. Si vous exécutez [!INCLUDE[prod_short](includes/prod_short.md)] Printemps 2019 (v.14), vous devrez effectuer une étape supplémentaire qui modifie le code de l’application ou configure une connexion à Power BI.

1. <a name="registerapp"></a>Enregistrer une application pour l’API Exchange Online dans votre abonné Microsoft Entra.

   Dans cette étape, vous ajoutez une application enregistrée dans le locataire Microsoft Entra de votre plan Microsoft 365 ou Exchange Online. Comme d′autres services Azure qui fonctionnent avec Business Central, Exchange Online nécessite une application enregistrée dans Microsoft Entra ID. L’application enregistrée fournit des services d’authentification et d’autorisation entre Business Central et Exchange Online.

   Suivez les instructions détaillées de l’aide pour développeurs et professionnels de l’informatique dans [Enregistrer une application dans Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Au fur et à mesure que vous parcourez les instructions, rappelez-vous les points suivants :

   - Si vous avez déjà enregistré une application dans le cadre d’une intégration avec un autre produit Microsoft, tel que Power BI, réutilisez cette application enregistrée. Dans ce cas, vous n’aurez qu’à définir l’application avec les autorisations Office 365 Exchange Online décrites au point suivant.

   - Configurez l’application enregistrée avec les autorisations suivantes déléguées à l’API Office 365 Exchange Online :

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Pour [!INCLUDE[prod_short](includes/prod_short.md)] version 14, effectuez l’une des tâches suivantes :

   - Modifiez la page 6 700 en remplaçant `FALSE` par `TRUE` dans la ligne de code suivante dans le déclencheur `OnPageOpen` :

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Créez une page avec le code suivant sur le déclencheur OnPageOpen :

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Configurez Power BI en suivant les instructions sur [Configurer Business Central sur site pour l’intégration Power BI](admin-powerbi-setup.md#setup).

   Une fois la solution choisie en place, demandez aux utilisateurs d’exécuter la page nouvelle/modifiée ou de [se connecter à Power BI](across-working-with-powerbi.md#connect). Ils ne devront effectuer cette étape qu’une seule fois.

## Étapes suivantes

[Synchroniser les contacts de Business Central avec les contacts de Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
