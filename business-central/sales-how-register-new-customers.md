---
title: Créer une fiche client pour enregistrer de nouveaux clients | Microsoft Docs
description: Décrit comment créer une fiche client pour enregistrer des informations sur chaque nouveau client ou client auquel vous vendez.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a6404d39723df3d6c0d14ab7ff2bae783222dc67
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910990"
---
# <a name="register-new-customers"></a>Enregistrer de nouveaux clients
Les clients sont l'origine de vos revenus. Chaque client auquel vous vendez un élément doit être enregistré en tant que fiche client. Les fiches client contiennent les informations nécessaires à la vente de biens au client. Pour plus d'informations, voir [Facturer des ventes](sales-how-invoice-sales.md) et [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).  

Avant de pouvoir enregistrer de nouveaux clients, vous devez configurer divers codes vente que vous pouvez sélectionner lorsque vous renseignez les fiches client. Pour plus d'informations, reportez-vous à [Définition des ventes](sales-setup-sales.md).

> [!NOTE]  
>   Si des modèles client existent pour différents types de clients, une page s'affiche lorsque vous créez une nouvelle fiche client à partir de laquelle vous pouvez sélectionner un modèle client approprié. Si un seul modèle client existe, les nouvelles fiches client utiliseront toujours ce modèle.  
<br><br>  
<br><br>  
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="to-create-a-new-customer-card"></a>Pour créer une fiche client
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.  
2. Sur la page **Clients**, sélectionnez l'action **Nouveau**.

    Si un seul modèle client existe, une nouvelle fiche client avec certains champs renseignés à l'aide des informations provenant du modèle s'ouvre.

    Si plusieurs modèles client existent, une page s'affiche et vous permet de sélectionner un modèle client. Dans ce cas, suivez les deux étapes suivantes.
3. Sur la page **Sélectionnez un modèle pour un nouveau client**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche client.
4. Cliquez sur le bouton **OK**. Une fiche client avec certains champs contenant les informations provenant de ce modèle s'ouvre.  
5. Renseignez ou modifiez les champs de la fiche client selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sur le raccourci **Prix vente**, vous pouvez afficher les prix spéciaux ou les remises accordées au client si certains critères sont réunis, par exemple l'article, la quantité minimum commande ou la date de fin. Chaque ligne représente un prix spécial ou une remise ligne. Chaque colonne représente un critère qui doit s'appliquer pour garantir le prix spécial que vous saisissez dans le champ **Prix** ou la remise ligne que vous saisissez dans le champ **% remise ligne**. Pour plus d'informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).

Le client est désormais enregistré, et la fiche client est prête à être utilisée sur les documents vente.

Si vous souhaitez utiliser cette fiche client comme modèle lorsque vous créez de nouvelles fiches client, enregistrez-la comme modèle. Pour plus d'informations, reportez-vous à la section suivante.

## <a name="to-save-the-customer-card-as-a-template"></a>Pour enregistrer la fiche client en tant que modèle
1. Sur la page **Fiche client**, sélectionnez l'action **Sauvegarder comme modèle**. La page **Modèle client** s'ouvre et affiche la fiche client comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles, sélectionnez l'action **Axes analytiques**. La page **Modèles axe** s'ouvre et affiche tous les codes axe qui sont définis pour le client.
4. Modifiez ou entrez les codes axe s'appliquant aux nouvelles fiches client créées à l'aide du modèle.  
5. Lorsque vous avez terminé le nouveau modèle client, cliquez sur le bouton **OK**.

Le modèle client est ajouté à la liste des modèles client. Vous pouvez ainsi l'utiliser pour créer des fiches client.

## <a name="see-also"></a>Voir aussi
[Définition des modes de règlement](finance-payment-methods.md)  
[Fusionner l'enregistrement des doublons](sales-how-merge-duplicate-records.md)  
[Création des souches de numéros](ui-create-number-series.md)  
[Ventes](sales-manage-sales.md)    
[Définition des ventes](sales-setup-sales.md)    
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
