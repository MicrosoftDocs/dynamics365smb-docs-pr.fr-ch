---
title: "Personnalisation de Business\_Central Online à l’aide d’applications"
description: "En savoir plus sur l’ajout des fonctionnalités et la personnalisation de Business\_Central en installant des applications dans cet article."
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: edupont
---
# <a name="customizing-business-central-online-with-apps"></a>Personnalisation de Business Central Online à l’aide d’applications

Vous pouvez modifier [!INCLUDE[prod_short](includes/prod_short.md)] en ligne en installant des applications qui ajoutent des fonctionnalités, modifient le comportement de l’application, ou vous permettent d’accéder à de nouveaux services en ligne, par exemple. Ces applications sont également appelées *extensions*, car elles *s’étendent*[!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a>Gérer les applications

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

La première fois que vous lancez [!INCLUDE[prod_short](includes/prod_short.md)], certaines applications sont déjà installées. Au fil du temps, davantage d’applications seront disponibles. Il vous appartient de choisir si vous souhaitez les utiliser ou non.

Par exemple, Microsoft propose une application qui fournit une intégration à PayPal Payments Standard. Cette extension est installée par défaut. Si une autre extension proposant une intégration à un autre service de paiement devenait disponible, vous pouvez installer cette nouvelle extension et choisir lequel des deux services vous souhaitez utiliser.  

Pour utiliser les fonctionnalités fournies par une application, telles que l’ouverture de pages, la production de rapports, la sélection d’actions, etc., vous devez disposer des jeux d’autorisations installés avec cette application.

Pour installer ou désinstaller des applications à partir de AppSource ou ajouter des extensions par locataire, vous devez disposer des autorisations adéquates. Vous devez être membre du groupe d’utilisateurs **D365 Extension Mgt.** ou disposer explicitement du jeu d’autorisations **EXTEN. MGT. - ADMIN**. Si vous êtes un administrateur, vous pouvez attribuer des groupes d’utilisateurs et des autorisations à d’autres utilisateurs de votre entreprise. Pour plus d’informations, voir [Créer des utilisateurs conformément aux licences](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> Pour [!INCLUDE [prod_short](includes/prod_short.md)] en local, vous ne pouvez pas télécharger d’extensions par client ni installer d’applications AppSource via la page **Gestion des extensions**. Vous ne pouvez pas installer d’applications AppSource en local, y compris dans les déploiements basés sur Docker.

La page **Gestion des extensions** vous permet de gérer les applications. Vous pouvez accéder à cette page à partir de la page d’accueil. Sinon, choisissez l’icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis sélectionnez le lien associé. Pour plus d’informations, consultez [Installation et désinstallation d’applications](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si vous voulez accéder à une application, mais que vous ne pouvez pas trouver sa fonctionnalité, vérifiez la page **Gestion des extensions**, si l’application n’est pas répertoriée, vous pouvez la configurer comme décrit dans la section suivante.  

> [!NOTE]  
> Connectez-vous au site [AppSource.microsoft.com](https://appsource.microsoft.com/) à l’aide du compte de messagerie électronique que vous utilisez pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne. Utilisez le même compte de messagerie électronique pour d’autres services et produits pour une expérience agréable.  

Vous pouvez également accéder au marché à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Gestion des extensions**, vous pouvez voir les applications actuellement installées, et vous pouvez ouvrir la page **Marché des extensions** qui affiche les applications [!INCLUDE[prod_short](includes/prod_short.md)] actuellement disponibles dans AppSource. Si vous optez pour le lien *Plus d’applications*, vous êtes dirigé vers le site [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Si vous choisissez une application, vous pouvez consulter une documentation relative à ses fonctionnalités, et accéder au service d’aide de l’application pour en savoir plus. Lorsque vous choisissez d’obtenir une application, vous devez être d’accord avec les conditions d’utilisation. Si vous obtenez l’application à partir du site Web AppSource, vous serez connecté à [!INCLUDE[prod_short](includes/prod_short.md)] pour terminer l’installation.  

Lorsque vous installez une application, vous pouvez être amené à la configurer, par exemple spécifier un compte à utiliser avec l’extension **PayPal Payments Standard pour [!INCLUDE[prod_short](includes/prod_short.md)]**.
D’autres applications ajoutent simplement des champs à une page existante, ou ajoutent une nouvelle page, par exemple.   

Si vous désinstallez une application, et que vous changez ensuite d’avis, vous pouvez la réinstaller. Lorsque vous désinstallez une application que vous avez utilisée, les données sont conservées de sorte à demeurer disponibles si vous installez à nouveau l’application. Certaines applications sont nécessaires. Vous ne pouvez pas les désinstaller à partir de la page **Gestion des extensions**. Si vous essayez, un message d’erreur apparaît.  

Certaines applications sont fournies par Microsoft, et d’autres sont fournies par [d’autres sociétés](ui-extensions-other.md). Toutes les applications sont testées avant d’être mises à votre disposition, mais nous vous recommandons d’accéder aux liens qui sont inclus dans chaque extension pour en savoir plus sur l’application avant de décider de l’installer.  

> [!NOTE]  
> Vous pouvez vous tenir informé sur les nouvelles applications de Microsoft et d’autres fournisseurs sur le site [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a>Applications et transfert de données

Comme les applications suivantes communiquent avec d’autres services, elles peuvent transférer des données hors de la géographie de l’environnement [!INCLUDE[prod_short](includes/prod_short.md)] :

* Extension AMC Banking 365 Fundamentals
* Analyseur Image
* Prévisions de retard de paiement
* PayPal Payments Standard
* Stock prévu et ventes prévues
* WorldPay Payments Standard

Cela s’applique également à certaines fonctionnalités de l’application de base, telles que les fonctionnalités suivantes :

* Prévision de trésorerie
* Service d’échange de documents
* Connexions à Dataverse
* Service OCR
* Online Map
* N° id. intracomm. Union européenne Service

## <a name="connect-your-business"></a>Connectez votre entreprise

À partir de la 2è vague de lancement 2022, les environnements [!INCLUDE [prod_short](includes/prod_short.md)] en ligne peuvent répertorier une ou plusieurs applications sur les pages **Applications de connectivité** et **Applications bancaires**. Ces applications qui peuvent relier votre entreprise à des services externes afin d’augmenter votre productivité en automatisant les processus. Par exemple, vous pouvez vous connecter à vos banques et importer automatiquement les transactions bancaires. Les applications sont faciles à installer et à configurer directement à partir de cette page. Choisissez une application pour en savoir plus sur les fonctionnalités et les tarifs.  

Affichez la liste des applications suggérées en choisissant l’action **Applications de connectivité** dans la page **Gestion des extensions**.  

> [!NOTE]
> La première personne à ouvrir la page **Applications de connectivité** doit permettre à l’extension de se connecter à un service externe. Autoriser la connexion une fois ou toujours. Si vous choisissez de bloquer la connexion, vous devez trouver les applications pertinentes sur AppSource.

Ce service externe générera une liste d’applications pertinentes en fonction de votre pays ou de votre région

## <a name="recommended-apps"></a>Applications recommandées

Les partenaires et revendeurs Microsoft peuvent créer une application utilisable pour compiler des listes d’applications qu’ils recommandent souvent à leurs clients. S’ils le font, et qu’ils ont déployé l’application sur votre locataire, les applications seront disponibles sur la page **Applications recommandées**. Là, vous pouvez vous renseigner sur chaque application et décider de les installer.

> [!NOTE]
> Si vous êtes un partenaire ou un revendeur Microsoft et que vous souhaitez fournir une liste d’applications recommandées, consultez [Recommander des applications depuis AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) dans le contenu d’administration.

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/customize-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Installer et désinstaller des applications](ui-extensions-install-uninstall.md)  
[Personnaliser Business Central](ui-customizing-overview.md)  
[Applications Business Central par d’autres fournisseurs](ui-extensions-other.md)  
[Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Activer les paiements client via les services de paiement](sales-how-enable-payment-service-extensions.md)  
[Migrer des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configurer l’extension GetAddress.io UK Postal Code](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Applications [!INCLUDE[prod_short](includes/prod_short.md)] par d’autres fournisseurs](ui-extensions-other.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
