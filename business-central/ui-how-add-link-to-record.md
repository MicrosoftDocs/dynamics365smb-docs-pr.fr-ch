---
title: Procédure de liaison d'un enregistrement à des informations ou programmes externes | Microsoft Docs
description: Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu'une fiche client ou un document.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 781f43daf6482c7e29696dc7a03aa021550cde7d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629772"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a>Ajouter des liens à des sites Web, documents ou programmes sur des enregistrements
Sur un enregistrement spécifique, comme une fiche client, un document ou une commande vente, vous pouvez ajouter un lien à un document, site Web ou programme externe. Vous pouvez aussi sélectionner un lien qui ouvre un e-mail vierge adressé à un destinataire précis. La page Fiche de certains enregistrements comme les fiches client ou fournisseur, dispose d'un champ **Page d'accueil** dans lequel vous pouvez entrer une adresse Internet (URL). Pour insérer d'autres liens, vous pouvez utiliser la méthode décrite dans cet article.  

> [!IMPORTANT]
> Actuellement, cette capacité est disponible uniquement dans les déploiements locaux [!INCLUDE [prodshort](includes/prodshort.md)] avec le client Dynamics NAV Windows hérité.  

Un autre exemple est lorsque vous recevez des factures imprimées de fournisseurs. Vous pouvez les numériser et les enregistrer au format .pdf sur un site SharePoint. Ensuite, vous pouvez créer un lien d'une facture achat dans [!INCLUDE[d365fin_md](includes/d365fin_md.md)] vers la facture correspondante sur SharePoint. Vous pouvez aussi créer un lien depuis une fiche article vers la page correspondante du catalogue en ligne de votre fournisseur.

## <a name="to-add-a-link-on-a-record"></a>Pour ajouter un lien sur un enregistrement   

1.  Ouvrez l'enregistrement auquel vous voulez ajouter le lien, par exemple une fiche client ou une commande vente. Pour associer le lien à une ligne spécifique, par exemple une ligne feuille, sélectionnez la ligne.  

2.  Choisissez l'action **Liens** pour ouvrir les pages **Liens** qui affichent tous les liens actuels qui sont ajoutés à l'enregistrement.

3. Pour ajouter un nouveau lien, choisissez **+nouveau**.

4.  Dans le champ **Adresse du lien**, entrez

    -   Pour créer un lien vers un fichier sur votre ordinateur ou réseau, entrez le chemin d'accès complet et le nom du fichier, par exemple **C:\Mes documents\invoice1.doc**.
    -   Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.
    -   Pour créer un lien vers un programme, entrez une chaîne spécifique pour ouvrir le programme. Par exemple, pour ouvrir OneNote avec une page spécifique, entrez **onenote:///C:\Mes documents/test.one**. Ou, pour ouvrir Outlook avec un e-mail vierge à destination d'un alias spécifique, entrez **mailto:testalias** .  

5.  Dans le champ **Désignation**, entrez les informations sur le lien.  

6.  Cliquez sur le bouton **Enregistrer**.  

## <a name="to-delete-a-link-from-a-record"></a>Pour supprimer un lien dans un enregistrement  

Pour supprimer un lien, sur la page **Liens**, vous pouvez sélectionner **…**, puis **Supprimer**.

Si vous supprimez un enregistrement, par exemple, une ligne commande vente, une commande vente ou une fiche client, tous les liens contenus dans l'enregistrement sont supprimés. En revanche, si vous supprimez des enregistrements à l'aide d'un traitement par lots, par exemple, le traitement par lots **Supprimer cdes vente facturées**, les liens sont conservés dans la base de données. Pour supprimer les liens de la base de données, exécutez le codeunit **Supprimer les liens enregistrement orphelins**. Pour cela, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les liens enregistrement orphelins**, puis sélectionnez le lien associé.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Voir aussi  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
