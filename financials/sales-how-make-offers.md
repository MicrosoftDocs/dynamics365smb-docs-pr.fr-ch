---
title: "Créer une offre vente à un client | Microsoft Docs"
description: "Décrit comment créer une offre vente offrent ou un document de demande de proposition pour enregistrer votre offre à un client pour vendre des produits dans certaines conditions."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 552fbf283a9149c430ea1ed94bcea4bd22e43fea
ms.contentlocale: fr-ch
ms.lasthandoff: 01/30/2018

---
# <a name="make-offers"></a>Créer des offres
Vous créez un devis pour enregistrer votre proposition à un client pour vendre certains biens selon certaines conditions de livraison et de paiement. Vous pouvez envoyer un devis au client pour communiquer la proposition. Vous pouvez envoyer par e-mail le document en pièce jointe au format PDF. Vous pouvez faire en sorte que le corps du message soit prérempli avec un résumé du devis. Pour plus d'informations, voir [Envoyer des documents par e-mail](ui-how-send-documents-email.md).

Lorsque vous négociez avec le client, vous pouvez modifier et renvoyer autant de devis que nécessaire. Lorsque le client accepte le devis, vous convertissez le devis en facture vente ou en commande vente dans laquelle vous traitez la vente. Pour plus d'informations, voir [Facturer des ventes](sales-how-invoice-sales.md) ou [Vendre des produits](sales-how-sell-products.md).

Vous pouvez remplir les champs relatifs au client sur le devis de deux façons selon que le client est déjà enregistré ou non. Reportez-vous aux étapes 2 et 3 de la procédure ci-dessous.

## <a name="to-create-a-sales-quote"></a>Pour créer un devis
Sur la page d'accueil, sélectionnez l'action **Devis**.  
2. Dans le champ **Client**, entrez le nom d'un client existant.

   D'autres champs de la fenêtre **Devis** contiennent des informations standard sur le client sélectionné. Si le client n'est pas enregistré, procédez comme suit :
3. Dans le champ **Client**, entrez le nom du nouveau client.
4. Dans la boîte de dialogue d'enregistrement du nouveau client, cliquez sur le bouton **Oui**.
5. Dans la fenêtre **Sélectionnez un modèle pour un nouveau client**, sélectionnez un modèle sur lequel baser la nouvelle fiche client, puis cliquez sur le bouton **OK**.
6. Une nouvelle fiche client affiche des informations sur le modèle client sélectionné. Renseignez les champs restants. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).  
7. Lorsque vous avez terminé la fiche client, cliquez sur le bouton **OK** pour revenir à la fenêtre **Devis**.

   Plusieurs champs du devis sont désormais renseignés avec les informations que vous avez spécifiées sur la nouvelle fiche client.  
8. Renseignez les champs restants de la fenêtre **Devis**, selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Vous êtes maintenant prêt à renseigner les lignes commande vente pour les produits que vous vendez au client ou pour toute transaction avec le client que vous souhaitez enregistrer dans un compte général.   

Si vous avez défini des lignes vente récurrentes pour le client, tel qu'un ordre de réapprovisionnement mensuel, vous pouvez insérer ces lignes sur la commande par l'intermédiaire de l'action **Extraire les lignes vente récurrentes**.  
9. Sous le raccourci **Lignes**, dans le champ **Type**, sélectionnez le type de produit, de frais ou de transaction à valider pour le client avec la ligne vente.
10. Dans le champ **N°**, sélectionnez un enregistrement à valider en fonction de la valeur du champ **Type**.

 Laissez le champ **N°** vide dans les cas suivants : - Si la ligne est destinée à un commentaire. Saisissez le commentaire dans le champ **Description**.
 -Si la ligne est destinée à un article non stocké. Sélectionnez l'action **Sélectionner articles non stockés**. Pour en savoir plus, voir [Utiliser des articles non stockés](inventory-how-work-nonstock-items.md).

11. Dans le champ **Quantité**, entrez le nombre d'unités du produit, de frais ou de la transaction que la ligne enregistre pour le client.

    > [!NOTE]  
>   Si l'article est de type **Article - Service** ou **Ressource**, la quantité est une unité de temps, telle que les heures, comme indiqué dans le champ **Code unité de la ligne**.  

    La valeur du champ **Montant ligne** est calculée comme suit : *Prix unitaire* x *Quantité*.  

    Le prix et les montants ligne sont affichés avec ou sans la taxe de vente en fonction de la valeur que vous avez sélectionnée dans le champ **Prix incluant les taxes** de la fiche client.  
12. Si vous souhaitez accorder une remise, saisissez un pourcentage dans le champ **% remise ligne**. La valeur du champ **Montant ligne** est mise à jour en conséquence.  

    Si des prix article spéciaux sont définis sur le raccourci **Prix vente et remises ligne vente** dans la fiche client ou article, le prix et le montant de la ligne vente sont automatiquement mis à jour si les critères de prix convenus sont réunis. Pour plus d'informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Répétez les étapes 9 à 12 pour chaque produit que vous souhaitez proposer au client.  

    Les totaux sous les lignes sont calculés automatiquement au fur et à mesure que vous créez ou modifiez des lignes.  
14. Dans le champ **Montant remise facture**, entrez un montant qui doit être déduit de la valeur indiquée dans le champ **Total TTC**.

    Si vous avez défini des remises facture pour le client, le pourcentage spécifié est automatiquement inséré dans le champ **% remise facture** si les critères sont réunis, et le montant associé est inséré dans le champ **Montant remise facture sans TVA**. Pour plus d'informations, reportez-vous à [Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md).
15. Lorsque les lignes devis sont renseignées, sélectionnez l'action **Envoyer par e-mail**.
16. Dans la fenêtre **Envoyer e-mail**, renseignez les champs restants et examinez le devis intégré. Pour plus d'informations, voir [Envoyer des documents par e-mail](ui-how-send-documents-email.md).
17. Si le client accepte le devis, sélectionnez l'action **Établir facture** ou **Créer commande**.

Le devis est supprimé de la base de données. Une facture vente ou une commande vente basée sur les informations du devis et dans laquelle vous pouvez traiter la vente est créée. Dans le champ **N° devis** de la facture vente ou de la commande vente, vous pouvez visualiser le numéro du devis à partir duquel elle a été réalisée. Pour plus d'informations, voir [Facturer des ventes](sales-how-invoice-sales.md) ou [Vendre des produits](sales-how-sell-products.md).

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Définition des ventes](sales-setup-sales.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

