---
title: Utilisation de Business Central avec Outlook | Microsoft Docs
description: Ce service bénéficie d'une intégration complète à Office 365, ce qui vous permet de gérer tous vos interactions et messages d'affaires avec les clients et les fournisseurs directement dans Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 11/22/2019
ms.author: edupont
ms.openlocfilehash: 1e45b7cb19df3c057485451a95ae1633804fa865
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879155"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Utilisation de Business Central en tant que boîte de réception professionnelle dans Outlook

[!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet désormais de gérer les interactions commerciales avec vos clients et fournisseurs, directement dans Microsoft Outlook. Avec le complément Outlook de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez afficher des informations financières associées à des clients et des fournisseurs, ainsi que créer et envoyer des documents financiers, comme des devis et des factures.  

## <a name="getting-the-add-in"></a>Obtention du complément
Il pouvez aisément démarrer avec le module complémentaire [!INCLUDE[d365fin](includes/d365fin_md.md)] for Outlook. Dans le guide de configuration assistée **Configurer votre boîte de réception professionnelle dans Outlook**, vous pouvez configurer la connexion pour vous-même ou pour votre organisation si votre organisation utilise Office 365. Spécifiez simplement votre nom d'utilisateur et mot de passe Office 365, si vous êtes invité(e), et dites-nous si vous souhaitez recevoir un exemple de message électronique. Le complément [!INCLUDE[d365fin](includes/d365fin_md.md)] est alors automatiquement ajouté à votre Outlook. Pour plus d'informations, voir [Configuration minimale requise pour Outlook](product-requirements.md#outlook).  

Ensuite, lorsque vous ouvrez Outlook, vous voyez un message électronique dans *Admin Dynamics 365 Business Central*. Les nouveaux modules complémentaires sont ajoutés au ruban Outlook, et dans le navigateur, les modules complémentaires [!INCLUDE[prodshort](includes/prodshort.md)] apparaissent au-dessus ou au dessous du corps du message. Les modules complémentaires sont mis à jour régulièrement, et vous êtes informé qu'une nouvelle version est prête dans Outlook.  

> [!TIP]
> Si vous utilisez le nouvel Outlook sur le Web, les compléments [!INCLUDE [prodshort](includes/prodshort.md)] peuvent être cachés sous **Plus d'actions**. Si vous utilisez souvent le complément, vous pouvez l'épingler pour qu'il soit toujours immédiatement visible. Pour plus d'informations, voir [Utilisation des compléments dans Outlook sur le Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Si vous travaillez avec plus d'une entreprise [!INCLUDE [prodshort](includes/prodshort.md)], vous pouvez facilement basculer d'une entreprise à l'autre dans Outlook. Dans la barre d'actions du complément, choisissez **Plus d'actions** pour afficher l'option permettant de passer d'une entreprise à l'autre.  

<!--TEMP-->
> [!NOTE]
> Le passage d'une entreprise à l'autre nécessite la 2e vague de publication 2019 de [!INCLUDE [prodshort](includes/prodshort.md)] ou ultérieure, comme annoncé dans le [plan de publication](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Certaines sociétés utilisant Office 365 n'autorisent pas leurs utilisateurs à déployer des compléments. Ainsi vous devez vous assurer que vous disposez d'un abonnement Office 365 comprenant la messagerie et qui vous permet de déployer des compléments. Si vous souhaitez tout de même essayer le complément, vous pouvez [essayer gratuitement Office 365](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Utilisation du complément Panorama des contacts
Imaginons que vous receviez un e-mail d'un client souhaitant obtenir un devis pour certains articles. Directement dans Outlook, vous pouvez ouvrir le complément [!INCLUDE[d365fin](includes/d365fin_md.md)], qui identifie l'expéditeur comme un client, et ouvre la fiche client de sa société. À partir de ce tableau de bord, vous pouvez afficher des informations générales relatives au client, ainsi que rechercher davantage de détails sur des documents spécifiques. Vous pouvez également effectuer des recherches approfondies dans l'historique des ventes du client. S'il s'agit d'un nouveau contact, vous pouvez le créer en tant que tel dans [!INCLUDE[d365fin](includes/d365fin_md.md)] sans quitter Outlook.  

Dans le complément, vous pouvez créer un devis et l'envoyer à ce client sans quitter Outlook. Toutes les informations dont vous avez besoin pour envoyer le devis sont disponibles dans votre boîte de réception professionnelle dans Outlook.  
Une fois les données saisies, vous pouvez valider le devis. Vous pouvez ensuite l'envoyer par e-mail. [!INCLUDE[d365fin](includes/d365fin_md.md)] génère un fichier .PDF avec le devis et le joint au message électronique que vous rédigez dans le complément.  

De même, si vous recevez un e-mail d'un fournisseur, vous pouvez utiliser le complément pour travailler avec les fournisseurs et les factures achat.  

Il arrive parfois que vous souhaitiez visualiser davantage de champs que ceux qui s'affichent dans le complément, par exemple si vous souhaitez renseigner des lignes dans une facture. Afin de vous bénéficier d'un espace de travail plus important, vous pouvez ouvrir le complément sur une page distincte. Il s'agit toujours d'Outlook, mais vous disposez de davantage d'espace. Au fur et à mesure que vous saisissez des données pour le document dans l'affichage contextuel, les modifications sont automatiquement enregistrées. Lorsque vous avez terminé de saisir les données pour le document, vous pouvez cliquer sur le bouton **OK**. Sélectionner le cadre du complément dans Outlook actualise automatiquement le document avec les modifications que vous avez effectuées dans l'affichage contextuel.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Création de factures à partir de vos rendez-vous de réunion
Certaines sociétés enregistrent tous les rendez-vous facturables dans le calendrier Outlook. Avec [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez créer la facture du client directement à partir de l'article calendrier : ouvrez le rendez-vous, puis vous pouvez ouvrir le complément [!INCLUDE[d365fin](includes/d365fin_md.md)], rechercher des informations existantes ou créer une facture ou un autre document vente directement ici.  

## <a name="doing-quick-document-lookup"></a>Recherche rapide de document
Le complément Liens de document de [!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet d'accéder rapidement aux documents mentionnés dans les e-mails. Le complément est disponible pour un e-mail si un numéro de document est identifié dans le corps du message. Ouvrir le complément vous permet d'accéder rapidement à ce document.  

Par exemple, si vous recevez un e-mail qui mentionne le texte *S-QUO100*, [!INCLUDE[d365fin](includes/d365fin_md.md)] l'identifie comme un devis et vous pouvez donc ouvrir ce document dans Outlook. Dans Outlook, cliquez sur le bouton **Liens de document** situé juste au-dessus du corps du message. Dans Outlook Web App, sélectionnez le texte *S-QUO1001* dans le corps du message.  

Dans le complément Liens de document, vous pouvez modifier le document et effectuer des opérations sur celui-ci, comme dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Ajout de compléments manuellement
Dans certains cas, les compléments ne sont pas ajoutés automatiquement dans Outlook. Même si vous (ou l'un de vos collègues) avez exécuté le guide de configuration assistée pour le compte de la société, [!INCLUDE[d365fin](includes/d365fin_md.md)] ne s'affiche pas forcément dans Outlook. Si vous rencontrez ce problème, vous pouvez ajouter le complément [!INCLUDE[d365fin](includes/d365fin_md.md)] manuellement.  

Premièrement, vous devez vérifier que vous avez accès aux compléments dans votre compte Office 365. Ouvrez simplement votre Outlook dans un navigateur, ouvrez un message, sélectionnez **Plus d'actions** (...) en haut du message, puis en bas de la liste, choisissez **Obtenir des compléments** . Cela ouvre la page **Compléments pour Outlook**, sur laquelle vous pouvez activer [!INCLUDE[prodshort](includes/prodshort.md)] pour votre Outlook. Ensuite, lorsque vous revenez dans Outlook, [!INCLUDE[prodshort](includes/prodshort.md)] devrait être disponible.  

De même dans le client de bureau Outlook, vous pouvez vérifier si [!INCLUDE[d365fin](includes/d365fin_md.md)] est répertorié sur la page **Obtenir des compléments**.  

Dans les deux cas, si [!INCLUDE[d365fin](includes/d365fin_md.md)] n'est toujours pas disponible, vous devez vous procurer les fichiers de manifeste macro complémentaire. Pour plus d'informations, contactez votre administrateur Office 365.

## <a name="using-other-email-accounts"></a>Utilisation d'autres comptes de messagerie

Les compléments sont conçus pour être utilisés avec Office 365. Si vous utilisez [!INCLUDE [prodshort](includes/prodshort.md)] sur site, votre administrateur saura si vous pouvez utiliser les compléments [!INCLUDE [prodshort](includes/prodshort.md)] dans Outlook. Pour plus d'informations, voir [Quelle adresse e-mail puis-je utiliser avec [!INCLUDE[prodshort](includes/prodshort.md)] ?](across-faq.md#what-email-address-can-i-use-with-) et [Fonctionnalités nécessitant des circonstances spécifiques](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).  

## <a name="see-also"></a>Voir aussi

[Mise en route](product-get-started.md)  
[Obtention de Business Central sur mon périphérique mobile](install-mobile-app.md)  
[Envoyer des documents par e-mail](ui-how-send-documents-email.md)  
[Finances](finance.md)  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Configuration minimale requise pour Outlook](product-requirements.md#outlook)  
[Utilisation des compléments dans Outlook sur le Web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
