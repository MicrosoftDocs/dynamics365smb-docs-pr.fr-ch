---
title: Fusionner les doublons d’enregistrements fournisseur ou client
description: Décrit comment consolider les informations sur les clients ou les fournisseurs lorsque vous avez des entrées en double pour certains.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="merge-duplicate-records" />Fusionner les doublons d’enregistrements

Puisque différents utilisateurs créent de nouvelles fiches contact, fournisseur ou client au fil du temps, ou puisque de nouveaux enregistrements sont créés automatiquement pendant la migration, un client, fournisseur ou contact peut être représenté dans le système avec plusieurs enregistrements. Dans ce cas, vous pouvez utiliser la page **Fusionner le doublon** depuis la fiche de l’enregistrement que vous souhaitez conserver. La page vous donne un aperçu des valeurs de champ dupliquées et vous fournit des fonctions pour sélectionner quelles valeurs conserver ou ignorer lors de la fusion des deux enregistrements en un seul.

> [!NOTE]
> Seuls les utilisateurs avec l’autorisation FUSIONNER LES DOUBLONS peuvent utiliser cette fonctionnalité.

> [!TIP]
> La page **Fusionner le doublon** affiche tous les champs où les valeurs sont différentes pour les deux enregistrements comparés. Par conséquent, un doublon est indiqué par la page affichant très peu de champs. Cela dit, si la page affiche plusieurs champs, l’enregistrement supposé n’est probablement pas un doublon.

La procédure suivante se base sur une fiche article. La procédure est identique pour les fiches fournisseur ou contact.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Clients**, puis choisissez le lien associé.
2. Sélectionnez le client pour lequel vous savez, ou vous supposez, qu’il existe un doublon d’enregistrement, puis sélectionnez l’action **Modifier**.
3. Sur la page **Fiche client**, sélectionnez l’action **Fusionner avec**.
4. Sur la page **Fusionner le doublon**, dans le champ **Fusionner avec**, sélectionnez le client pour lequel vous soupçonnez qu’il existe un doublon de celui que vous avez ouvert, indiqué dans le champ **Actuel**.

    Le raccourci **Champs** répertorie les champs où les valeurs sont différentes pour les deux clients. Cela signifie que si le client sélectionné est vraiment un doublon, alors très peu de champs seulement doivent être répertoriés, comme les erreurs de saisie et autres erreurs de saisie des données.

    Le raccourci **Tables associées** répertorie les tables où les champs ont une relation avec les deux clients. Les champs **Nombre actuel** et **Nombre en double** présentent le nombre de champs dans les tables associées où la valeur **N°** du client actuel et du doublon de client est utilisée. Sur la page **Fusionner le doublon**, cette section est ici uniquement à titre informatif. Cependant, si des conflits de fusion existent, vous les résoudrez sur la page **Fusionner les conflits de doublon**. Voir les étapes 8 à 12.   

5. Pour chaque champ pour lequel vous souhaitez utiliser une autre valeur que la valeur actuelle, cochez la case **Remplacer**. La valeur du champ **Valeur secondaire** est ensuite transférée vers l’enregistrement actuel lorsque vous exécutez le processus.
6. Lorsque vous avez fini de sélectionner quelles valeurs conserver ou remplacer, choisissez l’action **Fusionner**.

    Le système vérifie si la fusion des valeurs pour le doublon de client dans le client actuel génère un conflit. Un conflit existe si une valeur dans au moins un champ de clé primaire est identique pour certains clients même si la valeur dans le champ **Non** est différente pour les deux clients.

7. Si aucun conflit n’est identifié, sélectionnez le bouton **Oui** dans la zone de message de confirmation.

    Le doublon de client est renommé de telle sorte que toute utilisation de sa valeur **N°** dans tous les champs avec des relations avec la table client sera remplacée par la valeur **N°** du client actuel.
8. Si des conflits existent, sélectionnez l’action **Résoudre (xx) conflits avant fusion** sur le raccourci **Conflits**, qui s’affiche si des conflits existent.
9. Sur la page **Fusionner les conflits de doublon**, sélectionnez la ligne pour une table concernée par un conflit, puis choisissez l’action **Afficher les détails**.

    La page **Fusionner le doublon** affiche maintenant les champs de la table sélectionnée qui entraînent un conflit de fusion entre les deux enregistrements client. Vous observerez dans les deux valeurs récapitulées dans les champs **Actuel** et **Conflits avec** et sur les lignes sur lesquelles au moins un champ de clé principale est identique pour les deux clients et la valeur du champ **N°** est différent pour les deux clients.   
10. Si vous ne souhaitez pas conserver le doublon d’enregistrement client, choisissez l’action **Supprimer le doublon**, puis choisissez le bouton **Fermer**.

    Les valeurs de champ identiques, autres que la valeur du champ **N°**, sont supprimées depuis le doublon d’enregistrement et inséré sur l’enregistrement actuel.
11. Si vous souhaitez conserver le doublon d’enregistrement client après la fusion, sélectionnez l’option **Renommer le doublon**.
12. Sur les lignes, pas pour le champ **N°**, où le champ a la même valeur sur les deux enregistrements, changez la valeur dans la champ **Valeur secondaire**, puis sélectionnez le bouton **Fermer**.

    La valeur du champ en conflit est mise à jour sur le doublon d’enregistrement de telle sorte qu’elle peut être fusionnée avec l’enregistrement actuel. Le doublon d’enregistrement existe toujours après la fusion.
13. Répétez les étapes 8 à 12 jusqu’à ce que tous les conflits soient résolus. Le raccourci **Conflits** disparaît.
14. Sur la page **Fusionner le doublon**, sélectionnez à nouveau l’action **Fusionner**, puis cliquez sur le bouton **Oui** dans la zone du message de confirmation.

> [!NOTE]
> Pour les contacts, vous pouvez utiliser la fonctionnalité pour trouver des doublons de contact avant d’utiliser la page **Fusionner le doublon**. Pour plus d’informations, reportez-vous à la rubrique [Recherche de doublons de contact](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics--business-central" />Voir la [formation Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi

[Ventes](sales-manage-sales.md)  
[Configurer les contacts](marketing-setup-contacts.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
