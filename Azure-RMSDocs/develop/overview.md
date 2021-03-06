---
title: "Présentation - RMS SDK 4.2 | Azure RMS"
description: "AD RMS et Azure RMS sont une technologie de protection des informations qui vous aide à protéger les informations numériques contre toute utilisation non autorisée."
keywords: 
author: bruceperlerms
ms.author: bruceper
manager: mbaldwin
ms.date: 02/23/2017
ms.topic: article
ms.prod: 
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: 8A13494E-C1D7-407D-BCD1-A406915EA578
audience: developer
ms.reviewer: shubhamp
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 7068e0529409eb783f16bc207a17be27cd5d82a8
ms.openlocfilehash: 19afce2a84e979ca1a25ec2ff6473dd3d6edd610


---

# <a name="overview"></a>Vue d'ensemble

Microsoft Rights Management SDK 4.2 est une technologie de protection des informations disponible pour plusieurs plateformes.  Elle fournit un Kit de développement logiciel (SDK), ou framework, conçu pour les ordinateurs clients et les appareils, qui a pour objectif d’aider à protéger l’accès et l’utilisation des informations qui circulent entre les applications compatibles avec la gestion des droits. Les SDK pour ces plateformes fournissent une API simple permettant à un développeur d’applications de protéger ou de consommer du contenu numérique, de récupérer des modèles et d’acquérir des stratégies à partir d’un serveur, ainsi que d’autres tâches de gestion des droits.

Pour plus d’informations sur les plateformes actuellement prises en charge, consultez notre portail de documentation de développement pour [Microsoft Rights Management SDK](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md).

Voici quelques-uns des scénarios possibles :

-   Un cabinet juridique veut empêcher que les e-mails sensibles soient imprimés ou transférés sur un appareil mobile.
-   Les développeurs de logiciels de conception et de fabrication assistées par ordinateur veulent limiter l’accès au module de dessin à un petit groupe d’utilisateurs de la division Recherche sans exiger l’utilisation de mots de passe.
-   Les propriétaires d’une application mobile de conception graphique veulent utiliser une même licence permettant la consultation gratuite de copies basse résolution de leurs images, mais exigeant un paiement pour accéder aux versions haute résolution.
-   Les propriétaires d’une bibliothèque de documents en ligne veulent octroyer les droits d’afficher, d’imprimer ou de modifier des documents en fonction de l’identité de l’utilisateur, quand des documents sont téléchargés vers un appareil mobile.
-   Une entreprise veut publier des informations sensibles sur les employés sur un site web interne qui limite les droits de consultation et de modification à certains utilisateurs.

MS RMS SDK 4.2 peut être téléchargé et distribué gratuitement avec votre logiciel tiers, à condition d’en accuser réception et d’accepter son contrat de licence, pour permettre l’accès du client à du contenu dont les droits ont été protégés en utilisant et en déployant des serveurs AD RMS dans votre environnement. Pour plus d’informations, consultez [Prise en main](get-started.md).

## <a name="sdk-highlights"></a>Principales fonctionnalités du SDK


MS RMS SDK 4.2 offre certaines nouvelles fonctionnalités intéressantes, notamment :

-   **API remodelée** : L’API MS RMS SDK 4.2 a été remodelée par souci de simplicité, pour que les développeurs puissent bénéficier d’une API de chiffrement et de déchiffrement simple et transparente assurant la cohérence des comportements RMS avec un minimum d’effort.
-   **Prise en charge hybride pour AD RMS et Azure RMS** : une même application RMS peut consommer et protéger du contenu d’un serveur AD RMS (avec l’extension pour appareil mobile d’AD RMS) et du service Azure RMS. MS RMS SDK 4.2 détecte de manière transparente le point de terminaison approprié que les administrateurs informatiques peuvent configurer.
-   **Utilisez votre propre bibliothèque d’authentification** : en tant que développeur d’applications, vous pouvez choisir la bibliothèque d’authentification utilisée avec MS RMS SDK 4.2. Qu’il s’agisse de la [Bibliothèque d’authentification Azure AD](https://msdn.microsoft.com/library/jj573266.aspx) ou de la bibliothèque personnalisée de votre organisation, MS RMS SDK 4.2 isole la pile d’authentification pour vous permettre de choisir la bibliothèque la plus adaptée à vos besoins.
-   **Utilisez votre propre interface utilisateur** : avec MS RMS SDK 4.2, vous pouvez désormais implémenter votre interface utilisateur personnalisée. Qu’il s’agisse de la protection du contenu, du choix des modèles ou de l’affichage et de la modification des autorisations tout en consommant du contenu protégé, MS RMS SDK 4.2 n’applique aucune interface utilisateur intégrée à vos applications. Si vous le souhaitez, vous pouvez toutefois utiliser les bibliothèques d’interface utilisateur Microsoft RMS pour toutes les plateformes par le biais de notre [compte GitHub](https://github.com/AzureAD/).
-   **Accédez au contenu protégé hors connexion** : avec MS RMS SDK 4.2, les utilisateurs de votre application peuvent accéder au contenu protégé même quand il n’y a aucune connectivité à internet. MS RMS SDK 4.2 met en cache de manière sécurisée les stratégies de consommation du contenu protégé pour que vos utilisateurs puissent accéder hors connexion aux données protégées par RMS.

Utilisez le guide de [Prise en main](get-started.md) pour commencer votre projet d’application d’informations protégées.

## <a name="related-topics"></a>Rubriques connexes

* [SDK Microsoft Rights Management](active-directory-rights-management-services-multi-platform-thin-client-sdk-portal.md)
* [Prise en main](get-started.md)
* [Bibliothèque d’authentification Azure AD](https://msdn.microsoft.com/en-us/library/jj573266.aspx)
* [Compte GitHub](https://github.com/AzureAD/)

[!INCLUDE[Commenting house rules](../includes/houserules.md)]


<!--HONumber=Jan17_HO1-->


