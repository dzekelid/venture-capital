---
swagger: "2.0"
x-collection-name: Backupify
x-complete: 1
info:
  title: Backupify
  description: the-backupify-api-allows-you-to-integrate-the-leading-saas-backup-solution-into-your-software-making-it-easy-to-give-your-customers-the-data-protection-they-need--
  version: 1.0.0
host: api.backupify.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/authenticate_vendor:
    get:
      summary: A simple method to test authentication of a vendor access token. The
        response body is empty JSON object.
      description: A simple method to test authentication of a vendor access token.
        the response body is empty json object..
      operationId: getV1AuthenticateVendor
      x-api-path-slug: v1authenticate-vendor-get
      parameters:
      - in: header
        name: Authorization
        description: Bearer Access Token granted from client_credentials for vendor
      responses:
        200:
          description: OK
      tags:
      - V1
      - Authenticate
      - Vendor
---