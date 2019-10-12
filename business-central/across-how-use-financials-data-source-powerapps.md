---
title: Utilisez vos données pour créer une application | Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer une application métier à l'aide de PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305052"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Connexion à vos données Business Central pour générer un application professionnelle à l'aide de PowerApps
Vous pouvez rendre vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles sous forme de source de données dans PowerApps.  

> [!NOTE]  
>   Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec PowerApps.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans PowerApps
1. Dans votre navigateur, accédez à [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), puis connectez-vous.
2. Sur la page d'accueil, choisissez **Applications**, **Créez une application** et **Canevas** pour créer une application de canevas. Cette application sera conçue pour être utilisée sur un appareil mobile, mais vous pouvez également choisir d'utiliser un autre modèle.

    L'étape suivante pour créer un PowerApp consiste à sélectionner vos données. Cliquez sur l'icône représentant une flèche et choisissez l'option **Nouvelle connexion** dans le coin supérieur gauche de la page.
3. Dans la liste des connexions disponibles, choisissez **Business Central**, puis choisissez le bouton **Créer**.

    PowerApps se connectera à votre [!INCLUDE [prodshort](includes/prodshort.md)] à l'aide des informations d'identification avec lesquelles vous vous êtes connecté. Si vous n'êtes pas un administrateur de votre [!INCLUDE [prodshort](includes/prodshort.md)], vous devrez peut-être vous connecter avec un autre compte.  

4.  PowerApps affiche la liste *Environnements et des sociétés* disponibles à partir de [!INCLUDE [prodshort](includes/prodshort.md)]. Choisissez l'environnement et la société contenant les données auxquelles vous souhaitez vous connecter. Une liste d’API est ensuite présentée. Sélectionnez l'**API**à laquelle vous voulez vous connecter.

Ces tables font partie de l'API [!INCLUDE [prodshort](includes/prodshort.md)]. Il n'est pas nécessaire de configurer les points de terminaison vous-même, le connecteur [!INCLUDE [prodshort](includes/prodshort.md)] pour PowerApps s'en charge à votre place.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

À ce stade, vous êtes connecté à vos données [!INCLUDE [prodshort](includes/prodshort.md)] et vous êtes prêt à générer votre application PowerApp. Vous pouvez ajouter des écrans supplémentaires et vous connecter à des données supplémentaires à partir de votre [!INCLUDE [prodshort](includes/prodshort.md)]. Pour plus d'informations, voir [Créer une application de canevas à partir d'un modèle dans PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Lorsque vous avez conçu et créé votre application, vous pouvez la partager avec vos collègues. Pour plus d'informations, voir [Enregistrer et publier une application de canevas dans PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Si vous souhaitez vous connecter à [!INCLUDE [prodshort](includes/prodshort.md)] sur site, vous devez choisir le connecteur **Business Central (sur site)** dans l'étape 3.  

## <a name="see-also"></a>Voir aussi

[Créer une application de canevas à partir d'un modèle dans PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Mise en route](product-get-started.md)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finances](finance.md)  
[Familiarisation avec le développement d'applications connectées pour Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
