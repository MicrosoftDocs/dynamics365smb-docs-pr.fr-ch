---
title: Enregistrer la sortie de consommation pour l’ordre de fabrication
description: Cette rubrique explique comment enregistrer la consommation et la sortie pour une ligne de l’ordre de fabrication lancé qui apparaît sur la page Feuille production.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="register-consumption-and-output-for-one-released-production-order-line" />Enregistrer la consommation et la production pour une ligne ordre de fabrication lancé

Cette tâche est réalisée sur la page **Feuille production**. La feuille combine en une seule feuille les fonctions des feuilles distinctes consommation et production. Vous accédez directement à la feuille combinée depuis un ordre de fabrication lancé. Son objectif principal est de valider manuellement la consommation de composants, la quantité d’articles finis produits et le temps passé dans les opérations. Les valeurs sont validées en comptabilité sous l’ordre de fabrication lancé. Les quantités consommées sont validées comme écritures comptables article négatives, les quantités produites sont validées comme écritures comptables article positives et les heures sont validées comme écritures comptables capacité. Ces valeurs validées peuvent également être visualisées au bas de la feuille sous forme de quantités réelles.  

> [!NOTE]  
> Parce que les données relatives à la consommation sont traitées avec celles relatives à la production, cette feuille permet d’afficher les opérations et les composants liés dans une structure opératoire logique. les composants sont indentés sous l’opération à laquelle ils correspondent. Vous devrez pour cela utiliser des codes lien gamme.  

> [!NOTE]  
> les composants ne comportant pas de code lien gamme apparaissent en haut de la feuille.  

## <a name="to-register-consumption-and-output" />Pour enregistrer la consommation et la production

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. lancés**, puis sélectionnez le lien associé.  
2. Ouvrez une ligne d’O.F. lancé qui est prête à être enregistrée, puis sur le raccourci **Lignes**, choisissez l’action **Ligne**, puis l’action **Feuille production**.  

    La page **Feuille production** s’ouvre et affiche les lignes feuille pour la ligne O.F. en fonction des pages **Composant O.F.** et **Gamme O.F.** Ces lignes proviennent de la nomenclature de production et de la gamme affectées à l’article en cours de production. Pour plus d’informations, voir [Créer des nomenclatures de production](production-how-to-create-routings.md).  

3. Dans le champ **Date comptabilisation** situé en haut de la feuille, vous pouvez entrer une date comptabilisation à appliquer à toutes les lignes. Par défaut, ce champ affiche la date de travail. Il permet d’aligner rapidement les dates comptabilisation de toutes les lignes, si nécessaire.  

    > [!NOTE]  
    >  Si vous entrez la date comptabilisation sur une ligne, celle-ci est prioritaire par rapport à la date entrée dans le champ.  

4. Dans le champ **Filtre méthode consommation** situé en haut de la feuille, vous pouvez choisir d’afficher également la consommation et la production validées automatiquement à l’aide des méthodes de consommation définies respectivement pour l’article et pour la ressource. Pour plus d’informations, voir [Activer la consommation en aval des composants en fonction de la production réalisée](production-how-to-flush-components-according-to-operation-output.md).

5. Entrez maintenant les quantités de consommation et production appropriées dans les champs modifiables.  
  
    Sur chaque type de ligne de la feuille, seuls les champs appropriés sont indiquées. Les autres sont vierges et protégés en écriture.  

    À l’ouverture de la feuille, celle-ci comporte les quantités à valider. Si aucune donnée n’a été validée jusque-là, tous les champs de quantité affichent par défaut les quantités prévues issues de l’O.F. Si des validations partielles ont eu lieu, les champs de quantité des lignes affichent les quantités restantes. Les quantités et délais déjà validés pour la commande apparaissent au bas de la feuille en tant qu’entrées réelles.  

    Vous pouvez définir les quantités devant figurer dans le champ **Quantité produite** lors de la première ouverture de la feuille. Pour ce faire, utilisez le champ **Quantité produite prédéfinie** du raccourci **Général** de la page **Paramètres production**.

    > [!NOTE]  
    >  Seule la quantité produite figurant dans la dernière ligne feuille du type d’écriture **Production** ajuste le niveau de stock durant la validation de la feuille. Par conséquent, ne validez pas la feuille, avec les quantités produites prévues sur la dernière ligne de sortie, que lorsque tous les articles finis auront été réellement produits.  

6. Sélectionnez le champ **Terminé** des lignes de sortie pour indiquer que l’opération est terminée. Ce champ est lié au champ **Statut de la gamme** des lignes gamme O.F.  
7. Choisissez l’action **Valider** pour enregistrer les quantités entrées, puis fermez la feuille.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    S’il reste des valeurs à valider, la feuille les indiquera la prochaine fois que vous l’ouvrirez. Les valeurs validées sont affichées sous forme de valeurs réelles au bas de la feuille.  

    > [!NOTE]  
    >  Si un article consommé est bloqué, la feuille ne valide pas les quantités produites correspondantes. Si un poste ou un centre de charge est bloqué, la feuille ne valide ni les quantités produites ni les temps opératoires de la ligne de sortie considérée.  

    > [!NOTE]  
    > Si vous fermez la feuille sans la valider, les modifications apportées seront perdues.  

> [!WARNING]  
> La page **Feuille production** ne peut pas être utilisée par deux utilisateurs simultanément. Cela signifie que si l’utilisateur 2 ouvre la page et entre des données alors que l’utilisateur 1 travaille déjà sur la page, l’utilisateur 2 peut perdre des données lorsque l’utilisateur 1 ferme la page.  

## <a name="see-also" />Voir aussi

[Production](production-manage-manufacturing.md)  
[Paramétrage de la production](production-configure-production-processes.md)  
[Planifié](production-planning.md)  
[Stock](inventory-manage-inventory.md)  
[Achats](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
