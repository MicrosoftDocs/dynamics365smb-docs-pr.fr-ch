---
title: Consolider les soldes d’une société qui est à la fois un client et un fournisseur
description: Décrit comment consolider les soldes d’un client qui est aussi un fournisseur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor"></a>Consolider les soldes d’une société qui est à la fois un client et un fournisseur
Une société avec laquelle vous travaillez peut être à la fois un client et un fournisseur. Lorsque c’est le cas, vous pouvez éviter d’effectuer des paiements ou des réceptions inutiles et peut-être économiser sur les frais de transaction en consolidant les soldes client et fournisseur de la société. La consolidation compare les soldes de la société en tant que fournisseur et en tant que client, puis ajuste le montant de sorte que soit le solde du client soit le solde du fournisseur reste, selon le montant le plus élevé. 

Pour consolider les soldes, vous devez d’abord lier les sociétés client et fournisseur via un contact de type **Société**. Un client ou un fournisseur ne peut avoir qu’un seul contact du type **Société**. Pour plus d’informations, voir [Créer des contacts](marketing-create-contact-companies.md).

Après avoir lié les sociétés, la page **Fiche client** comporte le champ **Solde en tant que fournisseur** et la page **Fiche fournisseur** comporte le champ **Solde en tant que client**.

Bien que ce ne soit pas une exigence, les sociétés client et fournisseur sont généralement la même entité juridique. 

## <a name="before-you-start"></a>Avant de commencer
Avant de consolider les soldes, spécifiez quelques paramètres sur la page **Paramètres marketing**. 

* Dans le raccourci **Interactions**, vous devez spécifier les codes relation d’affaires dans les champs **Clients** et **Fournisseurs**. [!INCLUDE[prod_short](includes/prod_short.md)] utilise ces informations pour déterminer le type de relation à afficher pour les contacts. 
* Facultatif : dans le raccourci **Doublons**, activez ou désactivez la recherche des doublons. Par défaut, la recherche de doublons est activée. Pour plus d’informations, voir [Gestion des doublons](#handling-duplicates). 

## <a name="link-an-existing-customer-and-vendor-company-through-a-contact"></a>Lier une société client et fournisseur via un contact
Les étapes suivantes décrivent comment lier un client et un fournisseur via un contact.

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Client** ou **Fournisseur**, puis choisissez le lien associé.
2. Choisissez le client ou le fournisseur, puis sélectionnez l’action **Contact**.
3. Si le champ **Relation d’affaires contact** contient une valeur autre que **Aucune**, vous devez supprimer la relation. Pour ce faire, utilisez l’action **Relation d’affaires**, puis supprimez la relation. 
4. Selon que vous avez choisi **Client** ou **Fournisseur** à l’étape 1, choisissez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") puis saisissez l’autre partie. C’est-à-dire que si vous avez choisi **Fournisseur**, vous devez rechercher **Client**.
5. Choisissez le fournisseur ou le client, puis choisissez l’action **Contacts**.
6. Sélectionnez l’action **Lier avec existant**, puis sélectionnez l’option **Client** ou **Fournisseur**.
7. Choisissez le client ou le fournisseur.

## <a name="create-a-vendor-from-a-customer-or-vice-versa"></a>Créer un client à partir d’un fournisseur ou inversement
Vous pouvez créer un fournisseur à partir d’un client existant ou un client à partir d’un fournisseur. À partir des pages **Client** ou **Fournisseur**, ouvrez la page **Contact**. Sélectionnez l’action **Créer comme**, puis sélectionnez les options **Client** ou **Fournisseur**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact"></a>Créer un client ou fournisseur et le lier via un contact fournisseur ou un contact client
1. Créez un client ou un fournisseur. Pour plus d’informations, voir [Enregistrer de nouveaux clients](sales-how-register-new-customers.md) ou [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).
2. Après avoir configuré le client ou le fournisseur, choisissez l’action **Créer**, puis choisissez l’option **Client** ou l’option **Fournisseur**. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company"></a>Pour consolider les soldes client et fournisseur pour une société contact
Sur la page **Feuille paiement**, utilisez l’action **Soldes client/fournisseur nets** pour consolider les soldes client/fournisseur en un seul montant net. L’action crée, mais ne valide pas, les lignes feuille paiement qui contiennent les soldes nets.

> [!NOTE]
> Si les soldes client ou fournisseur contiennent des montants dans des devises différentes, une ligne est créée pour le montant dans chaque devise.

## <a name="handling-duplicates"></a>Gestion des doublons
Si vous activez la recherche de doublons dans le raccourci **Doublons** sur la page **Paramètres marketing**, un avertissement s’affiche lorsque vous modifiez les valeurs des champs qui font partie des paramètres des chaînes de recherche de doublons. Lorsqu’un doublon est trouvé, vous pouvez effectuer les actions suivantes :

* Combiner les contacts en double en un seul contact qui est le même pour le client et le fournisseur en utilisant la fonctionnalité **Fusionner avec** sur la page **Fiche contact**. En règle générale, la fusion des contacts n’est effectuée que lorsque le client et le fournisseur sont la même entité juridique. Pour en savoir plus, reportez-vous à la rubrique [Fusionner l’enregistrement des doublons](sales-how-merge-duplicate-records.md). 
* Supprimer la relation d’affaires fournisseur pour le contact fournisseur ou client, puis utiliser l’action **Lier à un élément existant** pour créer un lien vers un autre contact.    

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)  
