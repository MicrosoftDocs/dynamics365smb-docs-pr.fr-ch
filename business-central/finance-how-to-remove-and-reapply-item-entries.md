---
title: Supprimer et relettrer des écritures article
description: Vous pouvez visualiser et modifier manuellement certaines écritures lettrage article qui sont créées automatiquement lors des mouvements de stock.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '506, 521, 9125'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="remove-and-reapply-item-ledger-entries"></a>Supprimer et relettrer des écritures comptables article
Sur la page **Feuille lettrage**, vous pouvez visualiser et modifier manuellement certaines écritures lettrage article qui sont créées automatiquement lors des mouvements de stock.  

Lorsque vous validez une transaction où des articles entrent ou sortent du stock, un lettrage article est créé entre chaque entrée de stock et sortie du stock. Ces applications déterminent le flux des coûts de biens entrant dans le stock vers des coûts de biens sortant du stock. En raison du mode de calcul du coût unitaire, un lettrage article incorrect peut produire un coût moyen ou un coût unitaire erroné. Pour plus d’informations, voir Détails de conception : traçabilité.

Vous pouvez être amené à annuler un lettrage ou à relettrer des écritures comptables article dans les scénarios suivants :

- Vous avez oublié d’effectuer un lettrage fixe.
- Vous avez effectué un lettrage incorrect.
- Vous devez retourner un article sur lequel une vente a déjà été lettrée.

Si possible, utilisez un document pour relettrer une écriture comptable article. Par exemple, si vous devez procéder à un retour achat d’un article sur lequel une vente a déjà été lettrée, vous pouvez relettrer en créant et validant le document de retour achat à l’aide du lettrage correct dans le champ **Écr. article à lettrer** dans la ligne retour achat. Vous pouvez utiliser la fonction **Affichage de lignes document validées à contrepasser** ou **Copier à partir du document** dans le document de retour achat pour faciliter cette opération. Lorsque vous validez le document, l’écriture comptable article est automatiquement relettrée. Pour plus d’informations, reportez-vous à [Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md).

Si vous ne pouvez pas utiliser un document pour un relettrage, par exemple si vous devez corriger un lettrage fixe, utilisez la page **Feuille lettrage** pour corriger un lettrage.

> [!Warning]  
> Il est important de se rappeler les considérations suivantes lorsque vous travaillez sur la feuille lettrage :
    - Vous ne devez pas laisser des écritures lettrage non lettrées pendant de longues périodes, car d’autres utilisateurs ne peuvent pas traiter les articles jusqu’à ce que vous relettriez les écritures lettrage ou clôturiez la page **Feuille lettrage**. Les utilisateurs qui essaient d’exécuter des actions qui concernent une écriture lettrage manuellement délettrée reçoivent le message d’erreur suivant : « Il est impossible d’effectuer cette opération car les écritures de l’article XXX ne sont pas lettrées dans la feuille lettrage par l’utilisateur XXX. »
    - Vous devez relettrer uniquement les écritures comptables article en dehors des heures de travail afin d’éviter les conflits avec d’autres utilisateurs qui valident des transactions portant sur les mêmes articles.
    - Lorsque vous fermez la feuille lettrage, [!INCLUDE[prod_short](includes/prod_short.md)] effectue un contrôle pour s’assurer que toutes les entrées sont lettrées. Par exemple, si vous supprimez un lettrage de quantité mais ne créez pas de nouveau lettrage et, ce faisant, fermez la feuille lettrage, un nouveau lettrage est créé. Cela permet de ne pas toucher au coût. Cependant, si vous supprimez un lettrage fixe, un nouveau lettrage fixe n’est pas créé automatiquement lorsque vous fermez la feuille. Vous devez le faire manuellement en créant un lettrage dans la feuille.
    - Vous pouvez supprimer des lettrages de plusieurs écritures à la fois dans la feuille lettrage. Toutefois, comme le lettrage d’écritures affecte l’ensemble des écritures qui sont disponibles pour le lettrage, vous ne pouvez pas créer un lettrage pour plusieurs écritures à la fois.
    - La feuille lettrage ne peut pas effectuer de lettrage dans la situation suivante : si la quantité en stock est insuffisante pour le lettrage, la feuille lettrage ne peut pas effectuer un lettrage lorsque vous tentez de lettrer une écriture de sortie de stock sans informations de traçabilité sur une écriture d’entrée de stock avec des informations traçabilité.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Pour supprimer un lettrage article en utilisant la feuille lettrage

