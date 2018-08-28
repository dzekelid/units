---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Create a unit
  description: Creates a unit.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/items/units:
    get:
      summary: List units
      description: Lists all units.
      operationId: getRestItemsUnits
      x-api-path-slug: restitemsunits-get
      parameters:
      - in: query
        name: updatedAt
        description: Filter restricts the list of results to items updated after the
          specified date
      responses:
        200:
          description: OK
      tags:
      - List
      - Units
    post:
      summary: Create a unit
      description: Creates a unit.
      operationId: postRestItemsUnits
      x-api-path-slug: restitemsunits-post
      parameters:
      - in: body
        name: /rest/items/units
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Unit
  /rest/items/units/{id}:
    delete:
      summary: Delete a unit
      description: Deletes a unit. The ID of the unit must be specified.
      operationId: deleteRestItemsUnits
      x-api-path-slug: restitemsunitsid-delete
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Unit
    get:
      summary: Get a unit
      description: Gets a unit. The ID of the unit must be specified.
      operationId: getRestItemsUnits
      x-api-path-slug: restitemsunitsid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Unit
    put:
      summary: Update a unit
      description: Updates a unit. The ID of the unit must be specified.
      operationId: putRestItemsUnits
      x-api-path-slug: restitemsunitsid-put
      parameters:
      - in: body
        name: /rest/items/units/{id}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Unit
  /rest/items/units/{id}/names:
    get:
      summary: List unit names
      description: Lists the unit names of a unit. The ID of the unit must be specified.
      operationId: getRestItemsUnitsNames
      x-api-path-slug: restitemsunitsidnames-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - List
      - Unit
      - Names
    post:
      summary: Create a unit name
      description: Creates a unit name. The ID of the unit and the language must be
        specified.
      operationId: postRestItemsUnitsNames
      x-api-path-slug: restitemsunitsidnames-post
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Unit
      - Name
  /rest/items/units/{id}/names/{lang}:
    delete:
      summary: Delete a unit name
      description: Deletes a unit name. The ID of the unit and the language must be
        specified.
      operationId: deleteRestItemsUnitsNamesLang
      x-api-path-slug: restitemsunitsidnameslang-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Unit
      - Name
    get:
      summary: Get a unit name
      description: Gets a unit name. The ID of the unit and the language must be specified.
      operationId: getRestItemsUnitsNamesLang
      x-api-path-slug: restitemsunitsidnameslang-get
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Unit
      - Name
    put:
      summary: Update a unit name
      description: Updates a unit name. The ID of the unit and the language must be
        specified.
      operationId: putRestItemsUnitsNamesLang
      x-api-path-slug: restitemsunitsidnameslang-put
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Unit
      - Name
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