# Usage in English

This section explains how to configure the API, main endpoints, etc.

## Key Endpoints
- `/sites` ...
- `/spreadjobs` ...
- ...

## General Instructions

To use the CBFTP API, you must include HTTP Basic authentication (username:password) encoded in Base64 in all requests. For example, if the password is `bestpass`, the header should be:

```
Authorization: Basic OmJlc3RwYXNz
```

### Example REST Calls

#### List Sites

```bash
curl -k -u :bestpass https://localhost:55477/sites
```

#### Send a Raw Command

```bash
curl -k -u :bestpass -X POST https://localhost:55477/raw -d '{
  "command": "site deluser me",
  "sites": ["SITE1"]
}'
```

#### Add a Site

```bash
curl -k -u :bestpass -X POST https://localhost:55477/sites -d @newsite.json
```

## HTTP Methods

- **GET**: Read an existing resource
- **POST**: Create a new resource
- **PATCH**: Update an existing resource
- **DELETE**: Delete a resource

## Main Endpoints

- `/sites` (list/add); `/sites/{siteName}` (details/update/delete)
- `/sites/{siteName}/sections` (list/add); `/sites/{siteName}/sections/{sectionName}` (details/update/delete)
- `/raw`: Execute a raw command (`POST`)
- `/spreadjobs` (list/create); `/spreadjobs/{jobName}` (details/abort/reset)
- `/transferjobs` (list/create); `/transferjobs/{transferId}` (details/abort/reset)
- `/path`: List or delete a directory
- `/file`: Retrieve the content of a file
- `/info`: Build info, stats, configuration
