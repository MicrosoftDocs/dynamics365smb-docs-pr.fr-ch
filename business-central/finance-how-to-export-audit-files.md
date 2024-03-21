---
title: Exportation de fichier d’audit
description: 'Cet article explique comment configurer différents formats d’exportation, puis les utiliser, en fonction des besoins de l’auditeur ou de l’autorité.'
author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.devlang: al
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# <a name="audit-file-export"></a>Exportation de fichier d’audit

L’exportation d’informations comptables à partir du système représente une demande courante de certaines autorités ou de certains auditeurs au niveau local. Les formats d’exportation et les informations requises peuvent différer. Les écritures pour l’exportation sont généralement des écritures comptables ou des écritures de taxe sur la valeur ajoutée (TVA). Cependant, d’autres informations sont parfois requises.

**Exportation de fichiers d’audit** est une extension préinstallée qui vous permet d’exporter différentes écritures, en fonction des besoins de l’auditeur ou de l’autorité. Quel que soit le type de format ou les écritures, vous pouvez utiliser la fonctionnalité de l’extension pour contrôler le processus d’exportation des données. La fonctionnalité n’a pas de format de fichier préinstallé pour l’exportation. Par conséquent, vous devez soit installer une application qui a un format spécifique (par exemple, SIE, SAF-T ou FAC) ou développer la vôtre.

> [!NOTE]
> Actuellement, vous pouvez sélectionner le format SIE (Suède), FEC (France) et SAF-T comme application supplémentaire. Les partenaires peuvent également développer un format personnalisé. Le nombre de formats disponibles augmentera avec le temps.

## <a name="set-up-audit-file-export"></a>Configurer l’exportation de fichiers d’audit

