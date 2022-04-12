---
title: Champs obligatoires pour exécuter les processus
description: En savoir plus sur les champs marqués avec un astérisque rouge, ce qui indique qu’ils sont requis et doivent être renseignés pour exécuter les processus.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: fd114fab64ac6d3f33db2b281d39c9d7a9fc9a1f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513513"
---
# <a name="detecting-mandatory-fields"></a>Détection de champs obligatoires
Lorsque vous entrez des données sur les pages dans [!INCLUDE[prod_short](includes/prod_short.md)], certains champs sont marqués par un astérisque rouge. L’astérisque rouge signifie que le champ doit être renseigné pour terminer un processus qui utilise ce champ, par exemple, valider une transaction qui utilise la valeur du champ.

Même si le champ contient un astérisque rouge, vous n’êtes pas forcé de remplir le champ avant de poursuivre avec les autres champs ou fermer la page. L’astérisque rouge sert uniquement à rappeler que la fin d’un certain processus restera bloquée.

## <a name="examples"></a>Exemples
Sur la page **Fiche client**, l’astérisque rouge figure dans le champ **Nom**, dans le champ **Code zone recouvrement** et dans les champs de groupe comptabilisation pour indiquer que vous ne pouvez pas valider une transaction de vente pour le client à moins que les champs soient renseignés.

Sur la page **Fiche article**, l’astérisque rouge figure dans le champ **Description** pour indiquer que vous ne pouvez pas entrer l’article dans une ligne document, par exemple une commande vente, à moins que ce champ soient renseigné.

## <a name="see-also"></a>Voir aussi
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]