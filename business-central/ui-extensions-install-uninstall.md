---
title: Installer et désinstaller des applications
description: "Découvrez comment installer et désinstaller des applications et des extensions dans Business\_Central."
author: SusanneWindfeldPedersen
ms.author: solsen
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 20350'
---

# Installer et désinstaller des extensions (applications) dans Business Central

Vous pouvez modifier [!INCLUDE[prod_short](includes/prod_short.md)] en installant des applications qui, par exemple, ajoutent des fonctionnalités, modifient le comportement de l’application, ou vous permettent d’accéder à de nouveaux services en ligne. Pour plus d’informations, voir [Personnalisation de Business Central à l’aide d’extensions](ui-extensions.md).

> [!NOTE]
> Pour installer ou désinstaller des applications à partir de AppSource ou ajouter des applications par locataire, vous devez disposer des autorisations adéquates. Vous devez être membre du groupe d’utilisateurs Gestion des extensions D365 ou vous devez disposer de l’ensemble d’autorisations EXTEND. MGT. - ADMIN. Si vous êtes un administrateur, vous pouvez attribuer des groupes d’utilisateurs et des autorisations à d’autres utilisateurs de votre entreprise. Pour en savoir plus sur les groupes d’utilisateurs et les autorisations, consultez [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).
>
> Pour utiliser les fonctionnalités fournies par une extension, telles que l’ouverture de pages, la production de rapports, la sélection d’actions, etc., vous devez disposer des jeux d’autorisations installés avec cette extension.

Pour utiliser une extension, vous devez disposer des ensembles d’autorisations qui l’accompagnent.

## <a name="install"></a>Installer une extension

La page **Gestion des extensions** vous permet de gérer les applications et les extensions. Vous pouvez accéder à cette page à partir de la page d’accueil. Sinon, choisissez l’icône **Rechercher une page ou un état** ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis choisissez le lien associé.  

