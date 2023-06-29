---
title: Importation de nombreuses images d’articles depuis un fichier ZIP
description: 'Pour importer plusieurs images d’article, nommez simplement vos fichiers image avec des noms correspondant à vos numéros d’article, comprimez-les en un fichier ZIP, puis utilisez la page Importer les images d’articles.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="import-multiple-item-pictures"></a><a name="import-multiple-item-pictures"></a>Importer plusieurs images d’article
Vous pouvez importer plusieurs images d’articles à la fois. Nommez simplement vos fichiers image avec des noms correspondant à vos numéros d’article, comprimez-les en un fichier zip, puis utilisez la page Importer les images d’articles pour gérer quelles images d’articles importer.

Tous les formats de fichier courants sont pris en charge.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Nommer les fichiers image avec les noms d’article et préparez le fichier ZIP
1. À l’emplacement de stockage de vos images d’article, nommez chaque fichier selon le numéro de l’article concerné. Par exemple :

    |N° article|Nom de fichier|
    |-|-|
    |1000|1000.bmp|
    |1 001|1001.bmp|
    |1002|1002.bmp|

2. Recueillez tous les fichiers dans un fichier ZIP. Par exemple, dans Windows Explorer, sélectionnez les fichiers, puis choisissez **Envoyer vers**, **Dossier comprimé (zip)**.     

## <a name="to-import-item-pictures"></a><a name="to-import-item-pictures"></a>Pour importer des images d’article
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Paramètres stock**, puis choisissez le lien associé.
2. Sélectionnez l’action **Importer des images d’article**.
3. Dans le champ **Sélectionner un fichier ZIP**, sélectionnez le dossier ZIP pertinent, puis sélectionnez le bouton **Ouvrir**.

    Une ligne pour chaque élément et image est créée sur la page **Importer des images d’article**.

    > [!NOTE]
    > Pour les fichiers article qui ont déjà une image, la case à cocher **Une image existe déjà** est sélectionnée. Si vous ne souhaitez pas remplacer les images existantes, décochez la case **Remplacer les images**. Si vous ne souhaitez pas remplacer les images existantes individuelles, supprimez les lignes en question.

3. Sélectionnez l’action **Importer des images**.

Le champ **Importer le statut** est mis à jour pour montrer si l’importation de l’image a été ignorée ou a bien eu lieu.       

## <a name="see-also"></a><a name="see-also"></a>Voir aussi
[Enregistrer de nouveaux articles](inventory-how-register-new-items.md)  
[Création des souches de numéros](ui-create-number-series.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Ventes](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
