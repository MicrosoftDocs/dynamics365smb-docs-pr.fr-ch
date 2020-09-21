---
title: Installation d'extensions pour personnaliser Business Central | Microsoft Docs
description: En savoir plus sur l'ajout des fonctionnalités et la personnalisation de Business Central en installant des extensions.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765936"
---
# <a name="customizing-business-central-using-extensions"></a>Personnalisation de Business Central à l'aide d'extensions

Vous pouvez modifier [!INCLUDE[d365fin](includes/d365fin_md.md)] en installant des extensions qui ajoutent des fonctionnalités, modifient le comportement de l'application, ou vous permettent d'accéder à de nouveaux services en ligne, par exemple.

> [!NOTE]
> Pour installer des extensions à partir de AppSource ou ajouter des extensions par locataire, vous devez disposer des autorisations adéquates. Vous devez être membre du groupe d'utilisateurs D365 EXTENSION MGMT ou disposer du jeu d'autorisations D365 EXTENSION MGMT. Si vous êtes un administrateur, vous pouvez attribuer des groupes d'utilisateurs et des autorisations à d'autres utilisateurs de votre entreprise.<br /><br />
Pour utiliser les fonctionnalités fournies par une extension, telles que l'ouverture de pages, la production de rapports, la sélection d'actions, etc., vous devez disposer des jeux d'autorisations installés avec cette extension.

> [!IMPORTANT]  
> Le chargement des extensions par client et l'installation des extensions AppSource ne sont pas pris en charge via la page **Gestion des extensions** pour les installations sur site.

La première fois que vous lancez [!INCLUDE[d365fin](includes/d365fin_md.md)], certaines extensions sont déjà installées. Au fil du temps, davantage d'extensions seront disponibles. Il vous appartient de choisir si vous souhaitez les utiliser ou non.

Par exemple, Microsoft propose une extension qui fournit une intégration à PayPal Payments Standard. Cette extension est installée par défaut.
Si une autre extension proposant une intégration à un autre service de paiement devenait disponible, vous pouvez installer cette nouvelle extension et choisir lequel des deux services vous souhaitez utiliser.  

La page **Gestion des extensions** vous permet de gérer les extensions. Vous pouvez accéder à cette page à partir de la page d'accueil. Sinon, choisissez l'icône **Page ou état pour la recherche** ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") dans le coin supérieur droit, entrez **Extension**, puis sélectionnez le lien associé. Pour plus d’informations, consultez [Installation et désinstallation d’extensions](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Si vous voulez accéder à une extension mais que vous ne pouvez pas trouver sa fonctionnalité, vérifiez la page **Gestion des extensions**, si l'extension n'est pas répertoriée, vous pouvez la configurer comme décrit dans la section suivante.  

> [!NOTE]  
> Les nouvelles extensions ne sont pas disponibles dans AppSource juste après l'annonce d'une mise à jour. Vous pouvez vous tenir informé sur les extensions sur le site [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

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
