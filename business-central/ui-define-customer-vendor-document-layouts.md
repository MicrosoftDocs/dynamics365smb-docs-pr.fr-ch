---
title: Attribuer des présentations de documents aux clients ou aux fournisseurs
description: Lorsque des présentations de rapport personnalisées sont définies, vous pouvez les sélectionner à partir des fiches client et fournisseur pour spécifier que les présentations sélectionnées sont utilisées pour les documents que vous créez pour le client ou le fournisseur en question.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: cbd0fbea2e1567875dd7bda556271f693234a502
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510754"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Définir des présentations de document pour les clients et les fournisseurs
Lorsque des présentations de rapport personnalisées sont définies, vous pouvez les sélectionner à partir des fiches client et fournisseur pour spécifier les présentations qui sont utilisées pour différents types de documents que vous créez pour le client ou le fournisseur en question. La valeur du champ **Utilisation** définit le processus pour lequel la présentation du document est utilisée, par exemple **Relance**, **Expédition** et **Confirmation**.

En plus de définir les présentations à utiliser pour les documents, vous pouvez gagner du temps lors de l’envoi de documents à différents contacts client ou fournisseur en configurant les adresses e-mail de contacts spécifiques à utiliser avec des documents spécifiques. Par exemple, les relevés client sont envoyés aux contacts comptables, les commandes vente aux acheteurs des clients et les commandes achat aux vendeurs ou gestionnaires de comptes des fournisseurs.

Lorsque vous définissez une présentation de document pour un client ou un fournisseur, vous pouvez également spécifier l’adresse e-mail de la personne contact qui doit recevoir le document. Vous pouvez le faire rapidement avec la fonction **Sélectionner une adresse e-mail dans Contacts**, qui filtre automatiquement les adresses e-mail enregistrées pour le client ou le fournisseur en question.

Avant de pouvoir définir la présentation de document à utiliser pour les processus ainsi que le contact auquel envoyer le document, vous devez charger tous les rapports (documents) disponibles dans la page **Sélection des états**. Vous pouvez le faire rapidement avec la fonction **Copier à partir de la sélection des états**.

La section suivante décrit comment définir des présentations de document vente à partir d’une fiche client. Les étapes sont les mêmes pour les présentations de document achat à partir d’une fiche fournisseur.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Pour activer tous les documents vente disponibles pour un client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Ouvrez la fiche du client pour lequel vous souhaitez définir des présentations de document par processus métier.
3. Sur la page **Fiche client**, choisissez la page **Présentations document**.
4. Sur la page **Présentations document**, choisissez l’action **Copier à partir de la sélection des états**.

La page **Présentations document** pour le client en question est renseignée avec toutes les présentations de rapport pour les ventes disponibles dans le système. Pour plus d’informations sur leur création, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

Vous pouvez à présent procéder à l’ajustement de la liste avec les présentations de rapport personnalisées ou les adresses e-mail des contacts auxquels les documents doivent être envoyés.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Pour sélectionner une présentation de rapport personnalisée à utiliser pour la présentation du document vente
Si une présentation de rapport personnalisée n’est pas définie pour une ou plusieurs présentations de rapport définies dans la page **Présentations document** pour le client, vous pouvez le faire rapidement.

1. Sur la page **Présentations document**, sur la ligne d’une présentation de rapport pour laquelle vous souhaitez utiliser une présentation personnalisée, choisissez le champ **Description présentation personnalisée**. Le champ est renseigné si la présentation client est déjà sélectionnée ou vide.
2. Sur la page **Présentations rapport personnalisées**, sélectionnez la présentation de document spéciale que vous souhaitez utiliser pour le type de document vente en question. Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Pour configurer le contact qui reçoit la présentation de document pour un client
Vous pouvez gagner du temps lors de l’envoi de documents à différents contacts client ou fournisseur en spécifiant les adresses e-mail des contacts sur les différentes lignes de la page **Présentations document**. Par exemple, les relevés client peuvent être envoyés aux contacts comptables, les commandes vente aux acheteurs de vos clients et les commandes achat aux vendeurs ou gestionnaires de comptes des fournisseurs.

1. Sur la page **Présentations document**, sur la ligne d’une présentation de rapport que vous souhaitez envoyer à un contact spécifique pour le client, choisissez l’action **Sélectionner une adresse e-mail dans Contacts**.
2. Sur la page **Contacts**, sélectionnez la ligne du contact concerné, puis choisissez le bouton **OK**.

L’adresse e-mail du contact est maintenant insérée sur la ligne de présentation du document afin que le document vente en question, par exemple des relances, soit toujours envoyé à ce contact dans la société du client.

## <a name="see-also"></a>Voir aussi  
[Mettre à jour les présentations d’état personnalisées](ui-update-report-layouts.md)  
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Importer et exporter une présentation d’état ou de document personnalisée](ui-how-import-and-export-report-layout.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Gestion des présentations de rapport](ui-manage-report-layouts.md)  
[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  
[Utiliser des états, des traitements par lots et des XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]