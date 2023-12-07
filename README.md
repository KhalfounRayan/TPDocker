# Projet de Réseautage Docker pour Prestashop

Ce README décrit le déploiement d'une application e-commerce Prestashop à l'aide de Docker, en se concentrant sur les aspects de réseautage entre les conteneurs de l'application.

## Table des Matières
1. [Introduction](#introduction)
2. [Architecture](#architecture)
3. [Aperçu des Tâches](#aperçu-des-tâches)
   - [Tâche 1 : Déploiement dans un Réseau](#tâche-1-déploiement-dans-un-réseau)
   - [Tâche 2 : Création de Réseaux Avancés](#tâche-2-création-de-réseaux-avancés)
4. [Exigences de Soumission](#exigences-de-soumission)
5. [Membres de l'Équipe](#membres-de-léquipe)

## Introduction

L'objectif de ce projet est de déployer une application e-commerce Prestashop en utilisant des conteneurs Docker. L'application se compose d'un site web frontend et d'une base de données pour stocker les données persistantes.

## Architecture

![Diagramme d'Architecture](archi.png)

Le diagramme ci-dessus représente l'architecture réseau pour le déploiement de l'application Prestashop.

## Aperçu des Tâches

### Tâche 1 : Déploiement dans un Réseau

Déployer l'application de manière à ce que le conteneur du site web frontal et le conteneur de la base de données puissent communiquer en utilisant leurs noms.

### Tâche 2 : Création de Réseaux Avancés

- Créer deux réseaux avec les CIDR spécifiés dans les schémas : `ynov-frontend-network` et `ynov-backend-network`.
- Utiliser l'option `--subnet` pour ajouter un sous-réseau lors de la création des réseaux.
- Mettre en place un conteneur intermédiaire, tel qu'un `gateway` ou `router`, et le connecter aux deux réseaux.
- Configurer la table de routage dans le `gateway` avec la commande `ip route add <FROM_CIDR_REPLACE_ME> via <GATEWAY_IP_FROM_EACH_NETWORK_SIDE>` pour les deux réseaux.

## Exigences de Soumission

- Produire un PDF de votre travail avec des captures d'écran et des descriptions détaillées.
- Créer un dépôt GitHub public et soumettre l'URL de ce dépôt sur Moodle.
- Rédiger un fichier README propre avec une table des matières, des sections, et des captures d'écran démontrant votre travail.

## Membres de l'Équipe

- **Membre 1** : Nabil Hatri
- **Membre 2** : Rayan Khalfoun

