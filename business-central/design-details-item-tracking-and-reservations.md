---
title: "Détails de conception\_: traçabilité et réservations"
description: 'Cette rubrique présente la traçabilité et les réservations, et décrit les concepts qui leur sont associés.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-item-tracking-and-reservations"></a>Détails de conception : traçabilité et réservations

L’utilisation simultanée de la réservation et de la traçabilité spécifique est rare, parce qu’elles créent toutes les deux un couplage entre l’approvisionnement et la demande. Sauf pour les situations où un client ou un gestionnaire de production demande un lot spécifique, il est rarement judicieux de réserver des articles de stock qui possèdent déjà des numéros traçabilité pour un lettrage spécifique. Bien qu’il soit possible de réserver des articles nécessitant une traçabilité, une fonctionnalité spéciale est nécessaire pour éviter les conflits de disponibilité entre les préparateurs de commandes qui demandent les mêmes articles suivis.  
  
Le concept de Lien tardif garantit qu’une réservation non spécifique d’un numéro de série ou d’un numéro de lot reste légèrement couplée jusqu’à la validation. Au moment de la validation, le système de réservation peut remanier les réservations non spécifiques pour s’assurer que le lettrage fixe est possible par rapport au numéro de série/lot prélevé de manière effective. Par ailleurs, le numéro de lot ou de série est disponible pour une réservation spécifique dans d’autres documents demandant ce numéro de série ou de lot spécifique.  
  
Une réservation non spécifique est une réservation pour laquelle l’utilisateur ne se soucie pas de l’article prélevé en particulier, alors qu’une réservation spécifique est une réservation pour laquelle l’utilisateur se soucie de l’article prélevé en particulier.  
  
> [!NOTE]  
> La fonctionnalité Lien tardif concerne uniquement les articles qui sont paramétrés avec une traçabilité spécifique, et elle s’applique uniquement aux réservations sur le stock, et non sur les commandes approvisionnement entrantes.  
  
La réservation des numéros traçabilité se classe en deux catégories, comme indiqué dans le tableau ci-dessous.  
  
|Réservation|Désignation|  
|-----------------|---------------------------------------|  
|Spécifique|Vous sélectionnez un numéro de série ou de lot spécifique lorsque vous réservez l’article de stock à partir d’une demande, comme une commande vente.<br /><br /> Il s’agit d’une réservation normale. Il s’agit d’un rigide lien entre l’approvisionnement et la demande qui portent tous les deux des numéros de série ou de lot. **Remarque :** la demande indique les numéros de série ou de lot. <br /><br /> Par exemple, vous souhaitez réserver une boîte de peinture bleue du lot A, parce que le client la demande. Une boîte de peinture bleue du lot A est expédiée au client.|  
|Non spécifique|Vous ne sélectionnez pas un numéro de série ou de lot spécifique lorsque vous réservez l’article de stock à partir d’une demande, comme une commande vente.<br /><br /> Il s’agit d’un état qui est imposé à une écriture de réservation pour les numéros de série ou de lot qui ne sont pas spécifiquement sélectionnés. **Remarque :** la demande n’indique pas les numéros de série ou de lot. <br /><br /> Par exemple, vous souhaitez réserver une boîte de peinture de n’importe quel lot de votre commande vente. Une boîte de peinture bleue de n’importe quel numéro de série ou numéro de lot est expédiée au client.|  
  
La principale différence entre la réservation spécifique et la réservation non spécifique est définie par l’existence des numéros de série ou des numéros de lot du côté de la demande, comme l’indique le tableau ci-dessous.  

| Type            | Approvisionnement                | demande                   |
|-----------------|-----------------------|--------------------------|
| **Spécifique**    | Numéro de série ou de lot. | Numéro de série ou de lot.    |
| **Non spécifique** | Numéro de série ou de lot. | Aucun numéro de série ou de lot |
  
Lorsque vous réservez des quantités en stock à partir d’une ligne document sortant pour un article ayant des numéros de suivi article affectés et étant configuré pour un suivi d’article spécifique, la page **Réservation** vous conduit à travers différents flux de travail en fonction de votre besoin de numéros de série ou de lot.  
  
## <a name="specific-reservation"></a>Réservation spécifique
Lorsque vous choisissez **Reserve** depuis la ligne document sortant, une boîte de dialogue s’affiche vous demandant si vous souhaitez réserver des numéros de série ou de lot spécifiques. Si vous choisissez **Oui**, la liste s’affiche avec tous les numéros de série ou de lot affectés à la ligne document. La page **Réservation** s’ouvre après que vous avez sélectionné l’un des numéros de série ou de lot, et vous pouvez alors réserver parmi les numéros de série ou de lot sélectionnés comme d’habitude.  
  
Si certains des numéros traçabilité spécifiques que vous essayez de réserver sont contenus dans des réservations non spécifiques, un message au bas de la page **Réservation** vous indique quelle part de la quantité réservée totale se trouve dans des réservations non spécifiques et si elle est toujours disponible.  
  
## <a name="nonspecific-reservation"></a>Réservation non spécifique
Si vous choisissez **Non** dans la boîte de dialogue qui s’affiche, la page **Réservation** s’ouvre et vous permet de réserver parmi tous les numéros de série ou de lot dans le stock.  
  
