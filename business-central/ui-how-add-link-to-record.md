---
title: "Procédure de liaison d'un enregistrement à des informations ou programmes externes | Microsoft Docs"
description: "Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu'une fiche client ou un document."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2e70ad534a28cf5062e9e54a2dfbd3af6afaa39
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Ajout de liens à des sites Web, documents ou programmes sur des enregistrements
Sur un enregistrement spécifique, comme une fiche client, un document ou une commande vente, vous pouvez ajouter un lien à un document, site Web ou programme externe. Vous pouvez aussi sélectionner un lien qui ouvre un e-mail vierge adressé à un destinataire précis. La page Fiche de certains enregistrements comme les fiches client ou fournisseur, dispose d'un champ **Page d'accueil** dans lequel vous pouvez entrer une adresse Internet (URL). Pour insérer d'autres liens, vous pouvez utiliser la méthode décrite dans cet article.

Un autre exemple est lorsque vous recevez des factures imprimées de fournisseurs. Vous pouvez les numériser et les enregistrer au format .pdf sur un site SharePoint. Ensuite, vous pouvez créer un lien d'une facture achat dans [!INCLUDE[d365fin_md](includes/d365fin_md.md)] vers la facture correspondante sur SharePoint. Vous pouvez aussi créer un lien depuis une fiche article vers la page correspondante du catalogue en ligne de votre fournisseur.

## <a name="to-add-a-link-on-a-record"></a>Pour ajouter un lien sur un enregistrement   

1.  Ouvrez l'enregistrement auquel vous voulez ajouter le lien, par exemple une fiche client ou une commande vente. Pour associer le lien à une ligne spécifique, par exemple une ligne feuille, sélectionnez la ligne.  

2.  Choisissez l'action **Liens** pour ouvrir les fenêtres **Liens** qui affichent tous les liens actuels qui sont ajoutés à l'enregistrement.

3. Pour ajouter un nouveau lien, choisissez **+nouveau**.

4.  Dans le champ **Adresse du lien**, entrez

    -   Pour créer un lien vers un fichier sur votre ordinateur ou réseau, entrez le chemin d'accès complet et le nom du fichier, par exemple **C:My Documentsinvoice1.doc**.
    -   Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.
    -   Pour créer un lien vers un site Web, entrez l'adresse Internet (URL), par exemple **www.microsoft.com**.
    -   Pour créer un lien vers un programme, entrez une chaîne spécifique pour ouvrir le programme. Par exemple, pour ouvrir OneNote avec une page spécifique, entrez **onenote:///C:My Documentstest.one**. Ou, pour ouvrir Outlook avec un e-mail vierge à destination d'un alias spécifique, entrez **mailto:testalias** .  

5.  Dans le champ **Désignation**, entrez les informations sur le lien.  

6.  Cliquez sur le bouton **Enregistrer**.  

## <a name="to-delete-a-link-from-a-record"></a>Pour supprimer un lien dans un enregistrement  

Pour supprimer un lien, dans la fenêtre **Liens**, vous pouvez sélectionner **…**, puis **Supprimer**.

Si vous supprimez un enregistrement, par exemple, une ligne commande vente, une commande vente ou une fiche client, tous les liens contenus dans l'enregistrement sont supprimés. En revanche, si vous supprimez des enregistrements à l'aide d'un traitement par lots, par exemple, le traitement par lots **Supprimer cdes vente facturées**, les liens sont conservés dans la base de données. Pour supprimer les liens de la base de données, exécutez le codeunit **Supprimer les liens enregistrement orphelins**. Pour cela, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer les liens enregistrement orphelins**, puis sélectionnez le lien associé.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  In the **Data Deletion** window, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Voir aussi  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

