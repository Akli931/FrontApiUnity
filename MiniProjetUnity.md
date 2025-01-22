# Mini-Projet Unity - Application de Connexion et Commentaires

## Description du Projet
Ce projet Unity inclut les fonctionnalités suivantes :
- Connexion et inscription des utilisateurs.
- Affichage des statistiques des utilisateurs dans une interface dédiée.
- Gestion des commentaires via une API JSON.
- Navigation entre trois scènes principales : Connexion, Statistiques, et Commentaires.

## Structure du Projet
### Dossiers principaux
- **Assets/** : Contient les ressources Unity (scripts, prefabs, etc.).
- **API/** : Contient la base de données et les fichiers nécessaires pour exécuter le serveur.

### Scènes
1. **LoginScene** : Scène de connexion et inscription.
2. **StateScene** : Scène affichant les statistiques des utilisateurs.
3. **CommentsScene** : Scène permettant aux utilisateurs de poster et de consulter des commentaires.

## Configuration de l'API
### Prérequis
- Installer Node.js sur votre machine : [Télécharger Node.js](https://nodejs.org/)
- Installer le package `json-server` globalement :
  ```bash
  npm install -g json-server
  ```

### Démarrage du serveur
1. Naviguez dans le dossier `API` :
  
   cd API

2. Assurez-vous que le fichier `db.json` contient les données initiales suivantes :
   ```json
   {
     "users": [
       { "username": "user1", "password": "pass1" },
       { "username": "user2", "password": "pass2" }
     ],
     "comments": []
   }
   ```
3. Lancez le serveur avec la commande suivante :
   ```bash
   json-server --watch db.json --port 3000
   ```
4. L'API sera accessible sur : [http://localhost:3000](http://localhost:3000)

## Fonctionnalités de l'API
- **Route des utilisateurs** :
  - `GET /users` : Récupère la liste des utilisateurs.
  - `POST /users` : Ajoute un nouvel utilisateur.
- **Route des commentaires** :
  - `GET /comments` : Récupère la liste des commentaires.
  - `POST /comments` : Ajoute un nouveau commentaire.




