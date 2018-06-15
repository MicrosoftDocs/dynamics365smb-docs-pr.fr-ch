---
title: "Résoudre les problèmes liés à l'inscription en self-service | Microsoft Docs"
description: "En savoir plus sur les motifs classiques pour lesquels vous ne pouvez pas terminer l'inscription à Business Central, et des manières de les résoudre."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f1d432ae73696e9e81bdc96c939051b676008e54
ms.contentlocale: fr-ch
ms.lasthandoff: 05/28/2018

---
# <a name="troubleshooting-self-service-sign-up"></a>Dépannage de l'inscription en self-service
L'inscription à [!INCLUDE[d365fin](includes/d365fin_md.md)] est simple et peut être effectuée très rapidement. Vous pouvez créer un compte gratuit même si vous représentez une société existante. Cet article aborde les problèmes que vous pouvez rencontrer lors de l'inscription.

## <a name="what-email-address-can-i-use-with-business-central"></a>Quelle adresse e-mail puis-je utiliser avec Business Central ?
[!INCLUDE[d365fin](includes/d365fin_md.md)] exige que vous utilisiez une adresse e-mail professionnelle ou scolaire pour votre inscription. [!INCLUDE[d365fin](includes/d365fin_md.md)] ne prend pas en charge les adresses e-mail fournies par les services de messagerie publics ni les opérateurs de télécommunications. Cela comprend outlook.com, hotmail.com, gmail.com, et d'autres.

Si vous essayez d'effectuer votre inscription à l'aide d'une adresse e-mail personnelle, vous recevez un message vous demandant d'utiliser une adresse professionnelle ou scolaire.

## <a name="troubleshooting"></a>Incident
Dans de nombreux cas, vous pouvez effectuer votre inscription à [!INCLUDE[d365fin](includes/d365fin_md.md)] en suivant simplement le processus d'inscription. Toutefois, il existe plusieurs raisons pour lesquelles vous pouvez ne pas être en mesure de terminer l'inscription en self-service. La table ci-dessous récapitule certaines des raisons les plus courantes pour lesquelles vous pouvez ne pas être en mesure de terminer l'inscription en self-service, ainsi que des solutions pour remédier au problème.

