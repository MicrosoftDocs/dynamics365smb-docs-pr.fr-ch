---
title: "Procédure\_: créer des factures ou des avoirs service"
description: "Découvrez comment utiliser Business\_Central pour créer de manière transparente des factures et des avoirs pour vos services."
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# <a name="create-service-invoices-or-credit-memos"></a>Créer des factures service ou des avoirs
La simplicité de facturation des commandes service est une fonctionnalité clé de [!INCLUDE[prod_short](includes/prod_short.md)]. Vous pouvez aussi configurer votre [!INCLUDE[prod_short](includes/prod_short.md)] afin qu’un technicien de service sur le terrain puisse créer une facture pour un service qui n’est pas connecté à un contrat ou une commande. Sinon, configurez [!INCLUDE[prod_short](includes/prod_short.md)] afin de facturer régulièrement les contrats de service. La période de facturation de chaque contrat définit la fréquence de facturation.

## <a name="to-invoice-several-service-contracts"></a>Pour facturer plusieurs contrats de service

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Créer des factures de contrat de service**, puis sélectionnez le lien associé.  
2. Définissez les filtres que vous souhaitez appliquer.  
3. Dans le champ **Date comptabilisation**, entrez la date à utiliser comme date comptabilisation pour les factures service.  
4. Dans le champ **Date facturation**, saisissez la date limite de facturation des contrats. Le traitement par lots inclut les contrats dont la prochaine date de facturation est antérieure à cette date.  
5. Dans le champ **Action**, sélectionnez **Créer factures**.  
6. Sélectionnez **OK** pour créer les factures service.  
  
Vous pouvez également facturer un contrat de service directement à partir de la page **Contrat de service** si la date de la prochaine facture sur le contrat est antérieure à la date du jour.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Pour facturer un contrat de service à partir de la page Contrat de service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Contrats de service**, puis sélectionnez le lien associé.  
2. Sélectionnez le contrat de service à facturer, puis ouvrez la fiche de contrat.  
3. Choisissez l’action **Créer facture service**. 
4. Choisissez **Oui** pour créer les factures service.  
  
  > [!NOTE]  
  > Vous ne pouvez pas créer de factures service pour le contrat de service lorsque la valeur du champ **Changer statut** est paramétrée sur **Ouvert**.  

## <a name="to-post-an-invoice-from-a-service-order"></a>Pour valider une consommation à partir d’une commande service
La procédure suivante décrit comment définir la partie du service que vous allez facturer au client.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes service**, puis choisissez le lien associé.  
2. Sélectionnez la commande service à facturer, puis ouvrez la fiche de commande.  
3. Choisissez l’action **Lignes service**.  
4. Recherchez les écritures requises, puis spécifiez les quantités pour lesquelles vous allez facturer le client dans le champ **Qté à facturer**.  
  
   > [!NOTE]  
   > Vous pouvez facturer le client pour le service enregistré soit entièrement, soit partiellement. Si vous décidez de facturer entièrement le client, la valeur renseignée dans le champ **Qté à facturer** doit être égale à celle renseignée dans le champ **Quantité**. Vous pouvez valider une facture entière avec une expédition entière et que vous pouvez valider une facture entière pour une expédition entière déjà validée qui n’avait pas encore été facturée ni consommée précédemment.  
   >  
   > Lorsque vous validez une facture partielle, vous pouvez spécifier la quantité à facturer de deux façons. Si vous comptez valider le service avec l’option **Livrer et facturer**, la valeur renseignée dans le champ **Qté à facturer** doit être égale à celle renseignée dans le champ **Qté à expédier**. Si vous voulez facturer une expédition déjà validée, la quantité à facturer ne peut pas être supérieure à la valeur renseignée dans le champ **Qté expédiée**.  
  
