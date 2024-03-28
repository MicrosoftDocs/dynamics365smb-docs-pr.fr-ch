---
title: Configurer ou modifier le plan comptable (contient une vidéo)
description: En savoir plus sur la configuration de votre plan comptable pour afficher les comptes généraux qui stockent vos données financières.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 12/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Configurer ou modifier le plan comptable

Le plan comptable affiche les comptes généraux qui stockent vos données financières. [!INCLUDE[prod_short](includes/prod_short.md)] inclut un plan comptable standard prêt à prendre en charge votre société. Vous pouvez, cependant, modifier les comptes par défaut, et vous pouvez ajouter de nouveaux comptes.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Ajouter ou modifier les comptes

À partir du plan comptable, vous pouvez ouvrir chaque compte général et ajouter ou modifier des paramètres. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Vous pouvez, au besoin, utiliser plusieurs lignes pour le nom d’un compte général. Sur la page **Fiche compte général**, dans le groupe **Compte**, choisissez **Textes étendus**, puis remplissez une ou plusieurs lignes avec le texte à copier et le nom du compte.  

Pour les comptes de type **Total**, vous devez renseigner le champ **Totalisation**. Pour les comptes de type **Fin total**, ce champ est renseigné automatiquement par la fonction d’indentation. Après avoir configuré tous les comptes, choisissez l’action **Traiter**, puis choisissez **Indenter plan comptable**.  

> [!IMPORTANT]
> Si vous avez entré des définitions dans les champs **Totalisation** pour les comptes de type **Fin total** avant d’exécuter la fonction d’indentation, vous devez les entrer à nouveau car cette fonction remplace les valeurs de tous les champs **Fin total**.

## <a name="delete-accounts"></a>Supprimer les comptes

Vous pouvez supprimer un compte général. Toutefois, avant que de le supprimer, les conditions suivantes doivent être réunies :  

* Le solde du compte doit être nul.  
* Le champ **Autoriser suppr. cpte gén. av.** doit être défini sur la page **Paramètres comptabilité**, et le compte ne doit pas comporter d’écritures comptables à cette date ou après celle-ci.  
* Si le champ **Vérifier activité cpte général** de la page **Paramètres comptabilité** est sélectionné, le compte ne doit pas être utilisé dans les groupes comptabilisation ni dans une configuration de la validation.  

[!INCLUDE[prod_short](includes/prod_short.md)] vous empêche de supprimer un compte général qui stocke les données nécessaires au plan comptable.  

Vous pouvez également spécifier quand autoriser les utilisateurs à supprimer des comptes. Sur le **Configuration du Grand Livre** page, la **Bloquer la suppression des comptes généraux** la bascule fonctionne avec la date dans le **Vérifiez le compte G/L. Suppression après** champ pour agir comme une validation supplémentaire. Si vous activez **Bloquer la suppression des comptes généraux**, vous ne pouvez pas supprimer les comptes généraux avec des écritures comptables postérieures à la date indiquée dans le champ **Vérifier suppr. cpte gén. av.**. Pour supprimer un tel compte, une personne ayant accès au **Paramètres comptabilité** la page doit éteindre le **Bloquer la suppression des comptes généraux** basculer.  

La désactivation du champ **Bloquer la suppression des comptes généraux** est une pratique exemplaire, tout comme définir la date dans le champ **Vérifier suppr. cpte gén. ap.**, par exemple à la date à laquelle vous devez stocker vos données financières.  

### <a name="video-guidance"></a>Guidage vidéo

Cette vidéo montre comment spécifier si et quand les utilisateurs peuvent supprimer des comptes G/L.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="see-also"></a>Voir aussi

[Comptabilité et plan comptable](finance-general-ledger.md)  
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Utiliser les axes analytiques](finance-dimensions.md)  
[Importation des données à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Utiliser les états financiers](bi-how-work-account-schedule.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Clôturer les comptes de gestion dans la version française](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Imprimer les comptes de résultat dans la version australienne](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Imprimer les comptes de résultat dans la version néo-zélandaise](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Configurer et clôturer les soldes du compte de résultat dans la version espagnole](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Indenter et valider le plan comptable dans la version espagnole](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
