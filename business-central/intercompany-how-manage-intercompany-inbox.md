---
title: Gérer la boîte de réception et la boîte d’envoi intersociétés
description: Les transactions intersociétés que vous recevez de vos partenaires intersociétés sont stockées dans la boîte de réception Intersociétés où vous pouvez les traiter manuellement ou automatiquement.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.service: dynamics-365-business-central
---
# Gérer la boîte de réception et la boîte d’envoi intersociétés

Toutes les transactions intersociétés que vous recevez par voie électronique de vos partenaires intersociétés sont stockées dans la page **Boîte de réception intersociétés**. Pour savoir comment traiter les transactions intersociétés entrantes, accédez à [Traiter les transactions intersociétés entrantes](#process-incoming-intercompany-transactions). Toutes les transactions intersociétés que vous envoyez à vos partenaires intersociétés sont stockées dans la page **Boîte d’envoi intersociétés**. Pour savoir comment traiter les transactions intersociétés sortantes, accédez à [Pour traiter les transactions intersociétés sortantes](#to-process-outgoing-intercompany-transactions).

Cependant, selon votre configuration inter-sociétés, certaines transactions sont gérées automatiquement. Vous pouvez configurer la société source et les sociétés partenaires pour qu’elles créent automatiquement des documents et des journaux correspondant aux transactions que les partenaires valident via la feuille comptabilité intersociétés. Pour en savoir plus sur l’utilisation des feuilles intersociétés, accédez à [Remplir et valider une feuille intersociétés](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## Organisation de la boîte de réception  

Les champs de filtre, situés en haut de la page de la boîte de réception, permettent de déterminer les transactions qui apparaissent sur la page. Par exemple, si vous souhaitez uniquement consulter les transactions créées par un partenaire précis, utilisez les filtres **Source de la transaction** et **Code Partenaire Intersociétés**.  

### Source de la transaction  

Vous pouvez utiliser une transaction différemment selon qu’elle a été :  

* créée par votre partenaire Intersociétés  
* rejetée par votre partenaire Intersociétés qui vous l’a renvoyée  

Utilisez le champ **Afficher la source de la transaction** pour filtrer la page **Transactions boîte de réception Intersociétés**, afin qu’elle n’affiche qu’un seul des types de transaction suivants. Vous pouvez également filtrer la fenêtre en fonction du partenaire Intersociétés ou de la valeur du champ **Action de la ligne**.  

#### Créé(e) par votre partenaire Intersociétés  

 Lorsque vous recevez une nouvelle transaction créée par votre partenaire, vous pouvez soit :

* Accepter la transaction  
* Rejeter la transaction (et la renvoyer à votre partenaire)  
* Annuler la transaction (et la supprimer sans la renvoyer à votre partenaire)  

#### Renvoyé par le partenaire Intersociétés  

Si votre partenaire intersociété a rejeté la transaction, vous devez l’annuler dans la boîte de réception, puis créer des lignes correction, ou inverser la feuille ou le document dans votre société.  

## Recréation d’écritures boîte de réception  

Si vous acceptez une transaction de votre boîte de réception, mais que vous avez supprimé la feuille ou le document au lieu de le valider, vous pouvez recréer l’écriture boîte de réception et l’accepter à nouveau.  

## Obtenir une présentation des transactions intersociétés pour une période  

Vous pouvez afficher un aperçu des transactions intersociétés envoyées et reçues sur une période donnée. L’état **Transactions intersociétés** répertorie toutes les écritures comptables intersociétés, client et fournisseur.

> [!NOTE]  
> Si les partenaires intersociétés se trouvent dans la même base de données, les partenaires peuvent accepter automatiquement les transactions. Ils accèdent directement aux pages **Transactions de boîte de réception intersociétés traitées** et **Transactions de boîte d’envoi intersociétés traitées**. Pour en savoir plus sur l’acceptation automatique des transactions, accédez à [Accepter automatiquement les transactions des partenaires intersociétés](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Pour le partenaire de synchronisation, sur la page **Configuration intersociétés**, activez le bouton à bascule **Envoyer auto. des transactions**.
> * Pour les sociétés partenaires, sur la page **Partenaire intersociété**, activez le bouton à bascule **Accepter auto. les transactions**.  

## Importer des transactions intersociétés à partir d’un fichier

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Si l’un de vos partenaires intersociétés ne figure pas dans la même base de données que votre société, vous pouvez recevoir de lui des transactions intersociétés dans un fichier .xml. Vous devez ensuite importer ces transactions dans votre boîte de réception.  

1. Enregistrez le fichier à l’emplacement spécifié dans le champ **Détails boîte de réception intersociétés** lorsque vous configurez l’intersociété.  
2. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transactions boîte de réception Intersociétés**, puis sélectionnez le lien associé.
3. Sur la page **Transactions boîte de réception Intersociétés**, choisissez l’action **Importer le fichier de transaction**.  
4. sur la page qui apparaît, sélectionnez le fichier .xml qui contient les transactions, puis cliquez sur le bouton **Ouvrir**.  

Les transactions sont importées dans la boîte de réception. Vous pouvez alors les traiter.

## Traiter les transactions intersociétés entrantes  

Lorsque vos partenaires intersociétés vous envoient des transactions intersociétés, celles-ci arrivent dans votre boîte de réception intersociété. Vous devez évaluer chaque transaction qu’elle contient et prendre les mesures nécessaires.  

1. Sélectionnez l’![icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"),  entrez **Transactions boîte de réception Intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Transactions boîte de réception Intersociétés**, sélectionnez une ligne, puis choisissez une action **Accepter** pour traiter la ligne.
3. Sur la page **Terminer action boîte récep IC**, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Cliquez sur le bouton **OK**.  

Pour les lignes que vous acceptez, des lignes document ou feuille sont créées dans votre société. Ouvrez chaque document ou feuille, apportez les modifications nécessaires, puis validez-les.  

Les lignes que vous rejetez et renvoyez à votre partenaire sont placées dans votre boîte d’envoi intersociétés, où vous pouvez les envoyer à votre partenaire.

Pour les lignes rejetées et renvoyées par un partenaire, vous devez à présent valider une correction de la transaction initialement validée dans votre société.

## Pour traiter les transactions intersociétés sortantes  

Lorsque vous validez une feuille ou un document intersociété, ou que vous envoyez une confirmation de commande intersociété, les transactions sont envoyées à votre boîte d’envoi intersociété. Pour les envoyer à vos partenaires intersociétés, vous devez ouvrir la boîte d’envoi et les traiter.  

1. Sélectionnez ![l’icône en forme d’Ampoule qui ouvre la fenêtre de recherche](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Transactions boîte d’envoi Intersociétés**, puis sélectionnez le lien associé.  
2. Sur la page **Transactions boîte d’envoi Intersociétés**, sélectionnez une ligne, puis choisissez une action **Retourner à la boîte de réception** pour traiter la ligne.

Utilisez l’action **Envoyer au partenaire Intersociétés** pour envoyer des lignes à la boîte de réception du partenaire concerné.

Utilisez l’action **Retourner à la boîte de réception** pour déplacer les lignes vers votre boîte de réception où vous pouvez les accepter pour créer des documents ou des lignes feuille de votre société.  

Si vous utilisez l’action **Annuler**, vous devez à présent valider une correction de la transaction initialement validée dans votre société.  

## Recréer des transactions boîte de réception intersociétés  

Vous pouvez recréer une transaction dans la boîte de réception ou d’envoi. Par exemple, si vous avez accepté une transaction dans votre boîte de réception, mais que vous avez supprimé la feuille ou le document au lieu de le valider, vous pouvez recréer l’écriture boîte de réception et l’accepter à nouveau.  

La procédure suivante décrit comment recréer des transactions de boîte de réception. Le processus est le même pour les boîtes d’envoi.

1. Sélectionnez ![l’icône en forme d’ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transactions boîte de réception IC gérées**, puis choisissez le lien associé.  
2. Sur la page **Transactions boîte de réception IC gérées**, sélectionnez la ligne contenant la transaction à recréer dans la boîte de réception, puis choisissez l’action **Recréer la transaction boîte de réception**.  

## Voir aussi

[Gestion des transactions intersociétés](intercompany-manage.md)  
[Finances](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des feuilles comptabilité](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