1.  Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille lettrage**, puis sélectionnez le lien associé.  
2.  La page **Feuille lettrage** s’ouvre en affichant les écritures comptables article existantes de tous les articles.  
3.  Définissez les filtres du raccourci **Général** pour faciliter la recherche de l’écriture comptable article pour laquelle vous souhaitez modifier le lettrage.  
4.  Sélectionnez l’écriture comptable article appropriée, puis sélectionnez l’action **Écritures lettrées**. La page **Voir écritures lettrées - Ecritures lettrées** s’ouvre et affiche l’écriture ou écritures comptables article actuellement lettrées pour l’écriture sélectionnée.  
5.  Sélectionnez l’écriture comptable article pour laquelle vous souhaitez supprimer le lettrage.  
6.  Sélectionnez l’action **Supprimer lettrage**. Cette action supprime l’écriture lettrage article qui lie les deux écritures comptables article et la déplace vers la page **Voir écritures lettrées - Ecritures délettrées**.  
7.  Fermez la page **Afficher les écritures lettrées – Écritures lettrées**.  

 Le champ **Quantité restante** des deux écritures comptables article sont augmentés de la quantité délettrée. L’écriture comptable article supprimée peut à présent être relettrée sur la page **Afficher les écritures lettrées – Écritures non lettrées**.  

> [!IMPORTANT]  
>  Vous ne devez pas laisser des écritures lettrage non lettrées pendant de longues périodes, car d’autres utilisateurs ne peuvent pas traiter les articles concernés jusqu’à ce que vous relettriez les écritures lettrage ou clôturiez la page **Feuille lettrage**. Le message d’erreur suivant s’affiche si vous essayez d’exécuter des actions qui concernent une écriture lettrage manuellement délettrée :  
>   
>  **Il est impossible d’effectuer cette opération car les écritures de l’article \<item\> ne sont pas lettrées dans la feuille lettrage par l’utilisateur \<user\>.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Pour relettrer un lettrage article en utilisant la feuille lettrage

1.  Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 2.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Feuille lettrage**, puis sélectionnez le lien associé.  
2.  La page **Feuille lettrage** s’ouvre en affichant les écritures comptables article existantes de tous les articles.  
3.  Pour relettrer des écritures supprimées depuis l’ouverture de la feuille, sélectionnez l’écriture comptable article que vous souhaitez relettrer et sélectionnez l’action **Relettrer**.  

    > [!NOTE]  
    >  Ce relettrage vers le solde de départ se produit aussi automatiquement lorsque vous fermez la page **Feuille lettrage**.  
4.  Pour lettrer une écriture comptable article en cours disponible dans une autre écriture, sélectionnez l’écriture comptable article que vous souhaitez lettrer. Sélectionnez l’action **Écritures non lettrées**. La page **Afficher les écritures lettrées – Écritures non lettrées** s’ouvre.  
5.  Sélectionnez une ou plusieurs écritures comptables article que vous voulez lettrer dans l’écriture sélectionnée sur la page **Feuille lettrage**, puis choisissez le bouton **OK**.  

     Une écriture lettrage article est créée entre les deux écritures comptables article. Les champs **Quantité restante** des deux écritures sont réduits de la quantité lettrée.  

    > [!NOTE]  
    >  Si vous avez choisi d’effectuer un lettrage qui créerait une boucle infinie dans le processus d’ajustement des coûts, le lettrage que vous avez proposé n’est pas appliqué. Cela peut se produire lorsque les écritures originales ont créé un stock négatif. Le lettrage n’est pas effectué. Par conséquent, vous devez sélectionner une autre écriture pour le lettrage.  
6.  Si, dans les **Paramètres stock**, le champ **Ajustement automatique des coûts** est défini sur **Toujours**, le traitement par lots d’ajustement des coûts est exécuté automatiquement après que vous avez effectué un relettrage. Sinon, exécutez le traitement par lots **Ajuster coûts - Écr. article** pour être sûr que tous les coûts sont actualisés.  

## <a name="see-also"></a>Voir aussi

[Clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Traiter les retours ou annulations d’achats](purchasing-how-process-purchase-returns-cancellations.md)  
 [Gestion des coûts ajustés](finance-manage-inventory-costs.md)   
 [Détails de conception : lettrage article](design-details-item-application.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
