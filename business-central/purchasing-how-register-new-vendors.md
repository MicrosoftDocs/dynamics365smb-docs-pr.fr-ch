---
title: Créer une fiche fournisseur pour enregistrer de nouveaux fournisseurs
description: Dans cette rubrique, découvrez comment créer une fiche fournisseur pour enregistrer un nouveau fournisseur et enregistrer les fiches fournisseur en tant que modèle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 662239446426cf64ac20d766e21aee55b92f9809
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2021
ms.locfileid: "7587699"
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
Vous pouvez ajouter de nouveaux fournisseurs manuellement, en remplissant les champs sur la page **Fiche fournisseur**, ou vous pouvez utiliser des modèles contenant des informations prédéfinies. Par exemple, vous pouvez créer des modèles pour différents types de profils de fournisseurs. L’utilisation de modèles permet de gagner du temps lors de l’ajout de nouveaux fournisseurs et permet de garantir que les informations sont correctes à chaque fois. Si vous créez des modèles pour plusieurs types de fournisseurs, vous pouvez choisir le modèle à utiliser lorsque vous ajoutez un fournisseur. Si vous ne créez qu’un seul modèle, il sera utilisé pour tous les nouveaux fournisseurs. Après avoir créé un modèle, vous pouvez utiliser l’action **Appliquer le modèle** pour l’appliquer à un ou plusieurs fournisseurs sélectionnés. Pour créer un modèle, vous remplissez les informations que vous souhaitez réutiliser sur la page Fiche fournisseur, puis l’enregistrez en tant que modèle. Pour plus d’informations, consultez [Pour enregistrer la fiche fournisseur en tant que modèle](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Il peut être utile de personnaliser la page **Modèle de fournisseur** lorsque vous créez un modèle. Par exemple, vous souhaiterez peut-être ajouter un champ qui n’est pas déjà affiché sur la page. Pour plus d’informations, voir [Personnaliser votre espace de travail](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Vous pouvez également créer un fournisseur à partir d’un contact. Pour plus d’informations, reportez-vous à [Pour créer un contact comme client, fournisseur, employé ou compte bancaire à partir d’un contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Pour créer un fournisseur

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Si vous ne connaissez pas l’adresse de facturation qui sera utilisée pour chaque facture fournisseur, ne renseignez pas le champ **N° fournisseur**. Sélectionnez plutôt le numéro du fournisseur à payer après avoir configuré une demande de prix, une commande ou un en-tête facture.

Le fournisseur est désormais enregistré, et la fiche fournisseur est prête à être utilisée sur les documents d’achat.

Si vous souhaitez utiliser cette fiche fournisseur comme modèle lorsque vous créez de nouvelles fiches fournisseur, enregistrez-la comme modèle fournisseur. Pour plus d’informations, consultez la section [Pour enregistrer la fiche fournisseur en tant que modèle](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Suppression et modification des informations sur le fournisseur

Vous pouvez modifier les informations des fiches fournisseur à tout moment. Toutefois, si vous avez enregistré une transaction pour un fournisseur, vous ne pouvez pas supprimer la fiche car les écritures comptables peuvent être nécessaires aux fins d’audit. Pour supprimer des fiches fournisseur avec des écritures comptables, contactez votre partenaire Microsoft pour le faire via le code.

> [!TIP]
> Vous pouvez modifier l’IBAN sur le compte bancaire d’un fournisseur sans que le changement n’affecte vos écritures d’historique de registre de virements. Les écritures du registre des virements stockent l’IBAN du destinataire et le numéro de compte bancaire du destinataire qui ont été spécifiés dans les champs Compte bancaire du fournisseur et Nom du destinataire de la page Fiche fournisseur lorsque les écritures ont été créées.


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