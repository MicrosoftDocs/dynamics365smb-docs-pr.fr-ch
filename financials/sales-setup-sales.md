---
title: "Aperçu des tâches de configuration des processus de vente | Microsoft Docs"
description: "Décrit les tâches permettant de configurer des règles et des valeurs pour définir vos stratégies et vos processus de vente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a16201e48cc823e687c9941082d34044d9612a29
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-sales"></a>Définition des ventes.
Avant de pouvoir gérer les processus de vente, vous devez configurer les règles et valeurs qui définissent les stratégies de vente de la société.

Vous devez définir la configuration générale, notamment les documents vente requis et le mode de validation des valeurs correspondantes. Celle-ci a généralement lieu une seule fois au cours de la phase initiale de l'implémentation.

Une série de tâches distincte en relation avec l'enregistrement de nouveaux clients consiste à enregistrer les prix spéciaux ou les accords de remise établis avec chaque client.

La configuration des ventes en relation avec les finances, comme les modes de règlement et les devises, sont traitées dans la section Paramètres financiers. Pour plus d'informations, reportez-vous à [Configuration de Finance](finance-setup-finance.md).

| Pour | Voir |
| --- | --- |
| Créer une fiche client pour chaque client auquel vous vendez des éléments. |[Procédure : enregistrer de nouveaux clients](sales-how-register-new-customers.md) |
| Autoriser les clients à payer via Paypal en sélectionnant le logo Paypal sur les documents vente. |[Procédure : activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md) |
| Entrer les différentes remises et prix spéciaux accordés aux clients en fonction de l'article, des quantités et/ou de la date. |[Procédure : enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md) |
| Configurer les vendeurs de sorte à pouvoir les affecter aux contacts client ou à évaluer les performances des vendeurs et vous en servir comme base pour calculer la commission et les bonus. |[Procédure : configurer des vendeurs](sales-how-setup-salespeople.md) |
| Spécifier pour différents clients ou pour tous les clients le moyen par lequel les documents vente sont envoyés par défaut lorsque vous sélectionnez l'action **Valider et envoyer**. |[Procédure : configurer des profils d'envoi de documents](sales-how-setup-document-send-profiles.md) |
| Configurer votre e-mail de sorte qu'il contienne un résumé des informations du document vente qui est envoyé. |[Procédure : envoyer des documents par e-mail](ui-how-send-documents-email.md). |
|Utilisez un service Web UE pour vérifier le numéro d'immatriculation de TVA d'un client.|[Procédure : Vérifier les numéros d'identification intracomm.](sales-how-to-verify-vat-registration-numbers.md)|
|Entrer des informations sur les différents transporteurs utilisés, notamment un lien vers les prestations de traçabilité des colis.|[Procédure : configurer des transporteurs](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

