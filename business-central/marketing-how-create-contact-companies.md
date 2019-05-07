---
title: Créer des sociétés contact| Microsoft Docs
description: Décrit comment créer un contact pour chaque nouvelle société ou société prospect avec laquelle vous collaborez ou entretenez des relations.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 67945b8825ae94ff3a09a4072309c401abb41c6b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "920997"
---
# <a name="create-contacts"></a>Créez des contacts
Vous pouvez créer un contact pour chaque nouvelle société avec laquelle vous êtes en contact, par exemple un client, un fournisseur, un prospect, une banque, un cabinet d'avocats, un consultant, et ainsi de suite.

Il existe deux méthodes permettant de créer un contact : à partir de zéro ou à partir d'un client, d'un fournisseur ou d'un compte bancaire existant.

## <a name="create-a-company-contact-from-scratch"></a>Créer un contact société à partir de zéro
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contacts**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **N°**, saisissez le numéro du contact.

    Si vous avez configuré une souche de numéros pour les contacts sur la page **Paramètres Marketing**, appuyez sur la touche Entrée pour sélectionner le numéro de contact suivant.  
4. Définissez **Type** à **Société**.
5. Renseignez les autres champs selon vos besoins.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Pour créer un contact société à partir d'un client, d'un fournisseur ou d'un compte bancaire
Si vous avez configuré plusieurs clients, fournisseurs et comptes bancaires, vous pouvez créer des contacts sur la base des données existantes. Lorsque vous créez un contact de cette façon, les informations de contact sont synchronisées avec les informations du client, du fournisseur ou du compte bancaire.

> [!NOTE]  
>   Avant de créer des sociétés contact de cette manière, vous devez spécifier un code relation d'affaires pour les clients, les fournisseurs, ainsi que des comptes bancaires sur la page **Paramètres marketing**. Si vous devez créer des contacts à partir de comptes bancaires, vous devez également spécifier des souches de numéros pour les comptes bancaires sur la page **Paramètres comptabilité**.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez une des actions suivantes, selon l'emplacement à partir duquel vous souhaitez créer des contacts, puis sélectionnez le lien associé.
   * **Créer contacts à partir des clients**
   * **Créer des contacts à partir des fournisseurs**
   * **Créer des contacts à partir des comptes bancaires**
2. Sur la page de traitement par lots qui s'affiche, dans la section **Client**, **Fournisseur** ou **Compte bancaire**, définissez des filtres si vous souhaitez créer des contacts à partir de clients, de fournisseurs ou de comptes bancaires spécifiques.
3. Pour démarrer la création de contacts, cliquez sur le bouton **OK**.

    Les numéros de contact suivants de la souche de numéros sont affectés aux nouveaux contacts. La relation d'affaires des fournisseurs qui est spécifiée sur la page **Paramètres Marketing** est affectée aux contacts nouvellement créés.

> [!TIP]  
>   Vous pouvez également créer un client, un fournisseur ou un compte bancaire à partir d'un contact. Pour plus d'informations, reportez-vous à [Créer un client, un fournisseur ou un compte bancaire à partir d'un contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Voir aussi
[Synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Affecter des relations d'affaires à un contact](marketing-business-relations.md#AssignBusRelContact)  
[Affecter des secteurs d'activité à un contact](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Affecter des groupes de distribution à un contact](marketing-mailing-groups.md#AssignMailGroupContact)  
[Création de personnes contact](marketing-create-contact-persons.md)  
[Utilisation de Business Central](ui-work-product.md)
