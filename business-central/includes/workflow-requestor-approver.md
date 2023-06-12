---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
---

Lorsque vous configurez des utilisateurs pour les flux de travail approbation, il est important que le même utilisateur ne soit pas à la fois un demandeur et un approbateur dans un groupe d’utilisateurs de flux de travail. Lorsqu’un utilisateur est à la fois demandeur et approbateur, les approbations fonctionnent pour lui comme suit :

* Ses demandes sont toujours approuvées automatiquement.
* S’il y a plusieurs approbateurs, seuls les approbateurs avec un numéro de séquence plus élevé dans le groupe d’utilisateurs du flux de travail peuvent modifier le statut d’une demande en la définissant sur Approuvée. Les approbateurs avec un numéro de séquence inférieur peuvent approuver les demandes, cependant, leurs approbations n’affectent pas le statut d’une demande.