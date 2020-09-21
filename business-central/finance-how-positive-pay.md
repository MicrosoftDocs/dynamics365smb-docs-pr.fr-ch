---
title: Exporter des fichiers Positive Pay| Microsoft Docs
description: Vous pouvez vous assurer que la banque efface uniquement les chèques et les montants validés en exportant un fichier Positive Pay contenant des informations de paiement et fournisseur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: be71a8edc556708f88d00b088f49b52e2fd5ee45
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778933"
---
# <a name="export-a-positive-pay-file"></a>Exporter un fichier Positive Pay
Pour vous assurer que votre banque efface uniquement les chèques et les montants validés, vous pouvez exporter un fichier Positive Pay contenant des informations fournisseur, un numéro de chèque, un montant de paiement que vous envoyez à la banque pour référence lorsque vous traitez les paiements.

[!INCLUDE[d365fin](includes/d365fin_md.md)] est préconfiguré pour prendre en charge les fichiers Positive Pay de la Bank of America et de la City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Pour configurer une banque pour Positive Pay
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.
2. Ouvrez la fiche de la banque pour laquelle vous souhaitez utiliser Positive Pay.
3. Dans le champ **Code exportation Positive Pay**, entrez POSPAYBANK.
4. Fermez la page.

## <a name="to-export-a-positive-pay-file"></a>Pour exporter un fichier Positive Pay
1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Comptes bancaires**, puis sélectionnez le lien associé.
2. Sélectionnez le compte bancaire pour lequel vous voulez exporter un fichier Positive Pay.
3. Choisissez l'option **Exportation Positive Pay**.

    La page **Exportation Positive Pay** s'ouvre et affiche les paiements qui ont été effectués pour le compte bancaire depuis la dernière date de téléchargement, comme indiqué dans les champs **Date dernier téléchargement** et **Heure dernier téléchargement**.
4. Dans le champ **Date limite téléchargement**, spécifiez une date avant laquelle les paiements ne sont pas inclus dans le fichier exporté.
5. Sélectionnez l'option **Exporter**.
6. Sur la page **Exporter fichier**, choisissez le bouton **Enregistrer**, puis enregistrez le fichier à l'emplacement approprié.
7. Téléchargez le fichier sur votre site bancaire électronique.
8. Notez ou copiez le numéro de confirmation qui s'affiche lorsque le téléchargement du fichier est terminé.

Pour afficher les enregistrements Positive Pay exportés

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.
2. Sélectionnez le compte bancaire pour lequel vous voulez afficher l'enregistrement d'exportation de Positive Pay.
3. Choisissez l'option **Écritures Positive Pay**.

    Sur la page **Écritures Positive Pay**, vous pouvez afficher tous les enregistrements d'exportation de Positive Pay pour le compte bancaire.
4. Dans le champ **Numéro de confirmation**, entrez, pour chaque enregistrement d'exportation, le numéro de confirmation que vous recevez lorsque le téléchargement du fichier vers la banque est terminé.
5. Pour afficher les lignes de paiement associées, choisissez l'option **Détails écriture Positive Pay**.

Pour réexporter les fichiers Positive Pay

1. Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Compte bancaire**, puis sélectionnez le lien associé.
2. Sélectionnez le compte bancaire pour lequel vous voulez réeexporter les fichiers Positive Pay.
3. Choisissez l'option **Écritures Positive Pay**.
4. Sélectionnez la ligne du fichier d'exportation Positive Pay à réexporter.
5. Sur la page **Écritures Positive Pay**, choisissez l'option **Réexporter Positive Pay dans un fichier**.

## <a name="see-also"></a>Voir aussi
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utilisation de feuilles comptabilité](ui-work-general-journals.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
