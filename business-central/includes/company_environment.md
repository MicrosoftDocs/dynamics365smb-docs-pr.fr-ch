---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 77a6d87d56475aa9e649ece545764f3f362d055b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914504"
---
Les gens prennent parfois en charge plus d’une société et doivent facilement passer du travail dans une société à une autre dans [!INCLUDE [prodshort](prodshort.md)]. Par exemple, une entreprise peut avoir des bureaux de vente dans des villes et plusieurs pays, elle a donc créé un centre de profit pour chaque bureau. Les bureaux situés dans le même pays sont constitués en sociétés distinctes dans un environnement partagé. D’autres bureaux sont créés en tant que sociétés dans des environnements distincts car ils sont géographiquement basés dans d’autres pays.  

Qu’est-ce qu’un environnement ? Les sociétés dans [!INCLUDE[prodshort](prodshort.md)] existent dans ce qu’on appelle des *environnements* . Il existe deux types d’environnements, **Production** et **Sandbox** . En bref, les environnements de production contiennent des données métier en direct et les environnements sandbox sont utilisés comme un endroit sûr pour tester des choses comme de nouveaux processus ou fonctionnalités métier. Pour plus d’informations, voir [Types d’environnements](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments). Si vous avez accès à une société, vous avez accès à l’environnement dans lequel elle se trouve. Si vous avez accès à plusieurs sociétés et que celles-ci se trouvent dans des environnements différents, lorsque vous vous connectez à [!INCLUDE[prodshort](prodshort.md)] vous devez spécifier l’environnement dans lequel vous souhaitez travailler. Les environnements sont particuliers à un pays donné, donc si votre organisation travaille dans plusieurs pays, vous avez besoin d’environnements distincts pour chaque pays.  

Qu’est-ce qu’une société ? Considérez une *société* en tant que conteneur contenant des informations sur une entité juridique. En utilisant l’exemple ci-dessus, l’entreprise a un bureau de vente à Seattle et un autre à New York, donc elle crée une société à [!INCLUDE[prodshort](prodshort.md)] pour chaque bureau afin qu’elle puisse gérer les opérations pour chaque bureau séparément.  
