---
title: Utilisez vos données pour créer une application | Microsoft Docs
description: Vous pouvez rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer une application métier à l'aide de Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 8f0eb7a1562a8300bd7181ef6470c70f60934470
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528653"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Connexion à vos données Business Central pour générer un application professionnelle à l'aide de Power Apps

Vous pouvez rendre vos données [!INCLUDE[prodshort](includes/prodshort.md)] disponibles sous forme de source de données dans Power Apps.  

> [!NOTE]  
> Vous devez disposer d'un compte valide avec [!INCLUDE[prodshort](includes/prodshort.md)] et avec Power Apps.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>Pour ajouter [!INCLUDE[prodshort](includes/prodshort.md)] comme source de données dans Power Apps

1. Dans votre navigateur, accédez à [powerapps.microsoft.com](https://powerapps.microsoft.com/), puis connectez-vous.
2. Sur la page d'accueil, dans la section **Commencer à partir des données**, choisissez la vignette **Autres sources de données**.  

    Cela ouvre Power Apps Studio. Lors de la première connexion, vous devez spécifier le pays / la région.  
3. Dans la liste des connexions disponibles, choisissez **Business Central**, puis choisissez le bouton **Créer**.

    Power Apps se connectera à votre [!INCLUDE[prodshort](includes/prodshort.md)] à l'aide des informations d'identification avec lesquelles vous vous êtes connecté. Si vous n'êtes pas un administrateur de votre [!INCLUDE[prodshort](includes/prodshort.md)], vous devrez peut-être vous connecter avec un autre compte.  

4. Power Apps affiche la liste *Environnements et des sociétés* disponibles à partir de [!INCLUDE[prodshort](includes/prodshort.md)]. Choisissez l'environnement et la société contenant les données auxquelles vous souhaitez vous connecter, comme *PRODUCTION - Ma société*.  

5. Ensuite, une liste de tables qui sont exposées dans le cadre de l'API pour votre environnement vous sera présentée. Sélectionnez la table à laquelle vous souhaitez vous connecter, puis choisissez **Connecter**.

Ces tables sont exposées en tant que points de terminaison par le connecteur [!INCLUDE[prodshort](includes/prodshort.md)] pour Power Apps.  

> [!NOTE]
> Si vous souhaitez inclure des données d'autres tables de [!INCLUDE[prodshort](includes/prodshort.md)] dans votre application, vous devez faire appel à un développeur pour définir une API personnalisée [!INCLUDE[prodshort](includes/prodshort.md)] et utiliser cette API personnalisée via un connecteur personnalisé dans Power Apps. Pour plus d'informations, voir [Créer un connecteur personnalisé à partir de zéro](/connectors/custom-connectors/define-blank).  

À ce stade, vous êtes connecté à vos données [!INCLUDE[prodshort](includes/prodshort.md)] et vous êtes prêt à générer votre application PowerApp. Vous pouvez ajouter des écrans supplémentaires et vous connecter à des données supplémentaires à partir de votre [!INCLUDE[prodshort](includes/prodshort.md)]. Pour plus d'informations, voir [Créer une application de canevas à partir d'un exemple dans Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Lorsque vous avez conçu et créé votre application, vous pouvez la partager avec vos collègues. Pour plus d'informations, voir [Enregistrer et publier une application de canevas dans Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Si vous souhaitez vous connecter à [!INCLUDE[prodshort](includes/prodshort.md)] sur site, vous devez choisir le connecteur **Business Central (sur site)** dans l'étape 3.  

## <a name="see-also"></a>Voir aussi

[Créer une application de canevas à partir d'un modèle dans Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importation des données métier à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Familiarisation avec le développement d'applications connectées pour Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