En raison de la structure du système de réservation, quand vous placez une réservation non spécifique pour un article suivi, le système doit sélectionner les écritures comptables de l’article spécifique à réserver. Comme les écritures comptables article indiquent les numéros traçabilité, la réservation réserve indirectement des numéros de série ou de lot spécifiques, même si vous n’en aviez pas l’intention. Pour gérer cette situation, le système de réservation essaie de remanier les écritures de réservation non spécifiques avant la validation.  
  
Le système fait toujours ses réserves par rapport aux entrées spécifiques, mais il utilise un mécanisme de remaniement lorsqu’il existe une demande spécifique du numéro de lot ou de série de la réservation non spécifique. Cela peut être le cas lorsque vous validez une transaction de demande, comme une commande vente, une feuille de consommation ou un ordre de transfert, pour le numéro de série ou de lot, ou lorsque vous tentez de réserver spécifiquement le numéro de série ou de lot. Le système remanie les réservations pour rendre le numéro de lot ou de série disponible à la demande ou à la réservation spécifique, plaçant ainsi un numéro de lot ou de série différent dans la réservation non spécifique. Si la quantité dans le stock est insuffisante, le système remanie autant que possible, et vous recevez une erreur de disponibilité s’il y a toujours une quantité insuffisante au moment de la validation.  
  
> [!NOTE]  
>  Sur une réservation non spécifique le champ du numéro de lot ou de série est vide dans l’écriture réservation qui pointe vers la demande, telle que la vente.  
  
## <a name="reshuffle"></a>Remanier
Lorsqu’un utilisateur valide un document sortant après avoir prélevé le mauvais numéro de série ou de lot, d’autres réservations non spécifiques sont remaniées pour refléter le numéro de série ou de lot réel qui est prélevé. Cela satisfait le moteur de validation avec une application fixe entre l’approvisionnement et la demande.  
  
Pour tous les scénarios professionnels pris en charge, le remaniement est possible uniquement sur des écritures comptables article positives contenant des numéros de réservation et de série ou de lot, mais sans numéro de série ou de lot défini du côté de la demande.  
  
## <a name="supported-business-scenarios"></a>Scénarios professionnels pris en charge
La fonctionnalité Lien tardif prend en charge les scénarios professionnels suivants :  
  
* Saisie d’un numéro de série ou de lot spécifique sur un document sortant avec une réservation non spécifique d’un numéro de série ou de lot incorrect.  
* Réservation d’un numéro de série ou de lot particulier.  
* Validation d’un document sortant avec une réservation non spécifique d’un numéro de série ou de lot.  
  
### <a name="entering-serial-or-lot-numbers-on-an-outbound-document-with-wrong-nonspecific-reservation"></a>Saisie de numéros de série ou de lot sur un document sortant avec une réservation non spécifique incorrecte
Il s’agit du plus courant des trois scénarios pris en charge. Dans ce cas, la fonctionnalité Lien tardif garantit qu’un utilisateur peut saisir un numéro de série ou de lot, qui est réellement prélevé, sur un document sortant qui a déjà une réservation non spécifique d’un numéro de série ou de lot différent.  
  
Par exemple, le besoin apparaît lorsqu’un préparateur de commandes a d’abord effectué une réservation non spécifique d’un numéro de série ou de lot. Ultérieurement lorsque l’article est prélevé du stock réellement, le numéro de lot ou de série prélevé doit être entré sur la commande avant qu’elle soit validée. La réservation non spécifique est remaniée au moment de la validation pour garantir que le numéro de lot ou de série prélevé puisse être entré sans perdre la réservation et que le numéro de série ou de lot prélevé puisse être totalement lettré et validé.  
  
### <a name="reserve-specific-serial-or-lot-numbers"></a>Réserver des numéros de série ou de lot particuliers
Dans ce scénario commercial, la fonctionnalité Lien tardif garantit qu’un utilisateur qui tente de réserver un numéro de série ou de lot particulier actuellement non spécifiquement réservé peut le faire. Une réservation non spécifique est remaniée au moment de la réservation pour libérer le numéro de série ou de lot de la demande spécifique.  
  
Le remaniement se produit automatiquement, mais une aide intégrée est affichée au bas de la page **Réservation** et indique le texte suivant :  
  
**XX de la Total Reserved Quantity ne sont pas spécifiques et peuvent être disponibles.**  
  
En outre, le champ **Qté réservée non spécifique** indique le nombre d’écritures réservation non spécifiques. Par défaut, ce champ n’est pas visible aux utilisateurs.  
  
### <a name="posting-an-outbound-document-with-nonspecific-reservation-of-serial-or-lot-numbers"></a>Validation d’un document sortant avec une réservation non spécifique d’un numéro de série ou de lot.
Ce scénario d’activité est pris en charge par la fonctionnalité Late Binding qui permet l’application fixe et la validation de sortie de ce qui est réellement prélevé en remaniant une autre réservation non spécifique d’un numéro de série ou de lot. Si le remaniement n’est pas possible, le message d’erreur type suivant s’affiche lorsque l’utilisateur tente de valider l’expédition :  
  
**L’article XX ne peut pas être totalement lettré.**  
  
## <a name="see-also"></a>Voir aussi
[Détails de conception : traçabilité](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
