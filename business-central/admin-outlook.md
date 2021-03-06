---
title: Utilisation de Business Central avec Outlook | Microsoft Docs
description: Ce service bénéficie d’une intégration complète à Microsoft 365, ce qui vous permet de gérer tous vos interactions et messages d’affaires avec les clients et les fournisseurs directement dans Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2c8746098081a8f0b961f6ab2efd11c491104acc
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115401"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Utilisation de Business Central en tant que boîte de réception professionnelle dans Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] vous permet désormais de gérer les interactions commerciales avec vos clients et fournisseurs, directement dans Microsoft Outlook. Avec le complément Outlook de [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez afficher des informations financières associées à des clients et des fournisseurs, ainsi que créer et envoyer des documents financiers, comme des devis et des factures.  

## <a name="getting-the-add-in"></a>Obtention du complément
Il pouvez aisément démarrer avec le module complémentaire [!INCLUDE[prod_short](includes/prod_short.md)] for Outlook. Dans le guide de configuration assistée **Configurer votre boîte de réception professionnelle** dans Outlook, vous pouvez configurer la connexion pour vous-même ou pour votre organisation si votre organisation utilise Microsoft 365. Spécifiez simplement votre nom d’utilisateur et mot de passe Microsoft 365, si vous êtes invité, et dites-nous si vous souhaitez recevoir un exemple de message électronique. Le complément [!INCLUDE[prod_short](includes/prod_short.md)] est alors automatiquement ajouté à votre Outlook. Pour plus d’informations, voir [Configuration minimale requise pour Outlook](product-requirements.md#outlook).  

Ensuite, lorsque vous ouvrez Outlook, vous voyez un message électronique dans *Admin Dynamics 365 Business Central*. Les nouveaux modules complémentaires sont ajoutés au ruban Outlook, et dans le navigateur, les modules complémentaires [!INCLUDE[prod_short](includes/prod_short.md)] apparaissent au-dessus ou au dessous du corps du message. Les modules complémentaires sont mis à jour régulièrement, et vous êtes informé qu’une nouvelle version est prête dans Outlook.  

> [!TIP]
> Si vous utilisez le nouvel Outlook sur le Web, les compléments [!INCLUDE[prod_short](includes/prod_short.md)] peuvent être cachés sous **Plus d’actions**. Si vous utilisez souvent le complément, vous pouvez l’épingler pour qu’il soit toujours immédiatement visible. Pour plus d’informations, voir [Utilisation des compléments dans Outlook sur le Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Si vous travaillez avec plus d’une entreprise [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez facilement basculer d’une entreprise à l’autre dans Outlook. Dans la barre d’actions du complément, choisissez **Plus d’actions** pour afficher l’option permettant de passer d’une entreprise à l’autre.  

<!--TEMP-->
> [!NOTE]
> Le passage d’une entreprise à l’autre nécessite la 2e vague de publication 2019 de [!INCLUDE[prod_short](includes/prod_short.md)] ou ultérieure, comme annoncé dans le [plan de publication](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Certaines sociétés utilisant Microsoft 365 n’autorisent pas leurs utilisateurs à déployer des compléments. Ainsi vous devez vous assurer que vous disposez d’un abonnement Microsoft 365 comprenant la messagerie et qui vous permet de déployer des compléments. Si vous souhaitez tout de même essayer le complément, vous pouvez [essayer gratuitement Microsoft 365](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Utilisation du complément Panorama des contacts
Imaginons que vous receviez un e-mail d’un client souhaitant obtenir un devis pour certains articles. Directement dans Outlook, vous pouvez ouvrir le complément [!INCLUDE[prod_short](includes/prod_short.md)], qui identifie l’expéditeur comme un client, et ouvre la fiche client de cette société. À partir de ce tableau de bord, vous pouvez afficher des informations générales relatives au client, ainsi que rechercher davantage de détails sur des documents spécifiques. Vous pouvez également effectuer des recherches approfondies dans l’historique des ventes du client. S’il s’agit d’un nouveau contact, vous pouvez le créer en tant que tel dans [!INCLUDE[prod_short](includes/prod_short.md)] sans quitter Outlook.  

Dans le complément, vous pouvez créer un devis et l’envoyer à ce client sans quitter Outlook. Toutes les informations dont vous avez besoin pour envoyer le devis sont disponibles dans votre boîte de réception professionnelle dans Outlook.  
Une fois les données saisies, vous pouvez valider le devis. Vous pouvez ensuite l’envoyer par e-mail. [!INCLUDE[prod_short](includes/prod_short.md)] génère un fichier .PDF avec le devis et le joint au message électronique que vous rédigez dans le complément.  

De même, si vous recevez un e-mail d’un fournisseur, vous pouvez utiliser le complément pour travailler avec les fournisseurs et les factures achat.  

Il arrive parfois que vous souhaitiez visualiser davantage de champs que ceux qui s’affichent dans le complément, par exemple si vous souhaitez renseigner des lignes dans une facture. Afin de vous bénéficier d’un espace de travail plus important, vous pouvez ouvrir le complément sur une page distincte. Il s’agit toujours d’Outlook, mais vous disposez de davantage d’espace. Au fur et à mesure que vous saisissez des données pour le document dans l’affichage contextuel, les modifications sont automatiquement enregistrées. Lorsque vous avez terminé de saisir les données pour le document, vous pouvez cliquer sur le bouton **OK**. Sélectionner le cadre du complément dans Outlook actualise automatiquement le document avec les modifications que vous avez effectuées dans l’affichage contextuel.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Création de factures à partir de vos rendez-vous de réunion
Certaines sociétés enregistrent tous les rendez-vous facturables dans le calendrier Outlook. Avec [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez créer la facture du client directement à partir de l’article calendrier : ouvrez le rendez-vous, puis vous pouvez ouvrir le complément [!INCLUDE[prod_short](includes/prod_short.md)], rechercher des informations existantes ou créer une facture ou un autre document vente directement ici.  

## <a name="doing-quick-document-lookup"></a>Recherche rapide de document
Le complément Liens de document de [!INCLUDE[prod_short](includes/prod_short.md)] vous permet d’accéder rapidement aux documents mentionnés dans les e-mails. Le complément est disponible pour un e-mail si un numéro de document est identifié dans le corps du message. Ouvrir le complément vous permet d’accéder rapidement à ce document.  

Par exemple, si vous recevez un e-mail qui mentionne le texte *S-QUO100*, [!INCLUDE[prod_short](includes/prod_short.md)] l’identifie comme un devis et vous pouvez donc ouvrir ce document dans Outlook. Dans Outlook, cliquez sur le bouton **Liens de document** situé juste au-dessus du corps du message. Dans Outlook Web App, sélectionnez le texte *S-QUO1001* dans le corps du message.  

Dans le complément Liens de document, vous pouvez modifier le document et effectuer des opérations sur celui-ci, comme dans [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="adding-the-add-ins-manually"></a>Ajout de compléments manuellement
Dans certains cas, les compléments ne sont pas ajoutés automatiquement dans Outlook. Même si vous (ou l’un de vos collègues) avez exécuté le guide de configuration assistée pour le compte de la société, [!INCLUDE[prod_short](includes/prod_short.md)] ne s’affiche pas forcément dans Outlook. Si vous rencontrez ce problème, vous pouvez ajouter le complément [!INCLUDE[prod_short](includes/prod_short.md)] manuellement.  

Premièrement, vous devez vérifier que vous avez accès au complément dans votre compte Microsoft 365. Ouvrez simplement votre Outlook dans un navigateur, ouvrez un message, sélectionnez **Plus d’actions** (...) en haut du message, puis en bas de la liste, choisissez **Obtenir des compléments** . Cela ouvre la page **Compléments pour Outlook**, sur laquelle vous pouvez activer [!INCLUDE[prod_short](includes/prod_short.md)] pour votre Outlook. Ensuite, lorsque vous revenez dans Outlook, [!INCLUDE[prod_short](includes/prod_short.md)] devrait être disponible.  

De même dans le client de bureau Outlook, vous pouvez vérifier si [!INCLUDE[prod_short](includes/prod_short.md)] est répertorié sur la page **Obtenir des compléments**.  

Dans les deux cas, si [!INCLUDE[prod_short](includes/prod_short.md)] n’est toujours pas disponible, vous devez vous procurer les fichiers de manifeste macro complémentaire. Pour plus d’informations, contactez l’administrateur Microsoft 365.

## <a name="using-other-email-accounts"></a>Utilisation d’autres comptes de messagerie

Les compléments sont conçus pour être utilisés avec Microsoft 365. Si vous utilisez [!INCLUDE[prod_short](includes/prod_short.md)] sur site, votre administrateur saura si vous pouvez utiliser les compléments [!INCLUDE[prod_short](includes/prod_short.md)] dans Outlook. Pour plus d’informations, consultez [Quelle adresse e-mail puis-je utiliser avec [!INCLUDE[prod_short](includes/prod_short.md)] ?](/dynamics365/business-central/across-faq#email), et l’article [Fonctionnalités nécessitant des circonstances spécifiques](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) et la section [Pourquoi le complément Outlook ne fonctionne-t-il pas pour mes utilisateurs ?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) dans le FAQ général du contenu d’administration.  

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Voir aussi

[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Obtention de Business Central sur mon périphérique mobile](install-mobile-app.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Configuration minimale requise pour Outlook](product-requirements.md#outlook)  
[Utilisation des compléments dans Outlook sur le Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]