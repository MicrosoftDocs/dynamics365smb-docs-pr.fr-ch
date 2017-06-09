---
title: "Procédure : configurer des profils d&quot;envoi de documents| Microsoft Docs"
description: "Procédure : Configurer des profils d&quot;envoi de documents"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d42de516efcc866fcfb04f36fb9c3cbffd3a667d
ms.contentlocale: fr-ch
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-document-sending-profiles"></a>Procédure : Configurer des profils d'envoi de documents
Vous pouvez associer chaque client avec une méthode par défaut d'envoi de documents vente, afin d'éviter d'avoir à sélectionner une option d'envoi chaque fois que vous sélectionnez l'action **Valider et envoyer**.

Dans la fenêtre **Profils d'envoi de documents**, configurez différents profils d'envoi que vous pouvez sélectionner dans le champ **Profil d'envoi de documents** d'une fiche client. Vous pouvez cocher la case **Par défaut** pour spécifier que le profil d'envoi du document est le profil par défaut pour tous les clients, sauf pour les clients dont le champ **Profil d'envoi de documents** est renseigné avec un autre profil d'envoi.

Lorsque vous sélectionnez l'action **Valider et envoyer** dans un document vente, la boîte de dialogue **Valider et envoyer la confirmation** affiche le profil d'envoi utilisé, soit celui créé pour le client, soit le profil par défaut pour tous les clients. Dans la boîte de dialogue, vous pouvez modifier le profil d'envoi du document vente. Pour plus d'informations, reportez-vous à [Procédure : facturer des ventes](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Configurer un profil d'envoi de documents
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Profils d'envoi de documents**, puis sélectionnez le lien associé.
2. Dans la fenêtre **Profils d'envoi de documents**, sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Spécifier un profil d'envoi pour une fiche client
1. Dans le coin supérieur droit, sélectionnez l'icône **Page ou état pour la recherche** ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Clients**, puis sélectionnez le lien associé.
2. Ouvrez la fiche du client pour laquelle vous souhaitez configurer un profil d'envoi.
3. Dans le champ **Profil d'envoi de documents**, sélectionnez un profil configuré comme décrit dans la procédure précédente.

## <a name="see-also"></a>Voir aussi
[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

