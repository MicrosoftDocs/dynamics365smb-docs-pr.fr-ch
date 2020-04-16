---
title: Gestion des QR-factures | Microsoft Docs
description: Configurez l'extension Gestion des QR-factures et générez, envoyez et importez facilement des QR-factures.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QR-bill, invoice, incoming documents, payment reference
ms.date: 04/01/2020
ms.author: soalex
ms.openlocfilehash: 6cf85170efe4f2d415adc1b1db83699730a6ea60
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196419"
---
# <a name="qr-bill-management-in-d365fin"></a>Gestion des QR-factures dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)]
À partir du 1er juillet 2020, les sociétés en Suisse doivent pouvoir recevoir des QR-factures. Les QR-factures sont des bordereaux de paiement qui suivent les factures, et constituent une initiative nationale visant à rationaliser les processus de paiement. Les QR-factures remplacent tous les borderaux de paiement existants et les fonctionnalités liées à l'ESR. Elles contiennent toutes les informations nécessaires pour effectuer les paiements, et un code QR sur le borderau de paiement facilite l'importation des informations dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Toutes les informations pertinentes sont importées et utilisées pour générer des paiements pour le vendeur qui a envoyé la QR-facture, y compris la référence du paiement, qui est automatiquement incluse dans les écritures comptables fournisseurs et exportée dans les fichiers de paiement à la banque.

## <a name="get-started-with-the-qr-bill-management-extension"></a>Commencer à utiliser l'extension Gestion des QR-factures
L'extension Gestion des QR-factures est incluse et automatiquement installée dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Pour commencer à utiliser l'extension, vous devez effectuer quelques changements de configuration dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Un moyen simple d'y parvenir est d'utiliser le guide de configuration assistée Configuration des QR-factures. Ce guide vous aidera à saisir des informations, telles que :

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
Lorsque vous créez une QR-facture, vous pouvez inclure des informations de facturation au format SWICO, comme le préconise SIX, le fournisseur suisse de l'infrastructure de paiement. Idéalement, les applications commerciales qui produisent ou importent des QR-factures devraient également pouvoir traiter des informations telles que le montant de la TVA, le numéro de facture du fournisseur, etc., car elles peuvent être précieuses pour la facture à payer. Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], nous importons ces informations mais utilisons uniquement le numéro de facture du fournisseur. Si vous souhaitez utiliser les autres informations, vous pouvez créer votre propre personnalisation.

## <a name="understanding-the-payment-reference"></a>Comprendre la référence de paiement
Les processus de paiement consistent à payer le bon montant à la bonne partie et à faciliter le rapprochement des paiements pour clôturer les comptes en souffrance. L'extension Gestion des QR-factures gère cela en générant une référence de paiement pour les QR-factures qui sont uniques pour les factures émises dans une société spécifique, ce qui signifie que la même référence de paiement ne peut pas être émise plusieurs fois. Si votre client utilise [!INCLUDE[d365fin](../../includes/d365fin_md.md)], la référence de paiement est importée lors de la réception des QR-factures, transférée à la page des Écritures comptables fournisseur et utilisée comme référence lors de la création des paiements fournisseur. Pour plus d'informations, voir [Réception des QR-factures](ui-extensions-qr-bill-management.md#receiving-qr-bills). Le flux est similaire à la fonctionnalité Référence ESR précédente que les QR-factures remplacent. Finalement, les fichiers de paiement (pain.001) seront envoyés de l'application commerciale du client à sa banque avec le message de transférer les montants sur le compte du fournisseur. La banque produira un fichier de relevé client (camt.054) que le fournisseur pourra importer pour rapprocher les comptes. Ce fichier comprendra la référence du paiement et est importé via la structure d'échange de données qui est mise à jour par l'extension Gestion des QR-factures pour importer les fichiers camt.054.  
Pour les références ESR, vous pouviez par exemple configurer les informations de manière à ce qu'elles contiennent le numéro de client et le numéro de facture. Vous ne pouvez pas configurer la référence de paiement dans les QR-factures. Il y aura toujours une relation 1:1 entre une QR-facture émise et un paiement, ce qui facilite le rapprochement et élimine la nécessité de configurer la référence de paiement sur les QR-factures. Au lieu de cela, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] utilise un compteur unique pour la référence de paiement. En outre, une logique est présente pour bloquer l'importation ou la numérisation de la même référence de paiement deux fois.

## <a name="scanning-and-importing-qr-bills"></a>Numérisation et importation de QR-factures
Pour numériser ou importer une QR-facture, vous devez utiliser l'un des types de scanners suivants :

* Un scanner de saisie qui décode le code QR et simule le clavier pour coller la valeur décodée directement dans un champ de [!INCLUDE[d365fin](../../includes/d365fin_md.md)].
* Un scanner qui peut décoder le code QR et l'enregistrer dans un fichier .txt que vous importez dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. 

> [!Note]
> Vous ne pouvez pas importer les QR-factures reçues sous forme de fichiers PDF directement dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)] car [!INCLUDE[d365fin](../../includes/d365fin_md.md)] ne peut pas interpréter les codes QR. Vous devez utiliser l'une des méthodes de numérisation.

