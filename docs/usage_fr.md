# Usage en Français

Cette section explique comment configurer l’API, les endpoints majeurs, etc.

## Endpoints Principaux
- `/sites` ...
- `/spreadjobs` ...
- ...

## Instructions Générales

Pour utiliser l'API CBFTP, vous devez inclure l'authentification HTTP Basic (username:password) encodée en Base64 dans toutes les requêtes. Par exemple, si le mot de passe est `bestpass`, l'en-tête doit être :

```
Authorization: Basic OmJlc3RwYXNz
```

### Exemple d'appels REST

#### Lister les sites

```bash
curl -k -u :bestpass https://localhost:55477/sites
```

#### Envoyer une commande brute

```bash
curl -k -u :bestpass -X POST https://localhost:55477/raw -d '{
  "command": "site deluser me",
  "sites": ["SITE1"]
}'
```

#### Ajouter un site

```bash
curl -k -u :bestpass -X POST https://localhost:55477/sites -d @newsite.json
```

## Méthodes HTTP

- **GET** : Lire une ressource existante
- **POST** : Créer une nouvelle ressource
- **PATCH** : Mettre à jour une ressource existante
- **DELETE** : Supprimer une ressource

## Endpoints Principaux

- `/sites` (lister/ajouter) ; `/sites/{siteName}` (détails/modifier/supprimer)
- `/sites/{siteName}/sections` (lister/ajouter) ; `/sites/{siteName}/sections/{sectionName}` (détails/modifier/supprimer)
- `/raw` : Exécuter une commande brute (`POST`)
- `/spreadjobs` (lister/créer) ; `/spreadjobs/{jobName}` (détails/abandon)
- `/transferjobs` (lister/créer) ; `/transferjobs/{transferId}` (détails/abandon)
- `/path` : Lister ou supprimer un répertoire
- `/file` : Récupérer le contenu d’un fichier
- `/info` : Informations build, stats, configuration
