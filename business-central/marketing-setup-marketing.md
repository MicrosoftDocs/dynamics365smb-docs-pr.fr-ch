---
title: Informations sur la configuration de la gestion du marketing et des contacts
description: "Vous pouvez configurer la gestion du marketing et des contacts dans Business\_Central pour optimiser les relations avec les prospects ou les clients, et améliorer des campagnes ou des promotions."
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect, client, customer, campaign, promo'
ms.search.forms: '5172, 5173, 5170, 5094, 429'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-relationship-management"></a>Paramétrage de la Gestion des relations

Avant de commencer à travailler avec vos contacts et prospects marketing, vous devez prendre certaines décisions et accomplir certaines étapes afin de configurer la façon dont le module marketing gère certains aspects de vos contacts. Par exemple, vous pouvez décider de synchroniser la fiche contact avec la fiche client, la fiche fournisseur, ou la fiche compte bancaire, spécifier comment les souches de numéros sont définies, ou quelles sont les salutations standard lorsque vous écrivez à vos contacts.

La gestion de vos contacts et la mise en place d’une stratégie visant à identifier, attirer et fidéliser les clients permet d’optimiser votre activité et d’accroître la satisfaction des clients. L’utilisation d’un système de gestion de contacts performant permet également de créer et de maintenir les relations avec vos clients. La communication est la clé de ces relations. Pour assurer la réussite de votre entreprise, il est nécessaire de personnaliser la communication avec les clients, fournisseurs et partenaires commerciaux potentiels et existants en fonction de leurs besoins spécifiques. La première étape consiste à établir une stratégie et à définir la manière dont votre société utilise les informations de contact. Dans la mesure où celles-ci seront consultées par de nombreux groupes différents de votre société, la mise en place d’un système performant permettra d’accroître la productivité.

Vous configurez la gestion du marketing et des contacts à partir de la page **Paramètres marketing**. Pour ouvrir la page **Paramètres marketing**, choisissez l’icône ![Ampoule qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration marketing**, puis choisissez le lien associé.

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Copie automatique des informations spécifiques des sociétés contact vers les personnes contact
Une partie des données relatives aux sociétés contact sont identiques aux données sur les personnes contact qui travaillent dans ces sociétés, comme l’adresse. Dans la section **Héritage** de la page **Paramètres marketing**, vous pouvez définir l’application de sorte qu’elle copier automatiquement des champs spécifiques de la fiche société contact vers la fiche personne contact chaque fois que vous créez une personne contact pour une société contact. Par exemple, vous pouvez choisir de copier un code vendeur, les infos adresse (adresse, adresse 2ème ligne, ville, code postal et région), les détails de communication (numéro de télécopie, numéro de télex et numéro de téléphone), et plus encore.

Lorsque vous modifiez l’un des champs dans la fiche société contact, l’application modifie automatiquement ce champ dans la fiche personne contact (sauf si vous avez modifié ce champ manuellement).

Pour plus d’informations, voir [Créer des contacts](marketing-create-contact-companies.md).

## <a name="use-predefined-defaults-on-new-contacts"></a>Utiliser des paramètres par défaut prédéfinis sur les nouveaux contacts
Vous pouvez configurer l’application pour qu’elle affecte automatiquement des codes langue, secteur, vendeur et pays/région par défaut à chaque nouveau contact. Vous pouvez également entrer un code cycle de vente par défaut que l’application affecte automatiquement à chaque nouvelle opportunité.

Les valeurs héritées des champs sont prioritaires sur les valeurs par défaut que vous avez définies. Par exemple, si vous avez choisi le français comme langue par défaut alors que la langue de la société contact est l’allemand, l’application affecte automatiquement le code langue de l’allemand aux personnes contact enregistrées pour cette société.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Enregistrement automatique des interactions
[!INCLUDE[prod_short](includes/prod_short.md)] peut enregistrer automatiquement les documents achat et vente en tant qu’interactions (par exemple, commandes, factures, bons de réception, etc.) ou en tant qu’e-mails, appels téléphoniques et bordereaux d’envoi.

Pour plus d’informations, reportez-vous à [Enregistrer automatiquement les interactions avec les contacts](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Synchronisation des contacts avec les clients et autres
Pour synchroniser la fiche contact avec la fiche client, la fiche fournisseur et la fiche compte bancaire, vous devez sélectionner un code relation d’affaires pour les clients, les fournisseurs et les comptes bancaires. Par exemple, vous ne pouvez lier un contact avec un client existant que si vous avez sélectionné un code relation d’affaires pour les clients sur la page **Paramètres marketing**.

Pour plus d’informations, reportez-vous à [Procédure de synchronisation des contacts avec les clients, les fournisseurs et les comptes bancaires](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).  

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Affectation d’une souche de numéros aux contacts et aux opportunités
Vous pouvez configurer des souches de numéros pour les contacts et les opportunités. Si vous avez configuré une souche de numéros pour les contacts, lorsque vous créez un contact et que vous appuyez ensuite sur <kbd>Entrée</kbd> dans le champ N° de la fiche contact, l’application saisit automatiquement le numéro de contact suivant.

Pour plus d’informations sur les souches de numéros reportez-vous à [Création des souches de numéros](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Recherche des doublons lors de la création de contacts
Vous pouvez configurer l’application pour qu’elle recherche automatiquement les doublons chaque fois que vous créez une société contact ou vous pouvez choisir d’effectuer une recherche manuelle lorsque les contacts sont créés. Vous pouvez également configurer l’application pour qu’il mette automatiquement à jour les chaînes de recherche chaque fois que vous modifiez les données de contact ou que vous créez un contact. Vous pouvez choisir le pourcentage de chaînes communes, c’est-à-dire le pourcentage de chaînes qui doivent être identiques dans deux contacts pour que l’application les considère comme des doublons.

## <a name="see-also"></a>Voir aussi
[Gestion de contacts](marketing-contacts.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
