# CBFTP OpenAPI Documentation

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![OpenAPI Version](https://img.shields.io/badge/OpenAPI-3.0.3-orange.svg)](#)

> **Langues / Languages** :
> - [Français](#fr)
> - [English](#en)

---

## Sommaire / Table of Contents

1. [Structure du Dépôt / Repository Structure](#structure-du-dépôt--repository-structure)
2. [Version FR](#fr---spécification-openapi)
3. [Version EN](#en---openapi-specification)
4. [Licence / License](#licence--license)

---

## Structure du Dépôt / Repository Structure

- [`cbftp-openapi_fr.yaml`](./cbftp-openapi_fr.yaml)  
  *Spécification OpenAPI en **français** (version 3.0.3).*
- [`cbftp-openapi_en.yaml`](./cbftp-openapi_en.yaml)  
  *OpenAPI specification in **English** (version 3.0.3).*
- [`postman_collection_fr.json`](./postman_collection_fr.json)  
  *Collection Postman en **français** pour tester l’API.*
- [`postman_collection_en.json`](./postman_collection_en.json)  
  *Postman collection in **English** for API testing.*
- [`readme.md`](./readme.md)  
  *(This file)*

---

## <a name="fr"></a>FR - Spécification OpenAPI

### Description

Ce projet contient la spécification **OpenAPI** de **CBFTP** en deux langues :
- **[`cbftp-openapi_fr.yaml`](./cbftp-openapi_fr.yaml)** (français)
- **[`cbftp-openapi_en.yaml`](./cbftp-openapi_en.yaml)** (anglais)

La spécification décrit :
1. Les **Endpoints REST** (ex. `/sites`, `/spreadjobs`, `/transferjobs`, etc.)  
2. Les **Schémas** (`Site`, `Section`, `SkiplistRule`, etc.)  
3. La **Sécurité** (HTTP Basic Auth) et l’**API UDP** (hors-scope OpenAPI)  
4. Les **Paramètres TLS**, **limites** et configurations associées

### Visualiser en Local

1. **Swagger Editor**  
   - Allez sur [editor.swagger.io](https://editor.swagger.io/).  
   - Copiez le contenu de `cbftp-openapi_fr.yaml` (ou uploadez le fichier) dans la fenêtre de gauche.  
   - Visualisez la documentation interactive à droite.

2. **Redoc CLI**  
   ```bash
   npm install -g redoc-cli
   redoc-cli serve cbftp-openapi_fr.yaml
   ```
   Ouvrez ensuite `http://127.0.0.1:8080`.

3. **Docker + Swagger UI**  
   - Téléchargez l’image [swaggerapi/swagger-ui](https://hub.docker.com/r/swaggerapi/swagger-ui).  
   - Montez votre fichier YAML et accédez-y dans votre navigateur.

### Exemple Postman (FR)

- [`postman_collection_fr.json`](./postman_collection_fr.json)  
  Importez ce fichier dans Postman pour **tester rapidement** l’API.  
  Pensez à désactiver la vérification SSL si vous utilisez un certificat auto-signé (Settings -> General -> **SSL certificate verification: OFF**).

---

## <a name="en"></a>EN - OpenAPI Specification

### Description

This repository provides the **OpenAPI** specification for **CBFTP** in two languages:
- **[`cbftp-openapi_fr.yaml`](./cbftp-openapi_fr.yaml)** (French)
- **[`cbftp-openapi_en.yaml`](./cbftp-openapi_en.yaml)** (English)

It covers:
1. **REST Endpoints** (`/sites`, `/spreadjobs`, `/transferjobs`, etc.)  
2. **Data Schemas** (`Site`, `Section`, `SkiplistRule`, etc.)  
3. **Security** (HTTP Basic Auth) and the **UDP API** (outside OpenAPI scope)  
4. **TLS settings**, **limits**, etc.

### View Locally

1. **Swagger Editor**  
   - Go to [editor.swagger.io](https://editor.swagger.io/).  
   - Copy-paste or upload `cbftp-openapi_en.yaml` into the left pane.  
   - Check the interactive documentation on the right side.

2. **Redoc CLI**  
   ```bash
   npm install -g redoc-cli
   redoc-cli serve cbftp-openapi_en.yaml
   ```
   Then open `http://127.0.0.1:8080`.

3. **Docker + Swagger UI**  
   - Pull [swaggerapi/swagger-ui](https://hub.docker.com/r/swaggerapi/swagger-ui).  
   - Mount your YAML file in the Docker container and open in your browser.

### Postman Example (EN)

- [`postman_collection_en.json`](./postman_collection_en.json)  
  Import it into Postman to quickly **test the API** in English.  
  Disable SSL certificate verification if using a self-signed cert (Settings -> General -> **SSL certificate verification: OFF**).

---

## <a name="licence"></a>Licence / License

Ce dépôt est sous licence [MIT](./LICENSE).  
*(English: This repository is licensed under the [MIT License](./LICENSE).)*

---

**Merci** pour votre intérêt pour **CBFTP** et son API REST.  
Pour toute question ou suggestion, ouvrez une **issue** ou consultez la documentation interne CBFTP.  
*(English: Thank you for your interest in CBFTP and its REST API. For questions or suggestions, open an issue or refer to the internal CBFTP documentation.)*

---