## <a name="receiving-qr-bills"></a>Réception de QR-factures
Vous pouvez recevoir les QR-factures à plusieurs endroits dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)] :

* **Documents entrants**, lorsque vous souhaitez qu'une QR-facture lance la création d'un nouveau document achat ou une nouvelle feuille achat.
* **Commandes achat et factures achat**, lorsque vous souhaitez importer des informations d'une QR-facture vers un document achat existant et les utiliser pour valider le montant et la devise et pour stocker la référence de paiement (Cette fonctionnalité est prévue pour la mise à jour de mai 2020 de [!INCLUDE[d365fin](../../includes/d365fin_md.md)]).
* **Feuilles achat**, lorsque vous souhaitez créer de nouvelles lignes feuille achat basées sur les QR-factures (Cette fonctionnalité est prévue pour la mise à jour de mai 2020 de [!INCLUDE[d365fin](../../includes/d365fin_md.md)]). 

### <a name="to-receive-a-qr-bill-through-an-incoming-documents"></a>Pour recevoir une QR-facture par le biais d'un document entrant
La réception d'une QR-facture par le biais de documents entrants est particulièrement utile lorsque le processus est automatisé, mais vous pouvez également recevoir manuellement une QR-facture par le biais de documents entrants.

1. Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Documents entrants**, puis choisissez le lien associé.
2. Dans la liste **Documents entrants**, créez une nouvelle écriture en choisissant **Nouveau**, puis **Nouveau**. 
3. Sur la page **Document entrant**, entrez une description dans la champ **Description**.
4. Pour importer la QR-facture, choisissez **Actions**, puis **QR-facture**, puis **Numériser QR-facture** pour numériser une QR-facture dans l'écriture document entrant.
 
> [!TIP]
> Après avoir importé la QR-facture, vous pouvez vérifier les erreurs éventuelles dans le raccourci **Détails correspondance**.

À partir du document entrant, vous pouvez créer une feuille achat ou une facture achat, et la référence de paiement de la QR-facture sera attribuée aux deux.

> [!Note]
> Lorsque vous importez des QR-factures, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] tentera de trouver un compte bancaire fournisseur avec un IBAN ou QR-IBAN correspondant. Lors de l'importation de QR-factures sur des documents entrants, et donc de la création d'un document ou d'une feuille achat, le compte bancaire du fournisseur déterminera le fournisseur à utiliser. L'approche des documents entrants permet de s'assurer que le bon fournisseur est attribué.

<!--

### Receiving a QR-Bill through Purchase Order or Purchase Invoice (Planned for May, 2020)
Receiving a QR-bill through a purchase order or purchase invoice validates the invoice amount and adds the payment reference to the ledgers. Like incoming documents, you can scan or import a QR-bill to an existing purchase order or invoice. This process uses the QR-IBAN or IBAN from the QR-bill to find the vendor with a matching number. If no match is found you cannot scan or import the QR-bill. If that happens, you can create the vendor bank account and then allow the QR-bill to be attached to the purchase document. When the QR-bill is scanned or imported to the purchase document it will add the amount, payment reference, and other information from the QR-bill. This is used for validation before posting the purchase document. Posting will be blocked if the amount of the order or invoice does not match the amount from the QR-bill. Validation also happens when you scan or import the QR-bill. If the payment reference is already used on a vendor ledger entry for a vendor, an error will display. Vendors cannot issue multiple QR-bills with the same payment reference. Similarly, an error will display if the QR-bill and payment reference has already been imported to an open purchase document. 

### Receiving a QR-Bill through a Purchase Journal (Planned for May, 2020)
You can scan or import QR-bills directly into a **Purchase Journal**. This is useful when you want to create new journal lines based on a QR-bill. Scanning or importing directly into a purchase journal creates a new **Purchase Journal Line** using the vendor and amount from the QR-bill, and tries to identify the vendor by finding a **Vendor Bank Account** that has a matching IBAN or QR-IBAN. For example, using purchase journals is useful if you do not want to use purchase orders or invoices.  -->

## <a name="reconciliation"></a>Rapprochement
Lors de l'importation de transactions bancaires (camt) sur la page Feuille rapprochement bancaire, le fichier est supposé inclure <!--not sure what "assumed to include" means--> la référence du paiement, qui trouvera automatiquement les **Écritures comptables client** à régler.    

## <a name="upcoming-capabilities-for-qr-bills"></a>Fonctionnalités futures des QR-factures
Nous prévoyons d'ajouter des fonctionnalités à l'extension Gestion des QR-factures dans les prochaines mises à jour de la vague 1 de la version 2020. Par exemple, vous pourrez recevoir des QR-factures par le biais de documents achat et de feuilles achat. Cela fournira des validations supplémentaires et vous permettra d'automatiser et de rationaliser les processus de réception. Pour savoir quand cela aura lieu, gardez un œil sur notre [Plan de versions](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-business-central/qr-bill-management-switzerland).

## <a name="see-also"></a>Voir aussi
[Fonctionnalité locale, Suisse](switzerland-local-functionality.md)  
