---
title: "Installation d'extensions pour personnaliser Dynamics 365 Business edition | Microsoft Docs"
description: "En savoir plus sur l'ajout des fonctionnalités et la personnalisation de Dynamics 365 Business edition en installant des extensions."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 07/07/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2f6bbbc213bce74b31bb4e8c64198559db2d105d
ms.contentlocale: fr-ch
ms.lasthandoff: 11/10/2017

---
# <a name="customizing-dynamics-365-business-edition-using-extensions"></a>Personnalisation de Dynamics 365, business edition à l'aide d'extensions
Vous pouvez modifier [!INCLUDE[d365fin](includes/d365fin_md.md)] en installant des extensions qui ajoutent des fonctionnalités, modifient le comportement de l'application, ou vous permettent d'accéder à de nouveaux services en ligne, par exemple.
La première fois que vous lancez [!INCLUDE[d365fin](includes/d365fin_md.md)], certaines extensions sont déjà installées. Au fil du temps, davantage d'extensions seront disponibles. Il vous appartient de choisir si vous souhaitez les utiliser ou non.

Par exemple, Microsoft propose une extension qui fournit une intégration à PayPal Payments Standard. Cette extension est installée par défaut.
Si une autre extension proposant une intégration à un autre service de paiement devenait disponible, vous pouvez installer cette nouvelle extension et choisir lequel des deux services vous souhaitez utiliser.  

La fenêtre **Gestion des extensions** vous permet de gérer les extensions. Vous pouvez accéder à cette fenêtre à partir de la page d'accueil. Sinon, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche") dans le coin supérieur droit, entrez **Extension**, puis sélectionnez le lien associé.  

> [!NOTE]  
>   Si vous voulez accéder à une extension mais que vous ne pouvez pas trouver sa fonctionnalité, vérifiez la fenêtre **Gestion des extensions**, si l'extension n'est pas répertoriée, vous pouvez la configurer comme décrit dans la section suivante.  

## <a name="installing-an-extension"></a>Installation d'une extension
Vous pouvez obtenir de nouvelles extensions depuis le marché à l'adresse [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1). Ici, vous trouverez toutes les extensions disponibles pour [!INCLUDE[d365fin](includes/d365fin_md.md)], et vous pourrez obtenir des applications, des extensions et des packs de contenu pour d'autres produits Microsoft. Définissez les filtres appropriés, observez les informations pour chaque extension et obtenez une extension pour votre [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Connectez-vous au site [AppSource.microsoft.com](https://appsource.microsoft.com/) à l'aide du compte de messagerie électronique que vous utilisez pour [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilisez le même compte de messagerie électronique pour d'autres services et produits pour une expérience agréable.  

Vous pouvez également accéder au marché à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dans la fenêtre **Gestion des extensions**, vous pouvez voir les extensions actuellement installées, et vous pouvez ouvrir la page **Marché des extensions** qui affiche les extensions [!INCLUDE[d365fin](includes/d365fin_md.md)] actuellement disponibles dans AppSource. Si vous optez pour le lien *Plus d'applications*, vous êtes dirigé vers le site [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Si vous choisissez une extension, vous pouvez consulter une documentation relative à ses fonctionnalités, et accéder au service d'aide de l'extension pour en savoir plus. Lorsque vous choisissez d'obtenir une extension, vous devez être d'accord avec les conditions d'utilisation. Si vous obtenez l'extension à partir du site Web AppSource, vous serez connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)] pour terminer l'installation.  

Lorsque vous installez une extension, vous pouvez être amené à la configurer, par exemple spécifier un compte à utiliser avec l'extension **PayPal Payments Standard pour [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
D'autres extensions ajoutent simplement des champs à une page existante, ou ajoutent une nouvelle page, par exemple.   

Si vous désinstallez une extension, et que vous changez ensuite d'avis, vous pouvez la réinstaller. Lorsque vous désinstallez une extension que vous avez utilisé, les données sont conservées de sorte à demeurer disponibles si vous installez à nouveau l'extension.  

Certaines extensions sont fournies par Microsoft, et d'autres sont fournies par [d'autres sociétés](ui-extensions-other.md). Toutes les sont extensions testées avant d'être mises à votre disposition, mais nous vous recommandons d'accéder aux liens qui sont inclus dans chaque extension pour en savoir plus sur l'extension avant de décider de l'installer.  

Microsoft fournit les extensions suivantes :  

* [Extension Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md)  
* [Extension Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [Extension QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md)  
* [Stock et ventes prévus](ui-extensions-sales-forecast.md)  
* [Extension Ceridian Payroll](ui-extensions-ceridian-payroll.md)  
* [Extension Importer le fichier de paie de Quickbooks](ui-extensions-quickbooks-payroll.md)  
* [Extension WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Extension GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
* [Extension QuickBooks Online Data Migration](ui-extensions-quickbooks-online-data-migration.md)
* [Portail Comptable](ui-extensions-accountant-portal.md)  
* [Analyseur Image](ui-extensions-image-analyzer.md)
* [Paiements et rapprochements (DK)](ui-extensions-payments-reconciliation-formats-dk.md)
* [C5 Data Migration](ui-extensions-c5-data-migration.md)

> [!NOTE]  
>  Les nouvelles extensions ne sont pas disponibles dans AppSource juste après l'annonce d'une mise à jour. Vous pouvez vous tenir informé sur les extensions sur le site [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Voir aussi
[Procédure: configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md)  
[Procédure : activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md)  
[Migrer des données métier à partir d'autres systèmes financiers](upload-data.md)  
[Configurer l'extension GetAddress.io UK Postal Code](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Extensions [!INCLUDE[d365fin](includes/d365fin_md.md)] par d'autres fournisseurs](ui-extensions-other.md)  
[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

