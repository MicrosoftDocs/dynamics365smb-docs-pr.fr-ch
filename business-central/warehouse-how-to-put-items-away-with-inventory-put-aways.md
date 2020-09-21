---
title: Comment ranger des articles avec le rangement stock | Microsoft Docs
description: Lorsque votre magasin est configuré pour exiger un traitement des rangements, mais qu'il ne l'est pas pour un traitement des réceptions, vous utilisez le document **Rangement stock** pour enregistrer et valider les informations de rangement et de réception pour vos documents origine. Le document origine entrant peut être une commande achat, un retour vente, un enlogement transfert ou un ordre de fabrication dont la production est prête à être rangée.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 37be68e0235fa326344bc0f024b4584eb0289f9f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779351"
---
# <a name="put-items-away-with-inventory-put-aways"></a>Ranger des articles avec le rangement stock
Lorsque votre magasin est configuré pour exiger un traitement des rangements, mais qu'il ne l'est pas pour un traitement des réceptions, vous utilisez le document **Rangement stock** pour enregistrer et valider les informations de rangement et de réception pour vos documents origine. Le document origine entrant peut être une commande achat, un retour vente, un ordre de transfert ou un ordre d'assemblage/de fabrication entrant dont la production est prête à être rangée.  

Vous pouvez créer un rangement stock de trois manières :  

- Créez le rangement en deux étapes en créant d'abord une demande entrepôt à partir du document origine, qui signale à l'entrepôt que le document origine est prêt pour rangement. Le rangement stock peut ensuite être créé à partir de la page **Rangement stock** sur la base du document origine.  
- Créez le rangement stock directement à partir du document origine proprement dit.  
- Créez des rangements stock pour plusieurs documents simultanément en utilisant un traitement par lots.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Pour demander un rangement stock en lançant le document d'origine
Pour les commandes achat, de retours vente et d'ordres de transfert enlogement, vous créez la demande entrepôt en lançant l'ordre. Ce qui suit décrit comment faire cela pour une commande achat.  

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes achat**, puis sélectionnez le lien associé.
2. Sélectionnez la commande achat que vous voulez lancer, puis sélectionnez l'action **Lancer**.  

    Pour les ordres de fabrication, vous créez la demande entrepôt en créant une demande d'enlogement à partir de l'ordre de fabrication lancé.  
3.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **O.F. lancés**, puis sélectionnez le lien associé.  
4. Choisissez l'action **Créer demande d'enlogement**.  

> [!NOTE]  
>  Vous pouvez également créer la demande enlogement entrepôt en sélectionnant le champ **Créer demande d'enlogement** lors de l'actualisation de l'ordre de fabrication. Pour plus d'informations, voir [Actualiser ou replanifier des ordres de fabrication](production-how-to-replan-refresh-production-orders.md).  

Lorsque la demande entrepôt est créée, un employé affecté dans l'entrepôt aux rangements des articles peut voir que le document origine est prêt et peut créer un document rangement stock.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Pour créer un rangement stock sur la base du document origine
Maintenant que la demande est créée, le magasinier peut créer un nouveau rangement stock sur la base du document origine lancé.   
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Rangement stock**, puis sélectionnez le lien associé.  
2. Sélectionnez l'action **Nouveau**.  
3. Dans le champ **Document origine**, sélectionnez le type de document origine que vous rangez.  
4. Dans le champ **N° origine**, sélectionnez le document origine.  
5. Sinon, choisissez l'action **Extraire document origine** pour sélectionner le document à partir de la liste des documents origine entrants prêts pour le rangement dans le magasin.  
6. Cliquez sur le bouton **OK** pour renseigner les lignes rangement en fonction du document origine sélectionné.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Pour créer un rangement stock à partir du document origine  
1.  Dans le document origine, qui peut être une commande achat, un retour vente, un ordre enlogement transfert ou un ordre de fabrication, choisissez l'action **Créer prélèv./rangement stock**.  
2. Activez la case à cocher **Créer prélèv./rangement stock**.
3. Cliquez sur le bouton **OK**. Un nouveau rangement stock est créé.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Pour créer plusieurs rangements stock avec un traitement par lots  
1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Créer prélèv./rangement stock**, puis sélectionnez le lien associé.  
2.  Sur le raccourci **Demande entrepôt** de la page demande, utilisez les champs **Document origine** et **N° origine** pour opérer un filtrage sur certains types de documents ou des plages de numéros de document.  
3.  Sur le raccourci **Options**, cochez la case **Créer rangement stock**.
4.  Cliquez sur le bouton **OK**. Les rangements stock spécifiés sont créés.

## <a name="to-record-the-inventory-put-away"></a>Pour enregistrer les rangements stock  
1. Ouvrez un document rangement déjà créé en en sélectionnant un sur la page **Rangements stock**.  
2. Dans le champ **Code emplacement** sur les lignes rangement, l'emplacement où les articles doivent être rangés est proposé sur la base d'un emplacement par défaut de l'article. Vous pouvez modifier l'emplacement sur la page, si nécessaire.  
3. Exécutez le rangement et saisissez les informations pour la quantité effectivement rangée dans le champ **Quantité à traiter**.

    S'il s'avère nécessaire de placer les articles d'une ligne dans plusieurs emplacements, notamment parce que l'emplacement indiqué est plein, alors utilisez la fonction **Eclater ligne** sur le raccourci **Lignes**. Pour plus d'informations sur l'éclatement des lignes, voir [Répartir des lignes activité entrepôt](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Une fois le rangement exécuté, choisissez l'action **Valider**.  

Le processus de validation valide la réception, ou la production pour les ordres de fabrication, des lignes document origine qui ont été rangées et, si le magasin utilise des emplacements, la validation crée également des écritures entrepôt pour valider les modifications apportées aux quantités emplacement.

## <a name="see-also"></a>Voir aussi  
[Gestion d'entrepôt](warehouse-manage-warehouse.md)  
[STOCKS ET EN-COURS](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion des assemblages](assembly-assemble-items.md)    
[Détails de conception : gestion d'entrepôt](design-details-warehouse-management.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
