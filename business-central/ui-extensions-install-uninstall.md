---
title: Installation et désinstallation d’extensions dans Business Central | Microsoft Docs
description: Installation et désinstallation d’extensions dans Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 09/04/2020
ms.author: solsen
ms.openlocfilehash: da6e53a314438ef7ce5063febf8ece1d18c69f7b
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766106"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Installation et désinstallation d’extensions dans Business Central

Vous pouvez modifier [!INCLUDE[d365fin](includes/d365fin_md.md)] en installant des extensions qui, par exemple, ajoutent des fonctionnalités, modifient le comportement de l'application, ou vous permettent d'accéder à de nouveaux services en ligne. Pour plus d'informations, voir [Personnalisation de Business Central à l'aide d'extensions](ui-extensions.md).

> [!NOTE]
> Pour installer des extensions à partir de AppSource ou ajouter des extensions par locataire, vous devez disposer des autorisations adéquates. Vous devez être membre du groupe d'utilisateurs D365 EXTENSION MGMT ou disposer du jeu d'autorisations D365 EXTENSION MGMT. Si vous êtes un administrateur, vous pouvez attribuer des groupes d'utilisateurs et des autorisations à d'autres utilisateurs de votre entreprise.<br /><br />
Pour utiliser les fonctionnalités fournies par une extension, telles que l'ouverture de pages, la production de rapports, la sélection d'actions, etc., vous devez disposer des jeux d'autorisations installés avec cette extension.

## <a name="installing-an-extension"></a>Installation d'une extension

La page **Gestion des extensions** vous permet de gérer les extensions. Vous pouvez accéder à cette page à partir de la page d'accueil. Sinon, choisissez l'icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis sélectionnez le lien associé.  

Vous pouvez obtenir de nouvelles extensions depuis le marché à l'adresse [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Ici, vous trouverez toutes les extensions disponibles pour [!INCLUDE[d365fin](includes/d365fin_md.md)], et vous pourrez obtenir des applications, des extensions et des packs de contenu pour d'autres produits Microsoft. Définissez les filtres appropriés, observez les informations pour chaque extension et obtenez une extension pour votre [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
> Connectez-vous au site [AppSource.microsoft.com](https://appsource.microsoft.com/) à l'aide du compte de messagerie électronique que vous utilisez pour [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilisez le même compte de messagerie électronique pour d'autres services et produits pour une expérience agréable.  

Vous pouvez également accéder au marché à partir de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Sur la page **Gestion des extensions**, vous pouvez voir les extensions actuellement installées, et vous pouvez ouvrir la page **Marché des extensions** qui affiche les extensions [!INCLUDE[d365fin](includes/d365fin_md.md)] actuellement disponibles dans AppSource. Si vous optez pour le lien *Plus d'applications*, vous êtes dirigé vers le site [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Si vous choisissez une extension, vous pouvez consulter une documentation relative à ses fonctionnalités, et accéder au service d'aide de l'extension pour en savoir plus. Lorsque vous choisissez d'obtenir une extension, vous devez être d'accord avec les conditions d'utilisation. Si vous obtenez l'extension à partir du site Web AppSource, vous serez connecté à [!INCLUDE[d365fin](includes/d365fin_md.md)] pour terminer l'installation.  

Lorsque vous installez une extension, vous pouvez être amené à la configurer, par exemple spécifier un compte à utiliser avec l'extension **PayPal Payments Standard pour [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
D'autres extensions ajoutent simplement des champs à une page existante, ou ajoutent une nouvelle page, par exemple.

Si vous désinstallez une extension, et que vous changez ensuite d'avis, vous pouvez la réinstaller. Lorsque vous désinstallez une extension que vous avez utilisée, les données sont conservées de sorte à demeurer disponibles si vous installez à nouveau l'extension. Certaines extensions sont nécessaires. Vous ne pouvez pas les désinstaller à partir de la page **Gestion des extensions**. Si vous essayez, un message d'erreur apparaît.

Certaines extensions sont fournies par Microsoft, et d'autres sont fournies par [d'autres sociétés](ui-extensions-other.md). Toutes les sont extensions testées avant d'être mises à votre disposition, mais nous vous recommandons d'accéder aux liens qui sont inclus dans chaque extension pour en savoir plus sur l'extension avant de décider de l'installer.

Microsoft fournit les extensions suivantes :

* [Portail Comptable pour Business Central](ui-extensions-accountant-portal.md)  
* [Extension Ceridian Payroll](ui-extensions-ceridian-payroll.md) 
* [Migration de données Dynamics GP](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md) 
* [Informations commerciales essentielles](ui-extensions-essential-business-insights.md)   
* [Analyseur Image](ui-extensions-image-analyzer.md) 
* [Cloud intelligent](ui-extensions-data-replication.md)    
* [Base du Cloud intelligent](ui-extensions-intelligent-cloud.md)  
* [Prévisions de retard de paiement](ui-extensions-late-payment-prediction.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md) 
* [Extension QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md)   
* [Migration des données QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md) 
* [Extension Importer le fichier de paie de Quickbooks](ui-extensions-quickbooks-payroll.md) 
* [Stock prévu et ventes prévues](ui-extensions-sales-forecast.md)   
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md) 
* [Extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)    
* [DK - Migration de données C5](ui-extensions-c5-data-migration.md)  
* [DK - Paiements et rapprochements](ui-extensions-payments-reconciliation-formats-dk.md)  
* [DK - Formats de fichier fiscal](ui-extensions-tax-file-formats-dk.md) 
* [RU - Extension GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Envoi d'un avis de versement](ui-extensions-send-remittance-advice.md) 
* [Extensions Business Central par d'autres fournisseurs](ui-extensions-other.md)

## <a name="uninstalling-an-extension"></a>Désinstallation d'une extension

Pour désinstaller une extension, allez sur la page **Gestion des extensions**. Si vous désinstallez une extension, et que vous changez d'avis ensuite, vous pouvez la réinstaller à nouveau. Lorsque vous désinstallez une extension que vous avez utilisée, les données sont conservées par défaut si vous installez à nouveau l'extension. Vous pouvez à la place choisir de supprimer les données avec l'extension. Ceci est contrôlé par la case à cocher **Supprimer les données d'extension**. Par défaut, cette case *n'est pas activée*.

> [!IMPORTANT]  
> Si vous activez la case à cocher **Supprimer les données d'extension**, une boîte de dialogue de confirmation s'affiche et vous devez choisir **OK**. Si la case à cocher **Supprimer les données d'extension** est activée, vous pouvez désormais désinstaller l'extension, et il vous sera demandé de reconfirmer que vous souhaitez désinstaller l'extension et supprimer les données. L'action ne peut pas être annulée.
Certaines extensions sont requises. Vous ne pouvez pas les désinstaller à partir de la page **Gestion des extensions**. Si vous essayez, un message d'erreur apparaît.  


## <a name="see-also"></a>Voir aussi
[Extension de Dynamics 365 Business Central](about-develop-extensions.md)  
[Extensions Business Central par d'autres fournisseurs](ui-extensions-other.md)  
[Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md)  
[Migration des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de l'extension GetAddress.io UK Postal Code](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Extensions [!INCLUDE[d365fin](includes/d365fin_md.md)] par d'autres fournisseurs](ui-extensions-other.md)  
[Mise en route](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
