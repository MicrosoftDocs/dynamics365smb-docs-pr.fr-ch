---
title: 'Gestion des QR-factures [CH]'
description: 'Cet article décrit les améliorations apportées à l''extension Gestion des QR-factures et la façon dont vous pouvez utiliser Business Central pour générer, envoyer et importer facilement vos QR-factures.'
author: sorenfriisalexandersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'QR-bill, invoice, incoming documents, payment reference'
ms.search.form: '11502, 11510, 11511, 11512, 11513, 11514, 11515, 11516, 11517, 11518'
ms.date: 04/05/2023
ms.author: soalex
---
# <a name="qr-bill-management-in-the-swiss-version-of-business-central"></a>Gestion des QR-factures dans la version suisse de Business Central

Depuis le 1er juillet 2020, les sociétés en Suisse doivent pouvoir recevoir des QR-factures. Les QR-factures sont des bordereaux de paiement qui suivent les factures, et constituent une initiative nationale visant à rationaliser les processus de paiement. Les QR-factures remplacent tous les borderaux de paiement existants et les fonctionnalités liées à l'ESR. Elles contiennent toutes les informations nécessaires pour effectuer les paiements, et un code QR sur le bordereau de paiement facilite l'importation des informations dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. Toutes les informations pertinentes sont importées et utilisées pour générer des paiements pour le fournisseur qui a envoyé la QR-facture, y compris la référence du paiement, qui est automatiquement incluse dans les écritures comptables fournisseurs et exportée dans les fichiers de paiement à la banque.

## <a name="get-started-with-the-qr-bill-management-extension"></a><a name="get-started"></a>Commencer à utiliser l'extension Gestion des QR-factures

L'extension Gestion des QR-factures est incluse et automatiquement installée dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. Pour commencer à utiliser l'extension, vous devez effectuer quelques changements de configuration dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. Pour y parvenir aisément, choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Paramétrage QR-facture**, puis sélectionnez le lien associé. Ce guide vous aide à saisir des informations, telles que :

