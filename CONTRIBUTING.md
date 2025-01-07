# Guide de Contribution / Contribution Guide

*(FR ci-dessous / EN below)*

---

## FR - Guide de Contribution

Merci de l’intérêt que vous portez au projet **CBFTP - OpenAPI** !  
Voici comment contribuer efficacement :

1. **Forkez** le dépôt [ZarTek-Creole/cbftp-openapi-doc](https://github.com/ZarTek-Creole/cbftp-openapi-doc).
2. **Clonez** votre fork en local :
   ```bash
   git clone https://github.com/<votre-user>/cbftp-openapi-doc.git
   ```
3. **Créez** une branche décrivant votre contribution :
   ```bash
   git checkout -b feat/mon-amélioration
   ```
4. **Modifiez** le fichier YAML approprié :
   - `cbftp-openapi_fr.yaml` (version française)
   - `cbftp-openapi_en.yaml` (version anglaise)
5. **Validez** votre modification :
   ```bash
   npm install -g swagger-cli
   swagger-cli validate cbftp-openapi_fr.yaml
   # ou
   swagger-cli validate cbftp-openapi_en.yaml
   ```
   Assurez-vous qu’aucune erreur n’est détectée.
6. **Commitez** et poussez vos changements sur votre branche :
   ```bash
   git add .
   git commit -m "Amélioration de la doc FR"
   git push origin feat/mon-amélioration
   ```
7. **Ouvrez** une Pull Request (PR) sur le dépôt original :
   - Décrivez clairement ce que vous avez changé et pourquoi.

Une fois la PR ouverte, les mainteneurs examineront vos modifications et pourront demander des ajustements avant de fusionner vos contributions.

### Recommandations

- Respectez la **convention de nommage** pour les branches (ex. `feat/...`, `fix/...`, `docs/...`).
- Vérifiez bien l’**indentation** YAML et la **cohérence** de la documentation (ex. pas de duplications dans `info.description`).
- Si vous modifiez la version dans `info.version`, pensez à mettre à jour le [CHANGELOG.md](./CHANGELOG.md) et/ou créer un tag Git si c’est une version majeure.

---

## EN - Contribution Guide

Thank you for your interest in the **CBFTP - OpenAPI** project!  
Below is how you can contribute effectively:

1. **Fork** the repository [ZarTek-Creole/cbftp-openapi-doc](https://github.com/ZarTek-Creole/cbftp-openapi-doc).
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<your-username>/cbftp-openapi-doc.git
   ```
3. **Create** a branch describing your contribution:
   ```bash
   git checkout -b feat/my-improvement
   ```
4. **Edit** the relevant YAML file:
   - `cbftp-openapi_en.yaml` (English version)
   - `cbftp-openapi_fr.yaml` (French version)
5. **Validate** your changes:
   ```bash
   npm install -g swagger-cli
   swagger-cli validate cbftp-openapi_en.yaml
   # or
   swagger-cli validate cbftp-openapi_fr.yaml
   ```
   Make sure there are no errors.
6. **Commit** and push your changes:
   ```bash
   git add .
   git commit -m "Improve English doc"
   git push origin feat/my-improvement
   ```
7. **Open** a Pull Request (PR) to the original repo:
   - Clearly describe what you changed and why.

The maintainers will review your PR and may request adjustments before merging.

### Recommendations

- Follow a **branch naming convention** (e.g., `feat/...`, `fix/...`, `docs/...`).
- Verify **YAML indentation** and **documentation consistency** (e.g. no duplicates in `info.description`).
- If you change `info.version`, consider updating [CHANGELOG.md](./CHANGELOG.md) and/or creating a Git tag if it’s a major release.
