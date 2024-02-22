---
author: brentholtorf
ms.topic: include
ms.date: 11/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Les champs **Date document** et **Date validation** dans les documents vente et achat vous aident à respecter les normes comptables et à obtenir des calculs financiers exacts. Les champs répondent à différents objectifs :

- Pour que [!INCLUDE [prod_short](prod_short.md)] puisse calculer correctement les frais financiers et le montant dû sur les factures vente, le champ **Date document** doit correspondre à l’une des dates suivantes :

   - La date sur la facture vente que vous avez envoyée au client. 
   - La date sur la facture achat que vous avez reçue de votre fournisseur.
- Le champ **Date validation** indique quand un document a été enregistré dans [!INCLUDE [prod_short](prod_short.md)]. De nombreuses normes et réglementations comptables exigent que les entreprises enregistrent et déclarent les transactions financières en fonction de la date à laquelle elles ont été effectuées.

En fonction de vos processus métier, ces dates peuvent ou non être identiques. Si elles sont identiques, vous pouvez configurer [!INCLUDE [prod_short](prod_short.md)] pour mettre à jour la date sur les documents vente et achat avec la date à laquelle vous les avez validés.  
  
Pour définir automatiquement les dates de document sur les dates de validation, dans les pages **Paramètres ventes** et **Paramètres achats**, activez le bouton bascule **Lier la date doc à la date validation**.

> [!NOTE]
> Le paramètre n’affecte pas les feuilles vente ou achat.