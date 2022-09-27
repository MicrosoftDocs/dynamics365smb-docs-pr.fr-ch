---
title: Personnalisation de Business Central Online à l’aide d’extensions
description: En savoir plus sur l’ajout des fonctionnalités et la personnalisation de Business Central en installant des extensions ici.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont
ms.openlocfilehash: 8ff68bbeb2d7603b1c4d1b612413279cca5eec86
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530475"
---
# <a name="customizing-business-central-online-using-extensions"></a>Personnalisation de Business Central Online à l’aide d’extensions

Vous pouvez modifier [!INCLUDE[prod_short](includes/prod_short.md)] en ligne en installant des extensions qui ajoutent des fonctionnalités, modifient le comportement de l’application, ou vous permettent d’accéder à de nouveaux services en ligne, par exemple.

> [!NOTE]
> Pour installer ou désinstaller des extensions à partir de AppSource ou ajouter des extensions par locataire, vous devez disposer des autorisations adéquates. Vous devez être membre du groupe d’utilisateurs **D365 Extension Mgt.** ou disposer explicitement du jeu d’autorisations **EXTEN. MGT. - ADMIN**. Si vous êtes un administrateur, vous pouvez attribuer des groupes d’utilisateurs et des autorisations à d’autres utilisateurs de votre entreprise. Pour plus d’informations, voir [Créer des utilisateurs conformément aux licences](ui-how-users-permissions.md).  
>
> Pour utiliser les fonctionnalités fournies par une extension, telles que l’ouverture de pages, la production de rapports, la sélection d’actions, etc., vous devez disposer des jeux d’autorisations installés avec cette extension.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

> [!IMPORTANT]  
> Le chargement des extensions par client et l’installation des extensions AppSource ne sont pas pris en charge via la page **Gestion des extensions** pour les installations sur site. Vous ne pouvez pas installer d’extensions AppSource sur site, y compris dans les déploiements basés sur Docker.

La première fois que vous lancez [!INCLUDE[prod_short](includes/prod_short.md)], certaines extensions sont déjà installées. Au fil du temps, davantage d’extensions seront disponibles. Il vous appartient de choisir si vous souhaitez les utiliser ou non.

Par exemple, Microsoft propose une extension qui fournit une intégration à PayPal Payments Standard. Cette extension est installée par défaut.
Si une autre extension proposant une intégration à un autre service de paiement devenait disponible, vous pouvez installer cette nouvelle extension et choisir lequel des deux services vous souhaitez utiliser.  

La page **Gestion des extensions** vous permet de gérer les extensions. Vous pouvez accéder à cette page à partir de la page d’accueil. Sinon, choisissez l’icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis sélectionnez le lien associé. Pour plus d’informations, consultez [Installation et désinstallation d’extensions](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si vous voulez accéder à une extension mais que vous ne pouvez pas trouver sa fonctionnalité, vérifiez la page **Gestion des extensions**, si l’extension n’est pas répertoriée, vous pouvez la configurer comme décrit dans la section suivante.  

> [!NOTE]  
> Connectez-vous au site [AppSource.microsoft.com](https://appsource.microsoft.com/) à l’aide du compte de messagerie électronique que vous utilisez pour [!INCLUDE[prod_short](includes/prod_short.md)] en ligne. Utilisez le même compte de messagerie électronique pour d’autres services et produits pour une expérience agréable.  

Vous pouvez également accéder au marché à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Gestion des extensions**, vous pouvez voir les extensions actuellement installées, et vous pouvez ouvrir la page **Marché des extensions** qui affiche les extensions [!INCLUDE[prod_short](includes/prod_short.md)] actuellement disponibles dans AppSource. Si vous optez pour le lien *Plus d’applications*, vous êtes dirigé vers le site [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Si vous choisissez une extension, vous pouvez consulter une documentation relative à ses fonctionnalités, et accéder au service d’aide de l’extension pour en savoir plus. Lorsque vous choisissez d’obtenir une extension, vous devez être d’accord avec les conditions d’utilisation. Si vous obtenez l’extension à partir du site Web AppSource, vous serez connecté à [!INCLUDE[prod_short](includes/prod_short.md)] pour terminer l’installation.  

Lorsque vous installez une extension, vous pouvez être amené à la configurer, par exemple spécifier un compte à utiliser avec l’extension **PayPal Payments Standard pour [!INCLUDE[prod_short](includes/prod_short.md)]**.
D’autres extensions ajoutent simplement des champs à une page existante, ou ajoutent une nouvelle page, par exemple.   

Si vous désinstallez une extension, et que vous changez ensuite d’avis, vous pouvez la réinstaller. Lorsque vous désinstallez une extension que vous avez utilisée, les données sont conservées de sorte à demeurer disponibles si vous installez à nouveau l’extension. Certaines extensions sont nécessaires. Vous ne pouvez pas les désinstaller à partir de la page **Gestion des extensions**. Si vous essayez, un message d’erreur apparaît.  

Certaines extensions sont fournies par Microsoft, et d’autres sont fournies par [d’autres sociétés](ui-extensions-other.md). Toutes les sont extensions testées avant d’être mises à votre disposition, mais nous vous recommandons d’accéder aux liens qui sont inclus dans chaque extension pour en savoir plus sur l’extension avant de décider de l’installer.  

> [!NOTE]  
> Vous pouvez vous tenir informé sur les nouvelles extensions de Microsoft et d’autres fournisseurs sur le site [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Extensions et transfert de données

Comme les extensions suivantes communiquent avec d’autres services, elles peuvent transférer des données hors de la géographie de l’environnement [!INCLUDE[prod_short](includes/prod_short.md)] :

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

## <a name="recommended-apps"></a>Applications recommandées
Les partenaires et revendeurs Microsoft peuvent créer des extensions utilisables pour compiler des listes d’applications qu’ils recommandent souvent à leurs clients. S’ils le font, et qu’ils ont déployé l’extension sur votre locataire, les applications seront disponibles sur la page **Applications recommandées**. Là, vous pouvez vous renseigner sur chaque application et décider de les installer.

> [!NOTE]
> Si vous êtes un partenaire ou un revendeur Microsoft et que vous souhaitez fournir une liste d’applications recommandées, consultez [Recommander des applications depuis AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/customize-dynamics-365-business-central/) associée

## <a name="see-also"></a>Voir aussi

[Installer et désinstaller des extensions](ui-extensions-install-uninstall.md)  
[Personnaliser Business Central](ui-customizing-overview.md)  
[Extensions Business Central par d’autres fournisseurs](ui-extensions-other.md)  
[Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md)  
[Migration des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de l’extension GetAddress.io UK Postal Code](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Extensions [!INCLUDE[prod_short](includes/prod_short.md)] par d’autres fournisseurs](ui-extensions-other.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
