---
title: Dépannage de votre Hub Entreprise
description: Découvrez comment contourner les problèmes lorsque vous dépannez votre Hub Entreprise dans Dynamics 365 Business Central pour gérer le travail dans plusieurs entreprises.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accountant, accounting, troubleshoot'
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Dépannage de votre Hub Entreprise

L’ajout de sociétés au tableau de bord Hub Entreprise est assez facile, mais cet article traite des problèmes que vous pouvez rencontrer en route.  

## Vérifier les erreurs

Utilisez l’action **Vérifier les erreurs** pour afficher une liste des erreurs récentes. Vous pouvez voir des détails supplémentaires pour chaque erreur et vous pouvez nettoyer le journal en supprimant les anciennes entrées.  

## Échec de la connexion

Il peut y avoir plusieurs raisons pour lesquelles vous ne pouvez pas vous connecter à une entreprise, notamment les suivantes :

- L’URL dans le champ **Lien d’environnement** n’est pas valide  

  Aller à la page **Liens d’environnements**, ouvrez l’environnement auquel vous ne pouvez pas vous connecter, puis choisissez l’action **Tester la connexion**.  
- La société du client est actuellement hors connexion, par exemple si elle est en cours de mise à niveau

  Dans votre tableau de bord, choisissez l’élément de menu **Outils**, puis **Vérifier les erreurs**. Cela ouvre une liste avec des informations techniques vous permettant de contacter votre administrateur si vous voyez des erreurs. Par exemple, le message d’erreur « *Le serveur a rejeté les informations d’identification du client* » suggère que vous n’avez pas accès.  
- Vous n’avez pas accès à toutes les entreprises de l’environnement auquel vous essayez de vous connecter

  Dans [!INCLUDE [prod_short](includes/prod_short.md)], une organisation peut avoir plusieurs centres de profit appelés entreprises et vous n’aurez peut-être pas accès à toutes les entreprises. Communiquez avec votre administrateur ou client pour vous assurer que vous avez accès aux sociétés dans lesquelles vous devez travailler.  

## Les données ne s’actualisent pas

Lorsque vous ajoutez une société ou que vous demandez une actualisation des données, [!INCLUDE [prod_short](includes/prod_short.md)] récupère les données. Mais vous devez actualiser la page vous-même, par exemple en choisissant l’action **Afficher à nouveau toutes les sociétés**, actualisez la page du navigateur, quittez le tableau de bord puis retournez-y, ou similaire.  

Si vous avez ajouté une entreprise, mais qu’elle ne s’affiche pas dans la liste, vous pouvez également utiliser l’action **Recharger toutes les entreprises** pour mettre à jour la liste.

## Voir aussi

[Gérer le travail entre plusieurs entreprises dans le Hub Entreprise](company-hub.md)  
[Ajouter des entreprises à votre Hub Entreprise](company-hub-add-company.md)  
[Expériences de comptables dans Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]