
# Site e-commerce de pâtisserie

## Présentation du projet

Développement d'une application web e-commerce dédiée à la vente de produits de pâtisserie. Le projet vise à digitaliser le parcours d'achat, de la consultation du catalogue jusqu'à la gestion des commandes, tout en proposant une architecture évolutive, maintenable et adaptée à de futures extensions.

L'objectif est de concevoir une solution pouvant évoluer d'une boutique indépendante vers une plateforme capable de gérer un catalogue plus important, davantage de clients et un volume croissant de commandes.

## Objectifs techniques

- Structurer une application web selon une architecture maintenable.
- Séparer la présentation, la logique métier et l'accès aux données.
- Organiser la gestion des produits, des clients et des commandes.
- Sécuriser les échanges et les opérations sensibles.
- Faciliter les tests, la maintenance et les évolutions fonctionnelles.
- Préparer la solution à une montée en charge progressive.

## Fonctionnalités métier

### 1. Catalogue de produits

- Organiser les produits par catégories.
- Présenter les noms, descriptions, prix et visuels des pâtisseries.
- Gérer la disponibilité des produits selon les fonctionnalités développées.
- Prévoir des mécanismes de recherche, de filtrage et de tri.
- Structurer les données pour faciliter l'évolution du catalogue.

### 2. Panier et commandes

- Gérer la sélection des produits et les quantités.
- Calculer le montant du panier à partir des prix et quantités.
- Contrôler les données transmises lors de la création d'une commande.
- Structurer le processus de commande et le suivi de son statut.
- Prévoir la conservation de l'historique des commandes.

### 3. Gestion des utilisateurs

- Structurer les informations des clients.
- Prévoir l'authentification et la gestion des sessions si elles sont implémentées.
- Séparer les fonctionnalités publiques des fonctionnalités réservées.
- Protéger les données personnelles et contrôler les accès.

### 4. Communication par e-mail

- Prévoir l'envoi de notifications liées aux commandes et aux comptes.
- Configurer un service SMTP ou un fournisseur de messagerie.
- Structurer les modèles de messages selon les événements métier.
- Gérer les erreurs d'envoi et éviter d'exposer les identifiants de messagerie.

## Architecture applicative

Une architecture évolutive peut s'organiser autour des couches suivantes :

- Présentation : interfaces et interactions utilisateur.
- Logique métier : règles de gestion du catalogue, du panier et des commandes.
- Accès aux données : opérations de lecture et d'écriture dans la base.
- Services transverses : messagerie, journalisation et configuration.
- Tests : vérification des règles métier et des fonctionnalités.

Cette séparation limite le couplage entre les composants et facilite leur évolution indépendante.

## Données et persistance

La modélisation peut s'appuyer sur les entités suivantes, selon le périmètre fonctionnel :

- Produit : nom, description, prix, catégorie et disponibilité.
- Catégorie : organisation du catalogue.
- Client : informations nécessaires au compte et à la commande.
- Commande : date, statut, montant et informations de livraison.
- Ligne de commande : produit, quantité et prix appliqué au moment de l'achat.
- Notification : suivi des communications, si cette fonctionnalité est développée.

Les contraintes d'intégrité et la validation des données doivent être prises en compte pour préserver la cohérence des commandes.

## Sécurité

- Valider les données côté serveur.
- Utiliser des requêtes paramétrées ou un ORM pour limiter les risques d'injection SQL.
- Protéger les secrets dans des variables d'environnement.
- Vérifier les autorisations sur les opérations sensibles.
- Appliquer HTTPS en production.
- Éviter de stocker les données de paiement sensibles.
- Journaliser les erreurs sans exposer de données personnelles.

## Tests et qualité

- Tester les règles de calcul du panier et des commandes.
- Vérifier les validations des formulaires.
- Tester les erreurs d'accès aux données et les cas limites.
- Contrôler les droits d'accès aux fonctionnalités sensibles.
- Utiliser Git pour suivre les modifications et faciliter la maintenance.

## Évolutivité et montée en charge

Pour accompagner une augmentation du nombre de visiteurs, de produits et de commandes, plusieurs améliorations peuvent être envisagées :

- Optimiser les requêtes SQL et ajouter des index adaptés.
- Mettre en cache les données du catalogue fréquemment consultées.
- Paginer les listes de produits et les historiques de commandes.
- Externaliser les images et fichiers vers un stockage adapté.
- Traiter les e-mails et tâches longues de manière asynchrone.
- Mettre en place une surveillance des erreurs et des performances.
- Automatiser les tests et les déploiements avec une chaîne CI/CD.
- Conteneuriser l'application si cela correspond à son architecture.
- Mettre en place des sauvegardes et une procédure de restauration.
- Effectuer des tests de charge avant une augmentation importante du trafic.

Ces éléments constituent des pistes d'évolution et ne signifient pas qu'ils sont déjà implémentés.

## Installation

Cloner le dépôt :

```bash
git clone https://github.com/mombouli2402/site-ecommerce-de-patisserie.git
cd site-ecommerce-de-patisserie
```

Installer ensuite les dépendances, configurer la base de données et lancer l'application selon le langage et le framework réellement utilisés.

Les commandes exactes doivent être documentées en fonction des fichiers de configuration du projet.

## Gestion du code source

Dépôt GitHub :
https://github.com/mombouli2402/site-ecommerce-de-patisserie

Git est utilisé pour le versionnement du code et GitHub pour héberger le dépôt.

## Auteur

Mombouli Trinité
GitHub : https://github.com/mombouli2402
