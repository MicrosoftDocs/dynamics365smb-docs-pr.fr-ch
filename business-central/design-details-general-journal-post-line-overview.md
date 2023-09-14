---
title: Aperçu de la ligne validation de feuille comptabilité
description: 'Cette rubrique présente les modifications apportées à Codeunit 12, Gen. Feuille article – Valider ligne, et est le seul endroit pour insérer les écritures du grand livre général, de la TVA et des clients et fournisseurs.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, general ledger, post'
ms.date: 06/15/2021
ms.author: bholtorf
---
# Aperçu de la ligne validation de feuille comptabilité

Codeunit 12, **Groupe compta.-Ligne validation**, est l’objet d’application majeur pour la validation de la comptabilité et est le seul emplacement pour insérer des écritures comptables, la TVA, et les écritures comptables client et fournisseur. Ce codeunit est également utilisé pour toutes les opérations Appliquer, Désappliquer et Inverser.  
  
Dans Microsoft Dynamics NAV 2013 R2, le codeunit a été repensé, car il était devenu très grand, avec environ 7 600 lignes de code. L’architecture a été modifiée et le codeunit a été rendu plus simple et plus facile à modifier. Cette documentation décrit les modifications et fournit les informations dont vous aurez besoin pour la mise à niveau.  
  
## Ancienne architecture  
L’ancienne architecture avait les fonctions suivantes :  
  
* Il y a eu une utilisation extensive des variables globales, qui ont augmenté la possibilité d’erreurs masquées dues à l’utilisation de variables avec une portée incorrecte.  
* Il y a eu beaucoup de procédures longues (avec plus de 100 lignes de code) qui présentaient également une complexité cyclomatique élevée (c’est-à-dire, beaucoup de formulations imbriquées CASSE, RÉPÉTITION, SI), ce qui a rendu le code très difficile à mire et modifier.  
* Plusieurs procédures qui n’étaient utilisées que localement et ne devaient être utilisées que localement n’ont pas été marquées comme locales.  
* La plupart des procédures n’avaient pas de paramètres et utilisaient des variables globales. Certains utilisaient des paramètres et écrasaient les variables globales par des valeurs locales.  
* Les combinaisons de code pour trouver les comptes généraux et créer des écritures comptables et les écritures TVA n’ont pas été standardisées et n’ont pas été variées d’un endroit à l’autre. En outre, il y a beaucoup de duplication de code et une symétrie rompue entre le code client et fournisseur.  
* Une grande partie du code dans le codeunit 12, approximativement 30 %, est lié aux calculs d’escompte et écart, même si ces fonctions ne sont pas nécessaires dans de nombreux pays ou régions.  
* Validation, Appliquer, Désappliquer, Contrepasser, Escompte et écart de paiement, et Ajustement du taux de change ont été associés dans le odeunit 12 à l’aide d’une longue liste de variables globales.  
  
### Nouvelle architecture  
Dans [!INCLUDE[prod_short](includes/prod_short.md)], le codeunit 12 présente les améliorations suivantes :  
  
* Le Codeunit 12 a été remanié en procédures plus petites (toutes inférieures à 100 lignes de code).  
* Des motifs standardisés pour la recherche des comptes généraux ont été mis en œuvre à l’aide de les fonctions de participation des tableaux de groupes de validation.  
* Un cadre de moteur de validation a été mis en œuvre pour gérer le début et la fin des transactions et pour trouver la création dans les écritures comptables et les écritures TVA, la collection d’ajustement TVA, et le calcul des montants supplémentaires en devise.  
* La duplication de code a été éliminée.  
* De nombreuses fonctions de participation ont été transférées vers les tableaux d’écritures comptables client et fournisseur correspondantes.  
* L’utilisation des variables globales a été réduite, de façon à ce que chaque procédure utilise des paramètres et contienne sa propre logique d’application.  
  
## Voir aussi

[Détails de conception : Structure de l’interface de validation](design-details-posting-interface-structure.md)  
[Détails de conception : Structure du moteur de validation](design-details-posting-engine-structure.md)  
[Détails de conception : Ligne validation de feuille comptabilité (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]