1. Sélectionnez le bouton de recherche ![Bouton de la loupe qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration de l’exportation de fichiers d’audit**, et sélectionnez le lien correspondant.
2. Sur la page **Configuration de l’exportation de fichiers d’audit** , suivez ces étapes :

    1. Dans le raccourci **Général** , dans le champ **Code format exportation fichier audit**, spécifiez le code du format d’exportation de fichiers d’audit par défaut. Seuls les formats qui ont été activés lorsqu’un format de fichier spécifique a été installé à partir de la gestion des fonctionnalités et ceux qui ont été ajoutés en tant que format personnalisé sont disponibles.
    2. Dans le raccourci **Qualité des données** , cochez la case **Vérifier informations société** pour être informé des champs d’informations sur l’entreprise qui n’ont pas été configurés correctement.
    3. Cochez la case **Vérifier le client** pour indiquer si vous souhaitez être averti des champs qui n’ont pas été correctement configurés pour des clients spécifiques.
    4. Cochez la case **Vérifier le fournisseur** pour indiquer si vous souhaitez être averti des champs qui n’ont pas été correctement configurés pour des fournisseurs spécifiques.
    5. Cochez la case **Vérifier le compte bancaire** pour indiquer si vous souhaitez être averti des champs qui n’ont pas été correctement configurés pour des comptes bancaires spécifiques.
    6. Cochez la case **Vérifier le code postal** pour être informé d’un code postal qui n’a pas été configuré correctement.
    7. Cochez la case **Vérifier l’adresse** pour être averti lorsqu’une adresse n’a pas été configurée correctement.
    8. Dans le champ **Code postal par défaut**, entrez le code postal à utiliser si aucun code postal n’est spécifié sur la fiche client ou fournisseur.

3. Sélectionnez le bouton de recherche ![Bouton de la loupe qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration du format de l’exportation de fichiers d’audit**, et sélectionnez le lien correspondant.
4. Sur la page **Configuration du format d’exportation de fichiers d’audit**, suivez ces étapes :

    1. Sélectionnez le format d’exportation de fichiers d’audit que vous souhaitez configurer. Seuls les formats qui ont été activés lorsqu’un format de fichier spécifique a été installé à partir de la gestion des fonctionnalités et ceux qui ont été ajoutés en tant que format personnalisé sont disponibles.
    2. Dans le champ **Nom de fichier d’audit**, spécifiez le nom de fichier par défaut ou le modèle de nom de fichier pour le fichier d’audit que vous souhaitez exporter.
    3. Cochez la case **Archiver vers zip** pour compresser automatiquement les fichiers exportés.

## <a name="provide-the-gl-account-mapping-for-audit-file-export"></a>Fournir le mappage du compte général pour l’exportation de fichiers d’audit

La plupart des formats requis par les autorités pour les comptes généraux nécessitent un plan comptable standard spécifique. Par conséquent, après avoir configuré vos comptes généraux, votre fichier exporté sera basé sur les mappages. Vous pouvez utiliser plus de mappages dans votre système.

Procédez comme suit pour fournir le mappage du compte général pour l’exportation de fichiers d’audit.

1. Sélectionnez le bouton de recherche ![Bouton de la loupe qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Mappage de compte général**, et sélectionnez le lien correspondant.
2. Sur la page **Mappage général**, sélectionnez **Nouveau** pour créer un mappage.
3. Dans le champ **Code**, spécifiez le code de mappage qui représente la période de déclaration.
4. Dans le champ **Type de compte standard**, sélectionnez le type de comptes généraux standard.
5. Dans le champ **Format d’exportation du fichier d’audit**, spécifiez le format d’exportation du fichier d’audit auquel les comptes généraux standard sont liés.
6. Dans le champ **Type de période**, le système spécifie une période comptable ou un type de période personnalisé qui a une date et une heure de début flexibles, en fonction de votre sélection. Si vous sélectionnez une période comptable spécifique, le champ sera défini sur **Période comptable**. Sinon, il sera défini sur **Plage de données**.
7. Dans le champ **Période comptable**, spécifiez la date de début de la période comptable qui sera utilisée comme période de rapport, si vous voulez qu’elles soient identiques.
8. Si vous réglez le champ **Période comptable**, les champs **Date de début** et **Date de fin** sont automatiquement définis, en fonction de la période que vous avez spécifiée. Sinon, vous pouvez définir manuellement les dates de début et de fin de votre rapport.
9. Si vous avez déjà ajouté un plan comptable standard, procédez comme suit :

    1. Dans le champ **N° catégorie compte standard** indiquez la catégorie du compte standard ou du code de regroupement utilisé pour le mappage.
    2. Dans le champ **N° de compte standard**, indiquez le code du compte standard ou du code de regroupement utilisé pour le mappage.

10. Cochez la case **Inclure le solde entrant** pour tenir compte du solde entrant du compte général de type **Compte de bilan** doit être pris en compte pour le mappage et non le solde période de la période de déclaration.
11. Pour lancer le mappage, procédez comme suit :

    1. Pour générer des lignes sur la page de **mappage de compte général** sur la base d’un plan de comptes existant, sélectionnez **Initialiser la source du mappage**. Pour copier le mappage du compte général à partir d’un autre code de mappage, sélectionnez **Copier depuis un autre mappage**. Lorsque vous avez terminé de créer des lignes, tous les comptes généraux qui ont enregistré des écritures seront marqués en vert.
    2. Pour marquer uniquement les comptes généraux qui ont des écritures, sélectionnez **Mettre à jour la disponibilité de l’écriture comptable**. Si l’option **Inclure le solde entrant** est activée, toutes les écritures comptables validées sont prises en compte pour le calcul. Sinon, seules les écritures comptables de la période de déclaration sont prises en compte.

## <a name="export-the-audit-file"></a>Exporter le fichier d’audit

1. Sélectionnez le bouton de recherche ![Bouton de la loupe qui ouvre la fonction Fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Documents d’exportation de fichiers d’audit**, et sélectionnez le lien correspondant.
2. Sur la page **Documents d’exportation de fichier d’audit**, sélectionnez **Nouveau**.
3. Sur le raccourci **Général**, suivez ces étapes :

    1. Dans le champ **Format d’exportation de fichiers d’audit** , sélectionnez le format utilisé pour exporter le fichier d’audit.
    2. Dans le champ **Code de mappage de compte général**, sélectionnez le code de mappage de compte général pour la période de déclaration.
    3. Cochez la case **Répartir par mois** si plusieurs fichiers d’audit doivent être générés par mois.
    4. Cochez la case **Répartir par date** si plusieurs fichiers d’audit doivent être générés par jour.
    5. Dans le champ **Commentaire d’en-tête**, entrez le commentaire à inclure dans l’en-tête du fichier d’audit.
    6. Dans le champ **Contact**, spécifiez le contact exporté vers l’en-tête du fichier d’audit.
    7. Cochez la case **Créer plusieurs fichiers zip** pour générer plusieurs fichiers zip.

        > [!IMPORTANT]
        > Cochez cette case uniquement si vous avez déjà installé certaines des applications de format ou si vous en avez créé une personnalisée. L’installation d’un ou plusieurs des formats spécifiques ajoutera probablement des champs et des fonctions à la fonctionnalité **Exportation de fichiers d’audit**, en fonction des exigences de format.

4. Sur le raccourci **Traitement**, suivez ces étapes :

    1. Cochez la case **Traitement parallèle** si vous souhaitez que la génération du fichier d’audit soit traitée par des tâches d’arrière-plan parallèles. Décochez la case pour exporter les données de votre session en cours.
    2. Si vous avez coché la case **Traitement parallèle**, dans le champ  **Nombre max. de tâches**, spécifiez le nombre maximal de tâches d’arrière-plan qui peuvent être exécutées en même temps.
    3. Dans le champ **Date/heure début au plus tôt**, spécifiez la date et l’heure au plus tôt auxquelles la tâche d’arrière-plan doit être exécutée. Si vous exécutez le processus en sélectionnant **Démarrer**, vous pouvez suivre l’état sur les raccourcis **Traitement** et **Lignes**.

5. Lorsque vous avez terminé, sélectionnez **Télécharger en tant que fichier** pour télécharger le fichier d’audit pour la ligne sélectionnée.

> [!IMPORTANT]
> Si vous avez plusieurs entrées à exporter, nous vous déconseillons de les exporter dans la session en cours, en raison d’éventuels problèmes de performances. Au lieu de cela, nous vous recommandons d’utiliser le traitement parallèle pendant les jours ou les heures non ouvrables.

## <a name="see-also"></a>Voir aussi
[Gestion financière](finance.md)  
[Comprendre la comptabilité et le plan comptable](finance-general-ledger.md)  
[Utilisation des axes analytiques](finance-dimensions.md)  
[Utiliser Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
