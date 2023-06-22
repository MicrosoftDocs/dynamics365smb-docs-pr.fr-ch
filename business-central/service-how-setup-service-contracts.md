---
title: Configurer des contrats de service
description: 'Découvrez comment configurer des contrats de service avec les conditions préalables requises, notamment des groupes de contrats de service, des modèles de contrat et des modèles de client.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="set-up-service-contracts" />Configurer des contrats de service
Avant de pouvoir utiliser les contrats, vous devez définir les éléments suivants : 

* **Groupes contrats de service** : regroupent les contrats de service liés, quelle que soit la nature de cette relation.
* **Groupes comptes contrat de service** : permettent de regrouper les comptes contrat de service pour les factures service créées pour les contrats de service. Vous affectez ces groupes aux contrats de service.  
* **Modèles contrat** : définissent les présentations des contrats incluant les détails de contrat de service les plus couramment utilisés. Vous pouvez créer des devis contrat de service à l’aide de modèles. Lorsque vous créez un devis contrat, les champs contiennent automatiquement la valeur des champs du modèle.
* **Modèles client** : permettent de créer des devis pour les contacts ou les clients potentiels qui ne sont pas enregistrés comme clients dans [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="to-set-up-a-service-contract-group" />Pour configurer un groupe de contrats de service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes de contrats de service**, puis sélectionnez le lien associé.  
2. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Activez la case à cocher **Remise sur cdes contrat seulement** si vous souhaitez que les remises contrat ou service ne soient valides que pour les commandes contrat de service, tels que de maintenance.  

## <a name="to-set-up-a-service-contract-account-group" />Pour configurer un groupe comptes contrats de service
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Groupes comptes contrat serv.**, puis sélectionnez le lien associé.  
2. Créez un groupe comptes contrat de service.   
3. Renseignez les champs **Code** et **Désignation**. Ces champs décrivent le groupe compte service.  
4. Renseignez le champ **Compte contrat non prépayé**, puis sélectionnez le numéro de compte général du compte non prépayé.  
5. Dans le champ **Compte contrat non prépayé**, sélectionnez le numéro de compte général du compte non prépayé.  

## <a name="to-set-up-a-contract-template" />Pour configurer un modèle de contrat
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles de contrats de service**, puis sélectionnez le lien associé.  
2. Créez un modèle contrat de service.  
3. Dans le champ **N°**, saisissez le numéro du modèle de contrat.  
  
     Si vous avez configuré une souche de numéros pour les modèles contrat sur la page **Paramètres Gestion des services**, vous pouvez sélectionner la touche <kbd>Entrée</kbd> pour que le programme saisisse le numéro modèle contrat suivant. Renseignez les autres champs, si nécessaire.  
  
4. Dans le raccourci **Facture**, renseignez les champs **Code gpe cptes contrat serv.**, **Période de facturation**, etc. Renseignez les autres champs, si nécessaire.  
5. Sélectionnez l’action **Remises service** pour ajouter des remises contrat.  

## <a name="to-set-up-a-customer-template" />Pour configurer un modèle client
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles client**, puis sélectionnez le lien associé.  
2. Créez une fiche modèle client.  
3. Sur le raccourci **Général**, tapez un code et une description pour le modèle client respectivement dans les champs **Code** et **Désignation**. 
4. Pour définir les critères de recherche, renseignez les autres champs tels que **Code pays/région**, **Code secteur** et **Code langue**.  
5. Renseignez les champs **Groupe compta. marché** et **Groupe compta. client**.  

## <a name="see-also" />Voir aussi
[Paramétrage de la gestion des services](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
