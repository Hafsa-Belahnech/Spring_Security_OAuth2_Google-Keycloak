# TP 13 : Intégration OAuth2 et OpenID Connect (Google & Keycloak)

Ce projet pratique porte sur la mise en œuvre de l'authentification déléguée dans une application **Spring Boot**. L'objectif est de sécuriser l'accès en utilisant des fournisseurs d'identité externes (IdP) via les protocoles **OAuth2** et **OIDC**.

## Objectifs
*   **Compréhension d'OAuth2/OIDC** : Maîtrise des concepts d'Access Token (autorisation) et d'ID Token (identité).
*   **Configuration Client OAuth2** : Paramétrage de Spring Security pour interagir avec des fournisseurs externes.
*   **Intégration Multi-Fournisseurs** : Mise en place de l'authentification via **Google Identity** et **Keycloak** (solution auto-hébergée).
*   **Gestion du Profil Utilisateur** : Extraction et affichage des informations (nom, email, photo) à partir du jeton d'identité.
*   **Flux d'Autorisation** : Compréhension du cycle de redirection, des *scopes* et du mécanisme de *callback*.

## Configuration du Fournisseur (Exemple Google)

Pour que l'application fonctionne, les identifiants suivants doivent être configurés dans le fichier `application.yml` :

1.  **Client ID** et **Client Secret** obtenus via la Google Cloud Console.
2.  **URI de redirection** autorisée : `http://localhost:8080/login/oauth2/code/google`

## Outils et Technologies utilisés
- IntelliJ, Maven, Spring Boot, JDK +17
- Dépendances : Spring Web, Spring Security, OAuth2 Client, Thymeleaf, Lombok

## Étapes de Réalisation

1.  **Initialisation** : Création du projet avec la dépendance `spring-boot-starter-oauth2-client`.
2.  **Configuration Google** : Création du projet sur Google Cloud et récupération des identifiants.
3.  **Flux d'Authentification** : Observation de la redirection automatique vers la page de login du fournisseur.
4.  **Récupération de l'Identity** : Utilisation de l'annotation `@AuthenticationPrincipal` pour accéder aux données utilisateur.
5.  **Variante Keycloak** : Configuration d'un royaume (*realm*) et d'un client local pour tester le SSO.
6.  **Sécurisation des Endpoints** : Définition des règles d'accès dans la classe de configuration de sécurité.

## Captures d'écran 
# Configuration dans la console de Google loud
<img width="946" height="275" alt="image" src="https://github.com/user-attachments/assets/45850217-2857-4dbe-8f61-36597448cd8d" />
<img width="908" height="774" alt="image" src="https://github.com/user-attachments/assets/26312431-c899-4970-837d-9ca495d8eccd" />
<img width="868" height="714" alt="image" src="https://github.com/user-attachments/assets/6cf9fb96-07be-4cd5-a1c6-0a5ab4a93199" />

# Initialisation de Spring Boot 
<img width="1600" height="716" alt="image" src="https://github.com/user-attachments/assets/73fdc31e-e954-44c6-bc67-0584566ce760" />

# La première page après authentification 
<img width="952" height="336" alt="image" src="https://github.com/user-attachments/assets/b010f27e-748a-416d-a052-cbcf613a4e27" />

# Personnalisation des Pages et Vues 

<img width="1600" height="456" alt="image" src="https://github.com/user-attachments/assets/9ee37da4-e79c-4d2d-8d96-ed6ec483ea55" />

**Login**
<img width="1600" height="476" alt="image" src="https://github.com/user-attachments/assets/d071007f-25f9-4950-98d5-a6bfad9f2ec9" />

**Profil**
<img width="1600" height="432" alt="image" src="https://github.com/user-attachments/assets/8a547e86-da6b-419c-9ba1-b559ab99b346" />

