---
title: Spécification des périodes comptabilisation
description: Vous spécifiez des périodes de validation (dates début et fin) pour configurer quand les utilisateurs peuvent valider en comptabilité.
author: brentholtorf
editor: ''
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: user setup
ms.search.form: 118
ms.date: 12/05/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="specify-posting-periods"></a>Spécification des périodes comptabilisation

Utilisez les périodes de validation pour spécifier quand les utilisateurs peuvent procéder à la validation dans la comptabilité.  

## <a name="to-specify-posting-periods"></a>Pour définir des périodes de validation

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Paramètres comptabilité**, puis choisissez le lien associé.  
2. Sur la page **Paramètres comptabilité**, définissez la période en entrant des dates dans les champs **Début période validation** et **Fin période validation**.  

> [!NOTE]  
> Ces périodes de validation s’appliquent à la société et à tous les utilisateurs. Pour autoriser des exceptions, vous pouvez définir différentes périodes de validation pour des utilisateurs spécifiques sur la page **Paramètres utilisateur**. Ces périodes de validation sont prioritaires sur celles spécifiées sur la page **Paramètres comptabilité**. Pour plus d’informations, reportez-vous à [Pour configurer des contraintes de temps pour les utilisateurs](ui-define-granular-permissions.md#to-set-up-time-constraints-for-users).

## <a name="video-guidance"></a>Guidage vidéo

Lorsque vous clôturez une période comptable, vous souhaiterez peut-être empêcher l’entrée de nouvelles publications ou autoriser uniquement certaines personnes à valider des transactions. La vidéo suivante montre comment contrôler quand et qui peut comptabiliser des transactions dans votre grand livre.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fAB8]

## <a name="see-also"></a>Voir aussi

[Finances](finance.md)  
[Exécution des processus de clôture d’exercice](year-how-complete-period-end-processes.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