| Symptôme/Message d'erreur | Cause et solution de contournement |
| --- | --- |
| Pour les adresses e-mail Office 365 qui ne sont pas enregistrés dans un pays pris en charge, vous recevez un message semblable au suivant lors de votre inscription :<br /><br />**L'inscription n'a pas fonctionné. Nous ne prenons pas encore en charge votre pays ou région.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] prend en charge actuellement uniquement les comptes e-mails Office 365 qui sont enregistrés sur un nombre limité de marchés. Pour plus d'informations, voir [Disponibilité régionale](#regional-availability). |
| Les adresse e-mail personnelles telles que nancy@gmail.com ne sont pas prises en charge. Vous recevez un message semblable au suivant lors de votre inscription :<br /><br />**Vous avez saisi une adresse e-mail personnelle. Veuillez saisir votre adresse e-mail professionnelle de sorte que nous puissions stocker les données de votre société en toute sécurité.**<br> Ou <br> **Il semble que votre adresse soit une adresse personnelle. Saisissez votre adresse professionnelle de sorte que vous puissions vous mettre en relation avec d'autres utilisateurs de votre société. Et vous ne inquiétez pas. Nous ne partagerons votre adresse avec personne.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ne prend pas en charge les adresses e-mail fournies par les services de messagerie publics ni les opérateurs de télécommunications. Pour terminer l'inscription, essayez de nouveau en utilisant une adresse e-mail affectée par votre entreprise ou établissement scolaire. Si vous ne parvenez toujours pas à vous inscrire et que vous souhaitez effectuer un processus de configuration plus avancé, vous pouvez prendre un nouvel abonnement gratuit Office 365 et utiliser cette adresse e-mail pour vous inscrire. |
| Adresses e-mail .gov ou .mil. Vous recevez un message semblable au suivant lors de votre inscription :<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] n'est pas disponible : [!INCLUDE[d365fin](includes/d365fin_md.md)] n'est pas disponible pour les utilisateurs ayant des adresses e-mail .gov ou .mil. pour le moment. Utilisez une autre adresse e-mail professionnelle ou vérifiez ultérieurement.** <br>Ou <br>**Nous ne sommes pas en mesure de terminer votre inscription. Il semble que [!INCLUDE[d365fin](includes/d365fin_md.md)] ne soit pas disponible à l'heure actuelle pour votre entreprise ou établissement scolaire.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ne prend pas en charge les adresses e-mail .gov ou .mil. |
| L'inscription en self-service n'est pas activée. Vous recevez un message semblable au suivant lors de votre inscription :<br /><br />**Nous ne sommes pas en mesure de terminer votre inscription. Votre service informatique a désactivé l'inscription à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour terminer votre inscription, contactez votre service informatique.** <br>Ou <br> **Il semble que votre adresse soit une adresse personnelle. Saisissez votre adresse professionnelle de sorte que vous puissions vous mettre en relation avec d'autres utilisateurs de votre société. Et vous ne inquiétez pas. Nous ne partagerons votre adresse avec personne.** |L'administrateur informatique de votre entreprise a désactivé l'inscription en self-service à [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pour terminer votre inscription, contactez votre administrateur informatique et demandez-lui de suivre les instructions sur la page ci-dessous afin d'autoriser les utilisateurs existants à s'inscrire à [!INCLUDE[d365fin](includes/d365fin_md.md)] et d'autoriser les nouveaux utilisateurs à rejoindre votre abonnement existant. Vous pouvez également rencontrer ce problème si vous avez effectué votre inscription à Office 365 par l'intermédiaire d'un partenaire. |
| L'adresse e-mail n'est pas un ID Office 365. Vous recevez un message semblable au suivant lors de votre inscription :<br /><br />**Nous ne vous trouvons pas sur contoso.com. Utilisez-vous un autre identifiant dans votre entreprise ou établissement scolaire ? Essayez d'effectuer votre inscription avec celui-ci. Si cela ne fonctionne pas, contactez votre service informatique.** |Votre entreprise utilise pour l'inscription à Office 365 et à d'autres services Microsoft des identifiants différents de votre adresse e-mail. Par exemple, votre adresse e-mail peut être Nancy.Smith@contoso.com alors que votre identifiant est nancys@contoso.com. Pour terminer votre inscription, utilisez l'identifiant que votre entreprise vous a affecté pour l'inscription à Office 365 ou à d'autres services Microsoft. Si vous ne connaissez pas cet identifiant, contactez votre administrateur informatique. Si vous ne parvenez toujours pas à vous inscrire et que vous pouvez effectuer un processus de configuration plus avancé, vous pouvez prendre un nouvel abonnement gratuit Office 365 et utiliser cette adresse e-mail pour vous inscrire. |
| Si votre compte Office 365 est enregistré dans un pays pris en charge, et que vous vous inscrivez à [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis un autre pays, vous recevrez un message comme le suivant pendant l'inscription :<br /><br />**L'inscription n'a pas fonctionné. Nous ne prenons pas encore en charge votre pays ou région.**| L'abonnement Office 365 de votre organisation est enregistré dans un pays spécifique dans le portail Administration Office 365. L'expérience d'inscription à [!INCLUDE[d365fin](includes/d365fin_md.md)] utilise la langue et les paramètres régionaux que votre navigateur actuel utilise, et par conséquent, vous pouvez recevoir le message d'erreur même si vous être dans un pays pris en charge. Demander à votre administrateur informatique de vérifier le pays spécifié dans le profil de l'organisation dans le [Portail d'administration Office 365](https://portal.office.com/adminportal/home#/companyprofile). Vous pouvez être amené à utiliser un autre compte pour [!INCLUDE[d365fin](includes/d365fin_md.md)].|

## <a name="regional-availability"></a>Disponibilité régionale
[!INCLUDE[d365fin](includes/d365fin_md.md)] est actuellement disponible sur les marchés suivants :

| Europe | Amérique du Nord |
| --- | --- |
| Autriche | Canada |
| Belgique | États-Unis |
| Danemark | |
| Allemagne | |
| Finlande | |
| France | |
| Italie | |
| Pays-Bas | |
| Espagne | |
| Suède | |
| Suisse | |
| Anglais (Royaume-Uni) | |

## <a name="see-also"></a>Voir aussi
[Bienvenue dans [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

