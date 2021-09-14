---
title: Gestion des QR-factures [CH]
description: Cet article décrit les améliorations apportées à l'extension Gestion des QR-factures et la façon dont vous pouvez utiliser Business Central pour générer, envoyer et importer facilement vos QR-factures.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QR-bill, invoice, incoming documents, payment reference
ms.date: 09/06/2021
ms.author: soalex
ms.openlocfilehash: a1ec0dfceba2755c70b8532ff00d49a4d76aba98
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482418"
---
# <a name="qr-bill-management-in-the-swiss-version-of-business-central"></a>Gestion des QR-factures dans la version suisse de Business Central
À partir du 1er juillet 2020, les sociétés en Suisse doivent pouvoir recevoir des QR-factures. Les QR-factures sont des bordereaux de paiement qui suivent les factures, et constituent une initiative nationale visant à rationaliser les processus de paiement. Les QR-factures remplacent tous les borderaux de paiement existants et les fonctionnalités liées à l'ESR. Elles contiennent toutes les informations nécessaires pour effectuer les paiements, et un code QR sur le borderau de paiement facilite l'importation des informations dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. Toutes les informations pertinentes sont importées et utilisées pour générer des paiements pour le vendeur qui a envoyé la QR-facture, y compris la référence du paiement, qui est automatiquement incluse dans les écritures comptables fournisseurs et exportée dans les fichiers de paiement à la banque.

## <a name="get-started-with-the-qr-bill-management-extension"></a>Commencer à utiliser l'extension Gestion des QR-factures
L'extension Gestion des QR-factures est incluse et automatiquement installée dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. Pour commencer à utiliser l'extension, vous devez effectuer quelques changements de configuration dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. Un moyen simple d'y parvenir est d'utiliser le guide de configuration assistée Configuration des QR-factures. Ce guide vous aidera à saisir des informations, telles que :

* Spécifier s'il faut utiliser votre IBAN ou QR-IBAN.
* Définir la manière d'afficher les noms et adresses sur les QR-factures, et d'utiliser le codage allemand des caractères Umlaut. Nous vous recommandons d'utiliser les valeurs par défaut.
* Sélectionner la présentation par défaut à utiliser pour les QR-factures. La présentation détermine s'il faut utiliser l'IBAN ou le QR-IBAN, si le type de référence est la référence créancier ou QR, et s'il faut inclure les informations de facturation dans le format SWICO.
* Activer les types de factures vente et service, ainsi que les méthodes de paiement, pour les QR-factures.
* Spécifier le modèle feuille et le nom feuille à utiliser lorsque vous générez des feuilles achat à partir de QR-factures scannées ou importées.

Si nécessaire, vous pouvez modifier ces paramètres sur les pages suivantes : 

* **Configuration des QR-factures** pour modifier les paramètres généraux. 
* **Présentation des QR-factures** pour modifier les paramètres de présentation.

## <a name="issuing-qr-bills"></a>Émission de QR-factures
Vous pouvez activer les QR-factures pour les factures vente et service. Cela ajoute une écriture à **Sélection des états : Ventes** qui génère un PDF supplémentaire avec la QR-facture lors de la génération des factures. 

## <a name="adding-billing-information-to-qr-bills"></a>Ajout d'informations de facturation aux QR-factures
Lorsque vous créez une QR-facture, vous pouvez inclure des informations de facturation au format SWICO, comme le préconise SIX, le fournisseur suisse de l'infrastructure de paiement. Idéalement, les applications commerciales qui produisent ou importent des QR-factures devraient également pouvoir traiter des informations telles que le montant de la TVA, le numéro de facture du fournisseur, etc., car elles peuvent être précieuses pour la facture à payer. Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], nous importons ces informations mais utilisons uniquement le numéro de facture du fournisseur. Si vous souhaitez utiliser les autres informations, vous pouvez créer votre propre personnalisation.

