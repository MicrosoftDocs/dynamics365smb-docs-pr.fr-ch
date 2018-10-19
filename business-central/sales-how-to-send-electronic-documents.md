---
title: "Envoyer des documents électroniques | Microsoft Docs"
description: "Découvrez comment envoyer des factures par voie électronique."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 507fd934ee30d2bcacbb298d0ab18fa351621922
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="send-electronic-documents"></a>Envoyer des documents électroniques
La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge l'envoi de factures et d'avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d'échange de documents. Un fournisseur de services d'échange de documents affecte des documents électroniques entre partenaires commerciaux. Pour assurer la prise en charge d'autres formats de documents électroniques, vous pouvez utiliser l'infrastructure d'échange de données.  

 Dans la version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)], un service d'échange de documents est préconfiguré et prêt à être installé pour votre société. Pour plus d'informations, reportez vous à [Configurer un service d'échange de document](across-how-to-set-up-a-document-exchange-service.md).  

 Pour envoyer une facture vente en tant que document électronique PEPPOL, sélectionnez l'option **Document électronique** dans la boîte de dialogue **Valider et envoyer** à partir de laquelle vous pouvez également configurer le profil d'envoi de document par défaut du client. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données des champs dans [Configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Envoyer une facture vente électronique  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente**, puis sélectionnez le lien associé.  

2.  Créez une facture vente.  

3.  Lorsque la facture vente est prête à être émise, sous l'onglet **Actions**, dans le groupe **Validation**, sélectionnez **Valider et envoyer**.  

     Si le profil d'envoi par défaut du client est **Document électronique**, il s'affiche dans la boîte de dialogue **Valider et envoyer une confirmation** et il vous suffit de choisir le bouton **Oui** pour valider et envoyer la facture par voie électronique au format sélectionné.  

4.  Dans la boîte de dialogue **Valider et envoyer une confirmation**, cliquez sur le bouton AssistEdit situé à droite du champ **Envoyer le document à**.  

5.  Dans la boîte de dialogue **Envoyer le document à**, dans le champ **Document électronique**, sélectionnez **Via le service d'échange de documents**.  

6.  Dans le champ **Format**, sélectionnez **PEPPOL**.  

7.  Cliquez sur le bouton **OK**. La boîte de dialogue **Valider et envoyer une confirmation** s'affiche. **Document électronique (PEPPOL)** est ajouté au champ **Envoyer le document à**.  

8.  Cliquez sur le bouton **Oui**.  

     La facture vente enregistrée est validée et envoyée au client en tant que document électronique au format PEPPOL.  

    > [!NOTE]  
    >  Vous pouvez également envoyer une facture vente validée en tant que document électronique. La procédure est la même que celle décrite dans cette rubrique pour les documents vente non validés. Dans la fenêtre **Facture vente enregistrée**, sous l'onglet **Actions**, dans le groupe **Général**, sélectionnez **Journal des activités** pour afficher le statut du document électronique. Pour plus d'informations, voir **Journal des activités**.  

## <a name="see-also"></a>Voir aussi  
[Facturer des ventes](sales-how-invoice-sales.md)  
[Configurer des profils d'envoi de documents](sales-how-setup-document-send-profiles.md)  
[Configurer l'envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Configurer un service d'échange de document](across-how-to-set-up-a-document-exchange-service.md)  
[Configurer les définitions d'échange de données](across-how-to-set-up-data-exchange-definitions.md)  
[Échanger des données par voir électronique](across-data-exchange.md)  
[Fonctionnalités marché](ui-across-business-areas.md)  

