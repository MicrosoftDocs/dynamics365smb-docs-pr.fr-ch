---
title: Paramétrer les méthodes préférées d’envoi des documents vente | Microsoft Docs
description: Décrit comment configurer la méthode préférée de chaque client pour l’envoi de documents vente, par exemple par e-mail, au format PDF, sous forme de document électronique, etc.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b54decd14cfa1003747ef2a56244ed3865d1ccd2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778562"
---
# <a name="set-up-document-sending-profiles"></a>Configurer des profils d’envoi de documents
Vous pouvez associer chaque client avec une méthode par défaut d’envoi de documents vente, afin d’éviter d’avoir à sélectionner une option d’envoi chaque fois que vous sélectionnez l’action **Valider et envoyer**.

Sur la page **Profils d’envoi de documents**, configurez différents profils d’envoi que vous pouvez sélectionner dans le champ **Profil d’envoi de documents** d’une fiche client. Vous pouvez cocher la case **Par défaut** pour spécifier que le profil d’envoi du document est le profil par défaut pour tous les clients, sauf pour les clients dont le champ **Profil d’envoi de documents** est renseigné avec un autre profil d’envoi.

Lorsque vous sélectionnez l’action **Valider et envoyer** dans un document vente, la boîte de dialogue **Valider et envoyer la confirmation** affiche le profil d’envoi utilisé, soit celui créé pour le client, soit le profil par défaut pour tous les clients. Dans la boîte de dialogue, vous pouvez modifier le profil d’envoi du document vente. Pour plus d’informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a>Configurer un profil d’envoi de documents
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Profils d’envoi de documents**, puis sélectionnez le lien associé.
2. Sur la page **Profils d’envoi de documents**, sélectionnez l’action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Spécifier un profil d’envoi pour une fiche client
1. Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.
2. Ouvrez la fiche du client pour laquelle vous souhaitez configurer un profil d’envoi.
3. Dans le champ **Profil d’envoi de documents**, sélectionnez un profil configuré comme décrit dans la procédure précédente.

## <a name="see-also"></a>Voir aussi
[Définition des ventes](sales-setup-sales.md)  
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]