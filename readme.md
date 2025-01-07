<!--
 README Bilingue : FR / EN - Amélioré pour GitHub
 Inclut validation, versioning, exemples, liens, etc.
-->

# CBFTP OpenAPI Documentation

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![OpenAPI Validation](https://img.shields.io/github/actions/workflow/status/ZarTek-Creole/cbftp-openapi-doc/validate.yml?label=OpenAPI%20Validation)](#) 
<!-- Si vous mettez en place un workflow GitHub Actions "validate.yml" pour Swagger CLI. -->
[![OpenAPI Version](https://img.shields.io/badge/OpenAPI-3.0.3-orange.svg)](#)

> **Langues / Languages** :
> - [Français](#fr)
> - [English](#en)

---

## <a name="fr"></a>FR - Spécification OpenAPI

### Description

Ce dépôt [**cbftp-openapi-doc**](https://github.com/ZarTek-Creole/cbftp-openapi-doc) contient la **spécification OpenAPI** du projet **CBFTP** en **deux langues** :

- **[`cbftp-openapi_fr.yaml`](./cbftp-openapi_fr.yaml)** : Version **française**  
- **[`cbftp-openapi_en.yaml`](./cbftp-openapi_en.yaml)** : Version **anglaise**

#### Portée de la documentation

1. **Endpoints REST** (ex.: `/sites`, `/spreadjobs`, `/transferjobs`, etc.)  
2. **Schémas de données** (Site, Section, SkiplistRule, SpreadJob, etc.)  
3. **Sécurité** (HTTP Basic Auth) et notes sur l’API UDP (hors-scope direct d’OpenAPI)  
4. **Paramètres TLS**, **limites**, etc.

#### Version et Changelog

- La variable `info.version` dans les fichiers YAML indique la **version** de la spec (ex. `1.3.0`).  
- Nous utilisons actuellement **OpenAPI 3.0.3** pour maximiser la compatibilité avec Swagger Editor.  
- Vous pouvez suivre l’évolution des modifications dans un fichier [CHANGELOG.md](./CHANGELOG.md) *(à créer)* et/ou via des **tags** (e.g. `v1.3.0`) dans GitHub.

### Comment Visualiser

1. **Swagger Editor**  
   - Allez sur [editor.swagger.io](https://editor.swagger.io/).  
   - Collez le contenu de `cbftp-openapi_fr.yaml` pour une documentation interactive **en français**.

2. **Redoc CLI**  
   ```bash
   npm install -g redoc-cli
   redoc-cli serve cbftp-openapi_fr.yaml
   ```
   Rendez-vous sur `http://127.0.0.1:8080` pour consulter la doc localement.

3. **Docker + Swagger UI**  
   - Récupérez l’image [swaggerapi/swagger-ui](https://hub.docker.com/r/swaggerapi/swagger-ui).  
   - Montez votre fichier YAML dans le container, puis accédez-y dans votre navigateur.

4. *(Facultatif)* **GitHub Pages**  
   - Vous pouvez héberger la documentation sur **GitHub Pages** pour un accès direct en ligne (ex.: `https://votre-user.github.io/cbftp-openapi-doc`).  
   - Il suffit de générer les pages HTML via [Redoc](https://redocly.com/redoc/) ou [Swagger UI](https://swagger.io/tools/swagger-ui/) et de les **publier** sur la branche `gh-pages`.

### Validation et Tests Locaux

- Installez **Swagger CLI** (ou **OpenAPI CLI**) :
  ```bash
  npm install -g swagger-cli
  ```
- Validez la syntaxe :
  ```bash
  swagger-cli validate cbftp-openapi_fr.yaml
  swagger-cli validate cbftp-openapi_en.yaml
  ```
- Vous pouvez configurer un **GitHub Action** (ex.: `.github/workflows/validate.yml`) pour effectuer ces vérifications à chaque *push* ou *pull request*.

### Exemples d’Appels (REST)

<details>
  <summary>Exemple cURL pour récupérer la liste des sites</summary>

```bash
curl -k -u :bestpass https://localhost:55477/sites
```
</details>

<details>
  <summary>Exemple de Postman Collection</summary>

Vous pouvez importer un fichier `postman_collection.json` contenant divers appels préconfigurés (auth Basic, URLs, etc.). Pensez à inclure **`-k`** ou désactiver la vérification SSL dans Postman (car CBFTP utilise un certificat auto-signé).

</details>

### Contribution

1. **Forkez** ce dépôt et créez une **branche** (ex.: `feat/ajout-endpoint-sections`).  
2. Modifiez `cbftp-openapi_fr.yaml` ou `cbftp-openapi_en.yaml` selon la langue voulue.  
3. Validez le YAML avec `swagger-cli` ou [editor.swagger.io](https://editor.swagger.io/).  
4. Ouvrez une **pull request** pour discuter des changements.  

*(Voir [CONTRIBUTING.md](./CONTRIBUTING.md) si vous souhaitez détailler davantage la procédure de contribution.)*

---

## <a name="en"></a>EN - OpenAPI Specification

### Description

This repository [**cbftp-openapi-doc**](https://github.com/ZarTek-Creole/cbftp-openapi-doc) provides the **OpenAPI** specification for **CBFTP** in **two languages**:

- **[`cbftp-openapi_fr.yaml`](./cbftp-openapi_fr.yaml)** : **French** version  
- **[`cbftp-openapi_en.yaml`](./cbftp-openapi_en.yaml)** : **English** version

#### Scope of the Documentation

1. **REST Endpoints** (`/sites`, `/spreadjobs`, `/transferjobs`, etc.)  
2. **Data Schemas** (Site, Section, SkiplistRule, SpreadJob, etc.)  
3. **Security** (HTTP Basic Auth) and UDP API notes (non-HTTP, thus out of scope for OpenAPI)  
4. **TLS settings**, **limits**, etc.

#### Version and Changelog

- The `info.version` field in the YAML files indicates the **spec version** (e.g., `1.3.0`).  
- We currently use **OpenAPI 3.0.3** for broader compatibility with Swagger Editor.  
- Consider keeping track of changes in a [CHANGELOG.md](./CHANGELOG.md) *(to be created)* or via GitHub tags (e.g., `v1.3.0`).

### How to View

1. **Swagger Editor**  
   - Go to [editor.swagger.io](https://editor.swagger.io/).  
   - Copy-paste `cbftp-openapi_en.yaml` into the left pane for an **English** interactive doc.

2. **Redoc CLI**  
   ```bash
   npm install -g redoc-cli
   redoc-cli serve cbftp-openapi_en.yaml
   ```
   Then open `http://127.0.0.1:8080` in your browser.

3. **Docker + Swagger UI**  
   - Pull the [swaggerapi/swagger-ui](https://hub.docker.com/r/swaggerapi/swagger-ui) image.  
   - Mount your local YAML file into the container, then open it in your browser.

4. *(Optional)* **GitHub Pages**  
   - You may **host** the rendered documentation via GitHub Pages, generating static HTML using [Redoc](https://redocly.com/redoc/) or [Swagger UI](https://swagger.io/tools/swagger-ui/).

### Validation & Local Testing

- Install **Swagger CLI**:
  ```bash
  npm install -g swagger-cli
  ```
- Validate syntax:
  ```bash
  swagger-cli validate cbftp-openapi_en.yaml
  swagger-cli validate cbftp-openapi_fr.yaml
  ```
- Optionally, add a **GitHub Action** (e.g., `.github/workflows/validate.yml`) to run these checks on every push/pull request.

### REST Call Examples

<details>
  <summary>cURL example to list sites</summary>

```bash
curl -k -u :bestpass https://localhost:55477/sites
```
</details>

<details>
  <summary>Postman Collection example</summary>

You can import a `postman_collection.json` file with preconfigured requests (Basic auth, URLs, etc.). Remember to disable SSL certificate verification in Postman if using a self-signed certificate.

</details>

### Contributing

1. **Fork** this repo and create a **branch** (e.g. `feat/add-transferjob-endpoint`).  
2. Update `cbftp-openapi_en.yaml` or `cbftp-openapi_fr.yaml`.  
3. Validate with `swagger-cli` or [editor.swagger.io](https://editor.swagger.io/).  
4. Open a **pull request** to discuss/merge changes.

*(See [CONTRIBUTING.md](./CONTRIBUTING.md) for more details if needed.)*

---

## Licence

Ce dépôt est sous licence [MIT](./LICENSE).  
*(English: This repository is licensed under the [MIT License](./LICENSE).)*

---

## Aide / Support

- Ouvrez une **issue** pour poser une question, signaler un problème ou proposer une amélioration.
- Consultez la documentation interne de **CBFTP** pour plus de détails sur l’API UDP ou d’autres fonctionnalités avancées.

**Merci / Thanks** pour votre intérêt dans CBFTP et son API REST !  
N’hésitez pas à [nous contacter](../../issues) ou à contribuer. 
