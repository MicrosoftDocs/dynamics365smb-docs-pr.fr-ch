---
title: Configurer des contrats de service | Microsoft Docs
description: Découvrez comment configurer des contrats de service.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 697de344a439bb0a91b1f74acc3d8b93d2f6d5d3
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/16/2019
ms.locfileid: "939191"
---
# <a name="set-up-service-contracts"></a>Configurer des contrats de service
Avant de pouvoir utiliser les contrats, vous devez définir les éléments suivants : 

* **Groupes contrats de service** : regroupent les contrats de service liés, quelle que soit la nature de cette relation.
* **Groupes comptes contrat de service** : permettent de regrouper les comptes contrat de service pour les factures service créées pour les contrats de service. Vous affectez ces groupes aux contrats de service.  
* **Modèles contrat** : définissent les présentations des contrats incluant les détails de contrat de service les plus couramment utilisés. Vous pouvez créer des devis contrat de service à l'aide de modèles. Lorsque vous créez un devis contrat, les champs contiennent automatiquement la valeur des champs du modèle.
* **Modèles client** : permettent de créer des devis pour les contacts ou les clients potentiels qui ne sont pas enregistrés comme clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Pour configurer un groupe de contrats de service  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes contrats de service**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Activez la case à cocher **Remise sur cdes contrat seulement** si vous souhaitez que les remises contrat ou service ne soient valides que pour les commandes contrat de service, tels que de maintenance.  

## <a name="to-set-up-a-service-contract-account-group"></a>Pour configurer un groupe comptes contrats de service  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes comptes contrat serv.**, puis sélectionnez le lien associé.  
2. Créez un groupe comptes contrat de service.   
3. Renseignez les champs **Code** et **Désignation**. Ces champs décrivent le groupe compte service.  
4. Renseignez le champ **Compte contrat non prépayé**, puis sélectionnez le numéro de compte général du compte non prépayé.  
5. Dans le champ **Compte contrat non prépayé**, sélectionnez le numéro de compte général du compte non prépayé.  

## <a name="to-set-up-a-contract-template"></a>Pour configurer un modèle de contrat  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Contrat de service - Modèles**, puis sélectionnez le lien associé.  
2. Créez un modèle contrat de service.  
3. Dans le champ **N°**, saisissez le numéro du modèle de contrat.  
  
     Si vous avez configuré une souche de numéros pour les modèles contrat sur la page **Paramètres Gestion des services**, vous pouvez appuyer sur la touche Entrée pour que le programme saisisse le numéro modèle contrat suivant. Renseignez les autres champs, si nécessaire.  
  
4. Dans le raccourci **Facture**, renseignez les champs **Code gpe cptes contrat serv.**, **Période de facturation**, etc. Renseignez les autres champs, si nécessaire.  
5. Sélectionnez l'action **Remises service** pour ajouter des remises contrat.  

## <a name="to-set-up-a-customer-template"></a>Pour configurer un modèle client  
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Modèles client**, puis sélectionnez le lien associé.  
2. Créez une fiche modèle client.  
3. Sur le raccourci **Général**, tapez un code et une description pour le modèle client respectivement dans les champs **Code** et **Désignation**. 
4. Pour définir les critères de recherche, renseignez les autres champs tels que **Code pays/région**, **Code secteur** et **Code langue**.  
5. Renseignez les champs **Groupe compta. marché** et **Groupe compta. client**.  

## <a name="see-also"></a>Voir aussi
[Paramétrage de la gestion des services](service-setup-service.md)