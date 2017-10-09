---
title: "Paramétrer les méthodes préférées d'envoi des documents vente | Microsoft Docs"
description: "Décrit comment configurer la méthode préférée de chaque client pour l'envoi de documents vente, par exemple par e-mail, au format PDF, sous forme de document électronique, etc."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7f7499e6e501207ed5fd6ebbee5b94d18c1d008e
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-document-sending-profiles"></a>Procédure : Configurer des profils d'envoi de documents
Vous pouvez associer chaque client avec une méthode par défaut d'envoi de documents vente, afin d'éviter d'avoir à sélectionner une option d'envoi chaque fois que vous sélectionnez l'action **Valider et envoyer**.

Dans la fenêtre **Profils d'envoi de documents**, configurez différents profils d'envoi que vous pouvez sélectionner dans le champ **Profil d'envoi de documents** d'une fiche client. Vous pouvez cocher la case **Par défaut** pour spécifier que le profil d'envoi du document est le profil par défaut pour tous les clients, sauf pour les clients dont le champ **Profil d'envoi de documents** est renseigné avec un autre profil d'envoi.

Lorsque vous sélectionnez l'action **Valider et envoyer** dans un document vente, la boîte de dialogue **Valider et envoyer la confirmation** affiche le profil d'envoi utilisé, soit celui créé pour le client, soit le profil par défaut pour tous les clients. Dans la boîte de dialogue, vous pouvez modifier le profil d'envoi du document vente. Pour plus d'informations, reportez-vous à [Procédure : facturer des ventes](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Configurer un profil d'envoi de documents
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Profils d'envoi de documents**, puis sélectionnez le lien connexe.
2. Dans la fenêtre **Profils d'envoi de documents**, sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Spécifier un profil d'envoi pour une fiche client
1. Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien connexe.
2. Ouvrez la fiche du client pour laquelle vous souhaitez configurer un profil d'envoi.
3. Dans le champ **Profil d'envoi de documents**, sélectionnez un profil configuré comme décrit dans la procédure précédente.

## <a name="see-also"></a>Voir aussi
[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

