# Let's Meet

> Projet en cours de conception.

## Idée générale

**Let's Meet** est une application web de gestion d'événements. L'objectif est de remplacer la gestion manuelle des événements (mariages, conférences, anniversaires, séminaires, etc.), source d'erreurs et de perte de temps, par une plateforme centralisée permettant de créer, organiser et suivre des événements de bout en bout : création de l'événement, gestion des participants, envoi automatique des invitations par e-mail et génération de PDF.

## Technologies

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

## Diagramme de cas d'utilisation

<img width="897" height="732" alt="cas-utilisations" src="https://github.com/user-attachments/assets/b89ccce9-d1b5-47fc-9840-cbef88cce26a" />

Le diagramme définit trois acteurs et leurs interactions avec le système :

**Admin**
Responsable de l'administration du système. Il gère les utilisateurs, les catégories et les événements, et peut exporter la liste des clients/événements au format CSV. Toutes ces actions incluent une authentification préalable (`<<include>> s'authentifier`).

**Visiteur**
Utilisateur non authentifié. Il peut consulter les événements, effectuer une recherche par titre ou filtrer par catégorie, sans avoir besoin de se connecter.

**Client**
Utilisateur authentifié disposant des droits les plus étendus côté utilisateur final. Il peut créer un événement, gérer les participants, ajouter des événements à ses favoris et participer à un événement. Ces actions nécessitent également une authentification (`<<include>>`).



Projet personnel — Zakaria Lemchaouri
