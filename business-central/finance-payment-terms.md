---
title: Configurer des conditions de paiement
description: "Dans la version de base de Business\_Central, utilisez les conditions de paiement pour gérer les dates d’échéance et les remises de paiement."
author: edupont04
ms.topic: conceptual
ms.search.form: 4
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-payment-terms"></a>Configurer des conditions de paiement

Les conditions de paiement déterminent la façon dont vous gérez les dates d’échéance et les remises de paiement. Vous pouvez configurer n’importe quel nombre de codes condition de paiement et utiliser des formules date pour définir les conditions de paiement. Lorsque vous vous inscrivez pour la première fois à [!INCLUDE [prod_short](includes/prod_short.md)], la société de démonstration fournit quelques méthodes de paiement que les entreprises utilisent souvent. Vous pouvez cependant en ajouter autant que nécessaire.  

Vous pouvez affecter des conditions de paiement aux clients et aux fournisseurs pour que les mêmes conditions soient toujours utilisées dans les documents achat et vente que vous créez pour eux. Si nécessaire, vous pouvez modifier les conditions du document de vente ou d’achat, par exemple si vous souhaitez qu’un client particulier vous paie dans les 7 jours au lieu des 14 jours par défaut. Cela ne modifie pas les conditions de paiement par défaut affecté au client. Les mêmes conditions de paiement sont utilisées pour les documents vente et achat.

Ensuite, lorsque vous validez une facture, [!INCLUDE [prod_short](includes/prod_short.md)] calcule les remises de paiement en fonction des conditions de paiement. La date d’escompte, c’est-à-dire la dernière date à laquelle le client peut payer et recevoir une remise sur le paiement, est également calculée à ce moment-là.  

De même, lorsque vous publiez un avoir, [!INCLUDE [prod_short](includes/prod_short.md)] calcule les remises de paiement possibles en fonction des conditions de paiement. Le système applique aux escomptes sur les avoirs les mêmes méthodes de calcul qu’aux escomptes sur les factures. Lorsqu’un avoir est appliqué à une facture, le montant de l’escompte sur l’avoir est retranché du montant de l’éventuel escompte sur la facture.  

Si vous souhaitez envoyer à vos clients des rappels de paiements en retard, vous devez configurer des niveaux et des conditions de rappel. Pour plus d’informations, voir [Configurer les conditions et niveaux de relance](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Pour configurer des conditions de paiement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Conditions de paiement**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Après avoir configuré les conditions de paiement, affectez-les aux clients et fournisseurs. Vous pouvez éventuellement ajouter des conditions de paiement à vos modes de règlement.  

> [!TIP]
> Dans la version de base de [!INCLUDE [prod_short](includes/prod_short.md)], les conditions de paiement avec paiements partiels ne sont pas prises en charge. Au lieu de cela, vous devez utiliser la fonctionnalité de prépaiement. Pour plus d’informations, reportez\-vous à [Configuration des acomptes](finance-set-up-prepayments.md).
>
> Dans certains pays/régions, vous *pouvez* mettre en place des conditions de paiement avec des paiements partiels. Pour savoir si cette fonctionnalité est prise en charge dans votre pays/région, consultez la section **Fonctionnalité locale** dans le volet de navigation sur le côté gauche d’un article [Microsoft Learn](about-localization.md).

## <a name="see-also"></a>Voir aussi

[Paramétrer les modes de paiement](finance-payment-methods.md)  
[Configuration des acomptes](finance-set-up-prepayments.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)  
[Enregistrer un nouveau fournisseur](purchasing-how-register-new-vendors.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
