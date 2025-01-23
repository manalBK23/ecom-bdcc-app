Voici un modèle de README GitHub pour ton projet en tant qu'étudiant ayant réalisé ce travail pratique sur Keycloak et la sécurisation d'une architecture micro-service Spring Angular avec Keycloak :

---

# Projet TP - Sécurisation d'une architecture avec Keycloak

## Description
Ce projet a pour but de sécuriser une architecture micro-service basée sur Spring et Angular à l'aide de Keycloak, un outil d'authentification et de gestion des utilisateurs. Le projet a été réalisé en deux parties : 

1. **Partie 1 :** Installation et configuration de Keycloak, gestion des utilisateurs et des rôles.
2. **Partie 2 :** Sécurisation d'une architecture micro-service Spring Angular avec Keycloak.

## Partie 1 : Installation et Configuration de Keycloak

### Étapes réalisées

1. **Télécharger Keycloak 19 :**
   - Télécharger la dernière version de Keycloak depuis [ici](https://www.keycloak.org/downloads).

2. **Démarrer Keycloak :**
   - Décompresser le fichier téléchargé et démarrer le serveur Keycloak en exécutant la commande suivante :
     ```bash
     ./bin/standalone.sh
     ```

3. **Créer un compte Admin :**
   - Lors de la première exécution, créer un compte Admin via l'interface Web de Keycloak accessible sur `http://localhost:8080`.

4. **Créer une Realm :**
   - Créer une nouvelle `Realm` pour organiser les utilisateurs, clients et rôles.

5. **Créer un client à sécuriser :**
   - Ajouter un client qui sera sécurisé par Keycloak. Ce client peut être une application web ou une API.

6. **Créer des utilisateurs :**
   - Créer des utilisateurs qui auront accès à l'application sécurisée.

7. **Créer des rôles :**
   - Définir des rôles d'utilisateur (par exemple : `admin`, `user`) pour gérer les permissions dans l'application.

8. **Affecter les rôles aux utilisateurs :**
   - Assigner des rôles aux utilisateurs pour définir leur niveau d'accès.

### Tests avec PostMan

1. **Tester l'authentification avec le mot de passe :**
   - Utiliser Postman pour envoyer une requête d'authentification avec un nom d'utilisateur et un mot de passe.

2. **Analyser les contenus des deux JWT Access Token et Refresh Token :**
   - Décoder les tokens JWT pour examiner les informations qu'ils contiennent (ex : `iss`, `sub`, `exp`).

3. **Tester l'authentification avec le Refresh Token :**
   - Tester la possibilité d'obtenir un nouveau token d'accès en utilisant le Refresh Token.

4. **Tester l'authentification avec Client ID et Client Secret :**
   - Utiliser l'authentification client avec un `client_id` et un `client_secret` pour récupérer un access token.

5. **Changer les paramètres des Tokens Access Token et Refresh Token :**
   - Modifier la configuration des tokens pour ajuster leur durée de validité, signature, etc.

## Partie 2 : Sécurisation d'une architecture Micro-Service Spring Angular avec Keycloak

### Étapes réalisées

Dans cette partie, nous avons sécurisé une architecture micro-service basée sur Spring et Angular avec Keycloak. Voici le lien vers le tutoriel que j'ai suivi pour cette partie :  
[Sécuriser une architecture micro-service Spring Angular avec Keycloak](https://www.youtube.com/watch?v=33B_nQgQaSs)

1. **Configurer Keycloak pour Spring Boot :**
   - Intégrer Keycloak avec l'application Spring Boot pour sécuriser les endpoints via OAuth2 et les JWT.

2. **Configurer Keycloak pour Angular :**
   - Utiliser la bibliothèque `keycloak-angular` pour interagir avec Keycloak depuis le frontend Angular et gérer l'authentification et l'autorisation.

3. **Protection des micro-services :**
   - Appliquer des contrôles d'accès aux API backend (Spring) en fonction des rôles définis dans Keycloak.

4. **Redirection et gestion des sessions :**
   - Gérer la redirection des utilisateurs après authentification et la gestion des sessions sur le frontend Angular.

## Technologies utilisées

- **Keycloak 19** : Système de gestion des utilisateurs et d'authentification.
- **Spring Boot** : Framework pour la création des micro-services.
- **Angular** : Framework frontend pour la création de l'application.
- **Postman** : Outil de test d'API pour tester l'authentification et les tokens JWT.

## Prérequis

- Keycloak installé et en cours d'exécution.
- Java 11 ou plus pour Spring Boot.
- Node.js et Angular CLI pour le frontend.
- Postman pour les tests d'API.

## Lancer l'application

### Démarrer Keycloak
1. Téléchargez et exécutez Keycloak comme indiqué dans la Partie 1.

### Démarrer le Backend (Spring Boot)
1. Clonez ce repository et ouvrez le projet Spring Boot dans votre IDE (ex : IntelliJ).
2. Démarrez l'application Spring Boot via la commande suivante :
   ```bash
   ./mvnw spring-boot:run
   ```

### Démarrer le Frontend (Angular)
1. Clonez ce repository et ouvrez le projet Angular dans votre IDE (ex : VSCode).
2. Installez les dépendances :
   ```bash
   npm install
   ```
3. Démarrez l'application Angular :
   ```bash
   ng serve
   ```


N'hésite pas à ajuster les sections spécifiques si nécessaire, mais cela devrait couvrir l'ensemble du travail réalisé.
