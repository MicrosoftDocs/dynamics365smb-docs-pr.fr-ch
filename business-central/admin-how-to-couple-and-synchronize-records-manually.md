---
title: Couplage et synchronisation (contient une vidéo)
description: Synchroniser un mappage de table d’intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de la table Dynamics 365 Sales qui sont couplées.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.search.form: 6250
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2bc46e165018d29684b116f7aac3745c9d533c42
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517617"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Couplage et synchronisation des enregistrements entre Dataverse et Business Central

Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)] avec des enregistrements dans Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Le couplage d’enregistrements permet d’afficher les informations Dataverse depuis [!INCLUDE[prod_short](includes/prod_short.md)], et vice-versa. Le couplage vous permet également de synchroniser les données entre les enregistrements. Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.

> [!Note]
> Le couplage et la synchronisation des données sont disponibles seulement si votre administrateur système a créé une connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)]. Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l’action **Configurer le couplage**. Si l’action est disponible, les applications sont connectées.   

## <a name="video-example"></a>Exemple vidéo
Cette vidéo montre le couplage et la synchronisation de données dans le cadre d’une intégration avec [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Pour coupler un enregistrement  
1.  Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  

    Vous pouvez également ouvrir la page de liste et sélectionner l’enregistrement à coupler.  

2.  Choisissez l’action **Configurer le couplage**.  
3.  Renseignez les champs, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record"></a>Pour synchroniser un enregistrement unique  
1.  Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler. Par exemple, la fiche Client ou Contact.  
2.  Choisissez l’action **Synchroniser maintenant**.  
3.  Si un enregistrement peut être synchronisé dans une direction, sélectionnez l’option qui affiche la direction de la mise à jour des données, puis cliquez sur **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Pour synchroniser un enregistrement unique à partir de [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  Dans [!INCLUDE[crm_md](includes/crm_md.md)], ouvrez le formulaire pour l’enregistrement que vous souhaitez coupler. Par exemple, le formulaire Fiche Compte ou Fiche Contact.  
2.  Choisissez l’action **[!INCLUDE[prod_short](includes/prod_short.md)]** dans le ruban pour ouvrir et coupler l’enregistrement automatiquement.

> [!Note]
> Vous pouvez synchroniser automatiquement un enregistrement unique depuis [!INCLUDE[crm_md](includes/crm_md.md)] seulement si l’option **Synch. uniquement les enregistrements couplés** est désactivée et si la direction de synchronisation est définie sur Bidirectionnelle ou À partir de la table d’intégration sur la page **Mappage de table d’intégration** pour l’enregistrement. Pour en savoir plus, consultez [Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Pour coupler plusieurs enregistrements à l’aide du couplage par correspondance

Vous pouvez spécifier les données à synchroniser pour une entité, telle qu’un client ou un contact, en couplant des enregistrements par correspondance. Vous pouvez affiner les correspondances en rendant la recherche sensible à la casse et en attribuant une priorité à chaque correspondance. Si aucune correspondance n’est trouvée, vous pouvez également spécifier que vous souhaitez créer l’entité dans Dataverse. Pour plus d’informations, consultez [Personnaliser le couplage par correspondance](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que Clients ou Contacts.
2. Choisissez l’action **Couplage par correspondance**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Pour synchroniser plusieurs enregistrements  
1.  Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que Clients ou Contacts.  
2.  Sélectionnez l’enregistrement à synchroniser, puis l’action **Synchroniser maintenant**.  
3.  Si des enregistrements peuvent être synchronisés dans une direction, sélectionnez l’option qui affiche la direction, puis cliquez sur **OK**.  

## <a name="uncoupling-records"></a>Découplage des enregistrements
Vous pouvez découpler un ou plusieurs enregistrements des pages de liste ou sur la page **Erreurs de synchronisation de données couplées** en choisissant une ou plusieurs lignes et en choisissant **Supprimer le couplage**. Vous pouvez également supprimer tous les couplages pour un ou plusieurs mappages de table sur la page **Mappages de table d’intégration**.

## <a name="see-also"></a>Voir aussi  
[Utiliser Dynamics 365 Sales depuis Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]