## <a name="understanding-the-payment-reference"></a>Comprendre la référence de paiement
Les processus de paiement consistent à payer le bon montant à la bonne partie et à faciliter le rapprochement des paiements pour clôturer les comptes en souffrance. L'extension Gestion des QR-factures gère cela en générant une référence de paiement pour les QR-factures qui sont uniques pour les factures émises dans une société spécifique, ce qui signifie que la même référence de paiement ne peut pas être émise plusieurs fois. Si votre client utilise [!INCLUDE[prod_short](../../includes/prod_short.md)], la référence de paiement est importée lors de la réception des QR-factures, transférée à la page des Écritures comptables fournisseur et utilisée comme référence lors de la création des paiements fournisseur. Pour plus d'informations, voir [Réception des QR-factures](ui-extensions-qr-bill-management.md#receiving-qr-bills). Le flux est similaire à la fonctionnalité Référence ESR précédente que les QR-factures remplacent. Finalement, les fichiers de paiement (pain.001) seront envoyés de l'application commerciale du client à sa banque avec le message de transférer les montants sur le compte du fournisseur. La banque produira un fichier de relevé client (camt.054) que le fournisseur pourra importer pour rapprocher les comptes. Ce fichier comprendra la référence du paiement et est importé via la structure d'échange de données qui est mise à jour par l'extension Gestion des QR-factures pour importer les fichiers camt.054.  
Pour les références ESR, vous pouviez par exemple configurer les informations de manière à ce qu'elles contiennent le numéro de client et le numéro de facture. Vous ne pouvez pas configurer la référence de paiement dans les QR-factures. Il y aura toujours une relation 1:1 entre une QR-facture émise et un paiement, ce qui facilite le rapprochement et élimine la nécessité de configurer la référence de paiement sur les QR-factures. Au lieu de cela, [!INCLUDE[prod_short](../../includes/prod_short.md)] utilise un compteur unique pour la référence de paiement. En outre, une logique est présente pour bloquer l'importation ou la numérisation de la même référence de paiement deux fois.

## <a name="using-multiple-bank-accounts-as-issuers-of-qr-bills"></a>Utilisation de plusieurs comptes bancaires comme émetteurs de QR-factures
Les émetteurs de QR-factures peuvent utiliser plusieurs comptes bancaires pour acheminer les paiements vers différents comptes bancaires. Cette fonctionnalité est liée au mode de paiement sur lequel vous pouvez spécifier le **N° compte bancaire des QR-factures**. Lorsqu'elle est spécifiée, l'information IBAN/QR-IBAN de ce compte bancaire sera utilisée sur les QR-factures qui utilisent la méthode de paiement donnée. Vous pouvez ainsi acheminer les paiements entrants vers le compte bancaire souhaité. Si vous n'utilisez pas plusieurs comptes bancaires et que vous spécifiez le **N° compte bancaire des QR-factures** sur la carte de mode de paiement, l'information QR-IBAN/IBAN provenant des informations sur la compagnie est utilisée sur les QR-factures à la place. Assurez-vous d'y avoir configuré au moins les informations de votre compte bancaire principal.

## <a name="scanning-and-importing-qr-bills"></a>Numérisation et importation de QR-factures
Pour numériser ou importer une QR-facture, vous devez utiliser l'un des types de scanners suivants :

* Un scanner de saisie qui décode le code QR et simule le clavier pour coller la valeur décodée directement dans un champ de [!INCLUDE[prod_short](../../includes/prod_short.md)].
* Un scanner qui peut décoder le code QR et l'enregistrer dans un fichier .txt que vous importez dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. 

> [!Note]
> Vous ne pouvez pas importer les QR-factures reçues sous forme de fichiers PDF directement dans [!INCLUDE[prod_short](../../includes/prod_short.md)] car [!INCLUDE[prod_short](../../includes/prod_short.md)] ne peut pas interpréter les codes QR. Vous devez utiliser l'une des méthodes de numérisation.

## <a name="receiving-qr-bills"></a>Réception de QR-factures
Vous pouvez recevoir les QR-factures à plusieurs endroits dans [!INCLUDE[prod_short](../../includes/prod_short.md)] :

* **Documents entrants**, lorsque vous souhaitez qu'une QR-facture lance la création d'un nouveau document achat ou une nouvelle feuille achat.
* **Commandes achat et factures achat**, lorsque vous souhaitez importer des informations d'une QR-facture vers un document achat existant et l'utiliser pour valider le montant et la devise et pour stocker la référence de paiement.
* **Feuilles achat**, lorsque vous souhaitez créer de nouvelles lignes feuille achat basées sur les QR-factures. 

### <a name="to-receive-a-qr-bill-through-an-incoming-documents"></a>Pour recevoir une QR-facture par le biais d'un document entrant
La réception d'une QR-facture par le biais de documents entrants est particulièrement utile lorsque le processus est automatisé, mais vous pouvez également recevoir manuellement une QR-facture par le biais de documents entrants.

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Documents entrants**, puis sélectionnez le lien associé.
2. Dans la liste **Documents entrants**, créez une nouvelle écriture en choisissant **Nouveau**, puis **Nouveau**. 
3. Sur la page **Document entrant**, entrez une description dans la champ **Description**.
4. Pour importer la QR-facture, choisissez **Actions**, puis **QR-facture**, puis **Numériser QR-facture** pour numériser une QR-facture dans l'écriture document entrant.
 
> [!TIP]
> Après avoir importé la QR-facture, vous pouvez vérifier les erreurs éventuelles dans le raccourci **Détails correspondance**.

À partir du document entrant, vous pouvez créer une feuille achat ou une facture achat, et la référence de paiement de la QR-facture sera attribuée aux deux.

> [!Note]
> Lorsque vous importez des QR-factures, [!INCLUDE[prod_short](../../includes/prod_short.md)] tentera de trouver un compte bancaire fournisseur avec un IBAN ou QR-IBAN correspondant. Lors de l'importation de QR-factures sur des documents entrants, et donc de la création d'un document ou d'une feuille achat, le compte bancaire du fournisseur déterminera le fournisseur à utiliser. L'approche des documents entrants permet de s'assurer que le bon fournisseur est attribué.

### <a name="receiving-a-qr-bill-through-purchase-order-or-purchase-invoice"></a>Réception d'une QR-facture par le biais d'une commande achat ou d'une facture achat
La réception d'une QR-facture par le biais d'une commande achat ou d'une facture achat valide le montant de la facture et ajoute la référence de paiement à la comptabilité. Comme pour les documents entrants, vous pouvez numériser ou importer une QR-facture dans une facture ou une commande achat existante. Ce processus utilise le QR-IBAN ou IBAN de la QR-facture pour trouver le fournisseur ayant un numéro correspondant. Si aucune correspondance n'est trouvée, vous ne pouvez pas numériser ou importer la QR-facture. Dans ce cas, vous pouvez créer le compte bancaire fournisseur et ensuite permettre que la QR-facture soit jointe au document achat. Lorsque la QR-facture est numérisée ou importée dans le document achat, elle ajoutera le montant, la référence de paiement ainsi que d'autres informations figurant sur la QR-facture. Elles serviront pour la validation avant la comptabilisation du document achat. La comptabilisation sera bloquée si le montant de la commande ou de la facture ne correspond pas à celui de la QR-facture. Une validation se produit également si vous numérisez ou importez la QR-facture. Si la référence de paiement est déjà utilisée sur une écriture comptable fournisseur pour un fournisseur, une erreur s'affichera. Les fournisseurs ne peuvent pas émettre plusieurs QR-factures avec la même référence de paiement. De même, une erreur s'affichera si la QR-facture et la référence de paiement ont déjà été importées vers un document achat ouvert. 

### <a name="receiving-a-qr-bill-through-a-purchase-journal"></a>Réception d'une QR-facture par le biais d'une feuille achat
Vous pouvez numériser ou importer des QR-factures directement dans une **feuille achat**. C'est utile lorsque vous souhaitez créer de nouvelles lignes feuille basées sur une QR-facture. La numérisation ou l'importation directement dans une feuille achat créer une nouvelle **ligne feuille achat** qui utilise le fournisseur et le montant de la QR-facture, et tente d'identifier le fournisseur en trouvant un **Compte bancaire fournisseur** ayant un IBAN ou QR-IBAN correspondant. Par exemple, il est utile d'utiliser des feuilles achat si vous ne souhaitez pas utiliser de factures ou commandes achat.

## <a name="reconciliation"></a>Rapprochement
Lors de l'importation de transactions bancaires (camt) sur la page Feuille rapprochement bancaire, le fichier est supposé inclure la référence de paiement qui trouvera automatiquement les **écritures comptables client** correspondantes à régler.    

## <a name="upcoming-capabilities-for-qr-bills"></a>Fonctionnalités futures des QR-factures
Nous prévoyons d'ajouter des fonctionnalités à l'extension Gestion des QR-factures dans les prochaines mises à jour de la vague 1 de la version 2020. Par exemple, vous pourrez recevoir des QR-factures par le biais de documents achat et de feuilles achat. Cela fournira des validations supplémentaires et vous permettra d'automatiser et de rationaliser les processus de réception. Pour savoir quand cela aura lieu, gardez un œil sur notre [Plan de versions](/dynamics365-release-plan/2020wave1/dynamics365-business-central/qr-bill-management-switzerland).

## <a name="see-also"></a>Voir aussi
[Fonctionnalité locale, Suisse](switzerland-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
