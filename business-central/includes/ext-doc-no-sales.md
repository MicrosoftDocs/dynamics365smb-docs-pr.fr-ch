---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116081"
---
Sur les documents et les feuilles vente, vous pouvez spécifier un numéro de document faisant référence au système de numérotation du client. <!--You can enter a maximum of ten characters, both numbers and letters.--> Utilisez ce champ pour enregistrer le numéro que le client a attribué à la commande, à la facture ou à l’avoir. Vous pouvez utiliser ce numéro ultérieurment, si vous avez besoin de retrouver l’écriture validée à l’aide de ce numéro.  

Le champ **N° doc. ext. obligatoire** de la page **Paramètres ventes** précise s’il est obligatoire de saisir un numéro de document externe dans le champ **N° doc. externe** sur un en-tête vente et dans le champ **N° doc. externe** dans une ligne feuille comptabilité.

Si vous sélectionnez ce champ, il est impossible de valider une facture ou une ligne feuille sans numéro de document externe.

Le numéro de document externe est inclus dans les documents validés où vous pouvez effectuer une recherche d’après le numéro pertinent. Vous pouvez également effectuer une recherche à l’aide du numéro de document externe lors de la navigation sur les écritures comptables client.

Une autre façon de gérer les numéros de document externe consiste à utiliser le champ **Votre référence**. Si vous utilisez le champ **Votre référence**, le numéro sera inclus dans les documents validés, et vous pouvez le rechercher de la même manière que vous recherchez les valeurs dans les champs **N° de document externe**. Mais le champ n’est pas disponible sur les lignes feuille.