Vous pouvez obtenir de nouvelles applications depuis le marché à l’adresse [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Le marché propose toutes les applications disponibles pour [!INCLUDE[prod_short](includes/prod_short.md)], ainsi que des applications et des packs de contenu pour d’autres produits Microsoft. Définissez les filtres appropriés, observez les informations pour chaque extension et obtenez une extension pour votre [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Connectez-vous au site [AppSource.microsoft.com](https://appsource.microsoft.com/) à l’aide du compte de messagerie électronique que vous utilisez pour [!INCLUDE[prod_short](includes/prod_short.md)]. Utilisez le même compte de messagerie électronique pour d’autres services et produits pour une expérience agréable.  

Vous pouvez également accéder à AppSource depuis [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Gestion des extensions**, vous pouvez voir les applications actuellement installées, et vous pouvez ouvrir la page **Marché des extensions** qui affiche les applications [!INCLUDE[prod_short](includes/prod_short.md)] actuellement disponibles dans AppSource. Si vous optez pour le lien *Plus d’applications*, vous êtes dirigé vers le site [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Choisissez une application pour découvrir ses fonctionnalités, et vous pouvez accéder à l’aide de l’application pour en savoir plus. Lorsque vous choisissez d’obtenir une application, vous devez accepter ses conditions d’utilisation. Si vous obtenez l’application à partir du site web AppSource, vous serez connecté à [!INCLUDE[prod_short](includes/prod_short.md)] pour terminer l’installation.  

Après avoir installé une application, vous devrez peut-être la configurer. Certaines applications nécessitent que vous fournissiez certaines informations avant de pouvoir les utiliser. Par exemple, après avoir installé l’application **PayPal Payments Standard**, vous devez spécifier l’adresse e-mail ou l’ID de compte marchand de votre compte PayPal. Pour configurer une application ou pour connaître les informations dont vous aurez besoin, sur la page **Extensions installées**, choisissez l’action **Configurer**.  

D’autres applications ajoutent simplement des champs à une page existante, ou ajoutent une nouvelle page, par exemple.

Si vous désinstallez une application, et que vous changez ensuite d’avis, vous pouvez la réinstaller. Lorsque vous désinstallez une application que vous utilisiez, vos données ne sont pas supprimées. Les données sont disponibles si vous réinstallez l’application.

Certaines applications sont fournies par Microsoft, et d’autres sont fournies par [d’autres sociétés](ui-extensions-other.md). Nous vous recommandons d’en savoir plus sur l’application avant de choisir de l’installer.

Microsoft fournit les applications suivantes :

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
* [Importer le fichier de paie de Quickbooks](ui-extensions-quickbooks-payroll.md)
* [Stock prévu et ventes prévues](ui-extensions-sales-forecast.md)
* [Groupe TVA](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – Migration de données C5](ui-extensions-c5-data-migration.md)
* [DK – Paiements et rapprochements](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Formats de fichier fiscal](ui-extensions-tax-file-formats-dk.md)
* [Extension des codes postaux du R.-U. GetAddress.io](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [É.-U./CA/R.-U./AU/N.-Z./AS – Envoi d’un avis de versement](ui-extensions-send-remittance-advice.md)

## Configurer une application

Après avoir installé une application, vous devrez peut-être la configurer. Par exemple, pour l’application **PayPal Payments Standard pour [!INCLUDE[prod_short](includes/prod_short.md)]**, vous devez spécifier le compte PayPal à utiliser. Si tel est le cas, une fois l’installation terminée, [!INCLUDE[prod_short](includes/prod_short.md)] vous demande si vous souhaitez configurer l’application immédiatement. Les configurations peuvent être requises pour que l’application fonctionne, ou facultatives.

Si vous choisissez de configurer votre application immédiatement et qu’elle a une configuration requise, [!INCLUDE[prod_short](includes/prod_short.md)] ouvre la configuration requise. La configuration peut être soit une page où vous entrez des informations, soit un guide de configuration assistée qui vous aide à travers les étapes. Si vous ne terminez pas la configuration en une seule fois, vous pouvez utiliser la page **Configurations pour _nom de l’application_**, qui répertorie toutes les configurations de l’application. Configurations requises indiquées en **caractères gras**.

## Charger une extension par locataire (PTE)

Vous chargez un PTE en utilisant la page **Gestion des extensions**. Sur la page **Gestion des extensions**, accédez à **Gérer**, puis sélectionnez **Charger une extension**. Sur la page **Charger et déployer l’extension**, spécifiez le fichier .app à charger. Pour continuer, choisissez le bouton **Accepter**, puis le bouton **Déployer**, ce qui lancera le processus de déploiement du PTE.

Si le PTE contient d’importantes modifications de schéma, il est possible de *forcer* son chargement. Pour ce faire, dans **Mode de synchronisation des schémas**, sélectionnez l’option **Forcer**. Vous verrez une boîte de dialogue de confirmation qui vous permettra d’accepter avant de continuer.  

## Désinstaller une application

Pour désinstaller une application, allez sur la page **Gestion des extensions**. Pour désinstaller une application, sélectionnez-la sur la page, puis sélectionnez l’action **Désinstaller**. Si vous désinstallez une application, et que vous changez d’avis ensuite, vous pouvez la réinstaller à nouveau.

Par défaut, lorsque vous désinstallez une application que vous utilisiez, vos données ne sont pas supprimées. Si vous êtes sûr de ne plus installer l’application, vous pouvez supprimer les données lorsque vous la désinstallez. Pour supprimer les données lorsque vous désinstallez une application, activez le bouton bascule **Supprimer les données d’extension**. Une boîte de dialogue de confirmation s’affiche et vous devez choisir **Oui** pour l’activer. Lorsque l’option **Supprimer les données d’extension** est activée, vous pouvez désinstaller l’application, et il vous sera demandé de reconfirmer que vous souhaitez désinstaller l’application et supprimer les données.

> [!IMPORTANT]  
> * Des applications peuvent nécessiter ou dépendre de l’application que vous souhaitez désinstaller. Ces applications sont appelées *dépendances*. Vous ne pouvez pas désinstaller une application à moins de désinstaller également ses dépendances. Lorsque vous désinstallez une application avec des dépendances, une boîte de dialogue répertorie les dépendances. Pour continuer, vous devrez sélectionner **Oui** pour désinstaller l’application et ses dépendances.
> * Si vous activez le bouton bascule **Supprimer les données d’extension**, la désinstallation de l’application supprime toutes les données de l’application *ainsi que* les données de toutes les applications dépendantes. L’action ne peut pas être annulée.
> * Certaines applications sont nécessaires et vous ne pouvez pas les supprimer sur la page **Gestion des extensions**.  

## Voir aussi

[Personnalisation de Business Central](ui-customizing-overview.md)  
[Extensions Business Central par d’autres fournisseurs](ui-extensions-other.md)  
[Configuration du service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md)  
[Migrer des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configurer l’extension GetAddress.io UK Postal Code](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Extensions [!INCLUDE[prod_short](includes/prod_short.md)] par d’autres fournisseurs](ui-extensions-other.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]