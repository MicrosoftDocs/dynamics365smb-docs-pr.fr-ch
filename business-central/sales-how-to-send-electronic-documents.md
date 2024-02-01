---
title: Envoyer des documents électroniques
description: "Découvrez comment utiliser Business\_Central pour envoyer des factures et des avoirs électroniques au format PEPPOL."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="send-electronic-documents"></a>Envoi des documents électroniques

> [!NOTE]
> Le contenu de cet article s’applique uniquement aux versions de Dynamics 365 Business Central sorties avant la 2e vague de lancement 2023. Dans la 2e vague de lancement 2023, une nouvelle fonctionnalité pour les documents électroniques est incluse. Pour en savoir plus, consultez [Configurer des documents électroniques](finance-how-setup-edocuments.md).  

La version générique de [!INCLUDE[prod_short](includes/prod_short.md)] prend en charge l’envoi de factures et d’avoirs électroniques au format PEPPOL, qui est pris en charge par les principaux fournisseurs de services d’échange de documents. Un fournisseur de services d’échange de documents affecte des documents électroniques entre partenaires commerciaux. Pour assurer la prise en charge d’autres formats de documents électroniques, vous pouvez utiliser l’infrastructure d’échange de données.  

 Dans la version générique de [!INCLUDE[prod_short](includes/prod_short.md)], un service d’échange de documents est préconfiguré et prêt à être installé pour votre société. Pour plus d’informations, reportez vous à [Configurer un service d’échange de document](across-how-to-set-up-a-document-exchange-service.md). Cependant, dans certains cas, vous devez installer une application. Pour plus d’informations, voir [FAQ Facturation électronique](faq-electronic-invoicing.yml).  

 Pour envoyer une facture vente en tant que document PEPPOL électronique, sélectionnez l’option **Document électronique** dans la boîte de dialogue **Valider et envoyer**. Vous pouvez également définir le profil d’envoi de document par défaut du client à partir de cette boîte de dialogue. Au préalable, vous devez configurer différentes données de base, telles que les informations sur la société, les clients, les articles, et les unités de mesure. Celles-ci sont utilisées pour identifier les partenaires commerciaux et les articles lors de la conversion des données des champs dans [Configurer l’envoi et la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Envoyer une facture vente électronique

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente**, puis sélectionnez le lien associé.  

2. Créez une facture vente.  

3. Lorsque la facture vente est prête à être émise, sélectionnez l’action **Valider et envoyer**.  

     Si le profil d’envoi par défaut du client est **Document électronique**, il s’affichera dans la boîte de dialogue **Valider et envoyer une confirmation**. De cette façon, il vous suffit d’opter pour le bouton **Oui** pour valider et envoyer la facture par voie électronique dans le format sélectionné.  

4. Dans la boîte de dialogue **Valider et envoyer une confirmation**, cliquez sur le bouton AssistEdit situé à droite du champ **Envoyer le document à**.  

5. Dans la boîte de dialogue **Envoyer le document à**, dans le champ **Document électronique**, sélectionnez **Via le service d’échange de documents**.  

6. Dans le champ **Format**, sélectionnez **PEPPOL**.  

7. Cliquez sur le bouton **OK**. La boîte de dialogue **Valider et envoyer une confirmation** s’affiche. **Document électronique (PEPPOL)** est ajouté au champ **Envoyer le document à**.  

8. Cliquez sur le bouton **Oui**.  

     La facture vente enregistrée est validée et envoyée au client au format PEPPOL.  

    > [!NOTE]  
    >  Vous pouvez également envoyer une facture vente validée en tant que document électronique. La procédure est la même que celle décrite dans cette rubrique pour les documents vente non validés. Sur la page **Facture vente enregistrée**, sélectionnez l’action **Journal des activités** pour afficher le statut du document électronique.  

## <a name="see-also"></a>Voir aussi

[Facturation des ventes](sales-how-invoice-sales.md)  
[Configuration des profils d’envoi de documents](sales-how-setup-document-send-profiles.md)  
[Configuration de l’envoi et de la réception de documents électroniques](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Configurer un service d’échange de document](across-how-to-set-up-a-document-exchange-service.md)  
[Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md)  
[Échanger des données par voir électronique](across-data-exchange.md)  
[FAQ Facturation électronique](faq-electronic-invoicing.yml)  
[Fonctionnalités marché](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
