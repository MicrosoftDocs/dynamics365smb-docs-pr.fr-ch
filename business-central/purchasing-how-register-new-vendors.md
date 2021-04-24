---
title: Créer une fiche fournisseur pour enregistrer de nouveaux fournisseurs | Microsoft Docs
description: Apprendre comment créer une fiche fournisseur pour enregistrer un nouveau fournisseur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772694"
---
# <a name="register-new-vendors"></a>Enregistrer un nouveau fournisseur

Les fournisseurs fournissent les produits que vous vendez. Chaque fournisseur à qui vous achetez des biens doit être enregistré en tant que fiche fournisseur.

Avant de pouvoir enregistrer de nouveaux fournisseurs, vous devez configurer divers codes achat que vous pouvez sélectionner lorsque vous renseignez les fiches fournisseur. Lorsque toutes les données de base requises sont créées, vous pouvez configurer des éléments supplémentaires sur le fournisseur, comme par exemple attribuer une priorité au fournisseur à des fins de paiement et répertorier les articles que les fournisseurs peuvent fournir. Un autre groupe de tâches de configuration consiste à enregistrer vos accords concernant les remises, les prix et les modes de règlement. Pour plus d’informations, reportez-vous à [Définition des achats](purchasing-setup-purchasing.md).

Les fiches fournisseur contiennent les informations requises pour acheter des produits au fournisseur. Pour plus d’informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md) et [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

> [!NOTE]  
> Si des modèles fournisseur existent pour différents types de fournisseurs, une page s’affiche lorsque vous créez une fiche fournisseur à partir de laquelle vous pouvez sélectionner un modèle approprié. Si un seul modèle fournisseur existe, les nouvelles fiches fournisseur utiliseront toujours ce modèle.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Ajouter de nouveaux fournisseurs

Pour enregistrer un nouveau fournisseur, vous devez remplir une fiche fournisseur. Vous pouvez créer des modèles pour différents profils de fournisseurs ou ajouter des fournisseurs sans modèles. Vous pouvez également créer un fournisseur à partir d'un contact. Pour plus d’informations, reportez-vous à [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d'un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Si des modèles fournisseur existent pour différents types de fournisseurs, une page s’affiche lorsque vous créez une fiche fournisseur à partir de laquelle vous pouvez sélectionner un modèle approprié. Si un seul modèle fournisseur existe, les nouvelles fiches fournisseur utiliseront toujours ce modèle.  

### <a name="to-create-a-new-vendor-card"></a>Pour créer une fiche fournisseur

1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Fournisseurs**, puis sélectionnez le lien associé.  
2. Sur la page **Fournisseurs**, choisissez **Nouveau**.

    Si plusieurs modèles de fournisseur existent, une page s’affiche et vous permet de sélectionner un modèle fournisseur. Dans ce cas, suivez les deux étapes suivantes.
    1. Sur la page **Sélectionnez un modèle pour un nouveau fournisseur**, sélectionnez le modèle que vous souhaitez utiliser pour la nouvelle fiche fournisseur.
    2. Cliquez sur le bouton **OK**. Une nouvelle fiche fournisseur avec certains champs contenant les informations provenant de ce modèle s’ouvre.
3. Renseignez ou modifiez les champs de la fiche fournisseur selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > Si vous ne connaissez pas l’adresse de facturation qui sera utilisée pour chaque facture fournisseur, ne renseignez pas le champ **N° fournisseur**. Sélectionnez plutôt le numéro du fournisseur à payer après avoir configuré une demande de prix, une commande ou un en-tête facture.

Le fournisseur est désormais enregistré, et la fiche fournisseur est prête à être utilisée sur les documents d’achat.

Si vous souhaitez utiliser cette fiche fournisseur comme modèle lorsque vous créez de nouvelles fiches fournisseur, enregistrez-la comme modèle fournisseur. Pour plus d'informations, consultez la section [Pour enregistrer la fiche fournisseur en tant que modèle](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-vendor-cards"></a>Suppression de cartes fournisseur

Si vous avez enregistré une transaction pour un fournisseur, vous ne pouvez pas supprimer la carte car les écritures comptables peuvent être nécessaires pour l’audit. Pour supprimer des fiches fournisseur avec des écritures comptables, contactez votre partenaire Microsoft pour le faire via le code.

## <a name="to-save-the-vendor-card-as-a-template"></a>Pour enregistrer la fiche fournisseur en tant que modèle

1. Sur la page **Fiche fournisseur**, sélectionnez l’action **Sauvegarder comme modèle**. La page **Modèle fournisseur** s’ouvre et affiche la fiche fournisseur comme modèle.
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pour réutiliser les axes analytiques dans les modèles, sélectionnez l’action **Axes analytiques**. La page **Modèles axe** s’ouvre et affiche tous les codes axe qui sont définis pour le fournisseur.
4. Modifiez ou entrez les codes axe s’appliquant aux nouvelles fiches fournisseur créées à l’aide du modèle.
5. Lorsque vous avez terminé le nouveau modèle fournisseur, cliquez sur le bouton **OK**.  
   Le modèle fournisseur est ajouté à la liste des modèles fournisseur. Vous pouvez ainsi l’utiliser pour créer des fiches fournisseur.

## <a name="see-also"></a>Voir aussi

[Fusionner l’enregistrement des doublons](sales-how-merge-duplicate-records.md)  
[Création des souches de numéros](ui-create-number-series.md)  
[Achats](purchasing-manage-purchasing.md)  
[Enregistrer des achats](purchasing-how-record-purchases.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]