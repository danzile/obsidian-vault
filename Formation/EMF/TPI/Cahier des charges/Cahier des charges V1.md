+-----------------------------------------------------------------------+

| +------------------------------------------+----------------------+ |

| | **Informaticien/-ne CFC** | ![](./images/media/ | |

| | | image1.png){width="1 | |

| | Cahier des charges du travail pratique | .7333366141732283in" | |

| | individuel 2023 (TPI) | height="1. | |

| | | 1616688538932634in"} | |

| +==========================================+======================+ |

| +------------------------------------------+----------------------+ |

+=======================================================================+

+-----------------------------------------------------------------------+

  

**RemoteServerHub**

  

Nom de l'apprenti/-e : Danilo Anzile N° de l'apprenti/-e : 145655

  

+-------------------------------------+--------------------------------+

| Description générale du projet | |

| d'examen : | |

| | |

| L'entreprise hemmer gère environ | |

| 400 sites internet. Chaque | |

| développeur souhaitant se connecter | |

| à l'un de ces sites par SSH doit | |

| aller chercher les données de | |

| connexion dans le dossier du client | |

| puis entrer ces informations dans | |

| un terminal pour s'y connecter. Ces | |

| manipulations font perdre un temps | |

| considérable à chaque connexion. | |

| | |

| Le projet TPI consiste à développer | |

| une interface web permettant de | |

| faciliter la connexion SSH aux | |

| serveurs d'hébergement web favoris. | |

| | |

| Elle permet de récupérer des | |

| identifiants SSH stockés dans le | |

| gestionnaire de mot de passe | |

| « Bitwarden » pour ensuite pouvoir | |

| se connecter au serveur | |

| d'hébergement et ce, directement | |

| depuis l'interface web qui | |

| affichera un invité de commande. | |

+=====================================+================================+

| Domaine du TPI : (Cocher la case de | |

| couleur correspondante) | |

| | |

| ------------ | |

| ----------------------------------- | |

| ☒ Dévelo | |

| ppement ☐ Réseau ☐ Systèmes | |

| --- -------- | |

| ------- --- -------- --- ---------- | |

| | |

| ------------ | |

| ----------------------------------- | |

+-------------------------------------+--------------------------------+

| Tracé d'activité de l'apprenti/-e | |

| durant la dernière année | |

| d'apprentissage : | |

| | |

| Danilo réalise un stage de longue | |

| durée auprès de l'entreprise | |

| hemmer.ch sa à Fribourg. | |

+-------------------------------------+--------------------------------+

| **Coordonnées de l'apprenti/-e :** | |

| | |

| E-Mail : danilo@hemmer.ch\ | |

| Tél : 0799388205\ | |

| Prénom : Danilo\ | |

| Nom : Anzile\ | |

| Adresse : hemmer.ch sa\ | |

| Rue du Criblet 9\ | |

| 1700 Fribourg | |

+-------------------------------------+--------------------------------+

| **Le supérieur professionnel** | **Lieu et Date** |

| | |

| Jean-Baptiste Hemmer | Fribourg, le 17 février 2023 |

+-------------------------------------+--------------------------------+

  

-----------------------------------------------------------------------

  

-----------------------------------------------------------------------

  

Table des matières

  

1 Donnée du problème [3](#donnée-du-problème)

  

2 Formulation du mandat -- état désiré

[3](#formulation-du-mandat-état-désiré)

  

2.1 Description et objectifs du projet

[3](#description-et-objectifs-du-projet)

  

2.2 Exigences fonctionnelles [4](#exigences-fonctionnelles)

  

2.3 Analyse [5](#analyse)

  

2.4 Conception [5](#conception)

  

2.5 Réalisation [5](#réalisation)

  

3 Infrastructure nécessaire [5](#infrastructure-nécessaire)

  

4 Connaissances préalables [5](#connaissances-préalables)

  

5 Travaux préparatoires [5](#travaux-préparatoires)

  

6 Standards d'entreprise [5](#standards-dentreprise)

  

7 Documentation obligatoire [6](#documentation-obligatoire)

  

8 Critères d'évaluation [7](#critères-dévaluation)

  

9 Délais [7](#délais)

  

# Donnée du problème

  

L'entreprise hemmer utilise plusieurs serveurs pour stocker les sites

internet de ses clients. Chaque site a son propre identifiant et mot de

passe pour accéder à sa session SSH. Actuellement, toutes ces données

sont stockées dans des documents pdf spécifiques à chaque site (données

techniques).

  

L'idée du projet est d'utiliser un système pour centraliser les données

et faciliter l'accès aux serveurs grâce à une interface web qui récupère

les identifiants sur le gestionnaire de mots de passe Bitwarden.

  

Le TPI va se concentrer principalement sur cette interface web en local

qui peut être déployée sur chaque poste de travail en utilisant une

image docker.

  

# Formulation du mandat -- état désiré

  

## Description et objectifs du projet

  

Démarrage du projet et mise en place d\'un espace de développement en

local à l\'aide de « docker » et de « composer ». Création d\'un nouveau

projet dans « git » pour le développement du TPI.

  

Récupération des identifiants sur Bitwarden en utilisant l'api « Vault

Management API » qui est fournie. Afficher la liste des serveurs du côté

client.

  

## Architecture du projet

  

Pour ce projet, l'idée est d'utiliser une image docker afin de faciliter

le déploiement sur les postes de travail. Dans cette image docker, il y

aura deux services qui vont être déployés :

  

- une base de données contenant notamment les services Bitwarden liés

à l'image.

  

- un serveur web.

  

Le container serveur Web sera divisé en deux parties :

  

- le frontend qui sera basé sur du HTML5, CSS/Bootstrap et Javascript.

  

- le backend qui sera faite en utilisant Symfony comme Framework PHP.

  ![](./images/media/image2.png){width="4.0078740157480315in"

height="2.9291338582677167in"}Le container pour la base de données

utilisera MariaDB.

  

En ce qui concerne Bitwarden, une instance est déjà mise en place sur un

serveur chez hemmer et sera utiliser au travers d'une API.

  

Pour la partie frontend, voici un exemple de masque de l'application web

:

  

Vue du tableau de bord avec recherche / sélection d'un site (ici

hemmer.ch)

  

Les sources sont les divers connexions au API de Bitwarden que l'on peut

avoir.

  

![](./images/media/image3.png){width="6.499437882764655in"

height="4.252661854768154in"}

  

Au clic, ouverture d'un terminal dans l'application permettant l'accès

au serveur

  

![](./images/media/image4.png){width="6.4781616360454946in"

height="2.1428641732283467in"}

  

Mise en place d'une page de paramètres permettant l'ajout de différentes

options

  

![](./images/media/image5.png){width="6.3936165791776025in"

height="1.7241918197725283in"}

  

## Exigences fonctionnelles

  

+-------------+----------------------------------+--------+----------+

| **Exigence | **Description** | **Prio | * |

| fonc | | rité** | *Temps** |

| tionnelle** | | | |

| | | Haute | ** |

| | | | estimé** |

| | | M | |

| | | oyenne | (jours) |

| | | | |

| | | Basse | |

+=============+==================================+========+==========+

| Gestion de | Démarrage du projet et mise en | Haute | 0.5 jour |

| projet | place de la documentation. | | |

+-------------+----------------------------------+--------+----------+

| Analyse | Analyse des besoins pour le bon | Haute | 1 jour |

| | fonctionnement du projet. | | |

+-------------+----------------------------------+--------+----------+

| Do | Documentation du projet et des | Haute | 2 jours |

| cumentation | étapes réalisées. | | |

+-------------+----------------------------------+--------+----------+

| Technique | Mise en place de l'architecture | Haute | 0.5 jour |

| | de la base de données pour | | |

| | stocker les différents comptes | | |

| | Bitwarden. | | |

+-------------+----------------------------------+--------+----------+

| Technique | Réussir à se connecter à un | Haute | 0.5 jour |

| | serveur distant en SSH. | | |

+-------------+----------------------------------+--------+----------+

| Technique | Récupérer les identifiants de | Haute | 1 jour |

| | chaque site sur Bitwarden. | | |

+-------------+----------------------------------+--------+----------+

| Technique | Création de l'interface | Haute | 1 jour |

| | utilisateur | | |

+-------------+----------------------------------+--------+----------+

| Technique | Avoir un retour de la session | Haute | 1.5 jour |

| | SSH directement depuis | | |

| | l'interface du client. | | |

+-------------+----------------------------------+--------+----------+

| Technique | Soumettre des commandes depuis | M | 1 jour |

| | l'interface utilisateur vers la | oyenne | |

| | session SSH | | |

+-------------+----------------------------------+--------+----------+

| Technique | Déployer le projet sur une image | M | 0.5 jour |

| | docker | oyenne | |

+-------------+----------------------------------+--------+----------+

| Technique | Exporter / importer la base de | Basse | 0.5 jour |

| | données | | |

+-------------+----------------------------------+--------+----------+

| Technique | Ajouter plusieurs entrées | Basse | 0.5 jour |

| | Bitwarden | | |

+-------------+----------------------------------+--------+----------+

  

## Analyse

  

Cette phase de travail permet d'analyser les besoins tels qu'ils ont été

décrits dans la donnée du problème, en les représentant par des

diagrammes ou schémas adéquats.

  

Durant la phase d'analyse, l'apprenti/-e accomplit les tâches

suivantes :

  

- Mise en place d'un diagramme de fonctionnement

  

- Mise en place d'un diagramme de la structure du projet

  

- Documenter l'analyse

  

## Conception

  

Durant la phase de conception, l'apprenti/-e accomplit les tâches

suivantes :

  

- Documentation

  

- Planifier les tests fonctionnels

  

- Documenter la conception

  

## Réalisation

  

Durant la phase de réalisation, l'apprenti/-e accomplit les tâches

suivantes :

  

- Mise en place des outils de développement

  

- Création d'une nouvelle branche sur git pour la création du projet

  

- Mise en place de l'architecture docker nécessaire pour l'application

web

  

- Création de la base de données

  

- Mise en place de la vue frontend

  

- Mise en place du backend

  

- Communication avec l'API de Bitwarden

  

- Connexion au serveur en SSH via une interface

  

# Infrastructure nécessaire

  

Pour la réalisation du projet, l'apprenti/-e disposera de

l'infrastructure suivante :

  

- Toute l'infrastructure de l'entreprise telle qu'utilisée au

quotidien

  

- L'aide de ses collègues de travail, à sa demande

  

- Toute aide externe souhaitée / nécessaire

  

# Connaissances préalables

  

- HTML5

  

- CSS

  

- PHP / Symfony

  

- Composer

  

- MySQL

  

- Git

  

- Docker

  

# {#section .unnumbered}

  

# Travaux préparatoires

  

- Renseignement sur les outils nécessaires.

  

- Intégration de l'API Bitwarden

  

- Exécution de commandes SSH depuis l'interface web

  

- Affichage sur l'interface web de la réponse en SSH

  

- Structure du projet

  

# {#section-1 .unnumbered}

  

# Standards d'entreprise

  

- Utilisation de Bitwarden

  

- Utilisation de Git et composer

  

- Utilisation de Docker

  

- Notation des heures sur Périclès

  

# Documentation obligatoire

  

A la fin du projet, l'apprenti/-e doit fournir les documents suivants :

  

**Une planification**

  

Cette planification doit être réalisée au début du projet avant toute

autre action (selon modèle fourni). Elle décrit les étapes importantes

du projet ainsi que la durée estimée correspondante. Elle doit être

validée par le supérieur professionnel.

  

**Un journal de travail**

  

Ce document décrit les diverses étapes et activités liées au projet

(selon modèle fourni).

  

**Une documentation d'analyse**

  

Ce document détermine les exigences et contraintes du projet et permet

la justification des choix pour la réalisation du travail demandé. Ce

document est composé de :

  

1. Résumé

  

```{=html}

<!-- -->

```

1. Maquette

  

2. Diagramme d'utilisation

  

**Une documentation de réalisation**

  

La documentation de réalisation a pour objectif de faciliter la

maintenance et doit contenir les informations suivantes :

  

1. Conception (Diagramme d'interactions pour les cas d'utilisation

majeurs)

  

```{=html}

<!-- -->

```

3. Implémentation / réalisation (Descente de code)

  

4. Tests fonctionnels

  

5. Problèmes rencontrés

  

**Une documentation d'utilisation**

  

Ce document a pour objectif de permettre à l'utilisateur de se former

d'une manière autodidacte et doit contenir les informations suivantes :

  

1. Comment mettre en place une instance sur son propre poste de travail

  

2. Comment rajouter une nouvelle connexion à Bitwarden

  

**Un Web Summary**

  

Ce document a pour objectif de présenter le projet de manière succincte.

  

**La remise de la documentation**

  

La documentation est remise selon les instructions du manuel ICT-FR,

partie C, point 1.9.1 « Périmètre du rapport, Tips ».

  

Le manuel est disponible dans PkOrg sous : Documents Documents pour

tous :

  

<http://manuel.ict-fr.ch>

  

# Critères d'évaluation

  

http://criteres.ict-fr.ch

  

Compétences professionnelles globales (selon la grille d'appréciation)

  

Résultat et efficience

  

1. **Solution / Produit** (selon la grille d'appréciation)

  

2. **Critères spécifiques au projet**

  

- **Critère n° 1**

  

- **Critère n° 2**

  

- **Critère n° 3**

  

- **Critère n° 4**

  

- **Critère n° 5**

  

- **Critère n° 6**

  

- **Critère n° 7**

  

3. **Documentation** (selon la grille d'appréciation)

  

4. **Journal de travail** (selon la grille d'appréciation)

  

Présentation et entretien professionnel (selon la grille

d'appréciation)[\

]{.underline}

  

# Délais

  

Le projet y compris la remise du projet aux experts se terminera le

**date** à **heure**. Le dernier délai pour la présentation du projet

est fixé au 21 juin 2023 à 12:00.

  

La documentation est déposée sur PkOrg dans les temps.