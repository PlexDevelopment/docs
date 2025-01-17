---
id: httpd
title: HTTPD
---

# HTTPD

The HTTPD module sets up a basic web server to display information from Plex.

## Endpoints

The endpoints are what allow you to query the server and see information. All endpoints are formatted in JSON.

### /api/commands

This endpoint shows a list of registered commands on the server. It is an automatically generated help page. It is up to
plugin authors to provide accurate information about their plugins and the commands they provide.

### /api/indefbans

Displays a list of indefinite players in JSON format. This page is only accessible if your IP address is linked to an
admin on the server. If your server is using permissions, it will check if the player has the
`plex.httpd.indefbans.access` instead.

### /api/list

This will display a list of online players in JSON format. This is accessible to everyone.

### /api/punishments

If you go this page, it will ask you to enter a UUID in the URL. When you enter a valid UUID to the URL, it will display
that user's punishments in JSON format. An example URL would be `/api/punishments/78408086-1991-4c33-a571-d8fa325465b2`.
If your IP is not registered to an admin, it will not display IP addresses. If your server is using permissions, it will
check if the player has the `plex.httpd.punishments.access` instead.

### /api/schematics/download

This page allows anyone to download schematics from the server. No permission is required to access the page

### /api/schematics/upload

This page allows players who are an Admin or above to upload schematics. The corresponding permission to upload
schematics is `plex.httpd.schematics.upload`
