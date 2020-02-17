---
title: Valider un numéro d'identification intracommunautaire | Microsoft Docs
description: Valider un numéro d'identification intracommunautaire
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: f4d5023acba2e0cc5600b3f6675c3dcc325489d7
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992270"
---
# <a name="validate-a-vat-registration-number"></a>Valider un numéro d'identification intracommunautaire

## <a name="to-verify-vat-registration-numbers"></a>Pour vérifier les numéros d'identification TVA
Il est important que les numéros d'identification TVA des clients, fournisseurs et contacts soient valides. Par exemple, les sociétés modifient parfois leur statut d'assujettissement à la TVA, et dans certains pays, les autorités fiscales peuvent vous demander de fournir des états, tels que l'état Liste des ventes UE, qui répertorient les numéros d'identification TVA à utiliser lorsque vous faites des affaires.

La Commission européenne fournit le service VIES de validation des numéros TVA sur son site Web, qui est public et gratuit. [!INCLUDE[d365fin](includes/d365fin_md.md)] vous permet de supprimer cette étape et d'utiliser le service VIES pour valider et suivre les numéros de TVA des clients, fournisseurs et contacts directement à partir des fiches client, fournisseur et contact. Le service de [!INCLUDE[d365fin](includes/d365fin_md.md)] s'appelle **Services validation N° id. intracomm. Union européenne**. Il est disponible sur la page **Connexions au service**, et vous pouvez commencer à l'utiliser immédiatement. La connexion au service est gratuite, et l'inscription n'est pas obligatoire.

Afin d'activer **Services validation N° id. intracomm. Union européenne**, ouvrez l'entrée sur la page **Connexion au service**. Le champ **Point de terminaison de service** doit être déjà rempli. Sinon, vous pouvez utiliser l'action **Définir le point de terminaison par défaut**. Puis définissez le champ **Activé**.

> [!Note]
> Pour activer les Services validation N° id. intracomm. Union européenne, vous devez disposer des autorisations de l'administrateur.

Lorsque vous utilisez la connexion à notre service, nous enregistrons un historique des numéros de TVA et des vérifications pour chaque client, fournisseur ou contact dans le **Journal identif. intracomm** pour faciliter le suivi. Le journal est spécifique à chaque client. Par exemple, le journal est utile pour prouver que vous avez vérifié que le numéro de TVA actuel est correct. Lorsque vous vérifiez un numéro de TVA, la colonne **Identificateur de demande** du journal indique que vous avez effectué des actions.

Vous pouvez afficher le journal d'identification TVA sur les fiches client, fournisseur ou contact, sous le raccourci **Facturation**, en cliquant sur le bouton de recherche dans le champ **N° identif. intracomm.**  

Notre service peut aussi vous faire gagner du temps lorsque vous créez un client ou un fournisseur. Si vous connaissez le numéro TVA du client, vous pouvez le saisir dans le champ **N° identif. intracomm.** des fiches client ou fournisseur, et nous complèterons le nom du client pour vous. Certains pays fournissent également les adresses de société dans un format structuré. Dans ces pays, nous compléterons aussi l'adresse.  

Voici quelques points à noter concernant le service VIES de validation de numéros de TVA :

* Le service utilise le protocole http, ce qui signifie que les données transférées via le service ne sont pas cryptées.  
* Vous pouvez rencontrer des temps d'arrêt pour ce service dont Microsoft n'est pas responsable. Le service fait partie d'un vaste réseau de l'UE de registres de TVA nationaux.

## <a name="see-also"></a>Voir aussi  
[Configuration de la TVA](finance-setup-vat.md)  
[Configuration de la TVA sur encaissement](finance-setup-unrealized-vat.md)      
[Déclarer la TVA à une autorité fiscale](finance-how-report-vat.md)  
[Utiliser la TVA sur les ventes et les achats](finance-work-with-vat.md)  
[Fonctionnalités locales dans Business Central](about-localization.md)
