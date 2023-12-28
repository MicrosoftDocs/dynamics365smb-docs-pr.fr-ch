---
title: Configuration des conditions de paiement
description: Utilisez les Conditions de paiement pour gérer les dates d'échéance et les escomptes paiements.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 09/05/2023
ms.author: bholtorf
---
# <a name="set-up-payment-terms"></a>Configuration des conditions de paiement

Les conditions de paiement déterminent la façon dont vous gérez les dates d’échéance et les remises de paiement. Vous pouvez configurer n’importe quel nombre de codes condition de paiement et utiliser des formules date pour définir les conditions de paiement. Lorsque vous vous inscrivez pour la première fois à [!INCLUDE [prod_short](includes/prod_short.md)], la société de démonstration fournit quelques méthodes de paiement que les entreprises utilisent souvent. Vous pouvez cependant en ajouter autant que nécessaire.  

Si vous affectez des conditions de paiement aux clients et aux fournisseurs, les mêmes conditions soient toujours utilisées dans les documents achat et vente que vous créez pour eux. Les dates des documents vente et achat, et non leurs dates comptables, sont utilisées pour calculer les dates d’échéance des paiements. Si nécessaire, vous pouvez modifier les conditions du document de vente ou d’achat, par exemple si vous souhaitez qu’un client particulier vous paie dans les 7 jours au lieu des 14 jours par défaut. La modification des conditions sur le document ne modifie pas les conditions de paiement par défaut attribuées au client. Les mêmes conditions de paiement sont utilisées pour les documents vente et achat.

Lorsque vous validez une facture, [!INCLUDE [prod_short](includes/prod_short.md)] calcule les remises de paiement en fonction des conditions de paiement. La date de l’escompte du paiement spécifie la dernière date à laquelle le client peut obtenir un escompte. La date est également calculée lorsque vous validez une facture.  

De même, lorsque vous publiez un avoir, [!INCLUDE [prod_short](includes/prod_short.md)] calcule les remises de paiement en fonction des conditions de paiement. Il applique aux escomptes sur les avoirs comme pour les aux escomptes sur les factures. Lorsque vous appliquez un avoir à une facture, [!INCLUDE [prod_short](includes/prod_short.md)] réduit le montant de la remise pour la facture du montant de la remise de l’avoir.  

Si vous souhaitez envoyer à vos clients des rappels de paiements en retard, vous devez configurer des niveaux et des conditions de rappel. Pour en savoir plus sur les rappels, accédez à [Créer des niveaux et conditions de rappel](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Pour configurer des conditions de paiement

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Conditions de paiement**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Après avoir configuré les conditions de paiement, affectez-les aux clients et fournisseurs. Vous pouvez éventuellement ajouter des conditions de paiement à vos modes de règlement.  

> [!TIP]
> Dans la version de base de [!INCLUDE [prod_short](includes/prod_short.md)], les conditions de paiement avec paiements partiels ne sont pas prises en charge. Au lieu de cela, vous devez utiliser la fonctionnalité de prépaiement. Pour en savoir plus sur la configuration des prépaiements, consultez [Configurer des prépaiements](finance-set-up-prepayments.md).
>
> Dans certains pays/régions, vous *pouvez* mettre en place des conditions de paiement avec des paiements partiels. Pour savoir si cette fonctionnalité est prise en charge dans votre pays/région, accédez à la section **Fonctionnalité locale** dans le sommaire sur le côté gauche d’un article [Microsoft Learn](about-localization.md).

## <a name="see-also"></a>Voir aussi

[Configuration des modes de règlement](finance-payment-methods.md)  
[Configuration des acomptes](finance-set-up-prepayments.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)  
[Enregistrer un nouveau fournisseur](purchasing-how-register-new-vendors.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
