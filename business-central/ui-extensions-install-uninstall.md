---
title: Installer et désinstaller des extensions
description: Installation et désinstallation d’extensions dans Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 03/25/2022
ms.author: solsen
ms.openlocfilehash: fcdfe843071bc416973b7411e5702a690e7e377d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514766"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Installer et désinstaller des extensions dans Business Central

Vous pouvez modifier [!INCLUDE[prod_short](includes/prod_short.md)] en installant des extensions qui, par exemple, ajoutent des fonctionnalités, modifient le comportement de l’application, ou vous permettent d’accéder à de nouveaux services en ligne. Pour plus d’informations, voir [Personnalisation de Business Central à l’aide d’extensions](ui-extensions.md).

> [!NOTE]
> Pour installer ou désinstaller des extensions à partir de AppSource ou ajouter des extensions par locataire, vous devez disposer des autorisations adéquates. Vous devez soit être membre du groupe d’utilisateurs EXTEND. MGT. - ADMIN ou l’ensemble d’autorisation EXTEND. MGT. - ADMIN doit vous être accordé. Si vous êtes un administrateur, vous pouvez attribuer des groupes d’utilisateurs et des autorisations à d’autres utilisateurs de votre entreprise.
>
> Pour utiliser les fonctionnalités fournies par une extension, telles que l’ouverture de pages, la production de rapports, la sélection d’actions, etc., vous devez disposer des jeux d’autorisations installés avec cette extension.

> [!NOTE]  
> L’ensemble d’autorisations **EXTEND. MGT. - ADMIN** a été introduit dans la première vague de lancement de Business Central 2021 pour remplacer l’ensemble d’autorisations **D365 EXTENSION MGT** des versions antérieures.

## <a name="install-an-extension"></a><a name="install"></a>Installer une extension

La page **Gestion des extensions** vous permet de gérer les extensions. Vous pouvez accéder à cette page à partir de la page d’accueil. Sinon, choisissez l’icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis choisissez le lien associé.  

Vous pouvez obtenir de nouvelles extensions depuis le marché à l’adresse [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Ici, vous trouverez toutes les extensions disponibles pour [!INCLUDE[prod_short](includes/prod_short.md)], et vous pourrez obtenir des applications, des extensions et des packs de contenu pour d’autres produits Microsoft. Définissez les filtres appropriés, observez les informations pour chaque extension et obtenez une extension pour votre [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Connectez-vous au site [AppSource.microsoft.com](https://appsource.microsoft.com/) à l’aide du compte de messagerie électronique que vous utilisez pour [!INCLUDE[prod_short](includes/prod_short.md)]. Utilisez le même compte de messagerie électronique pour d’autres services et produits pour une expérience agréable.  

Vous pouvez également accéder au marché à partir de [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Gestion des extensions**, vous pouvez voir les extensions actuellement installées, et vous pouvez ouvrir la page **Marché des extensions** qui affiche les extensions [!INCLUDE[prod_short](includes/prod_short.md)] actuellement disponibles dans AppSource. Si vous optez pour le lien *Plus d’applications*, vous êtes dirigé vers le site [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Si vous choisissez une extension, vous pouvez consulter une documentation relative à ses fonctionnalités, et accéder au service d’aide de l’extension pour en savoir plus. Lorsque vous choisissez d’obtenir une extension, vous devez être d’accord avec les conditions d’utilisation. Si vous obtenez l’extension à partir du site Web AppSource, vous serez connecté à [!INCLUDE[prod_short](includes/prod_short.md)] pour terminer l’installation.  

Lorsque vous installez une extension, vous pouvez être amené à la configurer, par exemple spécifier un compte à utiliser avec l’extension **PayPal Payments Standard pour [!INCLUDE[prod_short](includes/prod_short.md)]**.
D’autres extensions ajoutent simplement des champs à une page existante, ou ajoutent une nouvelle page, par exemple.

Si vous désinstallez une extension, et que vous changez ensuite d’avis, vous pouvez la réinstaller. Lorsque vous désinstallez une extension que vous avez utilisée, les données sont conservées de sorte à demeurer disponibles si vous installez à nouveau l’extension. Certaines extensions sont nécessaires. Vous ne pouvez pas les désinstaller à partir de la page **Gestion des extensions**. Si vous essayez, un message d’erreur apparaît.

Certaines extensions sont fournies par Microsoft, et d’autres sont fournies par [d’autres sociétés](ui-extensions-other.md). Toutes les sont extensions testées avant d’être mises à votre disposition, mais nous vous recommandons d’accéder aux liens qui sont inclus dans chaque extension pour en savoir plus sur l’extension avant de décider de l’installer.

Microsoft fournit les extensions suivantes :

* [Extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
* [Extension Ceridian Payroll](ui-extensions-ceridian-payroll.md)
* [Hub Entreprise](ui-extensions-company-hub.md)  
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
* [Groupe TVA](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – Migration de données C5](ui-extensions-c5-data-migration.md)
* [DK – Paiements et rapprochements](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Formats de fichier fiscal](ui-extensions-tax-file-formats-dk.md)
* [Extension GetAddress.io UK Postcodes](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [É.-U./CA/R.-U./AU/N.-Z./ZA – Envoi d’un avis de versement](ui-extensions-send-remittance-advice.md)

## <a name="upload-a-per-tenant-extension-pte"></a>Charger une extension par locataire (PTE)

Vous chargez un PTE en utilisant la page **Gestion des extensions**. Sur la page **Gestion des extensions**, accédez à **Gérer**, puis sélectionnez **Charger une extension**. Sur la page **Charger et déployer l’extension**, spécifiez le fichier .app à charger. Pour continuer, choisissez le bouton **Accepter**, puis le bouton **Déployer** ; cela lancera le processus de déploiement du PTE.

Si le PTE contient d’importantes modifications de schéma, il est possible de *forcer* son chargement. Pour ce faire, en **Mode de synchronisation des schémas**, sélectionnez l’option **Forcer**. Vous verrez une boîte de dialogue de confirmation pour accepter avant de continuer.  

## <a name="uninstall-an-extension"></a>Désinstaller une extension

Pour désinstaller une extension, allez sur la page **Gestion des extensions**. Si vous désinstallez une extension, et que vous changez d’avis ensuite, vous pouvez la réinstaller à nouveau. Lorsque vous désinstallez une extension que vous avez utilisée, les données sont conservées par défaut si vous installez à nouveau l’extension. Vous pouvez à la place choisir de supprimer les données avec l’extension. Ceci est contrôlé par la case à cocher **Supprimer les données d’extension**. Par défaut, cette case *n’est pas activée*.

> [!IMPORTANT]  
> Si vous activez la case à cocher **Supprimer les données d’extension**, une boîte de dialogue de confirmation s’affiche et vous devez choisir **OK**. Si la case à cocher **Supprimer les données d’extension** est activée, vous pouvez désormais désinstaller l’extension, et il vous sera demandé de reconfirmer que vous souhaitez désinstaller l’extension et supprimer les données. L’action ne peut pas être annulée.
Certaines extensions sont requises. Vous ne pouvez pas les désinstaller à partir de la page **Gestion des extensions**. Si vous essayez, un message d’erreur apparaît.  

## <a name="see-also"></a>Voir aussi

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