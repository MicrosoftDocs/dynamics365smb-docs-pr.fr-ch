---
title: Gérer la boîte de réception et la boîte d’envoi intersociétés
description: Les transactions intersociétés que vous recevez de vos partenaires intersociétés sont stockées dans la boîte de réception Intersociétés où vous pouvez les traiter manuellement ou automatiquement.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: 600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d0f52d1debe40eb57ac0deb914d0e6bc32f0a5a1
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/01/2022
ms.locfileid: "8366390"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Gérer la boîte de réception et la boîte d’envoi intersociétés
Toutes les transactions intersociétés que vous recevez par voie électronique de vos partenaires intersociétés sont stockées dans la boîte de réception Intersociétés.  

## <a name="organizing-the-inbox"></a>Organisation de la boîte de réception  
 Les champs de filtre, situés en haut de la page de la boîte de réception, permettent de déterminer les transactions qui apparaissent sur la page. Par exemple, si vous souhaitez uniquement consulter les transactions créées par un partenaire précis, vous pouvez définir les filtres **Source de la transaction** et **Code Partenaire Intersociétés**.  

### <a name="transaction-source"></a>Source de la transaction  
Vous pouvez utiliser une transaction différemment selon qu’elle a été :  

- créée par votre partenaire Intersociétés  
- rejetée par votre partenaire Intersociétés qui vous l’a renvoyée  

Vous pouvez utiliser le champ **Afficher la source de la transaction** pour filtrer la page **Transactions boîte de réception Intersociétés**, afin qu’elle n’affiche qu’un seul des types de transaction suivants. (Vous pouvez également filtrer la fenêtre en fonction du partenaire Intersociétés ou de la valeur du champ **Action de la ligne**.)  

#### <a name="created-by-intercompany-partner"></a>créée par votre partenaire Intersociétés  
 Lorsque vous recevez une nouvelle transaction créée par votre partenaire, vous pouvez soit :

- Accepter la transaction  
- Rejeter la transaction (et la renvoyer à votre partenaire)  
- Annuler la transaction (et la supprimer sans la renvoyer à votre partenaire)  

#### <a name="returned-from-intercompany-partner"></a>Renvoyé par le partenaire Intersociétés  
 Si la transaction a été rejetée par votre partenaire Intersociétés, vous n’avez pas d’autre choix que d’annuler la transaction dans la boîte de réception. Vous devez créer des lignes de correction ou contrepasser la feuille ou le document de votre société.  

## <a name="recreating-inbox-entries"></a>Recréation d’écritures boîte de réception  
 Si vous acceptez une transaction de votre boîte de réception, mais que vous avez supprimé la feuille ou le document au lieu de le valider, vous pouvez recréer l’écriture boîte de réception et l’accepter à nouveau.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Affichage d’un aperçu des transactions intersociétés sur une période donnée  
 Vous pouvez afficher un aperçu des transactions intersociétés envoyées et reçues sur une période donnée. L’état **Transactions intersociétés** répertorie toutes les écritures comptables intersociétés, client et fournisseur.

 > [!NOTE]  
 > Si les partenaires intersociétés sont exprimés dans la même base de données, les transactions sont transférées sans recourir de fichier ou par e-mail. Voir le champ **Type transfert** sur la page **Partenaire Intersociétés**. <br /><br />
