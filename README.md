# Let's Meet

**Let's Meet** est une application web de gestion d'événements permettant de centraliser et d'automatiser l'organisation d'événements (mariages, conférences, anniversaires, séminaires, etc.), en remplaçant les processus manuels souvent source d'erreurs et de désorganisation.

## Contexte

Chacun a déjà organisé ou participé à un événement. Qu'il s'agisse d'un mariage, d'une conférence, d'un anniversaire ou d'un séminaire, une bonne organisation est essentielle pour offrir une expérience agréable et mémorable aux participants.

De nombreux événements sont encore gérés manuellement, ce qui entraîne des erreurs, un manque de coordination et une perte de temps. **Let's Meet** répond à ce besoin en proposant une plateforme centralisée et automatisée.

## Utilisateurs

L'application distingue trois profils d'utilisateurs :

- **Admin** : gère l'ensemble du système (utilisateurs, catégories, événements)
- **Visiteur** : peut consulter les événements sans être authentifié
- **Client** : utilisateur authentifié pouvant créer et participer à des événements

## Fonctionnalités

### Admin
- Gérer les utilisateurs
- Gérer les catégories
- Gérer les événements
- Exporter les clients / événements au format CSV

### Visiteur
- Consulter les événements
- Rechercher un événement par titre
- Filtrer les événements par catégorie

### Client
- S'authentifier
- Créer un événement
- Gérer les participants
- Ajouter des événements aux favoris
- Participer à un événement
- Télécharger l'invitation en PDF *(extension de "Participer à un événement")*
- Recevoir automatiquement un e-mail de confirmation

### Système automatique
- Envoi automatique d'e-mails (confirmation de participation, invitation) via un système d'emails automatisé, déclenché lors de la participation à un événement

> La plupart des actions (création d'événement, participation, favoris, etc.) nécessitent une authentification préalable (`<<include>>` de "s'authentifier"), comme illustré dans le diagramme de cas d'utilisation du projet.

## Architecture technique

| Composant | Technologie |
|---|---|
| Framework Back-end | Laravel |
| Langage | PHP 8.2+ |
| Base de données | MySQL |
| Serveur Web | Apache |
| Gestionnaire de dépendances | Composer |
| Front-end | Blade, HTML5, CSS3, JavaScript, Tailwind CSS |
| Génération de PDF | Laravel DomPDF |
| Contrôle de version | Git / GitHub |
| Environnement de développement | Visual Studio Code |
| Serveur local | XAMPP |

## Prérequis

- PHP >= 8.2
- Composer
- MySQL
- Serveur web (Apache, via XAMPP par exemple)
- Serveur SMTP configuré (pour l'envoi des notifications par e-mail)

## Installation

```bash
# Cloner le dépôt
git clone <url-du-depot>
cd lets-meet

# Installer les dépendances PHP
composer install

# Copier le fichier d'environnement et générer la clé d'application
cp .env.example .env
php artisan key:generate

# Configurer la base de données et le SMTP dans le fichier .env
# DB_DATABASE, DB_USERNAME, DB_PASSWORD
# MAIL_MAILER, MAIL_HOST, MAIL_PORT, MAIL_USERNAME, MAIL_PASSWORD

# Lancer les migrations
php artisan migrate

# Démarrer le serveur local
php artisan serve
```

## Sécurité

L'authentification et la gestion des utilisateurs respectent les bonnes pratiques de sécurité :
- Hachage des mots de passe
- Protection CSRF
- Validation des données côté serveur

## Besoins non fonctionnels

- **Performance** : réponses rapides même avec un volume important d'événements
- **Sécurité** : protection des données utilisateurs et des accès
- **Disponibilité** : accessibilité continue de l'application
- **Ergonomie** : interface simple et intuitive
- **Compatibilité** : fonctionne sur les navigateurs modernes (Chrome, Edge, Firefox, Safari)
- **Maintenabilité** : code structuré et documenté, suivi de versions via Git

## Licence

Projet académique — Zakaria Lemchaouri
