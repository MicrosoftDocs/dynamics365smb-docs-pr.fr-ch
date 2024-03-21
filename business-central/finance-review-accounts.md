---
title: Examiner la comptabilité
description: Vous pouvez suivre votre progression lorsque vous examinez les montants en comptabilité.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
ms.service: dynamics-365-business-central
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Examiner les montants dans la comptabilité

Vous avez peut-être une comptabilité qui exige une surveillance fréquence. Ou vous voudrez peut-être accélérer le processus d’examen à la fin du mois. Pour vous aider à garder une trace de ce que vous avez fait et pour accélérer les examens, utilisez l’action **Examiner les entrées** sur la page **Plan comptable** ou **Fiche compte général** pour chaque compte. 

## <a name="set-up-accounts-for-reviews"></a>Configurer les comptes à des fins d’examen

Sur la page **Fiche compte général** pour chaque compte, spécifiez comment autoriser les examens dans le champ **Stratégie de révision**.

|Vérifier la stratégie  |Description  |
|---------|---------|
|Aucun     | Vous ne pouvez pas marquer les écritures comptables comme examinées. Par exemple, utilisez cette option pour des comptes tels que les fournisseurs, les clients et les comptes bancaires pour lesquels il existe d’autres moyens d’examiner leurs montants.        |
|Autoriser la révision     | Vous n’êtes pas obligé d’inclure des écritures dans un examen, et les montants des écritures de débit et de crédit n’ont pas à s’équilibrer. Vous supprimez un examen, par exemple, si vous avez fait une erreur.        |
|Autoriser la révision et solde de correspondance     | Les montants totaux des écritures de débit et de crédit lors de l’examen doivent correspondre. Les champs **Débit** et **Crédit** indiquent ces montants, et le champ **Solde** indique le total. Ce paramètre vous permet également de supprimer un examen. Lorsque vous supprimez un examen d’une ou plusieurs écritures, les écritures de débit et de crédit doivent toujours s’équilibrer.        |

## <a name="mark-entries-as-reviewed"></a>Marquer les écritures comme examinées

Choisissez les écritures que vous avez examinées, puis utilisez l’action **Définir la sélection comme révisée**. Chaque fois que vous marquez une ou plusieurs écritures comme examinées, elles reçoivent le même numéro dans la colonne **Identifiant révisé**. L’identifiant de révision est un moyen pratique de garder une trace des écritures qui ont été révisées en même temps. [!INCLUDE [prod_short](includes/prod_short.md)] enregistre également l’utilisateur qui a fait l’examen et quand il l’a fait.

Si vous marquez des écritures comme révisées, mais que vous regrettez de l’avoir fait, utilisez l’action **Définir la sélection comme non révisée**.

* Si la stratégie Examen autorisé est attribuée au compte, l’action réinitialise l’identifiant examiné à 0 et supprime la personne ainsi que la date et l’heure de l’examen. 
* Si la stratégie Examen du solde autorisé et de correspondance est attribuée, le crédit et le débit doivent toujours s’équilibrer. Par exemple, si l’une des écritures d’un examen est une erreur, vous pouvez choisir une autre écriture avec la bonne valeur. L’écriture de remplacement n’a pas besoin d’avoir le même identifiant révisé.

> [!TIP]
> Un moyen rapide de choisir plusieurs écritures consiste à maintenir la touche Ctrl ou Maj enfoncée pendant que vous choisissez les écritures. Ctrl vous permet de sélectionner des écritures spécifiques et Maj sélectionne toutes les écritures entre la première et la dernière écritures sélectionnées.

## <a name="review-accounts-that-have-old-entries"></a>Examiner les comptes qui ont d’anciennes écritures

Vous avez peut-être des écritures de périodes passées que vous avez déjà examinées ou qui n’ont tout simplement pas besoin d’être révisées. Vous souhaitez simplement commencer à examiner les écritures à partir, par exemple, du début de l’année ou de la période comptable. Vous pouvez ensuite laisser les écritures telles quelles. Toutefois, si vous souhaitez analyser des données dans Excel ou en utilisant le mode d’analyse, marquez les écritures comme révisées. Pour en savoir plus sur l’analyse des écritures, consultez [Analyser les écritures](#analyze-entries). Pour marquer les écritures comme révisées, ajoutez un filtre dans le volet Filtre pour n’afficher que ces écritures, puis choisissez l’action **Marquer les écritures sélectionnées comme révisées**.

## <a name="filter-entries"></a>Filtrer les écritures

Pour obtenir une image plus claire, il existe plusieurs façons de filtrer les écritures sur la page **Réviser les écritures comptables**.

* Utilisez les actions **Afficher les écritures examinées** et **Masquer les écritures examinées** pour afficher uniquement les écritures que vous avez ou n’avez pas examinées. Pour effacer les filtres, utilisez l’action **Afficher toutes les écritures**.
* Utilisez le volet Filtre. Par exemple, vous pouvez filtrer par numéro de compte ou, si vous avez des écritures plus anciennes et que vous souhaitez toutes les marquer comme révisées, par date de publication.

## <a name="analyze-entries"></a>Analyser les écritures

Il existe plusieurs façons d’analyser les écritures comptables que vous avez examinées.

* Activez le mode d’analyse, par exemple, pour regrouper les écritures en fonction de leur identifiant révisé. Pour en savoir plus sur le mode d’analyse, accédez à [Analyser les données de la page de liste à l’aide du mode d’analyse](analysis-mode.md).
* Exportez les écritures vers Excel.

## <a name="see-also"></a>Voir aussi

[Familiarisation avec la comptabilité et le plan comptable](finance-general-ledger.md)  
[Configurer ou modifier le plan comptable](finance-setup-chart-accounts.md)  
