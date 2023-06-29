---
title: Résolution des erreurs de synchronisation
description: 'Cette rubrique offre des instructions pour identifier, résoudre les problèmes et les erreurs de synchronisation.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a>Résolution des erreurs de synchronisation


Il y a beaucoup de pièces mobiles impliquées dans l’intégration [!INCLUDE[prod_short](includes/prod_short.md)] avec [!INCLUDE[prod_short](includes/cds_long_md.md)], et parfois les choses ne se passent pas bien. Cette rubrique répertorie certaines des erreurs types qui se produisent et donne des indications sur la manière de les résoudre.

Les erreurs se produisent souvent à cause de quelque chose qu’un utilisateur a fait pour coupler des enregistrements ou parce que la configuration de l’intégration est fausse. Pour les erreurs liées aux enregistrements couplés, les utilisateurs peuvent les résoudre eux-mêmes. Ces erreurs sont causées par des actions telles que la suppression de données dans l’une des applications métier mais pas les deux, puis la synchronisation. Pour plus d’informations, voir [Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md).

Les erreurs liées à la configuration de l’intégration nécessitent généralement l’attention de l’administrateur. Vous pouvez voir ces erreurs sur la page **Erreurs de synchronisation d’intégration**. 

Le tableau suivant fournit des exemples de problèmes typiques :  

|Problème  |Résolution  |
|---------|---------|
|Les autorisations et les rôles attribués à l’utilisateur d’intégration ne sont pas corrects. | Cette erreur vient de [!INCLUDE[prod_short](includes/cds_long_md.md)] et comprend souvent le texte suivant « Utilisateur principal (Id=\<user id>, type=8) ne dispose pas du privilège \<privilegeName> ». Cette erreur se produit, car il manque à l’utilisateur d’intégration un privilège lui permettant d’accéder à une entité. En règle générale, cette erreur se produit si vous synchronisez des entités personnalisées ou si une application est installée dans [!INCLUDE[prod_short](includes/cds_long_md.md)] qui nécessite l’autorisation d’accéder à d’autres entités [!INCLUDE[prod_short](includes/cds_long_md.md)]. Pour résoudre cette erreur, attribuez l’autorisation à l’utilisateur d’intégration dans [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Vous pouvez trouver le nom d’utilisateur d’intégration sur la page **Configuration de la connexion Dataverse**. Le message d’erreur fournira le nom de l’autorisation, ce qui peut vous aider à identifier l’entité pour laquelle vous avez besoin d’une autorisation. Pour ajouter le privilège manquant, connectez-vous à [!INCLUDE[prod_short](includes/cds_long_md.md)] avec un compte administrateur et modifiez le rôle de sécurité attribué à l’utilisateur d’intégration. Pour plus d’informations, voir [Créer ou modifier un rôle de sécurité pour gérer l’accès](/power-platform/admin/create-edit-security-role). |
|Vous couplez un enregistrement qui utilise un autre enregistrement qui n’est pas couplé. Par exemple, un client dont la devise n’est pas couplée ou un article pour lequel l’unité n’est pas couplée. | Vous devez d’abord coupler l’enregistrement dépendant, par exemple une devise ou une unité, puis réessayer le couplage. |

Voici quelques outils sur la page Erreurs de synchronisation d’intégration qui peuvent vous aider à résoudre manuellement ces problèmes.  

* Les champs **Origine** et **Destination** peuvent contenir des liens vers la ligne où l’erreur a été trouvée. Cliquez sur le lien pour rechercher l’erreur.  
* Les actions **Supprimer les écritures ultérieures à 7 jours** et **Supprimer toutes les écritures** vont nettoyer la liste. En règle générale, vous utilisez ces actions après avoir résolu la cause d’une erreur affectant de nombreux enregistrements. Faites attention, cependant. Ces actions peuvent supprimer des erreurs toujours pertinentes.
* L’action **Afficher la pile d’appels de l’erreur** affiche des informations qui peuvent aider à identifier la cause de l’erreur. Si vous ne pouvez pas résoudre l’erreur vous-même et que vous décidez de soumettre une demande d’assistance, incluez les informations dans la demande d’assistance.

## <a name="see-also"></a><a name="see-also"></a>Voir aussi
[Intégration à Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuration des comptes d’utilisateur pour intégration à Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurer une connexion vers Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Coupler et synchroniser des enregistrements manuellement](admin-how-to-couple-and-synchronize-records-manually.md)  
[Afficher le statut d’une synchronisation](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
