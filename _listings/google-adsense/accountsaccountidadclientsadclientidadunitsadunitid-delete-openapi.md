---
swagger: "2.0"
x-collection-name: Google Adsense
x-complete: 0
info:
  title: Google Adsense API Delete Ad Unit
  version: 1.0.0
  description: Delete the specified ad unit from the specified publisher AdSense account.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{accountId}/adclients/{adClientId}/adunits:
    get:
      summary: Get Ad Units
      description: List all ad units in the specified publisher's AdSense account.
      operationId: adsensehost.accounts.adunits.list
      x-api-path-slug: accountsaccountidadclientsadclientidadunits-get
      parameters:
      - in: path
        name: accountId
        description: Account which contains the ad client
      - in: path
        name: adClientId
        description: Ad client for which to list ad units
      - in: query
        name: includeInactive
        description: Whether to include inactive ad units
      - in: query
        name: maxResults
        description: The maximum number of ad units to include in the response, used
          for paging
      - in: query
        name: pageToken
        description: A continuation token, used to page through ad units
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
    patch:
      summary: Update Ad Units
      description: Update the supplied ad unit in the specified publisher AdSense
        account. This method supports patch semantics.
      operationId: adsensehost.accounts.adunits.patch
      x-api-path-slug: accountsaccountidadclientsadclientidadunits-patch
      parameters:
      - in: path
        name: accountId
        description: Account which contains the ad client
      - in: path
        name: adClientId
        description: Ad client which contains the ad unit
      - in: query
        name: adUnitId
        description: Ad unit to get
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
    post:
      summary: Create Ad Unit
      description: Insert the supplied ad unit into the specified publisher AdSense
        account.
      operationId: adsensehost.accounts.adunits.insert
      x-api-path-slug: accountsaccountidadclientsadclientidadunits-post
      parameters:
      - in: path
        name: accountId
        description: Account which will contain the ad unit
      - in: path
        name: adClientId
        description: Ad client into which to insert the ad unit
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
    put:
      summary: Update Ad Unit
      description: Update the supplied ad unit in the specified publisher AdSense
        account.
      operationId: adsensehost.accounts.adunits.update
      x-api-path-slug: accountsaccountidadclientsadclientidadunits-put
      parameters:
      - in: path
        name: accountId
        description: Account which contains the ad client
      - in: path
        name: adClientId
        description: Ad client which contains the ad unit
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
  /accounts/{accountId}/adclients/{adClientId}/adunits/{adUnitId}:
    delete:
      summary: Delete Ad Unit
      description: Delete the specified ad unit from the specified publisher AdSense
        account.
      operationId: adsensehost.accounts.adunits.delete
      x-api-path-slug: accountsaccountidadclientsadclientidadunitsadunitid-delete
      parameters:
      - in: path
        name: accountId
        description: Account which contains the ad unit
      - in: path
        name: adClientId
        description: Ad client for which to get ad unit
      - in: path
        name: adUnitId
        description: Ad unit to delete
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
    get:
      summary: Get Ad Unit
      description: Get the specified host ad unit in this AdSense account.
      operationId: adsensehost.accounts.adunits.get
      x-api-path-slug: accountsaccountidadclientsadclientidadunitsadunitid-get
      parameters:
      - in: path
        name: accountId
        description: Account which contains the ad unit
      - in: path
        name: adClientId
        description: Ad client for which to get ad unit
      - in: path
        name: adUnitId
        description: Ad unit to get
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
  /accounts/{accountId}/adclients/{adClientId}/adunits/{adUnitId}/adcode:
    get:
      summary: Get Ad Unit Code
      description: Get ad code for the specified ad unit, attaching the specified
        host custom channels.
      operationId: adsensehost.accounts.adunits.getAdCode
      x-api-path-slug: accountsaccountidadclientsadclientidadunitsadunitidadcode-get
      parameters:
      - in: path
        name: accountId
        description: Account which contains the ad client
      - in: path
        name: adClientId
        description: Ad client with contains the ad unit
      - in: path
        name: adUnitId
        description: Ad unit to get the code for
      - in: query
        name: hostCustomChannelId
        description: Host custom channel to attach to the ad code
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Units
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