5. Sélectionnez **Valider**, puis **Facturer** ou **Livrer et facturer**. Pour plus d’informations sur ces options, voir [Validation dans la Gestion des services](service-service-posting.md).  
  
 La ligne service que vous avez sélectionnée est validée. Vous pouvez valider plusieurs lignes service en même temps en les sélectionnant et en choisissant **Valider**. Si vous procédez de la sorte, assurez-vous que vous avez entré toutes les informations nécessaires dans les lignes que vous voulez valider.  
  
 Lorsque vous validez la commande avec l’option **Facturer**, une facture service validée est générée ainsi que les écritures comptables correspondantes et les champs appropriés sont mis à jour dans les lignes service de la commande. En outre, les documents expédition validés précédemment sont mis à jour avec les quantités facturées. Si vous sélectionnez l’option de validation **Livrer et facturer**, une expédition validée est également générée.

## <a name="to-create-a-service-invoice-manually"></a>Pour créer une facture service manuellement
Typiquement, après avoir validé une facture service avec l’option **Facturer** ou **Livrer et facturer**, une facture service validée est crée automatiquement. Toutefois, il se peut que vous deviez émettre une facture qui est non liée à un contrat de service ou à une facture service. Cette procédure explique comment émettre une facture au moment où le client reçoit le service.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures service**, puis sélectionnez le lien associé.  
2. Créez une facture service.  
3. Renseignez le champ **N°** .  
  
    > [!NOTE]  
    >  Si vous avez configuré une souche de numéros pour les factures service sur la page **Paramètres Gestion des services**, vous pouvez sélectionner <kbd>Entrée</kbd> pour sélectionner le numéro de facture service suivant disponible.  
  
4. Dans le champ **N° client**, entrez le numéro d’un client. Sélectionnez le client approprié dans la liste.  
  
    Les champs de client sont automatiquement renseignés avec les informations de la fiche **Client**.  
  
5. Entrez une date dans le champ **Date comptabilisation**. Cette date est affichée sur les écritures validées. Ce champ est renseigné avec la date du jour mais vous pouvez la modifier manuellement.  
6. Renseignez le champ **Date document**. La date que vous entrez apparaît sur la facture imprimée et est utilisée pour calculer la date d’échéance.  
7. Renseignez les lignes service de la facture. Renseignez les champs **Type**, **N°**, et **Quantité** pour enregistrer des articles, des ressources et/ou des coûts utilisés pour la maintenance. 

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders"></a>Pour créer une facture qui combine les lignes expédition enregistrées d’une ou de plusieurs commandes service
Il se peut que vous deviez créer une facture service pour le service qui a déjà été expédié, à partir d’une ou plusieurs commandes service, mais pas encore facturé ni consommé. Vous pouvez renseigner les lignes facture automatiquement avec les lignes expédition validées sélectionnées pour un client spécifique.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures service**, puis sélectionnez le lien associé.  
2. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Créez des lignes facture pour les services expédiés mais non facturés. Vous pouvez également utiliser l’action **Extraire lignes expédition** pour ajouter des lignes expédition validées à la facture.  
4. Validez la facture service.  
  
 La facture service validée et les écritures comptables correspondantes sont créées. Les documents expédition validés précédemment sont mis à jour avec les quantités facturées et les quantités appropriées des lignes service des ordres origine.  

## <a name="to-create-a-service-credit-memo"></a>Pour créer un avoir service
Un document avoir service est typiquement utilisé lorsqu’un client retourne un article, mais il peut également être utilisé pour offrir au client une compensation ou pour corriger une facture erronée.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Avoirs service**, puis sélectionnez le lien associé.  
2. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Les champs **Date comptabilisation** et **Date document** affichent la date de travail. Si nécessaire, vous pouvez la modifier.    
4. Sur les lignes avoir, entrez les informations relatives aux articles retournés ou retirés, ou à la compensation qui sera donnée au client.  

## <a name="see-also"></a>Voir aussi
[Valider des factures service](service-how-to-post-service-orders.md)  
[Paramétrage de la gestion des services](service-setup-service.md)  
[Validation de service](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
