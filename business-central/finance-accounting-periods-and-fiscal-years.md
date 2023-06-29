---
title: Utilisation des périodes et exercices comptables
description: En savoir plus sur l’utilisation des périodes comptables pour définir le moment où votre société fait état de ses performances financières.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 08/25/2022
ms.author: bholtorf
---
# <a name="work-with-accounting-periods-and-fiscal-years"></a><a name="work-with-accounting-periods-and-fiscal-years"></a>Utiliser des périodes et exercices comptables

Les périodes comptables, également appelées périodes de report, sont des périodes pour lesquelles une société ou une organisation présente ses performances financières, en générant par exemple leurs résultats ou leur bilan. Généralement, les périodes comptables sont liées à l’exercice comptable de la société, qui peut contenir plusieurs périodes comptables, telles que des mois ou des trimestres.

Pour de nombreuses entreprises, l’année fiscale ne correspond pas à l’année civile, par exemple lorsque l’année fiscale se termine le 30 juin au lieu du 31 décembre. Pour les sociétés que vous venez de créer, l’exercice fiscal peut même durer plus de 12 mois.  

[!INCLUDE[prod_short](includes/prod_short.md)] nécessite uniquement des périodes comptables si vous souhaitez fermer un compte de gestion, ou exécuter des tâches de compression de données.

Vous pouvez utiliser des périodes comptables dans la génération d’états, par exemple lorsque vous consultez les écritures validées sur la page **Réalisé/budget** où l’intervalle de génération d’état est spécifié. L’une des options consiste à spécifier la génération d’état par période comptable. Vous pouvez également créer un état financier qui compare les résultats de différentes périodes comptables.

## <a name="creating-a-new-fiscal-year"></a><a name="creating-a-new-fiscal-year"></a>Création d’exercice comptable

Vous pouvez créer des périodes comptables en bloc, à l’aide du traitement par lots **Créer exercice comptable**, ou manuellement.

### <a name="how-to-create-accounting-periods-in-bulk"></a><a name="how-to-create-accounting-periods-in-bulk"></a>Comment créer des périodes comptables en bloc

Utilisez le traitement par lots **Créer exercice comptable** pour diviser un exercice comptable en périodes de même durée.  

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Rechercher une page ou un état") entrez **Périodes comptables**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Créer exercice**.
3. Dans le champ **Date début**, saisissez la date à laquelle l’exercice comptable commence.  
4. Dans le champ **Nombre de périodes**, spécifiez le nombre de périodes comptables composant l’exercice comptable. Il peut y avoir un maximum de 365 périodes dans une année.  
5. Dans le champ **Base période**, entrez une durée pour chaque période. Les identificateurs de durée sont 1M pour un mois, 1T pour un trimestre, et 1Y pour une année.  
6. Cliquez sur **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a><a name="how-to-create-accounting-periods-manually"></a>Comment créer des périodes comptables manuellement

Si les périodes comptables de l’exercice comptable ont différentes durées, comme le calendrier 4-4-5 utilisé dans la vente au détail, vous pouvez les établir manuellement.  
  
1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Rechercher une page ou un état") entrez **Périodes comptables**, puis sélectionnez le lien associé.  
2. Dans le champ **Date début**, saisissez la date à laquelle l’exercice comptable commence. Le champ **Nom** affiche à présent le nom du mois.  
3. Activez la case à cocher **Nouvel exercice comptable** pour indiquer qu’il s’agit de la première période de l’exercice. [!INCLUDE[prod_short](includes/prod_short.md)] utilise cette période pour déterminer les périodes à clôturer en fin d’exercice.
4. Répétez les étapes 2 et 3 pour chaque période restante.  

## <a name="closing-a-fiscal-year"></a><a name="closing-a-fiscal-year"></a>Clôture d’un exercice comptable

Clôturer l’exercice comptable est l’une des tâches pour clôturer les livres. Une fois l’exercice comptable clôturé, les cases **Fermé** et **Verrouillage date** sont activées pour toutes les périodes de l’exercice. Vous ne pouvez pas rouvrir un exercice ou désactiver les cases.

> [!NOTE]  
> Vous devez toujours avoir au moins un exercice comptable ouvert. Lorsque vous clôturez un exercice, assurez-vous qu’un exercice a été créé. De plus, sachez que lorsque vous clôturez un exercice, vous ne pouvez pas modifier la date début de l’exercice suivant.

1. Choisissez l’icône ![age ou état pour la recherche.](media/ui-search/search_small.png "Icône Page ou état pour la recherche") entrez **Périodes comptables**, puis sélectionnez le lien associé.  
2. Choisissez l’action **Clôturer exercice**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a><a name="posting-entries-to-a-closed-fiscal-year"></a>Validation d’écritures dans un exercice comptable clôturé

Même si un exercice comptable est clôturé, vous pouvez toujours y valider des écritures. Dans ce cas, les écritures sont marquées comme validées dans un exercice comptable clôturé et la case à cocher **Ecr. exercice précédent** est activée. Par défaut, la case à cocher n’est pas affichée sur la page, mais vous pouvez l’ajouter. Les étapes suivantes consistent à clôturer les comptes de gestion traités et à transférer les résultats de l’année sur un compte de bilan. Répétez ces étapes chaque fois que vous validez des écritures dans un exercice comptable clôturé.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi

[Clôture des livres](year-close-books.md)  
[Clôture des exercices et des périodes](year-close-years-periods.md)  
[Comment utiliser les états financiers](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
