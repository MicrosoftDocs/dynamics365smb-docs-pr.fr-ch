---
title: Procédure de configuration d’un service d’échange de document | Microsoft Docs
description: Utilisez un fournisseur de services externe pour échanger des documents électroniques avec vos partenaires commerciaux.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="set-up-a-document-exchange-service"></a><a name="set-up-a-document-exchange-service"></a>Configurer un service d’échange de document

Dans le cadre de l’Infrastructure d’échange de données, vous pouvez échanger des documents de vente et d’achat avec vos partenaires commerciaux sans étapes supplémentaires, telles que joindre les documents aux e-mails sous forme de fichiers PDF. Par exemple, lorsque vous êtes prêt à facturer un client, vous pouvez publier la facture et l’envoyer pour paiement sous forme de fichier que votre client peut recevoir dans son application de gestion d’entreprise. Pour plus d’informations, voir [Échanger des données par voir électronique](across-data-exchange.md).

> [!NOTE]
> La configuration d’un service d’échange de documents pour Business Central sur site nécessite quelques étapes supplémentaires pour l’autorisation. Pour plus d’informations, voir [Paramètres de Business Central local](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a><a name="connecting-with-trading-partners"></a>Connexion avec des partenaires commerciaux

L’échange de documents électroniques nécessite une connexion avec vos partenaires commerciaux. Pour faciliter la création d’une connexion sécurisée, [!INCLUDE[prod_short](includes/prod_short.md)] en ligne est configuré pour utiliser l’application d’intégration de Business Central. L’application est disponible sur l’App Store de Tradeshift, et tout ce que vous et vos partenaires commerciaux avez à faire est de créer un compte Tradeshift, puis d’activer l’application. L’application d’intégration de Business Central est disponible en versions de production et sandbox. Par exemple, la version sandbox est utile pour tester l’échange de documents. Vous pouvez basculer entre les versions de production et sandbox en activant ou désactivant le bouton à bascule **Sandbox** de la page **Paramètres du service d’échange documents**. Lorsque vous le faites, les informations du raccourci **Service** sont mises à jour pour vous.

Alternativement, si vous souhaitez utiliser un autre service, vous devez fournir des informations pour établir la connexion. Pour plus d’informations, reportez vous à [Se connecter à un service d’échange de document](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a><a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Pour se connecter à l’application d’intégration de Business Central sur Tradeshift

Vous pouvez rapidement créer un compte Tradeshift et commencer à utiliser l’application d’intégration de Business Central à partir de la page **Paramètres du service d’échange documents**. Choisissez soit le lien **Activer l’application** dans la notification ou le champ **URL de l’application** pour accéder à l’application dans la boutique d’applications Tradeshift. Sur la page de connexion de Tradeshift, connectez-vous ou inscrivez-vous.

> [!NOTE]
> Une fois que vous vous êtes connecté à votre compte Tradeshift, le site peut ne pas vous diriger vers la page où vous activez l’application. Pour ce faire, vous pouvez cliquer sur le lien sur la page **Paramètres du service d’échange documents** dans Business Central pour accéder directement à l’application.

Si vous décidez d’arrêter d’utiliser l’application d’intégration de Business Central, vous devez la désactiver dans la boutique d’applications Tradeshift. 

## <a name="to-connect-to-a-document-exchange-service"></a><a name="to-connect-to-a-document-exchange-service"></a>Se connecter à un service d’échange de document

Si vous préférez utiliser un autre service d’échange de documents, vous devez fournir certaines informations pour vous connecter au service.

1. Choisissez l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration du service d’échange de document**, puis sélectionnez le lien associé.  
2. Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Description|  
    |---------------------------------|---------------------------------------|  
    |**Agent utilisateur**|Entrez tout texte que vous pouvez utiliser pour identifier votre société dans les processus d’échange de documents.|  
    |**Activé**|Indiquez si la connexion au service est activée.<br><br> **Remarque :** lorsque vous activez le service, au moins deux écritures de la file projets sont créées pour traiter l’envoi et la réception des documents électroniques. Lorsque vous désactivez le service, les écritures de file projets sont supprimées.|  
    |**Sandbox**|Indiquez si vous vous connectez à une version sandbox du service d’échange de documents.|
    |**URL d’inscription**|Spécifiez la page Web sur laquelle vous vous êtes connecté au service d’échange de documents.|  
    |**URL d’application**|Choisissez le lien pour ouvrir la boutique d’applications et activer ou désactiver l’application d’intégration de Business Central.|
    |**URL service**|Spécifiez l’adresse du service d’échange de documents qui sera appelé lorsque vous envoyez ou recevez des documents électroniques.|  
    |**URL de connexion**|Spécifiez l’URL de la page que vous utilisez pour vous connecter au service d’échange de documents. Il s’agit de la page où vous entrez le nom d’utilisateur et le mot de passe de votre entreprise.|  
    
    > [!NOTE]  
    > Vos identifiants de connexion sont automatiquement chiffrés. Vous ne pouvez pas désactiver ce chiffrement.

    > [!NOTE]
    > Si vous ne pouvez pas vous connecter au service d’échange de documents en raison d’un problème d’autorisation, c’est peut-être parce que[!INCLUDE[prod_short](includes/prod_short.md)] ne peut pas renouveler automatiquement le jeton d’accès. Par exemple, cela peut se produire si vous n’avez pas utilisé le service pendant un certain temps. Vous pouvez renouveler le jeton manuellement en utilisant l’action **Renouveler le jeton**.

## <a name="settings-for-business-central-on-premises"></a><a name="settings-for-business-central-on-premises"></a>Paramètres de Business Central local

Pour connecter Business Central sur site, vous devez créer une application dans la boutique d’applications de Tradeshift. Lorsque vous le faites, utilisez l’URL de redirection du champ **URL de redirection** sur la page **Configuration du service d’échange de documents**. Après avoir enregistré votre application, Tradeshift fournira un identifiant client et un secret client. Dans [!INCLUDE[prod_short](includes/prod_short.md)], entrez ces valeurs dans le raccourci **Autorisation** de la page **Configuration du service d’échange de documents**.

Si vous préférez stocker l’ID d’application et le secret dans un emplacement différent, vous pouvez laisser les champs ID client et Secret client vides et écrire une extension pour récupérer l’ID et le secret depuis l’emplacement. Vous pouvez fournir le secret lors de l’exécution en vous abonnant aux événements OnGetClientId et OnGetClientSecret dans codeunit 1410 « Doc. Exch. Service Mgt. »

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/electronic-documents-dynamics-365-business-central/) associée

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Configuration de l’échange de données](across-set-up-data-exchange.md)  
[Échanger des données par voir électronique](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
