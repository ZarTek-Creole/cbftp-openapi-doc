# CBFTP API Endpoints

This document provides a list of all available endpoints in the CBFTP API.

## Sites

- `GET /sites`: List all sites
- `POST /sites`: Create a new site
- `GET /sites/{siteName}`: Get site information
- `PATCH /sites/{siteName}`: Update a site
- `DELETE /sites/{siteName}`: Delete a site

## Sites -> Sections

- `GET /sites/{siteName}/sections`: List sections of a site
- `POST /sites/{siteName}/sections`: Add a section to a site
- `GET /sites/{siteName}/sections/{sectionName}`: Get details of a specific section
- `PATCH /sites/{siteName}/sections/{sectionName}`: Update a section
- `DELETE /sites/{siteName}/sections/{sectionName}`: Delete a section

## SpreadJobs

- `GET /spreadjobs`: List all spread jobs
- `POST /spreadjobs`: Create a new spread job
- `GET /spreadjobs/{jobName}`: Get detailed info of a spread job
- `POST /spreadjobs/{jobName}?action=abort/reset`: Perform actions on an existing spread job (abort, reset, etc.)

## TransferJobs

- `GET /transferjobs`: List transfers
- `POST /transferjobs`: Create a new transfer
- `GET /transferjobs/{transferId}`: Get details of a specific transfer
- `POST /transferjobs/{transferId}?action=abort/reset`: Perform actions on an existing transfer (abort, reset, etc.)

## Path

- `GET /path`: List a directory
- `DELETE /path`: Delete a directory

## File

- `GET /file`: Display a file

## Raw

- `POST /raw`: Send a raw command

## Info

- `GET /info`: Display various CBFTP information
