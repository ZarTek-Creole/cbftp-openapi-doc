# Collection Postman en Français

## Introduction

Cette page fournit des instructions sur l'utilisation de la collection Postman en français pour tester l'API CBFTP.

## Importer la Collection

1. Ouvrez Postman.
2. Cliquez sur **Import** dans le coin supérieur gauche.
3. Sélectionnez l'onglet **Upload Files**.
4. Choisissez le fichier `postman_collection_fr.json` et importez-le.

## Utilisation de la Collection

Une fois la collection importée, vous verrez une liste de requêtes organisées par catégories (Sites, SpreadJobs, TransferJobs, etc.). Vous pouvez exécuter chaque requête pour tester les différents endpoints de l'API CBFTP.

### Exemple de Requête

Pour exécuter une requête, suivez ces étapes :

1. Sélectionnez une requête dans la collection (par exemple, **GET /sites**).
2. Cliquez sur **Send** pour envoyer la requête.
3. Consultez la réponse dans le panneau de droite.

### Configuration de l'Environnement

Assurez-vous de configurer l'environnement Postman avec les bonnes variables (par exemple, l'URL de base de l'API, les informations d'authentification, etc.). Vous pouvez créer un nouvel environnement en cliquant sur l'icône d'engrenage en haut à droite et en sélectionnant **Manage Environments**.

## Remarques

- Si vous utilisez un certificat auto-signé, désactivez la vérification SSL dans les paramètres de Postman (Settings -> General -> **SSL certificate verification: OFF**).
- Consultez la documentation de l'API pour plus de détails sur les endpoints et les paramètres disponibles.

## Ressources

- [Documentation de l'API CBFTP (FR)](../cbftp-openapi_fr.yaml)
- [Collection Postman (FR)](../../postman_collection_fr.json)
