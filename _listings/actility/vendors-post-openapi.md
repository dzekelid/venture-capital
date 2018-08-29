---
swagger: "2.0"
x-collection-name: Actility
x-complete: 0
info:
  title: ThingPark DX Core API Vendor creation
  description: Creates a new vendor with a primary user having all admin rights. Note
    that the vendor id can be chosen. If not fully specified, the vendor id and name
    attribute values are deduced from the primaryUser attribute values.
  version: 1.0.0
host: dx-api.thingpark.com
basePath: /core/v141/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /vendors:
    post:
      summary: Vendor creation
      description: Creates a new vendor with a primary user having all admin rights.
        Note that the vendor id can be chosen. If not fully specified, the vendor
        id and name attribute values are deduced from the primaryUser attribute values.
      operationId: creates-a-new-vendor-with-a-primary-user-having-all-admin-rights-note-that-the-vendor-id-can-be-chos
      x-api-path-slug: vendors-post
      parameters:
      - in: body
        name: vendor
        description: Contents of the vendor to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Vendor
      - Creation
  /vendors/{vendorRef}:
    get:
      summary: Vendor retrieval
      description: Retrieves the vendor corresponding to the provided vendor ref,
        if that vendor is within authorized scopes.
      operationId: retrieves-the-vendor-corresponding-to-the-provided-vendor-ref-if-that-vendor-is-within-authorized-sc
      x-api-path-slug: vendorsvendorref-get
      parameters:
      - in: path
        name: vendorRef
        description: Ref of the vendor to retrieve
      responses:
        200:
          description: OK
      tags:
      - Vendor
      - Retrieval
    put:
      summary: Vendor update
      description: Updates the vendor corresponding to the provided vendor ref, if
        that vendor is within authorized scopes.
      operationId: updates-the-vendor-corresponding-to-the-provided-vendor-ref-if-that-vendor-is-within-authorized-scop
      x-api-path-slug: vendorsvendorref-put
      parameters:
      - in: body
        name: vendor
        description: Contents of the vendor to update
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: vendorRef
        description: Ref of the vendor to update
      responses:
        200:
          description: OK
      tags:
      - Vendor
      - Update
    delete:
      summary: Vendor deletion
      description: Deletes the vendor corresponding to the provided vendor ref, if
        that vendor is within authorized scopes.
      operationId: deletes-the-vendor-corresponding-to-the-provided-vendor-ref-if-that-vendor-is-within-authorized-scop
      x-api-path-slug: vendorsvendorref-delete
      parameters:
      - in: path
        name: vendorRef
        description: Ref of the vendor to delete
      responses:
        200:
          description: OK
      tags:
      - Vendor
      - Deletion
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---