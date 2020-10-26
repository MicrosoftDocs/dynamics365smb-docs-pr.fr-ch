---
title: Aperçu des tâches de configuration des processus de vente | Microsoft Docs
description: Décrit les tâches permettant de configurer des règles et des valeurs pour définir vos stratégies et vos processus de vente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b7eb82e5fc3dc20449f3fc8352fbda4e80372a20
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910445"
---
# <a name="setting-up-sales"></a>Définition des ventes.
Avant de pouvoir gérer les processus de vente, vous devez configurer les règles et valeurs qui définissent les stratégies de vente de la société.

Vous devez définir la configuration générale, notamment les documents vente requis et le mode de validation des valeurs correspondantes. Celle-ci a généralement lieu une seule fois au cours de la phase initiale de l’implémentation.

Une série de tâches distincte en relation avec l’enregistrement de nouveaux clients consiste à enregistrer les prix spéciaux ou les accords de remise établis avec chaque client.

La configuration des ventes en relation avec les finances, comme les modes de règlement et les devises, sont traitées dans la section Paramètres financiers. Pour plus d’informations, reportez-vous à [Configuration de Finance](finance-setup-finance.md).

| Pour | Voir |
| --- | --- |
| Créer une fiche client pour chaque client auquel vous vendez des éléments. |[Enregistrer de nouveaux clients](sales-how-register-new-customers.md) |
| Autoriser les clients à payer via Paypal en sélectionnant le logo Paypal sur les documents vente. |[Activer les paiements client via Paypal](sales-how-enable-payment-service-extensions.md) |
| Entrer les différentes remises et prix spéciaux accordés aux clients en fonction de l’article, des quantités et/ou de la date. |[Enregistrement des prix de vente, des remises et des accords sur les paiements](sales-how-record-sales-price-discount-payment-agreements.md) |
| Configurer les vendeurs de sorte à pouvoir les affecter aux contacts client ou à évaluer les performances des vendeurs et vous en servir comme base pour calculer la commission et les bonus. |[Configurer des vendeurs](sales-how-setup-salespeople.md) |
| Spécifier pour différents clients ou pour tous les clients le moyen par lequel les documents vente sont envoyés par défaut lorsque vous sélectionnez l’action **Valider et envoyer** . |[Configurer des profils d’envoi de documents](sales-how-setup-document-send-profiles.md) |
| Configurer votre e-mail de sorte qu’il contienne un résumé des informations du document vente qui est envoyé. |[Envoyer des documents par e-mail](ui-how-send-documents-email.md). |
|Utilisez un service Web UE pour vérifier le numéro d’immatriculation de TVA d’un client.|[Vérifier les numéros d’identification TVA](finance-setup-vat.md)|
|Définissez les différents incoterms que vous proposez aux clients ou que vos fournisseurs vous proposent.|[Configurer des conditions de livraison](sales-how-set-up-shipment-methods.md)|
|Entrer des informations sur les différents transporteurs utilisés, notamment un lien vers les prestations de traçabilité des colis.|[Configurer des transporteurs](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Voir la formation associée sur [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)

## <a name="see-also"></a>Voir aussi
[Ventes](sales-manage-sales.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
