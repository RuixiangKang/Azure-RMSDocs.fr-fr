---
title: "Types d’applications | Azure RMS"
description: "Cette rubrique traite des types d’applications que vous pouvez choisir de créer avec une gestion des droits."
keywords: 
author: bruceperlerms
ms.author: bruceper
manager: mbaldwin
ms.date: 02/23/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 97169FC3-1395-4433-A632-7B0F020FABFE
audience: developer
ms.reviewer: shubhamp
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 7068e0529409eb783f16bc207a17be27cd5d82a8
ms.openlocfilehash: 22c0525adf64c6b3a7fa4ecd51573aef8e31b5bb


---

# <a name="application-types"></a>Application types (Types d’applications)


Cette rubrique traite des types d’applications que vous pouvez choisir de créer avec une gestion des droits.

Les types d’application suivants sont actuellement pris en charge par Rights Management Services SDK 2.1

## <a name="simple-applications"></a>Applications simples

Une application simple peut être un outil de ligne de commande conçu pour chiffrer un fichier donné. Pour obtenir un exemple d’une application simple avec gestion des droits, consultez notre implémentation de *IPCHelloWorld* dans [Développement de votre application](developing-your-application.md).

### <a name="server-mode-applications"></a>Applications en mode serveur

Le *mode serveur* est conçu pour les applications non interactives qui consomment, protègent ou traitent du contenu protégé par RMS. Un exemple est une application de *protection contre la perte de données* qui s’exécute en tant que service sur un serveur de fichiers et qui protège automatiquement les documents sensibles. Consultez l’[exemple IpcDlp](https://Code.MSDN.Microsoft.Com/IpcDlp-Sample-Application-d30bb99d) pour un exemple de ce type d’application.

Si votre application utilise le *mode serveur*, elle doit s’authentifier auprès du serveur RMS en mode silencieux. Contrairement au *mode client*, RMS SDK 2.1 n’ouvre pas une invite demandant des informations d’identification quand il échoue à s’authentifier en mode silencieux. En outre, lors de l’exécution en *mode serveur*, un manifeste d’application n’est pas nécessaire.

Pour plus d’informations sur la définition du mode de sécurité de l’API, consultez [Définition du mode de sécurité de l’API](setting-the-api-security-mode-api-mode.md).

### <a name="rich-client-applications"></a>Applications clientes enrichies

Une application cliente enrichie permet aux utilisateurs d’afficher et de manipuler des données via une interface utilisateur graphique. Souvent, les données présentées dans cette interface utilisateur sont importantes et sensibles au vol ou à une exposition accidentelle. La prise en charge de la protection des informations améliore généralement les scénarios existants, mais elle n’est pas l’objectif principal du développement de l’application.

L’utilisation de RMS SDK 2.1 avec des applications clientes enrichies vous aide à :

-   Vérifier que ces données sont toujours chiffrées.

-   Empêcher les utilisateurs d’extraire des données à un format non protégé (par exemple pour empêcher l’utilisation du Presse-papiers pour copier et coller).

Microsoft Notepad est une application cliente enrichie simple. Microsoft Office est une application cliente enrichie plus complexe.

Pour plus d’informations sur la protection de votre application, consultez [Comprendre les restrictions d’utilisation](understanding-usage-restrictions.md).

## <a name="related-topics"></a>Rubriques connexes

- [Exemple IpcDlp](https://Code.MSDN.Microsoft.Com/IpcDlp-Sample-Application-d30bb99d)
- [Développement de votre application](developing-your-application.md)
- [Définition du mode de sécurité de l’API](setting-the-api-security-mode-api-mode.md)
- [Comprendre les restrictions d’utilisation](understanding-usage-restrictions.md)

[!INCLUDE[Commenting house rules](../includes/houserules.md)]


<!--HONumber=Jan17_HO1-->


