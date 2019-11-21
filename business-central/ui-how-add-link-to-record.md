---
title: Ajouter des pièces jointes, des liens et des notes sur des enregistrements | Microsoft Docs
description: Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu'une fiche client ou un document.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649803"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Gérer les pièces jointes, les liens et les notes sur les fiches et les documents

Dans le Récapitulatif de la plupart des fiches et des documents, vous pouvez joindre des fichiers, ajouter des liens et rédiger des notes. Pour les liens et les notes, vous pouvez également le faire sur la page de liste en sélectionnant d’abord la ligne associée.

Pour afficher ou modifier l’un de ces types d’informations jointes, vous devez d’abord ouvrir l'onglet **Pièces jointes** dans le Récapitulatif. Le nombre situé derrière le titre de l'onglet indique le nombre de fichiers, liens ou notes attachés existants pour la fiche ou le document.

Les pièces jointes, les liens et les notes restent attachés au fur et à mesure du traitement de la fiche ou du document dans d'autres états, par exemple d'une commande client en cours à une facture client enregistrée. Notez cependant qu'aucun type de pièce jointe n'est sorti du système, par exemple lors de l'impression ou de l'enregistrement dans un fichier.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Pour joindre un fichier à une facture achat
Vous pouvez joindre tout type de fichier contenant du texte, des images ou des vidéos à une fiche ou à un document. Ceci est utile, par exemple, lorsque vous souhaitez stocker la facture d’un fournisseur sous forme de fichier PDF sur la facture achat correspondante dans [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Les fichiers joints à la fonction Documents entrants ne sont pas inclus dans l'onglet **Pièces jointes**. Pour plus d'informations, voir [Documents entrants](across-income-documents.md).

La procédure suivante se base sur une commande vente. Les étapes sont similaires pour tous les autres documents et fiches pris en charge.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.
2. Ouvrez les commandes ventes auxquelles vous souhaitez joindre un fichier.
3. Dans le Récapitulatif, ouvrez l'onglet **Pièces jointes**.
4. Choisissez la valeur associée au champ **Documents**, telle que « 0 ».
5. Sur la page **Documents joints**, dans le champ **Pièce jointe**, choisissez le bouton **Sélectionner un fichier**.
5. Sélectionnez un fichier à n'importe quel emplacement, puis choisissez le bouton **Ouvrir**.

Le fichier est désormais joint à la facture achat.

## <a name="to-add-a-link-from-an-item-card"></a>Pour ajouter un lien à partir d'une fiche article
Vous pouvez ajouter un lien à partir d'une fiche ou d'un document à n’importe quelle URL ou n’importe quel chemin d'accès. Ceci est utile, par exemple, lorsque vous souhaitez lier une fiche article au catalogue d'articles du fournisseur.

La procédure suivante se base sur une fiche article. Les étapes sont similaires pour toutes les autres fiches et tous les documents pris en charge.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Articles**, puis sélectionnez le lien associé.
2. Sélectionnez l'article à partir duquel vous souhaitez ajouter un lien, puis choisissez l'onglet **Pièces jointes** dans le Récapitulatif.
3. Dans la section **Liens**, choisissez l'icône **+**.
4. Entrez le lien dans le champ **Adresse du lien**.

    Le lien doit être une URL Internet ou intranet valide.

5. Dans le champ **Description**, entrez les informations sur le lien.  
6. Cliquez sur le bouton **OK**.

Le lien est maintenant attaché à la fiche article.  

## <a name="to-write-a-note-on-a-sales-order"></a>Pour écrire une note sur une commande client
Vous pouvez écrire une note sur un document ou une ficher, par exemple pour communiquer des instructions spéciales aux autres utilisateurs du document ou de la fiche. Vous pouvez inclure des liens et des URL de fichier dans les notes.

> [!NOTE]
> Les notes sur l'onglet **Pièces jointes** ne sont pas liées à la fonctionnalité de notes internes, qui est principalement utilisée pour communiquer entre les utilisateurs de workflows. Pour plus d'informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md).

La procédure suivante se base sur une commande vente. Les étapes sont similaires pour tous les autres documents et fiches pris en charge.

1. Choisissez l'icône ![Ampoule qui ouvre la fonction de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez la commande vente pour laquelle vous souhaitez écrire une note, puis choisissez l'onglet **Pièces jointes** dans le Récapitulatif.
3. Dans la section **Notes**, choisissez l'icône **+**.
4. Dans le champ **Note**, écrivez n’importe quel texte, par exemple « Ceci est une commande urgente ».
5. Cliquez sur le bouton **OK**.

La note est maintenant jointe à la commande client.

## <a name="see-also"></a>Voir aussi  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Documents entrants](across-income-documents.md)  
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)  
