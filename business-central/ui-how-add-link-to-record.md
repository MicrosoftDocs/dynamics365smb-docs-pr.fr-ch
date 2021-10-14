---
title: Ajouter des pièces jointes, des liens et des notes sur des enregistrements
description: Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu’une fiche client ou un document.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 76829c832bfde71d46b2fa2a942aa68db9f5701a
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588795"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Gérer les pièces jointes, les liens et les notes sur les fiches et les documents

Dans le Récapitulatif de la plupart des fiches et des documents, vous pouvez joindre des fichiers, ajouter des liens et rédiger des notes. Pour les liens et les notes, vous pouvez également le faire sur la page de liste en sélectionnant d’abord la ligne associée.

Pour afficher ou modifier l’un de ces types d’informations jointes, vous devez d’abord ouvrir l’onglet **Pièces jointes** dans le Récapitulatif. Le nombre situé derrière le titre de l’onglet indique le nombre de fichiers, liens ou notes attachés existants pour la fiche ou le document.

Les pièces jointes, les liens et les notes restent attachés au fur et à mesure du traitement de la fiche ou du document dans d’autres états, par exemple d’une commande client en cours à une facture client enregistrée. Cependant, aucun type de document joint n’est sorti du système, par exemple lors de l’impression ou de l’enregistrement dans un fichier.

> [!NOTE]
> Lorsque vous expédiez et facturez partiellement une commande vente ou achat, le document joint ne sera annexé qu’à la facture finale de cette commande. De même, lorsque vous facturez à l’aide de la fonction Reports, le document joint est annexé aux écritures comptables pour le document, mais pas pour les écritures report.
>
> Si vous supprimez une commande avant qu’elle ne soit facturée, la pièce jointe est également supprimée. Lorsque vous facturez des commandes achat à l’aide de l’action Obtenir des lignes de réception à partir d’une facture achat, la pièce jointe sur les commandes achat n’est pas ajoutée à la facture achat.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Pour joindre un fichier à une facture achat
Vous pouvez joindre tout type de fichier contenant du texte, des images ou des vidéos à une fiche ou à un document. Ceci est utile, par exemple, lorsque vous souhaitez stocker la facture d’un fournisseur sous forme de fichier PDF sur la facture achat correspondante dans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Les fichiers joints à la fonction Documents entrants ne sont pas inclus dans l’onglet **Pièces jointes**. Pour plus d’informations, voir [Documents entrants](across-income-documents.md).

La procédure suivante se base sur une facture achat. Les étapes sont similaires pour tous les autres documents et fiches pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.
2. Ouvrez les commandes ventes auxquelles vous souhaitez joindre un fichier.
3. Dans le Récapitulatif, ouvrez l’onglet **Pièces jointes**.
4. Choisissez la valeur associée au champ **Documents**, telle que « 0 ».
5. Sur la page **Documents joints**, dans le champ **Pièce jointe**, choisissez l’action **Sélectionner un fichier**.
5. Sélectionnez un fichier à n’importe quel emplacement, puis choisissez le bouton **Ouvrir**.

Le fichier est désormais joint à la facture achat.

## <a name="to-view-an-attached-file"></a>Pour afficher un fichier joint
1. Dans le Récapitulatif, ouvrez l’onglet **Pièces jointes**.
2. Choisissez la valeur associée au champ **Documents**, telle que « 1 ».
3. Sur la page **Documents joints**, sélectionnez l’action **Aperçu**.
4. Ouvrez le fichier téléchargé.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Pour enregistrer un document en tant que pièce jointe PDF
Chaque fois que vous devez enregistrer un document en tant que fichier, vous pouvez utiliser l’action **Joindre en tant que PDF** pour capturer le contenu actuel du document sous forme de fichier PDF joint au récapitulatif du document. Cela est utile, par exemple, lorsque des documents suivent plusieurs étapes d’un processus, comme un processus de vente ou un flux de travail approbation, et que vous souhaitez vous référer à une impression de l’étape précédente.

La procédure suivante se base sur une commande vente. Les étapes sont similaires pour tous les autres documents pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez une commande vente, puis l’action **Joindre en tant que PDF**.

Un fichier PDF avec le contenu actuel de la commande vente est ajouté à l’onglet **Pièces jointes** du récapitulatif.

## <a name="to-add-a-link-from-an-item-card"></a>Pour ajouter un lien à partir d’une fiche article
Vous pouvez ajouter un lien à partir d’une fiche ou d’un document à n’importe quelle URL. Ceci est utile, par exemple, lorsque vous souhaitez lier une fiche article au catalogue d’articles du fournisseur.

La procédure suivante se base sur une fiche article. Les étapes sont similaires pour toutes les autres fiches et tous les documents pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l’article à partir duquel vous souhaitez ajouter un lien, puis choisissez l’onglet **Pièces jointes** dans le Récapitulatif.
3. Dans la section **Liens**, choisissez l’icône **+**.
4. Entrez le lien dans le champ **Adresse du lien**.

    Le lien doit être une URL Internet ou intranet valide.

5. Dans le champ **Description**, entrez les informations sur le lien.  
6. Cliquez sur le bouton **OK**.

Le lien est maintenant attaché à la fiche article.  

## <a name="to-write-a-note-on-a-sales-order"></a>Pour écrire une note sur une commande client
Vous pouvez écrire une note sur un document ou une ficher, par exemple pour communiquer des instructions spéciales aux autres utilisateurs du document ou de la fiche. Vous pouvez inclure des liens et des URL de fichier dans les notes.

> [!NOTE]
> Les notes sur l’onglet **Pièces jointes** ne sont pas liées à la fonctionnalité de notes internes, qui est principalement utilisée pour communiquer entre les utilisateurs de workflows. Pour plus d’informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md).

La procédure suivante se base sur une commande vente. Les étapes sont similaires pour tous les autres documents et fiches pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Commandes vente**, puis sélectionnez le lien associé.
2. Sélectionnez la commande vente pour laquelle vous souhaitez écrire une note, puis choisissez l’onglet **Pièces jointes** dans le Récapitulatif.
3. Dans la section **Notes**, choisissez l’icône **+**.
4. Dans le champ **Note**, écrivez n’importe quel texte, par exemple « Ceci est une commande urgente ».
5. Cliquez sur le bouton **OK**.

La note est maintenant jointe à la commande client.

## <a name="see-also"></a>Voir aussi  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Documents entrants](across-income-documents.md)  
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
