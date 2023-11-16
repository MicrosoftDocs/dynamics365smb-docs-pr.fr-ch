---
title: Mappage de champs lors de l’importation de fichiers SEPA CAMT | Microsoft Docs
description: 'Dans les marchés européens, vous pouvez importer des fichiers de relevé bancaire selon les normes régionales SEPA (Espace unique de paiement en euros).'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/06/2023
ms.custom: bap-template
---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Mappage de champs lors de l’importation de fichiers SEPA CAMT

[!INCLUDE[prod_short](includes/prod_short.md)] prend en charge les normes régionales SEPA (Espace unique de paiement en euros) pour importer les relevés bancaires SEPA (format CAMT). Pour plus d’informations, voir [Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

 La norme SEPA CAMT standard présente elle-même des variations locales. Par conséquent, vous pouvez être amené à modifier la définition d’échange de données générique (représentée par le code **SEPA CAMT** sur la page **Définitions d’échange de données**) pour l’adapter à une variation locale de la norme. Les tables suivantes indiquent le mappage d’élément à champ pour les tables 81, 273 et 274 dans l’implémentation de SEPA CAMT dans [!INCLUDE[prod_short](includes/prod_short.md)].  

 Pour plus d’informations sur la création ou l’ajustement de définition d’échange de données, voir [Configurer les définitions d’échange de données](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>Mappage des données de CAMT aux champs de la table Feuille comptabilité (81)

|Chemin d’accès d’articles|Élément message|Type de données|Désignation|Identifiant signe négatif|N° champ|Nom du champ|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Montant|Décimale|Le montant de l’argent dans l’écriture de caisse.||13|Montant|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texte.|Indique si l’écriture est une écriture de crédit ou débit|DBIT|13|Montant|  
|Stmt/Ntry/BookgDt/Dt|Date|Date|Date à laquelle une écriture est validée dans un compte sur les livres de compte du gestionnaire||5|Date comptabilisation|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|La date et l’heure auxquelles une écriture est validée dans un compte sur les livres de compte du gestionnaire||5|Date comptabilisation|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nom|Texte.|Le nom de la partie qui doit une somme d’argent au créancier (final)||1 221|Informations payeur|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Non structuré|Texte.|Les informations à votre disposition pour activer la correspondance/le rapprochement d’une écriture avec les articles que le paiement doit régler, telles que les factures commerciales dans un système comptes-clients, sous forme non structurée||8|Désignation|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texte.|Informations supplémentaires sur l’écriture.||1 222|Informations transaction|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>Mappage des données de CAMT aux champs de la table Rapprochement bancaire (273)

|Chemin d’accès d’articles|Élément message|Type de données|Désignation|Identifiant signe négatif|N° champ|Nom du champ|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Date|Date et heure de création du message||3|Date relevé|  
|Stmt/Bal/Amt|Montant|Décimale|Le montant résultant des montants ajustés pour toutes les écritures débit et crédit||4|Solde final du relevé|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>Mappage des données de CAMT aux champs de la table Ligne rapprochement bancaire (274)

|Chemin d’accès d’articles|Élément message|Type de données|Désignation|Identifiant signe négatif|N° champ|Nom du champ|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Montant|Décimale|Le montant de l’argent dans l’écriture de caisse.||7|Montant relevé|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texte.|Indique si l’écriture est une écriture de crédit ou débit|DBIT|7|Montant relevé|  
|Stmt/Ntry/BookgDt/Dt|Date|Date|Date à laquelle une écriture est validée dans un compte sur les livres de compte du gestionnaire||5|Date transaction|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|La date et l’heure auxquelles une écriture est validée dans un compte sur les livres de compte du gestionnaire||5|Date transaction|  
|Stmt/Ntry/ValDt/Dt|Date|Date|Date à laquelle les immobilisations sont disponibles pour le propriétaire du compte en cas d’écriture créditrice, ou cessent d’être disponibles pour le propriétaire du compte en cas d’écriture débitrice||12|Date de valeur|  
|Stmt/Ntry/ValDt/DtTm|DateTime|DateTime|La date et l’heure auxquelles les immobilisations sont disponibles pour le propriétaire du compte en cas d’écriture créditrice, ou cessent d’être disponibles pour le propriétaire du compte en cas d’écriture débitrice||12|Date de valeur|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nom|Texte.|Le nom de la partie qui doit une somme d’argent au créancier (final)||15|Informations payeur|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Non structuré|Texte.|Les informations à votre disposition pour activer la correspondance/le rapprochement d’une écriture avec les articles que le paiement doit régler, telles que les factures commerciales dans un système comptes-clients, sous forme non structurée||6|Désignation|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texte.|Informations supplémentaires sur l’écriture.||16|Informations transaction|  

 Les articles dans le nœud **Ntry** qui sont importés dans [!INCLUDE[prod_short](includes/prod_short.md)] mais ne sont associés à aucun champ sont stockés dans la table **Définition colonne échange comptabilité**. Les utilisateurs peuvent afficher ces éléments des pages **Feuille rapprochement bancaire**, **Lettrage paiement** et **Rapprochement bancaire** en choisissant l’action **Détails lignes de relevé bancaire**. Pour plus d’informations, voir [Rapprocher les paiements à l’aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]
> Dans une importation de relevés bancaires CAMT, [!INCLUDE[prod_short](includes/prod_short.md)] s’attend à ce que chaque transaction soit unique, ce qui signifie que le champ **ID transaction** qui provient de la balise *Stmt/Ntry/NtryDtls/TxDtls/Refs/EndToEndId* dans le fichier CAMT, doit être unique dans le rapprochement du compte bancaire ouvert. Si les informations ne sont pas présentes, [!INCLUDE[prod_short](includes/prod_short.md)] ignore le paiement. Si un rapprochement bancaire antérieur sur le même compte bancaire a été validé avec le même ID de transaction que lors de l’importation en cours, la transaction en cours ne sera pas automatiquement rapprochée, mais elle peut toujours être importée.

## <a name="see-also"></a>Voir aussi

[Configuration de l’échange de données](across-set-up-data-exchange.md)  
[Échanger des données par voir électronique](across-data-exchange.md)  
[Utiliser l’extension AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Utiliser des schémas XML pour préparer des définitions d’échange de données](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Rapprocher les paiements à l’aide de l’application automatique](receivables-how-reconcile-payments-auto-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
