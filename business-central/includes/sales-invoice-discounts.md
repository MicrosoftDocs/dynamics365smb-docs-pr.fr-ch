---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
---
Après avoir ajouté tous les articles sur les lignes, vous pouvez calculer la remise sur facture pour l’ensemble du document vente en choisissant l’action **Calculer remise facture**.

La remise est calculée sur la base de toutes les lignes du document vente où la case **Autoriser remise facture** est cochée. Par défaut, les remises facture sont autorisées. Toutefois, les lignes avec des frais annexes, par exemple, ne sont pas incluses dans le calcul de la remise facture. Pour appliquer une remise à ces lignes, entrez une valeur dans le champ **Montant remise ligne** sur les lignes.  

> [!NOTE]
> Par défaut, les champs **Autoriser remise facture** et **Montant remise ligne** sont cachés sur les lignes. Si les champs ne sont pas disponibles, vous pouvez les ajouter en personnalisant la page. Pour plus d’informations, voir [Personnaliser votre espace de travail](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

> [!TIP]
> Si le champ **Calculer remise facture** est sélectionné sur la page **Paramètres ventes**, la remise facture est calculée automatiquement. Le moment du calcul diffère selon le type de document vente que vous utilisez.
>
> Si vous utilisez une commande client, la remise est calculée quand vous ajoutez une ligne. Pour tous les autres documents vente, tels que les factures vente, la remise est calculée quand vous effectuez l’une des actions suivantes :
>
> * Afficher les statistiques
> * Afficher une impression test
> * Imprimer
> * Comptabilisation

Vous définissez les conditions de remise facture pour un client sur la page **Remise facture client**. Le code devise du document vente est utilisé pour trouver les conditions remise facture de la devise.

Si vous n’avez pas défini de remises facture pour les devises étrangères, les conditions de remise sur la page **Remises facture client** sont utilisées pour calculer la remise. Le calcul utilise votre devise locale et le taux de change en vigueur à la date comptabilisation du document.
