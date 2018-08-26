---
swagger: "2.0"
x-collection-name: Actility
x-complete: 1
info:
  title: ThingPark DX Maker API
  description: api-providing-features-for-device-makers-such-as-preprovisioning-on-standalone-join-servers-
  version: 1.0.0
host: dx-api.thingpark.com
basePath: /maker/v011/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /appKeyGens:
    post:
      summary: AppKey generation
      description: Generate some encrypted VendorKeys with an HSM. Encrypted VendorKeys
        can be decrypted with the private part of provided RSA key. A VendorKey is
        a concatenation of an AppKey (128 bits) and hsmEncryptedAppKey (128 bits).
      operationId: generate-some-encrypted-vendorkeys-with-an-hsm-encrypted-vendorkeys-can-be-decrypted-with-the-privat
      x-api-path-slug: appkeygens-post
      parameters:
      - in: body
        name: appKeyGen
        description: Configuration for AppKey generation
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: number
        description: Define the number of AppKey generated
      responses:
        200:
          description: OK
      tags:
      - AppKey
      - Generation
---