* Spécifier s'il faut utiliser votre IBAN ou QR-IBAN. Un QR-IBAN est un IBAN qui contient un nombre entre 30000 et 31999 sur les positions 5 à 9, par exemple *CH55 30024 123456789012*.
* Définir la manière d'afficher les noms et adresses sur les QR-factures, et d'utiliser le codage allemand des caractères Umlaut. (Nous vous recommandons d'utiliser les valeurs par défaut).
* Sélectionnez la **Mise en page QR-facture par défaut**. La présentation détermine s'il faut utiliser l'IBAN ou le QR-IBAN, si le type de référence est la référence créancier ou QR, et s'il faut inclure les informations de facturation dans le format SWICO.
* Activez les types de factures vente et service, ainsi que les méthodes de paiement, pour les QR-factures.
* Spécifier le modèle feuille et le nom feuille à utiliser lorsque vous générez des feuilles achat à partir de QR-factures scannées ou importées.

Si nécessaire, vous pouvez modifier les paramètres de présentation sur la page **Mise en page QR-facture**.

## <a name="issuing-qr-bills"></a>Émission de QR-factures

Vous pouvez activer les QR-factures pour les factures vente et service. Cette option ajoute une écriture à la page **Sélection des états : Ventes** qui génère un PDF supplémentaire avec la QR-facture lors de la génération des factures. Pour activer la fonctionnalité, choisissez le champ **Types de document activés pour les QR-factures** sur la page **Paramétrage QR-facture**, et activez les types de document désirés en sélectionnant la case appropriée dans la colonne **Activé**.

## <a name="adding-billing-information-to-qr-bills"></a>Ajout d'informations de facturation aux QR-factures

Lorsque vous créez une QR-facture, vous pouvez inclure des informations de facturation au format SWICO, comme le préconise SIX, le fournisseur suisse de l'infrastructure de paiement. Idéalement, les applications commerciales qui produisent ou importent des QR-factures devraient également pouvoir traiter des informations telles que le montant de la TVA, le numéro de facture du fournisseur, etc., car elles peuvent être précieuses pour la facture à payer. Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], nous importons ces informations mais utilisons uniquement le numéro de facture du fournisseur. Si vous souhaitez inclure d'autres informations, vous devez opter pour une personnalisation.

## <a name="understanding-the-payment-reference"></a>Comprendre la référence de paiement

Les processus de paiement consistent à payer le bon montant à la bonne partie et à faciliter le rapprochement des paiements pour clôturer les comptes en souffrance. L'extension Gestion des QR-factures gère ces processus en générant une référence de paiement pour les QR-factures qui est unique pour les factures émises dans une société spécifique, ce qui signifie que la même référence de paiement ne peut pas être émise plusieurs fois.  

Si votre client utilise également [!INCLUDE[prod_short](../../includes/prod_short.md)], la référence de paiement est importée lors de la réception des QR-factures, transférée à leur page **Écritures comptables fournisseur** et utilisée comme référence lors de la création des paiements fournisseur. Pour plus d'informations, voir [Réception des QR-factures](ui-extensions-qr-bill-management.md#receiving-qr-bills).

Le flux est similaire à la fonctionnalité de référence ESR précédente que les QR-factures remplacent. Finalement, les fichiers de paiement (pain.001) sont envoyés de l'application commerciale du client à sa banque avec le message de transférer les montants sur le compte du fournisseur. La banque produit ensuite un fichier de relevé client (camt.054) que le fournisseur peut importer pour rapprocher les comptes. Ce fichier comprend la référence du paiement et est importé via la structure d'échange de données qui est mise à jour par l'extension Gestion des QR-factures pour importer les fichiers camt.054.

Pour les références ESR, vous pouvez par exemple configurer les informations de manière à ce qu'elles incluent le numéro de client et le numéro de facture. Vous ne pouvez pas configurer la référence de paiement dans les QR-factures. Il y aura toujours une relation 1:1 entre une QR-facture émise et un paiement, ce qui facilite le rapprochement et élimine la nécessité de configurer la référence de paiement sur les QR-factures. Au lieu de cela, [!INCLUDE[prod_short](../../includes/prod_short.md)] utilise un compteur unique pour la référence de paiement. En outre, une logique est présente pour bloquer l'importation ou la numérisation de la même référence de paiement deux fois.

### <a name="formats-for-qr-references-and-creditor-references"></a><a name="formats"></a>Formats pour les références QR et les références créditeur

La référence QR est composée de 26 positions numériques plus un chiffre de contrôle.  

La référence ISO du créditeur (ISO 11649) permet au créditeur d'effectuer des comparaisons automatiques entre ses factures et les paiements entrants. Elle doit inclure la valeur *RF* en positions 1-2 et un caractère de test correct en positions 3-4, et peut comprendre jusqu'à 25 caractères au maximum.  

## <a name="using-multiple-bank-accounts-as-issuers-of-qr-bills"></a><a name="multiplebankaccounts"></a>Utilisation de plusieurs comptes bancaires comme émetteurs de QR-factures

Les émetteurs de QR-factures peuvent utiliser plusieurs comptes bancaires pour acheminer les paiements vers différents comptes bancaires. Cela est lié au mode de paiement où vous spécifiez le **N° compte bancaire des QR-factures**. Une fois spécifié, l'information QR-IBAN/IBAN provenant de ce compte bancaire sera utilisée sur les QR-factures qui utilisent le mode de paiement donné. Vous pouvez ainsi acheminer les paiements entrants vers le compte bancaire souhaité. Si vous n'utilisez pas plusieurs comptes bancaires et que vous spécifiez le **N° compte bancaire des QR-factures** sur la fiche **Modes de paiement**, l'information QR-IBAN/IBAN provenant de la page **Informations sur la compagnie** est utilisée sur les QR-factures à la place. Assurez-vous d'y avoir configuré au moins les informations de votre compte bancaire principal. Pour plus d'informations, voir [Configurer des comptes bancaires](../../bank-how-setup-bank-accounts.md)

> [!NOTE]
> Si vous êtes un émetteur de QR-factures, configurez vos comptes bancaires de manière à afficher les bons comptes auprès de vos clients, selon que vous utilisez des QR-IBAN ou des IBAN ordinaires. Si vous êtes un receveur et payeur de QR-factures, nous vous recommandons de configurer correctement les comptes bancaires des fournisseurs pour le paiement et le transfert vers des comptes avec des IBAN ordinaires ou des QR-IBAN.

### <a name="adding-a-qr-iban-to-a-new-or-existing-bank-account"></a>Ajout d'un QR-IBAN à un compte bancaire nouveau ou existant

Pour utiliser un QR-IBAN différent de celui défini sur la page **Informations société**, spécifiez les informations de compte bancaire dans la **Fiche compte bancaire**:

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Dans la liste **Modes de règlement**, sélectionnez l'action **Nouveau** ou **Modifier**.
3. Sur le raccourci **Transfert**, entrez le compte bancaire dans le champ **QR-IBAN**.

## <a name="scanning-and-importing-qr-bills"></a>Numérisation et importation de QR-factures

Pour numériser ou importer une QR-facture, vous devez utiliser l'un des types de scanners suivants :

* Un scanner de saisie qui décode le code QR et simule le clavier pour coller la valeur décodée directement dans un champ de [!INCLUDE[prod_short](../../includes/prod_short.md)].
* Un scanner qui peut décoder le code QR et l'enregistrer dans un fichier .txt que vous importez dans [!INCLUDE[prod_short](../../includes/prod_short.md)]. 

> [!NOTE]
> Vous ne pouvez pas importer les QR-factures reçues sous forme de fichiers PDF directement dans [!INCLUDE[prod_short](../../includes/prod_short.md)] car [!INCLUDE[prod_short](../../includes/prod_short.md)] ne peut pas interpréter les codes QR. Vous devez utiliser l'une des méthodes de numérisation mentionnées ci-dessus.

## <a name="receiving-qr-bills"></a>Réception de QR-factures

Vous pouvez recevoir les QR-factures à plusieurs endroits dans [!INCLUDE[prod_short](../../includes/prod_short.md)] :

* **Documents entrants**, lorsque vous souhaitez qu'une QR-facture lance la création d'un nouveau document achat ou une nouvelle feuille achat.
* **Commandes achat et factures achat**, lorsque vous souhaitez importer des informations d'une QR-facture vers un document achat existant et l'utiliser pour valider le montant et la devise et pour stocker la référence de paiement.
* **Feuilles achat**, lorsque vous souhaitez créer de nouvelles lignes feuille achat basées sur les QR-factures. 

### <a name="receiving-a-qr-bill-through-an-incoming-document"></a>Réception d'une QR-facture par le biais d'un document entrant

La réception d'une QR-facture par le biais de documents entrants est particulièrement utile lorsque le processus est automatisé, mais vous pouvez également recevoir manuellement une QR-facture par le biais de documents entrants.

1. Choisissez l'icône d'![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Documents entrants**, puis sélectionnez le lien associé.
2. Dans la liste **Documents entrants**, créez une nouvelle écriture en choisissant **Nouveau**, puis **Nouveau**.
3. Sur la page **Document entrant**, entrez une description dans la champ **Description**.
4. Pour importer la QR-facture, choisissez l'une des actions suivantes :
   * **Numériser QR-facture** pour numériser une QR-facture dans l'écriture document entrant.
   * **Importer fichier QR-facture numérisé** pour utiliser un fichier généré par le deuxième type de scanner décrit dans la section [Numérisation et importation de QR-factures](#scanning-and-importing-qr-bills).

> [!TIP]
> Après avoir importé la QR-facture, vous pouvez vérifier les erreurs éventuelles dans le raccourci **Détails correspondance**.

À partir du document entrant, vous pouvez créer une feuille achat ou une facture achat, et la référence de paiement de la QR-facture est attribuée aux deux. Pour plus d'informations, voir [Utilisation des documents entrants](../../across-income-documents.md)

> [!NOTE]
> Lorsque vous importez des QR-factures, [!INCLUDE[prod_short](../../includes/prod_short.md)] recherchera un compte bancaire fournisseur avec un IBAN ou QR-IBAN correspondant. Lors de l’importation de QR-factures sur des documents entrants, un document ou une feuille achat est créé(e) et le compte bancaire du fournisseur détermine le fournisseur à utiliser. L'approche des documents entrants permet de s'assurer que le bon fournisseur est attribué. 

#### <a name="receiving-through-the-kofax-ocr-service"></a>Réception par le biais du service OCR Kofax

> [!NOTE]
> Si des sociétés existantes dans [!INCLUDE[prod_short](../../includes/prod_short.md)] veulent qu’une référence QR soit renvoyée lorsqu’elles utilisent le service OCR Kofax, elles doivent mettre à jour la définition d’échange de données existante utilisée comme **Type échange de données** pour le traitement des factures dans les documents entrants.  

Effectuez les étapes suivantes pour mettre à jour une définition d’échange de données existante. 

1. Sélectionnez l’icône d’![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Définitions d’échange de données**, puis sélectionnez le lien associé. 
2. Dans la liste **Définitions d’échange de données**, recherchez la ligne à mettre à jour, puis ouvrez la fiche. 
3. Sur le raccourci **Définitions ligne**, sélectionnez **OCRINVHEADER**.  
4. Sur le raccourci **Définitions de colonne**, créez une ligne, puis entrez les valeurs suivantes.

    | Champ | Valeur |
    |-------|-------|
    | **N° colonne** | 11513 |
    | **Nom** | N ° référence QR-facture suisse |
    | **Description** | N ° référence QR-facture suisse |
    | **Chemin** | /Document/HeaderFields/HeaderField\[Type\[text()='qrreference'\]\]/Text |
    
5. Sur le raccourci **Définitions ligne**, sélectionnez **Correspondance champ**.  
6. Sur la page **Correspondance champ**, créez une ligne, puis entrez les valeurs suivantes.

    | Champ | Valeur |
    |-------|-------|
    | **N° colonne** | 11513 |
    | **ID table cible** | 38 |
    | **ID champ cible** | 171 |
    | **Valider uniquement** | FAUX |

7. Fermez les pages.  

### <a name="receiving-a-qr-bill-through-purchase-orders-or-purchase-invoices"></a>Réception d'une QR-facture par le biais de commandes achat ou de factures achat

La réception d'une QR-facture par le biais d'une commande achat ou d'une facture achat valide le montant de la facture et ajoute la référence de paiement à la comptabilité. Comme pour les documents entrants, vous pouvez numériser ou importer une QR-facture dans une facture ou une commande achat existante. Ce processus utilise le QR-IBAN ou IBAN de la QR-facture pour trouver le fournisseur ayant un numéro correspondant. En l'absence de correspondance, vous ne pouvez pas numériser ou importer la QR-facture et vous devrez donc créer le compte bancaire fournisseur et ensuite permettre que la QR-facture soit jointe au document achat.

* Pour ajouter une QR-facture à un document achat existant, sélectionnez le document cible, puis choisissez l'action **Numériser QR-facture** ou **Importer fichier QR-facture numérisé** sur la page **Commandes achat** ou **Factures achat**.

Lorsque la QR-facture est numérisée ou importée dans le document achat, le montant, la référence de paiement ainsi que d'autres informations figurant sur la QR-facture sont ajoutés. Ces données serviront pour la validation avant la comptabilisation du document achat. La comptabilisation sera bloquée si le montant sur la commande ou la facture ne correspond pas à celui sur la QR-facture. Une validation se produit également si vous numérisez ou importez la QR-facture. Si la référence de paiement est déjà utilisée sur une écriture comptable fournisseur pour un fournisseur, une erreur s'affiche. Les fournisseurs ne peuvent pas émettre plusieurs QR-factures avec la même référence de paiement. De même, une erreur s'affiche si la QR-facture et la référence de paiement ont déjà été importées vers un document achat ouvert.

### <a name="receiving-a-qr-bill-through-a-purchase-journal"></a>Réception d'une QR-facture par le biais d'une feuille achat

Vous pouvez numériser ou importer des QR-factures directement dans une feuille achat. Cette option est utile lorsque vous souhaitez créer de nouvelles lignes feuille basées sur une QR-facture. La numérisation ou l'importation directement dans une feuille achat créer une nouvelle **Ligne feuille achat** qui utilise le fournisseur et le montant de la QR-facture, et tente d'identifier le fournisseur en trouvant un **Compte bancaire fournisseur** contenant un IBAN ou QR-IBAN correspondant. Par exemple, il est utile d'utiliser des feuilles achat si vous ne souhaitez pas utiliser de factures ou commandes achat.

1. Choisissez l'icône d'![ Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Feuilles achat**, puis sélectionnez le lien associé.
2. Dans la liste **Feuilles achat**, créez une nouvelle écriture en choisissant l'une des actions suivantes :
   * **Numériser QR-facture** pour numériser une QR-facture dans l'écriture document entrant.
   * **Importer fichier QR-facture numérisé** pour utiliser le fichier généré par le deuxième type de scanner décrit dans la section [Numérisation et importation de QR-factures](#scanning-and-importing-qr-bills).

## <a name="reconciliation"></a>Rapprochement

Lors de l'importation de transactions bancaires (camt) sur la page **Feuilles rapprochement paiement**, le fichier est supposé inclure la référence de paiement et les **Écritures comptables client** correspondantes sont automatiquement trouvées pour régler la transaction.

## <a name="see-also"></a>Voir aussi

[Paiements électroniques, Suisse](swiss-electronic-payments.md)  
[Fonctionnalité locale, Suisse](switzerland-local-functionality.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