Dans ce cas, vous pouvez configurer le système pour qu’il ignore la boîte de réception et la boîte d’envoi en sélectionnant la case à cocher **Auto. Accepter les transactions** sur la page **Partenaire Intersociétés** et la case à cocher **Auto. Envoyer des transactions** sur la page **Paramétrage intersociétés** respectivement. Les transactions intersociétés entrantes ne peuvent être acceptées automatiquement que si le planificateur de tâches est activé. Pour plus d’informations, reportez-vous à la rubrique [Configuration de Business Central Server - Paramètres du planificateur de tâches](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## <a name="to-import-intercompany-transactions-from-a-file"></a>Pour importer des transactions intersociétés à partir d’un fichier  
Si l’un de vos partenaires intersociétés ne figure pas dans la même base de données que votre société, vous pouvez recevoir de lui des transactions intersociétés dans un fichier .xml. Vous devez ensuite importer ces transactions dans votre boîte de réception.  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Informations société**, puis choisissez le lien associé.
2. Enregistrez le fichier à l’emplacement spécifié dans le champ **Détails sur boîte récep Intersoc.** de la page **Informations société**.  
3. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transactions boîte de réception Intersociétés**, puis sélectionnez le lien associé.
4. Sur la page **Transactions boîte de réception Intersociétés**, choisissez l’action **Importer le fichier de transaction**.  
5. sur la page qui apparaît, sélectionnez le fichier .xml qui contient les transactions, puis cliquez sur le bouton **Ouvrir**.  

Les transactions sont importées dans la boîte de réception. Vous pouvez alors les traiter.

## <a name="to-process-incoming-intercompany-transactions"></a>Pour traiter les transactions intersociétés entrantes  
Lorsque vos partenaires intersociétés vous envoient des transactions intersociétés, celles-ci arrivent dans votre boîte de réception intersociété. Vous devez évaluer chaque transaction qu’elle contient et prendre les mesures nécessaires.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transactions boîte de réception Intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Transactions boîte de réception Intersociétés**, sélectionnez une ligne, puis choisissez une action **Accepter** pour traiter la ligne.
3. Sur la page **Terminer action boîte récep IC**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Choisissez le bouton **OK**.  

Pour les lignes que vous avez traitées avec l’action **Accepter**, des lignes document ou feuille sont créées dans votre société. Ouvrez chaque document ou feuille, apportez les modifications nécessaires, puis validez-les.  

Les lignes que vous avez traitées avec l’action **Renvoyer au partenaire** sont déplacées vers la boîte d’envoi d’où vous pouvez ensuite les envoyer à votre partenaire.

Pour les lignes que vous avez traitées avec l’action **Renvoyé par le partenaire**, vous devez à présent valider une correction de la transaction initialement validée dans votre société.

## <a name="to-process-outgoing-intercompany-transactions"></a>Pour traiter les transactions intersociétés sortantes  
Lorsque vous validez une feuille ou un document intersociété, ou que vous envoyez une confirmation de commande intersociété, les transactions sont envoyées à votre boîte d’envoi intersociété. Pour qu’elles soient envoyées à vos partenaires intersociétés, vous devez ouvrir la boîte d’envoi et les traiter.  

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transactions boîte d’envoi Intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Transactions boîte d’envoi Intersociétés**, sélectionnez une ligne, puis choisissez une action **Retourner à la boîte de réception** pour traiter la ligne.

Les lignes que vous avez traitées avec l’action **Envoyer au partenaire Intersociétés** sont transmises à la boîte de réception du partenaire concerné.

Les lignes que vous avez traitées avec l’action **Retourner à la boîte de réception** sont déplacées vers la boîte de réception où vous pouvez les accepter pour créer des documents ou des lignes feuille de votre société.  

Pour les lignes que vous avez traitées avec l’action **Annuler**, vous devez à présent valider une correction de la transaction initialement validée dans votre société.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Pour recréer des transactions boîte de réception intersociétés  
À l’occasion, vous pouvez recréer une transaction dans la boîte de réception ou d’envoi. Par exemple, si vous avez accepté une transaction dans votre boîte de réception, mais que vous avez supprimé la feuille ou le document au lieu de le valider, vous pouvez recréer l’écriture boîte de réception et l’accepter à nouveau.  

La procédure suivante décrit comment recréer des transactions de boîte de réception. Le processus est le même pour les boîtes d’envoi.

  1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transactions boîte de réception IC gérées**, puis choisissez le lien associé.  

  2.  Sur la page **Transactions boîte de réception IC gérées**, sélectionnez la ligne contenant la transaction à recréer dans la boîte de réception, puis choisissez l’action **Recréer la transaction boîte de réception**.  

## <a name="see-also"></a>Voir aussi
[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
